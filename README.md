# Image-Segmentation
Comparing objective functions for segmentation of skin lesions in dermatology images.

## To run the code:
### (a) Acquire the dataset
To download the dataset, go to https://challenge.isic-archive.com/data/ and scroll to the 2018 section and download these files
![image](https://user-images.githubusercontent.com/74062350/208822724-3015a1ec-fdcb-4c06-86b1-4542ebb792d4.png)
for the training data, which is spilt into training and validation set. After downloading the files and extracting it, copy these two folders and paste it into the parent directory of the project inside a new folder “dataset”. Then you can run the project lcoally using jupyter notebook.
For the test set, download these files:
![image](https://user-images.githubusercontent.com/74062350/208822803-e9c87d12-59fc-487e-9c92-4f87e61b7954.png)
which is used as the test set, as the original test set does not have the ground truth published. After extracting the two files, paste them in the parent directory of the project inside a new folder “test_datasets”.
To use in Google Colab, upload the datasets folder into a google drive. The notebook has commented codes to mount it into the Colab environment.
### (b) Install code
Using anaconda is preferred for running the project as it contains most of the libraries except pytorch which must be installed. Google Colab can also be used, in that case just upload the notebooks into Google Colab and uncomment the Gdrive mounting codes to get access to the dataset in drive. 
### (c) Run to reproduce results
Run the train_segmentation notebook to train the model. Set the Experiment_Name variable to the desired name, we used the rule “unet_isic2018_’nameofLossFunction’”.
To test the models, open the test_segmentation notebook. Set the name of the model_path variable as the particular loss function model .pth file you want to test.
Loss function definitions and instance creations are commented within the notebooks.

Finally, special thanks to [Hasib Zunair](https://github.com/hasibzunair) for his generous guidance on this project and his gift with the source code. 
