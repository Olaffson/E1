# E1 — Grilles d'évaluation d'analyse de besoin data
## Projet : ShopNow Marketplace
### Certification RNCP 37638 — Expert en données massives (Data Engineer)

---

## Contexte du projet

**ShopNow** est une plateforme e-commerce en cours de transformation vers un modèle **marketplace multi-vendeurs**. L'organisation souhaite centraliser et exploiter les données produites par l'ensemble des acteurs de la plateforme (vendeurs tiers, acheteurs, équipes internes) afin de piloter la performance commerciale, améliorer l'expérience client et répondre aux exigences strictes du **RGPD**.

L'infrastructure cible repose sur **Microsoft Azure** (Azure Data Factory, Azure Synapse Analytics, Azure Data Lake Storage, Power BI). Le projet data a pour but de construire un entrepôt de données (data warehouse) permettant des analyses fiables sur les ventes, les vendeurs, les stocks et les comportements clients.

**Commanditaire** : Direction Générale / DSI de ShopNow  
**Rôle du candidat** : Data Engineer — chef de projet data

---

## GRILLE 1 — Entretien avec les usagers qui **produisent** la donnée

> *Destinée aux métiers qui génèrent, saisissent ou alimentent les données : vendeurs tiers, équipe logistique/opérations, équipe produit/catalogue.*

---

### Informations générales sur l'interlocuteur

| Champ | Réponse |
|---|---|
| Nom / Prénom | |
| Intitulé du poste | |
| Service / Département | |
| Ancienneté dans le poste | |
| Date de l'entretien | |
| Durée estimée | 45 min |

---

### Bloc 1 — Activités métier et périmètre fonctionnel

**Objectif** : Comprendre les activités métier qui génèrent de la donnée et identifier les enjeux liés à la transformation marketplace.

| N° | Question | Réponse / Notes |
|---|---|---|
| 1.1 | Pouvez-vous décrire vos principales missions au quotidien ? | |
| 1.2 | Quelles sont les actions ou processus dans votre travail qui génèrent de la donnée (ex : création d'une fiche produit, validation d'une commande, mise à jour de stock) ? | |
| 1.3 | Y a-t-il des activités saisonnières ou événementielles (soldes, Black Friday) qui modifient significativement le volume ou la nature des données produites ? | |
| 1.4 | Avez-vous connaissance de la transformation en cours vers un modèle marketplace multi-vendeurs ? En quoi cela impacte-t-il vos activités actuelles ? | |
| 1.5 | Quels sont selon vous les principaux défis ou risques liés à cette transformation pour votre métier ? | |
| 1.6 | Existe-t-il des processus manuels actuellement (tableurs, saisies papier, exports CSV) qui pourraient être automatisés dans le cadre du projet ? | |

---

### Bloc 2 — Caractérisation des données produites

**Objectif** : Identifier les données générées, leur structure, leur volume et leur fréquence de production.

| N° | Question | Réponse / Notes |
|---|---|---|
| 2.1 | Quels types de données produisez-vous ou saisissez-vous dans le cadre de vos missions (commandes, produits, stocks, transactions, avis, retours…) ? | |
| 2.2 | Ces données sont-elles structurées (tables SQL, formulaires), semi-structurées (JSON, XML) ou non structurées (fichiers, images, emails) ? | |
| 2.3 | Quel est le volume approximatif de données générées par jour / semaine / mois ? | |
| 2.4 | À quelle fréquence ces données sont-elles créées ou mises à jour (temps réel, toutes les heures, quotidiennement…) ? | |
| 2.5 | Existe-t-il des données sensibles ou personnelles parmi celles que vous produisez (coordonnées vendeurs, données bancaires, identité clients) ? Si oui, lesquelles ? | |
| 2.6 | Y a-t-il des données critiques dont la perte ou l'indisponibilité aurait un impact immédiat sur votre activité ? Lesquelles ? | |
| 2.7 | Les données que vous produisez sont-elles partagées avec d'autres équipes ou systèmes ? Si oui, lesquels et sous quelle forme ? | |

---

### Bloc 3 — Métadonnées

**Objectif** : Identifier les informations contextuelles associées aux données (qui, quand, comment, pourquoi).

