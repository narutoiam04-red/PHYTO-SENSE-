# PHYTO-SENSE-
🌱 PHYTO-SENSE ∞ is a multimodal living-sensor research platform combining ESP32-based sensing, environmental monitoring, plant imaging, and data analysis to experimentally study plant nutrient-stress responses and recovery under controlled conditions.




# 🌱 PHYTO-SENSE ∞

### A Multimodal Living-Sensor Network for Non-Destructive Detection and Recovery Monitoring of Plant Nutrient Stress

PHYTO-SENSE ∞ is an experimental research platform designed to investigate whether measurements collected from living plants, environmental sensors, and digital imaging can reveal systematic changes associated with experimentally induced nutrient stress and subsequent recovery.

The project combines **embedded sensing, plant science, environmental monitoring, computer vision, data logging, and data analysis** into a single research system.

> **Environment → Living Response → Measurement → Intelligence → Recovery**

## 🎯 Research Question

**Can measurements from living plants, combined with environmental sensors, detect experimentally induced nutrient stress and track recovery after appropriate nutrient restoration?**

PHYTO-SENSE ∞ does **not** claim to diagnose every plant disease or nutrient deficiency. Its objective is to experimentally investigate measurable biological responses under controlled conditions.

## 🔬 Experimental Design

The prototype uses three plants:

- **P1 — Control:** normal complete nutrition
- **P2 — Experimental Group A:** controlled nutrient-limitation condition
- **P3 — Experimental Group B:** a different controlled nutrient-limitation condition

Plants are monitored under standardized conditions, followed by controlled treatment and restoration phases.

### Experimental Phases

1. **Baseline** — establish normal measurements
2. **Controlled Condition** — introduce the planned nutrient limitation
3. **Restoration** — return experimental plants to appropriate nutrition
4. **Recovery** — continuously monitor changes after restoration

## 📡 Multimodal Sensing

Each plant node can collect:

- 🌱 Soil moisture
- 🌡️ Temperature
- 🍃 Leaf/surface temperature
- 💡 Environmental light
- 💧 Air humidity
- 🌤️ Environmental temperature
- 📸 Plant images
- 📏 Growth and morphological measurements

### Hardware

- ESP32
- DS18B20 temperature sensor
- MLX90614 non-contact temperature sensor
- Soil-moisture sensor
- BME280
- BH1750
- DS3231 RTC
- MicroSD card module
- OLED display
- LED indicators
- Camera

## 📸 PHYTO-VISION

The imaging subsystem converts visual plant changes into measurable data rather than relying only on subjective observations.

Potential image-derived variables include:

- Leaf area
- Plant height
- Leaf count
- Colour features
- Morphological changes
- Growth over time

For example, instead of saying:

> "Plant 2 looks less healthy."

the system can investigate:

> "Projected leaf area changed by X% relative to baseline."

## 💾 Data Logging

Sensor measurements are timestamped using the DS3231 RTC and stored for later analysis.

Example:

| Date | Time | Plant | Air Temp | Humidity | Soil | Leaf Temp |
|---|---|---|---:|---:|---:|---:|
| 25-08-26 | 09:00 | P1 | 28.4°C | 63% | 54% | 29.1°C |
| 25-08-26 | 09:00 | P2 | 28.5°C | 62% | 49% | 30.0°C |
| 25-08-26 | 09:00 | P3 | 28.4°C | 63% | 51% | 29.6°C |

Raw data will be preserved for reproducible analysis.

## 🖥️ Live Laboratory Dashboard

The OLED provides a real-time view of sensor measurements:

```text
PHYTO-SENSE ∞
NODE: P02

TEMP     28.5 C
HUM      62.4 %
SOIL     48.2 %
LEAF     30.1 C
LIGHT    842 lx

STATE: MONITORING
