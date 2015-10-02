# Lab601: Identify the design pattern and participants from the program (group of 2 students)

In this lab, each group of 2 students has to identify a design pattern and all participants 
from the provided C# source code. 

## Submission: a written report which contains

1. A class diagram of the original source code
![570610601](http://www.uppic.biz/images/2015/09/29/Lab601.png)
2. Detail explaination about the identified pattern and all the parcipants
> **Answer:** This code have abstract factory pattern that encapsulated a group of factories without specifying their concrete classes.

3. Explain how to include "an asian herbivore and an asian carnivore" to the program: 
  - Show the class diagram of the program after including the new requirment.
  > 
  - Test the new requirment by modifying the main function and show the result.
  ![570610601](http://www.uppic.biz/images/2015/10/02/Lab601_edited_result.png)
  - Show the main function and snippet of C# code that is related to the process.
  ```cs
  public static void Main()
  {
      ContinentFactory africa = new AfricaFactory();
      AnimalWorld world = new AnimalWorld(africa);
      world.RunFoodChain();

      ContinentFactory america = new AmericaFactory();
      world = new AnimalWorld(america);
      world.RunFoodChain();

      ContinentFactory asia = new AsiaFactory();
      world = new AnimalWorld(asia);
      world.RunFoodChain();

      // Wait for user input
      Console.ReadKey();
  }
  
  class AsiaFactory : ContinentFactory
  {
      public override Herbivore CreateHerbivore()
      {
          return new Deer();
      }
      public override Carnivore CreateCarnivore()
      {
          return new Tiger();
      }
  }
  class Deer : Herbivore
  {
  }
  class Tiger : Carnivore
  {
      public override void Eat(Herbivore h)
      {
          // Eat Deer
          Console.WriteLine(this.GetType().Name +
            " eats " + h.GetType().Name);
      }
  }
  ```
