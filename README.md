# Book Recommender with LLMs 

This project is a semantic book recommender built using concepts from FreeCodeCamp's LLM course. 
Instead of relying on traditional keyword-based matching, this recommender system leverages natural language processing (NLP) and semantic similarity to suggest books based on their content, themes, and user preferences.

How It Works
* Uses large language models (LLMs) to analyze and compare book descriptions.
* Employs embedding models to convert text into numerical representations for similarity comparison.
* Suggests books based on semantic closeness rather than simple metadata matching.
* This approach allows for more accurate and meaningful recommendations, making it ideal for book lovers looking for their next great read based on thematic and contextual relevance.

There are five components:
* Text data cleaning (code in the notebook `data-exploration.ipynb`)
* Semantic (vector) search and how to build a vector database (code in the notebook `vector-search.ipynb`). This allows users to find the most similar books to a natural language query (e.g., "a book about a person seeking revenge").
* Doing text classification using zero-shot classification in LLMs (code in the notebook `text-classification.ipynb`). This allows us to classify the books as "fiction" or "non-fiction", creating a facet that users can filter the books on. 
* Doing sentiment analysis using LLMs and extracting the emotions from text (code in the notebook `sentiment-analysis.ipynb`). This will allow users to sort books by their tone, such as how suspenseful, joyful or sad the books are.
* Creating a web application using Gradio for users to get book recommendations (code in the file `gradio-dashboard.py`).

This project was initially created in Python 3.11. In order to run the project, the following dependencies are required:
* [kagglehub](https://pypi.org/project/kagglehub/)
* [pandas](https://pypi.org/project/pandas/)
* [matplotlib](https://pypi.org/project/matplotlib/)
* [seaborn](https://pypi.org/project/seaborn/)
* [python-dotenv](https://pypi.org/project/python-dotenv/)
* [langchain-community](https://pypi.org/project/langchain-community/)
* [langchain-opencv](https://pypi.org/project/langchain-opencv/)
* [langchain-chroma](https://pypi.org/project/langchain-chroma/)
* [transformers](https://pypi.org/project/transformers/)
* [gradio](https://pypi.org/project/gradio/)
* [notebook](https://pypi.org/project/notebook/)
* [ipywidgets](https://pypi.org/project/ipywidgets/)

A requirements.txt file containing all the project dependencies is provided in requirements.txt

In order to create your vector database, you'll need to create a .env file in your root directory containing your OpenAI API Key/Hugging Face API Key. 
I have used both Open AI and Hugging Face models in text classification.  
The Final Gradio Dashboard uses hugging face model to recommend books.