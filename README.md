

# Leishmaniasis Drug Discovery: Machine Learning Approach

## **Overview**
This repository showcases the development and implementation of a machine learning-based solution to accelerate drug discovery for the treatment of **Leishmaniasis**, a neglected tropical disease. This project was undertaken as part of a summer internship at Guru Gobind Singh Indraprastha University.

### **Abstract**
Drug discovery is a time-intensive and costly endeavor. This project applies machine learning (ML) techniques to predict the bioactivity of chemical compounds against Leishmania parasites, leveraging molecular fingerprinting methods and various ML classifiers. The study identifies key molecular features and develops ensemble models to improve prediction accuracy, reducing the overall cost and time for drug development.

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
1. Develop an ML pipeline to classify chemical compounds as active or inactive against Leishmania.
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
The reduction from 278,045 to approximately 10,000 entries was necessitated by the following factors:
1. **Duplicate Removal**: A significant number of entries were duplicates based on SMILES representations, reducing the dataset to 94,435 unique compounds.
2. **Bioactivity Filtering**: Only the most commonly reported bioactivity types (IC50, Percent Effect, Inhibition, EC50) were retained to maintain focus and reduce sparsity.
3. **Unit Standardization**: Entries with inconsistent or unconvertible unit measurements were removed, ensuring uniformity in bioactivity data.
4. **Quality Control**: Irrelevant or unreliable data points were excluded to enhance the dataset's reliability and focus on high-quality experimental results.
5. **Binary Classification**: Intermediate classes were eliminated to simplify the classification task, leaving only active and inactive categories.

### **Preprocessing Steps**
1. **Duplicate Removal** – Reduced dataset from 278,045 to 94,435 entries.
2. **Bioactivity Filtering** – Focused on IC50, Percent Effect, Inhibition, and EC50 values.
3. **Unit Standardization** – Converted all values to nanomolar (nM).
4. **Binary Classification** – Threshold of 10,000 nM used to classify compounds:
   - Active: <10,000 nM
   - Inactive: >10,000 nM
5. **Feature Selection** – Retained key columns: SMILES, Standard Type, Standard Value, and Units.

---

## **Methodology**
1. **Feature Engineering**
   - Generated molecular fingerprints: **Morgan**, **MACCS**, **RDKit**, **Atom Pair**.
   - Applied dimensionality reduction using PCA and t-SNE for visualization.

   ### **PCA Plot**
   *Insert PCA plot here*

   ### **t-SNE Plot**
   *Insert t-SNE plot here*

2. **Algorithms Used**
   - **Classical Models**: Random Forest, Logistic Regression, Gradient Boosting, KNN, SVC, Decision Tree, AdaBoost.
   - **Ensemble Models**: VotingClassifier.
   - **ANN**: Multi-Layer Perceptron (MLP) for deeper insights.

3. **Evaluation Metrics**
   - Accuracy
   - Precision
   - Recall
   - F1 Score

4. **Ensemble Learning**
   - Combined predictions of top-performing models to boost overall performance.

---

## **Results**
- **Best Fingerprint**: **RDKit Fingerprint**
- **Optimal Model**: Random Forest + RDKit Fingerprinting
- **Accuracy Achieved**: 90%
- **Key Feature Identified**: RDKit_747

### **Visual Highlights**
1. **PCA and t-SNE Plots**
   - Visualize molecular fingerprint distributions.
   - *Insert PCA and t-SNE plots here.*

2. **Heatmaps**
   - Showcase performance metrics for each fingerprint and classifier.
   - *Insert heatmap showing model evaluation metrics here.*

3. **Bar Graph Comparisons**
   - Accuracy across models and fingerprints.
   - Recall across models and fingerprints.
   - F1 Scores across models and fingerprints.
   - *Insert bar graphs for accuracy, recall, and F1 score comparisons here.*

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
