# STM32F407 Peripheral Examples

30 self-contained STM32CubeIDE projects for the **STM32F407VGT6**, each focused on one peripheral or technique. They range from GPIO and interrupts through advanced timer modes, PWM with dead-time and DMA, and finish with an ADC series for **battery voltage and temperature monitoring**, the groundwork for my [Battery Management System thesis](https://github.com/channel1umut-lang/BMS-BATTERY-MANAGEMENT-SYSTEM-Thesis).

**Tech:** C · STM32 HAL · STM32CubeMX / CubeIDE · ARM Cortex-M4

---

## 📚 Projects

### GPIO & interrupts
| # | Project | What it shows |
|---|---|---|
| 000 | [GPIO_PROCESS](000_GPIO_PROCESS) | Basic GPIO output |
| 001 | [Button_led](001_Button_led) | Reading a button, driving an LED |
| 002 | [Interrupt](002_Interrupt) | External interrupts (EXTI) |

### ADC
| # | Project | What it shows |
|---|---|---|
| 003 | [ADC_Value](003_ADC_Value) | Single-channel ADC read |
| 004 | [Real_Value_ADC_and_Multiple](004_Real_Value_ADC_and_Multiplee) | Converting raw counts to voltage, multiple channels |
| 005 | [Multiple ADC + internal temp sensor](005_Read_Multiple_ADC_Read_Internal_Tep_Sensor_Interrupt) | Scan mode, internal temperature sensor, ADC interrupt |
| 020 | [DMA_MULTI_ADC](020_DMA__MULTI_ADC) | Multi-channel ADC with DMA |

### Timers
| # | Project | What it shows |
|---|---|---|
| 006 | [Timer_Interrupt](006_Timer_Interrupt) | Periodic timer interrupt |
| 007 | [TIMER_EXT_TRIG_MODE1](007_TIMER_EXT_TRIG_MODE1) | External clock mode 1 |
| 008 | [TIMER_EXT_TRIGGER_MODE2](008_TIMER_EXT_TRIGER_MODE2) | External clock mode 2 |
| 009 | [TIMER_INTERNAL_TRIG_INPUT](009_TIMER_INTERNAL_TRIG_INPUT) | Internal trigger chaining (+ [interrupt version](009_TIMER_INTERNAL_TRIG_INPUT_INTERRUPT)) |
| 010 | [TIM_SLAVE_MODE_RESET](010_TIM_SLAVE_MODE_RESET_MODE) | Slave mode: reset |
| 011 | [TIMER_SLAVE_GATED_MODE](011_TIMER_SLAVE_GATED_MODE) | Slave mode: gated |
| 012 | [TIMER_SLAVE_TRIGGER_EXT](012_TIMER_SLAVE_TRIGGER_MODE_EXT) | Slave mode: trigger (external) |
| 013 | [TIMER_SLAVE_TRIGGER_INTERNAL](013_TIMER_SLAVE_TRIGGER_MODE_INTERNAL) | Slave mode: trigger (internal) |
| 014 | [TIMER_INPUT_CAPTURE](014_TIMER_INPUT_CAPTURE) | Measuring signal period / frequency (+ [interrupt version](015_TIMER_INPUT_CAPTURE_INTERRUPT)) |
| 016 | [TIMER_OUTPUT_COMPARE](016_TIMER_OUTPUT_COMPARE) | Output compare / toggling |

### PWM
| # | Project | What it shows |
|---|---|---|
| 017 | [PWM](017_PWM) | PWM generation |
| 018 | [PWM_POT_LED_BRIGHTNESS](018_PWM_POTANS_LED_BRIGHT) | Potentiometer (ADC) → LED brightness (PWM) |
| 019 | [PWM_COMPLEMENTARY_DEAD_TIME](019_PWM_COMLEMENTARY_DEAD_TIME) | Complementary outputs with dead-time insertion (half-bridge driving) |

### UART
| # | Project | What it shows |
|---|---|---|
| 021 | [USART_SEND_DATA](021_USART_SEND_DATA) | Transmitting data |
| 022 | [USART_RECEIVE_DATA](022_USART_RESIEVE_DATA) | Receiving data |

### Battery monitoring series
| # | Project | What it shows |
|---|---|---|
| 500 | [ADC_BATTERY_VOLT](500_ADC_BATTERY_VOLT) | Measuring a battery cell voltage |
| 501 | […_SINGLE_INTERRUPT](501_ADC_BATTERY_VOLT_SINGLE_INTERRUPT) | Interrupt-driven single cell |
| 502 | […_MULTIPLE](502_ADC_BATTERY_VOLT_MULTIPLE) | Multiple cells |
| 503 | […_MULTIPLE_INTERRUPT](503_ADC_BATTERY_VOLT_MULTIPLE_INTERRUPT) | Multiple cells, interrupt-driven |
| 504 | [MULTI_BATTERY_MULTI_TEMP_DMA](504_ADC_MULTI_BATTERY_MULTI_TEMP_SENSOR_DMA_INTERRUPT) | Multiple cells + temperature sensors with DMA |
| 505 | [ADC_BATTERY_VOLT_DIVIDER](505_ADC_BATTERY_VOLT_DEVIDER) | Measuring higher voltages through a resistor divider |

---

## ▶️ Building

Each folder is a standalone STM32CubeIDE project: **File → Import → Existing Projects into Workspace**, select the folder, then build and flash with an ST-Link. The `.ioc` file in each project opens the pin/clock configuration in STM32CubeMX.
