# 2023-02-11-ROKA
Not completed (2023-02-11 Backjoon 1081 title : sum)

#include <stdio.h>

int sum = 0;

int main()
{
  int j = 1;
  while(j) {
    int i,k = 0;
      scanf("%d %d", &i, &k);
      if(((i >= 0) && (i <= 2000000000)) && ((k >= 0) && (k <= 2000000000))) {
        if((i > 99) || (k > 99))
          if((i > 9) || (k > 9)) {
            for(int q = i; q <= k; q++) { // 항상 i는 k보다 크다는 조건을 만족해야함.
              sum += q % 10;
            }
          }
        }
      else
        break;
  }
      printf("범위를 넘었기 때문에 종료이며 더해진값은 %d이다.\n", sum);
    return 0;
}

// 2000000000 % 1000000000
// 2000000000 % 100000000
// 2000000000 % 10000000
// 2000000000 % 1000000
// 2000000000 % 100000
// 2000000000 % 10000
// 2000000000 % 1000
// 2000000000 % 100
// 2000000000 % 10
// 2000000000 % 1

// if(i <10 i<100 i<1000 i<10000 i<100000 i<1000000 i<10000000 i<100000000 i<1000000000)
