# LLM_Corpus_Search_J8
LLM's and an NLP method are used to extract keywords from a large corpus of documents and than search for the key documents and chunks related to a specific query.

# Package 1 - Processing Pipeline
This package is used to build the database and and used anytime new documents need to be added. The package passes the document through docling to use an OCR package on the documents. It than runs the markdown files through a large API based LLM to extract the meta data. A smaller locally hosted LLM than takes all of the chunks of that document and extracts the keywords. The metadata info and the keywords are stored in a LanceDB
# Package 2 - Query and Identify
This package uses an embedding model to embed the query. The package than uses cosine similarity to rank all chunks after being compared to the query. The average similarity score of all the chunks in a document are found. The top 10 documents are listed as being the most relevant to the query. The package also lists the top 25 chunks related to the query.
