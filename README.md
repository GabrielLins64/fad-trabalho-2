<h1>LEGO Bricks Dataset Analysis</h1>

This repository contains the code and report for analyzing the LEGO Bricks dataset. The dataset is split into training and testing sets, and various analyses are performed to understand the data and address the given work questions. 

---

- [Dataset Description](#dataset-description)
- [Dataset Split](#dataset-split)
- [SVD Analysis](#svd-analysis)
- [Dimensionality Reduction](#dimensionality-reduction)
- [Accuracy Analysis](#accuracy-analysis)
- [Repository Structure](#repository-structure)
- [Requirements](#requirements)
- [Usage](#usage)
- [License](#license)
- [References](#references)

---

## Dataset Description

The LEGO Bricks dataset [1] contains 40,000 images of 50 different LEGO bricks, where all 50 bricks are rendered by 800 different angels. The images were computer rendered using the Autodesk Maya 2020, by Joost Hazelzet. It's under the GPL 2 license.

## Dataset Split

The first step in the analysis is to split the LEGO Bricks dataset into training and testing sets. The dataset is divided into two parts to train the classification model and evaluate its performance. The split ensures that the model is trained on a representative sample of the data and then tested on unseen samples.

## SVD Analysis

To gain insights into the dataset, the Singular Value Decomposition (SVD) of the centralized training matrix (X train) is calculated. SVD is a matrix factorization technique that decomposes a matrix into its singular values and corresponding singular vectors [2]. By analyzing the singular values, we can understand the variability present in the data.

A chart is plotted to visualize the relationship between the singular values and the cumulated variability. This chart helps determine the significance of each singular value in capturing the variability in the data.

## Dimensionality Reduction

Based on the chart of singular values and cumulated variability, a suitable threshold is selected to reduce the dimensionality of the classification problem. By retaining only a certain number of significant singular values, we can reduce the dimensionality of the dataset while preserving most of the information [2].

## Accuracy Analysis

To evaluate the impact of dimensionality reduction on the classification model, a plot is generated showing the number of singular values used against the accuracy of the model. This analysis helps determine the trade-off between dimensionality reduction and classification performance.

## Repository Structure

The repository is organized as follows:

- `dataset/`: Directory containing the LEGO Bricks dataset
- `fad-gabriel_lins.ipynb`: Notebook containing the code for dataset splitting, SVD analysis, dimensionality reduction, and accuracy analysis

Feel free to explore the code and report to understand the analysis process and findings.

## Requirements

To run the code and reproduce the analysis, the following dependencies are required:

- [Python (version 3.10)](https://www.python.org/downloads/)
- [Dataset LEGO Bricks](https://www.kaggle.com/datasets/joosthazelzet/lego-brick-images)
- [Python-Poetry](https://python-poetry.org/)
- [Jupyter Notebook](https://jupyter.org/)

Please ensure that the necessary dependencies are installed before running the code.

## Usage

1. Clone this repository to your local machine.
2. Ensure that the dataset is placed in the `dataset/` directory.
3. Activate the virtual environment:

```shell
poetry shell
```

4. Install the required dependencies mentioned in the `pyproject.toml` file.

```shell
poetry install
```

5. Install the virtual environment in the ipykernel

```shell
chmod +x installkernel.sh
./installkernel.sh
```

6. Run the notebook `fad-gabriel_lins.ipynb` to perform the analysis.

## License

The LEGO Bricks dataset used in this analysis is subject to GPL-2 license. Please refer to the dataset documentation for more information.

The code in this repository is licensed under the [MIT License](LICENSE).

## References

[1] Hazelzet, Joost. "LEGO Brick Images." Kaggle, 2019. Accessed June 20, 2023. Available at: https://www.kaggle.com/datasets/joosthazelzet/lego-brick-images

[2] Álgebra Linear: Teoria e Aplicações, por Thelmo de Araujo. Rio de Janeiro: SBM, 2014.
