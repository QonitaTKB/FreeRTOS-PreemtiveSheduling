Exercise 4 - Gain a good understanding of task behaviour where a priority preemptive scheduling policy is used.
This project demonstrates the use of FreeRTOS on an STM32F103C8T6 microcontroller to execute multiple tasks controlling LEDs. The system consists of two main tasks responsible for turning on the green and red LEDs in specific patterns, along with one additional default task. Each function is handled in a separate task scheduled by FreeRTOS, enabling multitasking in a real-time environment.
Diagram Task:
Required Hardware:

STM32F103C8T6
LEDs
Required Software:

STM32CubeIDE
FreeRTOS
How it Works:

Task FlashGreenLedTask controls the green LED with the following pattern:

The green LED blinks at 0.5-second intervals, and after blinking 8 times (totaling 4 seconds), the LED turns off, and the task enters a delay of 6 seconds.
The total periodicity for this task is 10 seconds.
Task FlashRedLedTask controls the red LED with the following pattern:

The red LED blinks rapidly at 50ms intervals, and after blinking 10 times (totaling 0.5 seconds), the LED turns off, and the task enters a delay of 1.5 seconds.
The total periodicity for this task is 2 seconds.
Task Priorities:

Task FlashRedLedTask has a higher priority than Task FlashGreenLedTask, so it will preempt the green LED task when scheduled.

Demo Video:
