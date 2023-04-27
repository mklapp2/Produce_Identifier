# Produce_Identifier
This project allows for the training and use of a machine learning model to identify fruits and vegetables in images.

#User Guide

##Setup/Installation Steps:
1.	Clone the Produce Identifier repo to the desired install location. Note the location of this directory, which will be referred to as the Produce_Identifier directory.
2.	Install miniconda or Anaconda if one of these is not already installed.
a.	Download an appropriate installer here: https://docs.conda.io/en/latest/miniconda.html#latest-miniconda-installer-links
b.	Open the folder containing the downloaded installer and launch the installer by double clicking.
c.	Follow the prompts to complete the installation of miniconda.
3.	Open an anaconda prompt and navigate to the directory that the Produce Identifier repo was cloned to (the Produce Identifier directory from step 1).
4.	Enter the following command: conda env update --name produce_identifier_env --file environment.yml --prune
5.	Wait for the project dependencies to install.
6.	Congratulations, the product can now be run!

##Running the Product:
1.	Navigate to the Produce_Identifier directory. Open the User-Submissions directory found within. Add any user input photos of produce to identify into this folder. Note: Only produce types found in the training data set can be identified.
2.	Open an anaconda prompt and navigate to the Produce_Identifier directory.
3.	Run the following command: conda activate produce_identifier_env
4.	Run the command: jupyter notebook
5.	In the browser window, double click the Produce_Identifier.ipynb file to launch the application.
6.	In the menu, click the Kernel dropdown and select “Restart & Run All”.
7.	Scroll down and view the Training Image Counts visual to confirm that training images were found (and that the labels were parsed appropriately).
8.	Scroll down to the Confusion Matrix visual to confirm that the model appears to perform well on the test data.
9.	Scroll down to the User Supplied Data at the bottom of the application interface.
10.	Go to the “Selected user file” drop-down and select the image file you wish for the model to identify. The application will display the image, predicted label, predicted label confidence, and a graph of the top five predicted labels and their confidence levels.

##Optional Actions:
Selecting a different trained model:
1.	Scroll to the ‘Settings’ cell output.
2.	Click the ‘Selected saved model’ dropdown and select the desired model. Note that the models are automatically named based on the time at which they were created. 
3.	Click on the ‘Data Preparation’ cell (below Settings).
4.	In the menu at the top, click the Cell dropdown and then select “Run All Below”. This will run the predictions using the selected model.
Training a Model:
1.	Scroll to the ‘Settings’ cell output.
2.	Uncheck the ‘Load pre-trained model’ option; this will force the training of a new model.
3.	Use the ‘Number of Epochs’ slider to select a maximum number of training epochs.
4.	Click on the ‘Data Preparation’ cell (below Settings).
5.	In the menu at the top, click the Cell dropdown and then select “Run All Below”. This will train a model using the data in the Training and Validation folders (inside Produce_Identifier). The names of each folder in Training and Validation will serve as the accepted labels for the model. The folders in each must be made to match and have proper images in jpeg format.



Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg
