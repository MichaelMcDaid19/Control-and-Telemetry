## RC Car Landspeed World Record – Trade Studies (UK, ~3–5 mile course)

### 0) Mission assumptions & what matters most

* **Range**: 3–5 miles (≈ 5–8 km) **at ground level** is *harder* than it sounds because the car and its antenna sit very low; you lose Fresnel clearance quickly.
* **Top priorities (in order)**:

  1. **Link robustness** (margin at 5–8 km ground-level LOS, resistance to multipath)
  2. **Predictable latency** (steering feel + stability)
  3. **Failsafe / safety** (positive “kill”, deterministic behavior on RF loss)
  4. **Telemetry** (RSSI/LQ, battery, temps, GPS speed, etc.)
  5. **UK legality / compliance** (power + duty-cycle constraints can matter in 868 MHz SRD bands) ([www.ofcom.org.uk][1])

---

## 1) UK radio compliance snapshot (practical)

### 868 MHz SRD band: powerful but can be constrained

* In the UK/EU, **868 MHz “Short Range Devices”** rules commonly include **EIRP caps and duty-cycle (or LBT/AFA) requirements** depending on sub-band. ([www.ofcom.org.uk][1])
* This matters because **RC control is “chatty”** (continuous packets), which can collide with duty-cycle-limited sub-bands if your system isn’t using an allowed mechanism.

**Takeaway:** 868 MHz is still usually the best engineering choice for 5–8 km ground-level control, but you should **select a system/firmware mode intended for EU/UK operation** and design for **big link margin** (good antennas, mounting, ground station elevation).

---

## 2) Controller interface trade study (the “handset”)

### Options compared (UK pricing & availability examples)

| Option                                        | Typical use-case fit                                                                       | Strengths                                                                                                                             | Drawbacks                                                                                | Price / availability (UK examples)                           |
| --------------------------------------------- | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| **RadioMaster MT12 (EdgeTX “surface” radio)** | Best “flexible + hackable” surface controller; pairs perfectly with ELRS/Crossfire modules | Open, programmable mixes/logic; easy telemetry screens; can run ELRS or external long-range module; purpose-built surface form factor | Slightly more “setup” effort than a traditional race radio; depends on module ecosystem  | **£129.99** (often stocked) ([hobbyrc.co.uk][2])             |
| **Sanwa MT-5 + RX-493i**                      | High-end racing feel (short/medium range)                                                  | Excellent ergonomics; telemetry indicator function to help optimize receiver placement                                                | Still a **2.4 GHz** surface link—range margin at 5–8 km is typically the limiting factor | ~**£274.99** (example listing) ([modelsport.co.uk][3])       |
| **Sanwa M17S + RX-493i**                      | “No-compromise” race interface                                                             | Top-tier latency/feel; premium telemetry + features                                                                                   | Expensive; still 2.4 GHz; range remains the big risk for 3–5 miles                       | **£539.99** (in stock example) ([modelsport.co.uk][4])       |
| **Futaba T4PM Plus**                          | Reliable mainstream competition radio                                                      | Strong ecosystem, good feel                                                                                                           | Still 2.4 GHz; less “scriptable” than EdgeTX                                             | **£242.99** in stock example ([wheelspinmodels.co.uk][5])    |
| **Spektrum DX5 Rugged**                       | Rugged basher interface                                                                    | Durable; familiar                                                                                                                     | Availability varies (often limited/discontinued depending on retailer)                   | Example “in stock” listing **£269.99** ([rcmodelz.co.uk][6]) |
| **FlySky Noble NB4 Pro+**                     | Feature-rich surface radio                                                                 | Lots of features, AFHDS3; multi-protocol outputs on some RX                                                                           | Vendor-stated “remote distance” claims often not at 5–8 km ground-level; still 2.4 GHz   | **£429** in stock example ([scmodels.co.uk][7])              |

### Interface recommendation (for 3–5 miles)

If you only pick one controller platform for a record attempt:

