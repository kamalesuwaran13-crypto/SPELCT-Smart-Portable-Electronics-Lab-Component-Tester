# SPELCT – Smart Portable Electronics Lab & Component Tester

## Electronics & Hardware Product Development Engineer Internship

**Week 1 Task:** Product Conceptualization and Requirement Analysis  
**Prepared by:** KAMALESUWARAN V  
**Department:** Electronics and Communication Engineering (ECE)

## Project Overview

SPELCT is a proposed portable electronics testing and learning device for electronics students, laboratory users, hobbyists, and entry-level technicians. The concept combines common component-testing functions with a guided user interface so that the device can identify a component, display its measured parameters, and help the user understand the result.

The product is planned as a safe low-voltage educational prototype. It is not intended to replace certified or precision laboratory instruments.

## Problem Statement

Electronics learners often need several separate tools while identifying unknown components, checking whether a component is usable, and learning its basic characteristics. A portable integrated tester can make this workflow faster and easier while reducing the number of separate basic instruments required for first-level checks.

## Target Users

- Diploma and engineering students
- Electronics laboratories
- Hobbyists and makers
- Entry-level electronics technicians
- Teachers and technical trainers

## Proposed Features

- Automatic identification of supported electronic components
- Resistance and capacitance measurement
- Diode and LED testing
- BJT/MOSFET identification where supported
- Continuity/basic connection testing
- Guided color display
- Rechargeable portable operation
- USB-C power and charging
- Optional wireless result logging
- Protected low-voltage test interface

## Product Architecture

The proposed system contains:

1. Component/test input interface
2. Input protection and signal-conditioning stage
3. Measurement front end
4. ESP32-S3-class controller
5. Color display and user controls
6. Rechargeable battery and USB-C power system
7. Optional Wi-Fi/Bluetooth result logging

## Week 1 Product Requirements

| ID | Requirement | Priority |
|---|---|---|
| FR-01 | Automatically identify supported common component categories | Must |
| FR-02 | Measure resistance over a useful educational range | Must |
| FR-03 | Measure capacitance over a useful educational range | Must |
| FR-04 | Test diode polarity and forward voltage within defined limits | Must |
| FR-05 | Identify supported BJT/MOSFET type and terminal arrangement | Should |
| FR-06 | Provide continuity/basic connection checking | Should |
| FR-07 | Display results on an integrated color display | Must |
| FR-08 | Show guided messages for unsupported or unsafe conditions | Must |
| FR-09 | Support optional result logging/export | Could |
| NFR-01 | Operate only within defined low-voltage test limits | Must |
| NFR-02 | Include appropriate input protection | Must |
| NFR-03 | Produce repeatable measurements within the product target tolerance | Must |
| NFR-04 | Complete typical identification in a practical time | Should |
| NFR-05 | Be portable and rechargeable | Should |
| NFR-06 | Support calibration and future firmware updates | Should |

## Preliminary Hardware Plan

- ESP32-S3-class microcontroller
- 2.4–2.8 inch class color TFT display
- ZIF socket / protected test terminals
- Analog measurement and signal-conditioning circuitry
- Input protection circuitry
- Rechargeable battery
- Regulated power rails
- USB-C charging interface
- Handheld insulated enclosure

The final component selection will be made during circuit design after measurement range, accuracy, cost, availability, and protection requirements are evaluated.

## Market and Competitor Study

Compact component testers already demonstrate demand for portable automatic component identification. A relevant market reference is the FNIRSI LCR-P1, which combines LCR and semiconductor testing in a handheld format.

The SPELCT concept is differentiated by focusing on the **student learning workflow**: guided test instructions, clear component symbols, pin information, measurement interpretation, and optional result history instead of only displaying raw measurements.

## Development Roadmap

### Phase 1 – Discovery
Market research, target-user analysis, competitor study, concept selection, and initial requirements.

### Phase 2 – Product Definition
Measurement targets, system architecture, preliminary BOM, interface definition, and risk review.

### Phase 3 – Engineering Prototype
Develop the low-voltage measurement front end, protection circuit, controller interface, display UI, and firmware prototype.

### Phase 4 – Verification
Calibration, reference-component comparison, repeatability testing, power testing, and safe misuse-condition testing.

### Phase 5 – Productization
Custom PCB, enclosure design, connector optimization, UI refinement, cost reduction, and design review.

### Phase 6 – Pilot / Production Readiness
Design-for-manufacturing, supplier planning, assembly procedure, end-of-line testing, and pilot build.

## Key Engineering Challenges

- Measurement accuracy over different component ranges
- Protecting the input from incorrect connections
- Handling previously charged capacitors safely within the product's declared limits
- Reducing analog noise from the display, regulator, charging system, and wireless subsystem
- Reliable semiconductor identification
- Calibration across manufactured units
- Durable sockets and test connectors
- Balancing cost, accuracy, battery life, and portability

## Week 1 Deliverables Completed

- Product concept defined
- Problem statement and market need identified
- Target users analyzed
- Competitor study completed
- Features and benefits defined
- Functional and non-functional requirements prepared
- Preliminary product architecture developed
- Product-development risks identified
- Development roadmap prepared
- Feasibility assessed

## Repository Structure

```text
SPELCT-Smart-Portable-Electronics-Lab-Component-Tester/
├── README.md
├── Week-1/
├── Hardware/
├── Firmware/
├── Documentation/
└── Images/
```

The repository will be expanded as the internship progresses through circuit design, simulation, prototyping, firmware development, PCB design, testing, and product optimization.

## Safety Scope

SPELCT is being developed as a **low-voltage educational electronics prototype**. The prototype is not intended for direct mains-voltage testing or use as a certified professional measurement instrument.

## Author

**KAMALESUWARAN V**  
Electronics and Communication Engineering (ECE)  
Electronics & Hardware Product Development Engineer Internship


---

## Week 2 – Electronic Schematic Design and Simulation Planning

Week 2 develops the preliminary electronic architecture and simulation strategy for SPELCT. It covers the protected test interface, analog front end, ESP32-S3 controller, power management, display/user interface, SPICE simulation test cases, signal-integrity considerations, design risks, and refinement process.

➡️ **[Open Week 2 Documentation](Week-2/README.md)**

**Current internship progress:**  
- ✅ Week 1 – Product Conceptualization and Requirement Analysis  
- ✅ Week 2 – Electronic Schematic Design and Simulation Planning
