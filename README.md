#include<stdio.h>
#include<stdlib.h>
//#include<conio.h>
#include<string.h>
#include<stdbool.h>
// variables

int code[100];
char name[100][50];
int qty[100];
double price[100],total[100],payment[100],dis[100];
int i,n,j,op;
int codee;
char namee[100];
int qtyy;
double pricee;
double totall;
double paymentt;
double diss;
bool check = false;
int b = 0;
int opsearch;
// function
void Input()
{
    printf("Enter Code  : ");scanf("%d",&code[i]);fflush(stdin);
    printf("Enter Name  : ");gets(name[i]);
    printf("Enter Qty   : ");scanf("%d",&qty[i]);
    printf("Enter Price : ");scanf("%lf",&price[i]);
}
double Total()
{
    total[i] = price[i] * qty[i];
    return total[i];
}
double Disscount()
{
    if(Total() >= 1 && Total() <= 20)
    {
        dis[i] = (Total()*10)/100;
    }
    else if(Total() > 20 && Total() <= 40)
    {
        dis[i] = (Total()*20)/100;
    }
    else if(Total() > 40 && Total() <= 60)
    {
        dis[i] = (Total()*30)/100;
    }
    else
    {
        dis[i] = (Total()*50)/100;
    }
    return dis[i];
}
double Payment()
{
    payment[i] = Total() - Disscount();
    return payment[i];
}
void Header()
{
    printf("%-12s %-12s %-12s %-12s %-12s %-12s %-12s\n","Code","Name","Qty","Price","Total","Discount","Payment");
}

