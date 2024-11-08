<div align="center">

# Text Sentiment Analysis using Caikit and Hugging Face

This project implements text sentiment analysis using Caikit and Hugging Face. This allows users to perform sentiment analysis on text samples and provides insight into the emotional tone of the content (positive or negative).

============================================================================================
</div>

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Requirements](#requirements)
- [License](#license)

## Features

- Sentiment analysis of text inputs.
- Built with the Caikit runtime to manage AI models.
- Utilizes Hugging Face models for advanced natural language processing.
- Easy-to-use client application for querying the model.

## Installation

To set up the project locally, follow these steps:

1. Step 0: Install Caikit runtime
   
   Install virtualenv for our Python requirements
   ``` bash
   pip install --user virtualenv

2. Step 1: Create the project

   Run the following commands create a new project and Python package:
   ``` bash
   mkdir -p /home/project/text-sentiment/text_sentiment
   cd /home/project/text-sentiment/text_sentiment
   ```
   Note: The text_sentiment package name must use an underscore (_), not a dash (-) for importing packages.

 3. Step 2: Create the data model specification
    
    Run the following commands to create a data_model directory to store the data model:
    ``` bash
    mkdir data_model
    cd data_model
    ```
    Note: The Caikit runtime default data model specification package name is data_model in the root package directory.

    In the data_model directory, create a classification.py file by clicking the Open button below and copy the following code in it and save the file:
    ``` bash
    
 
   


## Usage

1. Start the Caikit runtime:

   ```bash
   python start_runtime.py

2. In a new terminal, run the client application to perform sentiment analysis:

   ```bash
   python client.py

3. The client will provide text input, and you can see the sentiment analysis results in the terminal.

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

## Requirements

* Python 3.7 or higher
* Caikit
* Hugging Face Transformers
* Other dependencies as listed in requirements.txt

## License

This project is licensed under the MIT License - see the LICENSE file for details.

### Instructions to Add the README

1. Create a file named `README.md` in the root of your project directory:

   ```bash
   touch README.md

2. Open the README.md file in a text editor and copy-paste the above content into it.

3. Save the file.

4. Finally, commit the changes and push them to your GitHub repository:

   ```bash
   git add README.md
   git commit -m "Add README file for Text Sentiment Analysis project"
   git push
