# Intro to Python: Object Oriented Programming

**<a href="https://github.com/JoeGanser/teaching/blob/main/Lectures/Python_for_DS/ObjectOrientedProgramming1/OOP_part1.ipynb">Notebook Github Repo</>**

### Example 1: Importing & Instantiating a class


```python
from timewithproperties import Time #comment: see source [1]

wake_up = Time(hour=7,minute=45,second=30)

print(wake_up.time)
```

??? note "timewithproperties.py"
    ```py linenums="1"
    from itertools import combinations

    """Class with time read-write properties"""
    from datetime import datetime,timedelta
    class Time:
    """Class time with read-write properties"""
	    def __init__(self,hour = 0,minute = 0,second = 0):
        """Initialize each attrbiute"""
		    self.hour = int(hour)
		    self.minute = int(minute)
		    self.second = int(second)
		    self.time = (self.hour,self.minute,self.second)

	    @property
	    def hour(self):
        """Return the hour"""
		    return self._hour

	    @hour.setter
	    def hour(self,hour):
        """Set the hour."""
		    if not (0<=hour<24):
			    raise ValueError(f'Hour ({hour}) must be 0-23')
		    self._hour = hour

	    @property
        def minute(self):
        """Return the minute"""
            return self._minute

	    @minute.setter
        def minute(self,minute):
        """Set minute"""
            if not (0<=minute<60):
                raise ValueError(f'Minute({minute}) must be 0-59')
		    self._minute = minute

	    @property
	    def second(self):
        """Return the second"""
		    return self._second


	    @second.setter
	    def second(self,second):
		""" Set the second"""
		    if not (0<=second<60):
                raise ValueError(f'Second ({second}) must be 0-59')
		    self._second = second


	    def set_time(self,hour=0,minute=0,second=0):
		"""set values of hour, minute and second"""
		    self.hour = hour
		    self.minute = minute
		    self.second = second
		    self._time  = (hour,minute,second)


	    @property
	    def time(self):
		"""Return hour, minute and second as a tuple"""
		    return self._time

	    @time.setter
	    def time(self,time_tuple):
		    """Set time form a tuple comntianing hour,minute and second"""
		    self.set_time(time_tuple[0],time_tuple[1],time_tuple[2])
	

	    def add_time(self,hour,minute,second):
            current_time = datetime.strptime('{0}:{1}:{2}'.format(self.hour,self.minute,self.second), '%H:%M:%S')
		    new_time = current_time + timedelta(days=0,hours=hour,minutes=minute,seconds=second)
		    new_time_print = new_time.strftime('%H:%M:%S')
		    print('new time: ',new_time_print)
		    hour,minute,second = [int(j) for j in new_time_print.split(':')]
		    self.set_time(hour,minute,second)
    ```


### Example 2: Using a function within a class


```python
from timewithproperties import Time

wake_up2 = Time(hour=7,minute=45,second=30)

wake_up2.add_time(hour=4,minute=5,second=10)

print(wake_up2.time)
```

### Example 3: Using Class doc strings

Show the doc strings associated with;
* Time class
* the `add_time` function in the time class


```python
Time?
```


```python
Time.add_time?
```

### Example 4: Building a class doc string


```python
class demo:
    """This is the class doc string."""
    def __init__(self,variable1):
        self.variable1 =variable1
    
    def print_variables(self):
        """This is the doc string for this function in this class"""
        print(self.variable1)
        
        
d = demo('hello')
d.print_variables()
```

### Example 5: Public vs Private Attributes

* The `__` underscore at the beginning of the class is what defines the private vs public property; e.g. `self.__private_data`


```python
class Private:
    def __init__(self):
        self.public_data="public"
        self.__private_data="private"
        
p = Private()
print(p.public_data)
print(p.__private_data)
```

### Example 6: Decorators

In this example we create a decorator function that takes an arbitrary python function and multiplies it's output by a factor of 10.


```python
def multiply_by10(func):
    def inner(*args,**kwargs):
        return 10*func(*args,**kwargs)
    return inner

@multiply_by10
def add_two_numbers(a,b):
    return a+b

add_two_numbers(3,5)
```

### Example 7: Read only vs changeable properties

* Class with a property setter


```python
class property_setter:
    def __init__(self,alpha):
        self._a = alpha
        
    @property
    def a(self):
        return self._a
    
    @a.setter
    def a(self,alpha):
        self._a = alpha
        
p7 = property_setter('hello')
print(p7._a)

p7._a='good bye'
print(p7._a)
```

**Class **without** a property setter, for mutability**


```python
class property_no_setter:
    def __init__(self,alpha):
        self._a = alpha
        
    @property
    def a(self):
        return self._a

        
p71 = property_no_setter('hello')
print(p71.a)

p71.a='good bye'
print(p71.a)
```

### Example 8: Representing a class


```python
class demo_repr_method:
    def __init__(self,alpha):
        self.alpha = alpha
        
    def __repr__(self):
        """Return initialization strin for the class"""
        return (f'demo_repr_method(alpha={self.alpha})')
```


```python
d = demo_repr_method(45)

print(d.__repr__())
```

**What happens if we change the parameters?**


```python
d.alpha = 19

print(d.__repr__())
```


```python

```

### Sources
* [1] Timewithproperties.py - this file taken from the textbook "Intro to Python for Computer Science and Data Science" By Deitel & Deitel, Pearson Publications 2020