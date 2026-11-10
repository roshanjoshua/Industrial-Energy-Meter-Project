# Industrial-Energy-Meter-Project
The Industrial Energy Meter with Data Logger is an embedded-based power monitoring system designed to measure, calculate, display, and record the electrical parameters of an industrial load in real time. The system is developed using the STM32F446RE ARM Cortex-M4 microcontroller, programmed using Embedded C and STM32 HAL libraries. It monitors essential electrical parameters such as AC voltage, current, active power, apparent power, power factor, frequency, and accumulated energy consumption.

The hardware consists of a ZMPT101B voltage sensor for isolated AC voltage measurement and an appropriate current sensor, such as the ACS712 or a suitably rated CT sensor, for measuring load current. The sensor outputs are connected to the STM32's ADC channels, where the microcontroller samples the analog signals and processes them using digital signal calculations. RMS voltage and current are calculated from sampled waveforms, while active power is determined by averaging instantaneous voltage-current products. Power factor and energy consumption are subsequently derived from these measurements.

A 16×2 LCD with an I2C interface is integrated to display real-time electrical parameters while minimizing GPIO usage. An RTC module (DS3231) maintains accurate timestamps, and an SPI-based microSD card module provides non-volatile storage for recorded measurements. The firmware periodically logs voltage, current, power, power factor, frequency, and energy consumption along with timestamps in CSV format for subsequent analysis.

The STM32 peripherals utilized include ADC for sensor acquisition, I2C for LCD and RTC communication, SPI for SD card interfacing, UART for debugging and optional serial monitoring, DMA for efficient ADC sampling, and hardware timers for precise sampling intervals and periodic data logging.

Additional firmware features include threshold-based overcurrent and overvoltage detection, configurable alarm limits, sensor calibration, and fault indication using LEDs or a buzzer. The project demonstrates practical implementation of embedded firmware, peripheral interfacing, real-time data acquisition, signal processing, file handling, and industrial electrical monitoring.


<img width="1157" height="569" alt="image" src="https://github.com/user-attachments/assets/4bc76d84-f93f-41eb-b143-54f2bfd766fe" />
