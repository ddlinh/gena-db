# Gena User Guide

## What is Gena Knowledge Graph?
**Gena Knowledge Graph** represents the relationships between Nutrition and Health and focuses especially on the association of Chemical/Nutrient/Biochemical entity group with Mental Health. There are 5 main modules in this project with the corresponding codes below:
1. [Get the available data from 2 available Knowledge base called DOID Ontology and BC5CDR Corpus](https://github.com/ddlinh/gena-db/blob/main/src/%5Bcode%5D%20food_and_disease_data.ipynb)
2. [Get the related papers using specific keywords](https://github.com/ddlinh/gena-db/blob/main/src/%5Bcode%5D%20Get_and_Clean_Papers.ipynb)
3. [Named Entity Recognition](https://github.com/ddlinh/gena-db/blob/main/src/%5Bcode%5D%20Named_Entities_Recognition.ipynb)
4. [Relation Extraction](https://github.com/ddlinh/gena-db/blob/main/src/%5Bcode%5D%20Relation_Extraction.ipynb)
5. Knowledge Graph Construction with 2 small steps:
    * [Setting unique ID for entities](https://github.com/ddlinh/gena-db/blob/main/src/%5Bcode%5D%20Triple_Construction.ipynb)
    * [Creating Knowledge Graph using Neo4J](https://github.com/ddlinh/gena-db/blob/main/src/%5Bcode%5D%20GENA_KG.ipynb)

## How to access to Gena Knowledge Graph?
1. Access to [Gena DB](https://browser.neo4j.io/?connectURL=neo4j%2Bs%3A%2F%2Fneo4j%405cd8c3cd.databases.neo4j.io%2F).
2. Enter:
    * username: neo4j
    * password: RWY0rgJWWysmEbk808JCUv74jF-VrKBEfchJxy1vp5Q
3. Make your first query with [CQL](https://neo4j.com/developer/cypher/).
   * For example: "MATCH (n1)-[r]->(n2) RETURN n1, r, n2 LIMIT 20")
   <img width="655" alt="image" src="https://user-images.githubusercontent.com/60208884/171038060-be2d6670-54ed-4b92-9bb7-b0863c52c0a2.png">
