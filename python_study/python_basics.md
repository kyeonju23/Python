자료형
===================
* python 기초 정리

# 1. 숫자형
    - 정수형(Integer)
    - 실수형(Floating-point)
    - 8진수(Octal) > o or O 와 16진수(Hexadecimal) > 0x
    - 사칙연산(+, - ,*, /)
    - 제곱 **
    - 나머지 %
    - 몫 반환 //
    
# 2. 문자열 자료형
    문자열 만들기
    - 큰따옴표("a" or """a""")
    - 작은따옴표('a')
    - 백슬래시(\)를 사용해 작은따옴표와 큰따옴표를 문자열에 포함시키기
    food = 'Python\'s favorite food is perl'
    say = "\"Python is very easy.\" he says."
    - 줄바꾸기 \n
    - 연속된 따옴표 사용하기: 문자열이 여러 줄인 경우 이스케이프 코드를 사용하는 것보다 따옴표를 연속해서 쓰는 것이 훨씬 깔끔

    [이스케이프 코드]
    - 프로그래밍을 할 대 사용할 수 있도록 미리 정의해 둔 "문자 조합"
    - \n 문자열 안에서 줄을 바꿀 때 사용	
    - \t 문자열 사이에 탭 간격을 줄 때 사용
    - \\ 문자 \를 그대로 표현할 때 사용
    - \' 작은따옴표(')를 그대로 표현할 때 사용
    - \" 큰따옴표(")를 그대로 표현할 때 사용
    - \r 캐리지 리턴(줄 바꿈 문자, 현재 커서를 가장 앞으로 이동)
    - \f 폼 피드(줄 바꿈 문자, 현재 커서를 다음 줄로 이동)
    - \a 벨 소리(출력할 때 PC 스피커에서 '삑' 소리가 난다)
    - \b 백 스페이스
    - \000 널 문자

- 인덱싱(indexing): 가리킨다
    문자열을 뒤에서부터 읽기 위해서는 마이너스(-) 기호 붙이기
- 슬라이싱(Slicing): 잘라낸다
    a[시작번호:끝번호] 끝 번호에 해당하는 것은 포함하지 않음
- 문자열 포매팅(Formatting): 문자열 안에 어떤 값을 삽입하는 방법
    문자열 안에서 숫자를 넣고 싶은 자리에 %d 문자를 넣어주고, 삽입할 숫자는 가장 뒤에 있는 % 문자 다음에 넣는다. (%d는 문자열 포맷 코드)
    숫자 대신 문자를 넣고 싶다면 %s 후 % 뒤에 따옴표를 사용하여 문자 삽입 

    [문자열 포맷 코드]
    %s	문자열(String)
    %c	문자 1개(character)
    %d	정수(Integer)
    %f	부동소수(floating-point)
    %o	8진수
    %x	16진수
    %%	Literal % (문자 % 자체)
          
            
- 정렬
왼쪽 < , 오른쪽 >, 가운데 ^ 
공백채우기: 채워 넣을 문자 값은 정렬 문자 바로 앞에 넣기
- f 문자열 포매팅(python 3.6 이상부터 사용 가능) 문자열 앞에 f 접두사를 붙이면 사용 가능

    [문자열 관련 함수]
    - 문자 개수 세기(count)
    - 위치 알려주기(find, index): 찾는 문자나 문자열이 존재하지 않는다면 -1 을 반환
    - 문자열 삽입(join)
    - 소문자 -> 대문자 (upper)
    - 대문자 -> 소문자 (lower)
    - 공백 제거
        왼쪽(lstrip), 오른쪽(rstrip), 양쪽(strip)
    - 문자열 바꾸기(replace)
    - 문자열 나누기(split)

    
# 3. 리스트 자료형
리스트 생성 시 대괄호[]로 감싸주고 각 요소값은 쉼표(,)로 구분
리스트명 = [요소1, 요소2, 요소3, ...]
리스트 안에는 어떠한 자료형도 포함시킬 수 있다.
비어있는 리스트는 a = list()로 생성할 수도 있다. 

    - 리스트 더하기(+)
    - 리스트 반복하기(*)
    - 리스트 길이 구하기(len) 
    - 리스트 삭제 (del)
        a = [1,2,3]
        del a[1]
        즉, del 객체
        * 객체: 파이썬에서 사용되는 모든 자료형
    - 리스트에 요소 추가(append)
    - 리스트 정렬(sort)
    - 리스트 뒤집기(reverse)
    - 위치 반환(index): 리스트에 x 값이 있으면 x의 위치 값을 돌려줌
    - 리스트 요소 삽입(insert): insert(a,b) : 리스트의 a번째 위치에 b를 삽입
    - 리스트 요소 제거(remove): 리스트에서 첫 번째로 나오는 x를 삭제하는 함수
    - 리스트 요소 끄집어내기(pop): 리스트의 맨 마지막 요소를 돌려주고 그 요소는 삭제
    - 리스트에 포함된 요소 x의 개수 세기(count): 리스트 안에 x가 몇 개 있는지 조사하여 그 개수를 돌려주는 함수
    - 리스트 확장(extend): extend(x) 에서 x는 리스트만 올 수 있으며 원래의 a 리스트에 x 리스트 더하기 

# 4. 튜플 자료형
리스트와 다른 점
- 리스트는 []로 둘러싸지만 튜플은 ()로 둘러쌈
- 리스트는 그 값의 생성, 삭제, 수정이 가능하지만 튜플은 그 값을 바꿀 수 없음(변경, 삭제 불가능)

