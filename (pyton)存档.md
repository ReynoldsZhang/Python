str_spe = "I don\'t"#str_spe = "I don't"����ɹ���
str_spe



name = input("Your name is:")
print("Hello %s, good morning!"%name)


def say(message, time= 1):
    print(message * time)

say('hello')

say('hello ', 3)

a = say('hello ', 3)
a



def do(*p):#�У�*�����ڣ����Կ����ж������
    print(p)

do(1, 2, 3)#���ᱨ��


def does(p):#û�У�*�����ڣ��޷�����������
    print(p)

does(1, 2, 3)#�ᱨ��












class Car():   #���ж���
    def infor(self):
        print("This is a car")

car = Car()
car.infor()

isinstance(car, Car)

isinstance(car, str)

class A:
    pass

class A:
    def __init__(hahaha, v):   #(init)�����������
        hahaha.value = v
    def show(hahaha):
        print(hahaha.value)

a = A(3)
a.show()



class Student:
    def __init__(self):  #������c++�е�Ĭ�Ϲ��캯��
        self.name = None
        self. grade = None
        
    def print_grade(self):
        print("%s grade is %s" %(self. name, self.grade))
        
s1 = Student()  #��������s1
s1.name = "Tony"
s1.grade = 8

s2 = Student()  #��������s2
s2.name = "Jony"
s2.grade = 7

s1.print_grade()
s2.print_grade()
#����һ���࣬����ʱ��

ANOTHER WAY


class Student:
    def __init__(self, name, grade): #������c++�е��вι��캯��
        self.name = name
        self.grade = grade
        
    def print_grade(self):
        print("%s grade is %s" %(self.name, self.grade))
        
s1 = Student("Tony", 8) #��������s1
s2 = Student("Jony", 7) #��������s2

s1.print_grade()
s2. print_grade()
#����һ������࣬Ч��һ��



class Car:
    price = 100000    #����������
    def __init__(self, c):
        self.color = c   #����ʵ������

car1 = Car("Red")  #ʵ��������

car2 = Car("Bule")

#�鿴ʵ�����Ժ������Ե�֪
print(car1.color, Car.price)

#�޸�������
Car.price = 110000

#��̬����������
Car.name = 'aaa'

#�޸�ʵ������
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
�̳У�
Animal������Ϊ����
   ��������
Dog �� CatΪAnimal���Ӵ�
���������������ƣ��Ҽ̳���Animal�����������ܣ�
"""

#���Ƕ�̬
class CLanguage:
    def say(self):
        print("��ֵ���� CLanguage ���ʵ������")
class CPython:
    def say(self):
        print("��ֵ���� CPython ���ʵ������")
a = CLanguage()
a.say()
a = CPython()
a.say()

class CLanguage:
    def say(self):
        print("���õ��� CLanguage ���say����")
class CPython:
    def say(self):
        print("���õ��� CPython ���say����")
class CLinux(CLanguage):
    def say(self):
        print("���õ��� CLinux ���say����")
        
a = CLanguage()
a.say()
a = CPython()
a.say()
a = CLinux()
a.say()




import pandas as pd   #����һ���� pdΪ����

obj = pd.Series([4, 7, -5, 3])
obj

obj.index

obj2 = pd.Series([4, 7 , -5, 3], index = ["a", "b", "c", "d"])
obj2

obj2["b":"c"]  #��֮ǰ����Ƭ��ͬ

obj.describe() #����һ��series����

obj.index

#���
print(obj2.sum())
#���ֵ
print(obj2.mean())
#�����
print(obj2.max())
#����С
print(obj.min())
#����
print(obj2.count())
#���׼��
print(obj2.std())
#�󷽲�
print(obj2.var())
#����λ��
print(obj2.median())

obj2 * 2

dic = {"Python":1, "C":2, "Java":3, "Go":4, "Css":5, "SQL":6, "PHP":7}
obj3 = pd.Series(dic)
obj3

# ����Serise �� index������
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
    "����":[62, 72, 93, 88, 93],
    "��ѧ":[95, 65, 86, 66, 87],
    "Ӣ��":[66, 75, 82, 69, 82]
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

#reindex��������
se1 = pd.Series([1, 7, 3, 9], index=["d", "c", "a", "f"])
se1

data3 = pd.DataFrame({"k1":["one"] * 3 + ["tow"] * 4, "k2":[1, 1, 2, 3, 3, 4, 4]})
data3

d4.groupby('A').cum()   #���ݷ������


