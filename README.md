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

### · Data Preparation
  1. Creating an **automated annotation** program on the Doccano platform(【3】Auto-Annotation.ipynb). 
  2. Discerned the current **model’s shortcomings** clearly while efficiently completing the arduous annotation tasks.

### · Named Entity Recognition with BERT+BiLSTM+CRF
  ![image](https://github.com/Jbb-525/Construction-of-Academic-Knowledge-Graph-for-Semantic-Retrieval/assets/88278422/60e6f812-1f62-4149-8e15-95d609862302)
  
### · Analysis of Experimental Results
  ![image](https://github.com/Jbb-525/Construction-of-Academic-Knowledge-Graph-for-Semantic-Retrieval/assets/88278422/16be3c83-7352-4a3e-b441-ebbea3785450)

## ④ Ontology-Entity Connection
  1. Measured semantic similarity by **Cosine similarity**.
  2. According to the hierarchical structure, the ontology with the largest similarity is selected as the **candidate ontology**.
  3. Only the child nodes of the candidate ontology are selected to participate in the calculation.
  4. So on until the candidate ontology has **no lower level nodes**, or if the cosine similarity is **greater than 0.9** it can be stopped directly.

  ![image](https://github.com/Jbb-525/Construction-of-Academic-Knowledge-Graph-for-Semantic-Retrieval/assets/88278422/824e65d5-9173-4dc2-a700-4f6e6db228d6)

## ⑤ Semantic Retrievel
