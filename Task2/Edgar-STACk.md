# 栈的学习 7.18

```c++
#include <iostream>
#include <cstdio>
#define MAX 1024
#define Error 0xffffff
using namespace std;

class stack_by_edgar {
private:
	int sp = 0;
	int bp = 0;
	int val[MAX] = { 0 };
public:
	int pop()
	{
		if (this->is_empty() == 1)
		{
			printf("ERROE STACK IS EMPTY------------------[*]\n");
			return Error;
		}
		int retval = this->val[sp];
		this->sp--;
		return retval;
	}
	void push(int num)
	{
		if (this->is_full() == 1)
		{
			printf("ERROR STACK IS FULL------------------[*]\n");
			return;
		}
		this->sp++;
		this->val[sp] = num;
	}
	bool is_full()
	{
		if (this->sp >= MAX)
		{
			return 1;
		}
		return 0;
	}
	bool is_empty()
	{
		if (this->sp <= this->bp)
		{
			return 1;
		}
		return 0;
	}
	void clear()
	{
		this->sp = 0;
		this->bp = 0;
		memset(this->val, 0, sizeof(this->val));
	}
	int pop_bp()
	{
		if (this->is_empty() == 1)
		{
			printf("ERROR STACK IS EMPTY\n");
		}
		int retval = this->val[this->bp];
		this->bp++;
		return retval;
	}
};

int main()
{
	stack_by_edgar a;
	a.push(1);
	a.push(2);
	a.push(3);
	int kkp = a.pop();
	kkp = a.pop();
	kkp = a.pop();
	kkp = a.pop();
	cout << kkp;
	return 0;
}
```

先上本人写的实现代码，栈在计算机中算是一个比较简单的数据结构，所以说也就比较重要了，之后就是 他的特点有啥？

* 先进后出
* 单列数据结构

其他好像也没啥可写的特点啊，

然后就是在计算机中这是一个非常重要的数据结构，比如说在函数调用的情况下，函数以及参数就是入栈和出栈的排列关系，所以就是一种微妙的关系了，毕竟内存是线性结构，就特别好玩了。

然后汇编方面

```assembly
push 
pop
esp
ebp
```

记住这三个参数大概就可以了，别的没啥好玩的了