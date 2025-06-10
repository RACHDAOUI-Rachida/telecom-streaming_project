# Telecom Data Pipeline for Mediation, Rating and Billing Process

## 📌 Project Overview

This project simulates a complete telecom billing pipeline. It includes:
- **Synthetic CDR (Call Detail Record) generation**
- **Mediation layer**: cleansing and normalization of raw CDRs
- **Rating engine**: application of pricing rules based on usage
- **Billing engine**: generation of monthly invoices per client

The objective is to demonstrate a simplified version of a real telecom billing architecture, ideal for data processing and ETL practices.

---

## 🏗️ Architecture Overview

[Synthetic Data Generator]
↓
[Mediation Layer]
↓
[Rating Engine]
↓
[Billing Engine]
↓
[Output Reports / Invoices]


---

## ⚙️ Technologies Used

- **Python 3.x**
- **Pandas** for data processing
- **Faker** for synthetic data generation
- **CSV/JSON** as data formats
- **Jupyter Notebooks** for prototyping (optional)
- **Matplotlib / Seaborn** for visualization (optional)
- *(Optional)* PostgreSQL or SQLite for data persistence

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/RACHDAOUI-Rachida/telecom-streaming_project.git
cd telecom-streaming_project
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate




4. Run the Pipeline

Each component has a dedicated script:

generate_cdr.py: generates synthetic telecom records

mediation.py: cleans and prepares the data

rating.py: applies pricing rules

billing.py: aggregates results and generates invoices

You can also use main.py to run the full pipeline sequentially.

python main.py



📁 Project Structure
Ce projet est un pipeline de traitement distribué pour les tâches de rating et billing, structuré autour de plusieurs composants Dockerisés. Voici l’arborescence :

.
├── billing-job/
│   ├── billing_app.py          # Application de calcul de facturation
│   └── dockerfile              # Dockerfile pour l'image billing
│
├── rating-job/
│   ├── rating_app.py           # Application de calcul de rating
│   ├── data_generator.py       # Générateur de données pour Kafka
│   ├── dockerfile              # Dockerfile pour l'image rating
│
├── data/
│   └── sample_data.jsonl       # Données d’exemple au format JSON Lines
│
├── docker-compose.yml          # Orchestration des services avec Docker Compose
├── kafka-producer.py           # Producteur Kafka indépendant
├── spark_app.py                # Application Spark pour le traitement en streaming
└── README.md                   # Documentation du projet