void Display()
{
    printf("%-12d %-12s %-12d %-12.2lf %-12.lf %-12.2lf %-12.2lf\n",code[i],name[i],qty[i],price[i],Total(),Disscount(),Payment());
}
// block main function
int main()
{
    do{
        printf("=====================[MENU]=====================\n");
        printf("[1 - Input DATA  ]\n");
        printf("[2 - View DATA   ]\n");
        printf("[3 - Search DATA ]\n");
        printf("[4 - Update DATA ]\n");
        printf("[5 - Delete DATA ]\n");
        printf("[6 - Insert DATA ]\n");
        printf("[7 - Add DATA    ]\n");
        printf("[8 - Sort DATA  ]\n");
        printf("[9 - Change DATA ]\n");
        printf("[10 - Exit DATA  ]\n");
        printf("=============================================\n");
        printf("Plase select one option from menu : ");scanf("%d",&op);
        switch(op)
        {
            case 1:{
                printf("Enter Number of Product : ");scanf("%d",&n);
                for(i=0;i<n;i++)
                {
                    printf("================[000%d]================\n",i+1);
                    Input();
                }
                break;
            }
            case 2:{
                Header();
                for(i=0;i<n;i++)
                {
                    Display();
                }
            }break;
            case 3:
            {
                int opsearch;char searchname[100];
                int searchcode; double searchtotal;
                bool check = false;
                printf("\t\t1 - Search by Name\n");
                printf("\t\t2 - Search by Code\n");
                printf("\t\t3 - Search by Total\n");
                printf("Please select one option by search : ");scanf("%d",&opsearch);
                switch(opsearch)
                {
                    case 1:{
                        
                        printf("Enter Name to Search : ");fflush(stdin);gets(searchname);
                        Header();
                        for(i=0;i<n;i++)
                        {
                            if(strcmp(name[i],searchname)==0)
                            {
                                Display();
                                check = true;
                            }
                        }
                        if(check==false)
                        {
                            printf("Search Not Found!\n");
                        }
                        else
                        {
                            printf("Search Product Found : \n");
                        }
                        break;
                    }
                    case 2:{
                        printf("Enter Code to Search : ");scanf("%d",&searchcode);
                        Header();
                        for(i=0;i<n;i++)
                        {
                            if(code[i] == searchcode)
                            {
                                Display();
                                check = true;
                            }
                        }
                        if(check==false)
                        {
                            printf("Search Not Found!\n");
                        }
                        else
                        {
                            printf("Search Product Found : \n");
                        }
                        break;
                    }
                    case 3:{
                        printf("Enter Total to Search : ");scanf("%lf",&searchtotal);
                        Header();
                        for(i=0;i<n;i++)
                        {
                            if(Total() == searchtotal)
                            {
                                Display();
                                check = true;
                            }
                        }
                        if(check==false)
                        {
                            printf("Search Not Found!\n");
                        }
                        else
                        {
                            printf("Search Product Found : \n");
                        }
                        break;
                    }
                } 
            }break;
            case 4:{
                int opsearch;char searchname[100];
                int searchcode; double searchtotal;
                bool check = false;
                printf("\t\t1 - Search by Name to Update\n");
                printf("\t\t2 - Search by Code to Update\n");
                printf("Please select one option by search : ");scanf("%d",&opsearch);
                switch(opsearch)
                {
                    case 1:{
                        printf("Enter Name to Search : ");fflush(stdin);gets(searchname);
                        for(i=0;i<n;i++)
                        {
                            if(strcmp(name[i],searchname)==0)
                            {
                                Input();
                                check = true;
                            }
                        }
                        if(check==false)
                        {
                            printf("Update Not Success...!\n");
                        }
                        else
                        {
                            printf("Update successfuly....\n");
                        }
                        break;
                    }
                    case 2:{
                        printf("Enter Code to Search : ");scanf("%d",&searchcode);
                        Header();
                        for(i=0;i<n;i++)
                        {
                            if(code[i] == searchcode)
                            {
                                Input();
                                check = true;
                            }
                        }
                        if(check==false)
                        {
                            printf("Update Not Successful...!\n");
                        }
                        else
                        {
                            printf("Update Successful..\n");
                        }
                        break;
                    }
                }
            }break;
            case 5:{
                int opsearch;char searchname[100];
                int searchcode; double searchtotal;
                bool check = false;
                printf("\t\t1 - Search by Name to Delete\n");
                printf("\t\t2 - Search by Code to Delete\n");
                printf("Please select one option by search : ");scanf("%d",&opsearch);
                switch(opsearch)
                {
                    case 1:{
                        printf("Enter Name to Search : ");fflush(stdin);gets(searchname);
                        for(i=0;i<n;i++)
                        {
                            if(strcmp(name[i],searchname)==0)
                            {
                                for(j=i;j<n;j++)
                                {
                                    code[j]=code[j+1];
                                    strcpy(name[j],name[j+1]);
                                    qty[j]=qty[j+1];
                                    price[j]=price[j+1];
                                    total[j]=total[j+1];
                                    dis[j]=dis[j+1];
                                    payment[j]=payment[j+1];
                                }
                                n--;
                                check=true;
                            }
                        }
                        if(check==false)
                        {
                            printf("Delete Not Success...!\n");
                        }
                        else
                        {
                            printf("Delete successfuly....\n");
                        }
                        break;
                    }
                    case 2:{
                        printf("Enter Code to Search : ");scanf("%d",&searchcode);
                        Header();
                        for(i=0;i<n;i++)
                        {
                            if(code[i] == searchcode)
                            {
                                for(j=i;j<n;j++)
                                {
                                    code[j]=code[j+1];
                                    strcpy(name[j],name[j+1]);
                                    qty[j]=qty[j+1];
                                    price[j]=price[j+1];
                                    total[j]=total[j+1];
                                    dis[j]=dis[j+1];
                                    payment[j]=payment[j+1];
                                }
                                n--;
                                check=true;
                            }
                        }
                        if(check==false)
                        {
                            printf("Update Not Successful...!\n");
                        }
                        else
                        {
                            printf("Update Successful..\n");
                        }
                        break;
                    }
                }
            }break;
            case 6:{
                int opsearch;char searchname[100];
                int searchcode; double searchtotal;
                bool check = false;
                printf("\t\t1 - Search by Name to Inserts\n");
                printf("\t\t2 - Search by Code to Inserts\n");
                printf("Please select one option by search : ");scanf("%d",&opsearch);
                switch(opsearch)
                {
                    case 1:{
                        printf("Enter Name to Search : ");fflush(stdin);gets(searchname);
                        for(i=0;i<n;i++)
                        {
                            if(strcmp(name[i],searchname)==0)
                            {
                                for(j=n;j>=i;j--)
                                {
                                    code[j]=code[j-1];
                                    strcpy(name[j],name[j-1]);
                                    qty[j]=qty[j+1];
                                    price[j]=price[j-1];
                                    total[j]=total[j-1];
                                    dis[j]=dis[j-1];
                                    payment[j]=payment[j-1];
                                }
                                n++;
                                Input();
                                check=true;
                                break;
                            }
                        }
                        if(check==false)
                        {
                            printf("Insert Not Success...!\n");
                        }
                        else
                        {
                            printf("Insert successfuly....\n");
                        }
                        break;
                    }
                    case 2:{
                        printf("Enter Code to Search : ");scanf("%d",&searchcode);
                        Header();
                        for(i=0;i<n;i++)
                        {
                            if(code[i] == searchcode)
                            {
                                for(j=n;j>=i;j--)
                                {
                                    code[j]=code[j-1];
                                    strcpy(name[j],name[j-1]);
                                    qty[j]=qty[j+1];
                                    price[j]=price[j-1];
                                    total[j]=total[j-1];
                                    dis[j]=dis[j-1];
                                    payment[j]=payment[j-1];
                                }
                                n++;
                                Input();
                                check=true;
                                break;
                            }
                        }
                        if(check==false)
                        {
                            printf("Insert Not Successful...!\n");
                        }
                        else
                        {
                            printf("Insert Successful..\n");
                        }
                        break;
                    }
                }
            }break;
            case 7:{
                int add;
                bool check=true;
                printf("Enter number to add : ");scanf("%d",&add);
                for(i=n;i<n+add;i++)
                {
                    Input();
                    check=true;
                }
                n+=add;
                if(check==false)
                {
                    printf("Add Not Successful...!\n");
                }
                else
                {
                    printf("Add successfuly....\n");
                }
            }break;
            case 8:{
                printf("\t\t1 - Sort by Name\n");
                printf("\t\t2 - Sort by Code\n");
                printf("\t\t3 - Sort by Total\n");
                printf("Please select one option by search : ");scanf("%d",&opsearch);
                switch(opsearch)
                {
                    case 1:{
                        for(i=0;i<n;i++)
                        {
                            for(j=i+1;j<n;j++)
                            {
                                if(strcmp(name[i],name[j])>0)
                                {
                                    codee = code[i];
                                    code[i] = code[j];
                                    code[j] = codee;
                                    strcpy(namee, name[i]);
                                    strcpy(name[i], name[j]);
                                    strcpy(name[j],namee);
                                    qtyy = qty[i];
                                    qty[i] = qty[j];
                                    qty[j] = qtyy;
                                    pricee = price[i];
                                    price[i] = price[j];
                                    price[j] = pricee;
                                    totall = total[i];
                                    total[i] = total[j];
                                    total[j] = totall;
                                    diss = dis[i];
                                    dis[i] = dis[j];
                                    dis[j] = diss;
                                    paymentt = payment[i];
                                    payment[i] = payment[j];
                                    payment[j] = paymentt;
                                    b=1;
                                }
                            }
                        }
                        if(b==0)
                        {
                            printf("Sort Not Successful...!\n");
                        }
                        else
                        {
                            printf("Sort Suceesfully...\n");
                        }
                    }break;
                    case 2:{
                        for(i=0;i<n;i++)
                        {
                            for(j=i+1;j<n;j++)
                            {
                                if(code[i] > code[j])
                                {
                                    codee = code[i];
                                    code[i] = code[j];
                                    code[j] = codee;
                                    strcpy(namee, name[i]);
                                    strcpy(name[i], name[j]);
                                    strcpy(name[j],namee);
                                    qtyy = qty[i];
                                    qty[i] = qty[j];
                                    qty[j] = qtyy;
                                    pricee = price[i];
                                    price[i] = price[j];
                                    price[j] = pricee;
                                    totall = total[i];
                                    total[i] = total[j];
                                    total[j] = totall;
                                    diss = dis[i];
                                    dis[i] = dis[j];
                                    dis[j] = diss;
                                    paymentt = payment[i];
                                    payment[i] = payment[j];
                                    payment[j] = paymentt;
                                    b=1;
                                }
                            }
                        }
                        if(b==0)
                        {
                            printf("Sort Not Successful...!\n");
                        }
                        else
                        {
                            printf("Sort Suceesfully...\n");
                        }
                    }break;
                    case 3:{
                        int opsearch;
                        printf("\t\t1 - small to large\n");
                        printf("\t\t2 - large to small\n");
                        printf("Please select one option by search : ");scanf("%d",&opsearch);
                        switch(opsearch)
                        {
                            case 1:{
                                for(i=0;i<n;i++)
                                {
                                    for(j=i+1;j<n;j++)
                                    {
                                        if(total[i]>total[j])
                                        {
                                            codee = code[i];
                                            code[i] = code[j];
                                            code[j] = codee;
                                            strcpy(namee, name[i]);
                                            strcpy(name[i], name[j]);
                                            strcpy(name[j],namee);
                                            qtyy = qty[i];
                                            qty[i] = qty[j];
                                            qty[j] = qtyy;
                                            pricee = price[i];
                                            price[i] = price[j];
                                            price[j] = pricee;
                                            totall = total[i];
                                            total[i] = total[j];
                                            total[j] = totall;
                                            diss = dis[i];
                                            dis[i] = dis[j];
                                            dis[j] = diss;
                                            paymentt = payment[i];
                                            payment[i] = payment[j];
                                            payment[j] = paymentt;
                                            b=1;
                                        }
                                    }
                                }
                                if(b==0)
                                {
                                    printf("Sort Not Successful...!\n");
                                }
                                else
                                {
                                    printf("Sort Suceesfully...\n");
                                }
                            }break;
                            case 2:{
                                for(i=0;i<n;i++)
                                {
                                    for(j=i+1;j<n;j++)
                                    {
                                        if(total[i]<total[j])
                                        {
                                            codee = code[i];
                                            code[i] = code[j];
                                            code[j] = codee;
                                            strcpy(namee, name[i]);
                                            strcpy(name[i], name[j]);
                                            strcpy(name[j],namee);
                                            qtyy = qty[i];
                                            qty[i] = qty[j];
                                            qty[j] = qtyy;
                                            pricee = price[i];
                                            price[i] = price[j];
                                            price[j] = pricee;
                                            totall = total[i];
                                            total[i] = total[j];
                                            total[j] = totall;
                                            diss = dis[i];
                                            dis[i] = dis[j];
                                            dis[j] = diss;
                                            paymentt = payment[i];
                                            payment[i] = payment[j];
                                            payment[j] = paymentt;
                                            b=1;
                                        }
                                    }
                                }
                                if(b==0)
                                {
                                    printf("Sort Not Successful...!\n");
                                }
                                else
                                {
                                    printf("Sort Suceesfully...\n");
                                }
                            }break;
                        }
                    }break;
                }
            }break;
            case 9:{
                system("cls");
            }
            case 10:{
                exit(0);
                //return 0;
            }
        }
    }while(op!=0);
    return 0;
}
