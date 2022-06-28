str_spe = "I don\'t"#str_spe = "I don't"不会成功的
str_spe



name = input("Your name is:")
print("Hello %s, good morning!"%name)


def say(message, time= 1):
    print(message * time)

say('hello')

say('hello ', 3)

a = say('hello ', 3)
a



def do(*p):#有（*）存在，所以可以有多个变量
    print(p)

do(1, 2, 3)#不会报错


def does(p):#没有（*）存在，无法输入多个变量
    print(p)

does(1, 2, 3)#会报错












class Car():   #自行定义
    def infor(self):
        print("This is a car")

car = Car()
car.infor()

isinstance(car, Car)

isinstance(car, str)

class A:
    pass

class A:
    def __init__(hahaha, v):   #(init)可以随意更换
        hahaha.value = v
    def show(hahaha):
        print(hahaha.value)

a = A(3)
a.show()



class Student:
    def __init__(self):  #类似于c++中的默认构造函数
        self.name = None
        self. grade = None
        
    def print_grade(self):
        print("%s grade is %s" %(self. name, self.grade))
        
s1 = Student()  #创建对象s1
s1.name = "Tony"
s1.grade = 8

s2 = Student()  #创建对象s2
s2.name = "Jony"
s2.grade = 7

s1.print_grade()
s2.print_grade()
#定义一个类，缩短时间

ANOTHER WAY


class Student:
    def __init__(self, name, grade): #类似于c++中的有参构造函数
        self.name = name
        self.grade = grade
        
    def print_grade(self):
        print("%s grade is %s" %(self.name, self.grade))
        
s1 = Student("Tony", 8) #创建对象s1
s2 = Student("Jony", 7) #创建对象s2

s1.print_grade()
s2. print_grade()
#比上一个更简洁，效果一样



class Car:
    price = 100000    #定义类属性
    def __init__(self, c):
        self.color = c   #定义实例属性

car1 = Car("Red")  #实例化对象

car2 = Car("Bule")

#查看实例属性和类属性得知
print(car1.color, Car.price)

#修改类属性
Car.price = 110000

#动态增加类属性
Car.name = 'aaa'

#修改实例属性
car1.color = "Yellow"
print(car2.color, Car.price, Car.name)
print(car1.color, Car.price, Car.name)



class Animal(object):
    def run(self):
        print('Animal is runing...')

class Dog(Animal):
    pass

class Cat(Animal):
    pass

dog = Dog()
dog.run()

cat = Cat()
cat.run()
"""
继承：
Animal被定义为父本
   他可以跑
Dog 和 Cat为Animal的子代
所以上面两个类似，且继承了Animal的特征（能跑）
"""

#不是多态
class CLanguage:
    def say(self):
        print("赋值的是 CLanguage 类的实例对象")
class CPython:
    def say(self):
        print("赋值的是 CPython 类的实例对象")
a = CLanguage()
a.say()
a = CPython()
a.say()

class CLanguage:
    def say(self):
        print("调用的是 CLanguage 类的say方法")
class CPython:
    def say(self):
        print("调用的是 CPython 类的say方法")
class CLinux(CLanguage):
    def say(self):
        print("调用的是 CLinux 类的say方法")
        
a = CLanguage()
a.say()
a = CPython()
a.say()
a = CLinux()
a.say()




import pandas as pd   #创建一个库 pd为库名

obj = pd.Series([4, 7, -5, 3])
obj

obj.index

obj2 = pd.Series([4, 7 , -5, 3], index = ["a", "b", "c", "d"])
obj2

obj2["b":"c"]  #与之前的切片不同

obj.describe() #返回一个series对象

obj.index

#求和
print(obj2.sum())
#求均值
print(obj2.mean())
#求最大
print(obj2.max())
#求最小
print(obj.min())
#计数
print(obj2.count())
#求标准差
print(obj2.std())
#求方差
print(obj2.var())
#求中位数
print(obj2.median())

obj2 * 2

dic = {"Python":1, "C":2, "Java":3, "Go":4, "Css":5, "SQL":6, "PHP":7}
obj3 = pd.Series(dic)
obj3

# 设置Serise 和 index的名字
obj3.name = "num"
obj3.index.name = "language"
obj3

ser5 = pd.Series(range(5))
ser5.where(ser5 > 0)

ser5.where(ser5>1,10)

pd.value_counts([1, 1, 3, 3, 3, 3, 2, 1])

ser6 = pd.Series(["cat", "dog", np.nan, "rabbit"])
ser6

ser6.map({"cat": "kitten", "dog": "puppy"})

ser6.map("I am a {}".format, na_action= "ignore")

ser7 = pd.Series([20, 21, 12], index=["London", "New York", "Helsinki"])
ser7

help(ser6.map)

ser7.apply(np.square)

ser7.apply(lambda x, value: x - value, args = (5,))

scores = {
    "语文":[62, 72, 93, 88, 93],
    "数学":[95, 65, 86, 66, 87],
    "英语":[66, 75, 82, 69, 82]
}
ids = [1001, 1002, 1003, 1004, 1005]
df2 = pd.DataFrame(data=scores, index=ids)
df2

df3 = pd.read_csv("data.csv")
df3

df2.describe()

df = pd.DataFrame(
    {"n":["wencky", "stany", "barbio"], "a":[29, 29, 3], "g":["w","m", "m"]}
)
df

df["id"] = [2001, 2002, 2003]
df.set_index("id", inplace=True)
df

#reindex重新索引
se1 = pd.Series([1, 7, 3, 9], index=["d", "c", "a", "f"])
se1

data3 = pd.DataFrame({"k1":["one"] * 3 + ["tow"] * 4, "k2":[1, 1, 2, 3, 3, 4, 4]})
data3

d4.groupby('A').cum()   #数据分组计算


