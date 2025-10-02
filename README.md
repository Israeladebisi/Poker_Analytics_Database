# Poker Analytics Database

[![Python](https://img.shields.io/badge/Python-3.11-blue.svg)](https://www.python.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-6.x-brightgreen.svg)](https://www.mongodb.com/)
[![Neo4j](https://img.shields.io/badge/Neo4j-5.x-orange.svg)](https://neo4j.com/)
[![Oracle](https://img.shields.io/badge/Oracle-19c-red.svg)](https://www.oracle.com/database/)

---

## 📌 Overview
This project compares three database systems—**Oracle RDBMS**, **MongoDB**, and **Neo4j**—using a poker tournament dataset.  
The goal is to evaluate how each system handles **structured, semi-structured, and graph-oriented data**, measuring **ease of use, efficiency, and query runtimes**.

The project is split into:
- 📓 A **Jupyter Notebook** with Oracle + MongoDB implementations.  
- 📄 A **detailed report** covering Neo4j, screenshots, and a final cross-database comparison.

---

## 🗂 Dataset
- **Source**: Poker tournament text files  
- **Scope**: 10 tournaments parsed into players, rounds, games, and hands  
- **Format**: Mix of structured (tabular), semi-structured (CSV/JSON), and graph CSVs  

---

## ⚙️ Tech Stack
- **Databases**: Oracle RDBMS · MongoDB · Neo4j  
- **Languages & Tools**: Python 3.11 · Pandas · PyMongo · oracledb · Cypher · SQL · MQL  
- **Notebooks**: Jupyter Notebook (Oracle & MongoDB analysis)  

---

## 📊 Sample Queries
The project explores a variety of analytical queries to test each database's strengths. Examples include:
- Group players by playing style. 
- Analyze win frequency by table position.
- Top 10 largest pots and winning hands  
- Top 9 winning card combinations by frequency  
- Players in a given tournament  
- Most common bet with pocket aces pre-flop  
- Player who won the most money in 2023  
- Most aggressive bettor  
- Players with most “Final Tables”  

(A full list of queries and their performance is available in the *[report](docs/report.md).*)  

---

## 📄 Reports & Docs
- 📘 [Full Project Report](docs/report.md)  
---

## 🔍 Results Summary
| Database     | Strengths                                  | Limitations                           |
|--------------|---------------------------------------------|----------------------------------------|
| Oracle RDBMS | Schema integrity, structured queries        | Rigid schema, costly schema changes    |
| MongoDB      | Flexible schema, semi-structured ingest     | Complex, nested aggregation pipelines  |
| Neo4j        | Graph analytics, relationship-driven queries| Less efficient for purely tabular data |

*(Detailed runtime comparison in the report)*  

---

## 📂 Repository Structure
```text
poker-analytics-database/
├── src/                 # Code for setting up and querying each database
│   ├── relational/      # Scripts for Oracle DB
│   ├── document/        # Scripts for MongoDB
│   ├── graph/           # Scripts for Neo4j
│   └── setup/           # Game/player files, parsers
│
├── data/                # Sample datasets
│   ├── games/        # Schema/architecture diagrams
│   └── Players CSV
│
├── docs/                # Documentation and resources
│   └── report.md
│
└──  README.md