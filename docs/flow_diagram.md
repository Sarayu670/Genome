# Genomic Interaction Classification System - Input-Output Flow Diagram

## How to Read This Diagram

This diagram shows how our genomic interaction classification system works, from start to finish. Think of it like a map showing how data moves through our system.

### Simple Guide to Understanding the Flow:

1. **Start at the Top**
   - The diagram flows from top to bottom
   - Data enters at the top and moves down through different stages

2. **Follow the Arrows**
   - Arrows (→) show how data moves from one step to the next
   - Each arrow represents a transformation or processing step

3. **Main Sections (Left to Right)**
   - **Data Collection**: Where we get our information
   - **Data Cleaning**: Making the data ready for use
   - **Model Building**: Creating our prediction system
   - **Web Interface**: How users interact with the system
   - **Results**: What users get at the end

4. **Color-Coded Boxes**
   - Each colored box represents a different process
   - Connected boxes show related steps

5. **Subprocesses**
   - Smaller boxes inside main boxes show detailed steps
   - These explain what happens within each main process

### Quick Reference:

- **Input**: Where data enters the system
- **Processing**: How we prepare the data
- **Model**: Our prediction system
- **Interface**: How users interact
- **Output**: Final results users receive

```mermaid
graph TD
    %% Input Layer
    A[Input Data] --> B[Data Loading & Preprocessing]
    
    %% Data Processing Layer
    B --> C[Feature Engineering]
    C --> D[Data Balancing]
    
    %% Model Development Layer
    D --> E[Model Training]
    E --> F[Model Evaluation]
    F --> G[Model Deployment]
    
    %% Web Interface Layer
    G --> H[Web Interface]
    H --> I[User Input]
    I --> J[Prediction Processing]
    J --> K[Results Visualization]
    
    %% Detailed Subprocesses
    subgraph "Data Loading & Preprocessing"
        B1[Load .csv/.xlsx Files] --> B2[Check Data Integrity]
        B2 --> B3[Handle Missing Values]
        B3 --> B4[Remove Duplicates]
        B4 --> B5[Format Data]
    end
    
    subgraph "Feature Engineering"
        C1[Statistical Analysis] --> C2[Feature Extraction]
        C2 --> C3[Feature Transformation]
        C3 --> C4[Feature Selection]
    end
    
    subgraph "Data Balancing"
        D1[Class Distribution Analysis] --> D2[SMOTE Oversampling]
        D2 --> D3[Undersampling]
        D3 --> D4[Balanced Dataset]
    end
    
    subgraph "Model Development"
        E1[Algorithm Selection] --> E2[Parameter Tuning]
        E2 --> E3[Cross-validation]
        E3 --> E4[Model Training]
    end
    
    subgraph "Web Interface"
        H1[Frontend UI] --> H2[Data Upload]
        H2 --> H3[Preprocessing]
        H3 --> H4[Prediction]
        H4 --> H5[Results Display]
    end
    
    %% Input Types
    A1[Genomic Interaction Data] --> A
    A2[User Uploaded Data] --> I
    
    %% Output Types
    K --> O1[Classification Results]
    K --> O2[Visualizations]
    K --> O3[Downloadable Reports]
```

## Flow Description

1. **Input Layer**
   - Initial genomic interaction data (81,203 interactions)
   - User-uploaded data through web interface

2. **Data Processing Layer**
   - Data loading and preprocessing
   - Feature engineering and transformation
   - Data balancing using SMOTE and undersampling

3. **Model Development Layer**
   - Random Forest model training
   - Hyperparameter tuning
   - Cross-validation and evaluation

4. **Web Interface Layer**
   - User-friendly interface for data upload
   - Real-time prediction processing
   - Interactive results visualization

5. **Output Layer**
   - Classification results
   - Interactive visualizations
   - Downloadable reports

## Key Components

- **Data Processing**: Ensures data quality and prepares features for modeling
- **Model Development**: Implements and optimizes the Random Forest classifier
- **Web Interface**: Provides easy access to the classification system
- **Results**: Delivers comprehensive and interpretable outputs

## Data Flow

1. Raw data → Preprocessed data
2. Preprocessed data → Feature-engineered data
3. Feature-engineered data → Balanced dataset
4. Balanced dataset → Trained model
5. User input → Processed prediction
6. Processed prediction → Visualized results 