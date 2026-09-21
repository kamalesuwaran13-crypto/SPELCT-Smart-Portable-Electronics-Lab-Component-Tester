# SPELCT Product Requirements – Week 1

| ID | Requirement | Type | Priority | Planned Verification |
|---|---|---|---|---|
| FR-01 | Identify supported common component categories automatically | Functional | Must | Known reference components |
| FR-02 | Measure resistance over a defined educational range | Functional | Must | Compare with reference resistors |
| FR-03 | Measure capacitance over a defined educational range | Functional | Must | Compare with reference capacitors |
| FR-04 | Test diode polarity and forward voltage within defined limits | Functional | Must | Reference diode tests |
| FR-05 | Identify supported BJT/MOSFET type and terminals | Functional | Should | Known semiconductor set |
| FR-06 | Provide continuity/basic connection checking | Functional | Should | Open/short tests |
| FR-07 | Display results on an integrated color display | UI | Must | Functional/usability test |
| FR-08 | Show messages for unsupported/unsafe input conditions | Safety/UI | Must | Fault-condition tests |
| FR-09 | Support optional result logging/export | Connectivity | Could | Interface test |
| NFR-01 | Operate within defined low-voltage test limits | Safety | Must | Electrical verification |
| NFR-02 | Include input protection suitable for declared limits | Safety | Must | Protection validation |
| NFR-03 | Provide repeatable measurements within target tolerance | Performance | Must | Repeated reference tests |
| NFR-04 | Complete typical tests in a practical student workflow time | Performance | Should | Timing tests |
| NFR-05 | Be portable and rechargeable | Usability | Should | Runtime/charging test |
| NFR-06 | Support calibration and firmware updates | Maintainability | Should | Firmware review |

## Design Principle
The prototype will remain a low-voltage educational device. Exact measurement ranges, tolerances, and protection limits will be finalized during detailed circuit design and verified experimentally rather than assumed.
