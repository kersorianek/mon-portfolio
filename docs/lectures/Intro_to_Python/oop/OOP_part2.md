
# Object Oriented Programming Part 2

<a href="https://github.com/JoeGanser/teaching/blob/main/Lectures/Python_for_DS/ObjectOrientedProgramming2/OOP_part2.ipynb">Link to Notebook on Github</a>

### Example 1 Building class inheritence


```python
class loan:
    #parent class
    def statement(self):
        print('I am a bank loan')
        
class mortgage(loan):
    #child class
    def announcement(self):
        print('My interest rate')
        
m = mortgage()
m.announcement()
m.statement()
```

### Example 2: Parent-child classes

**Parent-child classes that have methods of the same name.**

```python
class animal:
    def statement(self):
        print('animal class')

class fish(animal):
    def statement(self):
        print('fish class')
        
f = fish()
f.statement()
```

### Example 3: Overriding the child classes' method 

**Overriding the child classes' method that shares the same name as the parent via the `super()` clause**


```python
class animal:
    def statement(self):
        return 'animal class'
    
class fish(animal):
    def statement(self):
        if super().statement() is not None:
            return super().statement()
        else:
            return 'fish class'
        
f = fish()
f.statement()
```

### Example 4: Using the `super()` method

**class to extract the constructor from the parent class into the child class**

```python
class loan:
    def __init__(self,rate):
        self.rate=rate
    
    def statement(self):
        return 'the rate is {}%'.format(self.rate)
    
class mortgage(loan):
    def __init__(self,rate,downpayment):
        super().__init__(rate)
        self.downpayment = downpayment
    def statement(self):
        return super().statement()+' and downpayment is {}'.format(self.downpayment)
    
l = loan(3)
m = mortgage(l.rate,10000)
m.statement()
```

### Example 5: Definine name spaces/variable scopes


```python
#global name space

def outer_function():
    #enclosed name space
    n=100
    def inner_function():
        #local name space
        m=200
```

### Example 6: Demonstrating local name spaces


```python
def add_N_to_number(x):
    N=3
    return N+x

N
```

### Example 7: Demonstrating global name spaces


```python
def add_V_to_number(x):
    global V
    V=3
    return V+x

add_V_to_number(5)
```


```python
print(V)
```

### Example 8: Polymorphisms

**A basic polymorphism in python**

```python
dictionary = {'a':10,'b':20,'c':30,'d':40}
word = 'alpha'
List = [0,1,2,3]

print(len(dictionary))
print(len(word))
print(len(List))
```

### Example 9: Demonstrating using a polymorphism

**Demonstrating using a polymorphism for classes that have attributes of the same name (with a list)**

```python
class animal:
    def __init__(self,name):
        self.name = name

class plant:
    def __init__(self,name):
        self.name = name

for c in [animal('dolphin'),plant('birch_tree')]:
    print(c.name)
```

### Example 10: Polymorphisms the share names

**Demonstrating using a polymorphism for classes that have attributes of the same name (with a function)**

```python
class animal:
    def __init__(self,name):
        self.name = name

class plant:
    def __init__(self,name):
        self.name = name

def class_polymorphism_printer(c):
    print(c.name)
    
class_polymorphism_printer(plant('venus_fly_trap'))
class_polymorphism_printer(animal('cow'))
```

### Example 11: Class polymorphism with inheritence

**using the parent-child inheritence to alter the methods of the child class.**


```python
class animal:
    def __init__(self,name):
        self.name = name
    
class vertebrae(animal):
    def __init__(self,warm_blooded):
        super().__init__('alligator')
        self.warm_blooded = warm_blooded
        
    
v = vertebrae(False)
print(v.name)
print(v.warm_blooded)
```
