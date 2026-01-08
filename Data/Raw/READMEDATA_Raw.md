Dossier contenant les deux jeux de données provenant du Kaggle:
- "soil_data.csv" : premier jeu de données implémenté dans ce dossier,
- "train_timeseries.csv" : deuxième jeu de données volumineuse pour être implémenté dans ce dossier. Pour la trouver, il faut la télécharger en suivant ce lien : "https://www.kaggle.com/datasets/cdminix/us-drought-meteorological-data?resource=download".


Pour rappel, deux bases de données issues de Kaggle:
- soil_data.csv : Ce jeu contient des informations sur le sol et divers indices météorologiques pour différents États américains. La variable cible est le niveau de sécheresse, codé de 0 à 5, correspondant à une intensité croissante de la sécheresse. Ce jeu permet d’identifier l’état du sol et les facteurs environnementaux influençant la sécheresse.
- train_timeseries.csv : Ce second jeu contient des séries temporelles plus détaillées sur les mêmes régions et périodes, incluant des informations météorologiques supplémentaires (température, précipitations, humidité, etc.). L’objectif est de lier ces informations pour expliquer plus précisément les causes de la sécheresse.

Celles-ci regroupent des informations provenant de plusieurs sources officielles, notamment :
 - Le NASA POWER Project, développé par le NASA Langley Research Center(LaRC) dans le cadre du programme NASA Earth Science/Applied Science.
- Le U.S. Drought Monitor, un projet collaboratif impliquant le National Drought Mitigation Center (Université du Nebraska-Lincoln), le United States Department of Agriculture (USDA) et la National Oceanic and Atmospheric Administration (NOAA).

Le jeu de données concaténé est structuré sous la forme d’un problème de classification avec six niveaux de sécheresse (0 pour une absence de sécheresse, 1 pour un niveau modéré, et ainsi de suite). Chaque observation correspond au niveau de sécheresse d’un comté américain à une date donnée, accompagné des données de 18 indicateurs météorologiques sur les 90 derniers jours. Parmi ces variables, nous trouvons par exemple la température de surface terrestre en°C (TS) ou encore la vitesse minimale du vent à 10 mètres en m/s (WS10M-MIN).
Les États, comtés et autres subdivisions administratives des États-Unis sont désignés par leur code FIPS. Cet identifiant numérique sert principalement à la collecte, au traitement et à l’analyse des données gouvernementales et statistiques. Par exemple, le comté de Travis au Texas a le code FIPS 48453 (48 pour l’État du Texas + 453 pour le comté).