- 한 개의 요소만을 가질 때는 요소 뒤에 콤마(,)를 반디시 붙여야 하며 괄호()를 생략해도 무방
- 튜플과 리스트는 비슷한 역할을 하지만 프로그래밍 시 구별해서 사용해야 함
- 가장 큰 차이는 값을 변화시킬 수 있는가의 여부
    프로그램이 실행되는 동안 그 값이 항상 변하지 않기를 바란다거나 값이 바뀔까 걱정하고 싶지 않다면 주저없이 튜플을 사용해야 함
    실제 프로그램에서는 값이 변경되는 형태의 변수가 훨씬 많기 때문에 평균적으로 튜플보다는 리스트를 더 많이 사용

# 5. 딕셔너리 자료형
딕셔너리: Key 와 Value를 한 쌍으로 갖는 자료형
딕셔너리의 기본 
{Key1:Value1, Key2:Value2, Key3:Value3, ...}
Key와 Value의 쌍 여러 개가 { }로 둘러싸여 있다. 각각의 요소는 Key : Value 형태로 이루어져 있고 쉼표(,)로 구분되어 있다.
리스트나 튜플처럼 순차적으로 해당 요소값을 구하지 않고 Key와 Value를 얻음

### [딕셔너리 만들 때 주의할 사항]
딕셔너리에서 Key는 고유한 값이므로 중복되는 Key 값을 설정해 놓으면 하나를 제외한 나머지 것들이 모두 무시된다. 
-> 동일한 Key가 존재하면 어떤 Key에 해당하는 Value를 불러야 할 지 알 수 없기 때문
Key에는 리스트를 쓸 수 없다.(튜플은 사용 가능)
-> 리스트는 그 값이 변할 수 있기 때문

- Key 리스트 만들기(keys)
    a = {'name': 'pey', 'phone': '0119993323', 'birth': '1118'}
    a.keys()
    dict_keys(['name', 'phone', 'birth'])
    => 딕셔너리 a의 Key만을 모아서 dict_keys 객체를 돌려줌
    dict_keys 객체는 리스트를 사용하는 것과 차이가 없지만 리스트 고유의 append, insert, pop, removem sort 함수는 수행할 수 없음

    dict_keys 객체를 리스트로 변환  
        list(a.keys())
        ['name', 'phone', 'birth']

- Value 리스트 만들기(values)
    a.values()
    dict_values(['pey', '0119993323', '1118'])

    Key를 얻는 것과 마찬가지 방법으로 Value만 얻고 싶다면 values 함수를 사용하면 된다. 
    values 함수를 호출하면 dict_values 객체를 돌려준다.

- Key, Value 쌍 얻기(items)
    a.items()
    dict_items([('name', 'pey'), ('phone', '0119993323'), ('birth', '1118')])

    items 함수는 Key와 Value의 쌍을 튜플로 묶은 값을 dict_items 객체로 돌려준다. 
    dict_values 객체와 dict_items 객체 역시 dict_keys 객체와 마찬가지로 리스트를 사용하는 것과 동일하게 사용할 수 있다.

- Key: Value 쌍 모두 지우기(clear)
- Key로 Value얻기(get)
    a = {'name':'pey', 'phone':'0119993323', 'birth': '1118'}
    a.get('name')
    'pey'
    a.get('phone')
    '0119993323'

    딕셔너리 안에 찾으려는 Key 값이 없을 경우 미리 정해 둔 디폴트 값을 대신 가져오게 하고 싶을 때에는 get(x, '디폴트 값')을 사용하면 편리함
    a.get('foo','bar')
    'bar'

- 해당 Key가 딕셔너리 안에 있는지 조사하기(in)
    a = {'name':'pey', 'phone':'0119993323', 'birth': '1118'}
    'name' in a
        True
    'email' in a
        False


# 6. 집합 자료형
집합(set): 집합에 관련된 것을 쉽게 처리하기 위해 만든 자료형
집합 자료형은 set 키워드를 사용해 생성 가능
- s1 = set([1,2,3])

### 특징
- 중복을 허용하지 않는다.
- 순서가 없다.  ->  인덱싱으로 값을 얻을 수 없다. 
    만약 set 자료형에 저장된 값을 인덱싱으로 접근하려면 리스트나 튜플로 변환 후 수행
- 중복을 허용하지 않는 set의 특징은 자료형의 중복을 제거하기 위한 필터 역할로 종종 사용하기도 함

- 교집합 &  
    intersection() 함수를 사용해도 동일한 결과

- 합집합 | 
    union() 함수를 사용해도 동일한 결과

- 차집합 -
    difference 함수를 사용해도 동일한 결과

집합 자료형 관련 합수
- 값 1개 추가하기(add)
- 값 여러 개 추가하기(update)
- 특정 값 제거하기(remove)

# 7. 불 자료형
참(True)과 거짓(False)을 나타내는 자료형

- "python"	참
- ""	거짓
- [1, 2, 3]	참
- []	거짓
- ()	거짓
- {}	거짓
- 1	참
- 0	거짓
- None	거짓

# 8. 자료형의 값을 저장하는 공간, 변수
변수 이름 = 변수에 저장할 값
변수란? 객체를 가리키는 것
- id 함수: 변수가 가리키고 있는 객체의 주소 값을 돌려주는 파이썬 내장 함수
- 변수 복사 시 기존 변수 값을 수정하면 복사한 변수 값도 같이 변함(주소가 같기 때문)

변수 복사 시 기존 변수의 값을 가지고 오면서 다른 주소 값을 가지도록 하는 방법
1. [:] 이용
    ex) b = a[:]
2. copy 모듈 이용
    from copy import copy
    a = [1,2,3]
    b = copy(a) or b = a.copy()

변수를 만드는 여러가지 방법
1. a, b = ('python', 'life')
2. (a, b) = 'python', 'life'  
3. [a,b] = ['python', 'life']
4. a = b = 'python'