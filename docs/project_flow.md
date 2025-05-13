```mermaid
graph TD
    A[Input Data] --> B[Data Processing]
    B --> C[Feature Engineering]
    C --> D[Model Training]
    D --> E[Prediction System]
    
    E --> F1[Web Interface]
    E --> F2[Command Line Tools]
    
    F1 --> G1[Interactive Predictions]
    F2 --> G2[Batch Predictions]
    
    G1 --> H[Results & Visualizations]
    G2 --> H

    style A fill:#f9f,stroke:#333,stroke-width:2px
    style D fill:#bbf,stroke:#333,stroke-width:2px
    style E fill:#bfb,stroke:#333,stroke-width:2px
    style H fill:#fbb,stroke:#333,stroke-width:2px
```

# Project Flow Explanation

## 1. Input Data
- Genomic interactions dataset
- Features like supporting pairs, distances, and interaction types

## 2. Data Processing
- Data cleaning and preprocessing
- Handling missing values
- Data normalization

## 3. Feature Engineering
- Creating relevant features
- Feature selection
- Feature scaling

## 4. Model Training
- Random Forest model training
- Model validation
- Performance evaluation

## 5. Prediction System
- Two interfaces:
  - Web Application
  - Command Line Tools

## 6. Results & Visualizations
- Prediction outputs
- Statistical analysis
- Visual representations
- Performance metrics 