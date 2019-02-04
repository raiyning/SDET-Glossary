# SDET-Glossary
 
*place main contents of your branch withing allocated headers
 
### OOP main glossary


### Abstraction

Abstraction is one of the key concepts of object-oriented programming. In abstraction, the programmer hides all the irrelevant data about an object in order to reduce complexity and increase efficiency—hiding the implementation details while presenting the essential features to the user. An example of abstraction can be given with a database system. The user does not know how the data is stored and how the data is maintained to a very technical degree. The complexities are hidden from the user; only that which is essential is exposed.

### Encapsulation

Similar to abstraction, encapsulation also hides data, but this time, for the purpose of protection. Encapsulation binds data and functions that manipulate that data into a single unit such as a class (which is a model of objects). For example, in ruby, encapsulation can make methods and variables private within a class which prevents other classes from accessing them (unless they are made public), therefore, preventing the unauthorised use of them. Only the object's methods can directly manipulate or inspect its fields.

### Inheritance 

Inheritance is the idea of getting or inheriting features from a parent. This concept is essential in object-oriented programming. In OOP this means that a child class (or subclass) can inherit features from a parent class (super class). The child class inherits attributes and methods from the parent class. This enables the child class (subclass) to define new attributes and methods which are then applied to those that were inherited. In other words, what has been inherited can be overridden in the child class and new logic can be created.

### Polymorphism 

Poly is the Greek word for many; morph in the Greek means forms—so polymorphism means the ability to be many forms. In OOP polymorphism refers to the ability of a variable, function or object to take on many forms. Polymorphism incorporates inheritance due to the fact that classes that inherited from the  same parent class (super class) may contain methods (or functions) bearing the same name—but when executed, exhibit different behaviours. 

# Instance Variables

## Objectives

1. Define instance variables.
2. Distinguish instance variables from local variables
3. Describe how instance variables give objects attributes and properties

## Defining instance variables
* Instance variable are variables that leave through the instance of a class. declaring an instance variable in a method that belongs to a calss would make that variable useble in all other meethods that belong to that intstace of the class. We declare instance variable by adding ```@``` at the beggening of the variable name

## Distinguishing instace variables from local variables
* A variable is a way to pass data for instance ```test = "something"``` in this we set a new variable called ```test``` and its value is ```"something"```. Using the ```" "``` sign means the value is in the form of string. This way we passed values/data through variables. 
* When using this form of declaration it would be a local variable. Declaring it in a method means it is only acessible in that method of the class.
```
class TestClass
  def test_method
    duck = "test"
  end

  def test_method_two
    duck2 = duck
  end
end
```
* consider the two methods are present in a class. If someone were to instantiate the class ```test = TestClass.new``` and then run ```test.test_method``` then ```test.test_method_two``` the user would get an error ```undefined local variable duck``` . This happens because ```duck``` only exists in the first method.

* On the other hand if the variable was to be instantiated with ```@duck = "test"``` it would live throughout the whole instance. 
```
class TestClass
  def test_method
    @duck = "test"
  end

  def test_method_two
    duck2 = @duck
  end
end
```
If you were to look at the first example and replace ```duck``` with ```@duck``` then running the methods would result ```duck2 to be equal to "test"```

## Describe how instance variables give objects attributes and properties
* We use instance variables to pass atributes that are created in a different method and applied them in others.

## Classes and Modules
### What is a Class?
A class is defined inside a file. A class is a group of methods and attributes that share commonalities.

### What is a Module?
A module is a modular part of programming which can be called by classes in order to keep code DRY. This typically happens when many classes have the same method which does the same thing.

#### Glossary
DRY - Don't Repeat Yourself

### Ruby main glossary

 ### DataTypes
  Data types in Ruby represents different types of data like text, string, numbers, etc. All data types are based on classes because it is a Object-Oriented language. There are different data types in Ruby as follows:

                  Numbers
                  Boolean
                  Strings
                  Hashes
                  Arrays
                  Symbols

  #### Numbers:
   Generally a number is defined as a series of digits and by using a dot as a decimal mark. There are different kinds of numbers like integers and float.

      E.g. Integer = 3, 30, 300, 3000
          Float = 1.2, 1.23, 1.234, 1.2345

  #### Boolean:
   Boolean data type represents only one bit of information either true(1) or false(0).


      E.g.  if true
              puts "It is True!"
            else
              puts "It is False!"
            end

  #### Strings: 
  A string is a group of letters that represent a sentence or a word. Strings are defined by enclosing a text within a single (”) or double (“”) quotes. You can use both double quotes and single quotes to create strings.

      E.g. puts "String Data Type"

  #### Hashes: 
  A hash assign its values to its key. Value to a key is assigned by => sign. A key pair is separated with a comma between them and all the pairs are enclosed within curly braces.

      E.g. hash = colors = { "red" => 0xf00, "green" => 0x0f0, "blue" => 0x00f }

  #### Arrays: 
  An array stores data or list of data. It can contain all types of data. Data in an array are separated by comma in between them and are enclosed within square bracket.The position of elements in an array starts with 0. 

      E.g.  ary = ["fred", 10, 3.14, "This is a string", "last element"]


#### Symbols :

  A Symbol is basically the same as a String, but with one important difference. A Symbol is immutable. They are usually generated by using :name literal syntax

#### MVC
The Model-View-Controller (MVC) is an architectural pattern that separates an application into three main logical components: the model, the view, and the controller. Each of these components are built to handle specific development aspects of an application. MVC is one of the most frequently used industry-standard web development framework to create scalable and extensible projects.

![Image description](https://danielmiessler.com/images/MVC1.png)

Model -
The Model component corresponds to all the data-related logic that the user works with. This can represent either the data that is being transferred between the View and Controller components or any other business logic-related data. For example, a Customer object will retrieve the customer information from the database, manipulate it and update it data back to the database or use it to render data.

View -
The View component is used for all the UI logic of the application. For example, the Customer view will include all the UI components such as text boxes, dropdowns, etc. that the final user interacts with.

Controller -
Controllers act as an interface between Model and View components to process all the business logic and incoming requests, manipulate data using the Model component and interact with the Views to render the final output. For example, the Customer controller will handle all the interactions and inputs from the Customer View and update the database using the Customer Model. The same controller will be used to view the Customer data.
 
#### GEMS

Gem is a ruby software package which offers specific functionalities to programs that run ruby. For example, if you want to have a function that lets you authenticate within your program so you don't always need to write one out, you can get it in form of a gem to put within the program. Gems are stored in a file called in Ruby Gemfile. This file has to be located in the root of the project in order for the gems to run.

##### HTTParty

HTTParty is a gem you can use in Ruby to help call an external API through the use of request methods, such as GET, POST, PUT and DELETE. Through the use of the HTTParty gem, it helps to expose the module and encapsulate all of the methods from that specific module to help with calling the external API through the different request methods. 

##### Dotenv

Dotenv helps to load enviromental variables from an .env file into a specific file by calling it within the methods. If you want more information on this, click on the following link: https://github.com/bkeepers/dotenv

##### JSON

JSON gem helps provide the methods to use within your class in your project, so that you can easily parse through external API's into a json format. 

### Testing main glossary
 
### Data main glossary

