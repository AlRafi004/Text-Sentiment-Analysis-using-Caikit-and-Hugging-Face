<div align="center">

# Text Sentiment Analysis using Caikit and Hugging Face

This project implements text sentiment analysis using Caikit and Hugging Face. This allows users to perform sentiment analysis on text samples and provides insight into the emotional tone of the content (positive or negative).

<img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54">

✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✦✧✦✧✦✧✦✧✦✧✦✧✦

</div>

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Requirements](#requirements)
- [Explanation Continued](#explanation-continued)

✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✦✧✦✧✦✧✦✧✦✧✦✧✦

## Features

- Sentiment analysis of text inputs.
- Built with the Caikit runtime to manage AI models.
- Utilizes Hugging Face models for advanced natural language processing.
- Easy-to-use client application for querying the model.

✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✦✧✦✧✦✧✦✧✦✧✦✧✦

## Installation

To set up the project locally, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/AlRafi004/Text-Sentiment-Analysis-using-Caikit-and-Hugging-Face.git
   cd Text-Sentiment-Analysis-using-Caikit-and-Hugging-Face

2. Install the required dependencies:
   
   ```bash
   pip install -r requirements.txt

✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✦✧✦✧✦✧✦✧✦✧✦✧✦

## Usage

1. Start the Caikit runtime:

   ```bash
   python start_runtime.py

2. In a new terminal, run the client application to perform sentiment analysis:

   ```bash
   python client.py

3. The client will provide text input, and you can see the sentiment analysis results in the terminal.

✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✦✧✦✧✦✧✦✧✦✧✦✧✦

## Project Structure

```bash
text-sentiment/                        # Top-level package directory
    ├── start_runtime.py               # Wrapper to start the Caikit runtime as a gRPC server
    ├── client.py                      # Client to call the Caikit runtime for inference
    ├── requirements.txt               # Specifies library dependencies
    ├── models/                        # Directory containing Caikit model metadata and artifacts
    │   └── text_sentiment/config.yml  # Metadata defining the Caikit text sentiment model
    └── text_sentiment/                # Directory defining Caikit module(s)
        ├── config.yml                 # Configuration for the module and model input/output
        ├── __init__.py                # Makes the data_model and runtime_model packages visible
        ├── data_model/                # Directory for the Caikit data model
        │   ├── classification.py      # Data class representing AI model attributes
        │   └── __init__.py            # Makes the data model class visible
        └── runtime_model/             # Directory for the Caikit model wrapper
            ├── hf_module.py           # Class to bootstrap the AI model in Caikit
            └── __init__.py            # Makes the module class visible

```

✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✦✧✦✧✦✧✦✧✦✧✦✧✦

## Requirements

* Python 3.7 or higher
* Caikit
* Hugging Face Transformers
* Other dependencies as listed in requirements.txt

✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✦✧✦✧✦✧✦✧✦✧✦✧✦

## Explanation Continued

For further explanation is located in the README.md file inside the Analysis Sentiment file.

✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✧✦✦✧✦✧✦✧✦✧✦✧✦✧✦
