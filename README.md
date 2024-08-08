# Nuvolux - A Food Recipe Generator

**Nuvolux** is a personalized cooking companion, powered by the Gemini AI API, that helps you discover new recipes, explore flavors, and cook with confidence. By suggesting recipes based on the ingredients you have, it unleashes your culinary creativity. 

## Features

- **Ingredient-Based Recipe Suggestions:** Suggests recipes using only the ingredients you provide, ensuring no additional items are needed.
- **Detailed Recipe Information:** Each recipe comes with step-by-step instructions, nutritional information, and a brief summary of health benefits.
- **Image Search Integration:** Automatically retrieves a relevant image for each dish from Google Image Search.
- **User-Friendly Interface:** Simple and intuitive design that focuses on user experience.

## Table of Contents

- [Introduction](#introduction)
- [Key Functionalities](#Key-Functionalities)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Docker Setup](#docker-setup)
- [Environment Variables](#environment-variables)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

The Recipe Suggestion API is a Flask-based application that utilizes Google Custom Search and Google Generative AI to provide unique recipe ideas. It supports storing recipes in MongoDB and offers several endpoints for interacting with the stored data.

## Key Functionalities

- **Google API Integration**: Fetch recipes and images using Google APIs.
- **MongoDB Storage**: Store and retrieve recipes with MongoDB.
- **Health Check Endpoint**: Quickly verify the API's operational status.
- **Dockerized Deployment**: Simplify environment setup and scaling with Docker.

## Requirements

Before installing, ensure you have the following dependencies:

- **Python**: Version 3.8 or above
- **Docker**: For containerized deployment
- **MongoDB**: Database for storing recipes
- **Google Cloud Account**: Access to Google APIs

## Installation

### Step 1: Clone the Repository

```bash
git clone https://github.com/yourusername/recipe-suggestion-api.git
cd recipe-suggestion-api
```

### Step 2: Create a Virtual Environment

```bash
python -m venv env
source env/bin/activate  # On Windows use `env\Scripts\activate`
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Set Up Environment Variables

Create a .env file in the root directory based on the env_sample file provided. Fill in your API keys and database information.

```bash
GEMINI_API_KEY=<your-api-key>
MONGO_URI=<mongo-connection-url>
MONGO_DB=<db-name>
SEARCH_ENGINE_ID=<programmable-search-engine-id>
GOOGLE_API_KEY=<google-cloud-console-api>
```

### Step 5: Run the Application

```bash
python main.py
```

## Usage

Once the application is running, you can access the API at `http://127.0.0.1:5000`.

### Example Requests

- **Health Check**:
  ```bash
  curl http://127.0.0.1:5000/health_check
  ```
- **Get Suggested Recipes**:
  ```bash
  curl -X POST "http://127.0.0.1:5000/get_suggested_recipes
  ```
- **Get Recipes from Database**:
  ```bash
  curl -X POST "http://127.0.0.1:5010/get_recipes"
  ```

## API Endpoints

### /health_check
- **Method**:GET
- **Description**:Checks the API's operational status
- **Response**: 200 OK: "API is up and running."

### /get_recipes
- **Method**:GET
- **Description**:Retrieves all stored recipes from the MongoDB database.
- **Response**: 200 OK: JSON array of stored recipes.
