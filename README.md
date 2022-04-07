#define CRT_SECLRE_NO_WRNINGS 1
#include <stdio.h>
#include<string.h>
struct Book
{
    char name[20];
    short price;
};//创建一个结构体类型  结构成员操作符. ->
int main()
{
    //利用结构体类型-创建一个该类型的结构体变量
    struct Book b1 = { "c语言程序设计",55 };
    struct Book* pb = &b1;
    printf("书名：%s\n", b1.name); //c语言程序设计
    printf("价格：%d\n", b1.price);
    //结构体变量.成员
    printf("书名：%s\n", (*pb).name);
    printf("价格：%d\n", (*pb).price);
    //利用pb打印书名和价格
    printf("书名：%s\n", pb->name);
    printf("价格：%d\n", pb->price);
    //结构体->成员
    b1.price = 15; //price是变量，name是数组不可这样修改
    strcpy(b1.name,"C++");//strcpy-string copy-字符串拷贝-库函数 string.h
    printf("修改后的价格：%d\n", b1.price);
    printf("修改后的名字：%s\n", b1.name);
    return 0;
