# Exercise 4: Understanding Task Behaviour with Priority Preemptive Scheduling

This project demonstrates the use of FreeRTOS on an STM32F410RBTX microcontroller to execute multiple tasks controlling LEDs. The system consists of two main tasks responsible for turning on the green and red LEDs in specific patterns, along with one additional default task. Each function is handled in a separate task scheduled by FreeRTOS, enabling multitasking in a real-time environment.

---

## **Diagram Task**
![image](https://github.com/user-attachments/assets/483f38e5-9bb8-42e1-9f0b-d4232bd0ca2f)


---

## **Required Hardware**
- STM32F410RBTX
- LEDs (Green and Red)

---

## **Required Software**
- STM32CubeIDE
- FreeRTOS

---

## **How it Works**

### **Task FlashGreenLedTask**
This task controls the green LED with the following pattern:
- The green LED blinks at **0.5-second intervals**.
- After blinking **8 times** (totaling 4 seconds), the LED turns off, and the task enters a **6-second delay**.
- The total periodicity for this task is **10 seconds**.

### **Task FlashRedLedTask**
This task controls the red LED with the following pattern:
- The red LED blinks rapidly at **50ms intervals**.
- After blinking **10 times** (totaling 0.5 seconds), the LED turns off, and the task enters a **1.5-second delay**.
- The total periodicity for this task is **2 seconds**.

### **Task Priorities**
- **Task FlashRedLedTask** has a **higher priority** than **Task FlashGreenLedTask**, so it will preempt the green LED task when scheduled.


---
## **Hardware Overview**
![WhatsApp Image 2024-12-06 at 13 30 07_962163be](https://github.com/user-attachments/assets/4ac39d13-8106-4804-bd7d-c55d1a65fc15)

---
## **Demo Video**

https://github.com/user-attachments/assets/0aabec7e-3bf4-433d-b377-132583c7c307

