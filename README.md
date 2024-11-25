# Bankruptcy Prediction Dataset

This repository contains two benchmark datasets for corporate bankruptcy prediction, sourced from the Management Discussion and Analysis (MDA) sections of annual reports for publicly listed companies in the U.S. and China. These datasets are designed to facilitate reproducible research and model comparisons in the domain of financial distress prediction. 

Currently, each file in the dataset contains **ten samples**, evenly split between the two classes:
- **5 samples labeled as `0` (non-bankrupt instances)**, representing companies not facing financial distress.
- **5 samples labeled as `1` (bankrupt instances)**, representing companies experiencing financial distress.

**The complete dataset will be fully released after the publication of the related research article. **

## Data Description

The datasets are organized into two directories:
- **`data/US`**: Contains the dataset for U.S. publicly listed companies.
- **`data/CN`**: Contains the dataset for Chinese publicly listed companies.

Each dataset includes:
1. Preprocessed MDA texts aligned with bankruptcy labels.
2. Train, validation, and test splits with balanced distributions for model evaluation.

### Dataset Summary

| Dataset           | Time Span | Reports  | Non-Bankrupt Instances | Bankrupt Instances |
|-------------------|-----------|----------|------------------------|--------------------|
| **U.S. Dataset**  | 2000-2021 | 20,605   | 20,067                 | 538                |
| **Chinese Dataset** | 2000-2021 | 4,942    | 4,628                  | 314                |

### Label Distribution

#### U.S. Dataset
| Split      | Non-Bankrupt Instances | Bankrupt Instances |
|------------|-------------------------|--------------------|
| Training   | 16,050                 | 434                |
| Validation | 2,003                  | 58                 |
| Test       | 2,014                  | 46                 |

#### Chinese Dataset
| Split      | Non-Bankrupt Instances | Bankrupt Instances |
|------------|-------------------------|--------------------|
| Training   | 2,774                  | 190                |
| Validation | 923                    | 66                 |
| Test       | 931                    | 58                 |

## File Structure

```
├── data/
│   ├── US/
│   │   ├── train.csv    # Training set for U.S. dataset
│   │   ├── val.csv      # Validation set for U.S. dataset
│   │   ├── test.csv     # Test set for U.S. dataset
│   │   └── README.md    # Metadata and details about the U.S. dataset
│   ├── CN/
│   │   ├── train.csv    # Training set for Chinese dataset
│   │   ├── val.csv      # Validation set for Chinese dataset
│   │   ├── test.csv     # Test set for Chinese dataset
│   │   └── README.md    # Metadata and details about the Chinese dataset
└── README.md             # Overview of the datasets and usage instructions
```

### File Format
Each dataset is stored in CSV files with the following structure:
- `text`: The preprocessed MDA text.
- `label`: The binary label indicating bankruptcy status (`1` for bankrupt, `0` for non-bankrupt).

Example (U.S. Dataset):
| text                                           | label |
|------------------------------------------------|-------|
| "The company's revenues declined due to ..."  | 1     |
| "The management anticipates growth in ..."    | 0     |

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo-name/bankruptcy-dataset.git
   cd bankruptcy-dataset
   ```

2. Access the data:
   - For the U.S. dataset: Navigate to `data/US/`
   - For the Chinese dataset: Navigate to `data/CN/`

3. Load the data using your preferred Python data library:
   ```python
   import pandas as pd

   train_data = pd.read_csv('data/US/train.csv')
   val_data = pd.read_csv('data/US/val.csv')
   test_data = pd.read_csv('data/US/test.csv')
   ```

4. Use the datasets to train and evaluate your bankruptcy prediction models.

## Citation

If you use this dataset in your research, please cite the following paper:
```
@article{reference,
  title={Title},
  author={Name and Co-authors},
  journal={Journal Name},
  year={2024},
}
```

## License

This dataset is licensed under the [MIT License](https://opensource.org/license/mit).

## Contact

For questions or suggestions, please open an issue or contact [email].
