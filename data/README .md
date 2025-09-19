# Skin Cancer Segmentation

This repository contains multiple deep learning approaches for skin lesion segmentation using the **ISIC 2018 dataset**.

# Project Structure
```
Skin_Cancer_Segmentation/
│
├─ README.md
├─ requirements.txt
├─ .gitignore
├─ notebooks/
│   ├─ UNet.ipynb
│   ├─ enhancedunet.ipynb
│   ├─ teacher-student.ipynb
│   └─ ...
└─ data/
    ├─ README.md (instructions to download dataset)
    └─ sample_images/
```

---

##  Results & Model Comparison

We tested multiple segmentation models:

| Model              | Dice Coefficient | Notes                                     |
|--------------------|------------------|---------------------------------------- --|
| **UNet++**         | **0.8811**       | Best performance overall                  |
| **Teacher Model**  | 0.8714           | Slightly lower than student               |
| **Student Model**  | 0.8816           | Comparable to UNet++, outperformed teacher|
| **UNet (baseline)**| 0.8235           | Lowest among the tested models            |

### Key Insights
- **UNet++ achieved the best Dice/IoU scores.**
- In the **teacher-student framework**, the **student model outperformed the teacher**.
- Baseline **UNet** was significantly weaker.

---

## Dataset
You can use:
- [ISIC 2018 official dataset](https://challenge.isic-archive.com/data/)
- [ISIC 2018 Kaggle version](https://www.kaggle.com/datasets/trantoanthang/isic-2018)

Download the dataset and place it inside the `data/` folder.

---

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/Hithesh1768/Skin_Cancer_Segmentation.git
   cd Skin_Cancer_Segmentation
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Open and run the notebooks:
   - `notebooks/UNet.ipynb`
   - `notebooks/enhancedunet.ipynb`
   - `notebooks/teacher-student.ipynb`

---

## Credits
- UNet, UNet++, and Enhanced UNet implementations
- Teacher-Student Knowledge Distillation
- ISIC 2018 Dataset
