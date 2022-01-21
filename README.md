# magic-code
A very magic homework that I will never forget. (泰勒公式使用计算机计算)

#include <stdio.h>

#include <math.h>

int main()

{

	int i, j, n = 3, count = 1;
  
	long double x, term, a = 1, b = 1, c;
  
	scanf("%lf", &x);
  
	long double sum = x;
  
	do {
  
		for (i = 1; i <= n; i++)
    
		{
    
			a *= x;
      
		}
    
		for (j = 1; j <= n; j++)
    
		{
    
			b *= j;
      
		}
    
		c = double(pow(-1, count));
    
		term = c * (a / b);
    
		sum += term;
    
		n += 2;
    
		count += 1;
    
		a = 1;
    
		b = 1;
    
	} while (fabs(term) >= 1e-5);
  
	printf("%.3lf\n%d", sum, count);
  
	return 0;
  
}
