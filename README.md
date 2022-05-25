# Technical_interview
기술면접 대비를 위한 IT 기초 정리입니다.

기술면접 대비할려고 만든 프로젝트입니다.

여기에 기술면접 대비 내용을 기술하십시오.

# ➀ 프로그램 기본 개념

![image](https://user-images.githubusercontent.com/93306939/169712506-da2d7ff2-0398-4549-ae7b-7933dae59204.png)

#### <b>1. 저급 프로그래밍 언어（低級 프로그래밍 言語）or 로우 레벨 프로그래밍 언어(low-level programming language)</b>

저급언어
- 컴퓨터가 이해하기 쉬운 이진법으로 이루어진 언어이다
- 컴퓨터가 바로 이행 할 수 있지만 가독성 및 생산성이 낮다.
- 프로그램 속도가 빠르다.　
- 프로그램 크기 또한 고급언어 보다 작다.
- 저급언어에는 기계어와 어셈블리어 등이 있다.

### <b>1.1 기계어  </b>  
-기계어란 cpu가 직접 해독하고 실행할 수 있는 비트 단위로 쓰인 컴퓨터 언어를 통틀어 일컫는다.  
-기계어는 프로그램을 나타내는 가장 낮은 단계의 개념이다.  

### <b>1.2 기계어의 특징  </b>  
-기계어는 대부분 어셈블리어를 거쳐 짜여 지게 된다.  
-어셈블리어가 아직 만들어 지기 전에는 기계어를 직접 입력하여 프로그램을 작성하기도 했다.  
-컴퓨터가 알아들을 수 있는 유일한 프로그래밍 언어라고도 할 수 있다.  


 니모닉?
 
  참조할 어드레스 위치, 실행 명령(연산코드), 저장 어드레스 위치 등 2진수로 작성된 명령어 명세를 약칭으로 표현한것

![image](https://user-images.githubusercontent.com/93306939/169712693-7b2864f3-08aa-4db2-a581-79a603f1b6a1.png)


ex) 0000101 001 010 011(0A53H) - 레지스터 감산 <br/>
0000101 - 감산연산 SUB <br/>
001 - 어드레스 위치 R1 <br/>
010 - 어드레스 위치 R2 <br/>
011 - 연산 저장위치 R3 <br/>
같은 느낌

---------------------------------------------------------------------------------------------


### <b>1.3 어셈블리어  </b>  

-어셈블리어란 기계어를 사람이 이해하기 쉬운 기호와 1 : 1로 대응시켜 기호화한 프로그램 언어이다.  
-기호 언어라고도 부른다.  


### <b>1.4 어셈블리어의 특징  </b>

-저급언어 중에서도 밑바닥의 언어이다.  
-기계와 바로 통신이 가능하다. 그래서 빠르게 기계를 제어 할 수 있다.  
-최소한의 명령으로 이루어진 언어로 이진수 패턴을 사용하는 기계어와 비슷해서 명령을 내릴 때 매우 세밀하게 명령을 내린다.  
-하드웨어를 사실상 제어하는 형태이기 때문에 하드웨어의 구조를 따라서 프로그램을 달리 햐야 한다.  
-이러한 특징 때문에 어셈블리어는 배우기도 까다롭고 프로그래밍 하기도 어렵다.  
  
![image](https://user-images.githubusercontent.com/93306939/169713080-36aeec3f-8be7-4b79-a92b-848bb63bf2db.png)

좀 더 쉽게 표현  
위의 기계어 연산을 어셈블리어로 표현할 경우,  
ex) SUB R1,R2,R3 - 레지스터 감산  
어드레스 R1, R2에 값을 감산하여 R3에 저장하여라  


### <b>1.5 어셈블리어의 장단점  </b>  

장점  
- 프로그램의 실행 속도가 매우 빠르다. (기계에게 바로 명령을 내리기 때문에)  
- 프로그램의 크기가 매우 작다. (최소한의 명령을 사용하기 때문에)  
- 어떤 프로그램이라도 만들 수 있다. (하드웨어를 직접 제어 할 수 있기 때문에 어떠한 명령도 수행 할 수 있다.)  

단점  
- 배우기 힘들다. ( 고급언어인 c나 java등에서 코딩을 할 때에는 하드웨어적 지식이 필요 없지만, 어셈블리어는 하드웨어 지식이 뛰어나야 하기 때문에)  
- 큰 프로그램을 만들기 힘들다. (세밀한 제어가 필요하기 때문에 클 프로그램을 만들기에는 힘들다.)  
- 프로그램을 짤 때 시간이 오래 걸리고 디버그도 어렵다. (에러를 찾을 때 직접 찾아야 해서 어렵다.)  

 ### <b>1.6 어셈블리어의 용도  </b>  
-하드웨어 디바이스 드라이버  
 -드라이버라 불리는 하드웨어를 조절하는 프로그램을 만들 때 거의 대부분어셈블리어로 작성한다.  
 -하드웨어 제어는 드라이버 파일이 작고 실행 속도는 빨라야 함.  

일반 프로그램의 기능 최적화  
-게임이나 프로그램을 만들 때 100% 고급언어를 이용한다면. 속도가 느려 제 역할을 하지 못한다.  
 -속도가 필요하거나 하드웨어를 정밀하게 제어 할 때에는 어셈블리어를 이용한다.  
 -어셈블리 프로그램을 고급언어로 만든 프로그램과 링크시켜서 사용하는 것이 보편적이다.  

---------------------------------------------------------------------------------------------

<b>2 고급 프로그래밍 언어 또는 하이 레벨 프로그래밍 언어(high-level programming language)  
  사람이 이해하기 쉽게 작성된 프로그래밍 언어  </b>
  
  ### JAVA기준으로 설명  
  
  ![image](https://user-images.githubusercontent.com/93306939/169713638-2048897c-78d6-4f29-a2e5-3b1031a24102.png)

프로그래머 -> JAVA로 프로그래밍 -> JAVA 컴파일러가 소스 파일을 가상 기계어 파일인  
JAVA 클래스 파일로 만듬 (JAVA 바이트 코드로 변역) -> JAVA 바이트 코드를 JVM이 읽고 실행  

JAVA는 이러한 특징때문에 "플랫폼 독립적"임 JVM에 의해 읽고 실행되기 때문에  
OS에 관계없이 일관된 동작결과를 기대 가능.  
(이리한 방식때문에 JAVA는 컴파일러와 인터프리터의 특징을 모두 가지고 있음)  

//  

 컴파일러 : 소스코드 전문 -> 기계어로 번역 -> 프로그램 실행  
 장점 : 실행속도 빠름 // 단점 : 한번에 번역하므로 비교적 많은 메모리 요구  
 
 인터프리터 : 인터프리터 언어는 별도의 번역과정 없이 개발자가 작성한 소스코드를  
 실행 시점에 명령어를 실행 (한 줄씩 읽고 한 줄씩 실행)  
 장점 : 빌드 과정 없이 바로 실행가능, 메모리 적개 필요 // 단점 : 실행속도 느림  

+ C같은 경우 바로 기계어로 컴파일러 하므로 HW 기종에 맞게 컴파일 해야함.  
++ python의 경우도 플랫폼 독립적임  

//  

한마디로 사람이 이해할수 있는 고급 언어를 컴퓨터 언어인 기계어로 번역하는 과정을 거쳐 컴퓨터 동작을 수생 가능하게 해주는것  
즉, 사람이 이해하기 쉽게 작성된 프로그래밍 언어  


---------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------

# ➁ JAVA 기초

### <b>2.1 JAVA API의 이해.</b>  

프로그래밍 언어가 제공하는 기능을 개발자가 만든 프로그램 내에서  
쉽게 제어할 수 있게 만든 클래스들의 묶음  
(Application Programming Interface)  

패키지 단위로 묶여있음  
API Document를 통해 사용법을 제공  

---------------------------------------------------------------------------------------------

### <b>★2.2 자바의 메모리 구조  </b>  

Class영역 | Stack영역 | Heap영역 | Nailve method영역 | PC Register영역  <br/>
<br/>
![image](https://user-images.githubusercontent.com/93306939/169925587-47d01c18-6dcf-417a-8687-f526c5637851.png)
<br/>

**Class영역(Method영역)**  
 - JVM에서 읽어들인 클래스와 인터페이스에 대한 런타임 상수 풀, 메서드와 필드 Static 변수, 메서드 바이트 코드 등을 보관  
 
 
**Stack영역**  
 - 선입후출(FILO) 구조, 메서드 호출 시 생선되는 스레드 수행정보를 기록하는 Frame저장,메서드 정보, 지역변수, 매개변수, 연산 중 발생하는 임시 데이터 저장  


**Heap영역**  
 - 프로그램 상에서 데이터를 저장하기 위해 런타임 시 동적으로 할당하여 사용하는 메모리 영역 New 연산자를 통해 생생한 객체, 또는 인스턴스와 배열을 저장 (JVM이 관리)  


**Nailve method영역**  
 - 자바 외 언어로 작성된 네이티브 코드를 위한 메모리 C/C+등의 코드를 수행하기 위한 스택 native 메서드의 매개변수, 지역변수 등을 바이트코드로 저장  


**PC Register영역**  
 - 현재 실행 중인 JVM 주소를 가지고 있다. CPU 명령어 즉 lnstruction을 수행한다. CPU lnstruction을 수행하는 동안 필요한 정보를 CPU내 기억장치인 레지스터에 저장, 연산 및 결과값을 메모리에 전달하기 전 CUP내 기억장치임.  

---------------------------------------------------------------------------------------------

### <b>2.3 가비지 컬렉터(GC)는 언제 작동 되는가  </b>  

GC는 다음 방법 중 하나를 사용하여 요청할 수 있습니다.  

1) System.gc () : Java의 System 클래스는 가비지 콜렉터를 실행하기 위해 JVM을 요청할 수있는 정적 메소드 gc ()를 제공합니다.  
2) Runtime.getRuntime (). gc () : System.gc ()와 마찬가지로 'Runtime class'의 gc () 메서드를 사용하여 가비지 수집기를 실행하도록 JVM을 요청할 수도 있습니다.  

**가비지 컬렉터?**  
-쓰레기 수집(garbage collection 가비지 컬렉션[*], GC)은 메모리 관리 기법 중의 하나로, 프로그램이 동적으로 할당했던 메모리 영역 중에서 필요없게 된 영역을 해제하는 기능이다.  
쓰레기 수집은 동적 할당된 메모리 영역 가운데 더 이상 사용할 수 없게 된 영역을 탐지하여 자동으로 해제하는 기법이다. 더 이상 사용할 수 없게 된 영역이란, 어떤 변수도 가리키지 않게 된 영역을 의미한다.  
자바, C#, 그리고 일부 스크립트 언어들은 처음부터 쓰레기 수집 기법을 염두에 두고 설계되어, 언어 정의에 쓰레기 수집이 포함되어 있다.  

---------------------------------------------------------------------------------------------

### <b>2.4 자바의 자료형에 대해 설명하시오.  </b>  

![image](https://user-images.githubusercontent.com/93306939/169722024-c10ae161-3980-4596-b6e4-4b12070ab51a.png)
![image](https://user-images.githubusercontent.com/93306939/169722039-02ba7bc6-a0c3-4e13-a420-d40fe2869ddb.png)

---------------------------------------------------------------------------------------------

### <b>2.5 for문과 while문의 차이에 대해 설명하시오</b>  

 형식에서의 차이점뿐만 아니라  
쓰는 때가 편의에 따라 조금 다르다.  

while문: 조건이 true인 동안 반복 실행되고,  
false가 되는 순간 빠져나온다.  

<b>→조건이 트루인동안</b>  

for문: 주어진 조건동안  
'코드 실행 후 작업' 처리를 반복한다.  
while문과 다르게 초기값이 주어지면,   
조건을 만족할 때까지는 실행한다.  

<b>→그냥 조건동안</b>  
 
 for문과 while문 차이점(형식)
 
<b> for문: 1문장 안에서만 생존</b>  
(초기식/조건식/증감연산이 포함)  
→ 횟수가 정해졌을 때 사용   

<b>while: while문 바깥에서도 생존</b>   
1. while문 수행 전 초기화   
2. while문 내에서는 조건문   
3. while문 밑에서 증감연산 시도   
→ 특정 조건에서 종료될 때 사용   

**★결론★**
1. for문:
-반복횟수가 정해져 있다.
-배열과 함께 많이 쓴다.

2. while문:
-무한루프일 경우에 쓴다.
-특정 조건에 만족해야할 때까지 반복한다. 

---------------------------------------------------------------------------------------------

### <b>2.6 접근 지정자의 접근 범위에 대해 설명하시오.</b>  
## access modifier

접근 허용 가능 범위 순서는 다음과 같습니다. 접근 범위는 왼쪽부터 큽니다.  

**public > protected > default > private**  

- public : 접근을 제한이 없음  
- protected : 동일한 패키지 내에 존재하거나 파생클래스에서만 접근 가능  
- default : 아무런 접근 제한자를 명시하지 않으면 default 값이 되며, 동일한 패키지 내에서만 접근이 가능  
- private : 자기 자신의 클래스 내에서만 접근이 가능  

![image](https://user-images.githubusercontent.com/93306939/169728007-8db0dcac-6a8f-4736-9065-0684beace610.png)


---------------------------------------------------------------------------------------------
### <b>2.7 String과 StringBuffer의 차이에 대해 설명하시오</b>

 - String 클래스 문자열과 관련된 메서드를 제공하며, 객체 값으 변경 할 수 없는 immutable 객체이다. 즉, String 클래스의 메서드를 사용하여 문자열을 변경할 경우 원본이 되는 문자열은 변경 되지 않는다.  

 - StringBuffer 클래스도 문자열을 다루는 클래스이며, 객체 값을 변경 할 수 있는 mutable 객체이다. 즉, 문자열의 변경이 빈번하게 일어날 때 사용하면 좋다. (Thread Safe 객체 <-> StringBuilder)

---------------------------------------------------------------------------------------------

 ### <b>2.8 Static에 대해 설명하세요 </b>

- static keyword는 변수나 메서드 그리고 inner class 앞에 modifier 형태로 사용이 된다.  
- static을 사용해서 변수를 선언하게 되면 그 이름이 "클래스 변수"로 불리게 된다.
- static으로 선언된 변수는 객체 생성시 마다 초기화되지 않고, 모든 객체에 의해 공유되어 진다.
- static으로 선언된 변수나 메서드는 객체를 생성하지 않고 클래스의 이름으로 호출가능하다.
     [클래스 이름][변수], [클래스 이름][메서드]
- static 메서드 안에서는 static하지 않은 변수나 메서드를 호출할수 없다.

+ 정적(static)은 고정된이란 의미를 가지고 있습니다.  정적필드와 정적 메소드라고도 하며 이 둘을 합쳐 정적 멤버라고 합니다.정적 필드와 정적 메소드는 객체(인스턴스)에 소속된 멤버가 아니라 클래스에 고정된 멤버입니다. 그렇기에 클래스 로더가 클래스를 로딩해서 메소드 메모리 영역에 적재할때 클래스별로 관리됩니다. 따라서 클래스의 로딩이 끝나는 즉시 바로 사용할 수 있습니다.

![image](https://user-images.githubusercontent.com/93306939/169737815-faf5a22f-d85e-45c1-8ae9-56c7efa3f763.png)

Static 키워드를 통해 생성된 정적멤버들은 Heap영역이 아닌 Static영역에 할당됩니다. Static 영역에 할당된 메모리는 모든 객체가 공유하여 하나의 멤버를 어디서든지 참조할 수 있는 장점을 가지지만 Garbage Collector의 관리 영역 밖에 존재하기에 Static영역에 있는 멤버들은 프로그램의 종료시까지 메모리가 할당된 채로 존재하게 됩니다. 그렇기에 Static을 너무 남발하게 되면 만들고자 하는 시스템 성능에 악영향을 줄 수 있습니다.

---------------------------------------------------------------------------------------------

### <b>2.9 final에 대해 설명하세요</b>

- final keyword는 자바에서 클래스, 메서드, 변수 등 모든 요소의 앞에 modifier로 사용된다.
- 변수에 final을 쓰면 상수가 되고, 메서드에 final을 쓰면 오버라이딩이 안되고, 클래스에 final을 쓰면 상속이 안된다.
- 상수 선언 방법 [접근제한자] static final 식별자 이름 = 값;

+ 즉,  final 키워드는 어떤 곳에 사용되냐에 따라 다른 의미를 가지지만
+ final 키워드를 붙이면 무언가를 제한한다는 의미를 가지는 것은 공통적이 성격입니다.


---------------------------------------------------------------------------------------------

### <b>2.10 List, Set, Map에 대해 설명하세요</b>  

![image](https://user-images.githubusercontent.com/93306939/169738614-d815c5ef-1648-476f-a86b-ce1da03627da.png)

**List**  
 순서가 있고 중복을 허용합니다.  
 인덱스로 원소에 접근이 가능합니다.  
 크기가 가변적입니다.  

**Map**  
 Key와 Value의 한쌍으로 이루어지는 데이터의 집합.  
 Key에 대한 중복이 없으며 순서를 보장하지 않습니다.  
 뛰어난 검색 속도를 가집니다.  
 인덱스가 따로 존재하지 않기 때문에 iterator를 사용합니다.  

**Set**  
 데이터의 집합이며 순서가 없고 중복된 데이터를 허용하지 않습니다.  
 중복되지 않은 데이터를 구할 때 유용합니다.  
 빠른 검색 속도를 가집니다.  
 인덱스가 따로 존재하지 않기 때문에 iterator를 사용합니다.  
  
#### 요약  
- List는 기본적으로 데이터들이 순서대로 저장되며 중복을 허용한다.
- Map은 순서가 보장되지 않고 Key값의 중복은 허용하지 않지만 Value값의 중복은 허용된다.
- Set은 순서가 보장되지 않고 데이터들의 중복을 허용하지 않는다.

---------------------------------------------------------------------------------------------

### <b>2.11 제네릭(Generic)에 대해 설명하세오</b>  

 - 제네릭은 클래스나 인터페이스와 같은 타입을 매게변수로 지정하여 객체를 생성할 때 타입을 지정해주는것을 말한다.
 - 제네릭을 사용하는 이유는 타입에 안정한 컬렉션을 사용하기 위해 사용한다.
 
 + 제네릭 타입 생성
  FruitBox<타입 매개변수> box = new FruitBox<타입 매개변수>()

---------------------------------------------------------------------------------------------

### <b>2.12 래퍼 클래스 (Wraper Class)에 대해 설명하세요.</b>

 - Wrapper 클래스란 자바의 기본 자료형(Primitive Type)을 객체의 형식으로 표현하는 것을 말한다.
 
![image](https://user-images.githubusercontent.com/93306939/169746969-11058ce8-9a3f-4d9f-9b8d-3e030f85cd02.png)

---------------------------------------------------------------------------------------------

### <b>2.13 List와 배열의 차이에 대해 설명하세요</b>
 
 - List는 이기종 간의 데이터 집합이며 배열은 동일 데이터 타입의 집합이다.
 - List는 저장 공간의 길이가 가변형이며, 배열은 고정형이다.

---------------------------------------------------------------------------------------------

### <b>2.14 token이란 무엇인가?</b>
 
 - 토큰은 여러 의미로 사용될 수 있는데, 일반적으로 프로그램 언어에서는 문자열을 구분할 수 있는 단위라는 의미로 사용 됨
 
---------------------------------------------------------------------------------------------
 
### <b>2.15 class와 instance의 차이에 대해 설명하세요.</b>
 
  - class는 객체를 만들기 위한 틀(template), 또는 설계도(blueprint)이며 객체를 만들어 내기 위한 속성(변수)과 행동방식(메서드)을 포함하고 있다.
 
 - class는 참조형 데이터 타입이다.
 
 - insance는 class를 통해 구체적인 데이터를 전달받아 생성이라는 작업을 통해 메모리에 적재된 결과물을 말한다.
 
 + class는 붕어빵 틀 / instance는 붕어빵 / 안에 팥을 넣을지 슈크림을 넣을지는 내가 선택
![image](https://user-images.githubusercontent.com/93306939/169754305-e1a1ec4b-44f8-4c36-b20f-b7f1054715c6.png)
 
---------------------------------------------------------------------------------------------
 
### <b>2.16 객체 지향 프로그래밍(OOP)에 대해 설명하세요.</b>  
 
 - 객체지향 프로그래밍(object-oriented programming)이란 속성과 행동방식을 가진 객체(Object)들이 있고,  
 객체끼리 서로 상호 작용 하며 실행되도록 소프트웨어를 만드는 방식을 말한다.  
 
 - 객체 지향 프로그래밍은 컴퓨터 프로그래밍 패러다임 중 하나로, 프로그래밍에서 필요한 데이터를 추상화시켜 상태와 행위를 가진 객체를 만들고 그 객체들 간의 유기적인 상호작용을 통해 로직을 구성하는 프로그래밍 방법이다.  
<br/>
 
**장점**  
- 코드 재사용이 용이
  - 남이 만든 클래스를 가져와서 이용할 수 있고 상속을 통해 확장해서 사용할 수 있다.
- 유지보수가 쉬움
  - 절차 지향 프로그래밍에서는 코드를 수정해야할 때 일일이 찾아 수정해야하는 반면 객체 지향 프로그래밍에서는 수정해야 할 부분이 클래스 내부에 멤버 변수혹은 메서드로 존재하기 때문에 해당 부분만 수정하면 된다. 
- 대형 프로젝트에 적합
   - 클래스 단위로 모듈화시켜서 개발할 수 있으므로 대형 프로젝트처럼 여러 명, 여러 회사에서 프로젝트를 개발할 때 업무 분담하기 쉽다.

**단점**  
- 처리 속도가 상대적으로 느림
- 객체가 많으면 용량이 커질 수 있음
- 설계시 많은 시간과 노력이 필요

 
---------------------------------------------------------------------------------------------

### <b> 2.17 객체(Object)</b>

- 실제 세계에 존재하는 상태와 행동방식을 가진 모든 것
- 모든 객체는 속성과 행동방식으로 표현될 수 있다.
 
 ![image](https://user-images.githubusercontent.com/93306939/169753407-df1ace4a-273b-49da-aa3a-652cb1ae5b6c.png)

 위의 에어맨은 다음과 같은 속성과 메서드(행동방식)을 가짐  

현실세계　/　프로그램세계  
 속성 　 -> 　필드(변수)  
행동방식 ->　메서드(함수)  
 
 객체(object)는 사전적인 정의로 실제 존재하는 것을 말한다. 객체지향 이론에서는 사물과 같은 유형적인 것뿐만 아니라, 개념이나 논리와 같은 무형적인 것들도 객체로 간주한다. 프로그래밍에서의 객체는 클래스에 정의된 내용대로 메모리에 생성된 것을 뜻한다.[1] 일반적으로 객체는 다수의 속성과 기능을 가지고 있으며, 객체가 가지고 있는 속성과 그 기능을 객체의 멤버라고 한다.
 
---------------------------------------------------------------------------------------------
 
 ### <b> 2.18 은닉(Encapsulation)에 대해 설명하세요.</b>

 캡슐회는 만일의 상황(타인이 외부에서 조작)을 대비해서 외부에서 특정 속성이나 메서드를 시용자가 사용할 수 없도록 숨겨놓은 것입니다.

- 클래스 내부 구현을 숨기고 사용자에게는 인터페이스 만을 제공해 주는 것
- 데이터를 신뢰성 있게 관리하고 오류를 최소화할 수 있게 된다.

 **추가**
- 객체의 필드(속성), 메소드를 하나로 묶고, 실제 구현 내용을 외부에 감추는 것을 말한다.
- 외부 객체는 객체 내부의 구조를 얻지 못하며 객체가 노출해서 제공하는 필드와 메소드만 이용할 수 있다.
- 필드와 메소드를 캡슐화하여 보호하는 이유는 외부의 잘못된 사용으로 인해 객체가 손상되지 않도록 하는데 있다.
- 자바 언어는 캡슐화된 멤버를 노출시킬 것인지 숨길 것인지를 결정하기 위해 접근 제한자(Access Modifier)를 사용한다.  
 p.s 접근제한자는 [2.6](#access-modifier) 접근제한자 참고
 
 캡슐화라고도 한다.
 
---------------------------------------------------------------------------------------------

 ### <b> 2.19 lnheritance(상속)에 대해 설명하세요.</b>

 ![image](https://user-images.githubusercontent.com/93306939/169769039-77ed4fe4-5066-4e6e-9e17-d57d1075d0d6.png)

 - 클래스가 다른 클래스의 속성과 행동방식을 물려받아 구현하는 것
 - 상속을 받아 새로 만들어지는 클래스는 자식 클래스 (sub class)가 되고 멤버들을 상속해주는 클래스를 부모 클래스(super class)라고 한다
 - 객체지향 프로그래밍에서 코드의 재사용성과 확장성을 높임으로써 프로그램의 유지보수를 좀 더 쉽게 해준다.
  
 **상속의 대상**  
 자식 클래스가 부모 클래스로부터 상속을 받게 되면 부모 클래스의 필드와 메서드를 물려받게 된다.  
 단, 접근제어자가 private을 갖는 필드나 메소드는 상속이 불가하고, 패키지가 다를 경우 접근제어자가 default인 경우도 상속이 불가하다.  

 **상속의 장점**  
 상속의 장점은 처음에 설명했던 것과 큰 차이가 없다. 중복된 코드를 줄일 수 있고,  
 유지 보수가 편리하며, 통일성이 있고 다형성을 구현할 수 있다.  

**상속의 방법(선언) - extends**  
 상속을 받는 방법은 간단하다. 상속받을 자식 클래스 뒤에 extends 키워드를 사용하고 부모 클래스를 적어주면 된다.  
 
![image](https://user-images.githubusercontent.com/93306939/169769222-35289bd8-865d-45cd-b56b-84b3813eb835.png)
 
 그리고 자바에서는 자식 클래스가 여러 부모로부터 다중 상속을 받는 것은 불가능하다.  
 즉, 1개의 부모 클래스로부터의 단일 상속만 허용된다.  하지만 부모 클래스는 여러 개의 자식 클래스에게 상속이 가능하다.  

---------------------------------------------------------------------------------------------
 
### <b> 2.20 Polymorpgism(다형성)에 대해 설명하세요</b>  

![image](https://user-images.githubusercontent.com/93306939/169769752-51c25428-59b0-41b0-accf-4a98108cb11e.png)
다형성(polymorphism)이란 하나의 객체가 여러 가지 타입을 가질 수 있는 것을 의미합니다.  

 - 다형성이란 '많은 형태를 가지고 있다.' 라는 뜻  
 - 상속 관계에서 같은 기능이 여러 형태로 존재하는 것을 의미  
 - 메서드 오버로딩(method overloading)  
 - 메서드 오버라이딩(method overriding)  
 - 다형적 변수(polymorphic variable)


```
EX )  

class Parent { ... }  
class Child extends Parent { ... }  

...

Parent pa = new Parent(); // 허용  
Child ch = new Child();   // 허용  
Parent pc = new Child();  // 허용  
Child cp = new Parent();  // 오류 발생.  
```

---------------------------------------------------------------------------------------------

**오버로딩(Overloading)**  

구체적으로 메서드 오버로딩을 예시로 들면,  
자바의 PrintStream.class에 정의되어 있는 println이라는 함수는 다음과 같이 매개변수만  
다른 여러 개의 메소드가 정의되어 있다. 매개변수로 배열을 넣을 때, 문자열을 넣을 때, 그리고 객체를 넣을 때  
모두 println이라는 메소드 시그니처를 호출하여 원하는 내용을 출력하는 기능을 수행한다.  

```
public class PrintStream {  
	 
	public void println() {  
		this.newLine();  
	}  
  
	public void println(boolean x) {  
  		synchronized(this) {  
      	this.print(x);  
      	this.newLine();  
  		}  
	}  
  
	public void println(char x) {  
    	synchronized(this) {  
        	this.print(x);  
        	this.newLine();  
    	}  
	}  
  
	public void println(int x) {  
    	synchronized(this) {  
        	this.print(x);  
        	this.newLine();  
    	}  
	}  
	
}  
```

오버로딩은 여러 종류의 타입을 받아들여 결국엔 같은 기능을 하도록 만들기 위한 작업이다.  
이 역시 메소드를 동적으로 호출할 수 있으니 다형성이라고 할 수 있다.  
하지만 메소드를 오버로딩하는 경우 요구사항이 변경되었을 때 모든 메소드에서  
수정이 수반되므로 필요한 경우에만 적절히 고려하여 사용하는 것이 좋을 듯 하다.  
  
---------------------------------------------------------------------------------------------
  
**오버라이딩(Overriding)**  

오버로딩과 이름이 비슷해 헷갈릴수도 있다.  
오버라이딩은 상위 클래스의 메서드를 하위 클래스에서 재정의하는 것을 말한다.  
따라서 여기서는 상속의 개념이 추가된다.  
아래 예시로 보인 추상 클래스 Figure에는 하위 클래스에서 오버라이드 해야 할 메소드가 정의되어 있다.  

```  
public abstract class Figure {  
    protected int dot;  
    protected int area;  
  
    public Figure(final int dot, final int area) {  
        this.dot = dot;  
        this.area = area;  
    }  
  
    public abstract void display();  

	  // getter  
}  
```

Figure을 상속받은 하위 클래스인 Triangle 객체는 해당 객체에 맞는 기능을 구현한다.  

```
public class Triangle extends Figure {  
    public Triangle(final int dot, final int area) {  
        super(dot, area);  
    }  
  
    @Override  
    public void display() {  
        System.out.printf("넓이가 %d인 삼각형입니다.", area);  
    }  
}  
```

만약 사각형 객체를 추가하고 싶다면,  
같은 방식으로 Figure을 상속받되 메소드 부분에서 사각형에 맞는 display 메소드를 구현해주면 된다.  
이렇게 하면 추후 도형 객체가 추가되더라도 도형 객체가 실제로 사용되는 비즈니스 로직의 변경을 최소화할 수 있다.  

```
public static void main(String[] args) {  
    Figure figure = new Triangle(3, 10); // 도형 객체 추가 또는 변경 시 이 부분만 수정  
  
    for (int i = 0; i < figure.getDot(); i++) {  
        figure.display();  
    }  
}  
```


만약 여기서 다형성을 사용하지 않고 도형 객체를 추가하는 로직을 생각해 본다면  
아마 다음과 같이 if-else분기가 늘어나게 될 것이다.  
도형이 2개 밖에 없는데도 벌써 코드양 차이가 보이는가?  

``` 
public static void main1(String[] args) {  
    int dot = SCANNER.nextInt();  

    if (dot == 3) {  
        Triangle triangle = new Triangle(3, 10);  
        for (int i = 0; i < triangle.getDot(); i++) {  
            triangle.display();  
        }  
    } else if(dot == 4) {  
        Rectangle rectangle = new Rectangle(4, 20);  
        for (int i = 0; i < rectangle.getDot(); i++) {  
            rectangle.display();  
        }  
    }  

}  
```

여기까지 오버라이드 방식으로 다형성을 구현하는 방법을 살펴보았다.  
예시에서는 추상클래스를 사용했지만, 인터페이스도 구현의 정도만 차이가 있을 뿐 같은 사용 방식은 같다.  
오버라이드 다형성 방식을 잘 활용하면, 기능의 확장과 객체의 수정에 유연한 구조를 가져갈 수 있다.  

![image](https://user-images.githubusercontent.com/93306939/169774952-a115b143-fcf1-4063-9daa-e22ce452385c.png)

---------------------------------------------------------------------------------------------

### <b> 2.21 추상 클래스(Abstract Class)에 대해 설명하세요.</b>
 
 - 클래스 내에 일부 메서드가 구현되지 않고 선언부만 가진 형태의 메서드를 포함한 클래스
 - 구현되지 않은 메서드를 추상 메서드라고 부른다.
 - 추상 클래스는 new 키워드를 이용해서 객체를 생성할 수 없다.
 - 추상 클래스를 상속받는 클래스는 반드시 추상 클래스의 모든 추상 메서드를 오버라이딩 해야 된다.
 - 추상 메서드가 없어도 추상 클래스로 선언할 수 있다.

예시로 익숙한 실생활의 물건을 대상으로 추상화 과정을 실습해 보자.  
문방구 관리 프로그램을 작성한다면 문구점에서 파는 제품을 클래스로 표현해야 한다.  
각종 문구류의 특성을 파악하고 업무를 분석하여 다음과 같은 클래스를 만들었다.  

![image](https://user-images.githubusercontent.com/93306939/169777297-3226e98f-8769-4ea8-a035-88ba3b35ffb0.png)

이렇게 클래스로 만들어 놓고 보니 제품마다 중복되는 속성이 많다.  
모든 제품은 모델명이 있고 제조사와 가격에 대한 정보가 있다. 예를 들어 모나미 153 볼펜 500원짜리라는 식이다.  
모든 클래스가 이 속성을 개별적으로 보유할 필요는 없으니 공통 속성을 뽑아  
부모 클래스를 정의하고 부모로부터 상속받는 것이 구조상 바람직하다.  

![image](https://user-images.githubusercontent.com/93306939/169777439-70077a0a-2014-42f9-bef8-31ab99f2c783.png)

문방구의 모든 제품을 대표하는 루트 클래스에 문구류라는 이름을 붙였다.  
공통 속성이 부모쪽으로 옮겨져 자식 클래스는 간단해지며 모든 문구류를 칭하는 대표 타입이 생겼다.  
이 상태에서 연필과 볼펜을 보면 굵기라는 공통 속성이 발견되는데 이 속성을 가지는 필기류 클래스를 정의하고 연필과 볼펜을 그 하위에 둔다.  
 
상속은 부모의 속성을 자식에게 물려주는 것이니 순서상 부모를 먼저 정의해야 한다.  
그러나 상위의 부모를 정의하려면 자식들의 공통 속성을 잘 파악해야 하는데 웬만한 경험으로는 한 번에 계층을 완성하기 어렵다.  
왜냐하면 자식을 만들어 봐야 어떤 속성이 공통적인지 파악할 수 있기 때문이다.  

실제 모델링할 때는 자식 클래스의 집합을 먼저 만들고 공통된 속성을 추출하여 부모를 정의하는 것이 더 쉽다.  
사람의 사고는 특수한 것으로부터 일반성을 추출해 내는 것에 더 익숙하기 때문이다.  
이와같이 사물의 공통 속성을 뽑아 클래스 계층을 만드는 과정을 추상화라고 한다.  

**즉, 추상클래스는 A클래스, B클래스, C클래스들 간에 비슷한 필드와 메서드를 공통적으로 추출해 만들어진 클래스다.**

---------------------------------------------------------------------------------------------
 
### <b> 2.22 인터페이스(lnterface)에 대해 설명하세요.</b>
 
 - 인터페이스는 참조형 데이터타입의 일종으로 추상 메서드와 상수만이 정의된 클래스의 변형이라 할 수 있다.
 - new 키워드를 이용해서 객체를 생성할 수 없다.
 - 다른 클래스에 의해 구현(implements)된 다음 모든 추상 메서드의 몸체를 정의해 주어야 한다.
 - 인터페이스는 다중으로 구현(implements) 될 수 있으며 interfacer간에는 상속(extends) 할 수 있다.

![image](https://user-images.githubusercontent.com/93306939/169779036-b5429041-69f4-47e0-87c9-f93c3c80b4c9.png)

인터페이스는 객체를 어떻게 구성해야 하는지 정리한 설계도입니다.
인터페이스는 객체의 교환성(또는 다형성)을 높여줍니다.
인터페이스 변수에 인터페이스가 구현된 서로 다른 구현 객체를 할당해서 사용이 가능합니다.
구현 객체를 직접 몰라도 인터페이스 메서드만 알아도 객체 호출이 가능하게 합니다.
객체가 인터페이스를 사용하면, 인터페이스 메서드를 반드시 구현해야 하는 제약을 합니다.
 
 인터페이스의 장점
인터페이스를 사용하면 다중 상속이 가능할 뿐만 아니라 다음과 같은 장점을 가질 수 있습니다.

1. 대규모 프로젝트 개발 시 일관되고 정형화된 개발을 위한 표준화가 가능합니다.
2. 클래스의 작성과 인터페이스의 구현을 동시에 진행할 수 있으므로, 개발 시간을 단축할 수 있습니다.
3. 클래스와 클래스 간의 관계를 인터페이스로 연결하면, 클래스마다 독립적인 프로그래밍이 가능합니다.

2. 인터페이스(interface) 선언
인터페이스(Interface) 선언 형식은 다음과 같이합니다.

인터페이스(Interface)
```
[public] interface 인터페이스이름 { ... }
// 예시
public interface User { ... }
```

[더 자세한 내용은](https://interconnection.tistory.com/129)

---------------------------------------------------------------------------------------------

### p.s 추상클래스와 인터페이스 차이점  

 ![image](https://user-images.githubusercontent.com/93306939/169777175-2a8d39ee-5dc5-4531-9245-e3ac3eebb5bc.png)

**추상 클래스**  
클래스를 설계도라 하면, 추상 클래스는 **미완성 설계도**에 비유할 수 있다.  
(여기서 클래스가 미완성이라는 것은 추상 메서드를 포함하고 있다는 의미이다.)  

예를 들면, 같은 크기의TV라도 기능의 차이에 따라 여러 종류의 모델이 있지만  
설계도 90은 동일할테니, 어느정도 틀을 갖춘 상태에서 진행하는 것이 좋다.  
이때 사용할 수 있는 것이 추상 클래스이다.  

**인터페이스**  
인터페이스는 일종의 추상 클래스로, 추상 메서드를 갖지만  
추상 클래스보다 추상화 정도가 높아  
추상 클래스와 달리 몸통을 갖춘 일반 메서드, 멤버 변수를 구성원으로 가질 수 없다.  
추상 클래스를 미완성 설계도라 하면, 인터페이스는 구현된 것은 아무 것도 없는,  
밑그림만 그려진 **기본 설계도**라고 할 수 있다.  


**공통점**  
먼저 추상 클래스와 인터페이스의 공통점을 찾아보자.  
추상 클래스와 인터페이스 둘 다 가지고 있는 추상 메서드를 구현하도록 강제한다.  
또 인스턴스화가 불가능하다.  

그렇다면 추상 클래스 안에 원하는 것만 추상 메서드를 여러개 두거나,  
전부 추상 메서드로 만들면 되어 추상 클래스가 인터페이스 역할을 할 수 있다.  
만약 모든 클래스가 인터페이스만 사용해서 구현한다면,  
모든 클래스에서 공통으로 필요한 기능들은 각각 오버라이딩 하게 되니 코드의 중복이 발생한다.  
때문에 이 공통으로 필요한 기능들을 부모 클래스에서 일반 메서드로 구현한  
추상클래스를 상속 받아 자식 클래스에서 사용할 수 있도록 하면 될거같은데...  
왜 인터페이스는 왜 필요한걸까? 🤔  

**접근자 **
인터페이스에서 모든 변수는 public static final,  
모든 메소드는 public abstract이다.  
하지만 추상 클래스에서는 static이나 final이 아닌 필드를 가질 수 있고,  
public, protected, private 모두 가질 수 있다.  

개인적인 생각으로는 인터페이스만을 구현하면 public static final만을 사용해  
구현 객체의 같은 상태를 공유할수 밖에 없는데,  
추상 클래스는 static이나 final이 아닌 필드또한 가질 수 있기 때문에  
추상 클래스를 상속 받은 객체들이 같은 상태를 가지고 있을 수 있다.  

**다중 상속 여부**  
인터페이스를 구현하는 클래스는 다른 여러개 인터페이스를 함께 구현할 수 있다.  
하지만 자바에서는 다중 상속을 지원하지 않기 때문에 여러 추상 클래스를 상속할 수 없다.  

**사용 의도**  
물론 다중 상속 여부의 차이는 있지만 이것이 포인트가 아니라,  
이에 따른 사용 목적이 다르다는 것에 포인트를 맞춰보자.  
위에서 말한 다중 상속 여부에 따라 추상 클래스와 인터페이스의 사용 의도 또한 다르다.  

**추상 클래스**는 이를 상속할 각 객체들의 공통점을 찾아 추상화시켜 놓은 것으로,  
상속 관계를 타고 올라갔을 때 같은 부모 클래스를 상속하며  
부모 클래스가 가진 기능들을 구현해야할 경우 사용한다.  

**인터페이스**는 상속 관계를 타고 올라갔을 때  
다른 조상 클래스를 상속하더라도, 같은 기능이 필요할 경우 사용한다.  
클래스와 별도로 구현 객체가 같은 동작을 한다는 것을 보장하기 위해 사용한다.  

즉, 정리하자면  

**추상 클래스**  
관련성이 높은 클래스 간에 코드를 공유하고 싶은 경우  
추상 클래스를 상속 받을 클래스들이 공통으로 가지는 메소드와 필드가 많거나,  
public이외의 접근자(protected, private) 선언이 필요한 경우  
non-static, non-final 필드 선언이 필요한 경우 (각 인스턴스에서 상태 변경을 위한 메소드가 필요한 경우)  

**인터페이스**  
서로 관련성이 없는 클래스들이 인터페이스를 구현하게 되는 경우.  
ex) Comparable, Cloneable 인터페이스는 여러 클래스들에서 구현되는데, 구현클래스들 간에 관련성이 없다.  
특정 데이터 타입의 행동을 명시하고 싶은데, 어디서 그 행동이 구현되는지는 신경쓰지 않는 경우.  
다중상속을 허용하고 싶은 경우  

---------------------------------------------------------------------------------------------

### <b> 2.23 예외와 그 처리 방법에 대해 설명하세요.</b>
 
 - 예외란 에러의 한 종류로 프로그램이 종료되지 않고 계속 진행이 될 수 있도록 처리가능한 가벼운 에러라고 할 수 있다.

![image](https://user-images.githubusercontent.com/93306939/170161258-38b339a1-a8bd-4844-964e-b8260e0d2b0c.png)

자바는 예외처리를 담당하는 예외클래스들을 지원한다.  
예외클래스의 최상위 클래스는 Throwable 클래스이며 하위로 Error 와 Exception 클래스가 있다.  

**1. Error(에러)**  
에러(Error)란 컴퓨터 하드웨어의 오동작 또는 고장으로 인해 응용프로그램에 이상이 생겼거나 JVM 실행에 문제가 생겼을 경우 발생하는 것 따라서 개발자가 미리 예측하여 처리할 수 없기 때문에, 애플리케이션에서 오류에 대한 처리를 신경 쓰지 않아도 된다.  
즉, 걸리면 프로그램이 숨진다고 생각하면 된다 천재지변이다. (오류(Error 에러)- 시스템 레벨에서 발생)  
ex) 메모리 부족(OutOfMemoryError), 스택오버플로우(StackOverFlowError)  

**2. Exception(예외)**  
사용자의 잘못된 조작 또는 개발자의 잘못된 코딩으로 인해 발생하는 프로그램 오류.  
예외가 발생하면 프로그램이 종료가 된다는 것은 에러와 동일하지만 예외는 예외처리(Exception Handling)를 통해 프로그램을 종료되지 않고 정상적으로 작동되게 만들어줄 수 있다. 자바에서 예외처리는 Try Catch문을 통해 처리가능  
즉, 예외는 발생할 상황을 미리 예측하여 처리할 수 있다 (Exception(예외) - 보통 예외는 개발자 or 사용자가 낸다)  

ex)  
![image](https://user-images.githubusercontent.com/93306939/170161967-55fab383-6bf9-4866-b967-0c9b85630854.png)


그러면 우리가 처리 가능한 Exception의 종류에 대해 알아보도록 하자.  
Exception의 종류에는 **Checked Exception**과 **Unchecked Exception**이 있다.  
두 Exception의 가장 큰 차이는 '반드시 예외 처리를 해야 하는가?' 이다.  

![image](https://user-images.githubusercontent.com/93306939/170161109-2d72820c-ee0f-4cdb-8034-08f2414b2ff9.png)


**Checked Exception은** 체크 하는 시점이 컴파일 단계이기 때문에,  
별도의 예외 처리를 하지 않는다면 컴파일 자체가 되지 않는다. **반드시 예외 처리가 필요하다!!**  
확인 : 컴파일 단계  
예외 발생시 트랜잭션 처리 : roll-back 하지 않음  

반면에 **Unchecked Exception의 경우**는 충분히 개발자의 충분한 주의로 피할 수 있는 경우가 대부분이다.  
따라서 별도의 **예외 처리가 꼭 필요하지 않으며,** 처리하지 않더라도 컴파일도 되고 실행까지 가능하다.  
확인 : 실행단계 확인  
예외 발생시 트랜잭션 처리 : roll-back 진행됨.  
 
---------------------------------------------------------------------------------------------

### <b> 2.24 예외 처리 방법</b>
 
 ![image](https://user-images.githubusercontent.com/93306939/170161124-b4d2b922-e774-4a00-a537-77d97704b61f.png)

예외는 예외처리(Exception Handling)를 통해 프로그램을 종료되지 않고 정상적으로 작동되게 만들어줄 수 있다.  
자바에서 예외처리는 Try Catch문을 통해 해 줄 수 있습니다.  

예외 처리에 대한 자세한 방법은 아래 사이트를 참조 바람  
[자바의 예외처리](https://ccm3.net/archives/20672)


---------------------------------------------------------------------------------------------
 
### <b> 2.25 Thread란 무엇인가?</b>

 ![image](https://user-images.githubusercontent.com/93306939/170173607-f0747961-1af2-400f-9989-29a07aeb5e8e.png)

**JAVA Thread**  
- 자바 가상 기계(JVM)에 의해 스케쥴되는 실행 단위의 코드 블럭  
- 스레드의 생명 주기는 JVM에 의해 관리됨  
 
 **JVM과 멀티스레드의 관계**
 - 하나의 JVM은 하나의 자바 응용프로그램만 실행
	 - 자바 응용프로그램이 시작될 때 JVM이 함께 실행됨
	 - 자바 응용프로그램이 종료하면 JVM도 함께 종료함
 - 하나의 응용프로그램은 하나 이상의 스레드로 구성가능  

 ![image](https://user-images.githubusercontent.com/93306939/170174203-09b3a09e-098c-49f3-8f84-0b7ff81d67b3.png)

---------------------------------------------------------------------------------------------
 
### <b> 2.26 Stream이란 무엇인가?</b>
 
 자바 8에서 추가한 스트림(Streams)은 람다를 활용할 수 있는 기술 중 하나입니다.  
 자바 8 이전에는 배열 또는 컬렉션 인스턴스를 다루는 방법은 for 또는 foreach 문을 돌면서 요소 하나씩을 꺼내서 다루는 방법이었습니다.   
 간단한 경우라면 상관없지만 로직이 복잡해질수록 코드의 양이 많아져 여러 로직이 섞이게 되고, 메소드를 나눌 경우 루프를 여러 번 도는 경우가 발생합니다.  

스트림은 '데이터의 흐름’입니다. 배열 또는 컬렉션 인스턴스에 함수 여러 개를 조합해서 원하는 결과를 필터링하고 가공된 결과를 얻을 수 있습니다.  
또한 람다를 이용해서 코드의 양을 줄이고 간결하게 표현할 수 있습니다. 즉, 배열과 컬렉션을 함수형으로 처리할 수 있습니다.  

또 하나의 장점은 간단하게 병렬처리(multi-threading)가 가능하다는 점입니다.  
하나의 작업을 둘 이상의 작업으로 잘게 나눠서 동시에 진행하는 것을 병렬 처리(parallel processing)라고 합니다.  
즉 쓰레드를 이용해 많은 요소들을 빠르게 처리할 수 있습니다.  
 

---------------------------------------------------------------------------------------------
 
 ### <b> 2.27 객체 직렬화(Object Serialization)</b>
 
 - 객체를 byte기반의 데이터로 읽고 쓰는 기술
 - JVM의 메모리에서만 상주되어 있는 객체 데이터를 그대로 영속화(persistence)가 필요할 때 사용한다.
 - 영속화 된 데이터이기 때문에 네트워크로 전송도 가능하다.
 - 객체의 직렬화 조건
  - java.io.Serialization 인터페이스를 구현한다.
  - 직렬화의 대상이 되는 데이터는 멤버 변수들이며, 'has a'관계로 있는 멤버 변수 또한 직렬화가 가능해야한다.

 자세한 사용법 및 생성방법은 아래 사이트 참조  
[Java 스트림 Stream](https://futurecreator.github.io/2018/08/26/java-8-streams/)

---------------------------------------------------------------------------------------------

 
# 재귀호출

#include <stdio.h>  
  
int factorial(int n)  
{  
    if (n == 1)      // n이 1일 때  
        return 1;    // 1을 반환하고 재귀호출을 끝냄  
  
    return n * factorial(n - 1);    // n과 factorial 함수에 n - 1을 넣어서 반환된 값을 곱함  
}  
  
int main()  
{  
    printf("%d", factorial(5));  
  
    return 0;  
}  

형, 함수 factorial(int n)에 5를 넣어  
그러면 if로 들어가 (n == 1) 5니까 false야   
  
아래로 내려가서 return n * factorial(n - 1);이 실행되  

factorial(n - 1)가 함수 재귀호출을 했어    
  
이때 메모리는 아래 그림과 같아  

ㅣ　　　　　　　　　　　　　　　　ㅣ   
ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ  
ㅣ n - 1 지역변수 (여기선 5 - 1) 　　　ㅣ  
ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ  
ㅣ 반환 주소 값 (돌아올 위치) 　　　　ㅣ  
ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ  
ㅣ 5 (매개변수) 　　　　　　　　　　ㅣ    
  　
![image](https://user-images.githubusercontent.com/93306939/169744532-84501f83-1f3f-482a-8023-4e0b460fb462.png)
  
그러면 factorial(n - 1)가 호출됬으니 n == 5   
5 - 1인 4로 factorial(int n)를 호출해  
  
  
이때 메모리는 아래 그림과 같아  
ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ  
ㅣ　　　　　　　　　　　　　　　  ㅣ   
ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ  
ㅣ n - 1 지역변수 (여기선 4 - 1)  　　　ㅣ  
ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ  
ㅣ 반환 주소 값 (돌아올 위치)    　　 ㅣ  
ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ  
ㅣ 4 (매개변수)　　　　　　　　　　　ㅣ  
ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ  
ㅣ n - 1 지역변수 (여기선 5 - 1)　　　  ㅣ  
ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ  
ㅣ 반환 주소 값 (돌아올 위치)   　　  ㅣ  
ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ  
ㅣ 5 (매개변수)　　　　　　　　　　ㅣ  
ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ  
  
if (n == 1) 이 아니니  
또 함수안에서 자기를 호출하고, 재귀를 해  
그러면 factorial(n - 1)가 호출됬으니 n == 4  
  
... 반복을 해  
  
이렇게 n == 1 까지 메모리가 쌓이고 1이 되면 1을 반환하고 끝낼꺼야  
  
return n * factorial(n - 1);  
그러면 여기 이 문장에서  
마지막에 1이 리턴됬으니  
처음은 2 * 1이 되고 이 값인 2를 반환 주소 값으로 보낼꺼야  
  
그러면 2가 반환 주소값으로 돌아가겠지?  
  
그러면 다음은 2가 반환 됬으니 3*2  
  
그다음은 4*6....  
  
![image](https://user-images.githubusercontent.com/93306939/169744557-32ad54c9-f0b0-4ad7-bf9f-66e0067d5350.png)

위 그림처럼 하나씩 반환 되겠지  
이러한 함수 호출 방식을 재귀 호출이라 합니다.  

![image](https://user-images.githubusercontent.com/93306939/169743896-863838c8-fbff-4684-895c-ac6513dd9648.png)

![image](https://user-images.githubusercontent.com/93306939/169743698-efabee76-4c3a-46e8-bbe1-dcd6ec8d080e.png)

