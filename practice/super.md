```python
class Base(object):
    def __init__(self):
        print "Base created"
        self.a = 1
        self.b = 2


class A(Base):
    def __init__(self):
        Base.__init__(self)


class B(Base):
    def __init__(self):
        super(Base, B).__init__(self)


A()
B()
print issubclass(A, Base)
```

refer:
[super](http://www.artima.com/weblogs/viewpost.jsp?thread=236275)
[descriptor](http://users.rcn.com/python/download/Descriptor.htm)
