
Chapter 7 식별자 이름을 지을 때 좋은 코딩 습관 Ⅱ
 (p.150 ~ 165)


1. 이름을 의미 있게 지어라

 - 좋지 못한 예
    double num1;
    double num2;

    int a;
    int b;

     -> 변수 비교/연산시 혼동을 줄 수 있다.

 - 좋은 예
    double ftp_bnk_rate;       /* 은행내부금리 */
    double krw_bs_avg_mon_bal; /* 원화BS월중평잔 */

-> 변수 이름에 투자하는 시간과 노력을 반드시 보상받는다!!



2. 비슷한 변수 이름을 사용하지 마라

 - 좋지 못한 예
    int number;
    long int numbers;
    short int num;

    int total1;
    double total2;


 - 좋은 예
    int number;
    short int digit; /* digit은 한자리 숫자를 의미함 */

    int iTotal;      /* 자료형을 상징하는 문자를 붙여 구분 */
    double dTotal;



3. 의미를 잃지 않는 범위에서 짧게 지어라

 - 좋지 못한 예
    char Management_Branch_Code_Name;    /*  관리부점코드명 */
    Break_Contol_System_Function();      /* 브레이크 제어시스템 함수 */


 - 좋은 예
    char mngm_brcd_nm;    /*  관리부점코드명 */
    BrkCtlSysFunc();      /* 브레이크 제어시스템 함수 */

     -> 단어를 모두 쓰지 않고 일부만 표기해도 무엇을 나타내는 단어인지 알 수 있는 경우
       될수 있는 한 줄여서 쓰는 것이 좋다.
       check  -> chk     button -> btn     selection -> sel
       source -> src     object -> obj     library   -> lib


 * 링크사이트 - DA포탈 - 조회업무 - 표준속성 조회
  - 표준속성명 입력 (Like 검색 '*' 문자 이용 가능)
  - 원하는 속성 더블클릭시 속성구성 조회 가능



4. 이름이 길면 밑줄 또는 대소문자로 구분하라
 
 - 좋지 못한 예
      Breakcontolsystempanel();
      -> 단어 구분이 힘들다.

 - 좋은 예
     Break_control_system_panel();   /* 밑줄을 사용하는 방법 */
     BreakControlSystemPanel();      /* 단어의 첫글자를 대문자로 하는 방법 */

 - 가장 좋은 예
     BrkCtlSys_Panel();              
      -> 단어를 줄여서 쓸 수 있는 부분은 단어의 첫 글자를 대문자로 만드는 방법 사용,
        단어를 줄일 수 없는 부분은 밑줄로 구분하는 방법 사용



5. 변수 이름을 밑줄로 시작하지 마라

 - 좋지 못한 예
    #include <stdio.h>
    #include <math.h>
    
    int _define;
    int _time;
 
  -> studio.h, stdlib.h, math.h 등 각종 헤더파일에서 많은 변수 이름이 밑줄로 시작한다.
     헤더 파일 안에 선언된 변수 이름과 우리가 작성한 프로그램 안에 있는 변수 이름이 우연히
    겹칠 가능성을 사전에 방지하기 위해서이다.


6. 밑줄을 과도하게 사용하지 마라
 - 밑줄을 과도하게 사용하면 실수하기 쉽다.


7. 대소문자를 적절히 배합해 식별자 이름을 지어라
8. 대소문자 구분을 악용하지 마라 Ⅰ
9. 대소문자 구분을 악용하지 마라 Ⅱ
10. 클래스 이름과 변수 이름을 같게 하지 마라
11. 변수 이름 중 강조할 부분을 대문자로 처리하라
