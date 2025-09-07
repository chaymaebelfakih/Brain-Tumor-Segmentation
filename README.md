# Segmentation des Tumeurs Cérébrales avec MultiEncoder UNet et Fusion par Ondelettes

## Description
Projet académique réalisé de Mars 2025 à Juillet 2025.  
Conception d’un modèle de Deep Learning basé sur l’architecture **MultiEncoder UNet avec fusion par ondelettes** pour le traitement et la segmentation d’IRM cérébrales 3D afin de détecter différentes zones de tumeur.

## Objectifs
- Segmenter les différentes zones tumorales sur des IRM cérébrales 3D.
- Utiliser une architecture avancée de Deep Learning pour améliorer la précision de segmentation.
- Comprendre et implémenter la fusion multi-modale par ondelettes.

## Technologies utilisées
- **Langages** : Python  
- **Frameworks** : TensorFlow, Keras  
- **Bibliothèques** : Nibabel, NumPy, Pandas  
- **Outils** : Jupyter Notebook, Matplotlib, Seaborn  

## Méthodologie
1. **Prétraitement des données** :  
   - Normalisation des images IRM  
   - Recadrage et redimensionnement  
   - Augmentation des données (flip, translation, décalage d’intensité)

2. **Conception du modèle** :  
   - Implémentation du MultiEncoder UNet  
   - Fusion des modalités IRM par ondelettes  
   - Décodeur 3D pour la segmentation finale

3. **Entraînement** :  
   - Fonction de perte hybride : Dice Loss + Binary CrossEntropy  
   - Optimiseur Adam avec learning rate 1e-5  
   - Validation à chaque époque

4. **Évaluation** :  
   - Mesures de performance : Dice Score, précision, rappel  
   - Visualisation des résultats de segmentation sur les IRM

## Résultats
- Modèle capable de segmenter avec précision les zones tumorales sur les IRM 3D.
- Amélioration notable de la segmentation grâce à la fusion par ondelettes.

## Conclusion
Ce projet m’a permis de :
- Comprendre en profondeur la segmentation d’images médicales.  
- Implémenter des architectures avancées de Deep Learning multi-modales.  
- Expérimenter la fusion de données IRM par ondelettes pour améliorer les performances.

## Auteur
**Ait Belfakih Chaymae**  
[LinkedIn](https://www.linkedin.com/in/chaymae-belfakih-b97226342/) | [Kaggle](https://www.kaggle.com/chaymaaitbelfakih)
