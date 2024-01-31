# Construction-of-Academic-Knowledge-Graph-for-Semantic-Retrieval

### This project aimed to construct a fine-grained academic knowledge graph with a stable hierarchical structure to achieve more precise and intelligent semantic retrieval of academic information.

## ① Data Spider

  Crawled papers from the CNKI (China National Knowledge Infrastructure) in the computer science field from the last five years as experimental data.
  
## ② Pattern Layer Design

### · Ontology Library Construction

  1. Scraped Wikipedia entries **layer by layer** from "https://zh.wikipedia.org/wiki/Category:".
  2. Utilized **depth-first** graph traversal algorithm to address loop-related issues.
  3. Utilized **breadth-first** graph traversal algorithm to address ontology redundancy issues.
  
  (Partial ontology tree display)
   ![image](https://github.com/Jbb-525/Construction-of-Academic-Knowledge-Graph-for-Semantic-Retrieval/assets/88278422/1e80716a-92e6-491e-aecb-b5c0b8680cb7)

### · Entity and Relationship Design

  1. Entity Description
  ![image](https://github.com/Jbb-525/Construction-of-Academic-Knowledge-Graph-for-Semantic-Retrieval/assets/88278422/fdad72c4-4853-4e32-bd84-17810a143db5)
  2. Relation Description
  ![image](https://github.com/Jbb-525/Construction-of-Academic-Knowledge-Graph-for-Semantic-Retrieval/assets/88278422/d32ed55f-bc16-44f3-887b-e1df3b460147)


## ③ Data Layer Construction


![image](https://github.com/Jbb-525/Construction-of-Academic-Knowledge-Graph-for-Semantic-Retrieval/assets/88278422/824e65d5-9173-4dc2-a700-4f6e6db228d6)

## ④ Semantic Retrievel
