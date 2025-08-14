# Personal Finance Transaction Categorization with AI

An intelligent transaction categorization system that combines vector embeddings, semantic search, and generative AI to automatically label and organize banking transactions for budgeting and financial analysis.

## 🎯 Overview

This project demonstrates a complete AI-powered pipeline that processes raw bank statements (CSV/PDF) and automatically categorizes transactions using:

- **Retrieval-Augmented Generation (RAG)** with ChromaDB vector store
- **Semantic embeddings** via Sentence Transformers (SBERT)
- **LLM fallback** with Google Gemini for edge cases
- **Function calling** for structured JSON outputs

## 🚀 Key Features

- **Multi-format ingestion**: Processes both CSV exports and PDF bank statements
- **Smart categorization**: Uses historical transaction patterns to classify new entries
- **Confidence-based fallback**: Automatically escalates uncertain cases to LLM review
- **Explainable AI**: Provides clear rationales for every categorization decision
- **Tax category mapping**: Assigns tax-relevant labels for financial reporting
- **High accuracy**: Achieves 90%+ auto-categorization coverage

## 🛠 Tech Stack

- **Python 3.10+** with pandas, scikit-learn
- **ChromaDB** for vector storage and similarity search
- **Sentence Transformers** (all-mpnet-base-v2) for embeddings
- **Google Gemini API** for generative AI fallback
- **PyPDF** for PDF statement parsing
- **Jupyter Notebook** for interactive development

## 📋 Prerequisites

- Python 3.10 or higher
- Google Gemini API key
- Jupyter Notebook or JupyterLab

## 🔧 Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/Personal-Finance-Transaction-Categorization-with-AI.git
cd Personal-Finance-Transaction-Categorization-with-AI
```

2. Install required packages:
```bash
pip install google-genai==1.7.0 chromadb sentence-transformers pypdf pandas numpy matplotlib tqdm
```

3. Set up your Google Gemini API key:
   - Get an API key from [Google AI Studio](https://makersuite.google.com/app/apikey)
   - Add it to your environment or notebook secrets

## 📊 Usage

1. **Prepare your data**: 
   - Export your bank transactions as CSV
   - Or use PDF bank statements

2. **Run the notebook**:
   - Open `budget-financial-advisory-category-assistant.ipynb`
   - Update file paths to point to your data
   - Execute cells sequentially

3. **Review results**:
   - Check auto-categorized transactions
   - Review any "UNKNOWN" cases
   - Export final categorized dataset

## 🔄 How It Works

1. **Data Ingestion**: Parses CSV/PDF bank statements into structured format
2. **Embedding Creation**: Converts transaction descriptions to vector embeddings
3. **Vector Storage**: Indexes embeddings in ChromaDB for similarity search
4. **RAG Classification**: Uses nearest neighbor lookup for categorization
5. **LLM Fallback**: Escalates uncertain cases to Gemini for analysis
6. **Structured Output**: Returns categories with explanations in JSON format

## 💡 GenAI Capabilities Demonstrated

- **Document Understanding**: CSV/PDF parsing and text extraction
- **Vector Embeddings**: Semantic representation of transaction descriptions
- **Vector Search**: Similarity-based retrieval from historical data
- **Retrieval-Augmented Generation**: Combining search with generative AI
- **Function Calling**: Structured API interactions with LLMs
- **Few-shot Prompting**: Learning from examples
- **Context Caching**: Optimizing API calls
- **Explainable AI**: Providing rationales for decisions

## 📈 Results

- **Coverage**: 90%+ transactions automatically categorized
- **Accuracy**: High precision on common transaction types
- **Transparency**: Every decision includes a clear rationale
- **Efficiency**: Processes hundreds of transactions in minutes

## 🎯 Use Cases

- Personal expense tracking and budgeting
- Tax preparation and financial reporting
- Business transaction analysis
- Financial advisory automation
- Expense categorization for accounting systems

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Google Gemini API for generative AI capabilities
- ChromaDB for vector storage
- Sentence Transformers for embeddings
- The open-source community for excellent tools and libraries

---

**Note**: This project is for educational and personal use. Always ensure compliance with your bank's terms of service when processing financial data.
