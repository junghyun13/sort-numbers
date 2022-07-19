# sort-numbers
# c program
# There are numbers in values, and let's use qsort() to sort the numbers in small order! values안에 숫자가 있는데 그 숫자를 작은 순서대로 정리하는데 qsort()를 이용해보자!
#include <stdio.h>
#include <stdlib.h>
int values[]={98,23,99,37,16};
int compare(const void *a,const void *b){
	return (*(int *)a-*(int*)b);
}
int main(void){
	int n;
	int values[]={98,23,99,37,16};
	qsort(values,5,sizeof(int),compare);
	printf("정렬후 배열:");
	for(n=0;n<5;n++){
		printf("%d ",values[n]);
	}
	printf("\n");
    return 0;
}
#result--> 16 23 37 98 99 
