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
Embedding is the process of representing a word or text in vector or number format with specific dimension.

As, the python code consisting on various special characters, generating embedding for each character will improve the model performance, than assigning a random values.

For generating embedding for Python code, gensim with Word2Vec model has be utilized and created a embedding with the same dimension ie 256.

**Squence to Sequence Model Building**

The model built for achieving the desired result with the reference of Attention is all you need, a transformer model by Google in 2017.

The transformer model consists of Encoder and Decoder block with varying number of blocks in each part. Here we experimented with various number of blocks in Encoder and Decoder also. Finally we used Three Encoder blocks and 3 Decode blocks.

Each Enoder block consisting of same architecture as Attention All you need paper with Mutlihead Attention and FUlly Connected Network
Each Decode block also having similar structure with Masked Attention, Mutli-head Attention and fully connected network.

**Training:**
The Complete sequence to Sequence model created and Trained for 50 Epochs.

**Inference**
To check the performance and Validate, the inference part created with a single Natural Language Statement, for which the python source need to be generated. 
