# **ECG Atrial Fibrillation Detection**
**Last Modified:** 25/03/2025  
**Project based on the PhysioNet/CinC Challenge 2017**  
**URL:** [PhysioNet Challenge 2017](https://www.physionet.org/challenge/2017/) 



## **Project Description**
This project aims to **detect atrial fibrillation (AF)** from single-lead ECG recordings.  
It was developed as part of the **AI in Healthcare course** by students from **MSc Data Science & Business Analytics (CentraleSupélec - ESSEC)**: **Dora VECSERNYES, Jinsuh YOU, and Julien DEHUT**.  

We applied **signal processing, machine learning, and deep learning** techniques to extract ECG features and train a classification model.  

---

## **Key Results**
- The best performance in the original PhysioNet Challenge was **0.83**.
- Our best model achieved an accuracy of **0.81**, which would rank us **9th out of 68** in the challenge.
- The biggest challenge was distinguishing between **Normal (N) and Other (O) classes**, due to **class imbalance** and subtle differences in ECG waveforms.
- Further improvements could include **ensemble models combining Random Forest and CNNs**.

---

## **Folder Structure**
### ** Notebooks**
| Notebook | Description |
|----------|------------|
| `ECG_Exploration.ipynb` | Exploratory Data Analysis (EDA) on original ECG signals records *.mat (possible to run the code only if you download the original dataset available at the URL given above) and the origial dataset merging into a *.csv file. |
| `RF_windowed.ipynb` | Preprocessing & Random Forest trained on **windowed ECG segments (5s segments with 4s overlap)**. |
| `RF_FFT_Wavelet.ipynb` | Preprocessing & Random Forest trained using **FFT and Wavelet transformations**. |
| `CNN_ensemble.ipynb` | Training different CNN architectures and combining them in an **ensemble model**. |

### ** Data & Reports**
| File | Description |
|------|------------|
| `full_ecg_with_answers.csv` | Merged dataset containing **8,528 ECG recordings** (original `.mat` files converted to CSV). |
| `ECG_Analysis.pdf` | **Slides presenting the project**. |
| `Final_report.pdf` | **Final report** with detailed methodology, results, and conclusions. |

---

## **Installation & Execution**
### ** Prerequisites**
Install required Python libraries:
bash
pip install numpy pandas matplotlib seaborn scikit-learn imbalanced-learn pywt tensorflow

Ensure you have Python 3.8+ and a GPU (optional for deep learning models).

### ** Running the Notebooks**
1. Clone this repository:
bash
git clone https://github.com/YourUsername/ECG_AF_Classification.git
cd ECG_AF_Classification

2. Open Jupyter Notebook:
bash
jupyter notebook

3. Open the ECG_Exploration.ipynb to explore the dataset, Don't run it, or run it only if you downloaded the original datasets of the challenge

4. Train models using RF_windowed.ipynb, RF_FFT_Wavelet.ipynb, or CNN_ensemble.ipynb.

---

## **Future Work**
- Validate the model on an independent dataset to confirm generalizability.
- Improve feature engineering (e.g., test additional entropy measures, fractal dimensions).
- Combine Random Forest & CNN models for a more robust classification.
- Optimize hyperparameters using Bayesian Optimization or Genetic Algorithms.

---

## **License**
This project is for educational purposes only.
If you use or modify the code, please cite the PhysioNet Challenge 2017 as the original dataset provider.

---

**Questions or suggestions?** Feel free to open an issue to contact us! 
