# BuzzBot

Generative AI-powered assistant built to deliver accurate, context-aware responses using the University of  Concordia's Knowledge Base. Leveraging a Retrieval-Augmented Generation (RAG) architecture, it combines large language models with a custom document retrieval system.



\# BuzzBot: GenAI Assistant for Concordia



\*\*BuzzBot\*\* is a Generative AI-powered assistant built to deliver accurate, context-aware responses using the University of Concordia's Knowledge Base. Leveraging a Retrieval-Augmented Generation (RAG) architecture, it combines large language models with a custom document retrieval system.



Developed with \*\*LangChain\*\*, \*\*LangGraph\*\*, \*\*FAISS\*\*, and \*\*Streamlit\*\*, BuzzBot provides intelligent, real-time support tailored to Concordia-specific content.



\## 🚀 Features



\* 📚 \*\*Retrieval-Augmented Generation (RAG)\*\*: Combines semantic search with generative AI to ground responses in university documentation.

\* 🔍 \*\*FAISS Vector Store\*\*: Efficient similarity search over preprocessed Concordia knowledge base content.

\* 🏗️ \*\*Modular Architecture\*\*: Scraping, embedding, retrieval, and chat modules organized for independent execution.

\* 💬 \*\*Dual Interface\*\*: Supports both \*\*web-based (Streamlit)\*\* and \*\*terminal-based\*\* chatbot interfaces.

\* 📝 \*\*Custom Prompts\*\*: Designed to prioritize official documentation and gracefully reject unsupported queries.

\* 🔒 \*\*Logging \& Debugging\*\*: Persistent logging for queries, retrievals, and LLM interactions to aid debugging.





\## ⚙️ Configuration



All system settings are managed via \*\*`config/config.yaml`\*\* including:



\* \*\*Paths\*\* for raw data, cleaned data, vector store files

\* \*\*Embedding model\*\* selection (default: `sentence-transformers/all-mpnet-base-v2`)

\* \*\*Vector store type\*\* (FAISS or in-memory)

\* \*\*Search parameters\*\*: default `k`, min relevance score

\* \*\*LLM provider configuration\*\* (Gemini, OpenAI, Ollama)



👉 \*\*To customize behavior\*\*, edit `config/config.yaml` before running the pipeline.







\## 🏃‍♂️ Quick Start



1\. \*\*Clone the repository:\*\*



```bash

git clone https://github.com/hardikgohil73253/buzzbot.git

cd huskybot

```



2\. \*\*Create a virtual environment \& install dependencies:\*\*



```bash

python -m venv venv

source venv/bin/activate  # or venv\\Scripts\\activate on Windows

pip install -r requirements.txt

```



3\. \*\*(Optional) Configure system settings:\*\*



Edit `config/config.yaml` if needed.



4\. \*\*Run scraping (optional if PDFs already downloaded):\*\*



```bash

python src/main.py --scrapedoc

```

⚠️ \*\*Note:\*\* The scraper uses Selenium to extract Concordia Knowledge Base articles. If the website structure or selectors change, the scraper may stop working and require code updates.



5\. \*\*Process PDFs and generate embeddings:\*\*



```bash

python src/main.py --processpdf

```



6\. \*\*Launch chatbot in Streamlit web UI:\*\*



```bash

python src/main.py --runchatbot web

```



Or launch in \*\*terminal mode:\*\*



```bash

python src/main.py --runchatbot terminal

```





\## 📝 Usage Example



\*\*Web interface:\*\*



\* Type your query in the input box (e.g., \*“How do I reset my NetID password?”\*)

\* BuzzBot retrieves relevant documents and responds with an answer based on Concordia’s official knowledge base.



\*\*Terminal interface:\*\*



```bash

$ python src/main.py --runchatbot terminal

>>> How do I connect to campus Wi-Fi?

```





\## 🏛️ Knowledge Base Coverage



Current deployment indexes \*\*674 Concordia Knowledge Base articles\*\* covering:



\* Information Technology

\* Student Academics \& Services

\* Parking \& Transportation

\* Teaching \& Learning Resources

\* HuskyCT



Expandable via re-running scraping and embedding workflows.





\## 🔮 Future Improvements



\* Upgrade to \*\*paid embedding models\*\* for improved accuracy on large datasets

\* Add frontend features like \*\*user login, saved chat history, and feedback forms\*\*

\* Increase the document corpus beyond the current 674 indexed articles





\## 🧑‍💻 Tech Stack



\* \[LangChain](https://www.langchain.com/)

\* \[LangGraph](https://github.com/langchain-ai/langgraph)

\* \[FAISS](https://faiss.ai/)

\* \[Streamlit](https://streamlit.io/)

\* \[Sentence-Transformers](https://www.sbert.net/)

\* Python, Selenium, PyMuPDF, PyYAML





\## 📄 License



This project is licensed under the \[MIT License](https://opensource.org/licenses/MIT).







