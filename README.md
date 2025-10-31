
# 🚢 Titanic Survival Prediction using Neural Networks

This project demonstrates the end-to-end process of building and optimising a neural network model to predict passenger survival from the Titanic dataset.  
It showcases key steps in a typical machine learning workflow — from data preparation to model evaluation — using TensorFlow/Keras.

---

## 🧭 Project Overview
The goal of this project is to predict which passengers survived the Titanic voyage based on available demographic and travel information.

The process includes:
- Data cleaning and preprocessing  
- Encoding categorical variables and scaling numerical features  
- Building and training neural networks with **Adam** and **RMSProp** optimisers  
- Applying **L2 regularisation**, **dropout**, and **early stopping** to reduce overfitting  
- Comparing model performance across different optimisation strategies

---

## ⚙️ Model Summary
- **Input Layer:** Number of neurons = number of input features  
- **Hidden Layer:** Dense layer with ReLU activation  
- **Output Layer:** Single neuron with Sigmoid activation for binary classification  
- **Loss Function:** Binary Cross-Entropy  
- **Optimisers:** Adam and RMSProp  
- **Regularisation:** L2 regularisation (λ=0.01) and Dropout  
- **Callbacks:** Early stopping (`patience=1`, `restore_best_weights=True`)

---

## 📊 Results Summary
| Model | Test Loss | Test Accuracy | Epochs Trained |
|--------|------------|----------------|----------------|
| Adam + L2 + Dropout + EarlyStopping | 0.5061 | 0.7989 | 17 |
| RMSProp + L2 + Dropout + EarlyStopping | 0.4851 | 0.8045 | 25 |

Both optimisers achieved comparable performance (~80% accuracy), with **RMSProp** showing slightly lower loss and smoother convergence.  
The use of **dropout** and **early stopping** effectively prevented overfitting, leading to stable generalisation on unseen data.

---

## 🧠 Key Learnings
- Importance of preprocessing (handling missing values, encoding, scaling)  
- How optimiser choice affects model convergence  
- The role of dropout and L2 regularisation in preventing overfitting  
- How early stopping improves training efficiency and generalisation  
- Interpreting training and validation curves for model evaluation

---

## 🛠️ Tech Stack
- **Python**
- **TensorFlow / Keras**
- **NumPy**
- **Pandas**
- **Matplotlib / Seaborn**
- **Scikit-learn**

---

## 💡 Reflections
Through this experiment, I explored how different optimisers and regularisation strategies influence neural network performance.  
The results demonstrated that with proper tuning and early stopping, both Adam and RMSProp can achieve robust generalisation on structured tabular data.

---

*Author: Ponlakshmi Raman*  
*Project Type: Deep Learning Practice — Neural Network Optimisation and Regularisation*
