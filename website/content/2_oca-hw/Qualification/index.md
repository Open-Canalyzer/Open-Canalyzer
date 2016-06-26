---
title: Qualification
prev: /2_oca-hw
toc: true
weight: 10
---

## Hardware tools
| Abbreviation | Name            | Comment |
|--------------|-----------------|---------|
| oca1         | Open-Canalyzer  |         |
| oca2         | Open-Canalyzer  |         |
| DMM          | Voltcraft VC-60 |         |
| Scope        | Rigol DS1054Z   |         |

## Software tools
| Abbreviation      | Name                         | Comment                                 |
|-------------------|------------------------------|-----------------------------------------|
| liboca            | oca library                  |                                         |
| oca-qualification | oca qualification executable | Tool that generates USB and CAN traffic |


## Qualification setup / environment
{{% notice note %}}
Insert diagram of connection setup. <br/>Add table with variables like temperature
{{% /notice %}}

## Power supplies
First check for shorts on each power supply net using the DMM.

| Name              | Min     | Max | Measured | Pass/Fail |
|-------------------|---------|-----|----------|-----------|
| VUSB -> GND       | 10k Ohm | INF |          |           |
| 5V_ISO -> GND_ISO | 10k Ohm | INF |          |           |
| 3V3(VCC) -> GND   | 10k Ohm | INF |          |           |

### 5V USB input
#### Output voltage
| Name              | Min   | Max   | Measured | Pass/Fail |
|-------------------|-------|-------|----------|-----------|
| VUSB -> GND       | 4.40V | 5.25V |          |           |
#### Noise
#### Startup and shutdown

### 5V Isolated
#### Output voltage
| Name              | Min   | Max   | Measured | Pass/Fail |
|-------------------|-------|-------|----------|-----------|
| 5V_ISO -> GND_ISO | 4.85V | 5.15V |          |           |
#### Isolation resistance
| Name            | Min       | Max   | Measured | Pass/Fail |
|-----------------|-----------|-------|----------|-----------|
| VUSB -> 5V_ISO  | 1000 Mohm | INF   |          |           |
| GND  -> GND_ISO | 1000 Mohm | INF   |          |           |

#### Noise
#### Ripple
#### Startup and shutdown
#### Thermal image

### 3V3
#### Output voltage
| Name              | Min    | Max    | Measured | Pass/Fail |
|-------------------|--------|--------|----------|-----------|
| 3V3(VCC) -> GND   | 3.235V | 3.365V |          |           |
#### Noise
#### Ripple
#### Startup and shutdown
#### Thermal image

## Clocks
### 8MHz oscillator
| Name      | Min       | Max      | Measured | Pass/Fail |
|-----------|-----------|----------|----------|-----------|
| Frequency | 7.992 MHz | 8.008 MHz|          |           |
| Jitter    |           |          |          |           |
| Rise time |           |          |          |           |
| Fall time |           |          |          |           |

## CAN
### Termination
### Signal integrity
#### CAN_TX / CAN_RX
#### CAN_H / CAN_L

## USB
### Signal integrity
#### USB_DP / USB_DN