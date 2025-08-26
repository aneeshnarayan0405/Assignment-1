# Movie Semantic Search Engine

This project implements an intelligent movie discovery system that enables users to find films based on plot content using natural language queries. The system leverages advanced semantic search techniques to understand query intent and return relevant movies even without exact keyword matches.

## Overview

The semantic search engine is built using cutting-edge natural language processing technologies:
- **SentenceTransformers** with the `all-MiniLM-L6-v2` model for generating high-quality text embeddings
- **Cosine similarity** computation for determining semantic relatedness between search queries and movie descriptions
- **Pandas** for efficient data processing and result presentation

Unlike traditional keyword-based search systems, this engine comprehends the contextual meaning of queries to deliver more accurate and intuitive results.

## Key Capabilities

- **Intelligent Search**: Understands semantic relationships and context in natural language queries
- **Ranked Results**: Provides top-N most relevant movies with confidence scores
- **Robust Testing**: Includes comprehensive test suite ensuring system reliability
- **Well-Documented Code**: Clean implementation with thorough documentation and error handling

## System Requirements

- Python 3.9+
- Git for repository management
- Jupyter Notebook environment

## Installation Guide

1. **Repository Setup**:
   ```bash
   git clone <repository-url>
   cd movie-search-assignment
   ```

2. **Environment Configuration**:
   
   *Windows Users*:
   ```bash
   python -m venv venv
   venv\Scripts\activate
   ```
   
   *macOS/Linux Users*:
   ```bash
   python -m venv venv
   source venv/bin/activate
   ```

3. **Dependency Installation**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Application**:
   ```bash
   jupyter notebook movie_search_solution.ipynb
   ```

## Project Architecture

```
movie-search-assignment/
├── movie_search.py              # Core search functionality module
├── movie_search_solution.ipynb  # Interactive demonstration notebook
├── movies.csv                   # Movie database with titles and plot summaries
├── requirements.txt             # Required Python packages
├── README.md                   # Project documentation
└── tests/
    └── test_movie_search.py    # Automated testing suite
```

## Quality Assurance

Execute the test suite to verify system functionality:

```bash
python -m unittest tests/test_movie_search.py -v
```

The tests validate:
- Proper DataFrame structure and column formatting
- Correct `top_n` parameter handling
- Valid similarity score ranges (0.0 to 1.0)
- Search result relevance and accuracy

## Implementation Examples

### Interactive Notebook Usage
Launch `movie_search_solution.ipynb` to explore the complete implementation with detailed explanations.

### Programmatic Usage
```python
from movie_search import search_movies

# Find movies matching a semantic query
results = search_movies('undercover agent mission in European city', top_n=5)
print(results)
```

### Sample Results
```
                    title                                               plot  similarity
0        Secret Agent 007  An undercover operative infiltrates a crimina...    0.892341
1       Mission: Brussels  A covert mission unfolds in the heart of Euro...    0.734567
2      International Spy  Espionage thriller set across multiple Europe...    0.681923
```

## Technical Implementation

### Search Process
1. **Embedding Generation**: Transform movie plots and user queries into numerical vector representations using pre-trained language models
2. **Similarity Assessment**: Calculate cosine similarity scores between query vectors and movie plot vectors
3. **Result Ranking**: Sort movies by similarity scores and return the most relevant matches

### Model Selection
The `all-MiniLM-L6-v2` model was chosen for its optimal balance of performance and computational efficiency, providing high-quality embeddings suitable for semantic search applications.

## Project Achievements

✅ **Semantic Search Implementation**: Successfully deployed SentenceTransformers-based search system  
✅ **Model Integration**: Properly configured `all-MiniLM-L6-v2` embedding model  
✅ **Interactive Documentation**: Created detailed Jupyter notebook with step-by-step explanations  
✅ **Function Development**: Implemented required `search_movies(query, top_n)` interface  
✅ **Testing Excellence**: Achieved 100% test pass rate (4/4 tests)  
✅ **Code Quality**: Maintained clean, well-commented, professional code structure  
✅ **Comprehensive Documentation**: Provided thorough project documentation and usage guides  

## Academic Context

This project was developed as coursework for the AI Systems Development program at IIIT Naya Raipur, demonstrating practical application of modern NLP techniques in information retrieval systems.