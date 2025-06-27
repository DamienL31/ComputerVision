## 💼 Dataset - 101_ObjectCategories 
## Table des Matières

- [Description du Projet et ressources](#description-du-projet-et-ressources)
- [Technologies Utilisées](#technologies-utilisees)
- [Étapes principales du projet](#etapes-principales-du-projet)
- [Partie 1 : Extraction et exploration des données](#partie-1--extraction-et-exploration-des-donnees)
- [Partie 2 : Visualisation image et traitement](#partie-2--visualisation-image-et-traitement)
- [Partie 3 : Modélisation et détections avancées](#partie-3--Modelisation-et-detections-avancees)
- [Auteur](#auteur)

## Description du Projet et ressources

Ce projet utilise le dataset **101 Object Categories** provenant de Caltech Vision Group. Il est disponible sous 2 formats soit par Kaggle soit en accédant au fichier .tar.gz présent ci-dessous. Il a pour but d'analyser, traiter des images ainsi que le développement de plusieurs modèles pour la classification et le traitement tels un modèle CNN, un modèle SVM pour la classification et l'utilisation d'un modèle YoloV5 pour la détection d'objets au sein d'une image. 

📷 L'ensemble de données Caltech101 contient des images de 101 catégories d'objets (par exemple, « hélicoptère », “éléphant” et « chaise », etc.) et une catégorie d'arrière-plan qui contient les images ne faisant pas partie des 101 catégories d'objets. Pour chaque catégorie d'objets, il y a entre 40 et 800 images, tandis que la plupart des classes ont environ 50 images. La résolution de l'image est d'environ 300×200 pixels et la taille du dossier est de 125Mo. 📷

📌 Télécharger via Kaggle ou API (https://www.kaggle.com/datasets/imbikramsaha/caltech-101) 📌

📥 Telecharger le Dataset via Google Drive (https://drive.google.com/uc?id=15Y8KiBpln7OHYQIRBlg_w4aNkXKNQumo) 📥

## Technologies Utilisées 

- Python dans un environnement Google Collab,
- tarfile
- OpenCV, cv2.kmeans,
- Pandas, NumPy, Matplotlib,
- TensorFlow, Keras, PyTorch,
- Yolov5
- Scikit-image, ImageDataGenerator, Scikit-learn,

## Etapes principales du projet 🕜

## Partie 1 : Extraction et exploration des données 📂

- Parcours de l'arborescence des classses, affichage des sous classes et sous dossiers correspondant aux catégories d'objets.
  
- Décompte du nombre d'images pour voir la répartition par dossiers et classement des classes par ordre décroissant d'occurence.

## Partie 2 : Visualisation image et traitement 🖼️

- Chargement d'une image, conversion en RGB.

- Application d'un filtrage Gaussian pour lisser l'image et réduire le bruit, conversion de l'image en gris et application d'un filtrage Canny pour détection des bors significatifs et réduire les détails non pertinents + Affichage comparatif image originale et floutée.

- Rotation de l'image, application du detecteur HOG (description d'image via analyse de l'orientation des gradients), application k means 3 couleurs pour segmentation l'image en zone de couleurs. 

## Partie 3 : Modélisation et détections avancées 🤖

- Prétraitement des images avec "ImageDataGenerator" (redimensionnement, normalisation, rotation, zoom..)
  
- Construction d'un modèle CNN en Keras (3 couches Conv2D avec ReLU + Maxpooling2D + Flatten + couche dense 128 neuronnes + Dropout 0.5 et couche de sortie "Dense" avec Softmax pour classification
  
- Compilation du modèle, entrainement sur 10 epochs et évaluation des performances. Accuracy : 0.58

- Création d'un modèle SVM pour comparaison (Extraction des descripteurs HOG, création Dataset (features, etiquettes), split données et évaluation. Accuracy : 0.53

- Installation modèle pré entrainé **YOLOv5** via Pytorch + application sur une classe spécifique pour detection + visualisation.

## Auteur 
Étudiant en Data Science
damien.lauger.edu@groupe-gema.com

