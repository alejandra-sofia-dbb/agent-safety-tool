Agent Safety Tool
Agent Safety Tool is an AI-driven system designed to evaluate the safety of actions performed by agents. It combines ontology-based reasoning, natural language processing, and a real-time risk assessment framework to ensure agents act safely and ethically.

Overview
This project integrates GPT-2 for natural language interpretation and an ontology server to dynamically update and assess risk levels. The core focus is to provide a framework where agents can assess potential risks of actions in real-time and update their ontology 
with new knowledge. The system is visualized using Neo4j, making it easier to track agent behavior, capabilities, and vulnerabilities.

Features
Natural Language Processing: Uses GPT-2 (a transformer model) to interpret user inputs.
Ontology-based Risk Assessment: Updates and queries an OWL ontology to assess risk levels for agent actions.
Neo4j Integration: Visualizes the relationships and hierarchies within the ontology.
Dynamic Updates: Continuously learns and updates the ontology based on new agent interactions and actions.
Key Components
1. AI Agent (src/ai_agent.py)
Interprets user actions using GPT-2 and generates structured responses.
Sends risk assessment requests to the ontology server.
2. Ontology Server (src/ontology_server.py)
Manages the OWL ontology, storing agent types, capabilities, tools, and associated risks.
Processes update requests and performs real-time risk evaluations.
3. Neo4j Integration (src/neo4j_integration.py)
Integrates Neo4j for visualizing the ontology structure and agent decision-making processes.
4. Ontology Data (data/agent-ontology.owx)
A dynamic, continuously evolving ontology representing agents, capabilities, tools, and risk levels.
5. Visualization (visualization/ontology_visualization.html)
Renders the ontology as an interactive graph using Neo4j and PyVis for easy exploration of agent behaviors.
Installation
To run this project locally:

Clone the repository:

bash
Copy code
git clone https://github.com/alejandra-sofia-dbb/agent-safety-tool.git
cd agent-safety-tool
Create a virtual environment:

bash
Copy code
python3 -m venv env
source env/bin/activate
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Run the ontology server:

bash
Copy code
cd src
python ontology_server.py
Test the AI agent by providing an action:

bash
Copy code
python ai_agent.py
Dependencies
Make sure the following dependencies are installed:

Flask: for running the ontology server.
Owlready2: for managing the OWL ontology.
Neo4j Python Driver: for integrating with Neo4j.
Transformers (Huggingface): for GPT-2 language model.
Install all dependencies using:

bash
Copy code
pip install -r requirements.txt
Project Structure
bash
Copy code
/src
   ai_agent.py               # AI agent for interpreting user actions
   ontology_server.py        # Ontology server for risk assessment
   neo4j_integration.py       # Integrates Neo4j for ontology visualization
/data
   agent-ontology.owx        # OWL-based ontology of agents, actions, and risks
/visualization
   ontology_visualization.html # HTML visualization of ontology (using PyVis)
/docs
   README.md                 # Project documentation
requirements.txt             # Python dependencies
Future Work
Model Improvement: Use more powerful models like GPT-3 for better natural language understanding.
Ontology Expansion: Enhance the ontology to handle more complex agent behaviors, including ethical decision-making and real-time data from sensors.
Real-time Monitoring: Integrate real-time data sources (e.g., system logs) to continuously monitor agent safety.


