# Cahier des charges ProjetFinal

## Déploiement de CloudPanther via AKS + supervision

### Introduction
- Automatisation sécurisée du déploiement du site CloudPanther sur un cluster AKS en utilisant github actions.
- Explication de l'importance de l'automatisation pour l'efficacité opérationnelle.
  
  Efficacité et rapidité : L'automatisation permet d'effectuer des tâches répétitives de déploiement et de gestion de manière rapide et efficace. Les processus automatisés peuvent être exécutés en quelques clics ou en utilisant des scripts, ce qui fait gagner du temps et réduit les erreurs humaines.

  Répétabilité et cohérence : Dans nôtre cas, l'automatisation garantit une cohérence dans le déploiement et la gestion du site. Je vais pouvoir utiliser les mêmes scripts ou configurations automatisées pour déployer l'application sur plusieurs environnements, assurant ainsi la cohérence des configurations et réduisant les risques d'erreurs.

  Elasticité : L'automatisation permet de mettre à l'échelle l'infrastructure de manière plus facile et rapide. Je vais pouvoir créer des scripts ou des modèles d'automatisation qui ajustent automatiquement les ressources en fonction de la charge de travail, permettant ainsi une mise à l'échelle horizontale ou verticale en fonction des besoins de l'application.

  Réduction des erreurs : L'automatisation réduit les erreurs manuelles potentielles. En évitant les tâches manuelles et en utilisant des processus automatisés, je minimises les risques d'erreurs humaines qui pourraient survenir lors du déploiement, de la configuration ou de la gestion de l'infrastructure.

  Sécurité renforcée : L'automatisation permet de mettre en place des pratiques de sécurité cohérentes et reproductibles. je peux automatiser la configuration des règles de sécurité, le déploiement des correctifs de sécurité, la gestion des secrets et d'autres aspects liés à la sécurité, réduisant ainsi les risques de vulnérabilités ou d'erreurs de configuration.

  Documentation et traçabilité : L'automatisation facilite la documentation des processus et des configurations. Les scripts, les modèles et les outils d'automatisation fournissent une traçabilité claire des actions effectuées, ce qui facilite la compréhension des changements apportés à l'infrastructure et permet de résoudre rapidement les problèmes.

  Agilité et évolutivité : L'automatisation permet de répondre rapidement aux besoins changeants de mon application. Je peux facilement répliquer ou migrer mon environnement de développement, de test ou de production en utilisant les mêmes scripts ou configurations automatisées, me permettant ainsi de gagner en agilité et de répondre rapidement aux demandes de déploiement.
  

### Objectifs du projet
- Enoncé clair des objectifs du projet : automatiser le déploiement du site existant sur un cluster AKS tout en assurant la sécurité du processus.
- Indication des bénéfices attendus, tels que l'accélération des déploiements, la réduction des erreurs humaines et la protection des données.

### Avantages du projet 
- Gestion automatisée des ressources : Kubernetes gère automatiquement l'allocation des ressources et assure une utilisation efficace des ressources disponibles sur le cluster AKS. La mise à l'échelle horizontale et verticale peut être facilement effectuée en ajoutant ou en supprimant des nœuds dans le cluster. 
  Dans la méthode actuelle, la gestion des ressources (allocation de la capacité de calcul, de la mémoire, etc.) doit être effectuée manuellement sur la VM. Cela peut entraîner une utilisation inefficace des ressources et nécessiter une surveillance et une mise à l'échelle manuelles en cas de besoin.

- Haute disponibilité et tolérance aux pannes : Kubernetes garantit la haute disponibilité de l'application en répartissant les charges de travail sur plusieurs nœuds du cluster AKS. En cas de panne d'un nœud, les conteneurs sont redéployés sur d'autres nœuds sains, minimisant ainsi les temps d'arrêt. 
  Assurer la haute disponibilité de l'application sur une seule VM peut être difficile. En cas de défaillance de la VM, il peut y avoir des temps d'arrêt jusqu'à ce que la VM soit réparée ou remplacée.

