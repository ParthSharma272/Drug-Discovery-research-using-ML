# Leishmaniasis Drug Discovery: Machine Learning Approach

## **Overview**
This repository showcases the development and implementation of a machine learning-based solution to accelerate drug discovery for the treatment of **Leishmaniasis**, a neglected tropical disease. This project was undertaken as part of a summer internship at Guru Gobind Singh Indraprastha University.

<p align="center">
  <img width="398" alt="Overview Image" src="https://github.com/user-attachments/assets/ea1061e1-0a7d-471c-8eb3-b0b9d79c06ab" />
</p>

---

## **Abstract**
Drug discovery is a time-intensive and costly endeavor. This project applies machine learning (ML) techniques to predict the bioactivity of chemical compounds against *Leishmania* parasites, leveraging molecular fingerprinting methods and various ML classifiers. The study identifies key molecular features and develops ensemble models to improve prediction accuracy, reducing the overall cost and time for drug development.

---

## **Table of Contents**
- [Background](#background)
- [Project Objectives](#project-objectives)
- [Dataset and Preprocessing](#dataset-and-preprocessing)
- [Methodology](#methodology)
- [Results](#results)
- [Key Insights](#key-insights)
- [Future Directions](#future-directions)
- [Technologies Used](#technologies-used)
- [Acknowledgments](#acknowledgments)

---

## **Background**
Leishmaniasis is caused by protozoan parasites transmitted via infected sandflies. The disease manifests in three primary forms:
1. **Cutaneous Leishmaniasis** – skin ulcers.
2. **Mucocutaneous Leishmaniasis** – tissue deformities.
3. **Visceral Leishmaniasis** – life-threatening organ damage.

Current drug discovery methods for Leishmaniasis are costly, slow, and prone to inefficiencies. Emerging drug resistance further underscores the need for innovative solutions. Machine learning accelerates this process by identifying promising compounds more effectively.

---

## **Project Objectives**
1. Develop an ML pipeline to classify chemical compounds as active or inactive against *Leishmania*.
2. Leverage molecular fingerprinting techniques like **Morgan**, **MACCS**, **RDKit**, and **Atom Pair**.
3. Evaluate and optimize models using ensemble techniques for higher accuracy.
4. Identify critical molecular features contributing to compound activity.

---

## **Dataset and Preprocessing**
### **Source**
Data was sourced from the **ChEMBL Database**, comprising:
- 278,045 initial entries.
- Final dataset reduced to **10,418 entries** after extensive preprocessing.

### **Why Reduce the Dataset?**
1. **Duplicate Removal**: Reduced to 94,435 unique compounds.
2. **Bioactivity Filtering**: Retained IC50, Percent Effect, Inhibition, and EC50 values.
3. **Unit Standardization**: Converted all values to nanomolar (nM).
4. **Binary Classification**: 
   - Active: <10,000 nM
   - Inactive: >10,000 nM

---

## **Methodology**

### **Feature Engineering**
- Generated molecular fingerprints: **Morgan**, **MACCS**, **RDKit**, **Atom Pair**.
- Applied PCA and t-SNE for visualization.

<p align="center">
  <img width="425" alt="PCA Plot" src="https://github.com/user-attachments/assets/9e6e030e-02a5-410d-832f-59b8ef3f7299" />
  <img width="432" alt="t-SNE Plot" src="https://github.com/user-attachments/assets/8822eee9-d192-440c-a45c-89cb5bec644a" />
</p>

### **Algorithms Used**
- **Classical Models**: Random Forest, Logistic Regression, Gradient Boosting, KNN, SVC, Decision Tree, AdaBoost.
- **Ensemble Models**: VotingClassifier.
- **ANN**: Multi-Layer Perceptron (MLP) for deeper insights.

### **Evaluation Metrics**
- Accuracy
- Precision
- Recall
- F1 Score

---

## **Results**

### **Best Results**
- **Best Fingerprint**: RDKit
- **Optimal Model**: Random Forest + RDKit
- **Accuracy Achieved**: 90%
- **Key Feature Identified**: RDKit_747

<p align="center">
  <img width="437" alt="Heatmap1" src="https://github.com/user-attachments/assets/3e8d7ecc-5e26-4f1c-9bd3-265995728e95" />
  <img width="457" alt="Heatmap2" src="https://github.com/user-attachments/assets/fc60ca40-2831-4044-9ba3-eca5ce57b916" />
</p>

---

## **Key Insights**
- **Feature Importance**: Identified critical molecular features influencing activity.
- **Data Constraints**: Limited high-quality data posed challenges but were mitigated using advanced preprocessing.
- **Ensemble Strength**: Ensemble techniques improved prediction reliability and accuracy.

---

## **Future Directions**
1. Expand the dataset to include more high-quality entries.
2. Experiment with deep learning models (e.g., Graph Neural Networks).
3. Investigate new molecular descriptors and cheminformatics tools.
4. Develop portable applications for drug activity prediction.

---

## **Technologies Used**
- **Languages**: Python
- **Libraries**: Numpy, Pandas, RDKit, Scikit-learn, XGBoost, Matplotlib, Seaborn, tqdm
- **Hardware**: Apple M1 Chip
- **Software**: macOS, Jupyter Notebook, Visual Studio Code

---

## **Acknowledgments**
Special thanks to **Dr. Sushobhan Chowdhury** for his guidance and to **Guru Gobind Singh Indraprastha University** for providing resources and support. The ChEMBL database was instrumental in this project.

---

## **License**
This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

