# Gena User Guide

## How to access to Gena Knowledge Graph on UI?
1. Access to [AuraDB Connection](https://workspace-preview.neo4j.io/terms-and-conditions) and click Accept on Terms & Condition.
![image](https://github.com/ddlinh/gena-db/assets/60208884/1f12afd7-b5a0-4bee-92a4-7f98e3bb7377)

2. Click the **Connection** dropdown, and choose the **Connect** option.
![image](https://github.com/ddlinh/gena-db/assets/60208884/d2efe4a3-42fb-4229-a448-931cd232c58f)

3. Enter:
(Wait 60 seconds before connecting using these details)
  * NEO4J_URI=neo4j+s://e5c905b4.databases.neo4j.io
  * NEO4J_USERNAME=neo4j
  * NEO4J_PASSWORD=jpAl3O0n2X4Znvco3LtqM9fGoNamvGJH4PpdxPEJvlM

![image](https://github.com/ddlinh/gena-db/assets/60208884/fbcc4f2f-1508-47f1-b388-0f3b4b6267af)


4. Make your first query with [CQL](https://neo4j.com/developer/cypher/).
   * For example: "MATCH (n1:NUTRITION)-[r]->(n2:MENTAL_HEALTH) RETURN n1, r, n2 LIMIT 10")
   ![image](https://github.com/ddlinh/gena-db/assets/60208884/cd9f33fe-6cdf-47da-851f-f09c9d435c09)

This query aims to extract the 10 directed relations from Nutrition to Mental Health. You can easily custom the query to get the desired information as instructed in CQL.

You can change the visualize mode by turning on the experimental visualization to get a more clear UI about the Nodes and Edges, as illustrated below.
![image](https://github.com/ddlinh/gena-db/assets/60208884/443f6bd2-9c67-4beb-aff4-21ba2529abcf)



## How to access to Gena Knowledge Graph from Application?
* **Python User**: https://neo4j.com/docs/aura/auradb/connecting-applications/python/
* **JavaScript User**: https://neo4j.com/docs/aura/auradb/connecting-applications/javascript/
* **Java User**: https://neo4j.com/docs/aura/auradb/connecting-applications/java/
* **Spring Boot User**: https://neo4j.com/docs/aura/auradb/connecting-applications/spring-boot/
* **.NET User**: https://neo4j.com/docs/aura/auradb/connecting-applications/dotnet/
* **GO User**: https://neo4j.com/docs/aura/auradb/connecting-applications/go/

## How to construct a GENA Database in AuraDB?

Let's move to the folder ./gena_data, there are 2 files which are:
* **gena_data_final.zip**: a zip file contains **gena_data_final.csv**, which includes all nodes and edges of GENA DB. Apart from building knowledge graph, you can use this file for any specific purpose.
* **GENA_KN.ipynb**: a jupyter notebook which includes codes to connect AuraDB via an identification (_uri_, _username_ and _password_), as well as to create nodes and edges from **gena_data_final.csv**
