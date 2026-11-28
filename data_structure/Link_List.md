单链表
struct Lnode
  {
    int data;
    Lnode *next;
  }

单链表建立
Londe *creat_Link_List(int n,int a[])
{
  Lnode *p,*head;
  p=new(Lnode);
  head=p;
  head->next=NULL;

  for(int i=n-1;i>=0;i--)
    {
      p=new(Lnode);
      p->data=a[i];
      p->next=head->next;
      head->next=p;
    }
  return head;
}

查找
