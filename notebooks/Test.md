# Test Mermaid Conversion

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

## Section 1: Before Mermaid

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

```mermaid
flowchart TB
    A[Start] --> B{Decision}
    B -->|Yes| C[Do Something]
    B -->|No| D[Do Something Else]
    C --> E[End]
    D --> E
    
    style A fill:#e3f2fd
    style E fill:#e8f5e9
```

### Section 2: After Mermaid

Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

# Test Notebook 2 - Additional Mermaid Test

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

## New Section Before Diagram

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.

```mermaid
flowchart TB
    A[Lorem] --> B{Ipsum}
    B -->|Dolor| C[Sit Amet]
    B -->|Consectetur| D[Adipiscing Elit]
    C --> E[Sed Do]
    D --> E
    E --> F[Eiusmod Tempor]
    
    style A fill:#e3f2fd
    style F fill:#e8f5e9
```

### New Section After Diagram

Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.

# Scientific Research Notebook - Data Analysis Pipeline

This notebook documents the experimental methodology and results for compound XR-247 efficacy analysis.

## 1. Experimental Timeline

Project timeline showing key phases of the research study from initial setup through final analysis.

```mermaid
gantt
    title Compound XR-247 Study Timeline
    dateFormat  YYYY-MM-DD
    section Phase 1
    Literature Review     :done,    des1, 2024-01-01, 30d
    Protocol Design       :done,    des2, after des1, 20d
    section Phase 2
    Sample Preparation    :active,  des3, 2024-02-20, 15d
    Initial Testing       :         des4, after des3, 25d
    section Phase 3
    Data Collection       :         des5, after des4, 30d
    Statistical Analysis  :         des6, after des5, 20d
```

## 2. Sample Distribution Analysis

Distribution of test samples across different experimental conditions showing concentration ranges.

```mermaid
pie title Sample Distribution by Concentration
    "0.1 mM" : 25
    "0.5 mM" : 35
    "1.0 mM" : 20
    "2.0 mM" : 15
    "Control" : 5
```

## 3. Laboratory Protocol Sequence

Standard operating procedure for compound preparation and testing workflow.

```mermaid
sequenceDiagram
    participant Tech as Lab Technician
    participant LIMS as LIMS System
    participant Inst as Instrument
    participant QC as Quality Control
    
    Tech->>LIMS: Register sample
    LIMS->>Tech: Generate barcode
    Tech->>Inst: Load sample
    Inst->>Inst: Run analysis
    Inst->>LIMS: Upload results
    LIMS->>QC: Flag for review
    QC->>LIMS: Approve/Reject
    LIMS->>Tech: Final report
```

## 4. Cell State Transitions

Cellular response states observed during compound exposure over 72-hour period.

```mermaid
stateDiagram-v2
    [*] --> Healthy
    Healthy --> Stressed: Compound exposure
    Stressed --> Apoptotic: High dose
    Stressed --> Recovery: Low dose
    Recovery --> Healthy: 24h recovery
    Apoptotic --> [*]
    
    Healthy: Normal metabolic activity
    Stressed: Elevated ROS levels
    Apoptotic: Caspase activation
    Recovery: Homeostasis restoration
```

## 5. Data Processing Pipeline

Computational workflow for analyzing high-throughput screening results.

```mermaid
flowchart LR
    A[Raw Data] --> B{Quality Check}
    B -->|Pass| C[Normalization]
    B -->|Fail| D[Exclude]
    C --> E[Statistical Analysis]
    E --> F[Hit Selection]
    F --> G{Validation}
    G -->|Confirmed| H[Report Hits]
    G -->|Failed| I[Re-analyze]
    I --> E
    
    style A fill:#e1f5fe
    style H fill:#c8e6c9
    style D fill:#ffcdd2
```

## 6. Molecular Structure Classification

Hierarchical classification of compound derivatives based on functional groups.

```mermaid
classDiagram
    class Compound {
        +String name
        +Float molecularWeight
        +String formula
        +calculate_properties()
    }
    
    class Derivative {
        +String functionalGroup
        +Float activity
        +test_efficacy()
    }
    
    class AlphaDerivative {
        +String alphaSubstituent
        +measure_binding()
    }
    
    class BetaDerivative {
        +String betaSubstituent
        +assess_selectivity()
    }
    
    Compound <|-- Derivative
    Derivative <|-- AlphaDerivative
    Derivative <|-- BetaDerivative
```








