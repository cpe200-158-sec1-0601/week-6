# Lab602: Identify design pattern and participants from program (group of 2 students)

In this lab, each group of 2 students has to identify a design pattern and all participants 
from the provided C# program. 

## Submission: a written report which contains

1. A class diagram of the original source code
![570610601](http://i58.tinypic.com/29dyccz.png)
2. Detail explaination about the identified pattern and all the parcipants

> This program uses abstract factory design pattern that Provide an interface for creating families of related objects. The abstract factory have around 4 participants.
* Document class is AbstractFactory – declares an interface for operations that create abstract products.
* Resume and Report classes are ConcreteFactory – implements the operations to create concrete product objects.
* Page class is AbstractProduct – declare an interface for a type ofproduct object.
* SkillPage, EducationPage, ExperiencePage, IntroductionPage, ResultsPage, ConclusionPage, SummaryPage and BibliographyPage classes are Product – defines a product object to be created by the concrete factory and implements the AbstractProduct interface.
