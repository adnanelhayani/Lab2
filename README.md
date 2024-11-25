# Lab 2 : PyTorch et Modèles de Vision par Ordinateur pour la Classification MNIST

## **Objectif**
Ce laboratoire a pour but d'apprendre à utiliser la bibliothèque PyTorch pour construire et entraîner différents modèles neuronaux, notamment des architectures CNN, Faster R-CNN, et des modèles préentraînés comme VGG16 et AlexNet, pour résoudre des problèmes de classification d'images.

---

## **Travail Réalisé**

### **1. Modèle CNN**
- Architecture définie avec des couches convolutionnelles, de pooling et entièrement connectées.
- **Hyperparamètres** :
  - Kernel : \(3 \times 3\)
  - Padding : \(1\)
  - Stride : \(1\)
  - Optimiseur : Adam (\(LR = 0.001\))
  - Régularisation : Décroissance \(L2\)
- **Résultats** :
  - **Précision (Accuracy)** : 0.9904
  - **Score F1** : 0.9904
  - **Pertes par époque** :
    - Epoch [1/10], Loss: 0.2536
    - Epoch [2/10], Loss: 0.0872
    - Epoch [3/10], Loss: 0.0663
    - Epoch [4/10], Loss: 0.0539
    - Epoch [5/10], Loss: 0.0445
    - Epoch [6/10], Loss: 0.0405
    - Epoch [7/10], Loss: 0.0345
    - Epoch [8/10], Loss: 0.0322
    - Epoch [9/10], Loss: 0.0269
    - Epoch [10/10], Loss: 0.0245

---

### **2. Modèle Faster R-CNN**
- Adaptation pour le dataset MNIST, avec les chiffres traités comme des régions d'intérêt (RoIs).
- **Résultats** :
  - **Précision (Accuracy)** : 0.8960
  - **Score F1** : 0.8608
  - **Pertes par époque** :
    - Epoch [1/3], Loss: 0.0743
    - Epoch [2/3], Loss: 0.0218
    - Epoch [3/3], Loss: 0.0136

---

### **3. Modèles Préentraînés**
#### **VGG16**
- Fine-tuning avec le dataset MNIST.
- **Résultats** :
  - Train Loss: 0.2746
  - Train Accuracy: 0.9127
  - Test Accuracy: 0.9850

#### **AlexNet**
- Fine-tuning avec le dataset MNIST.
- **Résultats** :
  - Train Loss: 0.2748
  - Train Accuracy: 0.9118
  - Test Accuracy: 0.9770

---

## **Comparaison des Modèles**

| Modèle          | Perte d'entraînement | Précision d'entraînement | Précision de test | Score F1    | Pertes par époque                             |
|------------------|-----------------------|---------------------------|-------------------|-------------|-----------------------------------------------|
| **CNN**         | -                     | -                         | **0.9904**        | **0.9904**  | Voir section CNN pour les détails             |
| **Faster R-CNN**| -                     | -                         | 0.8960           | 0.8608      | Voir section Faster R-CNN pour les détails    |
| **VGG16**       | 0.2746                | 0.9127                    | 0.9850           | -           | Non applicable                                |
| **AlexNet**     | 0.2748                | 0.9118                    | 0.9770           | -           | Non applicable                                |

---

## **Synthèse**
- **Ce que j’ai appris** :
  - Utilisation de PyTorch pour concevoir et entraîner différents modèles de vision par ordinateur.
  - Comparaison des modèles en fonction de leurs performances sur le dataset MNIST.
  - Fine-tuning de modèles préentraînés pour un nouveau dataset.
- **Défis rencontrés** :
  - Optimisation des hyperparamètres.
  - Entraînement de Faster R-CNN pour une tâche de classification.
  - Comparaison des architectures pour des métriques spécifiques.
- **Conclusions** :
  - Le **CNN** surpasse les autres modèles en termes de précision et de score F1 pour le dataset MNIST.
  - Les modèles préentraînés comme **VGG16** et **AlexNet** offrent de bonnes alternatives grâce au transfert d’apprentissage.
  - **Faster R-CNN**, bien que conçu pour la détection d’objets, est moins adapté à une tâche de classification simple comme celle-ci.

---

## **Guide d'Utilisation**
1. Clonez le dépôt :
   ```bash
   git clone https://github.com/votre-utilisateur/lab2-pytorch.git
