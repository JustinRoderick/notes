Framework that improves LLMs by retrieving relevant data from sources to provide the LLM with more context to answer questions rather than relying on memory or static training data alone. RAG helps to prevent hallucinations and ensure up to date and accurate information is available to LLMs.

## How it works
- Data from sources is broken into chunks to ensure that they are not too large.
- Those chunks are then converted to vectors using an embedding model.
- Those vectors are stored in a vector database.
- When a user asks an LLM a question it is also converted to a vector using the same embedding model.
- The question vector is then compared to the vectors in the db based on similarity.
- Similar vectors and its chunks of data are then added into the LLMs context to give more accurate responses.

## How does Vector Embedding work
 [Vector Embeddings](https://www.pinecone.io/learn/vector-embeddings/?utm_term=vector%20database&utm_campaign=vector-db-us&utm_source=adwords&utm_medium=ppc&hsa_acc=3111363649&hsa_cam=16569728076&hsa_grp=135276647900&hsa_ad=587750423880&hsa_src=g&hsa_tgt=kwd-1976865318&hsa_kw=vector%20database&hsa_mt=p&hsa_net=adwords&hsa_ver=3&gad_source=1&gad_campaignid=16569728076&gbraid=0AAAAABrtGFDFspNtvGG1Sl72nYYWRO29J&gclid=Cj0KCQiA8KTNBhD_ARIsAOvp6DK9sLzcOblZB3zMf38m_79blWWr_t2O6Lvef0TMrg4mEB3hZMTbdAcaAsALEALw_wcB)
 