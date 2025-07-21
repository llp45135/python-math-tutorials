# Python 描述符

描述符是实现了\_\_get\_\_ \_\_set\_\_ \_\_delete\_\_其中任一方法的类型对象，根据是否有\_\_set\_\_区别是否为数据描述符。

```python
class DataDesc:
    def __get__(self, obj, objtype=None):
        return 'data'
    def __set__(self, obj, value):
        pass

class NonDataDesc:
    def __get__(self, obj, objtype=None):
        return 'nondata'

class C:
    a = DataDesc()
    b = NonDataDesc()
    c = 42
    d = NonDataDesc()

obj = C()
obj.a = 'inst_a'
obj.b = 'inst_b'
obj.c = 'inst_c'
# d 没有实例属性，直接访问

print(obj.a)  # 'data'（数据描述符优先）
print(obj.b)  # 'inst_b'（实例属性优先）
print(obj.c)  # 'inst_c'（实例属性优先）
print(obj.d)  # 'nondata'（非数据描述符被触发）
```

由此，我们有以下总结：

1. 描述符必须是type类型的成员，也就是class定义的内部成员(或者通过type(,,)动态定义的类型)
2. 通过类名可访问描述符C.a，也可以通过实例对象访问obj.a，而实例对象访问时候会有以下查找顺序：
    1. 无论obj.__dict__中是否有a，优先查找C.__dict__中的数据描述符。
    2. 如果没有1那么回退到访问obj.__dict__该名称a的普通对象(当obj只有__slot__时候转而查找__slot__)
    3. 如果没有2则查找C.__dict__的非数据描述符
    4. 如果没有3则返回C.__dict__中名为a的普通对象
    5. 如果没有4则报错
3. 注意上述数据中的第三条，平时在class中使用def定义的都是function类型的实例，其实现了__get__方法，所以在obj调用实例方法obj.foo时候（此时obj.__dict__自然没有覆盖obj.foo的项），会访问function的描述符协议，导致其访问内容变为bound method而不是function。这也是为什么直接通过类名和实例名访问函数时候的行为不一样。
特别的，内建的staticmethod和classmethod都是实现了__get__的装饰器，所以访问这些方法时候都会按描述符协议去访问。