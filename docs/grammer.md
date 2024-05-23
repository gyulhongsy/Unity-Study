# C# 기초 문법
1. 기본 문법
2. 자료형과 변수
3. 조건문
4. 반복문
<br>

## 1. 기본 문법

### 주석
C#에서는 두 가지 주석 처리 방법을 제공합니다.
```
//한 줄 처리 주석입니다.

/*
여러줄 처리 주석입니다.
주석 안의 내용은 모두
코드 실행에 영향을 주지 않습니다.
*/
```
<br>

### 출력
C#에서는 콘솔에 출력하기 위해 `WriteLine()`메소드와 `Write()`메서드를 사용합니다.
```
Console.WriteLine("출력할 내용"); //내용 출력 후 자동으로 줄바꿈이 됩니다.
Console.Write("출력할 내용"); //내용 출력 후 줄바꿈이 되지 않습니다.
```
*추가로, 유니티의 로그 창에 출력하기 위해서는 아래의 코드를 사용합니다.
```
Debug.Log("유니티 로그창에 출력");
```
<br>

### 입력
- C#에서 사용자의 입력을 받을 때는 `ReadLing()`메서드를 사용합니다.
- ReadLine() 메서드는 문자열만 입력받으므로 숫자를 입력 받을 때는 자료형을 변경해주어야 합니다.
```
string input = Console.ReadLine();
Console.WriteLine("input: " + input);
```
- 실행결과
```
아무 것이나 입력
input: 아무 것이나 입력
```
<br>


## 2. 자료형과 변수

### 정수
- 3, 250, -57, 0등 소수점이 없는 숫자
- 사칙 연산자와 나머지 연산자를 사용하여 계산이 가능합니다.
- C#에서의  정수 자료형
  - **int**: 4바이트의 정수
  - **long**: 8바이트의 정수
- 정수 변수 생성과 출력
```
int a = 273;
int b = 52;

Console.WriteLine(a);
Console.WriteLine(b);
Console.WriteLine(a + b);
Console.WriteLine(a % b);
```
- 실행 결과
```
273
52
325
13
```
    
### 실수
- 소숫점이 들어간 숫자
- 정수와 마친가지로 사칙 연산자와를 사용하여 계산이 가능합니다.
- 나머지 연산자도 사용 가능하나 결과를 예측하기 어려워 추천하지 않습니다.
- C#에서의 실수 자료형
  - **float**: 4바이트의 실수
  - **double**: 8바이트의 실수
- 실수 변수 생성과 출력
```
double a = 52.273;
doubld b = 103.32

Console.WriteLine(a);
Console.WriteLine(b);
Console.WriteLine(a + b);
```
- 실행 결과
```
52.273
103.32
155.593
```

### 문자
- 글자 하나를 나타내는 자료형
- 작은 따옴표(')를 사용하여 만듭니다.
- C#은 알파벳 뿐만 아니라 한국어, 중국어, 일본어, 태국어, 아랍어 등의 문자를 모두 표현할 수 있습니다.
- C#에서의 문자 자료형
  - **char**: 문자 (2바이트)
- 문자 변수 생성과 출력
```
char a = 'A'

Console.WriteLine(a);
Console.WriteLine('가');
```
- 실행 결과
```
A
가
```

### 문자열
- 문자의 집합
- 큰 따옴표(")를 사용하여 생성합니다.
- 이스케이프 문자를 사용하여 문자열 내에서 따옴표를 작성하거나 여러 기능을 수행할 수 있습니다.
- C#에서의 문자열 자료형: **string**
- 자주 사용하는 이스케이프 문자의 종류
  - `\t`: 수평 탭
  - `\n`: 행 바꿈
  - `\\`: 역슬래시 입력
  - `\"`: 큰 따옴표 입력
- 문자열 변수 생성과 출력
```
string message = "hello world!";

Console.WriteLine(message);
Console.WriteLine("안녕하세요");
Console.WriteLine("안녕\t하세요");
Console.WriteLine("안녕\n하세요");
Console.WriteLine("\"안녕하세요\"");
```
- 실행 결과
```
hello world!
안녕하세요
안녕     하세요
안녕
하세요
"안녕하세요"
```
- 문자열 연결 연산자(+)로 **문자열을 연결**할 수 있습니다.
```
Console.WriteLine("안녕" + "하세요");
Console.WriteLine("가나다라" + "마바사" + "아자차카" + "타파하");
```
- 실행 결과
```
안녕하세요
가나다라마바사아자차카타파하
```
- "안녕하세요"라는 문자열의 0번째, 1번째, 3번째에 있는 **문자를 선택**하여 출력할 수 있습니다.
```
Console.WriteLine("안녕하세요"[0]);
Console.WriteLine("안녕하세요"[1]);
Console.WriteLine("안녕하세요"[3]);
```
- 실행 결과
```
안
녕
세
```

### 불
- 불은 참과 거짓을 표현할 때에 사용합니다.
- `true`와 `false`라는 두 가지 값 밖에 없습니다.
- 크기를 비교하는 비교 연산자로 참과 거짓을 만듭니다.
- 불 끼리는 논리 연산자를 사용할 수 없습니다.
- C#에서의 불 자료형: **bool**
- 불 변수의 생성과 출력
```
bool one = 10 < 0;
bool other = 100 > 20;

Console.WriteLine(one);
Console.WriteLine(other);
```
- 실행결과
```
False
True
```

### 자료형 검사
- `GetType()`: 해당 변수의 자료형을 추출
- GetType() 메서드는 변수뿐만 아니라 숫자 또는 문자열에 직접적으로 사용할 수 있습니다.
- 사용 예
```
long num = 522731033265;
double doub = 52.273;
char ch = '글';

Console.WriteLine((273).GetType());
Console.WriteLine(num.GetType());
Console.WriteLine((52.273F).GetType());
Console.WriteLine(doub.GetType());
Console.WriteLine(ch.GetType());
Console.WriteLine(("문자열").GetType());
```
- 실행결과
```
System.Int32
System.Int64
System.Single
System.Double
System.Char
System.String
```

### var 키워드
- C#은 `var` 키워드로 변수의 자료형을 자동으로 지정할 수 있습니다.
- 한 번 지정된 자료형은 계속 유지됩니다.
- var 키워드를 사용하려면 다음과 같은 2가지 조건을 만족해야 합니다.
  - 지역 변수로 선언하는 경우 (메서드 내부의 변수)
  - 변수를 선언과 동시에 초기화하는 경우
- long 자료형, float 자료형으로 선언하고 싶다면 숫자 뒤에 L또는 F를 붙여 명시적으로 알려줘야 합니다.
- var 키워드의 사용
```
static void Main(string[] args) //메인 메서드 내부에서도 사용 가능
{
    var numA = 100; //int 자료형
    var numB = 100L; //long 자료형
    var numC = 100.0; //double 자료형
    var numD = 100.0F; //float 자료형
    var str = "문자열";
}
```
<br>


## 3. 조건문

### if 조건문
`불_표현식`이 true면 중괄호 안의 문장을 실행하고 false면 문장을 무시합니다.
문장이 한 행이라면 중괄호를 생략할 수 있습니다.
- if 조건문
```
if (불_표현식)
{
    문장;
}
```
- 
