# day_3
国庆后第一天
#include <stdarg.h>
int sum(int n, ...);
int sum(int n, ...)
{
	int i, sum = 0;
	va_list vap;
	va_start(vap, n);
	for (i = 0; i < n; i++)
	{
		sum += va_arg(vap,int);//确认变量和字符格式
	}
	va_end(vap);
	return sum;
}

//va为可变参数

int main()
{
	int result = sum(4, 3, 2, 5, 76);
	printf("该组的和为：%d", result);
	return 0;
}
