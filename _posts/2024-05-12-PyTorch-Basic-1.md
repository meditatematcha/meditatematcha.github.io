---
classes: wide
toc: true
sidebar:
#nav: "docs"
layout: tag
permalink: /tags/PyTorch/
taxonomy: PyTorch # category name
entries_layout: grid # list (default), grid
---

## PyTorch Neural Network Model
nn.Module: Package with necessary modules for building Deep learning model
Every neural network is the sub-class of nn.Module

### Inheritance : super 
Absorb every function of parent class 

### Code
~~~
super().__init__() → python 3 only
super(Child Class,self).__init__() → python 2,3  
~~~

### Sample Code 
Model inheriting nn.Module
~~~
class Model_Name(nn.Module):
  def __init__(self):
    super(Model_Name, self).__init__() <- torch.nn.Module을 상속하고 있음 
~~~

Student inheriting Human  
~~~
class Student(Human):
    def __init__(self):
        super(Student,self).__init__()
~~~

### __init()__
: initialize the parameters of the neural network
defines what components your model is going to have, such as layers(nn.Linear, nn.Conv2d)) activation functions(nn.functional.relu, nn.functional.sigmoid), etc.

### forward()
: define forward operations of the neural network, specifies how the data flows 
( bacward operations can be done by using backward() - do not need to be defined)



## Reference
https://discuss.pytorch.org/t/what-is-the-difference-init-and-forward-in-a-network-model/173907
