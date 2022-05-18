### EX NO: 02
### DATE: 04-04-2022
# <p align="center"> BINARY CLASSIFICATION</p>
## AIM:
To write a python program to perform binary classification.

## Equipments Required:
1.Hardware – PCs

2.Anaconda – Python 3.7 Installation / Moodle-Code Runner /Google Colab.

## Theory Concept:
•	Binary classification is the task of classifying the elements of a set into two groups on the basis of a classification rule. 

•	Only two class instances are present in the dataset. 

•	It requires only one classifier model. 

•	Confusion Matrix is easy to derive and understand. 

  Example: Check email is spam or not, predicting gender based on height and weight.

## Libraries Used in the program.
## NUMPY

NumPy is a library for the Python programming language, adding support for large, multidimensional arrays and matrices, along with a large collection of high-level mathematical functions to operate on these arrays. 

## SKLEARN  
Scikit-learn is a free software machine learning library for the Python programming language. It features various classification, regression and clustering algorithms including support-vector machines. 

## MATPLOTLIB  

Matplotlib is a plotting library for the Python programming language and its numerical mathematics extension NumPy. It provides an object-oriented API for embedding plots into applications using generalpurpose GUI toolkits like Tkinter, wxPython, Qt, or GTK. 

## Algorithm: 
1.	Start the program. 
2.	Import libraries required as per requirement. 
3.	Define dataset use the make_ blobs () function to generate a synthetic multi -class classification dataset. 
4.	summarize dataset shape 
5.	summarize observations by class label 
6.	summarize first few examples  
7.	plot the dataset and color the by class label  
8.	stop the program 
 
## Program: 
```
/*
Program to implement binary classification. 
Developed by : U. VIVEK KRISHNA 
Register Number : 212219040180 
*/
```
```
from numpy import where 

from collections import Counter 

from sklearn.datasets import make_blobs 

from matplotlib import pyplot 

X,y=make_blobs(n_samples=10,centers=2,random_state=1)

print(X.shape,y.shape) 

counter=Counter(y) 

print(counter) 

for i in range(5):    
 
 print(X[i],y[i])

for label,_ in counter.items():     
 
 row_ix=where(y==label)[0]     
 
 pyplot.scatter(X[row_ix,0],X[row_ix,1],label=str(label)) 
 
pyplot.legend() 
```
## Output:
 ![image](https://user-images.githubusercontent.com/63917883/166456586-80efdce1-fc1a-4a72-a686-153a0faf7f77.png)

## Result:
Thus the python program performed binary classification successfully.
