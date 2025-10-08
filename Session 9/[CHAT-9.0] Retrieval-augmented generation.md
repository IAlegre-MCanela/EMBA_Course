# [CHAT-9.0] Retrieval-augmented generation

---

## What is retrieval-augmented generation?

**Retrieval-augmented generation** (RAG) is a technique that enhances a text generation model by allowing it to retrieve information from private data. So, the private data supplements the internal training data and data eventually captured by web search, leading to more accurate, relevant, and contextualized responses.

- RAG makes sense when:

    + Your chat app must use private, unplublished data.
    
    + The data have to be extracted from a database.
    
    + The knowledge base containing those data is too big to be included as part of the prompt.

- An alternative approach is **fine-tuning** (*i.e*. re-training) the LLm with your data. 

---

## Retrieval-augmented generation (RAG)

- Pros

    + Up-to-date.

    + Domain specific.

- Cons

    + Performance.

    + Processing.

---

## Fine-tuning

- Pros

    + Deep domain expertise.

    + Faster.

- Cons

    + Training complexity.

    + Computational cost.

    + Maintenance.

    + Catastrophic forgetting.

---

## Steps in RAG

- User prompt: A user submits a question or query to an RAG-powered system. 

- Retrieval: The system uses the user's query to search for external data, often stored in a **vector database**, to find the most relevant information.

- Augmentation: The retrieved external information is combined with the user's original prompt, "augmenting" the prompt with authoritative context. 

- Generation: The augmented prompt is sent to an LLM, which generates a more accurate and specific response. 

- Response: The final response is delivered to the user, often with citations to the external sources used for retrieval. 

---

## What is an embedding?

- An **embedding** is a representation of a piece of information, such as a word, a sentence or an image, as a vector in a space of a given dimension. Typical **embedding dimensions**, for the embedding models that you can manage in your computer, are 384, 512, 768 and 1,024. Nevertheless, the top performing LLMs work with higher embedding dimensions.

- For an embedding to be useful, "similar" pieces of information are represented by vectors that are close in a geometric sense. For instance, in a word embedding, words with similar meanings, such as 'nice' and 'beautiful', will be represented by close vectors. Unrelated words, such as 'computer' and 'dog', will be represented by non-close vectors.

- When we use an ML model to create embedding vectors associated to images or texts, we say that we are "encoding" them. In particular, the LLMs used for that purpose are called **encoders**. The most famous of these encoders is Google's BERT.

---

## Applications of embeddings

- Clustering. 

- Prediction. 

- Recommendation. 

- Outlier detection. 

- Text generation LLMs.

- Semantic search.

- Retrieval-augmented generation.

---

## Vector databases

- After encoding a collection of documentes as vectors, how can we store these vectors in such a way that they can be efficiently retrieved?

- The response (so far) of the industry to this question is the **vector database**:

    + Free databases like **ChromaDB**. 

    + Commercial databases like **Pinecone**. 
    
    + Old databases adapted to vectors, like **PostgreSQL**.
