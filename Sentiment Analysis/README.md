<div align="center">

# Text Sentiment Analysis using Caikit and Hugging Face

This project implements text sentiment analysis using Caikit and Hugging Face. This allows users to perform sentiment analysis on text samples and provides insight into the emotional tone of the content (positive or negative).

============================================================================================
</div>

## Analisis Pribadi

Pengaturan proyek ini dibuat untuk tingkat modularitas dan fleksibilitas yang tinggi dengan Caikit serta model Hugging Face, memisahkan setiap elemen agar dapat dengan mudah dirawat dan diintegrasikan. Modul `HuggingFaceSentimentModule` memungkinkan pemanfaatan dan penyimpanan model dengan baik, mendukung kebutuhan dinamis aplikasi di lingkungan produksi. Pengelolaan dependensi dengan menggunakan `virtualenv` dan `requirements.txt` memastikan konsistensi dalam proyek, sedangkan penerapan Caikit menyediakan kerangka kerja yang mempermudah pembuatan dan pengembangan pipeline AI. Proyek ini siap untuk diperluas melalui integrasi API dan otomatisasi proses, menawarkan dasar yang kokoh untuk aplikasi AI berbasis analisis sentimen di masa mendatang. 

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
   Note: The text_sentiment package name must use an underscore ( _ ), not a dash (-) for importing packages.

 3. Step 2: Create the data model specification
    
    * Run the following commands to create a data_model directory to store the data model:
    ``` bash
    mkdir data_model
    cd data_model
    ```
    Note: The Caikit runtime default data model specification package name is data_model in the root package directory.

    * In the data_model directory, create a **classification.py**

    * Make the classes visible in the project by creating an **init.py** file
 
4. Step 3: Create the model wrapper

   * Run the following commands to create a directory for the metadata that identifies the class.
     ``` bash
     cd /home/project/text-sentiment
      mkdir -p models/text_sentiment
      cd models/text_sentiment
     ```
     Note: The Caikit runtime default directory for model metatdata is models under the project root directory.

   * Create a **config.yml** file
   * Create a directory for the modle/wrapper class:
     ``` bash
     cd /home/project/text-sentiment/text_sentiment
     mkdir runtime_model
     cd runtime_model
     ```
   * Create an **hf_module.py** file
   * Make the class visible in the project by creating an **__init__.py** file
   * Provide library-specific configuration to be used by the runtime by creating a **config.yml** file.
     Return to the top-level Python package:
     ``` bash
     cd /home/project/text-sentiment/text_sentiment/
     ```
   * Create a **config.yml** file
   * Configure the library with the configuration file path and make the data_model and runtime_model packages visible by adding them to an **__init__.py** file.
   * Create an **__init__.py** file in the same top-level text_sentiment directory as the config.yml file

5. Step 4: Include the module and package dependencies
   * Go to the project root directory:
     ```bash
     cd /home/project/text-sentiment
     ```
   * Create a **requirements.txt** file and add the following dependencies
     ```bash
     caikit[all]==0.9.2
     
     # Only needed for Hugging Face
     scipy
     torch
     transformers~=4.27.2
     ```
   * Create and activate a virtual environment
     ```bash
     virtualenv -p python3 env
     source env/bin/activate
     ```
   * Install the dependencies by running the following command
     ```bash
     pip install -r requirements.txt
     ```

6. Step 5: Start the Caikit runtime
   * Create **start_runtime.py** file to start the runtime server.
     You must set the correct path to import text_sentiment based on where this **start_runtime.py** file is placed. In the following example, we assume that
     **start_runtime** file is at the same level as the **text_sentiment** package.
   * In one terminal, start the runtime server by running the following command
     ```bash
     python start_runtime.py
     ```

7. Step 6: Test the sentiment analysis
   * Create a **client.py** file
   * Use the Terminal menu item to open a new terminal, activate the virtual environment, and run the client code
     ```bash
     cd /home/project/text-sentiment/
     source env/bin/activate
     python client.py
     ```
   * The client code calls the model and queries it for sentiment analysis on a 2 different pieces of text, **I am not feeling well today!** and **Today is a nice sunny day.**
  
8. Next Steps
   Edit the client.py file and add additional phrases such as My dog is really cute and run the python client.py again to see the output of the sentiment model for the phrases you added.

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
text_sentiment/                           # Main package directory for text sentiment analysis
├── start_runtime.py                      # Starts Caikit runtime as a gRPC server; loads model on startup
├── client.py                             # Client to perform inference on the Caikit runtime
├── requirements.txt                      # Lists library dependencies
├── models/                               # Contains metadata and model artifacts
│   └── config.yml                        # Configuration metadata for the text sentiment model
│
├── caikit_module/                        # Directory for Caikit modules, data model, and runtime model
│   ├── config.yml                        # Main configuration file for module and model I/O
│   ├── __init__.py                       # Makes the module and data_model visible
│   │
│   ├── data_model/                       # Defines data format and attributes for the model
│   │   ├── classification.py             # Data class representing the model’s attributes
│   │   └── __init__.py                   # Initializes the data model package
│   │
│   └── runtime_model/                    # Contains the runtime components for serving the model
│       ├── hf_module.py                  # Class that bootstraps the AI model for training/inference
│       └── __init__.py                   # Initializes the runtime model package
```

## Prerequisites

* Linux/MacOS x86_64 
* Caikit (v0.9.2)
* Python (v3.8+)
* pip (v23.0+)

## Procedure

Complete the following tasks to configure the Caikit runtime and the AI model, and then test them from a client application:
1. Create the project
2. Create the data model specification
3. Create the model wrapper
4. Include the module and package dependencies
5. Start the Caikit runtime
6. Test the sentiment analysis


