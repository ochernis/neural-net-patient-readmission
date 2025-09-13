# Neural Network for Patient Readmission Prediction

This repository contains a lab project for building and improving a deep learning model to predict patient readmission risk based on electronic health records (EHR).  
The project demonstrates baseline and advanced training techniques, with a strong focus on preventing overfitting and ensuring reliable performance in healthcare applications.

---

## 📂 Project Structure
- `nn_training_lab.ipynb` — main Jupyter notebook with all steps of the lab
- `readmission_data.csv` — dataset used for model training and evaluation
- `logs/fit/` — TensorBoard logs for visualizing training

---

## 🔑 Implemented Steps
1. **Data Preparation**  
   - Cleaned and encoded patient demographics, labs, and diagnoses  
   - Converted readmission target to binary (readmitted vs. not readmitted)  
   - Train/validation/test split with stratification  

2. **Baseline Model**  
   - Simple dense neural network (64 → 32 → 1) with ReLU activations  
   - Trained without callbacks for reference performance  

3. **Training Visualization**  
   - Plotted training/validation curves (loss and recall)  
   - Evaluated baseline overfitting tendencies  

4. **Callbacks & Improved Model**  
   - Added EarlyStopping, ModelCheckpoint, TensorBoard, and ReduceLROnPlateau  
   - Used BatchNormalization, LeakyReLU, Dropout, and gradient clipping  
   - Improved training stability and reduced overfitting  

5. **Analysis & Reflection**  
   - Compared baseline vs. improved performance  
   - Discussed importance of monitoring, data quality, and generalization  
   - Highlighted healthcare implications  

---

## 📊 Results
- **Baseline Test Recall:** ~0.60  
- **Improved Model Test Recall:** ~0.57 (with much more stable validation curves)  
- EarlyStopping triggered at **epoch 24 of 100**, avoiding wasted computation  
- TensorBoard visualizations confirmed reduced overfitting and smoother training  

---

## 🚀 How to Run
1. Clone this repository:  
   ```bash
   git clone https://github.com/<your-username>/neural-net-patient-readmission.git
   cd neural-net-patient-readmission
2.	Install dependencies (TensorFlow, scikit-learn, pandas, matplotlib).
3.	Open nn_training_lab.ipynb in Jupyter Notebook or JupyterLab.
4.	Run cells step by step.
5.	To view TensorBoard logs:
   %load_ext tensorboard
   %tensorboard --logdir=logs/fit

🏥 Why This Matters

Reliable patient readmission prediction models can help hospitals:
	•	Allocate resources more efficiently
	•	Identify high-risk patients earlier
	•	Reduce healthcare costs while improving patient outcomes

⸻

📌 Notes
	•	The dataset is for educational purposes only.
	•	Final performance is limited by data quality; further improvements require better and more representative patient records.

⸻

✨ Acknowledgments

This lab was developed as part of a deep learning training module for healthcare analytics.
