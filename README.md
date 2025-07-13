# EIMP
Environmental Incident Management Platform

# Description 
## Contexte
Les autorités locales manquent souvent de visibilité en temps réel sur les incidents environnementaux (décharges sauvages, pollution, fuites, nuisances…).
Les citoyens, de leur côté, n’ont ni un canal structuré pour signaler ces problèmes, ni la certitude qu’ils sont traités efficacement.
➡️ Résultat : frustration, lenteur, perte de confiance.

## Problématique
* Comment permettre aux citoyens de signaler rapidement un incident environnemental de façon géolocalisée et sécurisée ?

* Comment les autorités peuvent-elles prioriser, traiter et suivre efficacement ces incidents ?

* Comment améliorer la communication et la transparence entre les deux parties, sans surcharger les agents publics ?

## Objectif fonctionnel
* Mettre en place une plateforme intuitive de signalement et suivi des incidents environnementaux.

## Objectif technique
* Concevoir une architecture modulaire, scalable et résiliente basée sur les microservices avec Spring Boot + Spring Cloud.
* Garantir la sécurité, la traçabilité, et l’observabilité des services.

## Objectif de valeur
* Réduire le délai de traitement des incidents de 40%
* Augmenter l’engagement citoyen
* Améliorer la satisfaction des agents publics
## Les microservices 
  * Service Signalement :
    * Création d'incidents géolocalisés (photo + description)
    * Stockage avec MongoDB + GridFS pour les fichiers

  * Service Traitement :
    * Attribution automatique aux équipes compétentes (IA simulée ou règle simple)
    * Workflow de validation avec état (en attente, en cours, résolu)

  * Service Notifications :
    * Envoi d’e-mails ou notifications push (Kafka + Mailgun)
  * Service Utilisateur :
    * Authentification (OAuth2 / JWT)
    * Rôles : citoyen, agent, admin
  * Service Suivi/Statistiques :
    * Dashboards pour la mairie avec agrégation via Spring Cloud Stream + Kafka