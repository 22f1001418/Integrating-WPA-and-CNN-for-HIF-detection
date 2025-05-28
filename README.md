
# ⚡ Fault Detection in Transmission Lines Using 1D CNN & Wavelet Packet Decomposition

This project presents a **machine learning-based diagnostic system** for detecting **high-impedance faults (HIFs)** in power transmission lines using a combination of **wavelet packet decomposition**, **feature engineering**, and a **1D Convolutional Neural Network (1D-CNN)**.

---

## 🚀 Project Pipeline

1. **Real-Time Data Generation**  
   - Current signals generated using a Simulink model for normal and fault conditions.

2. **Chunking of Data**  
   - Data is grouped into chunks of **2000 samples** (representing 10 ms of activity).

3. **Wavelet Packet Decomposition (WPD)**  
   - Applied **3-level decomposition** to each chunk.
   - Focused on the **‘aad’ node** based on spectral analysis.

4. **Feature Extraction**  
   - Computed **16 statistical features** per node per chunk (mean, std, skewness, kurtosis, etc.).

5. **Feature Selection**  
   - Used One-Way ANOVA, Bhattacharyya Distance, and T-Test.
   - Selected **kurtosis of the ‘aad’ node** as the key feature.

6. **Model Training with 1D CNN**  
   - Input: 1D array of kurtosis values.
   - Model: Custom 1D CNN built using Keras/TensorFlow.
   - Training: Early stopping, batch normalization, dropout used to optimize performance.

7. **Prediction & Evaluation**  
   - Model predicts fault or normal condition.
   - Evaluated with **accuracy**, **precision**, **recall**, **F1-score**, and **confusion matrix**.

---

## 🛠 Tech Stack

- **Simulink / MATLAB** – Signal generation & wavelet analysis  
- **Python** – Data processing & modeling  
- **Pandas, NumPy, SciPy** – Feature extraction & statistics  
- **TensorFlow / Keras** – CNN model development  
- **Matplotlib / Seaborn** – Visualization  

## 📬 Contact

For any queries or collaborations, feel free to connect:  
📧 kshitijmaheshwari9@gmail.com

🔗 https://www.linkedin.com/in/kshitij-maheshwari-66b9b4307/
