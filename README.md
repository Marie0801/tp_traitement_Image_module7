# 🍎 Projets de vision par ordinateur — Modules 7 et 8

## 1. Présentation générale

Ce dépôt regroupe deux projets pratiques de vision par ordinateur consacrés à la reconnaissance automatique des fruits. Le contexte est celui d'une entreprise de fabrication de jus qui souhaite faciliter le tri des bananes, oranges, pommes et tamarillos (*matunda ya damu*).

Le tri manuel des fruits mélangés demande du temps et mobilise plusieurs personnes. L'objectif est donc d'étudier différentes méthodes d'intelligence artificielle capables de reconnaître les catégories de fruits à partir de photographies.

Les deux projets permettent de comparer des approches classiques d'apprentissage automatique et des réseaux de neurones profonds.

## 2. Projet du Module 7 — Classification avec CNN et ResNet-18

### Objectif

Développer un système de classification capable de reconnaître quatre catégories de fruits :

- Banane
- Orange
- Pomme
- Tamarillo (*matunda ya damu*)

### Dataset

Le dataset contient 320 images, réparties en quatre classes de 80 images chacune.

| Ensemble | Nombre d'images |
|---|---:|
| Entraînement | 224 |
| Validation | 48 |
| Test | 48 |
| **Total** | **320** |

### Méthodes utilisées

**CNN personnalisé :** réseau convolutif développé pour apprendre les caractéristiques visuelles des fruits.

**ResNet-18 :** réseau préentraîné adapté aux quatre classes par transfert d'apprentissage et ajustement du modèle.

### Résultats expérimentaux

- CNN personnalisé : **66,67 % de précision sur le test**, soit 32 images correctement classées sur 48.
- ResNet-18 : **93,75 % de précision sur le test**, soit 45 images correctement classées sur 48, selon l'expérimentation rapportée.

Les résultats montrent l'intérêt du transfert d'apprentissage sur un dataset relativement limité. Certaines confusions subsistent entre des fruits visuellement proches.

## 3. Projet du Module 8 — Étude comparative des méthodes de classification

### Objectif

Comparer plusieurs approches de classification automatique des fruits afin d'étudier leurs performances et leurs limites sur des images.

### Méthodes utilisées

- **SVM (Support Vector Machine) :** classifieur fondé sur la recherche d'une frontière de séparation entre les classes.
- **k-NN (k-Nearest Neighbors) :** méthode qui classe une image en fonction des exemples les plus proches dans l'espace des caractéristiques.
- **CNN (Convolutional Neural Network) :** réseau de neurones qui apprend des caractéristiques visuelles à partir des images.
- **ResNet-18 :** réseau profond préentraîné utilisé par transfert d'apprentissage.

Le SVM et le k-NN représentent les méthodes classiques de référence. Le CNN et ResNet-18 permettent d'étudier les approches fondées sur l'apprentissage profond.

### Dataset

Le travail expérimental s'appuie sur des images de quatre classes : banane, orange, pomme et tamarillo.

Pour le dataset de référence du projet de classification, les données sont organisées en ensembles d'entraînement, de validation et de test. Les résultats doivent être associés au dataset et à la configuration utilisés dans chaque expérimentation.
voila le lien pour le photos du dataset : https://drive.google.com/drive/folders/1nH0Gy70G8VYB2wIfYtLIvPWDuTDgEQVK

### Évaluation

Les méthodes sont évaluées à l'aide de mesures adaptées à la classification, notamment :

- **Accuracy :** proportion totale d'images correctement classées.
- **F1-score :** équilibre entre précision et rappel.
- **Matrice de confusion :** identification des confusions entre les catégories.
- **Analyse des erreurs :** étude de l'influence de l'éclairage, du fond, de l'angle de prise de vue et de la maturité des fruits.

Les résultats chiffrés du SVM et du k-NN doivent être présentés séparément de ceux du CNN et de ResNet-18, en respectant les données et les configurations effectivement utilisées.

ons présentées dans ce dépôt. Il s'agit d'une méthode de détection d'objets qui pourrait faire l'objet d'une extension ultérieure nécessitant des annotations de boîtes englobantes. Le travail réalisé ici porte sur la classification des images de fruits.

## 4. Technologies utilisées

| Technologie | Utilisation |
|---|---|
| Python | Programmation |
| Google Colab | Environnement d'expérimentation |
| NumPy et Pandas | Manipulation des données |
| Scikit-learn | SVM, k-NN et métriques d'évaluation |
| PyTorch | Développement et entraînement des CNN |
| Torchvision | ResNet-18 et transformations d'images |
| Matplotlib | Visualisation des résultats |

## 5. Installation des bibliothèques

```bash
pip install numpy pandas scikit-learn matplotlib torch torchvision
```

Dans Google Colab, les bibliothèques déjà installées peuvent être utilisées directement.

## 6. Limites et usages responsables

Les performances dépendent de la qualité et de la diversité des images. Un modèle peut commettre davantage d'erreurs lorsque les conditions de prise de vue changent ou lorsque les fruits présentent des couleurs, des tailles ou des degrés de maturité différents de ceux des données d'entraînement.

La fiabilité de l'évaluation exige une séparation correcte entre entraînement, validation et test, sans fuite de données. Les images presque identiques ou issues du même fruit ne doivent pas être réparties entre plusieurs ensembles si cela risque de surestimer les performances.

Ces modèles constituent des prototypes d'aide au tri. Une intégration dans une machine réelle nécessiterait des essais supplémentaires en conditions opérationnelles.

## 7. Conclusion

Ces deux projets explorent différentes méthodes de classification automatique des fruits. Le premier met en œuvre un CNN personnalisé et ResNet-18, tandis que le second compare les approches classiques SVM et k-NN aux approches profondes CNN et ResNet-18.

Cette étude permet de comprendre les différences entre les méthodes, de mesurer leurs performances et d'identifier les limites liées aux données et aux conditions de prise de vue.

**Statut :** projets de classification réalisés selon les expérimentations documentées. Aucun entraînement YOLO n'est revendiqué.

**Domaine :** intelligence artificielle, apprentissage automatique et vision par ordinateur.  
**Institution :** ULPGL.
