# Movie Knowledge Graph using Neo4j and GROQ API

## Introduction
This project showcases how to construct a knowledge graph for a movie dataset using **Neo4j** and **GROQ API**. The dataset includes attributes such as `movieId`, `title`, `release year`, `actors`, `director`, `genres`, and `IMDb rating`. By combining the power of graph databases and GROQ queries, the project allows for advanced semantic queries, providing valuable insights into the movie domain.

---

## Features
- Creation of a movie knowledge graph with interconnected nodes (movies, actors, genres, directors).
- Querying the knowledge graph using Neo4j's Cypher language.
- Integration with GROQ API for data augmentation and enhanced querying.
- Semantic relationships and insights into movie data trends.

---

## Technologies Used
- **Neo4j**: Graph database for storing and querying movie data.
- **GROQ API**: For additional data enrichment and querying capabilities.
- **LangChain**: Framework for intelligent chain-based querying with LLM integration.
- **Python**: For data preprocessing, API integration, and orchestration.

---

## Dataset
The dataset includes the following fields:
- `movieId`: Unique identifier for each movie.
- `title`: Name of the movie.
- `released`: Year of release.
- `actors`: List of main actors.
- `director`: Name of the director.
- `genres`: Categories the movie belongs to.
- `imdbRating`: IMDb rating of the movie.

---

## Setup and Installation
### Prerequisites
1. **Neo4j AuraDB**: Set up a free instance on [Neo4j AuraDB](https://neo4j.com/cloud/aura/).
2. **GROQ API Key**: Obtain an API key from the GROQ platform.
3. **Python 3.8+**: Install Python on your system.

### Installation Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/SAKTHIVINASH2/Movie-Knowledge-Graph-using-Neo4j-and-GROQ-API.git
   cd Movie-Knowledge-Graph-using-Neo4j-and-GROQ-API
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
3. Add your API keys:
  - Update the config.py file with your Neo4j connection details and GROQ API key.
4. Load the dataset into Neo4j:
  - Use Cypher queries or provided scripts to populate the database with movie data.

---

### How to Run
1. Start your Neo4j database instance.
2. Run the Python script:
  ```bash
  python main.py
  ```
3. Query the knowledge graph using:
- The Neo4j Browser.
- Predefined GROQ-powered functions in the script.

---
### Example Query
To find the director of the movie GoldenEye:
```
response = chain.invoke({"query": "Who was the director of the movie GoldenEye"})
print(response)
```

---

### Project Structure
```
├── data/
│   └── link.txt          # Link to movie dataset
|   └── README.md         # dataset documentation
├── src/
│   ├──main.py              # Main script to run the project
|                           # Neo4j graph initialization and utilities
│                           # GROQ API integration functions
├── requirements.txt        # Required Python libraries
├── README.md               # Project documentation
```

--- 

### Result

<img src="result/visualisation (1).png" width="75%"/>

--- 

### Future Enhancements
- Add recommendation system capabilities using graph traversal.
- Visualize the graph for better exploration of relationships.
- Expand the dataset to include additional attributes like box office data or reviews.

---

### License
This project is licensed under the [MIT License](LICENSE).

---

### Contact
For any queries or suggestions, feel free to reach out at sakthivinashb@example.com.
