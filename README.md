# SDET-Glossary
 
*place main contents of your branch withing allocated headers
 
### OOP main glossary
 
## Instance Vriables

# Objectives
1. Define instance variables.
2. Distinguish instance variables from local variables
3. Describe how instance variables give objects attributes and properties

## Defining instance variables
* Instance variable are variables that leave through the instance of a class. declaring an instance variable in a method that belongs to a calss would make that variable useble in all other meethods that belong to that intstace of the class. We declare instance variable by addinf ```@``` at the beggening of the variable name

## Distinguishing instace variables from local variables
* A variable are ways to passs data. for instance ```test = "something"``` in this we set a new variable called ```test``` and its value is ```"something"``` using the ```" "``` sign means the value is in form of string. This way we passed values/data through variable. 
* When using this form of declaration it would be a local variable. Decalring it in a method it only be acessible in that method of the class.
```
class TestClass
  def test_method
    example = "test"
  end

  def test_method_two
    example2 = example
  end
end
```
* consider the two methods are present in a class. If someone were to instantiate the class ```test = TestClass.new``` and then run ```test.est_method``` then ```test.test_method_two``` the user would get an error undifined local variable example, This happens beacause example only exist in first method.

* On the other hand if the variable ws to be instanced with ```@example = test``` it would live trhoughout the whole instance. If you were to look at the example above and replace example with @example
```
class TestClass
  def test_method
    @example = "test"
  end

  def test_method_two
    example2 = @example
  end
end
```
if you were to run the instancing and methods in that case ```example2 would be equal to "test"```

## Describe how instance variables give objects attributes and properties
* We use instance variables to pass atributes that are created in a different method and applied them in others.

### Ruby main glossary
 
### Testing main glossary
 
### Data main glossary