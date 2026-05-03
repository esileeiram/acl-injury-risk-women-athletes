# ACL-injury-risk-women-athletes
# Facteurs de risque de blessure chez les femmes sportives
## Une analyse économétrique exploratoire

### Pourquoi ce projet
Moi-même victime d'une rupture du ligament croisé antérieur, j'ai voulu comprendre pourquoi les femmes sportives y sont statistiquement plus exposées que les hommes. Ce projet est une première exploration de cette question à travers une analyse économétrique sur données réelles.

### Données
Dataset : Collegiate Athlete Injury Dataset (Kaggle)
200 athlètes universitaires, 17 variables comportementales et physiques.

### Méthodologie
- Statistiques descriptives et visualisations
- Régression logistique (sklearn)
- Régression logistique économétrique avec p-values (statsmodels)
- Analyse spécifique sur sous-population féminine et masculine
- Mise en perspective avec la littérature scientifique : j'ai confronté mes résultats à la littérature scientifique pour tester leur cohérence et identifier ce que mon dataset ne capturait pas.


### Principaux résultats
- Fatigue et surcharge d'entraînement augmentent significativement le risque (p<0.05)
- La récupération est le facteur protecteur le plus puissant (p=0.001, coef=-3.20 sur les femmes uniquement), son effet est deux fois plus fort que chez les hommes.
- La surcharge d'entraînement est significative uniquement chez les femmes (p=0.036 vs p=0.235) à charge égale, les femmes sont plus exposées
- Le modèle explique mieux le risque féminin (Pseudo R²=0.56) que masculin (0.39)
- Les facteurs biologiques absents du dataset (hormonaux, biomécaniques) constituent une limite.
- Des programmes de prévention multicomposants réduisent les blessures ACL de 45% (Crossley et al., BJSM 2020)

*Ouverture : la récupération est le facteur protecteur le plus puissant mais elle est contrainte par les calendriers sportifs. Comment optimiser la prévention sous contrainte de calendrier sportif ?* 

### Limites du data set
- 200 observations, robustesse statistique limitée
- Dataset synthétique universitaire américain
- Absence de variables biologiques et biomécaniques
- Quasi-séparation sur le modèle féminin (8 blessures seulement)

### Outils
Python, Pandas, Statsmodels, Sklearn, Matplotlib, Seaborn

### Sources
- Larruskain J. et al. UEFA Women's Elite Club Injury Study, BJSM 2022
- Crossley KM. et al. Making football safer for women, BJSM 2020
- Nilstad A. et al. Risk factors for lower extremity injuries, AJSM 2014
- Herzberg SD. et al. Effects of the menstrual cycle phase on ACL risk, 2017