| N° | Question | Réponse / Notes |
|---|---|---|
| 3.1 | Existe-t-il un dictionnaire de données ou une documentation décrivant les champs que vous renseignez ? | |
| 3.2 | Les données que vous produisez sont-elles horodatées automatiquement ? Y a-t-il un suivi de l'auteur de la modification ? | |
| 3.3 | Existe-t-il des règles de nommage ou des formats imposés pour certains champs (ex : code produit, référence vendeur) ? | |
| 3.4 | Comment gérez-vous les erreurs de saisie ou les données incomplètes ? Existe-t-il des validations automatiques ? | |
| 3.5 | Y a-t-il des métadonnées de traçabilité importantes pour votre activité (historique des modifications, logs d'actions) ? | |

---

### Bloc 4 — Stockage et systèmes d'information

**Objectif** : Identifier les systèmes et outils utilisés pour stocker et gérer les données.

| N° | Question | Réponse / Notes |
|---|---|---|
| 4.1 | Dans quel(s) système(s) ou outil(s) saisissez-vous ou déposez-vous vos données (ERP, CMS, outil de gestion des commandes, Excel, API partenaire…) ? | |
| 4.2 | Ces systèmes sont-ils hébergés localement (on-premise) ou dans le cloud ? Savez-vous lesquels ? | |
| 4.3 | Y a-t-il des données stockées localement sur vos postes de travail (fichiers Excel, dossiers partagés) qui ne sont pas centralisées ? | |
| 4.4 | Y a-t-il des systèmes tiers ou des intégrations avec des partenaires externes qui génèrent des données (transporteurs, passerelles de paiement, places de marché) ? | |
| 4.5 | Connaissez-vous la durée de rétention appliquée aux données que vous produisez ? | |

---

### Bloc 5 — Accès aux données et gouvernance

**Objectif** : Comprendre les règles d'accès, les autorisations et la gouvernance autour des données produites.

| N° | Question | Réponse / Notes |
|---|---|---|
| 5.1 | Qui a accès aux données que vous produisez en dehors de votre équipe ? | |
| 5.2 | Existe-t-il des restrictions d'accès ou des habilitations spécifiques pour certaines données (données financières, données personnelles) ? | |
| 5.3 | Avez-vous déjà rencontré des situations où des données ont été consultées ou modifiées sans votre accord ? | |
| 5.4 | Êtes-vous informé(e) des règles RGPD qui s'appliquent aux données que vous gérez ? Avez-vous reçu une formation sur ce sujet ? | |
| 5.5 | Y a-t-il un responsable de la donnée désigné dans votre équipe (data owner / référent données) ? | |

---

### Bloc 6 — Traitements appliqués aux données

**Objectif** : Identifier les transformations, agrégations ou traitements que les producteurs de données réalisent eux-mêmes.

| N° | Question | Réponse / Notes |
|---|---|---|
| 6.1 | Réalisez-vous vous-même des traitements sur vos données avant de les transmettre à d'autres équipes (nettoyage, mise en forme, calculs) ? | |
| 6.2 | Existe-t-il des processus automatisés en place (scripts, imports automatiques, synchronisations) ? Si oui, par qui sont-ils maintenus ? | |
| 6.3 | Avez-vous déjà rencontré des problèmes de qualité de données (doublons, valeurs manquantes, formats incohérents) ? Comment ont-ils été traités ? | |
| 6.4 | Y a-t-il des règles métier implicites appliquées à vos données que nous devrions documenter (ex : une commande n'est validée que si le paiement est confirmé) ? | |

---

### Bloc 7 — Besoins et attentes vis-à-vis du projet data

| N° | Question | Réponse / Notes |
|---|---|---|
| 7.1 | Quelles améliorations attendez-vous du projet data en termes d'outils ou de processus pour votre métier ? | |
| 7.2 | Y a-t-il des données que vous voudriez pouvoir consulter ou suivre plus facilement qu'actuellement ? | |
| 7.3 | Avez-vous des contraintes particulières à prendre en compte (disponibilité, accès, confidentialité) ? | |
| 7.4 | Seriez-vous disponible pour valider les résultats du projet (recette fonctionnelle, tests) ? | |

---

### Synthèse de l'entretien — Producteur de données

| Élément | Contenu |
|---|---|
| Principales données produites identifiées | |
| Systèmes sources identifiés | |
| Points de vigilance RGPD | |
| Besoins exprimés | |
| Actions à mener suite à l'entretien | |

---
---

## GRILLE 2 — Entretien avec les usagers qui **exploitent** la donnée

> *Destinée aux métiers qui analysent, consultent ou utilisent les données pour prendre des décisions : direction commerciale, marketing, finance, contrôle de gestion, équipe analytics.*

---

### Informations générales sur l'interlocuteur

| Champ | Réponse |
|---|---|
| Nom / Prénom | |
| Intitulé du poste | |
| Service / Département | |
| Ancienneté dans le poste | |
| Date de l'entretien | |
| Durée estimée | 45 min |

---

### Bloc 1 — Activités métier et besoins d'analyse

**Objectif** : Comprendre les usages actuels de la donnée et les besoins analytiques liés à la transformation marketplace.

| N° | Question | Réponse / Notes |
|---|---|---|
| 1.1 | Pouvez-vous décrire vos principales missions et décisions qui reposent sur des données ? | |
| 1.2 | Quels sont les indicateurs clés (KPI) que vous suivez au quotidien / hebdomadairement / mensuellement ? | |
| 1.3 | Disposez-vous actuellement de tableaux de bord ou de rapports ? Qui les produit et à quelle fréquence sont-ils mis à jour ? | |
| 1.4 | Y a-t-il des analyses que vous aimeriez réaliser mais que vous ne pouvez pas faire actuellement faute de données ou d'outils ? | |
| 1.5 | Comment la transformation en marketplace multi-vendeurs va-t-elle modifier vos besoins d'analyse ? Quels nouveaux indicateurs seront nécessaires ? | |
| 1.6 | Quelle est la granularité des données dont vous avez besoin (détail par transaction, par vendeur, par produit, par jour…) ? | |

---

### Bloc 2 — Caractérisation des données exploitées

**Objectif** : Identifier les données consultées, leur nature, leur niveau de qualité requis et leur fraîcheur attendue.

| N° | Question | Réponse / Notes |
|---|---|---|
| 2.1 | Quels types de données consultez-vous dans le cadre de vos missions (ventes, marges, taux de retour, comportement client, performance vendeur…) ? | |
| 2.2 | Ces données proviennent-elles d'une source unique ou de plusieurs systèmes différents ? Si plusieurs, y a-t-il des incohérences entre elles ? | |
| 2.3 | Quelle est la fraîcheur des données dont vous avez besoin (données en temps réel, du jour précédent, de la semaine…) ? | |
| 2.4 | Avez-vous des problèmes de qualité de données actuels (chiffres incohérents entre rapports, données manquantes) ? Pouvez-vous les décrire ? | |
| 2.5 | Y a-t-il des données personnelles que vous consultez dans le cadre de vos analyses (ex : historique client nominatif, données de contact vendeur) ? | |
| 2.6 | Avez-vous des besoins d'historisation des données (comparaisons annuelles, évolution sur 3 ans…) ? Sur quelle profondeur historique ? | |

---

### Bloc 3 — Métadonnées et compréhension de la donnée

**Objectif** : Évaluer la maturité de l'exploitant vis-à-vis de la compréhension des données qu'il utilise.

| N° | Question | Réponse / Notes |
|---|---|---|
| 3.1 | Disposez-vous d'un glossaire métier définissant les termes et indicateurs utilisés dans vos rapports ? | |
| 3.2 | Connaissez-vous la source exacte des données que vous consultez (quel système, quelle base) ? | |
| 3.3 | Avez-vous déjà rencontré des situations où la définition d'un indicateur différait selon l'équipe ou le rapport consulté ? | |
| 3.4 | Y a-t-il des indicateurs dont le mode de calcul est ambigu ou mal documenté ? | |
| 3.5 | Quelles sont les données pour lesquelles vous avez le plus besoin de pouvoir tracer l'origine (auditabilité) ? | |

---

### Bloc 4 — Accès aux données et outils d'exploitation

**Objectif** : Identifier les outils utilisés pour accéder aux données et les contraintes d'accès.

| N° | Question | Réponse / Notes |
|---|---|---|
| 4.1 | Quels outils utilisez-vous pour consulter ou analyser les données (Power BI, Excel, SQL, Tableau, exports CSV…) ? | |
| 4.2 | Accédez-vous directement aux bases de données ou passez-vous par des exports ou des rapports intermédiaires ? | |
| 4.3 | Avez-vous des restrictions d'accès à certaines données que vous jugez nécessaires pour votre activité ? | |
| 4.4 | Combien de personnes dans votre équipe ont besoin d'accéder aux données analytiques du projet ? | |
| 4.5 | Y a-t-il des données auxquelles vous accédez et qui, selon vous, ne devraient pas être accessibles à tous (confidentialité commerciale, données personnelles) ? | |
| 4.6 | Avez-vous des besoins d'accès mobile ou nomade aux données (consultation hors bureau, en déplacement) ? | |

---

### Bloc 5 — Traitements et analyses réalisés

**Objectif** : Identifier les types d'analyses et de traitements que les exploitants réalisent sur les données.

| N° | Question | Réponse / Notes |
|---|---|---|
| 5.1 | Réalisez-vous des analyses de type comparatif (période N vs N-1, vendeur A vs vendeur B) ? | |
| 5.2 | Avez-vous besoin d'analyses prédictives ou de projections (prévision de ventes, anticipation de ruptures de stock) ? | |
| 5.3 | Faites-vous des croisements de données provenant de sources différentes ? Si oui, lesquelles ? | |
| 5.4 | Exportez-vous régulièrement des données vers d'autres outils (Excel, Google Sheets, PowerPoint) ? Pour quels usages ? | |
| 5.5 | Y a-t-il des traitements ou des calculs que vous réalisez manuellement chaque semaine/mois et qui pourraient être automatisés ? | |

---

### Bloc 6 — Exigences fonctionnelles et non-fonctionnelles

**Objectif** : Recueillir les exigences de performance, de disponibilité et d'accessibilité attendues par les exploitants.

| N° | Question | Réponse / Notes |
|---|---|---|
| 6.1 | À quelle fréquence consultez-vous les données analytiques (temps réel, quotidien, hebdomadaire) ? | |
| 6.2 | Quelle est la tolérance acceptable à un délai de mise à jour des données (ex : données du jour J disponibles à J+1 matin) ? | |
| 6.3 | Y a-t-il des plages horaires critiques où l'accès aux données est impératif (ex : réunion de direction tous les lundis matin) ? | |
| 6.4 | Avez-vous des besoins spécifiques d'accessibilité numérique pour consulter les rapports (taille de police, contraste, compatibilité lecteur d'écran) ? | |
| 6.5 | Quelles sont vos exigences en termes de performance des requêtes ou de chargement des tableaux de bord ? | |

---

### Bloc 7 — Gouvernance, conformité RGPD et sécurité

**Objectif** : S'assurer que les exploitants sont sensibilisés aux enjeux de conformité des données qu'ils consultent.

| N° | Question | Réponse / Notes |
|---|---|---|
| 7.1 | Êtes-vous informé(e) des obligations RGPD liées aux données que vous consultez (données clients, données vendeurs) ? | |
| 7.2 | Exportez-vous des données personnelles hors des systèmes sécurisés ? Si oui, dans quel cadre et avec quelles précautions ? | |
| 7.3 | Y a-t-il des données que vous consultez et dont vous ne savez pas si elles sont conformes au RGPD ? | |
| 7.4 | Avez-vous des exigences en matière de conservation ou de suppression des données analytiques ? | |
| 7.5 | Seriez-vous prêt(e) à participer à la définition des règles d'accès aux données analytiques dans le cadre du projet ? | |

---

### Bloc 8 — Attentes et priorités vis-à-vis du projet data

| N° | Question | Réponse / Notes |
|---|---|---|
| 8.1 | Quel est, selon vous, le bénéfice le plus important que vous attendez du projet data ? | |
| 8.2 | Y a-t-il un indicateur ou un rapport dont vous auriez besoin en priorité dès la première version livrée ? | |
| 8.3 | Seriez-vous disponible pour participer aux phases de validation et de recette des livrables analytiques ? | |
| 8.4 | Y a-t-il des contraintes organisationnelles ou calendaires à prendre en compte (ex : clôture financière, audit annuel) ? | |
| 8.5 | Avez-vous des retours d'expérience sur des projets data précédents (réussites ou échecs) qui pourraient nous aider ? | |

---

### Synthèse de l'entretien — Exploitant de données

| Élément | Contenu |
|---|---|
| Principaux besoins d'analyse identifiés | |
| KPI prioritaires exprimés | |
| Problèmes de qualité de données signalés | |
| Exigences de fraîcheur et de disponibilité | |
| Points de vigilance RGPD | |
| Actions à mener suite à l'entretien | |

---

## Annexe — Cartographie préliminaire des parties prenantes ShopNow Marketplace

| Catégorie | Rôle | Producteur / Exploitant |
|---|---|---|
| Vendeurs tiers | Gestionnaire de catalogue, responsable stock | Producteur |
| Logistique | Responsable expéditions, gestion des retours | Producteur |
| Équipe produit | Product Owner marketplace | Producteur / Exploitant |
| Direction Commerciale | Directeur commercial, responsable ventes | Exploitant |
| Marketing | Responsable acquisition, CRM | Exploitant |
| Finance / Contrôle de gestion | Analyste financier, DAF | Exploitant |
| DSI / Data Team | Data Engineer, Data Analyst | Producteur / Exploitant |
| Direction Générale | CEO, COO | Exploitant |
| DPO | Délégué à la Protection des Données | Exploitant (conformité) |

---

*Document rédigé dans le cadre de la certification RNCP 37638 — Expert en données massives (Data Engineer) — Simplon*
