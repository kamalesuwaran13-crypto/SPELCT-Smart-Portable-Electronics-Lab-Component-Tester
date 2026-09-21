# SPELCT – Smart Portable Electronics Lab & Component Tester

## Electronics & Hardware Product Development Engineer Internship

**Prepared by:** KAMALESUWARAN V  
**Department:** Electronics and Communication Engineering (ECE)

## Project Overview
SPELCT is a portable low-voltage electronics testing and learning device proposed for students, laboratories, hobbyists, makers, and entry-level technicians. The product combines common component-testing functions with a guided user interface so that users can identify supported components, view basic measurements, and understand the test result.

The project is being developed through a structured hardware-product-development process. **Week 1** established the product concept and requirements. **Week 2** converts those requirements into a preliminary electronic architecture and simulation strategy.

> **Safety scope:** SPELCT is an educational extra-low-voltage prototype. It is not intended for direct household-mains testing or as a certified precision instrument.

## Problem Statement
Electronics learners often use several separate tools and reference sources to identify components, check basic characteristics, and perform introductory troubleshooting. SPELCT aims to combine common first-level component checks into one portable guided device while maintaining a clear educational workflow.

## Target Users
- Diploma and engineering students
- Electronics laboratories
- Hobbyists and makers
- Entry-level electronics technicians
- Teachers and technical trainers

## Proposed Product Features
- Automatic identification of supported electronic components
- Resistance and capacitance measurement
- Diode and LED polarity/forward-response testing
- Supported BJT/MOSFET identification
- Continuity/basic connection checking
- Guided color display
- Rechargeable portable operation
- USB-C power/charging
- Optional Wi-Fi/BLE result logging
- Protected low-voltage test interface
- Calibration and firmware-update support

## Current Electronic Architecture
**Protected Test Interface → Input Protection / Discharge Check → Selectable Test Stimulus & Ranges → Analog Front End → ESP32-S3 Controller → TFT Display / User Controls / Optional Wireless Logging**

The battery/USB-C power stage supplies regulated low-voltage rails to the controller, display, and measurement circuitry.

---

## Week 1 – Product Conceptualization and Requirement Analysis

Week 1 focused on defining the product before detailed circuit development.

### Completed Work
- Product concept and problem statement
- Market need and target-user analysis
- Competitor study
- Product features and benefits
- Functional and non-functional requirements
- Preliminary architecture
- Product-development risks
- Feasibility assessment
- Development roadmap

➡️ **[Open Week 1 Documentation](Week-1/README.md)**  
➡️ **[Open Week 1 Product Requirements](Week-1/Product_Requirements.md)**

---

## Week 2 – Electronic Schematic Design and Simulation Planning

Week 2 develops the preliminary electronic design and establishes how important circuit functions will be evaluated before physical prototyping.

### Completed Work
- Preliminary electronic architecture
- Major circuit-section definition
- Power-management strategy
- Protected test-interface concept
- Analog front-end planning
- ESP32-S3 interface planning
- TFT/user-interface planning
- SPICE simulation strategy
- Functional simulation test cases
- Signal-integrity and noise considerations
- Design-risk analysis
- Design-refinement process
- 35-hour Week 2 work plan

➡️ **[Open Week 2 Documentation](Week-2/README.md)**

### Week 2 Simulation Approach
A SPICE-based tool such as LTspice can be used to evaluate the analog sections through DC operating-point analysis, DC sweeps, transient analysis, parameter sweeps, and tolerance/sensitivity studies.

Planned simulation areas include resistance measurement, capacitance timing, diode/LED response, semiconductor-identification concepts, input protection, supply variation, and filtering behavior.

---

## Product Requirements Summary

| ID | Requirement | Priority |
|---|---|---|
| FR-01 | Automatically identify supported component categories | Must |
| FR-02 | Measure resistance over a defined educational range | Must |
| FR-03 | Measure capacitance over a defined educational range | Must |
| FR-04 | Test diode polarity and forward response within defined limits | Must |
| FR-05 | Identify supported BJT/MOSFET type and terminals | Should |
| FR-06 | Provide continuity/basic connection checking | Should |
| FR-07 | Display results on an integrated color display | Must |
| FR-08 | Show messages for unsupported/unsafe conditions | Must |
| FR-09 | Support optional result logging/export | Could |
| NFR-01 | Operate within defined low-voltage test limits | Must |
| NFR-02 | Include appropriate input protection | Must |
| NFR-03 | Provide repeatable measurements within target tolerance | Must |
| NFR-04 | Complete typical tests in a practical time | Should |
| NFR-05 | Be portable and rechargeable | Should |
| NFR-06 | Support calibration and firmware updates | Should |

## Preliminary Hardware Plan
- ESP32-S3-class microcontroller
- 2.4–2.8 inch class color TFT display
- ZIF socket / protected test terminals
- Input-protection stage
- Selectable test/range circuitry
- Analog measurement and signal-conditioning circuitry
- Rechargeable battery
- Regulated power rails
- USB-C charging/power interface
- User controls
- Handheld insulated enclosure

Final component values, measurement ranges, accuracy targets, and protection ratings will be confirmed through simulation and later reference-component testing.

## Key Engineering Challenges
- Measurement accuracy across different component ranges
- Input protection against incorrect or unexpected conditions
- Safe handling of residual charge within the declared low-voltage scope
- ADC/reference stability and calibration
- Contact resistance at test terminals
- Analog-switch resistance/leakage
- Noise from the display, power subsystem, and wireless operation
- Reliable semiconductor identification
- User-friendly handling of unsupported components
- Cost, battery life, portability, and manufacturability

## Development Roadmap

### Phase 1 – Discovery / Week 1
Market research, target-user analysis, competitor study, concept selection, requirements, and feasibility.

### Phase 2 – Electronic Design / Week 2
Preliminary schematic architecture, interfaces, power/protection planning, simulation strategy, functional analysis, and design refinement.

### Phase 3 – Engineering Prototype
Build validated low-voltage circuit sections, integrate the controller/display, and develop firmware proof-of-concept.

### Phase 4 – Verification
Calibration, reference-component comparison, repeatability testing, power testing, and defined misuse-condition testing.

### Phase 5 – Productization
Custom PCB, enclosure design, connector optimization, UI refinement, cost reduction, and design review.

### Phase 6 – Pilot / Production Readiness
Design-for-manufacturing/testing, supplier planning, assembly procedure, end-of-line testing, and pilot build.

## Repository Structure

```text
SPELCT-Smart-Portable-Electronics-Lab-Component-Tester/
├── README.md
├── Week-1/
│   ├── README.md
│   └── Product_Requirements.md
├── Week-2/
│   └── README.md
├── Hardware/          (planned)
├── Firmware/          (planned)
├── Documentation/     (planned)
└── Images/            (planned)
```

## Current Internship Progress
- ✅ **Week 1:** Product Conceptualization and Requirement Analysis
- ✅ **Week 2:** Electronic Schematic Design and Simulation Planning
- ⏳ **Next Stage:** Prototype development/integration according to the internship schedule

## Author
**KAMALESUWARAN V**  
Electronics and Communication Engineering (ECE)  
Electronics & Hardware Product Development Engineer Internship
