# SLI Classification Project
## Team Members
Jack Runge (joru2460@colorado.edu)  
Joon Kim (seki2928@colorado.edu)  
Josh Daniels (joda4370@colorado.edu)
## Description
This project is used to classify SLI in TalkBank corpus
## Usage
There are two part of the project.
### Morpheme Segmentation
Use Google Colab to run Seq2Seq_Morpheme.ipynb  
It needs MorphoLEX_en_shuffle.tsv and All_Data_without_sp.txt to run.  
After execution, download All_Data_morphemes.txt to further process.  
  
You can change hyperparameters by chaning values in below.
```
batch_size = 64  # Batch size for training.
epochs = 50  # Number of epochs to train for.
latent_dim = 512  # Latent dimensionality of the encoding space.
```
### SLI Classification
It likes typical BERT classification.  
  
sli_baseline.py is a baseline program.  
It needs vocab.txt and All_Data_without_sp.txt  
  
sli_morpheme.py is a morpheme based program.  
It needs vocab.txt and All_Data_morphemes.txt  
  
Both you can change hyperparameters by chaning values in below.  
```
BATCH_SIZE = 32
LEARNING_RATE = 2e-5
NUM_TRAIN_EPOCHS = 2
```
