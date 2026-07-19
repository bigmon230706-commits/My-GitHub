#include<stdio.h>
#include<conio.h>

//danh sách liên kết

//khai báo nút
typedef int ItemType;
typedef struct Node
{
  ItemType info;
  struct Node* next;
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
void showNode(Node* p)
{
  printf("%4d", p->info);
}

//xóa nút khỏi bộ nhớ
void deleteNode(Node* &p)
{
  if(p == NULL)
    return;
  p->next = NULL;
  delete p;
}

//khai báo list
typedef struct List
{
  struct List* Head;
  struct List* Tail;
} List;

//khởi tạo list
void initList(List &l)
{
  l.Head = NULL;
  l.Tail = NULL;
}

//kiểm tra danh sách rỗng
int isEmpty(List l)
{
  if(l.Head = NULL)
    return 1;
  else
    return 0;
}

//duyệt danh sách
void showList(List l)
{
  if(isEmpty(l) == 1)
  {
    printf("Danh sách đang rỗng!!!");
    return;
  }
  for(Node* p = Head; p != NULL; p = p->next)
  {
    showNode(p);
    printf(" -> ");
  }
printf("NULL);

//thêm nút có giá trị vào đầu danh sách