* **Best overall controller interface**: **RadioMaster MT12**, because it can be the **surface-style controller** *and* host a true long-range RF module ecosystem (868 ELRS or Crossfire). ([hobbyrc.co.uk][2])
* Traditional high-end race radios (Sanwa/Futaba) are excellent for feel, but **the 2.4 GHz surface RF link is the risk** at 5–8 km ground-level.

---

## 3) Transmitter + receiver (RF link) trade study

### A) Traditional 2.4 GHz surface systems (Sanwa / Futaba / Spektrum / FlySky)

**What you get**

* “Race-grade” steering feel, great ergonomics, easy setup, mature RX packaging.

**Why it’s risky here**

* 3–5 miles at ground level is the corner case: low antennas + multipath + Fresnel loss.
* You can mitigate with elevated TX antenna / diversity RX / careful placement, but **margin** is the concern.

**Use it when**

* You have a **shorter course**, or you can place the driver station **very near the midpoint** and keep excellent LOS.

---

### B) 2.4 GHz ExpressLRS (ELRS)

**Pros**

* Strong telemetry, modern link management, good community support.
* Can be run on MT12 platforms (integrated ELRS variants) and others.

**Cons**

* Still 2.4 GHz propagation: you may make 5–8 km in ideal LOS with good antennas, but it’s less forgiving than sub-GHz at low heights.

**Use it when**

* You want a simpler build than sub-GHz, and your site has **excellent LOS** and you can elevate antennas.

---

### C) **868 MHz ExpressLRS** (recommended “value long-range” path)

**Typical hardware**

* **868 ELRS TX module** + **868 receiver** (CRSF interface to your vehicle controller)

**Example components & UK pricing**

* **RadioMaster Bandit “868/915” ELRS receiver (BR1)**: **£19.90**, in stock example ([Flying Tech][8])

  * BR1 **Bus interface: CRSF** ([RadioMaster RC][9])
* **RadioMaster Bandit 868MHz ELRS module**: **£99.50**, in stock example ([Flying Tech][10])

**Pros**

* Sub-GHz propagation is much better for ground-level range.
* CRSF is a clean integration path (1 UART for control + telemetry conceptually), and ELRS uses CRSF for serial receivers. ([docs.px4.io][11])
* Cost-effective.

**Cons / gotchas**

* **UK/EU 868 regulatory constraints** (power/duty-cycle/LBT) must be respected. ([www.ofcom.org.uk][1])
* Antenna quality and placement still matter enormously.

**Best for**

* 3–5 mile attempts where you want maximum value and open tooling.

---

### D) **868 MHz TBS Crossfire** (recommended “most proven long-range RC” path)

**Example components & UK pricing**

* **TBS Crossfire TX module (full-size)**: **£214.90**, “only 3 left” example ([Flying Tech][12])
* **TBS Crossfire Nano RX**:

  * **£23.90** in stock example ([Your FPV Drones, Buy Online, UK][13])
  * Another listing shows **£25.90** but out of stock ([hobbyrc.co.uk][14])
* Nano RX feature set includes **SBUS / PPM / PWM / CRSF** (and more) per docs/listings ([Team BlackSheep][15])

**Pros**

* Very mature long-range ecosystem, strong link behavior, excellent telemetry workflows.
* Flexible receiver outputs help whether your “flight controller” is a full autopilot, an MCU safety layer, or direct PWM. ([Team BlackSheep][15])

**Cons**

* More expensive than ELRS Bandit path.
* Same UK/EU sub-GHz compliance considerations apply. ([www.ofcom.org.uk][1])

**Best for**

* When you prioritize “proven long-range RC” over cost.

---

### E) Separate telemetry modem link (RFD868x / SiK) – **good for data, not ideal as primary control**

**What it is**

* High-power telemetry modems (often used with MAVLink/ArduPilot ecosystems).

**Example components & UK pricing**

* **RFD868x v2**: **£116.67 ex VAT / £140 inc VAT** example listing ([3dxr.co.uk][16])
* **RFD868x modem v2.0** (single): **£120.83** example ([The Bionic Eye][17])
* **RFD868x bundle** (pair): **£209.99** example, sold out ([Unmanned Tech][18])

