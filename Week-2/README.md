# Week 2 – Electronic Schematic Design and Simulation Planning

## Project
**SPELCT – Smart Portable Electronics Lab & Component Tester**

## Objective
Week 2 converts the Week 1 product concept and requirements into a preliminary electronic architecture and simulation plan. The goal is to validate important circuit functions before physical prototyping, identify design risks early, and establish measurable criteria for later hardware development.

## Week 1 Design Basis
SPELCT is a portable low-voltage educational component tester intended for electronics students, laboratories, hobbyists and entry-level technicians. The proposed functions include component identification, resistance and capacitance measurement, diode/LED testing, supported transistor identification, continuity checking, a guided color display, rechargeable operation and optional wireless logging.

## Preliminary Electronic Architecture
**Protected Test Interface → Input Protection / Discharge Check → Selectable Test Stimulus / Ranges → Analog Front End → ESP32-S3 Controller → TFT Display / User Controls / Optional Wi-Fi-BLE Logging**

A rechargeable battery and USB-C power subsystem supplies regulated low-voltage rails to the controller, display and measurement circuitry.

## Major Circuit Sections

### 1. Power Management
Rechargeable battery and USB-C charging/power input with regulated rails for the controller, display and analog circuitry. Local decoupling and sensible analog/digital power routing are required.

### 2. Test Interface
A ZIF socket and/or protected low-voltage terminals provide the component interface.

### 3. Input Protection and Discharge Check
The concept includes current limiting, suitable low-voltage clamping/protection and a pre-test check for unexpected residual voltage. Exact ratings will be finalized after supported measurement limits are defined.

### 4. Selectable Test Stimulus
The controller applies controlled low-energy test conditions through known paths. Multiple measurement states allow firmware to infer component behavior.

### 5. Analog Front End
The front end conditions test-node voltages for ADC/comparator measurement. Range selection, filtering, reference stability and calibration are important design considerations.

### 6. ESP32-S3 Controller
Coordinates measurement sequences, ADC acquisition, calculations, identification logic, display updates, calibration data and optional wireless logging.

### 7. Display and User Interface
A 2.4–2.8 inch class TFT is proposed for guided instructions, component symbols, measured values, pin information and warnings.

## Interface Specification

| Interface | Source | Destination | Main Design Concern |
|---|---|---|---|
| Power | Battery/USB-C stage | System rails | Regulation, noise, runtime |
| Test ports | Unknown component | Protection/front end | Misconnection, residual charge |
| Stimulus control | ESP32-S3 | Range/test switching | Safe default state |
| Measurement | Analog front end | ESP32 ADC | Range, resolution, reference, noise |
| Display | ESP32-S3 | TFT | Bus loading/update noise |
| User input | Buttons/encoder | ESP32-S3 | Debounce and robustness |
| Wireless | ESP32-S3 | External device | Power/noise and optional operation |

## Schematic Design Strategy
The detailed design should be divided into functional sheets:
1. Power and charging
2. Controller/programming interface
3. Display/user interface
4. Protected test interface
5. Analog measurement/range circuitry
6. Optional connectivity/expansion

Important regulated rails and analog nodes should include test points. Final measurement ranges, tolerances and component values should be confirmed through simulation and reference-component testing rather than assumed.

## Simulation Strategy
A SPICE-based simulator such as LTspice can be used for the analog sections.

Planned techniques include:
- DC operating-point analysis
- DC sweeps
- Transient analysis
- Parameter sweeps
- Noise/sensitivity investigation
- Supply/component tolerance checks

## Planned Simulation Test Cases

| Test | Purpose | Expected Outcome |
|---|---|---|
| Resistance channel | Evaluate known resistor models across proposed ranges | Distinguishable response within ADC range |
| Capacitance timing | Evaluate controlled charge/discharge | Timing changes predictably with capacitance |
| Diode/LED test | Test polarity and forward response at limited current | Device behavior can be distinguished |
| BJT identification | Evaluate known NPN/PNP models in controlled states | Sufficient response difference for classification |
| Input protection | Apply defined abnormal low-voltage cases | Protected nodes remain within declared limits |
| Supply variation | Sweep supply tolerance | Measurement path remains sufficiently stable |
| Filter response | Apply transient/noise disturbance | Reduced variation without excessive delay |

## Functional Analysis
Resistance measurement can use a known low-energy stimulus and reference path, with resistance inferred from measured voltage relationships. Capacitance can be estimated from controlled charge/discharge timing. Diodes can be characterized from polarity and forward response at limited test current. Semiconductor identification requires several controlled measurement states rather than a single reading.

Each analog function should first be simulated independently. Integration should follow only after its expected operating range and failure cases are understood.

## Power Management and Signal Integrity
- Use regulated rails appropriate to selected components.
- Place decoupling close to active devices.
- Keep sensitive analog nodes short.
- Avoid routing noisy display/wireless return currents through sensitive references.
- Use filtering where bandwidth permits.
- Use stable references and calibration data.
- Schedule wireless activity outside critical measurement periods if testing shows interference.

## Key Design Risks

| Risk | Planned Response |
|---|---|
| Unknown charged capacitor | Pre-test voltage check, defined discharge strategy and protection |
| Wide component range | Multiple ranges and declared supported limits |
| Contact resistance | Contact-quality checks; improved terminal method in later revision if needed |
| ADC/reference variation | Calibration and repeatability testing |
| Switch resistance/leakage | Include switching effects in simulation/calibration |
| Digital/wireless noise | Layout separation, decoupling, filtering and timed measurements |
| Unsupported component | Return an explicit unsupported/uncertain result |

## Design Refinement Process
**Define Test Case → Build SPICE Subcircuit → Run Analysis → Measure Nodes → Compare with Requirement → Adjust Values → Re-run → Document**

Only low-voltage sections that meet the defined design criteria should progress to the prototype stage.

## Week 2 Work Schedule

| Activity | Hours |
|---|---:|
| Review Week 1 requirements and simulation scope | 3 |
| Preliminary architecture and schematic development | 7 |
| Power/protection analysis | 4 |
| Measurement front-end simulation planning | 5 |
| Functional simulations and parameter sweeps | 7 |
| Noise/tolerance/refinement analysis | 4 |
| Documentation and design review | 5 |
| **Total** | **35** |

## Week 2 Deliverables
- Preliminary SPELCT electronic architecture
- Major component and interface description
- Simulation-tool selection and strategy
- Functional analysis of measurement circuits
- Power-management and signal-integrity considerations
- Risk and design-challenge analysis
- Design-refinement plan
- Structured documentation for Week 3 prototyping

## Safety Scope
SPELCT is a low-voltage educational component tester. Week 2 does not include direct household-mains or hazardous high-voltage testing. Simulation and future prototypes remain within clearly defined extra-low-voltage limits.

## Week 2 Outcome
Week 2 establishes a structured path from the product requirements to a preliminary electronic design. The next stage is to convert validated low-voltage circuit sections into a practical prototype and verify them using known reference components.

## Author
**KAMALESUWARAN V**  
Electronics and Communication Engineering (ECE)
