# Laya-BatteryMonitor Introduction (Rust)

Laya-BatteryMonitor is a Very lightweight and zero overhead daemon service for Android ROMs. It minimizes power usage by adjusting CPU frequency & governor based on screen state.

## Description

- Locks CPU frequency to minimum & Governor to powersave when the screen is off.
- Restores All CPU settings when the screen is turned on.
- Runs natively via init and doesn't need a module

## Installation

For installation and integration steps, refer to `README.txt`.
