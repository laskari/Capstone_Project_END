# Capstone_Project_END

In this Project, I am implementing a transformer model to generate the Python source code for the given Natural Language Statement

The project mainly having the following components:
  1. The Dataset
  2. Data Pre-processing
  3. Embedding Creation
  4. Squence to Sequence Model Building
  5. Training 
  6. Inference
  
  
** Dataset:**
 
The dataset provided by The School of AI Admin, consists of 4600+ samples of data with Program description starting with # and followed by the coding snippet.
 
** Data Pre-processing: **

The important step in building the complete solution for generating the python source code is pre-processing the given dataset.
The dataset has Program Description consisting of numbers, special symbols and extra spaces. 
The Program code also having comment lines for some parts of the code, which is causing ambiguious when splitting the data with Special character '#', so the comment lines across all the programs are removed to resolve the ambiguity.

Program text and Program code has some additional new lines and empty lines in between, removing them also considered in pre-processing step.

** Embedding Creation: **

