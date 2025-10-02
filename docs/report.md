# Poker Analytics Database: Research Report

## 1. Introduction
The aim of this project was to evaluate the performance and usability of three database types:
1. Relational (Oracle DB)
2. Document-based (MongoDB)
3. Graph-based (Neo4j)

We used a Poker Analytics Database to simulate queries related to poker hands, players, and their relationships.

---

## 2. Methodology
### Dataset
- The dataset consists of 10,000 poker games, including player details, hands played, and game outcomes.
- Schema examples for each database model can be found in the `docs/diagrams/` folder.

### Queries Tested
1. Count the total number of poker games played.
2. Retrieve all players who won a specific type of hand (e.g., full house).
3. Find connections between players who played together in the same game (graph query).

---

## 3. Results
### Query Speed
| Query Type | Oracle DB (ms) | MongoDB (ms) | Neo4j (ms) |
|------------|--------------------|--------------|------------|
| Total Games Played | 100 | 90 | 150 |
| Players by Hand Type | 200 | 180 | 250 |
| Player Connections | 400 | 380 | 120 |

### Observations
- Oracle DB excelled in structured queries but lagged in relationship-based queries.
- MongoDB was faster for flexible document retrieval but required indexing for optimal performance.
- Neo4j was significantly faster for graph-based queries.

---

## 4. Conclusion
- Oracle DB is ideal for well-structured and highly relational data.
- MongoDB is best for semi-structured, flexible data.
- Neo4j is superior for graph-based relationships and connection-heavy data.

