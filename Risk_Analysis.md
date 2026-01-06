# Vanguard Project - Risk Analysis Document
## RC Car Land Speed World Record Attempt - Control and Telemetry System

---

## Executive Summary

This document identifies and analyzes potential risks associated with the Control and Telemetry system for the Vanguard RC car land speed record project. The analysis covers technical, schedule, and financial risks, along with mitigation strategies to ensure project success.

---

## 1. Technical Risks

### 1.1 Electrical and Power System Risks

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| T-001 | **Electrical Short Circuits** | Medium | High | High |
| | *Description:* Short circuits in high-power systems could damage ESCs, motors, or flight controller | | | |
| | *Consequence:* Component failure, potential fire hazard, project delays | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| T-002 | **Battery Overheat or Fire** | Medium | Critical | Critical |
| | *Description:* High current draw at maximum speed may cause battery thermal runaway | | | |
| | *Consequence:* Fire hazard, complete vehicle destruction, safety incident | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| T-003 | **Overheating Electrical Components** | High | High | High |
| | *Description:* ESCs, motors, and flight controller may exceed thermal limits during sustained high-power operation | | | |
| | *Consequence:* Component damage, reduced performance, system shutdown | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| T-004 | **Thermal Expansion** | Medium | Medium | Medium |
| | *Description:* Heat-induced expansion may affect component mounting and aerodynamic shell fitment | | | |
| | *Consequence:* Mechanical interference, vibration issues, component disconnection | | | |

### 1.2 Communication and Control Risks

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| T-005 | **Radio Link Noise Interference** | Medium | Critical | High |
| | *Description:* EMI from high-power motors/ESCs may interfere with RC receiver signal | | | |
| | *Consequence:* Loss of control, failsafe activation, unsuccessful run | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| T-006 | **Insufficient Signal Range** | Low | Critical | Medium |
| | *Description:* Transmitter/receiver range may not cover entire run distance at record speeds | | | |
| | *Consequence:* Loss of control during critical high-speed phase | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| T-007 | **Control Latency Exceeds Threshold** | Medium | High | High |
| | *Description:* Delay from user input to actuator response may be too slow for high-speed control | | | |
| | *Consequence:* Inability to make timely corrections, loss of vehicle control | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| T-008 | **Control System Oscillations at Max Speed** | Medium | Critical | High |
| | *Description:* Stability control may introduce oscillations or instability at maximum velocity | | | |
| | *Consequence:* Vehicle crash, component damage, failed record attempt | | | |

### 1.3 Telemetry System Risks

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| T-009 | **Telemetry Bugs and Data Errors** | Medium | Medium | Medium |
| | *Description:* Software bugs may cause incorrect telemetry readings or command interpretation | | | |
| | *Consequence:* Incorrect operator decisions, undetected system issues | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| T-010 | **Sensor Inaccuracy** | Medium | Medium | Medium |
| | *Description:* Voltage, current, and speed sensors may provide readings outside acceptable error margins | | | |
| | *Consequence:* Incorrect data for operator, inability to verify record speed | | | |

### 1.4 Mechanical Interface Risks

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| T-011 | **Steering Instability at High RPM/Velocity** | High | Critical | Critical |
| | *Description:* Servo response may be unpredictable at high speeds, inability to maintain straight line | | | |
| | *Consequence:* Loss of directional control, vehicle crash | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| T-012 | **Vibration-Induced Signal Instability** | Medium | High | High |
| | *Description:* High-speed operation vibrations may cause intermittent connections or signal noise | | | |
| | *Consequence:* Erratic control behavior, component disconnection | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| T-013 | **ESC/Servo Failure Under High Power** | Medium | Critical | High |
| | *Description:* ESCs or servo may fail when subjected to maximum power demands | | | |
| | *Consequence:* Loss of propulsion or steering, vehicle damage | | | |

### 1.5 Safety System Risks

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| T-014 | **Failsafe Non-Activation** | Low | Critical | Medium |
| | *Description:* Kill switch may not activate on loss of transmission signal | | | |
| | *Consequence:* Uncontrolled vehicle, safety hazard | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| T-015 | **Unintended Motor Activation During Startup** | Low | High | Medium |
| | *Description:* Motors may activate unexpectedly during system initialization | | | |
| | *Consequence:* Personnel injury, component damage | | | |

