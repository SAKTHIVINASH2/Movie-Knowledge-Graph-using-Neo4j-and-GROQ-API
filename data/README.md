# **Movie Knowledge Graph Using Neo4j**
## **Movie Dataset: Key Fields**

The dataset used in this project includes several key fields that are essential for building the knowledge graph. Here’s a detailed breakdown of each field and its role:

### **1. `movieId` (Unique Identifier)**

- **Description**: A unique identifier for each movie in the dataset.
- **Purpose**: This helps distinguish each movie as a unique entity within the graph. By assigning each movie a unique ID, we can establish relationships with other entities like actors, directors, and genres.
- **Example**: `movieId: 101`, `movieId: 102`, `movieId: 103`.

### **2. `title` (Movie Name)**

- **Description**: The name of the movie.
- **Purpose**: The title is one of the most basic and recognizable attributes of a movie. In the knowledge graph, this will be linked to nodes representing the movie, and users will search or query the graph based on the movie's title.
- **Example**: `title: "GoldenEye"`, `title: "Inception"`, `title: "The Matrix"`.

### **3. `released` (Year of Release)**

- **Description**: The year the movie was released.
- **Purpose**: This field gives temporal context to the movie. In the graph, it helps organize movies by their release year and allows users to query for movies released in specific periods.
- **Example**: `released: 1995`, `released: 2010`, `released: 1999`.

### **4. `actors` (Main Actors in the Movie)**

- **Description**: A list of the main actors featured in the movie.
- **Purpose**: The actors' names are stored as attributes and are connected to the movie node. In the graph, actors can be represented as separate nodes linked to the movie, forming an actor-movie relationship.
- **Example**: `actors: ["Pierce Brosnan", "Sean Bean", "Izabella Scorupco"]` for *GoldenEye*.

### **5. `director` (Movie Director)**

- **Description**: The name of the director of the movie.
- **Purpose**: The director’s name is also a key attribute that establishes the **director-movie relationship**. In the graph, this helps identify the individual behind the movie and connect them to the films they have directed.
- **Example**: `director: "Martin Campbell"` for *GoldenEye*.

### **6. `genres` (Categories of the Movie)**

- **Description**: The genre or genres the movie belongs to (e.g., Action, Drama, Comedy).
- **Purpose**: The genre is an important piece of metadata that helps classify movies. In the graph, movies can be linked to one or more genre nodes, creating genre-movie relationships. This is particularly useful for querying movies by genre.
- **Example**: `genres: ["Action", "Adventure", "Thriller"]`.

### **7. `imdbRating` (IMDb Rating)**

- **Description**: The rating of the movie on IMDb, typically ranging from 1 to 10.
- **Purpose**: This numeric field helps evaluate the quality of the movie. It can be connected to the movie node in the graph and allows users to query movies based on ratings, for example, searching for movies with an IMDb rating higher than 8.
- **Example**: `imdbRating: 6.6`, `imdbRating: 8.8`, `imdbRating: 7.2`.

---

## **How the Dataset is Used in Neo4j**

In **Neo4j**, data is represented as **nodes** and **relationships**:

### **Nodes**  
- Represent entities such as **movies**, **actors**, **directors**, and **genres**.

### **Relationships**  
- Define how the entities are related to each other. For example:
  - `MOVIE -> ACTED_IN -> ACTOR`
  - `MOVIE -> DIRECTED_BY -> DIRECTOR`
  - `MOVIE -> BELONGS_TO -> GENRE`

This structure makes it easier to represent complex relationships and enables powerful queries like:
- Who acted in a specific movie?
- What other movies does a particular director have?
- Which actors belong to the "Action" genre?

---
