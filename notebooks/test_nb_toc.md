<!-- TOC -->
# Table of Contents

- [Introduction](#introduction)
- [Methods](#methods)
  - [Data Collection](#data-collection)
- [Methods](#methods)
  - [Data Collection](#data-collection)
  - [Statistical Analysis](#statistical-analysis)
- [Results](#results)
  - [Primary Outcomes](#primary-outcomes)
  - [Secondary Analysis](#secondary-analysis)
    - [Subgroup Analysis](#subgroup-analysis)
- [Conclusion](#conclusion)
- [Enzyme Kinetics Analysis](#enzyme-kinetics-analysis)

<!-- /TOC -->


# Test Notebook for TOC Generation

This notebook tests automatic table of contents generation.

```mermaid
graph TD
    A[Start] --> B[Generate TOC]
    B --> C[Parse Headers]
    C --> D[Create Links]
    D --> E[Insert TOC]
    
    style A fill:#e3f2fd
    style E fill:#c8e6c9

## Introduction

Basic introduction section.

```mermaid
flowchart LR
    A[Raw Data] --> B[Processing]
    B --> C[Analysis]
    C --> D[Results]
    
    style A fill:#fff3e0
    style D fill:#e8f5e9

## Methods

### Data Collection

Details about data collection.

```mermaid
sequenceDiagram
    participant User
    participant System
    participant Database
    
    User->>System: Submit data
    System->>Database: Store
    Database-->>System: Confirm
    System-->>User: Success

## Methods

### Data Collection

Details about data collection.

```mermaid
sequenceDiagram
    participant User
    participant System
    participant Database
    
    User->>System: Submit data
    System->>Database: Store
    Database-->>System: Confirm
    System-->>User: Success
```

### Statistical Analysis

Analysis methodology.

```mermaid
pie title Sample Distribution
    "Group A" : 40
    "Group B" : 35
    "Control" : 25
```

## Results

### Primary Outcomes

Main findings.

```mermaid
graph TD
    A[Treatment Group] --> B{Response}
    B -->|Positive| C[85%]
    B -->|Negative| D[15%]
    C --> E[Significant p<0.001]
    
    style C fill:#c8e6c9
    style E fill:#81c784
```

### Secondary Analysis

Additional results.

```mermaid
flowchart TB
    subgraph Baseline
        B1[N=100]
    end
    subgraph Week4
        W1[N=95]
    end
    subgraph Week8
        W2[N=92]
    end
    B1 --> W1
    W1 --> W2
```

#### Subgroup Analysis

Detailed breakdown.

```mermaid
pie title Response by Age Group
    "18-30 years" : 30
    "31-50 years" : 45
    "51+ years" : 25
```

## Conclusion

Summary and future work.

```mermaid
gantt
    title Research Timeline and Future Directions
    dateFormat YYYY-MM-DD
    section Completed
    Initial Study     :done, 2024-01-01, 2024-06-30
    Data Analysis     :done, 2024-07-01, 2024-09-30
    section In Progress
    Manuscript Prep   :active, 2024-10-01, 2024-12-31
    section Future Work
    Follow-up Study   :2025-01-01, 2025-06-30
    Clinical Trial    :2025-07-01, 2026-06-30
```

## Enzyme Kinetics Analysis

Michaelis-Menten kinetics describe the rate of enzymatic reactions by relating reaction velocity to substrate concentration.

```mermaid
graph LR
    S[Substrate S] -->|k1| ES[ES Complex]
    ES -->|k-1| S
    ES -->|k2| EP[EP Complex]
    EP -->|k3| E[Enzyme E] 
    EP --> P[Product P]
    E -->|k1| ES
    
    style S fill:#ffecb3
    style P fill:#a5d6a7
    style ES fill:#ce93d8
    style EP fill:#ce93d8
```

The steady-state assumption yields: v = (Vmax[S])/(Km + [S]) where Km = (k-1 + k2)/k1














