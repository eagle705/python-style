
#### 주석관련
- 파이썬에서는 주석을 코드 옆에 쓰기보다 위에 쓰는게 암묵적인 관례임
```python

# Apple price
some_value = 100

```

#### 한줄이 너무 길어질 때
- 보통은 \ (백슬래시) 로 구분함
- \ 쓰기 싫을 땐 () 처리 해도가능
```python
s = 'aaaaaaaaaaa' \
    + 'bbbbbbbbbbb'
b = ('aaaaaaaaaaa' 
    + 'bbbbbbbbbbb')
```


#### Not의 쓰임
- boolean 변수 체크할 때

```python
is_ok = True

if not is_ok:
    print('hello')
```

#### 값이 들어있지 않다는 판정을 하는 테크닉

```python
# True 판정: is_ok = True, 값이 있는 자료구조
# False 판정: False, 0, 0.0, '', [], (), {}, set()
is_ok = [1,2,3,4]
if is_ok:
    print("ok")
else:
    print("no") 
```

#### None 판정
- ==을 써도 None판정은 가능하나 is가 통상적인 방법임
- 이유는 아래 코드 참고!
```python
is_empty = None
if is_empty is None:
    print('yes')

print(1 == True) # True : 1과 True라는 값을 비교해서 같음
print(1 is True) # False : 1과 True는 오브젝트가 다르기 때문에 False

```

- 팁인데 help 함수를 쓰면 해당 자료구조의 클래스가 출력됨
```python
is_empty = None
print(help(is_empty))

"""
Help on NoneType object:

class NoneType(object)
 |  Methods defined here:
 |  
 |  __bool__(self, /)
 |      self != 0
 |  
 |  __new__(*args, **kwargs) from builtins.type
 |      Create and return a new object.  See help(type) for accurate signature.
 |  
 |  __repr__(self, /)
 |      Return repr(self).

None

Process finished with exit code 0
"""
```

