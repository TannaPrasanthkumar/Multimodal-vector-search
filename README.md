# Multimodal Movie Search with Weaviate

This project demonstrates how to build a multimodal search application using Weaviate as a vector database and open-source models from the `transformers` library for generating text and image embeddings. The application allows for searching movie data based on both text descriptions and movie posters.

## Project Explanation

The project utilizes Weaviate to store movie data and their corresponding vector representations (embeddings). Text embeddings are generated from movie titles and overviews using a Sentence Transformer model, while image embeddings are generated from movie posters using a Vision Transformer (ViT) model. By storing these embeddings in Weaviate, we can perform semantic search queries using either text or image inputs to find similar movies.

The notebook walks through the process of:

1.  Setting up a Weaviate collection with `none` vectorizers for both text and image vector spaces.
2.  Loading pre-trained text and image embedding models from the `transformers` library.
3.  Generating text and image embeddings for a dataset of movie information and posters.
4.  Importing the movie data and their embeddings into the Weaviate collection using batch import.
5.  Performing vector searches using both text and image queries.

## Use Cases

This type of multimodal search has various applications, including:

*   **Enhanced Movie Discovery:** Users can find movies not just by keywords but also by providing an image similar to the movie poster they are looking for.
*   **Content-Based Recommendation Systems:** Recommend movies with similar themes, styles, or visual aesthetics based on the embeddings.
*   **Duplicate Detection:** Identify movies with similar titles, overviews, or posters.
*   **Improving Search Relevance:** Combine text and image search results for more accurate and contextually relevant search outcomes.

## How to Run

1.  **Open in Google Colab:** Click the "Open in Colab" badge (if you add one) or upload the `.ipynb` notebook file to Google Colab.
2.  **Install Dependencies:** Run the first code cell (`%pip install ...`) to install the necessary libraries.
3.  **Connect to Weaviate:** Run the code cell to connect to Weaviate Embedded.
4.  **Load Data:** Run the cells to load the movie data from the JSON file.
5.  **Modify Weaviate Schema:** Run the cell to delete and recreate the Weaviate collection with the updated schema.
6.  **Load Embedding Models:** Run the cells to load the text and image embedding models.
7.  **Generate Embeddings:** Run the cells to generate text and image embeddings for the movie data.
8.  **Import Data:** Run the cell to import the data and embeddings into Weaviate.
9.  **Perform Searches:** Run the cells under the "Update the query" or "Text-search through the posters vector space" sections to perform vector searches using text or image queries.

**Note:** Ensure you have the `movies_data.json` file and the `poster` directory with movie poster images available in your Colab environment as referenced in the notebook.

---
