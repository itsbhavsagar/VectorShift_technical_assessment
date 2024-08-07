# VectorShift Frontend Technical Assessment

## Introduction

Thank you for participating in the VectorShift frontend technical assessment! This README provides instructions for completing the assessment, which involves working with both frontend and backend components. You’ll be using JavaScript/React for the frontend and Python/FastAPI for the backend.

## Project Structure

- **Frontend**: Located in the `/frontend` directory.
  - Source files: `/frontend/src`
- **Backend**: Located in the `/backend` directory.
  - Source files: `/backend`

## Setup Instructions

### Frontend

1. Navigate to the `/frontend` directory:
   ```bash
   cd /frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the frontend server:
   ```bash
   npm start
   ```

### Backend

1. Navigate to the `/backend` directory:
   ```bash
   cd /backend
   ```
2. Start the backend server:
   ```bash
   uvicorn main:app --reload
   ```

## Assessment Parts

### Part 1: Node Abstraction

- **Objective**: Create an abstraction for node types (inputs, outputs, LLMs, text) to simplify creation and styling of new nodes.
- **Instructions**:
  - In `/frontend/src/nodes`, you will find JavaScript files for different node types.
  - Implement a new abstraction to manage these nodes efficiently.
  - Create five new nodes to demonstrate the effectiveness of your abstraction.

### Part 2: Styling

- **Objective**: Apply styling to the frontend components to create an appealing and unified design.
- **Instructions**:
  - Style various components as per your design vision.
  - You may use existing styles from VectorShift or create your own from scratch.
  - Feel free to use any React packages or libraries for styling.

### Part 3: Text Node Logic

- **Objective**: Enhance the functionality of the Text node to improve text input handling and variable definition.
- **Instructions**:
  - Modify the Text node in `/frontend/src/nodes` to adjust its size dynamically based on text input.
  - Implement variable definition within the text input using double curly brackets (e.g., `{{ input }}`), creating a corresponding Handle.

### Part 4: Backend Integration

- **Objective**: Integrate the frontend with the Python/FastAPI backend.
- **Instructions**:
  - Update `/frontend/src/submit.js` to send node and edge data to the `/pipelines/parse` endpoint.
  - Modify the `/pipelines/parse` endpoint in `/backend/main.py` to calculate the number of nodes and edges and determine if the pipeline forms a Directed Acyclic Graph (DAG).
  - Ensure the frontend displays an alert with the results from the backend (number of nodes, edges, and DAG status).
