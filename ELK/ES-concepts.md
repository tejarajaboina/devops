It will help to search faster at very high scale
Ex: how uber can find find cab,
##Document
    - Data is shared as Documents (JSON files) insted of table in db
##Index
    - Documents of similar traits are grouped into Indexes for quick responce
##Shard
    - Shred is specific to Index and shred will help in processing data, increasing shred size results in aster performance
    - we can maintain replication shreds to maintain high availablility
#CRUD (Create, Read, Update Delete)

###High relavence:
How to measure Relevance?
when you search some thing ES will search  and divides like
    - True Positive  : Most Relavent data (total Match)
    - False Positive : Less Relavent Data (less Match)
    - True Negatives : Most Un-relavent data (no Match at all)
    - False Negatives: less Un-relavent data (may be matched)

- Precision
   it retrived most relavent data 
    ```
                  True Positives
    Precision = ----------------------------------
                  True Positive + False Positives

    ```
- Recall
    gives lot of data event not matched perfectly
 ```
                  True Positives
    Recall = ----------------------------------
                  True Positive + False negative

    ```
precision and Recall are vice versa.

## What is Score?
- score 

##DF : Document Frequence
##IDF : Irrelavent Document Frequency

