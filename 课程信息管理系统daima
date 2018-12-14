#include<stdio.h>
#include<windows.h>
#include<stdlib.h>
#include<string.h>
int i=0;
typedef struct
{
    char courseid[20];//课程号
    char coursename[20];//课程名称
    char profession[20];//专业
    char xingzhi[20];//性质
    char xueshi[20];//学时
    char xuefen[20];//学分
} file;
file course[100];
void menu()
{
    printf("                                                  课程管理系统\n");
    printf("                                         $************菜单************$\n");
    printf("                                         $                            $\n");
    printf("                                         $ 浏览数据请输入           1 $\n");
    printf("                                         $                            $\n");
    printf("                                         $ 增加数据请输入           2 $\n");
    printf("                                         $                            $\n");
    printf("                                         $ 修改数据请输入           3 $\n");
    printf("                                         $                            $\n");
    printf("                                         $ 查询数据请输入           4 $\n");
    printf("                                         $                            $\n");
    printf("                                         $ 删除数据请输入           5 $\n");
    printf("                                         $                            $\n");
    printf("                                         $ 退出程序请输入           6 $\n");
    printf("                                         $                            $\n");
    printf("                                         $*****************************\n");
    system("color F5");
}
void see()//浏览数据的功能
{   int j;
    for(j=0; j<i; j++)
    {
        printf("课程号:%s 课程名称:%s 专业:%s 性质:%s 学时:%s 学分:%s\n",course[j].courseid,course[j].coursename,course[j].profession,course[j].xingzhi,course[j].xueshi,course[j].xuefen);
    }
    system("pause");
}
void add()//添加数据
{
    int a;
    printf("请输入增加数据的个数");
    scanf("%d",&a);
    system("cls");
    int b=i+a;
    for(i; i<b; i++)
    {
        printf("请顺序输入课程号 课程名称 专业 性质 学时 学分\n");
        scanf("%s%s%s%s%s%s",course[i].courseid,course[i].coursename,course[i].profession,course[i].xingzhi,course[i].xueshi,course[i].xuefen);
        system("cls");
    }
}
void change()//修改数据
{
    char a[20];
    printf("请输入想要修改的课程名称");
    scanf("%s",a);
    system("cls");
    int j;
    for(j=0; j<i; j++)
    {
        if(strcmp(course[j].coursename,a)==0)
        {
            printf("请顺序输入课程号 课程名称 专业 性质 学时 学分\n");
            scanf("%s%s%s%s%s%s",course[j].courseid,course[j].coursename,course[j].profession,course[j].xingzhi,course[j].xueshi,course[j].xuefen);
            break;
        }
    }
}
void search()//查询功能
{
    int a,j;
    char n[20];
    printf("按课程名称搜索请按1 按课程号搜索请按2");
    scanf("%d",&a);
    system("cls");
    if(a==1)
    {
        printf("请输入课程名称");
        scanf("%s",n);
        system("cls");
        for(j=0; j<i; j++)
        {
            if(strcmp(course[j].coursename,n)==0)
            {
                printf("课程号:%s 课程名称:%s 专业:%s 性质:%s 学时:%s 学分:%s\n",course[j].courseid,course[j].coursename,course[j].profession,course[j].xingzhi,course[j].xueshi,course[j].xuefen);
            }
        }
        system("pause");
    }
    else if(a==2)
    {
        printf("请输入课程号");
        scanf("%s",n);
        system("cls");
        for(j=0; j<i; j++)
        {
            if(strcmp(course[j].courseid,n)==0)
            {
                 printf("课程号:%s 课程名称:%s 专业:%s 性质:%s 学时:%s 学分:%s\n",course[j].courseid,course[j].coursename,course[j].profession,course[j].xingzhi,course[j].xueshi,course[j].xuefen);
            }
        }
        system("pause");
    }
}
void dell()//删除功能
{
    char v[20];
    printf("请输入你要删除的课程号");
    scanf("%s",v);
    for(int j=0;j<i;j++)
    {
        if(strcmp(v,course[j].courseid)==0)//字符串比较
        {
            for(int k=j;k<i-1;k++)//将查询到的数据下一位向前挪一位
            {
                strcpy(course[k].courseid,course[k+1].courseid);//字符串拷贝函数，把后面的字符串赋给前面的字符串，下同
                strcpy(course[k].coursename,course[k+1].coursename);
                strcpy(course[k].profession,course[k+1].profession);
                strcpy(course[k].xingzhi,course[k+1].xingzhi);
                strcpy(course[k].xueshi,course[k+1].xueshi);
                strcpy(course[k].xuefen,course[k+1].xuefen);
            }
            strcpy(course[i-1].courseid,"");//将最后一位置为空
            strcpy(course[i-1].coursename,"");
            strcpy(course[i-1].profession,"");
            strcpy(course[i-1].xingzhi,"");
            strcpy(course[i-1].xueshi,"");
            strcpy(course[i-1].xuefen,"");
            i--;//将数据总数减少一个
            break;//跳出循环
        }
    }

}
int main()
{
    while(1)
    {
        system("cls");
        menu();
        int a;
        scanf("%d",&a);
        system("cls");
        switch (a)
        {
        case 1:see();
            break;
        case 2:add();
            break;
        case 3:change();
            break;
        case 4: search();
            break;
        case 5:dell();
            break;
        case 6: exit(0);
        default:printf("请重新输入");
        }
    }
    return 0;
}

