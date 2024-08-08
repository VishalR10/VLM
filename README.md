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
