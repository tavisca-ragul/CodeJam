#include <assert.h>
#include <limits.h>
#include <math.h>
#include <stdbool.h>
#include <stddef.h>
#include <stdint.h>
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main()
{
    int arr[10][10], row = 0, column = 0, row_size, column_size, itr = 0, sum = 0, max = -99999;
    char temp = 'y';
    while (1) {  
        int end = scanf ("%d%c", &itr, &temp);
        if(end == 1)
            break;
        arr[row][column] = itr;
        column++;
        if(temp == '\n') {
            row++; 
            column = 0;
        }
    }
    row_size = row+1;
    column_size = column;
    for(row = 0; row < row_size-2; row++) {
        for(column = 0; column < column_size-2; column++) {
            sum += arr[row][column] + arr[row][column+1] + arr[row][column+2] + arr[row+1][column+1] + arr[row+2][column] + arr[row+2][column+1] + arr[row+2][column+2];
            if(sum > max)
                max = sum;
            sum = 0;
        }     
    }
    printf("%d", max);
    return 0;
}
