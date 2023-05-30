# Cahier des charges ProjetFinal

## Déploiement de CloudPanther via AKS + supervision

### Introduction
- Automatisation sécurisée du déploiement du site CloudPanther sur un cluster AKS en utilisant github actions.
- Explication de l'importance de l'automatisation et de la sécurité pour l'efficacité opérationnelle et la protection des données sensibles.

### Objectifs du projet
- Énoncé clair des objectifs du projet : automatiser le déploiement du site existant sur un cluster AKS tout en assurant la sécurité du processus.
- Indication des bénéfices attendus, tels que l'accélération des déploiements, la réduction des erreurs humaines et la protection des données.

### Exigences fonctionnelles
- Définition des fonctionnalités requises pour l'automatisation du déploiement :
- Clonage du référentiel CLOUDPANTHER à partir de GitHub.
- Construction et empaquetage sécurisé du site.
- Configuration de l'environnement AKS pour assurer la sécurité.
- Déploiement du site sur le cluster AKS en utilisant des méthodes sécurisées.
- Exécution de tests de vérification pour s'assurer du bon déploiement.

### Exigences non fonctionnelles
- Identification des exigences de sécurité spécifiques, telles que :
- Utilisation de secrets pour stocker les informations d'authentification et autres données sensibles.
- Chiffrement des données sensibles en transit et au repos.
- Contrôle d'accès et gestion des autorisations appropriées pour les ressources AKS.
- Surveillance et journalisation des activités de déploiement.

### Architecture sécurisée
- Description de l'architecture technique sécurisée :
- Utilisation de secrets GitHub pour stocker les informations sensibles.
- Utilisation de flux de travail GitHub Actions avec des contrôles d'accès appropriés.
- Configuration sécurisée du cluster AKS avec des politiques de sécurité et des mises à jour régulières.

### Plan de déploiement et de sécurité
- Définition d'une méthodologie pour le déploiement sécurisé :
- Analyse des risques et identification des vulnérabilités potentielles.
- Développement de scripts et de flux de travail sécurisés pour automatiser le déploiement.
- Validation du processus de déploiement et des contrôles de sécurité.
- Intégration de mécanismes de surveillance et d'alerte en cas d'activités suspectes.

### Plan de test
- Définition des cas de test pour vérifier le déploiement sécurisé du site :
- Tests d'intégration pour s'assurer que le site fonctionne correctement sur le cluster AKS.
- Tests de sécurité pour identifier les vulnérabilités potentielles.
- Tests de performance pour évaluer les performances du site déployé.

### Documentation et formation
- Préparation d'une documentation détaillée décrivant le processus d'automatisation et les mesures de sécurité mises en place.
