# Lab602: Identify design pattern and participants from program (group of 2 students)

In this lab, each group of 2 students has to identify a design pattern and all participants 
from the provided C# program. 

## Submission: a written report which contains

1. A class diagram of the original source code
![570610601](http://i58.tinypic.com/29dyccz.png)
2. Detail explaination about the identified pattern and all the parcipants

> This program uses factory method design pattern that define an interface for creating an object and let subclasses decide hich class to instantiate. The factory method have around 4 participants.
######Product – defines the interface of objects the factory method creates.
######ConcreteProduct – implements the Product interface.
######Creator – declare the factory method, which returns an object of type Product.
######ConcreteCreator – overrides the factory method to return an instance of a ConcreteProduct.
