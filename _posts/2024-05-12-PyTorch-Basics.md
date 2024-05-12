---
classes: wide
toc: true
#sidebar:
#  nav: "docs"
layout: tag
permalink: /tags/PyTorch/
taxonomy: PyTorch # category name
entries_layout: grid # list (default), grid
---

## PyTorch 모델로 쓰기 위한 두가지 조건. 

Every neural network is the sub-class of nn.Module

### code 
~~~
class Model_Name(nn.Module):
~~~




Inheritance 
super 

To absorb every function other classes have

e.g. Parent Class : Human & Child Class: Student 
~~~
class Student(Human):
    def __init__(self):
        super(Student,self).__init__()
~~~


### Code
~~~
super().__init__() → python 3 only
super(Child Class,self).__init__() → python 2,3  // Recommend using this expression  
~~~

    class Model_Name(nn.Module):
        def __init__(self):
    super(Model_Name, self).__init__() <- torch.nn.Module을 상속하고 있음 

Need to override __init()__과 forward()

### __init()__
: define the  module (e.g nn.Linear, nn.Conv2d), activation function(e.g nn.functional.relu, nn.functional.sigmoid) used in the model 

### forward()
: define operations in the model 
( bacward operations can be done by using backward()- do not need to define)


PyTorch의 nn 라이브러리는 Neural Network의 모든 것을 포괄하는 모든 신경망 모델의 Base Class이다. 



nn.Module을 상속한 subclass가 신경망 모델로 사용되기 위해선 앞서 소개한 두 메소드를 override 해야한다. 

__init__(self): initialize; 내가 사용하고 싶은, 내 신경망 모델에 사용될 구성품들을 정의 및 초기화 하는 메소드이다. 
forward(self, x): specify the connections;  이닛에서 정의된 구성품들을 연결하는 메소드이다. 

