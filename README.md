# Technical_interview
기술면접 대비를 위한 IT 기초 정리입니다.

기술면접 대비할려고 만든 프로젝트입니다.

여기에 기술면접 대비 내용을 기술하십시오.

# ➀ 프로그램 기본 개념

![image](https://user-images.githubusercontent.com/93306939/169712506-da2d7ff2-0398-4549-ae7b-7933dae59204.png)

1. 저급 프로그래밍 언어（低級 프로그래밍 言語）or 로우 레벨 프로그래밍 언어(low-level programming language)

저급언어
- 컴퓨터가 이해하기 쉬운 이진법으로 이루어진 언어이다
- 컴퓨터가 바로 이행 할 수 있지만 가독성 및 생산성이 낮다.
- 프로그램 속도가 빠르다.　
- 프로그램 크기 또한 고급언어 보다 작다.
- 저급언어에는 기계어와 어셈블리어 등이 있다.

1.1 기계어  
-기계어란 cpu가 직접 해독하고 실행할 수 있는 비트 단위로 쓰인 컴퓨터 언어를 통틀어 일컫는다.  
-기계어는 프로그램을 나타내는 가장 낮은 단계의 개념이다.  

1.2 기계어의 특징  
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


1.3 어셈블리어  
-어셈블리어란 기계어를 사람이 이해하기 쉬운 기호와 1 : 1로 대응시켜 기호화한 프로그램 언어이다.  
-기호 언어라고도 부른다.  


어셈블리어의 특징  
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


1.4 어셈블리어의 장단점

장점  
- 프로그램의 실행 속도가 매우 빠르다. (기계에게 바로 명령을 내리기 때문에)  
- 프로그램의 크기가 매우 작다. (최소한의 명령을 사용하기 때문에)  
- 어떤 프로그램이라도 만들 수 있다. (하드웨어를 직접 제어 할 수 있기 때문에 어떠한 명령도 수행 할 수 있다.)  

단점  
- 배우기 힘들다. ( 고급언어인 c나 java등에서 코딩을 할 때에는 하드웨어적 지식이 필요 없지만, 어셈블리어는 하드웨어 지식이 뛰어나야 하기 때문에)  
- 큰 프로그램을 만들기 힘들다. (세밀한 제어가 필요하기 때문에 클 프로그램을 만들기에는 힘들다.)  
- 프로그램을 짤 때 시간이 오래 걸리고 디버그도 어렵다. (에러를 찾을 때 직접 찾아야 해서 어렵다.)  

1.5 어셈블리어의 용도  
하드웨어 디바이스 드라이버  
-드라이버라 불리는 하드웨어를 조절하는 프로그램을 만들 때 거의 대부분어셈블리어로 작성한다.  
-하드웨어 제어는 드라이버 파일이 작고 실행 속도는 빨라야 함.  

일반 프로그램의 기능 최적화  
-게임이나 프로그램을 만들 때 100% 고급언어를 이용한다면. 속도가 느려 제 역할을 하지 못한다.  
-속도가 필요하거나 하드웨어를 정밀하게 제어 할 때에는 어셈블리어를 이용한다.  
-어셈블리 프로그램을 고급언어로 만든 프로그램과 링크시켜서 사용하는 것이 보편적이다.  

---------------------------------------------------------------------------------------------

2. 고급 프로그래밍 언어 또는 하이 레벨 프로그래밍 언어(high-level programming language)  
  사람이 이해하기 쉽게 작성된 프로그래밍 언어  
  
  JAVA기준으로 설명  
  
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

2.1 JAVA의 이해.

프로그래밍 언어가 제공하는 기능을 개발자가 만든 프로그램 내에서  
쉽게 제어할 수 있게 만든 클래스들의 묶음  
(Application Programming Interface)  

패키지 단위로 묶여있음  
API Document를 통해 사용법을 제공  


★자바의 메모리 구조  

Class영역 | Stack영역 | Heap영역 | Nailve method영역 | PC Register영역  

Class영역(Method영역)  
 - JVM에서 읽어들인 클래스와 인터페이스에 대한 런타임 상수 풀, 메서드와 필드 Static 변수, 메서드 바이트 코드 등을 보관  
 
Stack영역  
 - 선입후출(FILO) 구조, 메서드 호출 시 생선되는 스레드 수행정보를 기록하는 Frame저장,메서드 정보, 지역변수, 매개변수, 연산 중 발생하는 임시 데이터 저장  

Heap영역  
 - 프로그램 상에서 데이터를 저장하기 위해 런타임 시 동적으로 할당하여 사용하는 메모리 영역 New 연산자를 통해 생생한 객체, 또는 인스턴스와 배열을 저장 (JVM이 관리)  

Nailve method영역  
 - 자바 외 언어로 작성된 네이티브 코드를 위한 메모리 C/C+등의 코드를 수행하기 위한 스택 native 메서드의 매개변수, 지역변수 등을 바이트코드로 저장  

PC Register영역  
 - 현재 실행 중인 JVM 주소를 가지고 있다. CPU 명령어 즉 lnstruction을 수행한다. CPU lnstruction을 수행하는 동안 필요한 정보를 CPU내 기억장치인 레지스터에 저장, 연산 및 결과값을 메모리에 전달하기 전 CUP내 기억장치임.  


가비지 컬렉터(GC)는 언제 작동 되는가  

GC는 다음 방법 중 하나를 사용하여 요청할 수 있습니다.

# 1) System.gc () : Java의 System 클래스는 가비지 콜렉터를 실행하기 위해 JVM을 요청할 수있는 정적 메소드 gc ()를 제공합니다.

# 2) Runtime.getRuntime (). gc () : System.gc ()와 마찬가지로 'Runtime class'의 gc () 메서드를 사용하여 가비지 수집기를 실행하도록 JVM을 요청할 수도 있습니다.

<b>가비지 컬렉터?  
-쓰레기 수집(garbage collection 가비지 컬렉션[*], GC)은 메모리 관리 기법 중의 하나로, 프로그램이 동적으로 할당했던 메모리 영역 중에서 필요없게 된 영역을 해제하는 기능이다.  
쓰레기 수집은 동적 할당된 메모리 영역 가운데 더 이상 사용할 수 없게 된 영역을 탐지하여 자동으로 해제하는 기법이다. 더 이상 사용할 수 없게 된 영역이란, 어떤 변수도 가리키지 않게 된 영역을 의미한다.  
자바, C#, 그리고 일부 스크립트 언어들은 처음부터 쓰레기 수집 기법을 염두에 두고 설계되어, 언어 정의에 쓰레기 수집이 포함되어 있다.  </b>

---------------------------------------------------------------------------------------------




# 6. 메타버스란?
