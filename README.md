# SDET-Glossary
 
*place main contents of your branch withing allocated headers
 
### OOP main glossary
 
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
