## Chapter 03. 띄어 쓸 때 좋은 코딩 습관  

---  

## 1) 한 줄에 한 문장만 쓰라

문장은 ';'로 구분된다.  
주석처리가 용이하다.  

<pre>  
(ex 1-1)  
<code>  
    int num1; int num2; double dbl1; /* num1:수1, num2:수2, */  
</code>  
  
(ex 1-2)  
<code>  
    int num1; /* 수1*/
    int num2; /* 수2*/
    double dbl1;
</code>  
</pre>  


## 2) 선언문과 실행문을 구분하라.  

가독성을 위하여 선언문과 실행문 사이에 빈줄을 삽입한다.  

<pre>  
(ex 2-1)  
<code>  
    int num1;
    int num2;
    int sum;
    sum = num1 + num2;
</code>  
  
(ex 2-2)  
<code>  
    int num1;
    int num2;
    int sum;

    sum = num1 + num2;
</code>  
</pre>  


## 3) 단락을 구분하라.  

비슷한 역할을 담당하는 실행문을 구분지어 주면 가독성이 높아진다.  

<pre>  
(ex 3-1)  
<code>  
#include &lt;studio.h&gt;
int main(void) {
    int num1;
    int num2;
    pintf("첫번째수를 입력하시오");
    scanf("&d",&num1);
    pintf("두 번째수를 입력하시오");
    scanf("&d",&num2);
    sum = num1 + num2;
    printf("두 수의 합은 %d이다.\n");
    return 0;
}
</code>  
  
(ex 3-2)  
<code>  
#include &lt;studio.h&gt;

int main(void) {

    int num1;
    int num2;

    pintf("첫번째수를 입력하시오");
    scanf("&d",&num1);

    pintf("두 번째수를 입력하시오");
    scanf("&d",&num2);

    sum = num1 + num2;
    printf("두 수의 합은 %d이다.\n");

    return 0;
}
</code>  
</pre>  


## 4) 제어문들 사이를 구분하라.  

프로그램의 흐름을 바꾸는 제어문의 가독성을 높혀 오류를 줄일 수 있다.  

<pre>  
(ex 4-1)  
<code>  
    if(num1 == num2)
        printf("두 숫자는 같다");
    if(num1 != num2)
        printf("두 숫자는 다르다.");
</code>  
  
(ex 4-2)  
<code>  
    if(num1 == num2) {
        printf("두 숫자는 같다");
    }

    if(num1 != num2) {
        printf("두 숫자는 다르다.");
    }
</code>  
</pre>  


## 5) 함수들 사이를 구분하라.  

함수들 사이에 공백을 2~3줄 추가하면 함수의 모듈화를 식별하기 쉬워진다.  
* 함수의 시작과 끝을 파악한다.  
* 프로그램내 함수의 갯수 파악이 용이하다.  
* 특정 함수의 위치 파악이 용이하다.  

<pre>  
(ex 5-1)  
<code>  
void func1(void){
    pintf("첫번째수를 입력하시오");
    scanf("&d", &num1);
}
void func2(void){
    pintf("두번째수를 입력하시오");
    scanf("&d", &num2);
}
void func3(void){
    pintf("세번째수를 입력하시오");
    scanf("&d", &num3);
}
</code>  
  
(ex 5-2)  
<code>  
void func1(void){
    pintf("첫번째수를 입력하시오");
    scanf("&d", &num1);
}

void func2(void){
    pintf("두번째수를 입력하시오");
    scanf("&d", &num2);
}

void func3(void){
    pintf("세번째수를 입력하시오");
    scanf("&d", &num3);
}
</code>  
</pre>  


## 6) 연산자의 앞뒤로 빈 칸을 둬라.  

<pre>  
(ex 6-1)  
<code>  
    for(x=1,y=,z=,x<=y&&x<=z,y++,z++)
</code>  
  
(ex 6-2)  
<code>  
    for(x = 1, y = 1, z = 1, x <= y && x <= z, y++, z++)
</code>  
</pre>  


## 7) 단항 연산자를 피연산자와 띄어 쓰지 마라.  

컴파일러 경고를 발생시킬뿐 아니라 이해도 어렵다.  
괄호를 사용하면 이해를 높힐 수 있다.  

<pre>  
(ex 7-1)  
<code>  
    f = a + ++ b - c -- d + e;
</code>  
  
(ex 7-2)  
<code>  
    f = a + (++b) - c (--d) + e;
</code>  
</pre>  


## 8) 세미콜론 앞에 공백을 두지마라.  

<pre>  
(ex 8-1)  
<code>  
    double double1;
    int num1      ;
</code>  
  
(ex 8-2)  
<code>  
    double double1;
    int num1;
</code>  
</pre>  


## 9) 탭을 남용하지 마라.  

<pre>  
(ex 9-1)  
<code>  
    if (num1 == num2){
        num1 =  num2;
    }
</code>  
  
(ex 9-2)  
<code>  
    if(num1 == num2){
        num1 = num2;
    }
</code>  
</pre>  


## 10) 특히 쉼표 뒤에 빈칸을 둬라.  

<pre>  
(ex 10-1)  
<code>  
    for(x=1,y=1,z=1,x<=y&&x<=z,y++,z++)
</code>  
  
(ex 10-2)  
<code>  
    for(x=1, y=1, z=1, x<=y&&x<=z, y++, z++)
</code>  
</pre>  


## 11) 쉼표 뒤에 너무 많은 빈 칸을 두지 마라.  

강조를 위해 빈 칸을 넢게 하는것은 보기에 좋지않다.  

<pre>  
(ex 11-1)  
<code>  
    pintf("고객의 기여도는      ROYAL3+++     입니다.");
</code>  
  
(ex 11-2)  
<code>  
    pintf("고객의 기여도는 'ROYAL3+++' 입니다.");
</code>  
</pre>  


## 12) 변수 초기화 시 줄을 맞춰라.  

<pre>  
(ex 12-1)  
<code>  
    int enteryear = 2016;
    int entermonth = 12;
    int exityear = 2016;
    int exitrmonth = 12;
    double enterdouble1 = 2016.000;  
    double enterdouble2 = 12.000;
    long double exityearlongdouble = 2016.000;
    long double exitmonthlongdouble = 12.000;
</code>  
  
(ex 12-2)  
<code>  
    int enteryear   = 2016;
    int entermonth  = 12;

    int exityear    = 2016;
    int exitrmonth  = 12;

    double enterdouble1 = 2016.000;  
    double enterdouble2 = 12.000;

    long double exityearlongdouble  = 2016.000;
    long double exitmonthlongdouble = 12.000;
</code>  
</pre>  


## 13) 한 줄에 변수 한개만 선언하라.  

작성자의 의도와 컴파일러의 해석이 다르다.

<pre>  
(ex 13-1)  
<code>  
    int num1; num2;
    double dbl1; dbl2; /* dbl2 를 int 형으로 인식함.*/
</code>  
  
(ex 13-2)  
<code>  
    int num1; int num2;
    double dbl1; double dbl2;
</code>  
  
(ex 13-3)  
<code>  
    int num1;
    int num2;
    double dbl1;
    double dbl2;
</code>  
</pre>  

