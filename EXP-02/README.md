### EX NO: 02
### DATE : 01-04-2022
# <P align="center"> BINARY CLASSIFICATION</p>
## AIM:

To write a python program to perform binary classification.

## EQUIPMENTS REQUIRED:

1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner /Google Colab

## RELATED THEORITICAL CONCEPT:

Binary classification is a form of classification — the process of predicting categorical variables — where the output is restricted to two classes.
It is used in many different data science applications, such as Medical Diagnosis, Email analysis, Marketing, etc.
For example, in medical diagnosis, a binary classifier for a specific disease could take in symptoms of a patient and predict whether the patient is healthy or has a disease. The possible outcomes of the diagnosis are positive and negative.

## ALGORITHM:

1. Import the necessary modules.
2. Create the Dataset using make_blob function.
3. Assign the counter value using the Counter Function and with the help of a for loop iterate over the values.
4. Plot the row values in the graph.

## PROGRAM:

```
/*
Program to implement binary classification.
Developed by: P.Ramadevi
Register Number: 212219040119
*/
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

## OUTPUT:
![image](https://user-images.githubusercontent.com/75235293/164049056-faef23a9-63d5-44ce-8a0e-fcb06003d1f2.png)


## RESULT:

Thus the python program performed binary classification successfully.
