# Occupancy Counter using IR Sensor, Slide Switch, OLED and NeoPixel

## Project Overview

This project counts object/person detection using an IR sensor.
Count is displayed on OLED and reset is controlled using a slide switch.

## Components Used

* STM32 Nucleo Board
* IR Sensor
* Slide Switch
* NeoPixel LED Ring (WS2812)
* OLED Display (SSD1306 I2C)

## Pin Configuration

* IR Sensor → PB10
* Slide Switch → PB0
* NeoPixel → PB4 (TIM3 CH1 PWM Output)
* OLED SDA → PB9
* OLED SCL → PB8

## Working Principle

* IR sensor detects object crossing.

* Count increments for every detection.

* OLED displays COUNT and current value.

* NeoPixel glows during counting.

* Slide switch resets count.

* OLED displays RESET and 0.

* NeoPixel turns OFF.

## Software Configuration

* PB10 configured as GPIO Input
* PB0 configured as GPIO Input Pull-up
* TIM3 PWM used for NeoPixel
* I2C1 used for OLED display

## Output

* Counter increases from 0 to 9
* Reset returns count to zero

## Real Life Application

Used in room occupancy counting, visitor counting, and entrance monitoring systems.

## Files Included

* main.c
* ssd1306.c
* ssd1306.h
