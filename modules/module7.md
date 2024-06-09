## Introduction du module 7 et objectifs

- Avantages d'Amazon CloudWatch.
- Avantages d'AWS CloudTrail.
- Avantages d'AWS Trusted Advisor.
---

## Amazon CloudWatch

Service de surveillance et de gestion des ressources AWS et des applications exécutées sur AWS.

- Surveillance des Ressources :
   - Collecte et suit les métriques des services AWS et des applications.
   - Surveille les instances EC2, les bases de données RDS, les fonctions Lambda, etc.
- Journalisation :
   - Collecte, surveille et analyse les logs d'application et de système.
   - Intègre les logs de divers services AWS pour une visibilité centralisée.
- Alertes et Notifications :
   - Configurez des alarmes pour recevoir des notifications en cas de dépassement de seuils prédéfinis.
   - Utilise Amazon SNS pour envoyer des alertes via email, SMS, ou appels d'API.
  
---

## Amazon CloudWatch : Tableau de bord

![](../images/cloudwatch.png)<!-- .element height="80%" width="80%" -->

---

## AWS CloudTrail

Service qui permet la gouvernance, la conformité, l'audit opérationnel et la gestion des risques de votre compte AWS.

- Enregistrement des Activités :
   - Enregistre les appels d'API AWS, les actions de la console, et les événements AWS SDK.
   - Capture les informations sur l'utilisateur, l'heure, l'IP source, et les détails des demandes.
- Surveillance Continue :
   - Fournit une visibilité continue sur les activités des utilisateurs et des ressources AWS.
   - Génère des journaux d'événements détaillés et les envoie à Amazon S3.
- Intégration avec CloudWatch :
   - Envoie les événements CloudTrail à Amazon CloudWatch Logs pour la surveillance en temps réel et les alertes.

---

## Exemple : événement Cloud Trail

![](../images/cloudtrail.png)<!-- .element height="80%" width="80%" -->

---

## CloudTrail Insights

- Dans CloudTrail, vous pouvez également activer CloudTrail Insights. Cette fonction facultative permet à CloudTrail de détecter automatiquement les activités d'API inhabituelles sur votre compte AWS. 

- Par exemple, CloudTrail Insights peut détecter si un nombre plus élevé d'instances Amazon EC2 que d'habitude a récemment été lancé dans votre compte. Vous pouvez ensuite consulter tous les détails de l'événement pour déterminer les actions que vous devez effectuer ensuite.

---

<!-- .slide: data-auto-animate -->
#### Quiz: Quelles tâches pouvez-vous effectuer à l'aide d'AWS CloudTrail ? (Sélectionnez DEUX propositions.) <!-- .element: style="color:#fd9731;" -->

- Surveiller votre infrastructure et vos ressources AWS en temps réel
- Suivre les activités des utilisateurs et les demandes d'API dans l'ensemble de votre infrastructure AWS
- Afficher les métriques et les graphiques pour surveiller les performances des ressources
- Filtrer les journaux pour faciliter l'analyse opérationnelle et le dépannage
- Configurer les actions et alertes automatiques en réponse aux métriques

---

<!-- .slide: data-auto-animate -->
#### Quiz: Quelles tâches pouvez-vous effectuer à l'aide d'AWS CloudTrail ? (Sélectionnez DEUX propositions.) <!-- .element: style="color:#fd9731;" -->

- Surveiller votre infrastructure et vos ressources AWS en temps réel
- Suivre les activités des utilisateurs et les demandes d'API dans l'ensemble de votre infrastructure AWS <!-- .element: style="color:#0de07d;" -->
- Afficher les métriques et les graphiques pour surveiller les performances des ressources
- Filtrer les journaux pour faciliter l'analyse opérationnelle et le dépannage <!-- .element: style="color:#0de07d;" -->
- Configurer les actions et alertes automatiques en réponse aux métriques

---

## AWS Trusted Advisor

- service web qui inspecte votre environnement AWS et fournit des recommandations en temps réel, conformément aux bonnes pratiques AWS.
- compare ses résultats aux bonnes pratiques AWS selon cinq catégories : 
   - l'optimisation des coûts, 
   - les performances, 
   - la sécurité, 
   - la tolérance aux pannes,
   - les limites de service.

---

## Tableau de bord : trustadvisor

![](../images/trustadvisor.jpg)<!-- .element height="80%" width="80%" -->

- La coche verte indique le nombre d'éléments pour lesquels aucun problème n'a été détecté.
- Le triangle orange représente le nombre d'avertissements/recommandations
- Le cercle rouge représente les problèmes critiques/actions recommandées.

---

<!-- .slide: data-auto-animate -->
#### Quiz: Quelles actions pouvez-vous effectuer à l'aide d'Amazon CloudWatch ? (Sélectionnez DEUX propositions.) <!-- .element: style="color:#fd9731;" -->

- Surveiller l'utilisation et les performances de vos ressources
- Recevoir des conseils en temps réel pour améliorer votre environnement AWS
- Comparer votre infrastructure aux bonnes pratiques AWS en cinq catégories
- Accéder aux métriques à partir d'un tableau de bord unique
- Détecter automatiquement les activités inhabituelles du compte

---

<!-- .slide: data-auto-animate -->
#### Quiz: Quelles actions pouvez-vous effectuer à l'aide d'Amazon CloudWatch ? (Sélectionnez DEUX propositions.) <!-- .element: style="color:#fd9731;" -->

- Surveiller l'utilisation et les performances de vos ressources <!-- .element: style="color:#0de07d;" -->
- Recevoir des conseils en temps réel pour améliorer votre environnement AWS
- Comparer votre infrastructure aux bonnes pratiques AWS en cinq catégories
- Accéder aux métriques à partir d'un tableau de bord unique <!-- .element: style="color:#0de07d;" -->
- Détecter automatiquement les activités inhabituelles du compte

---

<!-- .slide: data-auto-animate -->
#### Quiz: Quel service vous permet de vérifier la sécurité de vos compartiments Amazon S3 en vérifiant les autorisations d'accès libre ? <!-- .element: style="color:#fd9731;" -->

- Amazon CloudWatch
- AWS CloudTrail
- AWS Trusted Advisor
- Amazon GuardDuty

---

<!-- .slide: data-auto-animate -->
#### Quiz: Quel service vous permet de vérifier la sécurité de vos compartiments Amazon S3 en vérifiant les autorisations d'accès libre ? <!-- .element: style="color:#fd9731;" -->

- Amazon CloudWatch
- AWS CloudTrail
- AWS Trusted Advisor <!-- .element: style="color:#0de07d;" -->
- Amazon GuardDuty

---

<!-- .slide: data-auto-animate -->
#### Quiz: Quelles sont les catégories incluses dans le tableau de bord AWS Trusted Advisor ? (Sélectionnez DEUX propositions.) <!-- .element: style="color:#fd9731;" -->

- Fiabilité
- Performances
- Capacité de mise à l'échelle
- Élasticité
- Tolérance aux pannes

---

<!-- .slide: data-auto-animate -->
#### Quiz: Quelles sont les catégories incluses dans le tableau de bord AWS Trusted Advisor ? (Sélectionnez DEUX propositions.) <!-- .element: style="color:#fd9731;" -->

- Fiabilité
- Performances <!-- .element: style="color:#0de07d;" -->
- Capacité de mise à l'échelle
- Élasticité
- Tolérance aux pannes <!-- .element: style="color:#0de07d;" -->


