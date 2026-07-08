# Stabilization Control System (SCS)

This is a real-time embedded control system for a 2-DOF (azimuth and elevation) stabilization platform on a mobile system. The goal was to keep the platform pointed accurately and stay stable even while the vehicle it's mounted on is moving or going over rough terrain.

## What it does

The SCS sits between the Trajectory Control Computer (TCC), which tells it where to point, and the motors that actually move the platform. It takes the commanded target, reads sensor feedback, runs a control loop, and drives the motors to reach and hold that position. The whole loop runs on a fixed timing schedule so control timing stays predictable, since any drift here directly affects targeting accuracy.

It also acts as the communication link between the different subsystems and the master device, managing all data exchange over CAN bus with precise timing across more than 40 different message IDs, each tied to a different assembly in the system. It reads and processes data from each of these and acts on it accordingly.

## How it's built

- Firmware written in C++ on an STM32 microcontroller, with a fixed scheduling slot for sensing, I/O, and communication. Every control cycle runs at a fixed time interval instead of a free-running loop, so timing stays consistent.
- Control is done through a nested PID setup: a fast inner rate loop (2.1 ms) handles disturbance rejection, and a slower outer position loop (25.2 ms) handles precise tracking.
- A Kalman filter fuses high frequency gyroscope data with absolute encoder feedback, so the controller works off a clean state estimate instead of raw, noisy sensor data.
- Communication runs over CAN bus. I wrote a bare-metal driver for four MCP2518FD CAN controllers set up in a redundant primary/secondary configuration, so one CAN failure doesn't bring the whole system down.
- Added watchdog supervision and power sequencing logic so the system boots up safely and can recover from a fault without needing a manual reset.

## Tools used

STM32CubeIDE, C++, MCP2518FD CAN controllers, MCP23S17 IO Expander, oscilloscope, logic analyzer, CAN sniffer, ST-Link.

## Result

The system holds under 2% steady-state error under dynamic disturbance, and was tested against real vibration and movement conditions before being integrated with the rest of the platform.
