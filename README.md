# OOPS

Object-Oriented Programming (OOP) is a programming paradigm based on the concept of "objects." Objects are instances of classes that encapsulate data (attributes) and behavior (methods) into a single entity. OOP makes it easier to design and structure complex systems by representing them as a collection of interacting objects.

## Key Principles of OOP

>**Encapsulation:** Wrapping data and methods into a single unit (class) and restricting direct access to some components.


```csharp

using System;
internal class Student{
      
     public static void Main(String arg[]){
        int x=10;
        Console.WriteLine($"value of x is:{x}");

     }


}
```

>**Abstraction:** Hiding implementation details from the user and exposing only the essential features.

```csharp
using System;

public abstract class School{
    public abstract void Details();
}
public class Student:School{
    public void Details(){
        Console.WriteLine("This is XYZ from class X);
    }
    public static void Main(){
        Student obj = new Student();
        obj.Details();
    }
}


```

>**Inheritance:** Allowing a new class to acquire the properties and methods of an existing class.

```csharp
using System;

internal class Class1
{
  public Class1()
  {
    Console.WriteLine("Class1 constructor is called.");
  }
  public void Test1()
  {
    Console.WriteLine("Method 1"); 
  }
  public void Test2()
  {
    Console.WriteLine("Method 2"); 
  }
}
internal class Class2 : Class1
{
  public Class2()
  {
    Console.WriteLine("Class2 constructor is called.");
  }
  public void Test3()
  {
    Console.WriteLine("Method 3");
  }
  public void Test4()
  {
    Console.WriteLine("Method 4");
  }
  static void Main()
  {
    Class2 c = new Class2();
    c.Test1(); c.Test2();	//Calling members of parent class
    c.Test3(); c.Test4();	//Calling members of current class
    Console.ReadLine(); 
  }
}


```

>**Polymorphism:** Allowing objects to be treated as instances of their parent class, enabling one interface to be used for different data types.
```csharp
internal class LoadParent
{
   public void Test()
   {
      Console.WriteLine("Parent Class Test Method Is Called.");
   }
   public virtual void Show()  //Overridable
   {
      Console.WriteLine("Parent Class Show Method Is Called.");
   }
   public void Display()
   {
      Console.WriteLine("Parent Class Display Method Is Called.");
   }
}
internal class LoadChild : LoadParent
{
   //Overloading parent's Test method in child
   public void Test(int i)
   {
      Console.WriteLine("Child Class Test Method Is Called.");
   }
   static void Main()
   {
      LoadChild c = new LoadChild();
      c.Test();   	
      c.Test(10);    	
      c.Show();       	
      c.Display();   
      Console.ReadLine();
   }
}

```
