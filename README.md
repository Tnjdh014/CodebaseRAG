
This repository demonstrates an advanced Retrieval-Augmented Generation (RAG) workflow for querying codebases. The project enables users to understand specific functionalities (e.g., JavaScript parser usage) in a codebase by embedding query and file content, storing them in a Pinecone vector store, and retrieving context for LLM-based responses.

# CODEBASE RAG  

An advanced Retrieval-Augmented Generation (RAG) workflow for querying codebases. This project enables users to ask detailed questions about a codebase (e.g., "How is the JavaScript parser used?") and receive precise, context-aware answers using machine learning and vector storage.  

## Features  
- **Google Colab Integration**: Fully compatible with Google Colab for ease of use.  
- **Repository Cloning**: Clone GitHub repositories directly into the runtime environment.  
- **File Parsing**: Supports popular programming languages like Python, JavaScript, C++, and more.  
- **Embeddings Generation**: Leverages Hugging Face models for semantic embeddings.  
- **Vector Search**: Uses Pinecone for fast and efficient similarity search.  
- **LLM Integration**: Generates detailed answers with Llama 3.1 via the Groq API.

## Setup  

1. Clone this repository or open the Colab notebook directly.  
2. Install the required dependencies by running the following in a Colab cell:  
   ```bash
   !pip install pygithub langchain langchain-community openai tiktoken pinecone-client langchain_pinecone sentence-transformers
   ```  
3. Set up your API keys for Pinecone and Groq/OpenAI:
   - Add them as environment variables in the Colab runtime or use the `userdata.get` method for secure storage.  
4. Run the cells to clone the repository, parse files, and query the codebase.

## Example Usage  

### Querying a Repository  
1. Provide a GitHub repository URL in the notebook:  
   ```python
   repo_url = "https://github.com/username/repo-name"
   path = clone_repository(repo_url)
   ```
2. Query the codebase with a natural language question:  
   ```python
   response = perform_rag("How is the JavaScript parser used?")
   print(response)
   ```  

## Supported Languages  
- Python  
- JavaScript/TypeScript  
- C++  
- Java  
- Go  
- And more...

## Requirements  
- Google Colab (or local runtime with Python 3.7+)  
- Pinecone account and API key  
- OpenAI or Groq API key  

## License  
This project is licensed under the MIT License.  

## Contributions  
Feel free to submit issues or pull requests for improvements.  

---

Copy this template into a `README.md` file, and upload it to your repository for better project visibility.