**Important regulatory/throughput caveat**

* EU certified variants may enforce **low-power full duty cycle vs high-power low duty cycle** modes (trade range vs throughput). ([old.unmannedtechshop.co.uk][19])

**Pros**

* Great for **telemetry/logging**, longer-range data backhaul, and redundancy.
* Integrates naturally if you later adopt an autopilot stack.

**Cons**

* As a *primary real-time RC control link*, it’s not as straightforward (and can run into duty-cycle/throughput issues depending on mode). ([old.unmannedtechshop.co.uk][19])

**Best use**

* **Secondary telemetry link** (video-less speed record attempts still benefit hugely from a separate “data pipe”).

---

### F) What **not** to do in the UK: 902–928 MHz “900 MHz ISM” gear as-is

* Example: **RFD900x** covers **902–928 MHz** ([The Bionic Eye][20])
* That band plan is not the UK/EU SRD 868 allocation; you generally want **868-family** hardware for UK operation. ([www.ofcom.org.uk][1])

---

## 4) Receiver-side integration (since your “flight controller” is unknown)

### Integration patterns (pick one now, stay compatible with the others)

#### Pattern 1 — **No flight controller** (direct control)

* Receiver outputs **PWM** to:

  * ESC throttle
  * Steering servo
  * Optional brake/paro/kill actuator
* You rely on **receiver failsafe** and an external **hardware kill**.

**Good**

* Simple, fewer failure modes, minimal latency.

**Risk**

* Less opportunity for “stability assist”, traction management, speed limiting, brake blending, etc.

#### Pattern 2 — “Safety MCU / bridge” (recommended minimum for a record car)

* Receiver outputs **CRSF/SBUS** into a small MCU (or later, an autopilot).
* MCU enforces:

  * **arming logic**
  * **deadman switch**
  * **rate limiting** (steering slew limits at 200+ mph equivalent)
  * **failsafe braking**
  * optional **independent kill relay**
* MCU outputs PWM/CAN to ESC/servo.

**Good**

* Big safety upside without committing to a full autopilot.

#### Pattern 3 — Full autopilot / “flight controller” (Pixhawk/ArduPilot Rover-like stack)

* Receiver → FC via **CRSF** (single UART concept for RC+telemetry) ([docs.px4.io][11])
* FC handles stabilization/assist + logs + structured telemetry.

**Good**

* Best observability & automation.

**Risk**

* More integration effort; must be tested thoroughly.

### Compatibility tip: choose RF gear that speaks **CRSF**

* **CRSF** is used by Crossfire and also by ELRS systems. ([docs.px4.io][11])
* Example: Bandit BR1 receiver bus interface is **CRSF** ([RadioMaster RC][9])
* Crossfire Nano RX supports CRSF (and other outputs) ([Team BlackSheep][15])

### If you need PWM but want CRSF long-range RF anyway

* Use a **CRSF/ELRS → PWM converter board** (8ch) if your RF receiver is serial-only. ([Flying Tech][21])

---

## 5) Recommended “best paths” for your specific case (UK, 3–5 miles)

### Recommendation A (best value + long-range margin)

**RadioMaster MT12 + 868 ELRS (Bandit)**

* **Controller**: RadioMaster MT12 (surface) ([hobbyrc.co.uk][2])
* **TX module**: Bandit 868 module ([Flying Tech][10])
* **Vehicle RX**: Bandit BR1 (CRSF) ([Flying Tech][8])
* **Vehicle control**: CRSF → (FC or safety MCU). If no FC, add CRSF→PWM converter. ([Flying Tech][21])

**Why this wins**

* Strong propagation (868) + low cost + open tooling + clean CRSF integration.

**Main drawback**

* You must be deliberate about **UK/EU 868 compliance modes** and antenna setup. ([www.ofcom.org.uk][1])

---

### Recommendation B (most “proven long-range RC ecosystem”)

