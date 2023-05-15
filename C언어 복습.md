1. do while 문 
```
#include <stdio.h>
int main(void) {
  int i = 0;
  do {
    printf("1---새로만들기\n");
    printf("2---파일열기\n");
    printf("3---파일닫기\n");
    printf("하나를 선택하시오:");
    scanf("%d", &i);
  } 
  
  while (i < 1 || i > 3);
  printf("선택된 메뉴 = %d\n", i);
  return 0;
}
```

2. while 문 (합계 계산)

```
#include <stdio.h>

int main() {
  int n, sum = 0, i = 1;
  printf("정수를 입력하시오:");
  scanf("%d", &n);

  while (i <= n) 
  {
    sum += i;  sum = sum + 1
    i++;
  }

  printf("1부터 %d까지의 합은 %d입니다.", n, sum);
  return 0;
}
```

3. 정수형의 올림 변환 (char형 overflow 발생)
```
#include <stdio.h>
int main(void)
{
    char c;
    int i;
    float f;

    c = 10000; //내림변환
    i = 1.23456 + 10; //내림변환
    f = 10 + 20; //올림변환
    
    printf("c = %d, i = %d, f = %f \n", c, i, f);
    return 0;

```
4. 함수 호출
```
#include <stdio.h>

void print_stars()
{
for (int i = 0; i < 30; i++)

    printf("*");

}   

int main(void)
{
    print_stars();
    printf("\nHello World!\n");
    print_stars();
    
    return 0;
}
```
5. 거스름돈 계산
```
#include <stdio.h>
int main(void)
 {
    int money, change;
    int price, c5000, c1000, c500, c100;

    printf("물건 값을 입력하시오: ");
    scanf("%d", &price); // 물건 값을 입력받는다.
    printf("투입한 금액을 입력하시오: ");
    scanf("%d", &money); // 물건 값을 입력받는다.

    change = money - price; // 거스름돈을 change에 저장
    c1000 = change / 1000; // 남은 잔돈에서 1000원권의 개수를 계산한다.
    change = change % 1000; //나머지 연산자를 사용하여 남은 잔돈을 계산한다.
    c500 = change / 500; // 남은 잔돈에서 500원 동전의 개수를 계산한다.
    change = change % 500; //나머지 연산자를 사용하여 남은 잔돈을 계산한다

    printf("\n천원권: %d장\n", c1000);
    printf("오백원 동전: %d개\n", c500);
    printf("백원 동전: %d개\n", c100);

    return 0;
}
```
6. double형 실수의 합계, 나눗셈 계산
```
#include <stdio.h>

int main() {
    
    double x, y, result;

    printf ("두 개의 실수를 입력하시오: ");
    scanf("%lf %lf",&x, &y);

    result = x + y;
    printf("%f + %f = %f\n", x, y, result);

    result = x / y;
    printf("%f / %f = %f\n", x, y, result);

return 0;
}
```
7. ++! 증감연산자
```
#include <stdio.h>
int main(void)
{
    int x=10, y=10;

    printf("x=%d\n", x);
    printf("++x의 값=%d\n", ++x);
    printf("x=%d\n\n", x);

    printf("y=%d\n", y);
    printf("y++의 값=%d\n", y++);
    printf("y=%d\n", y);

    return 0;
}
```
8. if문 gerchar
```
#include <stdio.h>
int main(void)

{
    char ch;
    printf("문자를 입력하시오:");

    ch = getchar();
    if( ch >='A' && ch <= 'Z')
        printf("%c는 대문자입니다.\n", ch);
    else if (ch >= 'a' && ch <= 'z')
        printf("%c는 소문자입니다.\n", ch);
    else if (ch >= '0' && ch <= '9')
        printf("%c는 숫자입니다.\n", ch);
    else
        printf("%c는 기타문자입니다.\n", ch);
        
        return 0;
}
```
9. if, else (max함수)
```
#include <stdio.h>


int max(int x, int y)
{
    if (x > y)
    
       return x;

    else
        return y;
}
int main(void)
{
    int x, y, larger;

    printf("정수 2개를 입력하시오:");
    scanf("%d %d", &x, &y);

    larger = max (x, y);
    printf("더 큰 값은 %d입니다. \n",larger);

    return 0;
}
```
10. get_integer 함수
```
#include <stdio.h>

int get_integer() 
{
    int value;
    printf("정수를 입력하시오: ");
    scanf("%d", &value);
    return value;
}

int add(int x, int y)
{
    return x + y;
}
int main(void)
{
    int x = get_integer();
    int y = get_integer();
    int sum = add(x, y);
    printf("두수의 합은 %d입니다.\n", sum);
    return 0;
}
```

11. 구구단
```.c
#include <stdio.h>

int main(void) {

  int dan = 2;

  do {
    int count = 1;
    printf("구구단\n");
    do {
      printf("%d * %d = %d\n", dan, count, dan * count);
      count++;
    } while (count <= 9);

    printf("/n/n");
    dan++;
  } while (dan <= 2);

  return 0;
}
```
12. * 30개씩 10줄 찍기
```.c
#include <stdio.h>

int main(void) {
  int i = 0, j = 0;

  for(i = 1; i <= 10; i++) {
    
      for(j = 1; j <= 30; j++){
      printf("*");
  }
  printf("\n");
  }
  return 0;
}
```
12 -1 (for - while 문)
```.c
#include <stdio.h>

int main(void) {

  int i = 0, j;

  for (i = 1; i <= 10; i++) {
    j = 1;
    while (j <= 30) {
      j = j + 1;
      printf("*");
    }

    printf("\n");
  }
  return 0;
}
```
