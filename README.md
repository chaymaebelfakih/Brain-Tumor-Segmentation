Segmentation des Tumeurs Cérébrales avec MultiEncoder UNet et Fusion par Ondelettes
📌 Description

Ce projet propose un modèle de Deep Learning basé sur l’architecture MultiEncoder UNet avec fusion par ondelettes et module d’attention contextuelle (GCAM) pour la segmentation automatique d’IRM cérébrales 3D (dataset BraTS 2021).

🎯 Objectifs

Segmenter automatiquement les différentes zones tumorales (nécrose, œdème, tumeur active).

Exploiter la complémentarité des modalités IRM (T1, T1ce, T2, FLAIR).

Améliorer la précision de segmentation grâce à la fusion multi-modale par ondelettes et l’attention globale.

🗂️ Données utilisées

Dataset : BraTS 2021 (Kaggle)

Patients : 1251 (IRM multimodales + masques de segmentation)

Modalités :

T1 : vue anatomique

T1ce : post-contraste (tumeur active)

T2 : œdème

FLAIR : zones pathologiques

Classes :

0 : tissu sain

1 : nécrose

2 : œdème

4 : tumeur rehaussée par contraste

📷 Exemple d’IRM multimodales et segmentation :




⚙️ Méthodologie

Prétraitement des données

Normalisation, recadrage et redimensionnement

Data augmentation (flip, translation, bruit d’intensité)

Architecture du modèle

Multi-encodeurs 3D (un par modalité IRM)

Fusion par ondelettes 3D (WFM) pour combiner basses et hautes fréquences

Module d’Attention Contextuelle (GCAM) pour capturer les dépendances globales

Décodeur 3D avec skip connections fusionnées

📐 Schéma du modèle :


Entraînement

Fonction de perte hybride : BCEDiceLoss (Binary Cross Entropy + Dice Loss)

Optimiseur : Adam, learning rate initial 1e-5 avec décroissance polynomiale

Validation croisée sur le dataset BraTS

Évaluation

Dice Similarity Coefficient (DSC)

Hausdorff Distance 95% (HD95)

Visualisation des résultats de segmentation

📊 Résultats

La combinaison WFM + GCAM a permis une amélioration significative du Dice Score et une réduction de la distance HD95.

La fusion tardive (multi-encodeurs + ondelettes) a montré de meilleures performances que la fusion précoce.

📈 Exemple de segmentation prédite vs vérité terrain :


✅ Conclusion & Perspectives

Le modèle proposé optimise l’exploitation des différentes modalités IRM et capture efficacement le contexte spatial global.

Limites : complexité computationnelle élevée, besoin d’un dataset multimodal de qualité.

Perspectives : optimisation architecturale, intégration de transformers 3D pour renforcer le contexte global.

🛠️ Technologies utilisées

Langage : Python

Frameworks : TensorFlow, Keras

Bibliothèques : Nibabel, NumPy, Pandas, Matplotlib, Seaborn

Outils : Jupyter Notebook

👩‍💻 Auteur

Ait Belfakih Chaymae
LinkedIn
 | Kaggle