---

## 2. Schedule Risks

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| S-001 | **Parts Order Delays** | High | High | High |
| | *Description:* Specialized components (ESCs, motors, flight controllers) may have long lead times | | | |
| | *Consequence:* Delayed assembly, missed testing windows | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| S-002 | **Design and Integration Complexity** | High | High | High |
| | *Description:* Fitting all control and telemetry components into RC car chassis may be challenging | | | |
| | *Consequence:* Extended design iterations, delayed completion | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| S-003 | **Software Development Delays** | Medium | High | High |
| | *Description:* Telemetry and control software may require more development time than expected | | | |
| | *Consequence:* Delayed system testing, rushed implementation | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| S-004 | **Sensor Calibration Time** | Medium | Medium | Medium |
| | *Description:* Multiple sensor types may need to be tested and calibrated for reliability | | | |
| | *Consequence:* Extended testing phase, delayed validation | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| S-005 | **Testing Delays** | Medium | High | High |
| | *Description:* Weather, venue availability, or technical issues may delay testing | | | |
| | *Consequence:* Insufficient validation before record attempt, missed record attempt window | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| S-006 | **Cross-Team Coordination Delays** | Medium | Medium | Medium |
| | *Description:* Dependencies on other teams (aerodynamics, chassis, power) may cause bottlenecks | | | |
| | *Consequence:* Integration delays, rework requirements | | | |

---

## 3. Financial Risks

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| F-001 | **Component Cost Overruns** | Medium | Medium | Medium |
| | *Description:* High-performance components (ESCs, sensors, flight controllers) may exceed budget | | | |
| | *Consequence:* Budget constraints, need for cost-cutting compromises | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| F-002 | **Component Replacement Costs** | High | Medium | High |
| | *Description:* High-speed testing may result in component damage requiring replacements | | | |
| | *Consequence:* Increased project costs, budget depletion | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| F-003 | **Shipping and Import Costs** | Medium | Low | Low |
| | *Description:* Specialized components may require expensive international shipping | | | |
| | *Consequence:* Budget pressure, potential delays | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| F-004 | **Workshop and Facility Costs** | Low | Medium | Low |
| | *Description:* Testing and assembly may require workshop access fees | | | |
| | *Consequence:* Increased operational costs | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| F-005 | **Sponsorship Shortfall** | Medium | High | High |
| | *Description:* Expected sponsorship funding may not materialize | | | |
| | *Consequence:* Reduced budget, scaled-back project scope | | | |

| Risk ID | Risk | Likelihood | Impact | Risk Level |
|---------|------|------------|--------|------------|
| F-006 | **Software/Licensing Costs** | Low | Low | Low |
| | *Description:* Development tools or software licenses may add unexpected costs | | | |
| | *Consequence:* Minor budget impact | | | |

---

## 4. Mitigation Strategies

### 4.1 Technical Risk Mitigations

| Risk ID | Mitigation Strategy |
|---------|---------------------|
| T-001 | Read documentation for correct connections; implement proper fusing; use conformal coating on PCBs; conduct thorough pre-run inspections |
| T-002 | Use battery temperature monitoring; implement automatic power cutoff at thermal threshold; use fireproof battery containment; have fire suppression equipment on-site |
| T-003 | Use heat sinks and suitable heat dissipation methods; conduct temperature checks across range of durations and power levels; design adequate airflow paths |
| T-004 | Use materials with low thermal expansion coefficients; allow for thermal expansion in component mounting; test at operating temperatures |
| T-005 | Expose antennas from RC car body; use shielded wiring; position receiver away from EMI sources; test radio link integrity at full power |
| T-006 | Verify signal range at open area before record attempt; consider range extenders; establish communication checkpoints along run |
| T-007 | Benchmark and optimize control loop timing; select low-latency components; test response times at various power levels |
| T-008 | Extensive stability control testing and tuning; incremental speed testing; implement stability monitoring in telemetry |
| T-009 | Efficient and collaborative coding practices; code reviews; comprehensive testing; verify telemetry accuracy before full runs |
| T-010 | Review technical documents to select sensors with best specifications; cross-reference multiple sensor types; calibrate against known references |
| T-011 | Check steering sensitivity at high RPM and velocities; tune servo parameters; implement gyro-assisted stability |
| T-012 | Use vibration-dampened mounting; secure all connections; use locking connectors; bench test under simulated vibration |
| T-013 | Verify ESC and servo specifications exceed requirements; conduct high-power bench testing; have spare components available |
| T-014 | Test kill switch activation on every run; verify failsafe behavior during signal range testing; implement redundant safety systems |
| T-015 | Implement arming sequence; require explicit activation commands; test startup behavior before each session |

