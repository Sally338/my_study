顺序表基本操作
1.查找 查找x返回x位置
int Line_search(int x,int n,int data[])
{
  int j,i;
  for(j=0;j<n;j++)
  {
    if(data[j]==x) return ++j;
  }
  retrun 0;
}
2.插入 data[]第i个位置插入e
int Line_insert(int i,int n,int e,int data[],int maxlen)
  {
    int j;
    if((i<1)||(i>n+1)) AfxMessageBox("插入位置非法");
    else
      {
        if(n>=maxlen) AfxMessageBox("溢出");
        else
          {
            for(j=n-1;j>=i-1;j--) data[j+1]=data[j];
            data[i-1]=e;
            n=n+1;
          }
        }
      return n;
    }
    3.删除第i个位置元素
    int Line_delete(int i,int n,int data[])
      {
        int j;
        if(n==0)
          {
            AfxMessageBox("表空！");
            return 0;
          }
        else
          {
            if((i<1)||(i>n)) AfxMessageBox("删除位置非法！")；
            else
              {
                for(j=i;j<=n-1;j++) data[j-1]=data[j];
                n=n-1;
              }
          }
        return n;
      }
