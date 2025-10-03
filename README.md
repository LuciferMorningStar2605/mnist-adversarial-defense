# mnist-adversarial-defense

## 📌 Objective
To understand and implement **adversarial attacks** on deep learning models, gain hands-on experience in generating adversarial examples, evaluate model robustness, and apply **defense mechanisms** on a CNN trained on the MNIST dataset.

---

## 📂 Project Overview
This project explores the vulnerability of Convolutional Neural Networks (CNNs) to adversarial attacks and the effectiveness of defense mechanisms.  
- Built and trained a CNN for **handwritten digit classification** on MNIST.  
- Applied **FGSM (Fast Gradient Sign Method)** to craft adversarial samples.  
- Evaluated CNN performance on **clean vs. adversarial data**.  
- Implemented **adversarial training** to improve model robustness.  
- Compared performance metrics before and after defense.  

---

## 📊 Dataset
- **MNIST Dataset**:  
  - Training Samples: 60,000 (28×28 grayscale images)  
  - Test Samples: 10,000  
  - Classes: 10 (digits 0–9)  

---

## ⚙️ Project Workflow
1. **Data Preprocessing**
   - Normalization of pixel values.
   - One-hot encoding of labels.
   - Reshaping images to `(28,28,1)`.

2. **CNN Model**
   - Layers: Conv2D → MaxPooling2D → Dropout → Dense → Softmax.
   - Optimizer: Adam.
   - Loss: Categorical Crossentropy.
   - Achieved **~99% validation accuracy** on clean data.

3. **Adversarial Attack**
   - Implemented **FGSM Attack** with ε = 0.25.
   - Generated adversarial examples by adding perturbations to clean images.
   - Observed performance drop on adversarial inputs (~72% accuracy).

4. **Defense Mechanism**
   - Applied **Adversarial Training** with perturbed samples.
   - Improved adversarial accuracy from **~72% → ~96%**.
   - Maintained clean accuracy (~99%).

5. **Evaluation**
   - Compared original vs. defended model.
   - Visualized accuracy/loss curves, confusion matrices, adversarial samples.

---

## 📈 Results
- **Original Model**  
  - Clean Test Accuracy: **99.2%**  
  - Adversarial Test Accuracy: **72.2%**  

- **Robust Model (after defense)**  
  - Clean Test Accuracy: **99.2%**  
  - Adversarial Test Accuracy: **96.2%**  

---

## 📌 Key Learnings
- CNNs are highly accurate on clean data but vulnerable to adversarial attacks.  
- FGSM can significantly degrade model performance.  
- Adversarial training is an effective strategy to improve robustness.  
- Trade-offs exist between robustness and accuracy, but defense can greatly reduce risk.  

---

## 📦 Requirements
Create a `requirements.txt` with:
```txt
numpy
pandas
matplotlib
seaborn
scikit-learn
tensorflow
keras