**MT12 (or other module bay radio) + TBS Crossfire 868**

* **TX module**: TBS Crossfire full module £214.90 example ([Flying Tech][12])
* **RX**: Crossfire Nano RX ~£23.90–£29.95 examples ([Your FPV Drones, Buy Online, UK][13])
* **Outputs**: CRSF/SBUS/PWM options help whichever vehicle controller you end up with ([Team BlackSheep][15])

**Why this wins**

* Very robust long-range behavior, flexible RX outputs.

**Main drawback**

* Cost.

---

### Recommendation C (add-on for “serious telemetry” and post-run analysis)

**Separate RFD868x (or similar) telemetry pipe**

* Use it to stream/record: pack voltage, ESC current/temps, GPS speed, RSSI/LQ, control commands, etc.
* You’ll often learn more from data than from “seat feel” at record speeds.

**Reality check**

* EU/UK-certified modes may restrict throughput vs power. ([old.unmannedtechshop.co.uk][19])

---

## 6) Practical engineering notes that make or break 3–5 mile control

### Antenna & mounting (do not skip)

* **Get the TX antenna up high** (tripod/mast). Even 2–5 m helps dramatically at 5–8 km.
* On-car antenna:

  * Keep away from carbon, ESC power leads, and noisy DC/DC converters
  * Give it a clean ground reference where applicable
  * Test multiple placements and log LQ/RSSI

### Safety architecture (strongly recommended)

* **Two independent “stop” mechanisms**:

  1. RF failsafe → command brake + neutral
  2. Independent **hardware kill** (relay or pyrofuse-style cutoff) triggered by a dedicated channel and/or watchdog
* “Arming” sequence: require **two actions** (e.g., switch + trigger) before full throttle is allowed.

---

## 7) Example BOM (copy/paste baseline)

### Baseline long-range control (ELRS 868)

* RadioMaster MT12 surface radio – **£129.99** ([hobbyrc.co.uk][2])
* Bandit 868 ELRS TX module – **£99.50** ([Flying Tech][10])
* Bandit BR1 868 ELRS receiver (CRSF) – **£19.90** ([Flying Tech][8])
* Optional: CRSF/ELRS → 8ch PWM converter – (for “no FC” builds) ([Flying Tech][21])

### Alternative long-range control (Crossfire)

* TBS Crossfire TX module – **£214.90** ([Flying Tech][12])
* TBS Crossfire Nano RX – **£23.90** (in stock example) ([Your FPV Drones, Buy Online, UK][13])

### Optional telemetry backhaul

* RFD868x v2 single modem – **~£120.83** ([The Bionic Eye][17])
* RFD868x pair bundle – **£209.99** (example listing) ([Unmanned Tech][18])

