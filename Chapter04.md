## CHAPTER 4. 들여 쓸 때 좋은 코딩 습관

1.중괄호위치
함수의 시작이나 블록의 시작점과 끝점을 알려주는 {  }(중괄호)는 들여쓰기가 굉장히 중요!

<pre>
<code>

첫 번째 Style : 중괄호를 문장과 한 줄에 쓰는 방법
void main(){
int i,j;
 for(i=2; j<=9; i++) {
   for(j=1; j<=9; j++) {
     printf(“%d x %d = %2d”, I, j, i*j); }
  printf(“\n”); } }
  
  
두 번째 Style : 중괄호를 문장과 다른 줄에 쓰는 방법
void main()
{
int i,j;
for(i=2; j<=9; i++)
{
for(j=1; j<=9; j++)
{
printf(“%d x %d = %2d”, I, j, i*j);
}
printf(“\n”);
}
}

세 번째 Style : 첫 번째와 두 번째를 혼합한 방법
void main()
{
int i,j;
  for(i=2; j<=9; i++) {
    for(j=1; j<=9; j++) {
     printf(“%d x %d = %2d”, i, j, i*j);
    }
   printf(“\n”);
  }
}



</code>
</pre>

2.중괄호위치를 통일 시켜라
 중괄호의 위치를 통일 시켜주어야 한다.
 문장이 길어질수록 통일된 중괄호가 도움이된다.

<pre>
<code>

몸체를 들여 쓰지 않는 경우
void main()
{
printf(“들여쓰기 예제\n”);
}

몸체만 들여 쓴 경우
void main()
{
 printf(“들여쓰기 예제\n”);
}

중괄호까지  들여 쓴 경우
void main()
   {
   printf(“들여쓰기 예제\n”);
   }

</code>
</pre>

3. 내부블록을 들여 써라
 함수 내에 블록이 존재한다면 ?
 함수의 몸체를 이루는 문장이 시작되는 지점에 맞추어 중괄호를 써준다.
 그리고 블록을 이루는 문장은 중괄호보다 더 들여써주면 좋다.

<pre>
<code>
내부블록을 들여쓰지 않은 경우


int main()
{
int a=1;
if(a==1){
int a=2;
printf(“블록 내에서 a는 %d”, a);
}
printf(“블록 밖에서 a는 %d”, a);
return 0;
}

내부블록을 들여 쓴 경우

int main()
{
  int a=1;
  
  if(a==1){
    int a=2;
    printf(“%d”, a);
  }
  printf(“%d”, a);
return 0;
}
</code>
</pre>


4. 피 제어부를 들여 써라 
들여쓰기의 효과를 볼 수 있는 것은 바로 제어문을 사용할 때!


<pre>
<code>
void main() 
{
int[] index = { 5, 4, 2, 1, 3};
int i, j, temp;
for (i = 0; i < index.length – 1; i++)
for (j = 0; j < index.length – 1 – i; j++)
if (index[j] > index[j + 1])
temp = index[j];
index[j] = index[j + 1];
index[j + 1] = temp;
}


void main() 
{
    int[] index = { 5, 4, 2, 1, 3};
    int i, j, temp;

    for (i = 0; i < index.length – 1; i++) {
        for (j = 0; j < index.length – 1 – i; j++) {
           if (index[j] > index[j + 1]) {
             temp = index[j];
             index[j] = index[j + 1];
             index[j + 1] = temp;
           }
        }
    }
}


if(num1 == num2){
  printf(“%d는 %d와 같다.” , num1, num2);
}
필요없어도 사용하는 중괄호를 잉여중괄호라고 한다.

</code>
</pre>


5. 쓸떼 없는 들여쓰기를 하지마라

 쓸떼없는 들여쓰기로 혼동을 줄 수도 있으니 가능하면 주석을 사용하는 것이 좋다.

<pre>
<code>
  int main(void) {
   printf(“쓸데없는 들여쓰기”);
     return 0;
  }



  int main(void) {
   printf(“쓸데없는 들여쓰기”);
  /*  프로그램 종료  */
  return 0;
  }
  </code>
  </pre>
  
  6. 들여 쓰는 정도를 일정하게 하라
    들여 쓰기 하는 정도를 통일해주는 것이 좋다.
<pre>
<code>
  if(num1==1){
   if(num2==2){
          if(num3==3){
                            if(num4==4){
                            }
          }
   }
  }
  </code>
  </pre>
  
  7.들여 쓰는 깊이를 적당하게 하라

<pre>
<code>
   if(num1==1){
     if(num2==2){
       if(num3==3){
         if(num4==4){
    

   if(num1==1){
       if(num2==2){
           if(num3==3){
               if(num4==4){
        


   if(num1==1){
           if(num2==2){
                   if(num3==3){
                           if(num4==4){
                       
  
  가장 이상적인 들여쓰기는 Space bar 2~4번 정도이다.


  핵심은 많지도 적지도 않게 적당하게 들여쓰는 것이다. 

</code>
</pre>


8. 내어쓰기를 하지마라
  
  내어 쓴 부분을 강조하고자 내어 쓰기를 했다는 작성자.
<pre>
<code>
            if(a>=b){
    a++;
    b--;

    printf(“어이가없네”);
    }
    
    </pre>
    </code>
