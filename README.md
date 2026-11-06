# Jackpot Generator Pro – Backend

**Version:** 0.1.0  
**Status:** Initial Development  
**Platform:** Windows Development Environment  
**Language:** Python  
**API Framework:** FastAPI  
**Database:** SQLite (initial implementation)

---

## 1. Project Overview

Jackpot Generator Pro is a cross-platform lottery research and number-generation application.

This repository contains the shared Python backend responsible for historical lottery data importing, database management, statistical analysis, number scoring, and backtesting.

The backend will support two independent native mobile applications:

- **iOS:** Swift / Xcode
- **Android:** Kotlin / Android Studio

Both applications will communicate with this backend through a shared REST API.

## 2. Project Objectives

The backend is designed to:

1. Maintain a centralized national lottery research database.
2. Import historical lottery drawings from multiple file formats.
3. Automatically discover files and database structures.
4. Normalize different source formats into a common data model.
5. Validate drawings against game-specific historical rules.
6. Detect duplicate drawing records.
7. Maintain source provenance and import history.
8. Provide statistical research and analysis.
9. Support number-generation scoring and historical backtesting.
10. Supply standardized data to both mobile applications.

Historical statistical analysis is for research purposes only. Lottery drawings are independent random events, and historical patterns do not predict future winning numbers or improve the mathematical odds of winning.

## 3. System Architecture

    iOS Application (Swift)
             |
             |
    Android Application (Kotlin)
             |
             |
       REST API (FastAPI)
             |
             |
       Python Backend
             |
      -----------------
      |       |       |
    Import  Analysis Scoring
    Engine  Engine   Engine
      |       |       |
      -----------------
             |
      Central Database
           SQLite
             |
       Future PostgreSQL

## 4. Supported Import Formats

The directory-based import engine is intended to support:

| Format | Extension |
|---|---|
| SQLite | .db, .sqlite, .sqlite3 |
| Microsoft Excel | .xlsx |
| CSV | .csv |
| Text | .txt |
| JSON | .json |
| XML | .xml |

Additional connectors for Microsoft Access and external database servers may be introduced in later versions.

## 5. Directory Structure

    JackpotGeneratorPro-Backend/
    |
    ├── backend/
    │   ├── api/
    │   ├── services/
    │   │   ├── import_engine/
    │   │   ├── normalization/
    │   │   ├── validation/
    │   │   ├── analysis/
    │   │   ├── scoring/
    │   │   └── backtesting/
    │   ├── database/
    │   ├── configuration/
    │   └── tests/
    |
    ├── lottery_data/
    │   ├── data_sources/
    │   │   ├── powerball/
    │   │   ├── mega_millions/
    │   │   ├── texas_lotto/
    │   │   ├── illinois_lotto/
    │   │   └── other_states/
    │   ├── processed/
    │   ├── rejected/
    │   ├── logs/
    │   └── reports/
    |
    ├── documentation/
    |
    ├── requirements.txt
    ├── .gitignore
    └── README.md

## 6. Initial Lottery Support

The first implementation will concentrate on:

- Powerball
- Mega Millions

Future expansion will include:

- Texas Lottery games
- Illinois Lottery games
- Additional state lottery games
- Other eligible national lottery datasets

Each lottery game will maintain its own rules, drawing history, and statistical analysis.

Historical rule changes will be maintained with effective dates.

## 7. Development Environment

The initial development environment uses:

- Windows 10 or Windows 11
- Python 3.11 or newer
- Visual Studio Code
- Git
- GitHub Desktop
- FastAPI
- SQLAlchemy
- SQLite
- Pytest

## 8. Installation and Setup

### Clone the repository

    git clone YOUR_GITHUB_REPOSITORY_URL

    cd LottoLedgerPro-Backend

### Create a Python virtual environment

    python -m venv .venv

### Activate the environment

PowerShell:

    .\.ven
