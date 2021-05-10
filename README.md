Python 3.9.4 (tags/v3.9.4:1f2e308, Apr  6 2021, 13:40:21) [MSC v.1928 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license()" for more information.
>>> a = [3, 6, 9]
>>> type(a)
<class 'list'>
>>> 
>>> a[0]
3
>>> a[1]
6
>>> a[2]
9
>>> a[3]
Traceback (most recent call last):
  File "<pyshell#6>", line 1, in <module>
    a[3]
IndexError: list index out of range
>>> len(a)
3
>>> b = [6, 8, 9]
>>> a
[3, 6, 9]
>>> b
[6, 8, 9]
>>> a + b
[3, 6, 9, 6, 8, 9]
>>> ab = a + b
>>> ab
[3, 6, 9, 6, 8, 9]
>>> a
[3, 6, 9]
>>> b
[6, 8, 9]
>>> a.extend(b)
>>> a
[3, 6, 9, 6, 8, 9]
>>> len(a)
6
>>> a[5]
9
>>> a[5] = 99
>>> a
[3, 6, 9, 6, 8, 99]
>>> a[6]
Traceback (most recent call last):
  File "<pyshell#22>", line 1, in <module>
    a[6]
IndexError: list index out of range
>>> a[6] = 77
Traceback (most recent call last):
  File "<pyshell#23>", line 1, in <module>
    a[6] = 77
IndexError: list assignment index out of range
>>> a.append(77)
>>> a.append(44)
>>> a
[3, 6, 9, 6, 8, 99, 77, 44]
>>> len(a)
8
>>> a.append(66, 33)
Traceback (most recent call last):
  File "<pyshell#28>", line 1, in <module>
    a.append(66, 33)
TypeError: list.append() takes exactly one argument (2 given)
>>> a.append([66, 33])
>>> a
[3, 6, 9, 6, 8, 99, 77, 44, [66, 33]]
>>> a.extend([22, 88])
>>> a
[3, 6, 9, 6, 8, 99, 77, 44, [66, 33], 22, 88]
>>> a.insert(2, 80)
>>> a
[3, 6, 80, 9, 6, 8, 99, 77, 44, [66, 33], 22, 88]
>>> a.insert(4, 45)
>>> a
[3, 6, 80, 9, 45, 6, 8, 99, 77, 44, [66, 33], 22, 88]
>>> a.insert(0, 555)
>>> a
[555, 3, 6, 80, 9, 45, 6, 8, 99, 77, 44, [66, 33], 22, 88]
>>> a.pop()
88
>>> a.pop()
22
>>> a
[555, 3, 6, 80, 9, 45, 6, 8, 99, 77, 44, [66, 33]]
>>> a.pop()
[66, 33]
>>> a
[555, 3, 6, 80, 9, 45, 6, 8, 99, 77, 44]
>>> a.index(3)
1
>>> a.index(555)
0
>>> a.index(9)
4
>>> a.index(22222)
Traceback (most recent call last):
  File "<pyshell#47>", line 1, in <module>
    a.index(22222)
ValueError: 22222 is not in list
>>> a
[555, 3, 6, 80, 9, 45, 6, 8, 99, 77, 44]
>>> a.append(b)
>>> a
[555, 3, 6, 80, 9, 45, 6, 8, 99, 77, 44, [6, 8, 9]]
>>> a.remove(44)
>>> a
[555, 3, 6, 80, 9, 45, 6, 8, 99, 77, [6, 8, 9]]
>>> a.remove([6])
Traceback (most recent call last):
  File "<pyshell#53>", line 1, in <module>
    a.remove([6])
ValueError: list.remove(x): x not in list
>>> a.pop()
[6, 8, 9]
>>> t = a.pop()
>>> t
77
>>> t = a.pop()
>>> t
99
>>> a.append(b)
>>> a
[555, 3, 6, 80, 9, 45, 6, 8, [6, 8, 9]]
>>> a3 = a.pop()
>>> a3
[6, 8, 9]
>>> a3[2] = 77777
>>> a3
[6, 8, 77777]
>>> a.append(b)
>>> a
[555, 3, 6, 80, 9, 45, 6, 8, [6, 8, 77777]]
>>> a.append(9)
>>> a.append(9)
>>> a
[555, 3, 6, 80, 9, 45, 6, 8, [6, 8, 77777], 9, 9]
>>> a.count(9)
3
>>> a.count(6)
2
>>> a.count(3)
1
>>> a.count(3333)
0
>>> a.del(6)
SyntaxError: invalid syntax
>>> a.del(a[4])
SyntaxError: invalid syntax
>>> del(a[4])
>>> a
[555, 3, 6, 80, 45, 6, 8, [6, 8, 77777], 9, 9]
>>> a.remove(6)
>>> a.remove(9)
>>> a
[555, 3, 80, 45, 6, 8, [6, 8, 77777], 9]
>>> a
[555, 3, 80, 45, 6, 8, [6, 8, 77777], 9]
>>> aa = a
>>> id(a)
1946220962304
>>> id(aa)
1946220962304
>>> 
>>> a[1] = 4444
>>> aa
[555, 4444, 80, 45, 6, 8, [6, 8, 77777], 9]
>>> a
[555, 4444, 80, 45, 6, 8, [6, 8, 77777], 9]
>>> aaa = a.copy()
>>> aa
[555, 4444, 80, 45, 6, 8, [6, 8, 77777], 9]
>>> a
[555, 4444, 80, 45, 6, 8, [6, 8, 77777], 9]
>>> aaa
[555, 4444, 80, 45, 6, 8, [6, 8, 77777], 9]
>>> 
>>> a[1] = 22
>>> a
[555, 22, 80, 45, 6, 8, [6, 8, 77777], 9]
>>> aa
[555, 22, 80, 45, 6, 8, [6, 8, 77777], 9]
>>> 
>>> aaa
[555, 4444, 80, 45, 6, 8, [6, 8, 77777], 9]
>>> a.reverse()
>>> a
[9, [6, 8, 77777], 8, 6, 45, 80, 22, 555]
>>> a.sort()
Traceback (most recent call last):
  File "<pyshell#101>", line 1, in <module>
    a.sort()
TypeError: '<' not supported between instances of 'list' and 'int'
>>> a.remove([6, 8, 77777])
>>> a
[9, 8, 6, 45, 80, 22, 555]
>>> a.reverse()
>>> a
[555, 22, 80, 45, 6, 8, 9]
>>> a.sort()
>>> a
[6, 8, 9, 22, 45, 80, 555]
>>> a.sort(reverse=True)
>>> a
[555, 80, 45, 22, 9, 8, 6]
>>> a.remove(22)
>>> a
[555, 80, 45, 9, 8, 6]
>>> len(a)
6
>>> a.clear()
>>> a
[]
>>> len(a)
0
>>> 
>>> i = 100
>>> j = 300
>>> i
100
>>> j
300
>>> t = i
>>> i = j
>>> j = t
>>> 
>>> i
300
>>> j
100
>>> 
>>> i, j = j, i
>>> i
100
>>> j
300
>>> i, j = j, i ## data  맞교환
>>> 
>>> z = 10, 20, 30
>>> z
(10, 20, 30)
>>> type(z)
<class 'tuple'>
>>> z1, z2, z3 = z
>>> 
>>> 
>>> dir
<built-in function dir>
>>> dir()
['__annotations__', '__builtins__', '__doc__', '__loader__', '__name__', '__package__', '__spec__', 'a', 'b', 'bb', 'i', 'j', 't', 'tt', 'z', 'z1', 'z2', 'z3']
>>> del a, b, bb, i, j, t, tt
>>> dir()
['__annotations__', '__builtins__', '__doc__', '__loader__', '__name__', '__package__', '__spec__', 'z', 'z1', 'z2', 'z3']
>>> import  keyword
>>> keyword.kwlist
['False', 'None', 'True', '__peg_parser__', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
>>> 
>>> 
>>> 
>>> 
>>>  a = {1, 2, 3, 4, 5}
 
SyntaxError: unexpected indent
>>> a = {1, 2, 3, 4, 5}
>>> b = {2, 4, 6}
>>> type(a)
<class 'set'>
>>> a
{1, 2, 3, 4, 5}
b
>>> 
>>> b
{2, 4, 6}
>>> a  | b
{1, 2, 3, 4, 5, 6}
>>> a & b
{2, 4}
>>> a - b
{1, 3, 5}
>>> b - a
{6}
>>> a.union(b)
{1, 2, 3, 4, 5, 6}
>>> a | b
{1, 2, 3, 4, 5, 6}
>>> 
>>> a.intersection(b)
{2, 4}
>>> a & b
{2, 4}
>>> len(a)
5
>>> len(b)
3
>>> a[0]
Traceback (most recent call last):
  File "<pyshell#232>", line 1, in <module>
    a[0]
TypeError: 'set' object is not subscriptable
>>> a.add(5)
>>> a
{1, 2, 3, 4, 5}
>>> a.add(2)
>>> a.add(2)
>>> a
{1, 2, 3, 4, 5}
>>> k = []
>>> k.append(2)
>>> k.append(2)
>>> k.append(2)
>>> k.append(2)
>>> k
[2, 2, 2, 2]
>>> a.remove(1)
>>> a
{2, 3, 4, 5}
>>> 2 in a
True
>>> 2.issubset(a)
SyntaxError: invalid syntax
>>> (2).issubset(a)
Traceback (most recent call last):
  File "<pyshell#248>", line 1, in <module>
    (2).issubset(a)
AttributeError: 'int' object has no attribute 'issubset'
>>> b.issubset(a)
False
>>> a = {2, 3}
>>> a
{2, 3}
>>> a.add(1)
>>> a.add(4)
>>> a.add(4)
>>> a.add(5)
>>> a
{1, 2, 3, 4, 5}
>>> a2 = {2, 3}
>>> a2
{2, 3}
>>> a2.issu
Traceback (most recent call last):
  File "<pyshell#259>", line 1, in <module>
    a2.issu
AttributeError: 'set' object has no attribute 'issu'
>>> a2.issubset(a)
True
>>> a2.issuperset(a)
False
>>> 
>>> 
>>> 
>>> 
>>> d = {'이름':'강호동', '나이':51, '직업' : 'MC'}
>>> type(d)
<class 'dict'>
>>> d[0]
Traceback (most recent call last):
  File "<pyshell#268>", line 1, in <module>
    d[0]
KeyError: 0
>>> d['이름']
'강호동'
>>> d['나이']
51
>>> a.keys()
Traceback (most recent call last):
  File "<pyshell#271>", line 1, in <module>
    a.keys()
AttributeError: 'set' object has no attribute 'keys'
>>> d.keys()
dict_keys(['이름', '나이', '직업'])
>>> d.values()
dict_values(['강호동', 51, 'MC'])
>>> d.items()
dict_items([('이름', '강호동'), ('나이', 51), ('직업', 'MC')])
>>> for  key, value in d.items():
	print(key, value)

	
이름 강호동
나이 51
직업 MC
>>> 
>>> for  i, j in d.items():
	print(i, ' ===> ',  j)

	
이름  ===>  강호동
나이  ===>  51
직업  ===>  MC
>>> dir(dict)
['__class__', '__class_getitem__', '__contains__', '__delattr__', '__delitem__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__ior__', '__iter__', '__le__', '__len__', '__lt__', '__ne__', '__new__', '__or__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__ror__', '__setattr__', '__setitem__', '__sizeof__', '__str__', '__subclasshook__', 'clear', 'copy', 'fromkeys', 'get', 'items', 'keys', 'pop', 'popitem', 'setdefault', 'update', 'values']
>>> d
{'이름': '강호동', '나이': 51, '직업': 'MC'}
>>> d.update({'수입':30})
>>> d
{'이름': '강호동', '나이': 51, '직업': 'MC', '수입': 30}
>>> d.get()
Traceback (most recent call last):
  File "<pyshell#285>", line 1, in <module>
    d.get()
TypeError: get expected at least 1 argument, got 0
>>> d.get('수입')
30
>>> d.get('나이')
51
>>> d.pop()
Traceback (most recent call last):
  File "<pyshell#288>", line 1, in <module>
    d.pop()
TypeError: pop expected at least 1 argument, got 0
>>> d.popitem()
('수입', 30)
>>> d
{'이름': '강호동', '나이': 51, '직업': 'MC'}
>>> 
>>> 
>>> a
{1, 2, 3, 4, 5}
>>> 2 in a
True
>>> 2 not in a
False
>>> aaa = a
>>> id(a)
1949509039040
>>> id(aaa)
1949509039040
>>> a is aaa
True
>>> aaa is aaa
True
>>> a is not aaa
False
>>> 
>>> ac = a.copy()
>>> id(ac)
1949509041056
>>> a is ac
False
>>> True & False
False
>>> True | False
True
>>> True ^ False
True
>>> True ^ True
False
## 성적 처리

st = []

with open('c:\\dd\\ss.txt', 'r', encoding='utf8') as f:
    for i in range(10):
        st.append(f.readline().split()) ## 라인단위로 읽어드림 
        st[i][1] = int(st[i][1])  ## str ==> int형으로 변환 
        st[i][2] = int(st[i][2])
        st[i][3] = int(st[i][3])
        
        ## 총점, 평균
        total = st[i][1] +  st[i][2] +  st[i][3] 
        avg = total / 3
        st[i].append(total)
        st[i].append(avg)

## 과목별 평균, 반전체 평균
total_kor = total_eng = total_mat = 0

for i in range(10):
    total_kor = total_kor + st[i][1]
    total_eng = total_eng + st[i][2]
    total_mat = total_mat + st[i][3]

avg_kor = total_kor / len(st)
avg_eng = total_eng / len(st)
avg_mat = total_mat / len(st)


print(' ******    성 적 표     **********')
print(' *********************************')
print(' 이름  국어  영어  수학 총점  평균')
print(' *********************************')
for i in range(10):
    print(' {}   {}   {}   {}   {}  {:.1f}'.format(st[i][0], st[i][1],
                            st[i][2], st[i][3], st[i][4], st[i][5]))
    
print(' *********************************\n')

print('      {} | {}  | {} | {:.2f}'
      .format(avg_kor, avg_eng, avg_mat, (avg_kor + avg_eng + avg_mat) / 3))
