# FPV Component Selection Guide

A practical guide to matching flight controllers, ESCs, motors, frames, and propellers into a build that actually flies well. Maintained by [FPV Supply Co](https://fpvsupplyco.com).

---

## 1. Start With the Frame, Not the Electronics

The most common beginner mistake is buying an FC stack first and a frame later. The frame dictates everything else:

| Frame Size | Typical Prop Size | Best For |
|---|---|---|
| 2" – 2.5" | 2" – 2.5" | Indoor, cinewhoop, tight spaces |
| 3" – 3.5" | 3" – 3.5" | Light freestyle, sub-250g builds |
| 5" | 5" – 5.1" | The standard — freestyle, racing, cinematic |
| 7" | 7" | Long range, efficiency, payload |
| 10"+ | 10" – 13" | Heavy lift, cinematic, industrial platforms |

**Rule of thumb:** pick your frame size from where you will actually fly, then size the electronics to the frame.

---

## 2. Flight Controllers: F4 vs F7 vs H7

| MCU | Clock | Best For | Notes |
|---|---|---|---|
| **STM32 F4** (e.g. F405) | 168 MHz | Budget builds, simple setups | Plenty for most 5" freestyle builds |
| **STM32 F7** (e.g. F722, F745) | 216 MHz | Feature-rich builds | More UARTs, better for HD video + GPS + multiple peripherals |
| **STM32 H7** (e.g. H743) | 480 MHz | Racing, high-rate loops | Highest loop rates, 32-bit ESC support, blackbox headroom |

**What actually matters:**
- **UART count** — count your peripherals: receiver, GPS, VTX, camera control, HD video. Each needs a UART.
- **Blackbox storage** — onboard flash (e.g. 512MB) is far more convenient than an SD card for tuning.
- **Barometer** — needed for altitude hold and reliable GPS rescue.
- **Bluetooth** — lets you tune from a phone at the field with no cable. Genuinely useful.

---

## 3. ESC: Match the Current Rating to the Motors

The ESC must handle the **peak** current draw of your motors, not the average.

| Motor Size (5" class) | Typical Peak Draw | Minimum ESC |
|---|---|---|
| 2207 / 2306, low KV (1700–1900) | ~30–35A | 45A |
| 2207 / 2306, mid KV (2400–2600) | ~35–45A | 55A – 60A |
| 2207 / 2306, high KV (2700+) | ~45–55A | 60A – 80A |

**Key guidance:**

- **Always leave headroom.** An ESC rated at exactly your peak draw will run hot and eventually desync. Aim for 20–30% above peak.
- **4-in-1 vs individual ESCs** — 4-in-1 keeps builds clean and light. Individual ESCs are easier to replace after a crash. Most modern 5" builds use 4-in-1.
- **8-bit vs 32-bit** — 32-bit ESCs support higher PWM frequencies (up to 96kHz) and run smoother, but 8-bit (BLHeli_S) is cheaper and perfectly capable for most pilots.
- **AIO boards** — FC and ESC combined on one board. Great for whoops and sub-250g builds where space is critical. Repairability suffers, so match current rating carefully.

---

## 4. Motors: KV Is the Whole Story

**KV = RPM per volt.** Higher KV spins faster, lower KV spins slower with more torque.

The rule that matters: **lower KV pairs with higher cell count, higher KV pairs with lower cell count.**

| Build Type | Cell Count | Motor KV Range |
|---|---|---|
| 5" freestyle | 6S | 1700 – 1900 |
| 5" freestyle | 4S | 2400 – 2600 |
| 5" racing | 6S | 1900 – 2000 |
| 3.5" freestyle | 6S | 2500 – 2800 |
| 7" long range | 6S | 1200 – 1500 |
| Cinewhoop | 6S | 1700 – 2000 (ducted) |
| Tinywhoop | 1S – 2S | 0702 – 1103 (tiny stators) |

**Stator size matters too.** A 2207 has a 22mm stator diameter and 7mm height. Taller stators (2207 vs 2205) produce more torque — better for aggressive props, heavier builds, and freestyle. Shorter, wider stators spin up faster — better for racing.

---

## 5. Propellers: Match Pitch to Your Goal

| Prop Type | Characteristic | Use Case |
|---|---|---|
| **Low pitch** (e.g. 4.3") | Efficient, smooth | Long range, cinematic, cruising |
| **Mid pitch** (e.g. 4.5") | Balanced | All-round freestyle |
| **High pitch** (e.g. 5.0"+) | Aggressive thrust | Racing, punchy freestyle |
| **Tri-blade** | Grip + smooth video | Most freestyle/cinematic builds |
| **Bi-blade** | Efficiency | Long range, less grip |
| **Quad-blade** | Max grip | Racing, heavy lift |

**Important:** higher pitch props draw significantly more current. If you increase pitch, verify your ESC rating still has headroom.

---

## 6. Video Systems: Analog vs Digital

| | Analog | Digital (HD) |
|---|---|---|
| **Latency** | Lowest | Low (good systems are close) |
| **Image quality** | Low resolution but instant | HD recording + HD live feed |
| **Cost** | Cheap | Higher |
| **Best for** | Racing, budget, reliability | Cinematic, freestyle, content creation |

Both remain valid in 2026. Racing still favors analog for pure latency. Freestyle and cinematic work has largely moved to digital for the recording quality.

---

## 7. Radios & Receivers

- **ELRS (ExpressLRS)** — the current standard. Long range, low latency, cheap receivers. Default choice for new builds.
- **Crossfire** — mature, reliable, well supported. Good for long range.
- **RadioMaster** — the dominant radio ecosystem. Multi-protocol modules let one radio fly many aircraft.

**Recommendation:** build with ELRS unless you have a specific reason not to. It is well supported by open-source firmware and the receiver lineup is cheap.

---

## 8. Build Planning Checklist

Before ordering parts, confirm each of these:

- [ ] Frame size chosen based on where you fly
- [ ] FC has enough UARTs for all peripherals
- [ ] ESC current rating exceeds motor peak draw by 20–30%
- [ ] Motor KV matches your battery cell count
- [ ] Prop pitch is appropriate and accounted for in ESC sizing
- [ ] VTX power legal for your region and matched to your video system
- [ ] Receiver protocol compatible with your radio
- [ ] Battery connector and C-rating adequate for total current draw
- [ ] Spare props ordered (you will break them)

---

## 9. Where to Source These Parts

[**FPV Supply Co**](https://fpvsupplyco.com) supplies every category covered in this guide:

- [FC & ESC Stacks](https://fpvsupplyco.com/collections/fc-esc-stacks)
- [Brushless FPV Motors](https://fpvsupplyco.com/collections/brushless-fpv-motors)
- [Carbon Fiber FPV Frames](https://fpvsupplyco.com/collections/carbon-fiber-fpv-frames)
- [FPV Propellers](https://fpvsupplyco.com/collections/fpv-propellers)
- [FPV Cameras](https://fpvsupplyco.com/collections/fpv-cameras)
- [Video Transmitters (VTX)](https://fpvsupplyco.com/collections/video-transmitters-vtx)
- [FPV Receivers (RX)](https://fpvsupplyco.com/collections/fpv-receivers-rx)
- [RTF & BNF Drones](https://fpvsupplyco.com/collections/rtf-bnf-drones)

Building at volume or developing a custom platform? [Talk to us about OEM/ODM supply](https://fpvsupplyco.com/pages/contact-us).

---

*This guide is provided free for the FPV community. Specifications and guidance reflect common practice — always verify against your specific components' datasheets.*
