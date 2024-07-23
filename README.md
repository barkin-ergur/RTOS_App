# UART Interrupt-Driven Communication with FreeRTOS

This project demonstrates how to set up UART communication using interrupts on an STM32 microcontroller with FreeRTOS. The implementation includes receiving data via UART using interrupts, processing it within FreeRTOS tasks, and additional functionalities like a command-line interface (CLI), which enables a blinking LED task and periodic message sender tasks.

## Table of Contents
- [Hardware Requirements](#hardware-requirements)
- [Software Requirements](#software-requirements)
- [Setup and Usage](#setup-and-usage)

## Hardware Requirements

- NUCLEO-L476RG development board
- USB Type-A to Mini-B cable

## Software Requirements

- A serial terminal which can both transmit and receive data (e.g., Termite, PuTTY)
- STM32CubeProgrammer or STM32CubeIDE

## Setup and Usage

1. **Clone the Repository:**

    git clone https://github.com/yourusername/uart-freertos-stm32.git

2. **Using STM32CubeProgrammer:**

- Locate the FreeRTOS_Starter.bin file inside the Debug folder.
- Use STM32CubeProgrammer to upload the FreeRTOS_Starter.bin file to the microcontroller.

3. **Using STM32CubeIDE:**

- Take the entire project and open it as a project in STM32CubeIDE.
- Compile and upload the firmware to the microcontroller using the IDE.

4. **Open the Serial Terminal:**

- Open a serial terminal on your PC (e.g., PuTTY, Termite) and connect to the appropriate COM port.
- Set the baud rate to 115200.

5. **Run the Application:**

- Reset the microcontroller.
- You should see the message "UART communication has been established !!!" in the serial terminal.
- Type any message. The microcontroller should reply with "RECEIVED: YOUR MESSAGE".
- If you type "GREEN ON", the BlinkGreenLed function will be activated, and the green LED will start blinking.
- If you type "UART SENDER", the microcontroller will start sending the "TEST" message every 1 second.
