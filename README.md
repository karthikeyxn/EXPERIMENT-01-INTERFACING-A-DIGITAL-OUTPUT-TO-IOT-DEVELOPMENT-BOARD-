DATE: 05.03.2025

ROLL NO :212223040008
DEPARTMENT: B.E(CSE)
EXPERIMENT-01-INTERFACING-A-DIGITAL-OUTPUT-TO-IOT-DEVELOPMENT-BOARD
Aim: To Interface a Digital output (LED) to ARM IOT development board and write a program to blink an led
Components required: STM32 CUBE IDE, ARM IOT development board, STM programmer tool.
Theory
The full form of an ARM is an advanced reduced instruction set computer (RISC) machine, and it is a 32-bit processor architecture expanded by ARM holdings. The applications of an ARM processor include several microcontrollers as well as processors. The architecture of an ARM processor was licensed by many corporations for designing ARM processor-based SoC products and CPUs. This allows the corporations to manufacture their products using ARM architecture. Likewise, all main semiconductor companies will make ARM-based SOCs such as Samsung, Atmel, TI etc.

What is an ARM7 Processor? ARM7 processor is commonly used in embedded system applications. Also, it is a balance among classic as well as new-Cortex sequence. This processor is tremendous in finding the resources existing on the internet with excellence documentation offered by NXP Semiconductors. It suits completely for an apprentice to obtain in detail hardware & software design implementation. LPC2148 Microcontroller The LPC2148 microcontroller is designed by Philips (NXP Semiconductor) with several in-built features & peripherals. Due to these reasons, it will make more reliable as well as the efficient option for an application developer. LPC2148 is a 16-bit or 32-bit microcontroller based on ARM7 family. Features of LPC2148 The main features of LPC2148 include the following. • The LPC2148 is a 16 bit or 32 bit ARM7 family based microcontroller and available in a small LQFP64 package. • ISP (in system programming) or IAP (in application programming) using on-chip boot loader software. • On-chip static RAM is 8 kB-40 kB, on-chip flash memory is 32 kB-512 kB, the wide interface is 128 bit, or accelerator allows 60 MHz high-speed operation. • It takes 400 milliseconds time for erasing the data in full chip and 1 millisecond time for 256 bytes of programming. • Embedded Trace interfaces and Embedded ICE RT offers real-time debugging with high-speed tracing of instruction execution and on-chip Real Monitor software. • It has 2 kB of endpoint RAM and USB 2.0 full speed device controller. Furthermore, this microcontroller offers 8kB on-chip RAM nearby to USB with DMA. • One or two 10-bit ADCs offer 6 or 14 analogs i/ps with low conversion time as 2.44 μs/ channel. • Only 10 bit DAC offers changeable analog o/p. • External event counter/32 bit timers-2, PWM unit, & watchdog. • Low power RTC (real time clock) & 32 kHz clock input. • Several serial interfaces like two 16C550 UARTs, two I2C-buses with 400 kbit/s speed. • 5 volts tolerant quick general purpose Input/output pins in a small LQFP64 package. • Outside interrupt pins-21. • 60 MHz of utmost CPU CLK-clock obtainable from the programmable-on-chip phase locked loop by resolving time is 100 μs. • The incorporated oscillator on the chip will work by an exterior crystal that ranges from 1 MHz-25 MHz • The modes for power-conserving mainly comprise idle & power down. • For extra power optimization, there are individual enable or disable of peripheral functions and peripheral CLK scaling.

Procedure:
click on STM 32 CUBE IDE, the following screen will appear image

click on FILE, click on new stm 32 project image image

select the target to be programmed as shown below and click on next

image

4.select the program name image

corresponding ioc file will be generated automatically image
6.select the appropriate pins as gipo, in or out, USART or required options and configure image image

7.click on cntrl+S , automaticall C program will be generated image image 8. edit the program and as per required image

use project and build all image

once the project is bulild image

click on debug option image

connect the stm nucleo board and click on run image

STM 32 CUBE PROGRAM :
#include "main.h"
#include "stdio.h"
int main(void)
{
  while (1)
  {
    HAL_GPIO_WritePin(GPIOA,GPIO_PIN_0, GPIO_PIN_RESET);
    HAL_Delay(1000);
    HAL_GPIO_WritePin(GPIOA,GPIO_PIN_0, GPIO_PIN_SET);
    HAL_Delay(1000);
  }
}
OUTPUT :
419323363-3f6ba13f-40d0-40d3-afdb-d0fe498cc5bc 419323401-8001bdee-61f2-4925-a896-07378fd2d000

Result :
Interfacing a digital output with ARM microcontroller based IOT development is executed and the results are verified.
