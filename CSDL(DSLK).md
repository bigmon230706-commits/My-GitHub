#include<stdio.h>
#include<conio.h>

//danh sách liên kết

//khai báo nút
typedef int ItemType;
typedef struct Node
{
  ItemType info;
  Node* next;
}Node;

//tạo nút chứa giá trị x
Node* createNode(ItemType x)
{
  Node* p = (Node*)malloc(sizeof(Node));
  if(p == NULL)
  {
    printf("không đủ bộ nhó cáp phát!!!");
    getch();
    return NULL;
  }
  p->info = x;
  p->next = NULL;
  return p;
}

//xuất nội dung của nút ra màn hình
