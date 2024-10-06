# Dynamic Risk Assessment in Autonomous Agents Using Ontologies and AI

In this project I looked to implement dynamic safety checks for AI agents using ontology-based reasoning. The tool ensures that AI agents interact safely by performing real-time risk assessments based on their actions and continuously updating an ontology that represents agent capabilities, tools, and associated risks. The approach was inspired by the vast research emerging that looks at the opportunities in unifying symbolic reasoning approaches and LLMs, especially the paper "Unifying Large Language Models and Knowledge Graphs: A Roadmap" by Pan, Luo 2023. The interpretability innate to knowledge graphs and ontology based systems provided an opportunity to create a meaningful security layer for an AI agent.

## Project Overview

This project focuses on ensuring the safety of AI agents by dynamically assessing risk levels associated with their actions. Using a combination of natural language processing and symbolic reasoning through ontologies, this project builds a safety framework that allows agents to be flexible while adhering to strict security protocols. The system leverages real-time ontology updates and a visual representation of the agent's decision-making process for enhanced interpretability.

### Key Components
1. **AI Agent (`ai_agent.py`)**: Uses a GPT-2 model to interpret user inputs and generate structured actions.
2. **Ontology Server (`ontology_server.py`)**: Manages and updates the ontology, assesses risk levels, and provides an API for interaction with the AI agent.
3. **Neo4j Integration (`neo4j_integration.py`)**: Provides integration with Neo4j to visualize the evolving ontology structure and relationships.
4. **Ontology (`agent-ontology.owx`)**: An OWL-based ontology representing agent types, capabilities, tools, and risk levels.
5. **Ontology Visualization (`ontology_visualization.html`)**: Allows for easy visualization of the ontology structure using the Neo4j data.

## Features

- **Dynamic Ontology Updates**: The ontology is continuously updated based on interactions, ensuring the system adapts to new scenarios.
- **Safety Checks**: The AI agent performs safety checks on actions, determining if they are high-risk, based on predefined risk keywords and the ontology.
- **Ontology Visualization**: Integration with Neo4j enables easy visualization of the ontology's structure and relationships.

## Technologies Used

- **Transformers (GPT-2)**: Handles natural language processing and action interpretation.
- **Flask**: Provides the RESTful API for the ontology server.
- **Owlready2**: Used for managing and querying the OWL-based ontology.
- **Neo4j**: Visualizes the ontology and its relationships.
  
## Project Structure

- `ai_agent.py`: Main script for the AI agent that handles user interaction and ontology communication.
- `ontology_server.py`: Manages the ontology and risk assessments.
- `neo4j_integration.py`: Integrates the ontology with Neo4j for visualization purposes.
- `agent-ontology.owx`: The OWL-based ontology that represents agents, capabilities, tools, and risks.
- `ontology_visualization.html`: HTML file to visualize the ontology.

## Contributing

Feel free to submit a pull request if you'd like to contribute. Please ensure your changes align with the project's goals of improving AI agent safety.
