# 栈 （Stack）

## 栈的定义

- 栈作为一种线性数据结构，特征是**数据的插入和删除只能通过一端来实现**。这一端称为栈顶，另  外一端称为栈底。

----


## 栈的方法

- 初始化（InitStack)

- 出栈   (Pop)

- 压栈   (Push)

- 判满   (StackFull)

- 判空   (StackEmpty)

- 清空   (Clear)

- 遍历  （Display）



------



## 栈的衍生

- 栈帧：在C语言中每个栈帧对应着一个未运行完成的函数。栈帧中保存着该函数的返回地址和局部变量
- 逆序输出：输出次序与处理次序颠倒
- 递归嵌套
- 栈混洗
- 延迟缓冲
- 栈式计算：



----

```
#include <iostream>
#include <string>
#define N 10

using namespace std;

template <class t>
class stark
{
public:

void Clear()
{
    int i=0;
    for(;i<10;++i)
    {
        a[i]='0';
    }
    this->flag=0;
}
void putoutt()
{
	if((this->flag>-1)?1:0)
	{
		cout<<a[0]<<endl;
		a[0] = '0';
	}
}
void putin()

{
	if((this->flag<N)?1:0)
    {
        cin>>a[this->flag];
		cout<<this->flag+1<<"/10"<<endl;
			this->flag++;
	}
	else
	{
			if(this->flag==N)
	{
		cout<<"FULL"<<endl;
	}
	else if(this->flag==-1)
	{
		cout<<"EMPTY"<<endl;
	}
	}
}
	void putout()
{
	this->flag--;
	if((this->flag>-1)?1:0)
	{
		cout<<a[this->flag]<<" "<<endl;
		cout<<this->flag<<"/10"<<endl;
	}
	else
	{
			if(this->flag==N)
	{
		cout<<"FULL"<<endl;
	}
	else
	{
		cout<<"EMPTY"<<endl;
	}
		this->flag++;
	}
}

~stark()
{
	cout<<"END"<<endl;
}

private:
	t a[N];
	int flag=0;
};

#include <iostream>
#include <string>
#include "hnc.cpp"
using namespace std;

 int main()
{
	stark <string> t1;
	int flag1=1;
	char work;
	for(;flag1==1;)
	{
		cin>>work;
		switch (work)
		{
  		 case '+': t1.putin(); break;
		 case '-': t1.putout(); break;
		 case '!': flag1=0; break;
		 case '=': t1.putoutt();break;
		 case '~': t1.Clear();break;
		}
	}
	return 0;
}


```





