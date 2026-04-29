# MDM Solution – Power Platform (Diploma Thesis)

This repository contains an exported solution of a Master Data Management (MDM) prototype implemented using Microsoft Power Platform. The solution was developed as part of a diploma thesis focused on designing and validating an MDM approach for HR master data.

## 📌 Overview

The solution demonstrates how Microsoft Power Platform (Power Apps, Dataverse, Power Automate) can be used to implement a lightweight MDM system based on a medallion architecture (bronze → silver → gold).

The prototype integrates data from multiple source systems and provides mechanisms for:
- data ingestion
- data transformation and standardization
- duplicate detection and resolution
- change management
- centralized master data management via application layer

## 🏗️ Architecture

The solution follows a layered approach:

- **Bronze layer** – raw data ingestion from source systems
- **Silver layer** – data integration, transformation, and deduplication
- **Gold layer** – consolidated and curated master data

## 📁 Repository Structure

export/
│
├── MDMApp.zip # Solution ready to download

solution/
│
├── app_actions/ # Application logic and actions
├── canvas_apps/ # Canvas apps (Change Resolution, Matching Resolution)
├── workflows/ # Power Automate flows (data processing & orchestration)
├── web_resources/ # Supporting resources (UI, scripts)
│
├── customizations.xml # Dataverse customizations
├── solution.xml # Solution definition
└── [Content_Types].xml # Internal metadata

## ⚙️ Key Components

- **Power Apps**
  - Model-driven app for master data management
  - Canvas apps for:
    - Change Resolution
    - Matching Resolution

- **Microsoft Dataverse**
  - Central data storage
  - Implementation of medallion architecture

- **Power Automate**
  - Data ingestion from source systems (ERPNext, Odoo)
  - Transformation and orchestration flows

## 🔄 Functionality

The solution includes:

- Integration of multiple data sources
- Change detection using snapshot mechanism
- Manual validation of changes (Change Resolution app)
- Duplicate detection using:
  - unique identifiers
  - similarity scoring
- Manual merge of duplicate records (Matching Resolution app)
- Creation of a single source of truth (gold layer)

## ⚠️ Notes

- This repository contains an exported Power Platform solution.
- Some configuration (connections, environment variables) may be required to run the solution.
- The implementation represents a prototype (MVP) and is not intended for direct production use.

## 📚 Context

This solution was developed as part of a diploma thesis focused on:
> Designing and implementing an MDM solution using Microsoft Power Platform and evaluating its applicability in an organizational context.

## 👤 Author

Filip Lopen
