#include "stdio.h"
#include "smallest_digit.h"

int FindSmallest(int InputNumber)
{
    int min = InputNumber % 10;
    InputNumber /= 10;
    while(InputNumber != 0)
    {
        if(min > InputNumber % 10)
        {
            min = InputNumber % 10;
        }
        InputNumber /= 10;
    }
    return min;
}
