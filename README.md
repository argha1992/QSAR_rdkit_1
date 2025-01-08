
# QSAR Analysis for EGFR Kinase Activity

This repository contains a Jupyter Notebook for performing QSAR (Quantitative Structure-Activity Relationship) analysis on EGFR kinase inhibitors. The workflow includes filtering molecules based on activity, calculating molecular descriptors, and applying Lipinski's Rule of Five for drug-likeness assessment using RDKit.

## Features

1. **Database Processing**:
   - Convert dataset ('data1.txt' to 'data1.csv')
   - Loads a dataset (`data1.csv`) containing molecule information, including SMILES strings and IC50 values.
   - Filters active molecules with IC50 values between 0 and 10 nM.

3. **Descriptor Calculation**:
   - Computes physicochemical descriptors for active molecules:
     - Molecular Weight (MW)
     - LogP
     - Number of Hydrogen Bond Acceptors (HBA)
     - Number of Hydrogen Bond Donors (HBD)
     - Number of Rotatable Bonds

4. **Lipinski's Rule of Five Compliance**:
   - Filters molecules that satisfy Lipinski's Rule of Five:
     - MW ≤ 500
     - LogP ≤ 5
     - HBA ≤ 10
     - HBD ≤ 5

5. **Output Generation**:
   - Exports results to CSV files:
     - `active_molecules_descriptors.csv`: Physicochemical descriptors for active molecules.
     - `lipinski_accepted_molecules.csv`: Molecules passing Lipinski's Rule.

## Prerequisites

- **Python**: Version 3.7 or higher.
- **Jupyter Notebook**: To run the provided `.ipynb` file.
- **RDKit**: For cheminformatics calculations.

Install RDKit using:
```bash
conda install -c conda-forge rdkit
```

## Usage

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/argha1992/QSAR_rdkit_1.git
   cd QSAR-EGFR-Analysis
   ```

2. **Run the Notebook**:
   Open the Jupyter Notebook (`rdkit.ipynb`) in your environment:
   ```bash
   jupyter notebook rdkit.ipynb
   ```

3. **Follow the Steps**:
   - Load the dataset and classify molecules based on IC50 values.
   - Execute the cells to calculate descriptors and apply Lipinski's Rule.
   - View and export filtered results.

## Outputs

- `active_molecules_descriptors.csv`: Descriptors of active molecules.
- `lipinski_accepted_molecules.csv`: Molecules satisfying Lipinski's Rule of Five.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Author

[Argha Mitra](https://github.com/argha1992)

## Acknowledgements

- Developed using RDKit, an open-source cheminformatics toolkit.
