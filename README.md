# Baekjoon 
## 단계별 문제

### 1. 빠른 문자열 받기
##### no.15552
```
import sys
a, b, c = map(int, sys.stdin.readline().split())
```
> map() : 리스트의 요소를 지정된 함수로 처리해주는 함수 
> > int형으로 형변환
> input 대신 sys.stdin.readline 사용 가능 (한 줄 단위의 입력 -> 개행(\n) 문자 포함)
> > sys.stdin.readline.rstrip() or int(sys.stdin.readline())
> > 정해진 개수의 정수를 한줄에 입력 sys.stdin.readline().split()

### 2. 형변환
##### no.15552
```
print("Case #"+str(num)+":",A+B)
> Case #1: 2
```
> num을 문자열로 변환
```
print("Case #"+chr(num)+":",A+B)
> Case #: 2
```
> num을 문자로 변환
> > 하나의 캐릭터만 변환 가능

### 3. List 대괄호 없애기
##### no.10871
```
print(result)
> [1, 4, 2, 3]
print(" ".join(map(str,result)))
> 1 4 2 3
```
> 따옴표 안에 적힌 형태로 리스트 출력 현태를 변경
> > 따옴표 안에 공백을 넣어야 띄어쓰기 가능

### 3. 예외처리
##### no.10951
```
  try :
    a, b = map(int, sys.stdin.readline().split())
    print(a+b)
  except :
    break
```
> 오류가 발생하면 except 블록이 수행됨
```
  try :
    ...
  except 발생 오류 as 오류 메시지 변수 :
    ...
```
> 발생 오류와 오률 메시지 변수까지 포함
> > ex. except ZeroDivisionError as e :
> >     print(e)

### 4. 집합
##### no.3052
```
list = []
for i in range(10) :
  list.append(int(input())%42)
list = set(list)
print(len(list))
```
> list를 집합 자료형으로 변경 
> > list의 중복 value 제거 

### 5. 함수
##### no. 15596
```
def 함수명(parameter1, ...) :
  do something
  return result
```
> parameter의 경우 자료형을 구분할 필요 없음 
```
함수명(argument1, argument2, ...)
```
> 함수 동작 명령, return 값을 

### 6. split vs strip
```
a = int(input().strip)
b = int(input().split)
```
> strip : 좌우 whitespace 제거
> > 문자 하나 들어올 때 사용
> split : ()의 내용을 기준으로 str를 분할
> > 한 줄에 여러 문자가 들어올 때 사용 
