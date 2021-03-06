<p align="center"><img src="PytextLogo.PNG"\></p>

# Pytext : Text Generator
- Pytext is a program that allows you to generate texts (poems) using a deep learning model.
- The poem dataset is from : https://www.kaggle.com/michaelarman/poemsdataset

# Requirement

- You will need to install the following libraries :
  - tensorflow/keras
  - numpy
  - pandas
  - The other libraries should be installed thanks to these 3

# How it works (simplify)

- The user must choose among the available themes.
- The program will search for texts of the chosen theme.
- The program will clean the texts by removing special characters.
- The program reduces all capital letters and replaces all '\n' with ''.
- The program will tokenize the texts.
- The program will delimit the sequences, and create n_gram sequences. 
  - e.g. [ Hello, how, are, you, ...] --> [0,2,3,1,...]
  - [ Hello, how, are, you, ...] --> [0,2],[2,3],[3,1],...

<p align="center"><img src="n_gram.PNG"\></p>

- The program will search for the longest sequence, and then convert each sequence to an array.
- The program will create a set X and a set labels for training. (X contains all the words in a sequence except the last one, and Labels contains the last word).
- The program will categorise Labels for use.
- The program will train the model if you have never trained the model with the chosen theme.
- The user writes the first words of the text that will be generated using the model prediction.
- N words will be generated (N can be changed in the code (variable 'next_words')).
- At the end of the prediction, the program displays and saves the text in a text file with the name of the theme (if the text file already exists, the generated text is replaced by the new one).

# Example of generated text

<p align="center"><img src="output.PNG"\></p>
