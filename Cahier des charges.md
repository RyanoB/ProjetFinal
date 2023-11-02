# Cahier des charges ProjetFinal

## Déploiement de Wordpress via AKS
  
### Objectifs du projet

- Automatiser le déploiement de Wordpress et consolidation sur un cluster AKS.

- Quel sont les bénéfices attendus ? Accélération des déploiements, réduction des erreurs humaines, protection des données...

### Avantages du projet 
    
- Évolutivité et mise à l'échelle automatique : Un cluster AKS permet de faire évoluer automatiquement les ressources en fonction de la charge de l'application. Cela garantit que l'application peut gérer facilement une augmentation du trafic sans compromettre les performances.

- Gestion simplifiée : L'automatisation facilite la gestion des déploiements, des mises à jour et versions des configurations de l'application sur le cluster AKS. Les tâches répétitives peuvent être automatisées, ce qui réduit les erreurs et les efforts manuels nécessaires pour maintenir l'application en cours d'exécution.

- Haute disponibilité et tolérance aux pannes : En répartissant l'application sur plusieurs nodes/pods dans un cluster AKS, on assure une meilleure résilience et une disponibilité accrue. En cas de panne d'un node, l'application continue de fonctionner sans interruption grâce à la répartition de charge et à la capacité de basculer automatiquement vers d'autres nodes.

- Sécurité renforcée : L'utilisation d'un cluster AKS permet de mettre en œuvre des stratégies de sécurité avancées, telles que la gestion des identités et des accès, le chiffrement des données, filtrage des flux (network policy)...

- Portabilité et flexibilité : Avec un déploiement sur un cluster AKS, l'application devient indépendante de l'infrastructure sous-jacente, ce qui offre une plus grande flexibilité et une facilité de migration vers d'autres environnements de cloud ou de fournisseurs de cloud.

- Optimisation des ressources et des coûts : 
1. L'automatisation permet d'optimiser l'utilisation des ressources en ajustant automatiquement les capacités en fonction de la charge de travail.
2. La possibilité de faire tourner d'autres outils/app sur le cluster AKS (consolidation). 
   Cela permet d'économiser sur les coûts en évitant la surprovisionnement ou la sous-utilisation des ressources.

- Écosystème et intégration : L'utilisation d'un cluster AKS offre un écosystème riche d'outils et de services complémentaires pour faciliter la gestion, le déploiement, la surveillance et l'évolutivité de l'application.

En résumé, la méthode de déploiement sur un cluster AKS avec l'automatisation offre une élasticité, une gestion simplifiée, une haute disponibilité, une sécurité renforcée, une portabilité et une optimisation des ressources et des coûts. Ces avantages contribuent à une meilleure performance, une meilleure gestion de l'application et une expérience utilisateur améliorée.

### Etapes


 - Création du cluster AKS : Je vais maintenant créer un cluster AKS en spécifiant le nombre de nodes, les tailles des machines virtuelles et les autres paramètres selon les besoins de Wordpress (service, ingress).

 - Gestion de la sécurité : Pour garantir la sécurité de mon cluster AKS, je vais utiliser les fonctionnalités fournies par Azure, telles que le contrôle d'accès basé sur les rôles (RBAC). Je vais également configurer  le chiffrement TLS pour les communications entrantes et sortantes.

 - Déploiement de l'application : Je vais utiliser github action pour l'automatisation des déploiements de mon application sur le cluster AKS. Crée des fichiers de déploiement Kubernetes (fichiers YAML) pour décrire les ressources nécessaires (deployment, replicaset, services, ingress, etc.). En m'assurant de bien définir les règles de sécurité dans les fichiers de déploiement.

 - Surveillance et gestion : Configuration des outils de surveillance tels que Azure Monitor et Prometheus pour suivre les performances et la disponibilité de mon cluster AKS. Sans oublier de mettre en place des mécanismes de sauvegarde et de restauration pour mon cluster AKS.

 - Tests et validation : Et finalement, je vais effectuer des tests de charge, revu de code, génération de la documentation et validation des changements  directement dans mes pipelines.

### Compétences visées 

- Automatisation du déploiement de l'infrastructure.
- Sécurisation de l’infrastructure.
- Gérer le stockage des données.
- Gestion de différents services kubernetes.
- Exploiter une solution de supervision et de backup.
- Gestion de cycle de vie de l'application CI/CD.

### Documentation
- Préparation d'une documentation détaillée décrivant l'architecture, les processus d'automatisation et les mesures de sécurité mises en place.

