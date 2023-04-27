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
  } while (i < 1 || i > 3);
  printf("선택된 메뉴 = %d\n", i);
  return 0;
}
```

2-1. while 문 (합계 계산)

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

3. 정수형의 올림 변환
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
5.
```
