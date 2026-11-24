# Zephyr RTOS Foundational Course

## Course Details
**Organization:** [Iomico](https://iomico.com)  
**Program:** Zephyr Course: Fundamental (Cohort 2/2026)  
**Certificates & Documents:**
- 🎓 **[View Completion Certificate](documents/Certificate_Sri_Charan_Mittapelly.pdf)** *(Certificate ID: `uqhxdmvsu9`)*
- 📚 **[Course Lecture Slides & Notes](documents/lectures/)** *(Lectures 1–8 + Live Discussions)*
- 🔗 **[Dedicated Hands-On Code Repository on GitHub](https://github.com/sricharan037/zephyr-course)**

> *This course was completed as part of the intensive Cohort 2 training program delivered by **Iomico**, an embedded systems engineering and IoT R&D leader in the Zephyr ecosystem. The curriculum emphasizes industry-standard, production-grade RTOS development practices, spanning kernel configuration, hardware description, custom driver design, and automated unit testing.*

---

## Short Description
A practical, deep-dive embedded software engineering training on the **Zephyr Real-Time Operating System (RTOS)**. It covers the full lifecycle of RTOS application development—from West workspace topology and Kconfig configuration to Devicetree hardware description, custom board bring-up, out-of-tree driver creation, interactive shell integration, and automated Ztest/Twister unit testing with code coverage.

---

## Objective
- Master the modern embedded software stack powered by the Zephyr RTOS and Linux Foundation open-source tooling.
- Gain hands-on competence in building, flashing, and debugging applications for physical MCUs (ESP32 DevKitC) and simulated targets (QEMU x86).
- Learn hardware-agnostic design principles using Zephyr’s unified Driver Model and Devicetree (`.dts`, `.overlay`).
- Implement automated embedded testing methodologies using the Ztest framework and Twister test runner to generate validated code coverage reports.

---

## Hardware & Software Stack
- **Target Hardware**: ESP32 DevKitC (`esp32_devkitc/esp32/procpu`)
- **Emulation & Testing**: QEMU x86 Atom (`qemu_x86_atom`)
- **RTOS Version**: Zephyr RTOS v4.2.0 / v4.3.0
- **Build System & Toolchain**: Zephyr SDK 0.17.2, West meta-tool, CMake, Ninja, GCC / Clang
- **Hardware Modeling**: Devicetree Source (`.dts`, `app.overlay`), Devicetree Bindings (YAML)
- **Configuration Engine**: Kconfig (`prj.conf`, `Kconfig`)
- **Testing & Quality Assurance**: Ztest test framework, Twister test runner, Gcov / Lcov coverage

---

## Course Curriculum & Hands-On Implementations

### [Lecture 01: Welcome to Zephyr RTOS & Environment Setup](./documents/lectures/Lecture%2001%20-%20Welcome%20to%20Zephyr%20RTOS.pdf)
- Explored Zephyr RTOS architecture, kernel services, memory management, and multi-architecture hardware abstraction.
- Installed and configured the Zephyr SDK 0.17.2, Python virtual environments, and required dependencies on Windows.
- **Hands-on Task**: Initialized the development workspace and built/ran the foundational `hello_world` application.

### [Lecture 02: West Topologies & Application Build Flow](./documents/lectures/Lecture%2002%20-%20West_%20Topologies%20_%20Hello%20World.pdf)
- Analyzed West workspace topologies: T1 (application inside Zephyr repo), T2 (application repo as manifest), and T3 (forest topology).
- Managed multi-repository dependencies and project revisions via `west.yml`.
- **Hands-on Task**: Created an out-of-tree application repository and built a multithreaded `blinky` sample targeting the ESP32 microcontroller (`esp32_devkitc/esp32/procpu`).

### [Lecture 03: Application Configuration with Kconfig](./documents/lectures/Lecture%2003%20-%20App%20Configuration_%20Kconfig.pdf)
- Understood the Kconfig configuration language, menus, symbols, prompts, and boolean/integer types.
- Learned configuration precedence rules (`prj.conf`, board-specific defconfigs, Kconfig fragments).
- **Hands-on Task**: Defined custom application Kconfig symbols and dynamically switched firmware execution paths at compile time.

### [Lecture 04: Hardware Description with Devicetree (DTS)](./documents/lectures/Lecture%2004%20-%20App%20Configuration_%20Devicetree.pdf)
- Mastered Devicetree concepts: hierarchical node graphs, properties, phandles, interrupt routing, and peripheral pin multiplexing.
- Wrote Devicetree overlays (`app.overlay`) to redefine board pinouts without modifying vendor base files.
- Created custom Devicetree YAML bindings (`dts/bindings/sensor/my,led-sensor.yaml`) to define property schemas and validation rules.
- **Hands-on Task**: Mapped hardware pins and connected custom virtual sensor nodes to the ESP32 GPIO controller using Devicetree macros (`DT_NODELABEL`, `GPIO_DT_SPEC_GET`).

### [Lecture 05: Custom Board Definition & Hardware Bring-Up](./documents/lectures/Lecture%2005%20-%20Custom%20Boards.pdf)
- Examined the anatomy of a custom Zephyr board directory: `board.dts`, `board.yaml`, `board.cmake`, `Kconfig.board`, and `Kconfig.defconfig`.
- **Hands-on Task 1**: Created `our_board` using board inheritance and the copy/rename technique.
- **Hands-on Task 2**: Architected a completely new board target (`my_board`) from scratch, specifying SoC defconfigs, flash partitioning, and custom peripheral aliases.

### [Lecture 06: Zephyr Driver Development](./documents/lectures/Lecture%2006%20-%20Zephyr%20Driver%20Development.pdf)
- Studied Zephyr's unified device driver model: driver configuration structs, runtime data structs, and virtual API function pointer tables.
- Leveraged driver initialization macros (`DEVICE_DT_INST_DEFINE`) and execution levels (`POST_KERNEL`, `APPLICATION`).
- **Hands-on Task**: Built an out-of-tree device driver module for a custom LED sensor (`led_sensor.c`), implemented the standard Zephyr sensor API (`sensor_sample_fetch`, `sensor_channel_get`), and added a custom driver extension API.

### [Lecture 07: Shell Subsystem Integration](./documents/lectures/Lecture%2007%20-%20Shell%20Subsystem.pdf)
- Leveraged the Zephyr Shell subsystem to provide an interactive serial CLI for live device inspection, diagnostics, and debugging.
- Implemented static and dynamic shell commands using `SHELL_CMD_REGISTER` and `SHELL_STATIC_SUBCMD_SET_CREATE`.
- **Hands-on Task**: Exposed the custom LED sensor driver over UART, enabling runtime calibration, status querying, and value changes via `sensor set` shell commands.

### [Lecture 08: Unit Testing with Ztest & Twister](./documents/lectures/Lecture%2008%20-%20Unit%20Testing.pdf)
- Explored embedded test-driven development (TDD) using Zephyr's Ztest framework.
- Automated headless test execution across emulated platforms using the `twister` test runner.
- Generated code coverage metrics using Gcov and Lcov to identify untested execution branches.
- **Hands-on Task 1**: Wrote unit test suites for a custom `calculator` module and executed them in QEMU.
- **Hands-on Task 2**: Implemented comprehensive unit tests for a custom `ring_buf` (circular buffer) library, verifying buffer overflow handling, boundary conditions, and concurrency safety, achieving 100% test pass rates and generating HTML coverage reports.

---

## Repository Structure & Code Overview

```text
Zephyr_RTOS_Course/
├── README.md                      # Detailed project & course documentation
├── documents/
│   ├── Certificate_Sri_Charan_Mittapelly.pdf  # Iomico Completion Certificate
│   ├── toolchain_setup.txt        # Environment variables & West build commands
│   └── lectures/                  # Official course slide decks (Lectures 01–08 + Q&A)
└── code/                          # Source code and test suites
    ├── west.yml                   # West manifest file
    ├── app/
    │   ├── CMakeLists.txt
    │   ├── Kconfig
    │   ├── prj.conf               # Configuration: Serial, Console, Sensor, Shell
    │   ├── app.overlay            # Devicetree overlay for LED sensor node
    │   ├── src/
    │   │   └── main.c             # Application entry point
    │   ├── boards/
    │   │   ├── my_board/          # Custom board defined from scratch
    │   │   └── our_board/         # Custom board defined via template
    │   ├── drivers/
    │   │   └── my_driver_module/  # Out-of-tree LED sensor driver with DTS binding
    │   └── modules/
    │       ├── calculator/        # Custom calculator utility module
    │       └── ring_buf/          # Custom circular ring buffer module
    └── tests/
        ├── calculator/            # Ztest test suite for calculator module
        └── ring_buf/              # Ztest test suite and Twister specifications
```

---

## Results & Key Learnings
1. **Industry-Grade RTOS Experience**: Mastered the architecture of Zephyr RTOS, one of the fastest-growing open-source operating systems for commercial IoT and embedded devices.
2. **Hardware Abstraction & Portability**: Learned how to design hardware-independent embedded software using Devicetree overlays and unified driver models.
3. **Automated Testing & CI/CD**: Gained hands-on proficiency with headless simulation (QEMU) and Zephyr's native testing ecosystem (Ztest + Twister), enabling test automation without requiring physical hardware on every build.
4. **Verified Credential**: Awarded the official **Certificate of Completion** by **Iomico** for **Cohort 2/2026** (Certificate ID: `uqhxdmvsu9`).

---

**Submitted by:** Sri Charan Mittapelly  
**B.Tech ECE**, Kamala Institute of Technology and Science
