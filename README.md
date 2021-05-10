while True:
    number1 = int(input(' 첫 번째 수 : '))
    if number1 == 0:
        break
    number2 = int(input(' 두 번째 수 : '))

    print(' {} + {} = {}'.format(number1, number2, number1+number2))




## 덧셈만 할 줄 아는 계산기

def plus(x, y):
    print(' {} + {} = {}'.format(x, y, x+y))
    return None

def Add(x, y):
    return x+y

while True:
    number1 = int(input(' 첫 번째 수 : '))
    if number1 == 0:
        break
    number2 = int(input(' 두 번째 수 : '))

    plus(number1, number2)
    #print(' {} + {} = {}'.format(number1, number2, number1+number2))

    retv = Add(number1, number2)
    print(' {} + {} = {}'.format(number1, number2, retv))



## 초간단 계산기

def Add(x, y):
    return x+y

def Sub(x, y):
    return x-y

def Mul(x, y):
    return x*y

def Div(x, y):
    return x//y

while True:
    print(' ** 간단 계산기 ** ')
    n1 = int(input(' 첫 번째 수 : '))
    if n1 == 0:
        break
    
    op = input(' [ +, - * / ] : ')
    
    n2 = int(input(' 두 번째 수 : '))

    if op == '+':
        res = Add(n1, n2)
    elif op == '-':
        res = Sub(n1, n2)
    elif op == '*':
        res = Mul(n1, n2)
    elif op == '/':
        res = Div(n1, n2)
    else:
        print(op, '없는 연산입니다.')

    print(' {}  {}  {} = {}'.format(n1, op, n2, res))
## 가변인수 ( 개수가 달라질 수 있다.)

def 함수2(인수1, 인수2):
    print(인수1, 인수2)

함수2('korea', 'seoul')


def Add1(x):
    print(x+x)

def Add2(x, y):
    print(x+y)

def Add3(x=100, y=100, z=100):
    ''' 나는 값을 더하는 함수다'''  ## doc string
    print(' x = ', x, ' y = ', y, ' z = ', z)
    #print(x+y+z)

def Call(name = '철수'):
    print(name, '야!  놀자')

Call()
Call('만수')
Call('경수')
Call(name='민경')


Add3(10, 20, 30)
Add3(30, 50)
Add3(10)
Add3()
Add3(z=5, x=7, y=3)
def SUM(x):
    s = 0
    for i in x:
        s = s + i
    return s

def SUM100(*x):
    s = 0
    for i in x:
        s = s + i
    return s
      
a = [3, 6, 9]

print(SUM(a))
print(SUM([1, 2, 3, 4, 5, 6]))
print(SUM100(*a))
>>> def plus(x, y):
	return x+y

>>> plus(10, 30)
40
>>> id(plus)
1803547725888
>>> k = 50
>>> k2 = 50
>>> id(k), id(k2)
(1803507363664, 1803507363664)
>>> 
>>> p = plus
>>> id(plus), id(p)
(1803547725888, 1803547725888)
>>> 
>>> plus(2, 3)
5
>>> p(3, 5)
8
>>> for i in range(1, 101):
	p(i, i+1)



>> a2 = list(filter(f, range(1, 11)))
>>> type(a2)
<class 'list'>
>>> 
>>> map(f, a2)
<map object at 0x000001A3EBD0A1F0>
>>> list(map(f, a2))
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
>>> list(map(f, range(1, 11)))
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
>>> 
>>> range(2, 101, 2)
range(2, 101, 2)
>>> list(range(2, 101, 2))
[2, 4, 6, 8, 10, 12, 14, 16, 18, 20, 22, 24, 26, 28, 30, 32, 34, 36, 38, 40, 42, 44, 46, 48, 50, 52, 54, 56, 58, 60, 62, 64, 66, 68, 70, 72, 74, 76, 78, 80, 82, 84, 86, 88, 90, 92, 94, 96, 98, 100]
>>> a4 = list(range(2, 101, 2))
>>> type(a4)
<class 'list'>
>>> a4
[2, 4, 6, 8, 10, 12, 14, 16, 18, 20, 22, 24, 26, 28, 30, 32, 34, 36, 38, 40, 42, 44, 46, 48, 50, 52, 54, 56, 58, 60, 62, 64, 66, 68, 70, 72, 74, 76, 78, 80, 82, 84, 86, 88, 90, 92, 94, 96, 98, 100]
>>> a5 = list(range(5, 101, 5))
>>> a5
[5, 10, 15, 20, 25, 30, 35, 40, 45, 50, 55, 60, 65, 70, 75, 80, 85, 90, 95, 100]
>>> 
>>> list(map(lambda x:x*x, a2))
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
>>> 
>>> a2
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
>>> 
>>> list(map(lambda x:x*x, range(1, 11)))
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
>>> 
>>> def  ff(x):
	return x*x

>>> ff(1)
1
>>> ff(2)
4




	ff(i)

	
1
4
9
16
25
36
49
64
81
100
>>> list(map(lambda x:x*x, range(1, 11)))
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
>>> 
>>> fff = lambda x:x*x
>>> 
>>> list(map(fff, range(1, 11)))
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
>>> 

