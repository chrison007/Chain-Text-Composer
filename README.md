# Text Generation using Graph Model

## Overview

This project implements a basic text generation model using a graph-based approach, specifically a Markov Chain-like model. The code defines two classes, `Vertex` and `Graph`, representing words and their relationships in a text. The model uses the statistical relationships between words to generate new sequences of words.

## Classes

### 1. Vertex Class

- Represents a word in the text.
- Keeps track of adjacent words and their transition probabilities.
- Methods include adding edges, incrementing edge weights, getting adjacent nodes, generating a probability map for the next word, and selecting the next word.

### 2. Graph Class

- Represents the entire text as a graph of words.
- Manages a dictionary of vertices (words) and their relationships.
- Provides methods for adding vertices, retrieving vertices, getting the next word based on probabilities, and generating probability mappings for all vertices.

## Usage

1. **Creating a Graph:**
   ```python
   # Creating a graph
   graph = Graph()

2. # Adding vertices
  graph.add_vertex("apple")
  graph.add_vertex("banana")

3.# Adding edges between vertices
  vertex_apple = graph.get_vertex("apple")
  vertex_banana = graph.get_vertex("banana")
  vertex_apple.add_edge_to(vertex_banana, weight=2)

4. # Generating probability mappings
  graph.generate_probability_mappings()

# Getting the next word for a given vertex
  next_word = graph.get_next_word(vertex_apple)



