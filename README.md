# Forecasting mobile network traffic

This repository contains the implementation of a ML pipeline to forecast mobile network traffic in the city of Milan. 
The project was developed as part of the selection process for a doctoral position at IMDEA Networks Institute.

## Project Structure

```text
.
├── data/
│   ├── milano-grid.geojson  # Spatial grid of the city
│   └── telecom/             # Directory for traffic intensity files
|   └── df.parquet           # Data to run the prediction algorithm 
├── models/
│   └── best_model.json      # Pre-trained XGBoost hyperparameters
    └── best_params.json     # Parameters of the best performing model
├── tasks.ipynb              # Data analysis and inference script
├── requirements.txt         # Python dependencies
└── README.md                # This file
```

## Setup 

To set up the project on a **Linux** or **macOS** system, run the following commands in your terminal:

```bash
# Create a virtual environment to isolate dependencies
python3 -m venv venv

# Activate the virtual environment
source venv/bin/activate

# Install the required libraries
pip install -r requirements.txt
```

## Dataset Acquisition

The analysis is based on the "Telecommunications - SMS, Call, Internet - MI" dataset from the 2014 Big Data Challenge. 
To run the complete pipeline, please follow these steps:

1.  **Download the data**: Access the official repository at the following link:
     [Harvard Dataverse - Big Data Challenge Archive](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/EGZ9ES)

2.  **Organize the files**: Ensure the files are placed exactly as shown below to maintain compatibility with the relative paths in the source code:
    *   Place the traffic intensity files in: `data/telecom/`;
    *   Place the geographical grid file (`milano-grid.geojson`) in: `data/`.

