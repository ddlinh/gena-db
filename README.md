# Gena User Guide

## How to access to Gena Knowledge Graph on UI?
1. Access to [AuraDB Connection](https://workspace-preview.neo4j.io/terms-and-conditions) and click Accept on Terms & Condition.
![image](https://github.com/ddlinh/gena-db/assets/60208884/1f12afd7-b5a0-4bee-92a4-7f98e3bb7377)

2. Click the **Connection** dropdown, and choose the **Connect** option.
![image](https://github.com/ddlinh/gena-db/assets/60208884/d2efe4a3-42fb-4229-a448-931cd232c58f)

3. Enter:
    * uri: neo4j+s://e5c905b4.databases.neo4j.io
    * username: public_user
    * password: password_public_user
![image](https://github.com/ddlinh/gena-db/assets/60208884/3347a00f-5b93-49aa-aaa4-629cd2ae83ee)

4. Make your first query with [CQL](https://neo4j.com/developer/cypher/).
   * For example: "MATCH (n1:NUTRITION)-[r]->(n2:MENTAL_HEALTH) RETURN n1, r, n2 LIMIT 10")
   ![image](https://github.com/ddlinh/gena-db/assets/60208884/cd9f33fe-6cdf-47da-851f-f09c9d435c09)

This query aims to extract the 10 directed relations from Nutrition to Mental Health. You can easily custom the query to get the desired information as instructed in CQL.


## How to access to Gena Knowledge Graph from Application?
* **Python User**: https://neo4j.com/docs/aura/auradb/connecting-applications/python/
* **JavaScript User**: https://neo4j.com/docs/aura/auradb/connecting-applications/javascript/
* **Java User**: https://neo4j.com/docs/aura/auradb/connecting-applications/java/
* **Spring Boot User**: https://neo4j.com/docs/aura/auradb/connecting-applications/spring-boot/
* **.NET User**: https://neo4j.com/docs/aura/auradb/connecting-applications/dotnet/
* **GO User**: https://neo4j.com/docs/aura/auradb/connecting-applications/go/
