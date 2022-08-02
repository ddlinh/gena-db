# Instructions d'exécution du code source

## Comment exécuter un fiche sous le format .ipynb?
Il existe plusieurs façons d'exécuter un fichier `.ipynb` dont la plus facile est l'installation Anaconda et jupyter notebook (voir https://sparkbyexamples.com/python/install-anaconda-jupyter-notebook/).

Pour assurer les résultats ne sont pas perdus, il faut **copier d'abord un dossier similaire SC_18126023_Construction d'un graphe de connaissances pour la relation entre la nutrition et la santé_Dr.Nguyen Thi Hong Nhung.**

Après avoir installé le Jupyter Notebook et faire une copie, exécuter les fichiers `.ipynb` dans l'ordre Code 0, Code 1, ..., Code 7. Chaque fichier effectue les travaux différents:

1. `Code 0 - food_and_disease_data.ipynb`: collecter les relations disponibles entre maladie et chimie | nutrition.

2. `Code 1 - Entity_Filter.ipynb`: Filtrer et choisir les entités dans les groupes d'entité NUTRITION, MENTAL_HEALTH et BIOCHEMICAL issus des ontologies dans le dossier `DATASET/data/resource_csv`.

3. `Code 2 - Get_and_Clean_Papers.ipynb`: Collecter les abstraits d'articles biomédicaux sur le système PubMed et les nettoyer.

4. `Code 3 - Named_Entities_Recognition.ipynb`: Ajouter au modèle **bc5cdr** de sciSpacy les mots-clés appartenant aux groupes NUTRITION, MENTAL_HEALTH et BIOCHEMICAL de fichier *(2)*. Ensuite, filtrer et choisir les phrase dans les abstraits collectés qui contient les entités appartenant aux groupes d'entité d'intérêt.

5. `Code 4 - Relation Extraction.ipynb`: Utiliser les motifs DT proposés pour extraire les relations entre les entités.

6. `Code 5 - Model_Evaluation.ipynb`: Évaluer la tâche NER et RE par calculer leur précision.

7. `Code 6 - Triple_Construction.ipynb`: **Mapper l'ID unique** pour cette entité, réorganiser les données en 2 parties: **l'information d'entité** et **l'information de relation**.

8. `Code 7 - GENA_KG.ipynb`: Stocker les données organisés dans la base des données **Neo4J** sous la forme d'un graphe.

## Comment interagir avec le graphe de connaissance GENA sur Neo4J?

1. Accéder à Gena DB chez lien **https://browser.neo4j.io/?connectURL=neo4j%2Bs%3A%2F%2Fneo4j%408451226e.databases.neo4j.io%2F**

2. Entrer:
* username: neo4j
* password: RWY0rgJWWysmEbk808JCUv74jF-VrKBEfchJxy1vp5Q

3. Faire la première requête avec CQL.
**For example: "MATCH (n1)-[r]->(n2) RETURN n1, r, n2 LIMIT 20")**

## Mettre à jour chez **https://github.com/ddlinh/gena-db**