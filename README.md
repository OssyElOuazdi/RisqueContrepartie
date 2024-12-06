# Gestion des Risques de Contrepartie basé sur la Blockchain

## Description
Ce projet est une solution décentralisée pour gérer les risques de contrepartie en utilisant un smart contract basé sur la blockchain. Il permet de surveiller les expositions, de calculer les risques, et de gérer les dépassements de limites pour les différentes contreparties. La solution met l'accent sur la transparence, la sécurité et l'automatisation des processus critiques dans la gestion des risques.

## Fonctionnalités principales
- **Enregistrement des contreparties :** Ajoutez des contreparties avec leurs limites d'exposition et leurs scores de crédit.
- **Mise à jour des expositions :** Actualisez l'exposition courante d'une contrepartie tout en vérifiant les dépassements.
- **Calcul du risque :** Calculez un score de risque basé sur des facteurs tels que l'exposition, le score de crédit et d'autres paramètres financiers.
- **Ratios et pertes :**
  - Calcul du **ratio de couverture** (collatéral vs exposition).
  - Estimation des **pertes attendues** basées sur les probabilités de défaut (PD) et les pertes en cas de défaut (LGD).
- **Événements déclenchés :** Suivi en temps réel des actions importantes telles que l'ajout d'une contrepartie ou les dépassements de limites.

## Architecture
Le projet utilise :
- **Solidity** pour le développement du smart contract.
- **Polygon Amoy Testnet** comme environnement blockchain pour tester le contrat.
- **Remix IDE** ou tout autre outil compatible pour le déploiement et les tests.

## Prérequis
Pour utiliser ou déployer ce projet, vous aurez besoin de :
- Un portefeuille compatible (par ex. MetaMask).
- Une connexion à un testnet (comme le **Polygon Amoy Testnet**).
- Remix IDE ou un environnement de développement similaire pour travailler avec Solidity.

## Installation
1. Clonez le dépôt :  
   ```bash
   git clone https://github.com/OssyElOuazdi/RisqueContrepartie.git
   cd RisqueContrepartie
2. Déployez le smart contract avec Remix IDE :
- Importez le fichier .sol dans Remix.
- Connectez votre portefeuille au testnet.
- Compilez et déployez le contrat.

## Utilisation

### Ajout d'une contrepartie
Appelez la fonction `ajouterContrepartie` avec les paramètres nécessaires :

```solidity
ajouterContrepartie(adressePortefeuille, scoreCredit, limiteExposition, probabiliteDefaut, pertesEnCasDeDefaut, collaterale);
```

### Mise à jour de l'exposition
Pour mettre à jour l'exposition d'une contrepartie, appelez la fonction `mettreAJourExposition` avec l'adresse du portefeuille et la nouvelle exposition :

```solidity
mettreAJourExposition(adressePortefeuille, nouvelleExposition);
```

### Calcul du risque
Pour calculer le risque d'une contrepartie, utilisez la fonction `calculerRisque` avec l'adresse du portefeuille :

```solidity
calculerRisque(adressePortefeuille);
```

### Calcul du Ratio de Couverture
La fonction `calculerRatioCouverture` permet de calculer le ratio de couverture d'une contrepartie. Ce ratio mesure la proportion du collatéral par rapport à l'exposition courante.
Utilisez la fonction de cette manière :

```solidity
calculerRatioCouverture(adressePortefeuille);
```

### Calcul des Pertes Attendues
La fonction `calculerPertesAttendues` permet de calculer les pertes attendues pour une contrepartie, en fonction de son exposition courante, de la probabilité de défaut (PD), et des pertes en cas de défaut (LGD).
Utilisez cette fonction de cette manière :

```solidity
calculerPertesAttendues(adressePortefeuille);
```

## Tests
Des tests ont été effectués sur les cas suivants :
- Enregistrement d'une contrepartie.
- Détection des dépassements de limites.
- Calculs de ratios de couverture et pertes attendues.
- Gestion des entrées invalides.

### Exécution des tests

Vous pouvez exécuter les tests en utilisant Remix et voici comment procéder :

1. Ouvrez Remix IDE dans votre navigateur.
2. Importez le contrat Solidity dans l'éditeur.
3. Compilez le contrat.
4. Utilisez l'onglet "Deploy & Run" pour déployer le contrat sur un réseau de test local.
5. Interagissez avec le contrat en appelant ses fonctions pour tester les différents cas.

## Licence
Ce projet est sous licence **MIT**. Consultez le fichier [LICENSE](LICENSE) pour plus de détails.

## Auteur
**Oussama El Ouazdi**  
    Développeur débutant en blockchain. Passionné par la création de solutions décentralisées.

## Contact
Pour toute question ou suggestion, vous pouvez me contacter via :
*   **Email :** oussama25092002sm@gmail.com
*   **LinkedIn :** [Mon Profil](https://www.linkedin.com/in/oussama-el-ouazdi/)



