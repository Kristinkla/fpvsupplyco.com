# FPV Glossary

Plain-language definitions of the terms you will see when shopping for FPV parts. Maintained by [FPV Supply Co](https://fpvsupplyco.com).

---

## Core Electronics

**FC (Flight Controller)**
The brain of the drone. Runs the firmware (Betaflight, INAV, etc.), reads sensor data, and tells the ESCs how fast to spin each motor. Measured mainly by its MCU (microcontroller unit).

**ESC (Electronic Speed Controller)**
Takes the low-power signal from the FC and delivers the high-current power the motors need. Converts DC battery power into the three-phase AC that brushless motors require.

**4-in-1 ESC**
Four ESCs on a single board — one per motor. Standard on modern 5" builds because it saves space and weight.

**AIO (All-in-One)**
A board combining the FC and ESC (and sometimes VTX and receiver) in one unit. Common on whoops and sub-250g builds.

**Stack**
An FC and a 4-in-1 ESC sold as a matched pair, designed to bolt together with a fixed pinout. Buying a stack avoids wiring compatibility problems.

**MCU**
Microcontroller Unit — the actual chip on the FC. Common ones are STM32 F4, F7, and H7. Higher numbers mean more processing power.

**BEC**
Battery Eliminator Circuit — steps battery voltage down to a stable voltage (usually 5V or 9V) for peripherals like receivers, cameras, and GPS.

**PDB (Power Distribution Board)**
Older method of distributing battery power to ESCs. Mostly replaced by 4-in-1 ESCs, which handle distribution themselves.

---

## Motors

**Brushless Motor**
The standard FPV motor type. No brushes to wear out, higher efficiency, more power. Described by stator size and KV.

**KV**
RPM per volt of applied voltage. A 1900KV motor on 6S (~22.2V nominal) spins at roughly 42,000 RPM at full throttle. Higher KV = faster spin, lower torque per volt.

**Stator Size (e.g. 2207)**
First two digits are stator diameter in mm (22mm), last two are stator height in mm (07mm). A 2207 is "taller" than a 2205 — more torque, slightly slower response.

**Motor Poles**
Number of magnetic poles in the motor. Affects ESC timing settings and the RPM signal.

---

## Frames & Props

**Carbon Fiber Frame**
The structural chassis. Carbon fiber is used for its stiffness-to-weight ratio. Frame size (3", 5", 7") refers to the prop size it accepts.

**Duct / Ducted Frame**
A frame with protective shrouds around the props. Safer for indoor flight and around people (cinewhoops), at the cost of efficiency.

**Prop Pitch**
A measure of how "aggressive" a propeller is — how far it would advance through the air in one rotation. Higher pitch means more thrust and more current draw.

**Blade Count**
Number of blades per prop. Tri-blade is the freestyle standard. Bi-blade is more efficient. Quad-blade grips harder.

**CW / CCW**
Clockwise / counter-clockwise. Props and motor threads come in both — they must match, or the prop will unscrew itself in flight.

---

## Video & Radio Link

**VTX (Video Transmitter)**
Broadcasts the camera feed from the aircraft to your goggles. Rated in milliwatts — higher power means longer range but is legally regulated by region.

**VRX (Video Receiver)**
The receiving side, usually built into goggles.

**Analog Video**
Traditional FPV video. Lower resolution but very low latency. Still used in racing.

**Digital HD Video**
Systems that transmit an HD feed and record HD onboard. Examples include DJI O3/O4, Walksnail, and HDZero.

**RX (Receiver)**
Receives control commands from your radio transmitter and passes them to the FC.

**TX (Transmitter) / Radio**
The handheld controller you fly with.

**ELRS (ExpressLRS)**
An open-source radio link protocol. Long range, low latency, very cheap receivers. The current default choice for new builds.

**Crossfire**
A mature, reliable radio protocol by TBS. Popular for long range.

**UART**
A serial port on the FC used to connect one peripheral each. Running out of UARTs is a common constraint — count your peripherals before buying.

---

## Firmware & Setup

**Betaflight**
The dominant open-source flight controller firmware for FPV.

**INAV**
Firmware focused on GPS navigation, waypoint missions, and autonomous flight.

**BLHeli_S / BLHeli_32 / AM32**
ESC firmware families. BLHeli_32 and AM32 are "32-bit" — they support higher PWM frequencies and smoother motor response.

**PWM Frequency**
How often the ESC switches motor phases per second. Higher frequencies (e.g. 48kHz, 96kHz) run smoother and quieter but require 32-bit ESC hardware.

**Blackbox**
Onboard flight logging. Records gyro, motor, and control data for tuning analysis. Needs flash storage or an SD card.

**PID**
Proportional-Integral-Derivative — the tuning values that determine how the FC responds to disturbances. Poor PIDs cause oscillation or sluggish flight.

**Desync**
When the ESC loses sync with the motor, causing a sudden loss of power on one motor. Usually caused by an underrated ESC, bad motor timing, or damaged hardware.

---

## Build Classes

**Whoop / Tinywhoop**
Very small ducted drones, typically 1S–2S, meant for indoor flying. Under 250g by design.

**Cinewhoop**
A ducted drone sized for a small cinema camera. Prioritizes smooth, safe, close-proximity footage.

**Freestyle**
Flying style focused on acrobatic maneuvers freely, without a fixed race course.

**Racing**
Timed competition through gates. Prioritizes latency, acceleration, and durability.

**Long Range**
Efficiency-focused builds designed to fly far on a single battery. Typically 7" and up, low KV, bi-blade props.

**RTF (Ready-to-Fly)**
Comes fully assembled, with a radio and often goggles included. Fly it out of the box.

**BNF (Bind-and-Fly)**
Fully assembled, but you supply your own radio and goggles, and bind your own receiver.

---

## B2B / Supply Terms

**MOQ (Minimum Order Quantity)**
The smallest quantity a supplier will sell. Often applies to custom-configured or custom-branded products.

**OEM (Original Equipment Manufacturer)**
Manufacturing a product that carries the buyer's brand.

**ODM (Original Design Manufacturer)**
Designing *and* manufacturing a product that carries the buyer's brand — the supplier handles development, not just production.

**Sample Order**
A small first order for evaluation before committing to volume. Standard practice before bulk purchasing.

**Lead Time**
Time between placing an order and it shipping. Longer for custom configurations.

**DA (Dead on Arrival)**
Hardware that does not function when first received. Good suppliers test before shipping to minimize DA rate.

---

*Need a term that is not here? Open an [Issue](../../issues) and we will add it.*

---

Looking for parts? [FPV Supply Co](https://fpvsupplyco.com) supplies [FC & ESC stacks](https://fpvsupplyco.com/collections/fc-esc-stacks), [motors](https://fpvsupplyco.com/collections/brushless-fpv-motors), [frames](https://fpvsupplyco.com/collections/carbon-fiber-fpv-frames), [cameras](https://fpvsupplyco.com/collections/fpv-cameras), and [complete drones](https://fpvsupplyco.com/collections/rtf-bnf-drones).
