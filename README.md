# Streamy Video Streaming Backend Platform
## Software Technology Course Laboratory 1
* **Student Identity:** [WangYishuo]
* **Neptun System Code:** [BZTPMA]
* **Course Section Reference:** GEIAL314-B2a
---
## Iterative SDLC Blueprint
The diagram below presents the iterative SDLC workflow for Streamy video streaming backend platform.
It demonstrates the four-phase iterative workflow: requirements specification, UML architectural modeling, validation gate check, and Python implementation.

```mermaid
flowchart TD
    subgraph SpecPhase [1. Requirements Specification Block]
        A[Inception Abstract Created] --> B[SRS Requirements Compiling]
    end
    subgraph DesignPhase [2. UML Architectural Modeling]
        B --> C[Draft System Border Graphs]
        C --> D[Construct Advanced Class Models]
    end
    subgraph ValidationGate [3. Verification Gatekeeper Loop]
        D --> E{Does Architecture Match Code Specs?}
        E -- No: Refactor Blueprint --> B
    end
    subgraph ProductionPhase [4. Python Construction Layer]
        E -- Yes: Pass Gate --> F[Compile Python Class Skeletons]
        F --> G[Implement Internal Business Logic]
    end
    classDef decisionStyle fill:#f9f,stroke:#333,stroke-width:2px
    class E decisionStyle