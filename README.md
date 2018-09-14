# 9.14.2
数组的传递
// 9.14.3数组的传递和输出.cpp : 定义控制台应用程序的入口点。
// 数组的名称为数组首元素的地址，所以数组在函数间的传递其实是地址的传递，形参的修改将直接反应在实参中

#include "stdafx.h"
#include<iostream>
using namespace std;

void Row_Sum(int a[][4],int b){
	for(int i=0;i<b;i++){
		for(int j=0;j<4;j++){
			a[i][0]+=a[i][j];
		}
	}
}

int _tmain(int argc, _TCHAR* argv[])
{
	int table[3][4]={1,2,3,4,3,4,5,6,2,3,4,5};
	for(int i=0;i<3;i++){
		for(int j=0;j<4;j++){
			cout<<table[i][j]<<"   ";
		}
	}
	cout<<endl;
	Row_Sum(table,3);
	for(int i=0;i<3;i++){
		cout<<"Sum of row "<<i<<" is "<<table[i][0]<<endl;
			}
	return 0;
}

