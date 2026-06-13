# STM32 UART VCP (USB CDC)

This project demonstrates USB Virtual COM Port (VCP) communication using the STM32L052K8Tx microcontroller. The board is configured as a USB CDC device, allowing a PC to communicate with the STM32 as if it were a serial COM port.

The project continuously reads analog data using ADC with DMA, converts it into temperature values, and transmits the results to the PC through USB CDC. Temperature information is also displayed on a 16×2 I2C LCD.

## Features

* USB CDC (Virtual COM Port) communication
* ADC data acquisition with DMA
* Real-time temperature measurement
* Serial data transmission to PC
* 16×2 LCD interfacing via I2C
* Continuous data monitoring
* HAL library-based implementation
* Developed using STM32CubeIDE

## Hardware Used

* STM32L052K8Tx (NUCLEO-L052K8)
* USB Cable
* 16×2 LCD with I2C Backpack
* Potentiometer (Analog Input)
* Jumper Wires
* Breadboard

## Software Used

* STM32CubeIDE
* STM32 HAL Drivers
* STM32 USB Device Middleware
* Serial Terminal Software (Tera Term, PuTTY, Hercules)

## Peripherals Used

| Peripheral | Purpose                                      |
| ---------- | -------------------------------------------- |
| USB CDC    | Virtual COM Port Communication               |
| ADC1       | Analog Data Acquisition                      |
| DMA1       | Automatic ADC Data Transfer                  |
| I2C1       | LCD Communication                            |
| USART1     | UART Communication (available for expansion) |
| GPIO       | Input and Output Control                     |

## Working Principle

1. The STM32 initializes USB CDC and enumerates as a Virtual COM Port.
2. ADC1 continuously samples the analog signal.
3. DMA transfers ADC values to memory automatically.
4. The ADC value is converted into temperature.
5. Temperature values are transmitted to the PC via USB CDC.
6. The same data is displayed on the I2C LCD.

## Example Serial Output

```text id="qdbqkh"
Temp: 23

Temp: 24

Temp: 25

Temp: 26
```

## LCD Display

```text id="5q22gi"
Room Temp Cont
```

## Pin Configuration

### Analog Input

| Pin | Function      |
| --- | ------------- |
| PA0 | ADC Channel 0 |

### I2C LCD

| STM32 Pin | Function |
| --------- | -------- |
| PB6       | I2C1_SCL |
| PB7       | I2C1_SDA |

### User Button

| Pin | Function     |
| --- | ------------ |
| PB0 | Input Button |

### Output Pin

| Pin | Function   |
| --- | ---------- |
| PB3 | LED Output |

## Project Structure

```text id="oh7jys"
STM32_UART_VCP
│
├── Core
│   ├── Inc
│   └── Src
├── Drivers
├── USB_Device
├── Middlewares
├── STM32_UART_VCP.ioc
├── .project
├── .cproject
├── README.md
├── LICENSE
└── .gitignore
```

## Applications

* USB Serial Communication
* Sensor Data Logging
* PC-to-Microcontroller Communication
* Embedded Monitoring Systems
* Industrial Automation
* IoT Applications
* Debugging and Diagnostics

## Target MCU

* STM32L052K8Tx

## Communication Interfaces

* USB CDC (Virtual COM Port)
* I2C
* UART
* ADC with DMA

## IDE

* STM32CubeIDE

## Author

**Yash Mane**

## License

This project is licensed under the MIT License.
