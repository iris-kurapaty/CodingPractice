# CodingPractice
This repo is to document all the different steps taken in building a light & accurate model within 15 epochs

## Code Structure
.  
|---src  
|&nbsp;&nbsp;&nbsp;|---model.py  
|&nbsp;&nbsp;&nbsp;|---utils.py  
|---Step1.ipynb  
|---Step2.ipynb  
|---Step3.ipynb  
|---Step4.ipynb  
|---Step5.ipynb  
|---Step6.ipynb  
|---Step7.ipynb  
|---Step8.ipynb  

## Steps taken for Model Building
Step 1:
        - Target: 
		○ Getting the setup right
		○ Create util functions for displaying images and other plots
		○ Using basic transformers for the images and loading data
		○ Using a basic model and converting it a modular code 
		○ Creating basic train and test modular functions
	- Results:
		○ 6.3 M parameters
		○ Training Accuracy 99.96%
		○ Test Accuracy is 99.21%
	- Analysis:
		○ Too many parameters and epochs used.
		○ Training is hitting 99.96 and test accuracy reaches 99.21
		○ One strange drop in test accuracy to 98, model must be overfitting & is inconsistent
	- Link: https://github.com/iris-kurapaty/CodingPractice/blob/main/Step1.ipynb

Step 2:
	- Target: 
		○ To get the structure right (use squeeze - expand)
		○ Reduced total convolution layers to 7 and added 2 max pooling layers
		○ Change the no of channels to reduce parameters
	- Results:
		○ 57 K parameters
		○ Training Accuracy 99.56%
		○ Test Accuracy is 99.14%
	- Analysis:
		○ Big drop in number of parameters but still large
		○ Initially doing well but we see some over fitting in the later epochs
	- Link: https://github.com/iris-kurapaty/CodingPractice/blob/main/Step2.ipynb
Step 3:
	- Target: 
		○ To drop to the lightest model
		○ Reduced no of channels in each layer
	- Results:
		○ 5.9 K parameters
		○ Training Accuracy 98.88%
		○ Test Accuracy is 98.74%
	- Analysis:
		○ Parameters have dropped and so has accuracy. However in comparison only 10% of previous model
		○ Over fitting has reduced to a huge extent
		○ Accuracy needs to be pushed for train & test.
	- Link: https://github.com/iris-kurapaty/CodingPractice/blob/main/Step3.ipynb

Step 4:
	- Target: 
		○ Add Batch Normalization in every layer
	- Results:
		○ 6 K parameters
		○ Training Accuracy 99.68%
		○ Test Accuracy is 99.12%
	- Analysis:
		○ We see overfitting in the model with train accuracy rising much higher
		○ Accuracy needs to be converted for test
	- Link: https://github.com/iris-kurapaty/CodingPractice/blob/main/Step4.ipynb
Step 5:
	- Target: 
		○ Add Regularization to make training harder
	- Results:
		○ 6 K parameters
		○ Training Accuracy 98.8%
		○ Test Accuracy is 99.24%
	- Analysis:
		○ Training accuracy but it has helped with test accuracy which is above 99 & consistent.
		○ However test accuracy isnt going beyond 99.24 in 15 epochs.
		○ We can add GAP to see if the model capacity can be pushed.
	- Link: https://github.com/iris-kurapaty/CodingPractice/blob/main/Step5.ipynb
Step 6:
	- Target: 
		○ Add GAP to the last layer
		○ Changed the kernel size of the last convolution layer to adjust for GAP
	- Results:
		○ 5.4 K parameters
		○ Training Accuracy 98.7%
		○ Test Accuracy is 98.7%
	- Analysis:
		○ Not too much overfitting , however accuracy is still low
		○ Try to increase layers to check for increase in accuracy
	- Link: https://github.com/iris-kurapaty/CodingPractice/blob/main/Step6.ipynb
Step 7:
	- Target: 
		○ Adding layers to increase model capacity
		○ Fix the location of max pooling
		○ Change of dropout value to 5%
	- Results:
		○ 5 K parameters
		○ Training Accuracy 98.75%
		○ Test Accuracy is 99.21%
	- Analysis:
		○ Not too much overfitting , however accuracy is still low
		○ Try image augmentation 
	- Link: https://github.com/iris-kurapaty/CodingPractice/blob/main/Step7.ipynb
Step 8:
	- Target: 
		○ Adding image augmentation 
	- Results:
		○ 5 K parameters
		○ Training Accuracy 99.7%
		○ Test Accuracy is 99.2%
	- Analysis:
		○ Not too much overfitting , 
		○ Consistent accuracy of 99.2, however accuracy has not reached desired level
		○ Need to explore other methods of image augmentation
	- Link: https://github.com/iris-kurapaty/CodingPractice/blob/main/Step8.ipynb
![image](https://github.com/iris-kurapaty/CodingPractice/assets/52544352/4f33ab77-75b5-49b0-a85e-922ff22df0c4)
