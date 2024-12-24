# ASL Fingerspelling Data Preprocessing and Feature Engineering

This project focuses on preprocessing and feature engineering for the American Sign Language (ASL) Fingerspelling dataset. It prepares the data for further analysis and modeling by transforming raw input into a structured and memory-efficient format. The code is designed to handle large-scale datasets, such as those found in Kaggle competitions.

## Features

- **Data Preprocessing**: Efficient handling of CSV and Parquet files.
- **Visualization**: Interactive and static plots for understanding data distribution.
- **Memory Optimization**: Techniques to reduce memory usage during processing.
- **Feature Engineering**: Extracts meaningful features from landmark data.
- **Parallel Processing**: Speeds up computations using multiprocessing.

## Requirements

Ensure you have the following installed:

- Python 3.x
- Libraries:
  - `pandas`
  - `numpy`
  - `torch`
  - `tensorflow`
  - `seaborn`
  - `matplotlib`
  - `plotly`
  - `scikit-learn`
  - `tqdm`

Install dependencies using pip:
```bash
pip install pandas numpy torch tensorflow seaborn matplotlib plotly scikit-learn tqdm
```

## Data

The project uses the ASL Fingerspelling dataset available on Kaggle. Ensure the following files are in the working directory:

- `train.csv`: Contains training data.
- `supplemental_metadata.csv`: Additional metadata.
- `train_landmarks/*.parquet`: Landmark data files.

## How to Run

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-name>
   ```

2. Place the dataset files in the appropriate directories.

3. Run the preprocessing script:
   ```bash
   python preprocessing.py
   ```

4. Processed features and labels will be saved as:
   - `feature_data.npy`
   - `feature_labels.npy`

## Code Overview

### Preprocessing
- Loads and inspects the dataset (CSV and metadata).
- Cleans and formats the data for consistency.

### Visualization
- Plots participant distribution, phrase lengths, and other key metrics.

### Feature Engineering
- Extracts hand landmark features (e.g., mean, standard deviation).
- Handles missing values and aligns feature dimensions.

### Memory Optimization
- Reduces dataframe memory footprint by optimizing data types.

### Parallel Processing
- Uses multiprocessing for efficient file processing.

## Example Output

- **Data Inspection:**
  ```plaintext
  Total number of files: 10000
  Total number of unique phrases: 120
  ```

- **Feature Shape:**
  ```plaintext
  Features tensor shape: (10000, 3258)
  Labels tensor shape: (10000, 30)
  ```

## Contribution

Feel free to contribute by submitting issues or pull requests. Ensure your code follows the existing style and includes necessary documentation.





