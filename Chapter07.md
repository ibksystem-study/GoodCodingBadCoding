
Chapter 7 식별자 이름을 지을 때 좋은 코딩 습관 Ⅱ

1. 이름을 의미있게 지어라

 (좋지 못한 예)
    double num1;
    double num2; 

 (좋은 예)
    double ftp_bnk_rate;         /* 은행내부금리   */
    double krw_bs_avg_mon_bal;   /* 원화BS월중평잔 */

 -> 변수 이름에 투자하는 시간과 노력은 반드시 보상받는다!


2. 비슷한 변수 이름을 사용하지 마라
 - 변수 이름을 유사하게 짓게 되면 프로그램을 코딩하는 중에 혼동하기 쉽다.

 (좋지 못한 예)
    short int number;
    int numbers;

    int total;
    double total2;

 (좋은 예)
    short int digit;    /* 한자리 숫자를 뜻하는 단어를 사용하여 구분 */
    int number;
 
    int iTotal;         /* 자료형을 상징하는 문자를 붙여 구분 */
    double dTotal;


3. 의미를 잃지 않는 범위에서 짧게 지어라
 - 단어를 모두 쓰지 않고 일부만 표기해도 무엇을 나타내는 단어인지 알 수 있는 경우, 될 수 있는 한 줄여서 쓰는 것이 좋다.
   이를테면 check는 chk, button은 btn, selection은 sel, source는 src, object는 obj, library는 lib 처럼 말이다.
   * 기업은행 知캠프 - 링크사이트 - DA포탈에서 참고할 수 있다. (맨 아래에서 설명)

 (좋지 못한 예)
    char Management_Branch_Code_Name;
    
    Break_Control_System_Function();

 (좋은 예)
    char mngm_brcd_nm;
    
    BrkCtlSysFunc();


4. 이름이 길면 밑줄 또는 대소문자로 구분하라

 (좋지 못한 예)
    Breakcontrolsystempanel();

 (좋은 예)
    Break_control_system_panel();   /* 밑줄을 사용하는 방법 */
    BreakControlSystemPanel();      /* 단어의 첫글자를 대소문자로 하는 방법 */
    
 (가장 좋은 예)
    BrkCtlSys_Panel();
    -> 단어를 줄여서 쓸 수 있는 부분은 첫글자를 대문자로 하는 방법 사용,
       단어를 줄일 수 없는 부분은 밑줄로 구분하는 방법 사용

 - 주의사항! 이름을 줄여서 쓴다면 모든 프로그램에서 통일해서 사용하도록 한다.
  한쪽에서는 줄인 이름을, 한쪽에서는 줄이기 전 원래 이름을 사용하면 혼란스럽게 된다.


5. 변수 이름을 밑줄로 시작하지 마라
 - studio.h , stdlib.h , math.h 등 각종 헤더파일에서 많은 변수 이름이 밑줄로 시작한다.
   헤더 파일 안에 선언된 변수 이름과 우리가 작성한 프로그램 안에 있는 변수 이름이 우연히 겹칠 가능성을 사전에 방지하기 위해서이다.
   따라서 int _number , int _time 등과 같이 밑줄로 시작하는 변수는 사용하지 않도록 한다.


6. 밑줄을 과도하게 사용하지 마라
 - 밑줄을 과도하게 사용하면 실수하기 쉽다.

 (좋지 못한 예)
    char file__name___of__new____name;    /* 각 각 밑줄이 몇개인지 알 수 있는가? */
    file__name____of__new_____name = 'C';   /* 위 변수 이름과 같은가? */

 (좋은 예)
    char file_name_of_new_file;
    char fileNameOfNewFile;
    char newFileName;


7. 대소문자를 적절히 배합해 식별자 이름을 지어라
 - 기호 상수나 매크로 함수는 모든 글자를 대문자로만 짓는다.    예) #define TRUE 1
 - 함수, 클래스, 구조형, 공용형 등의 이름은 대문자로 시작한다. 예) Struct Grade { ... }
 - 변수나 객체의 이름은 소문자로 시작한다.                     예) Grade myGrade;


8. 대소문자 구분을 악용하지 마라 Ⅰ
 - C언어는 대문자와 소문자를 명백히 구분한다.
  예를 들어 int num, int Num, int NUM 은 C에서 모두 다른 변수로 취급한다.


9. 대소문자 구분을 악용하지 마라 Ⅱ 
 
(좋지 못한 예) 
    int iMyNumber = 100000;   /* 큰 수 */
    int iMynumber = 1;        /* 작은 수 */
    -> 큰 수는 대문자로, 작은 수는 소문자로 구분한 경우

 - 코드를 읽는 사람들은 두 변수를 혼동하기 쉽다.
 - 프로그래머는 C의 이러한 특성을 몰라서는 안되고, 악용해서도 안된다.
 

10. 클래스 이름과 변수 이름을 같게 하지 마라

 (좋지 못한 예)
    Class MyClass { 
      ... 
    }
    
    MyClass myclass;

 (좋은 예)
    Class MyClass {
      ...
    }
    
    MyClass mcFirstVar;   /* mc는 MyClass를 나타내는 접두사 */


11. 변수 이름 중 강조할 부분을 대문자로 처리하라 
 - 함수에서 잠깐 사용하고 마는 로컬 변수는 소문자만으로 변수 이름을 짓는다. 예) int num;
 - 다소 중요한 변수인 경우, 중간에 대문자를 적당히 넣어준다.                예) int MyNumber;
 - 특정 어휘만 강조하고 싶은 경우, 강조하고 싶은 낱말만을 대문자로 한다.    예) int newMOREthanTHIS;
 



* 링크사이트 - DA포탈 - 조회업무 - 표준속성 조회
 - 표준속성명 입력 (LIKE 검색의 경우 * 이용)
 - 원하는 속성 더블클릭시 속성구성 조회 가능

  사용예) 표준속성명을 '관리부점코드*'으로 검색시 조회결과
          관리부점코드         - mngm_brcd
          관리부점코드명       - mngm_brcd_nm
          관리부점코드변경여부 - mngm_brcd_mdfc_yn
          관리부점코드일치여부 - mngm_brcd_acrd_yn 

