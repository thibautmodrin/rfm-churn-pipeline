# 🧠 RFM + Churn Pipeline | Airbyte • Snowflake • dbt • Tableau

> 📦 Pipeline Data Marketing complet en cours de développement

---

## 🎯 Objectif

Ce projet a pour objectif de construire un **pipeline automatisé** permettant de :

- Identifier les **segments RFM** (Recency, Frequency, Monetary)
- Prédire les clients à **risque de churn**
- Visualiser et exploiter ces données dans un **dashboard marketing interactif**
- Faciliter l’**activation des segments** pour des campagnes ciblées

---

## 🧩 Problématique métier

> 🎯 *"Comment identifier et prédire les clients inactifs à risque de churn afin d’optimiser les campagnes de relance marketing et augmenter le taux de réachat ?"*

Contexte : Une boutique e-commerce constate une baisse de réachat. Le service marketing cherche à **cibler plus intelligemment ses relances** et **mieux allouer son budget d’acquisition**.

---

## 🧱 Stack technique

| Outil         | Rôle                                                        |
|---------------|-------------------------------------------------------------|
| **Airbyte**   | Ingestion automatisée (CSV / API CRM)                      |
| **Snowflake** | Stockage des données (raw, staging, marts)                 |
| **dbt**       | Transformation, scoring RFM, prédiction churn, documentation |
| **Tableau**   | Visualisation des segments et probabilités de churn        |
| *(optionnel)* **Airflow** | Orchestration du pipeline                     |

---

## 🔄 Pipeline


1. 📥 Airbyte → ingestion depuis CRM (ex : fichiers CSV, HubSpot)
2. 🧊 Snowflake → stockage des données brutes (raw)
3. ⚙️ dbt → nettoyage, calcul RFM, prédiction churn, tests
4. 📈 Tableau → dashboard interactif pour l'équipe marketing

---

## 🗂️ Structure du dépôt (en cours)

rfm-churn-pipeline/
├── airbyte/                  # Config Airbyte source/destination
├── dbt_project/              # Projet dbt complet (models, tests, docs)
├── tableau/                  # Dashboard + screenshots
├── data/                     # Données simulées clients / commandes
├── notebooks/                # Modèle de churn (exploration + prédiction)
├── snowflake_schema.sql      # Setup initial du data warehouse
├── requirements.txt
└── README.md
