# Internships and Courses Portfolio

Welcome to my **Internships and Courses Portfolio** repository! This repository showcases key engineering projects, research reports, and hands-on implementations I developed across professional internships and specialized technical training programs.

---

## 👨‍💻 About Me
- **Name**: Sri Charan Mittapelly
- **Field**: B.Tech in Electronics and Communication Engineering (ECE), 3rd Year
- **College**: Kamala Institute of Technology and Science, Huzarabad
- **Focus Areas**: Embedded Systems, Real-Time Operating Systems (RTOS), Automotive ADAS, Internet of Things (IoT), Firmware Engineering

---

## 📂 Portfolio Summary

| # | Project / Course | Organization | Domain | Credentials / Links |
|---|------------------|--------------|--------|---------------------|
| 1 | **[EV & ADAS System](./EV&ADAS_project)** | Emertxe | Automotive Embedded & ADAS | 🎓 [Certificate](./EV&ADAS_project/documents/Internship%20Completion%20Certificate%20-%20Sri%20Charan%20Mittapelly.pdf) • 🎥 [Video Demo](https://youtu.be/EQwRbna1PLI?si=PbaMT5ZqzDDylEkk) |
| 2 | **[CodeAlpha IoT Virtual Internship](./Code_Alpha_project)** | CodeAlpha | Internet of Things (IoT) | 🎓 [Certificate](./Code_Alpha_project/documents/Certificate_Sri%20Charan%20Mittapelly.pdf) • 📄 [LOR](./Code_Alpha_project/documents/LOR_Sri%20Charan%20Mittapelly.pdf) |
| 3 | **[Zephyr RTOS Foundational Course](./Zephyr_RTOS_Course)** | Iomico | Real-Time Operating Systems (RTOS) | 🎓 [Certificate](./Zephyr_RTOS_Course/documents/Certificate_Sri_Charan_Mittapelly.pdf) • 🔗 [GitHub Code](https://github.com/sricharan037/zephyr-course) |

---

## 🚀 Projects & Programs

### 1. [EV & ADAS System](./EV&ADAS_project)  
**Virtual Learning Internship at [Emertxe](https://www.emertxe.com) (Embedded Systems & IoT)**  
🎓 **[View Completion Certificate](./EV&ADAS_project/documents/Internship%20Completion%20Certificate%20-%20Sri%20Charan%20Mittapelly.pdf)** • 📄 **[Offer Letter](./EV&ADAS_project/documents/Offer%20Letter%20-%20Sri%20Charan%20Mittapelly.pdf)**  
🎥 **[Watch Project Explanation & Demo on YouTube](https://youtu.be/EQwRbna1PLI?si=PbaMT5ZqzDDylEkk)**

- **Hardware Platform**: STM32F103C8T6 "Blue Pill" (ARM Cortex-M3 @ 72 MHz) running inside PICSimLab.
- **Core Functionality**: Models core electric-vehicle dynamics (torque, acceleration, regenerative braking, battery state-of-charge, and range) alongside active ADAS safety features including Forward Collision Warning (FCW), Time-to-Collision (TTC) estimation, and Blind-Spot Detection (BSD) using 3 ultrasonic sensors.
- **Architecture & Telemetry**: Enforces safe-state behaviour with a dedicated bit-field fault manager (instantly cutting motor torque upon critical alarms) and streams structured telemetry over UART at 115200 bps to a real-time Python/Matplotlib dashboard cluster.

---

### 2. [CodeAlpha IoT Virtual Internship](./Code_Alpha_project)
**Virtual Learning Internship at CodeAlpha (Internet of Things)**  
🎓 **[View Completion Certificate](./Code_Alpha_project/documents/Certificate_Sri%20Charan%20Mittapelly.pdf)** • 📄 **[Letter of Recommendation (LOR)](./Code_Alpha_project/documents/LOR_Sri%20Charan%20Mittapelly.pdf)** • 📄 **[Offer Letter](./Code_Alpha_project/documents/Sri%20Charan%20Mittapelly%20.pdf)**

- **Scope & Work**: Completed a comprehensive curriculum focused on modern IoT architectures, smart sensors, and simulation tools.
- **Task 1 — Industrial IoT Report**: Detailed research paper analyzing the transition of legacy manufacturing into Industry 4.0 smart factories with IIoT sensor layers and predictive maintenance.
- **Task 2 — Ultrasonic Radar Simulation**: Implemented and simulated a real-time sweeping radar system on the Wokwi online platform using an Arduino Uno, HC-SR04 ultrasonic sensor, servo motor, and SSD1306 OLED display.
- **Task 4 — IoT & AI Integration Case Study**: In-depth analytical case study exploring the synergy between real-time IoT sensor networks and edge/cloud AI algorithms across healthcare, agriculture, and autonomous vehicles.

---

### 3. [Zephyr RTOS Foundational Course](./Zephyr_RTOS_Course)
**Intensive Technical Training at [Iomico](https://iomico.com) (Cohort 2/2026)**  
🎓 **[View Completion Certificate](./Zephyr_RTOS_Course/documents/Certificate_Sri_Charan_Mittapelly.pdf)** *(Certificate ID: `uqhxdmvsu9`)*  
🔗 **[Hands-On Code Repository on GitHub](https://github.com/sricharan037/zephyr-course)** • 📚 **[Course Lecture Slides](Zephyr_RTOS_Course/documents/lectures/)**

- **Hardware & Targets**: ESP32 DevKitC (`esp32_devkitc/esp32/procpu`) and QEMU x86 Atom (`qemu_x86_atom`).
- **Core Concepts**: Mastered Zephyr RTOS v4.2/v4.3, West workspace management, Kconfig build configurations, and Devicetree hardware description (`.dts`, `.overlay`, YAML bindings).
- **Driver & Hardware Bring-Up**: Built custom board definitions (`our_board`, `my_board`) from scratch and engineered an out-of-tree LED sensor driver conforming to the unified Zephyr Sensor Subsystem with custom extension APIs.
- **Shell & Testing**: Exposed dynamic runtime diagnostics over an interactive UART serial Shell (`sensor set` commands) and authored Ztest test suites with Twister for automated unit testing and code coverage reports.

---

## 🛠️ Technical Skill Badges

- **Embedded Platforms & MCUs**: STM32 (ARM Cortex-M3), ESP32 (Xtensa), Arduino Uno, QEMU x86
- **Operating Systems & Frameworks**: Zephyr RTOS, STM32 HAL, FreeRTOS concepts
- **Build Tools & Environments**: West, CMake, Ninja, STM32CubeIDE, PICSimLab, Wokwi, VS Code
- **Hardware Abstraction**: Devicetree (DTS), Devicetree Bindings (YAML), Kconfig
- **Languages**: Embedded C, C++, Python, Assembly basics
- **Testing & Quality Assurance**: Ztest, Twister, Gcov / Lcov
- **Protocols & Buses**: UART, GPIO, ADC, PWM, I2C, SPI
