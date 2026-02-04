# Projet d'Evaluation Machine Learning

Etudiant : Marc-Antoine Bernard

Cursus : ESTIA BIHAR

Année : 2025-26

## Dataset

le dataset a été fourni par la société Hupi. Il est issu d'un usecase réel anonymisé d'analyse de consommation d'eau.

## Objectif

Pour un opérateur public de distribution d’eau, la détection rapide des fuites sur le réseau est un enjeu stratégique majeur.

Les équipes terrain interviennent quotidiennement sur des milliers de kilomètres de canalisation, où les fuites peuvent passer inaperçues et entraîner des pertes importantes d’eau, des coûts élevés et des perturbations du service.

HUPI travaille depuis plusieurs mois afin de développer un Assistant Virtuel de détection de fuites, basé sur des modèles de Machine Learning.

Cet assistant prend en compte :
- les caractéristiques du réseau,
- les données historiques de consommation et de pression,
- ainsi que le profil et les habitudes de fonctionnement du réseau, afin d’alerter automatiquement et judicieusement lorsqu’un risque de fuite est détecté.

L’objectif est de concevoir des modèles auto-apprenants, capables de s’adapter aux spécificités de chaque zone géographique et de chaque type d’infrastructure, afin de générer des alertes personnalisées et adaptées à chaque contexte de réseau.

## Réalisation

Voir **presentation.ipynb** pour le code et **presentation.pdf** pour le rapport.

Informations complémentaires transmises par Hupi après la soutenance :
- Les compteurs présentant un volume insuffisant de données devaient effectivement être exclus de l’analyse, en raison d’un taux élevé d’indisponibilités de télérelève. Une action d’amélioration a été menée avec l’exploitant afin d’augmenter la fiabilité des données issues des compteurs.
- L’objectif de l’étude était d’estimer un niveau d’anomalie en comparant une consommation réelle à une consommation prédite. Le modèle de référence utilise habituellement comme prédiction la consommation mesurée entre 00h00 et 04h00, période durant laquelle la consommation attendue est proche de zéro. Cependant, dans le cadre de ce projet, les données disponibles étant agrégées sous forme d’un point quotidien unique, cette approche n’était pas applicable.

## Bonus

Réalisation d'un modèle DLinear from scratch en PyTorch compatible GPU NVIDIA Quadro M620. Voir **DLinear.ipynb**

Requirements :
- python==3.10.19
- torch==1.13.1
- numpy==1.24.3
- pandas==2.3.3