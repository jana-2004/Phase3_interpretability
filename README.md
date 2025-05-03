# Phase 3 - Interpretability

## Step 1: Upload Dataset from Kaggle to Colab

###  Dataset Link:
[Cardiovascular Disease Dataset](https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset)

###  Method A: Manual Upload
1. Download the dataset (`cardio_train.csv`) from Kaggle.
2. In Google Colab, click on the folder icon (left sidebar).
3. Click "Upload" and select the `cardio_train.csv` file.

###  Method B: Use Kaggle API (Recommended)

```python
# Install Kaggle API
!pip install kaggle

# Upload your kaggle.json file
from google.colab import files
files.upload()  # Upload kaggle.json here

# Move kaggle.json to the correct directory
!mkdir -p ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json

# Download the dataset
!kaggle datasets download -d sulianova/cardiovascular-disease-dataset

# Unzip the dataset
!unzip cardiovascular-disease-dataset.zip
```
## Step 2: Upload Notebooks to Colab

1. Download the notebook files (`.ipynb`) provided for this project.
2. Open [Google Colab](https://colab.research.google.com).
3. Click **File** → **Upload notebook**.
4. Select the `.ipynb` files from your local machine to upload them.


## Optional Step: Use GPU to Speed Up Execution

1. In the Colab menu, click **Runtime** → **Change runtime type**.
2. Under **Hardware accelerator**, choose `GPU`.
3. Click **Save**.
