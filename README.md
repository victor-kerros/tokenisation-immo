# tokenisation-immo

### Projet dans le cadre du cours "Python pour le Data Scientist" (2A ENSAE).

**Auteurs**
HOUAIRI Leo / JOUBERT Eloi / KERROS Victor

**Fichier principal**
Le fichier principal de ce dossier est **valo_immo**. Les 2 autres notebooks sont mentionnés à l'intérieur de celui-ci. 
*cleaning_dvf* traite d'une problématique de lignes dupliquées dans le fichier de donnnées que nous utilisons et que nous n'avons pas totalement résolue.
*external_data* importe, traite et réunit d'autres tables de données, qui sont ensuite importées dans le notebook principal via une fonction.

**Problématique :**
Dans un contexte d'explosion des prix de l'immobilier (+ 90 % en prix réel en France sur la période 2000-2020 selon l'OCDE), les frais d'agences représentent un coût de plus en plus conséquent (5 à 10 % du bien). La technologie Blockhain, utilisée dans l'immobilier depuis le 25 juin 2019, permet de réaliser, via la tokenisation, des transactions plus rapides, plus sûres, transparentes, à moindres coûts et en se passant de tiers de confiance.
Source : https://www.wavestone.com/fr/insight/blockchain-transaction-immobiliere/​ 

**Objectif :**
L'objectif de ce projet est de réaliser un algorithme de tokenisation de biens immobiliers qui pourra être utiliser pour les échanger dans un smart contract.

**Réalisatinon effective**
Nous ne sommes finalement pas allés jusqu'à la partie smart contract et nous sommes contentés de la prédiction de la valeur de biens immobiliers en fonction de leurs caractéristiques

**Point technique sur les smart contracts :**
Un smart contract est une transaction dont l'exécution est sécurisée via une blockchain, soumise à des conditions inscrites sur un programme informatique (valorisation du bien, délais et autres contraintes juridiques). Le smart contract peut faire appel à des données extérieures pour établir ces conditions (via des "oracles").

**Méthodologie :**
Pour réaliser notre projet, nous allons :
1) collecter des données pour déterminer les variables explicatives du prix de l'immobilier (analyse descriptive) ;
2) coder un algorithme de valorisation des biens immobiliers sur la base de données externes (modélisation) ;
3) coder un algorithme de tokenisation pouvant être utilisé dans un smart contract (**cette partie n'a finalement pas vue le jour**).

**Données et retraitement :**
​Nous procéderons au nettoyage de différentes données : historique des montants des loyers et des transactions foncières (data.gouv), données macroéconomiques (inflation, croissance, consommation énergétique). Nous tenterons également de réaliser du scrapping (transaction immobilières ou tweets, par exemple).
Nous croiserons ces données pour créer une database inédite afin d'entraîner notre algorithme.

**Analyse descriptive :**
Nous déterminerons à partir de ces données les corrélations entre ces variables (à partir de graphiques de tendances, de matrices de corrélations et éventuellement de cartes). Nous obtiendrons ainsi une première analyse sur les variables pertinentes à intégrer dans l'entraînement de notre algorithme de valorisation des biens immobiliers.

**Modélisation :**
Nous utiliserons des algorithmes de ML pour pricer les biens immobiliers afin de les tokeniser.
Nous essaierons d'abord une régression linéaire. Dans la mesure où le processus qui génère les prix immobiliers a toutes les chances d'être non linéaire, il sera aussi intéressant de tester des algorithmes plus sophistiqués que la régression linéaire (ex : Random Forests).