### 4.2 Schedule Risk Mitigations

| Risk ID | Mitigation Strategy |
|---------|---------------------|
| S-001 | Order parts early; identify alternative suppliers; maintain buffer stock of critical components |
| S-002 | Planning and coordination with other teams; create detailed CAD models before assembly; prototype with mockups |
| S-003 | Start software development early; use proven libraries where possible; implement continuous integration |
| S-004 | Begin sensor testing early in project; document calibration procedures; have backup sensor options identified |
| S-005 | Build schedule buffer; identify multiple testing venues; create indoor testing alternatives where possible |
| S-006 | Establish regular cross-team meetings; define clear interface specifications; use shared project tracking |

### 4.3 Financial Risk Mitigations

| Risk ID | Mitigation Strategy |
|---------|---------------------|
| F-001 | Detailed budgeting with contingency; prioritize critical components; seek component sponsorships |
| F-002 | Conduct incremental testing to minimize crash risk; design for repairability; stock spare components |
| F-003 | Consolidate orders to reduce shipping; identify local suppliers where possible; plan for customs delays |
| F-004 | Negotiate workshop access; utilize university facilities; share costs with other teams |
| F-005 | Diversify sponsorship sources; develop backup funding plans; prioritize essential expenditures |
| F-006 | Use open-source tools where possible; leverage educational licenses; plan software costs upfront |

---

## 5. Risk Matrix Summary

### Critical Risks (Require Immediate Attention)
- **T-002:** Battery Overheat or Fire
- **T-011:** Steering Instability at High RPM/Velocity

### High Risks (Require Active Management)
- **T-001:** Electrical Short Circuits
- **T-003:** Overheating Electrical Components
- **T-005:** Radio Link Noise Interference
- **T-007:** Control Latency Exceeds Threshold
- **T-008:** Control System Oscillations at Max Speed
- **T-012:** Vibration-Induced Signal Instability
- **T-013:** ESC/Servo Failure Under High Power
- **S-001:** Parts Order Delays
- **S-002:** Design and Integration Complexity
- **S-003:** Software Development Delays
- **S-005:** Testing Delays
- **F-002:** Component Replacement Costs
- **F-005:** Sponsorship Shortfall

### Medium Risks (Monitor Regularly)
- **T-004:** Thermal Expansion
- **T-006:** Insufficient Signal Range
- **T-009:** Telemetry Bugs and Data Errors
- **T-010:** Sensor Inaccuracy
- **T-014:** Failsafe Non-Activation
- **T-015:** Unintended Motor Activation During Startup
- **S-004:** Sensor Calibration Time
- **S-006:** Cross-Team Coordination Delays
- **F-001:** Component Cost Overruns

---

## 6. Verification and Testing Requirements

To address the identified risks, the following verification activities are mandated:

1. **Bench Testing:** All systems shall be simulated individually before integration
2. **Thermal Testing:** Temperature checks across range of durations and power levels
3. **Range Testing:** Signal range verification at open area (e.g., downs)
4. **Failsafe Testing:** Kill switch activation verification on loss of signal
5. **Telemetry Validation:** Accuracy verification before full test runs
6. **High-Power Testing:** ESC and servo validation at maximum power inputs
7. **Steering Sensitivity:** Testing at high RPM and velocities
8. **Pre/Post Run Checks:** System verification before and after every test run

---

## 7. Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2026-01-06 | Control & Telemetry Team | Initial release |

---

*This document should be reviewed and updated regularly as the project progresses and new risks are identified.*
