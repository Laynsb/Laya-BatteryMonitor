# Laya-BatteryMonitor Introduction (Rust)

Laya-BatteryMonitor is a very lightweight and zero-overhead daemon service for Android ROMs. It significantly minimizes power usage by adjusting the CPU frequency and governor based on the screen state.

## Description

- Automatically reduces CPU frequency when the screen is off, saving power without impacting performance when the device is in use.
- Switches to powersave governor in screen-off mode for better battery preservation.
- Significantly Lowering device temperature and Power consumption during screen-off (especially during hotspot)
- Wide compatibility across all devices
- Runs natively via OS's init and doesn't need a magisk module

## Installation

For installation and integration steps, refer to `guide.txt`.

## Core Behavior

• 🧠 Smart CPU Policy Handling.
Dynamically manages CPU frequency and governor behavior based on screen state changes. Fully adaptive to any device configuration.

• 🗑️ No dumpsys, No Bloat.
Avoids Android's heavyweight system utilities (dumpsys, top, etc.) for efficiency. Instead, uses direct low-level file access and event monitoring via native sysfs interfaces.

• 🔌 Event-Driven Power Saving.
Monitors screen state using efficient inotify hooks to avoid polling and wakeups. Automatically applies power-saving CPU settings when the screen turns off, and restores the last-used performance state on wake.

• ⚡ Microsecond-Class Efficiency.
Written in a low-overhead systems language (Rust), focused on thread safety, zero-cost abstraction, and fast execution.

• 📱 Modular & Headless.
No UI or frontend required. Designed for ROM integration. Can run silently in background with optional property toggling.

## LICENSE

Licensed under the Laynsb License v1.1

✅ Free for personal and non-commercial use.

✅ Redistribution is permitted as long as the original binary is kept intact and proper credit to Laynsb is given.

🚫 Modification of authorship, reverse engineering, or commercial distribution is strictly prohibited.


See LICENSE for full terms.
