---
layout: page
title: Фрагмент кода
---
***Это функция, вычисляющая сумму векторов на GPU:

```
__global__
void sum_vect(int *a, int *b, int *c,int dim)
{
 int id = threadIdx.x + blockIdx.x*blockDim.x;
 if(id < dim)
{
		c[id] = a[id] + b[id];
}
}
```
