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

### Ruby main glossary
 
### Testing main glossary
 
### Data main glossary
