# MNIST Adversarial Defense

Exploring adversarial attacks on deep learning models trained on MNIST
and implementing defense mechanisms to improve robustness.

## Overview
Adversarial examples are inputs crafted to fool ML models. This project
implements FGSM (Fast Gradient Sign Method) attacks on a CNN trained on
MNIST, then evaluates adversarial training as a defense strategy.

## Tech Stack
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=flat&logo=keras&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)

## What is an Adversarial Attack?
Adversarial attacks add small, imperceptible perturbations to input images
that cause ML models to misclassify them with high confidence.
Even a 99% accurate CNN can be fooled by carefully crafted noise.

## Techniques Covered
| Technique | Type | Description |
|-----------|------|-------------|
| FGSM | Attack | Fast Gradient Sign Method — one-step gradient attack |
| PGD | Attack | Projected Gradient Descent — iterative attack |
| Adversarial Training | Defense | Retrain on adversarial examples |
| Input Preprocessing | Defense | Denoising before inference |

## Project Workflow
1. Train baseline CNN on clean MNIST data
2. Generate adversarial examples using FGSM
3. Evaluate accuracy drop under attack
4. Implement adversarial training defense
5. Compare clean vs adversarial accuracy before and after defense
6. Visualise adversarial perturbations

## Results
| Scenario | Accuracy |
|----------|----------|
| Clean data | ~99% |
| Under FGSM attack | ~15-40% |
| After adversarial training | ~85%+ |

## Key Insights
- Small perturbations invisible to humans cause large accuracy drops
- Adversarial training significantly improves robustness
- There is an accuracy-robustness trade-off on clean data

## Setup
```bash
git clone https://github.com/LuciferMorningStar2605/mnist-adversarial-defense.git
pip install tensorflow keras numpy matplotlib
jupyter notebook
```
