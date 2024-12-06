# Exercise 4: Understanding Task Behaviour with Priority Preemptive Scheduling

This project demonstrates the use of FreeRTOS on an STM32F103C8T6 microcontroller to execute multiple tasks controlling LEDs. The system consists of two main tasks responsible for turning on the green and red LEDs in specific patterns, along with one additional default task. Each function is handled in a separate task scheduled by FreeRTOS, enabling multitasking in a real-time environment.

---

## **Diagram Task**


---

## **Required Hardware**
- STM32F103C8T6
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

---
## **Demo Video**