[1]: https://www.ofcom.org.uk/spectrum/radio-equipment/short-range-devices?utm_source=chatgpt.com "Short-range devices"
[2]: https://www.hobbyrc.co.uk/radiomaster-mt12-surface-radio-controller?utm_source=chatgpt.com "Radiomaster MT12 Surface Radio Controller"
[3]: https://www.modelsport.co.uk/product/sanwa-mt-5-radio-set-with-rx-493i-1342534?utm_source=chatgpt.com "Sanwa MT-5 Radio Set with RX-493I SA101A32671A"
[4]: https://www.modelsport.co.uk/product/sanwa-m17s-radio-set-with-rx493i-1367194?utm_source=chatgpt.com "Sanwa M17S Radio Set with RX493i SA101A32971A"
[5]: https://wheelspinmodels.co.uk/i/futaba-t4pm-plus-with-r334sbse-receiver-352854/?utm_source=chatgpt.com "Futaba T-4PM Plus With R334SBS-E Receiver"
[6]: https://www.rcmodelz.co.uk/spektrum-dx5-rugged-5ch-dsmr-tx-w-sr515.html?srsltid=AfmBOoqnQQR_44ok8OhBQWomldJvv1GvhYhsblRu9jDFtHC3BMqqvd0A&utm_source=chatgpt.com "Spektrum DX5 Rugged 5Ch DSMR Tx w/SR515"
[7]: https://scmodels.co.uk/flysky-noble-nb4-pro-2-4ghz-transmitter-2-receivers-nb4pro-plus?srsltid=AfmBOoqQNhXb6NLQ-xaiOdbK48ensEbI8jorgA9Dxbp6hikXzeA572RZ&utm_source=chatgpt.com "Flysky NOBLE NB4 Pro+ 2.4ghz Transmitter +2 Receivers ..."
[8]: https://www.flyingtech.co.uk/product/bandit-br1-expresslrs-915-868mhz-receiver/?utm_source=chatgpt.com "Bandit BR1 ExpressLRS 915/868MHZ Receiver"
[9]: https://radiomasterrc.com/products/bandit-br1-expresslrs-receiver?utm_source=chatgpt.com "Bandit BR1 ExpressLRS 915MHz Receiver"
[10]: https://www.flyingtech.co.uk/product/bandit-expresslrs-915-868mhz-rf-module/?utm_source=chatgpt.com "Bandit ExpressLRS 915/868MHZ RF Module"
[11]: https://docs.px4.io/main/en/telemetry/crsf_telemetry?utm_source=chatgpt.com "CRSF Telemetry (TBS Crossfire Telemetry) | PX4 Guide (main)"
[12]: https://www.flyingtech.co.uk/product/team-blacksheep-tbs-crossfire-long-range-uhf-transmitter-module/?utm_source=chatgpt.com "Team Blacksheep TBS Crossfire Long Range UHF ..."
[13]: https://yourfpv.co.uk/product/tbs-crossfire-nano-rx-fpv-long-range-drone-receiver/?utm_source=chatgpt.com "tbs crossfire nano rx - fpv long range drone receiver"
[14]: https://www.hobbyrc.co.uk/tbs-crossfire-nano-receiver?utm_source=chatgpt.com "TBS Crossfire Nano Receiver"
[15]: https://www.team-blacksheep.com/media/files/tbs-crossfire-nano-quickstart.pdf?srsltid=AfmBOopmnNFgiGX9-1eXKMQZfYr5d5FgYMDSLChUwgIdnuCIx4HOl09S&utm_source=chatgpt.com "TBS CROSSFIRE Nano RX"
[16]: https://www.3dxr.co.uk/radio-gear-c33/telemetry-c31/868-mhz-telemetry-c65/rf-design-rfd-868ux-v2-modem-p3750?utm_source=chatgpt.com "RF Design - RFD 868ux v2 Modem"
[17]: https://shop.thebioniceye.co.uk/products/rfd868xmodem?srsltid=AfmBOorejv0MrBcbC1M63uwOR8xW5GBbRYaTFnkWSLQx6n6GtnT_6FCQ&utm_source=chatgpt.com "RF Design RFD868x Modem v2.0 - The Bionic Eye"
[18]: https://www.unmannedtechshop.co.uk/products/rf-design-rfd-868x-long-range-telemetry-modem-bundle?srsltid=AfmBOoqMjX16I6Gft881T4SLHzQ5chHaiVM8dyPJrRjNSCIkiZep8nZ3&utm_source=chatgpt.com "RF Design RFD 868x Long Range Telemetry Modem Bundle"
[19]: https://old.unmannedtechshop.co.uk/product/rfd-868x-eu-long-range-telemetry-modem/?utm_source=chatgpt.com "RFD 868x EU V2 Long Range Telemetry Modem"
[20]: https://shop.thebioniceye.co.uk/products/rfd900xmodem?srsltid=AfmBOop6ZbGtNSpXJP6iyZqt3LpOs8drsPz9C54-2gN124UGYBsadPe4&utm_source=chatgpt.com "RF Design RFD900x Modem v2.0 - The Bionic Eye"
[21]: https://www.flyingtech.co.uk/product/crsf-elrs-to-8ch-pwm-converter-v2/?utm_source=chatgpt.com "CRSF ELRS to 8CH PWM Converter V2"