- Gestion simplifiée des mises à jour et des versions : Avec Kubernetes, le déploiement de nouvelles versions ou de mises à jour de l'application peut être réalisé de manière progressive et automatisée sans interruption de service. Les stratégies de déploiement permettent de gérer facilement les changements de version.
  La mise à jour et le déploiement de nouvelles versions de l'application sur une VM peuvent nécessiter des actions manuelles, ce qui peut entraîner des erreurs et des interruptions de service.

- Sécurité intégrée : Kubernetes offre des fonctionnalités intégrées pour la gestion des secrets, le contrôle d'accès basé sur les rôles (RBAC) et la sécurisation des communications entre les composants de l'application. Cela facilite la mise en place de bonnes pratiques de sécurité.
  La sécurité doit être configurée et maintenue manuellement sur la VM, ce qui peut être une tâche complexe. La gestion des secrets et des informations d'identification sensibles peut également être plus difficile.

- Portabilité et flexibilité : Kubernetes offre une portabilité accrue des applications. Une fois que ton application est containerisée et déployée sur Kubernetes, tu peux la déplacer facilement vers d'autres environnements Kubernetes ou même vers d'autres fournisseurs de cloud. Cela te donne plus de flexibilité pour l'avenir.
  La migration de l'application vers un autre environnement ou fournisseur de cloud peut être compliquée en raison des dépendances spécifiques à la VM et des configurations spécifiques à l'environnement.

  En résumé, l'utilisation de Kubernetes sur un cluster AKS offre une gestion automatisée des ressources, une haute disponibilité, une gestion simplifiée des mises à jour et des versions, une sécurité intégrée, et une plus grande portabilité et flexibilité par rapport à la méthode de déploiement actuelle de CloudPanther.

### Etapes

 - Analyse des prérequis : Je doit m'assurer d'avoir les accès nécessaires à l'environnement cloud, y compris les droits d'administrateur pour AKS. Sans oublier de vérifier si Cloud Panther est compatible avec une architecture de conteneurisation.

 - Containerisation du site : Pour déployer CloudPanther sur AKS, il faut d'abord containeriser l'application. Je vais utiliser Docker pour créer une image conteneur. Je dois m'assurer que l'image contient tous les prérequis logiciels nécessaires pour exécuter le site.

 - Création du cluster AKS : Je vais maintenant créer un cluster AKS en spécifiant le nombre de nœuds, les tailles des machines virtuelles et les autres paramètres selon les besoins de CloudPanther.

 - Gestion de la sécurité : Pour garantir la sécurité de mon cluster AKS, je vais utiliser les fonctionnalités fournies par Azure, telles que le contrôle d'accès basé sur les rôles (RBAC), le réseau virtuel (Virtual Network) et les groupes de sécurité réseau (Network Security Groups). Je vais également configurer  le chiffrement TLS pour les communications entrantes et sortantes.

 - Déploiement de l'application : je vais utiliser Kubernetes pour déployer mon application Cloud Panther sur le cluster AKS. Crée des fichiers de déploiement Kubernetes (fichiers YAML) pour décrire les ressources nécessaires (pods, services, ingress, etc.). En m'assurant de bien définir les règles de sécurité dans les fichiers de déploiement.

 - Surveillance et gestion : Configuration des outils de surveillance tels que Azure Monitor pour suivre les performances et la disponibilité de mon cluster AKS. Je vais utiliser des outils comme Azure Log Analytics pour collecter et analyser les journaux d'application. Sans oublier de mettre en place des mécanismes de sauvegarde et de restauration pour mon cluster AKS.

 - Tests et validation : Et finalement, je vais effectuer des tests pour vérifier que le site Cloud Panther fonctionne correctement sur le cluster AKS. Vérifier l'évolutivité, la résilience et la sécurité de l'application dans un environnement de production.

### Documentation
- Préparation d'une documentation détaillée décrivant le processus d'automatisation et les mesures de sécurité mises en place.
