#include<stdio.h>
#include<conio.h>
#include<string.h>
#include<windows.h>
#include<stdlib.h>
void gotoxy(int x,int y){
	COORD coord = {x, y};
	SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE),coord);
}
void wel()
{
	int x5=33;
	int y5=1;
	system("cls");
	system("Color 6");
   gotoxy(x5,y5++);printf("_____________________");
	gotoxy(x5,y5++);printf("|WELCOME TO BOOKSHOP|");
	gotoxy(x5,y5++);printf("---------------------");
	
}
void Pro()
{
	int x6=34;
	int y6=1;
	system("cls");
	system("Color B");
   gotoxy(x6,y6++);printf("__________________");
	gotoxy(x6,y6++);printf("|BOOK INFORMATION|");
	gotoxy(x6,y6++);printf("------------------");
}
void Sstaff()
{
	int x5=36;
	int y5=1;
	system("cls");
	system("Color 9");
   gotoxy(x5,y5++);printf("___________________");
	gotoxy(x5,y5++);printf("|STAFF INFORMATION|");
	gotoxy(x5,y5++);printf("-------------------");
}
void welcom()
{
	int x5=36;
	int y5=11;
	system("cls");
	system("Color B");
   gotoxy(x5,y5++);printf("_____________________");
	gotoxy(x5,y5++);printf("|WELCOME TO BOOKSHOP|");
	gotoxy(x5,y5++);printf("---------------------");
	Sleep(1000);
	system("cls");
}
void sel_order()
{
	int x8=35;
	int y8=1;
	system("cls");
	system("Color D");
   gotoxy(x8,y8++);printf("___________________________");
	gotoxy(x8,y8++);printf("|SELL AND ORDER INFORMATION|");
	gotoxy(x8,y8++);printf("---------------------------");
}
void Header_shop()
{
	printf("%30s%10s%10s%10s%10s\n","ID","NAME","QYT","PRICE","STATUS");
}
void Header_staff()
{
	printf("%10s%15s%15s%15s%15s%15s%13s\n","ID","NAME","GENDER","POSITION","SALARY","PHONE","ADDRESS");
}
void Header_sell()
{
	
}
void Header_date()
{
	
}
void loadingbar()
{
	system("Color 2");
    char x =219;
    //char x =178;
    //char x =175;
    //char x =177;
    
  printf("\n""\t\t\t\t        LOADING.....\t\t\t\t\n");
  
  printf("\t\t\t");
  for(int i=0;i<40;i++)
  {
    printf("%c",x);
    Sleep(80);
  }
  system("cls");
}
int main()
{
	 // Shop
     char Product[5][50][20];
   // Sell
     char Sell[5][60][10];
   //Staff
     char Staff[6][70][10];
     
   FILE *fpshop;
   FILE *fpstaff;
   FILE *newstaff;
   FILE *newshop;
   FILE *fpcshop;
   FILE *rd;
   FILE *sl;
   FILE *m;
   char answer[10];
   int i,j,n,op;
   int op1,n1;
   int m1,m2;
//   int a[100];
//   int b[100];
//   int total[100];
 	
	int d=0;																																																																																																															  	
	char temp[100];	  			 																																																																																																															  	
	do{
		
	   system("cls");
	   system("Color E");
      char uname[10];
      char password[10];
   	printf("\n\t\t\t\t\t<<>>__LOGIN__<<>>\n");
	   printf("\t\t\t\t\tUser Name :");scanf("%s",&uname);
	  if(strcmp(uname,"A")==0)
     {  
	     printf("\t\t\t\t\tPassword  :");scanf("%s",&password);
        if(strcmp(password,"1")==0)
		   { 
            system("cls");
	         loadingbar();
	         system("cls");
				welcom();  
	        do
	         {  
			 	
		         system("cls");
				   wel();	 	     
		         int x=30;
          	   int y=4;  
	            gotoxy(x,y++);printf("======>> OPTION <<=========");
               gotoxy(x,y++);printf("[1] -->> Book Information");
               gotoxy(x,y++);printf("[2] -->> Staff Information");
               gotoxy(x,y++);printf("[3] -->> Order And Sell Information");
               gotoxy(x,y++);printf("[4] -->> Exit");
               gotoxy(x,y++);printf("Please Chose Option___");scanf("%d",&op);
	            switch(op)
	            {
		            case 1:
                  {
						  do
			            { 
                       system("cls");
                       system("Color C");
                       int x1=35;
                       Pro();
                       int y1=4;
                       gotoxy(x1,y1++);printf(":::>> OPTION <<:::");
                       gotoxy(x1,y1++);printf("(1)<---> Input");
                       gotoxy(x1,y1++);printf("(2)<---> Show");
                       gotoxy(x1,y1++);printf("(3)<---> Search");
                       gotoxy(x1,y1++);printf("(4)<---> Sort");
                       gotoxy(x1,y1++);printf("(5)<---> Delete");
                       gotoxy(x1,y1++);printf("(6)<---> Update");
                       gotoxy(x1,y1++);printf("(7)<---> History");
                       gotoxy(x1,y1++);printf("(8)<---> Back");
                       gotoxy(x1,y1++);printf("Please Chose Option...");scanf("%d",&op1);
                       system("cls");
                       switch(op1)
                        {
          	              case 1:
        		               {
        							    	
 		 	                     system("Color 3");
							         fpcshop=fopen("SHOP2.txt","a");        
       		                  fpshop=fopen("SHOP.txt","a");
		         	            if(fpshop==NULL)
			                     {
			 	                    printf("\t\tError To Create File..!!\n");			
                              }
		                        printf("\t\t\tEnter Number Of Product = ");scanf("%d",&n);
		                        for(i=0;i<n;i++)
		                        {
                                 printf("\t\t\t PRODUCT #%d\n",i+1);
			                        printf("\t\tInput Book ID = ");fflush(stdin);scanf("%s",&Product[i][1]);fflush(stdin);
		                           printf("\t\tInput Book Name = ");scanf("%s",&Product[i][2]);
                                 printf("\t\tInput Book QTY = ");scanf("%s",&Product[i][3]);fflush(stdin);
	                              printf("\t\tInput Book Price = ");scanf("%s",&Product[i][4]);
							            printf("\t\tInput Status = ");scanf("%s",&Product[i][5]);	 				             
			                        fprintf(fpshop,"%30s%10s%10s%10s%10s\n",Product[i][1],Product[i][2],Product[i][3],Product[i][4],Product[i][5]);
										  	fprintf(fpcshop,"%30s%10s%10s%10s%10s\n",Product[i][1],Product[i][2],Product[i][3],Product[i][4],Product[i][5]);																																								 	                       
	                           }
										  printf("\t\t\tSave Complete!!!\n");       
					              fclose(fpshop);
									  fclose(fpcshop);    
                           }break;
                           case 2:
              	            {
                              system("Color 2");
           		  	            Header_shop();	   
        		                  fpshop=fopen("SHOP.txt","r");
	         	              if(fpshop==NULL)
			                    {
			 	                    printf("\t\t\tError To Opening File..!!\n");			
                             }  								 
			                    while(fscanf(fpshop," %s%s%s%s%s ",&Product[i][1],&Product[i][2],&Product[i][3],&Product[i][4],&Product[i][5])!=EOF)
									  	{
											printf("\t\t\t<>______________________________________________<>\n");																											                      
                                 printf("%30s%10s%10s%10s$%10s\n",Product[i][1],Product[i][2],Product[i][3],Product[i][4],Product[i][5]);					 	
		                        }
						           fclose(fpshop);																								  	    
		                     }break;
					            case 3:
				               {
				 	           																							 	
					 	          FILE *src;
						           int c=0;																		 											
						           int i=0;
									  char sid[10];																			  											
                             src=fopen("SEARCH.txt","w");
                             fpshop=fopen("SHOP.txt","r");
						           printf("Input ID to Search...");scanf("%s",&sid);
									  Header_shop();									  																															     								 
						           while(fscanf(fpshop," %s%s%s%s%s ",&Product[i][1],&Product[i][2],&Product[i][3],&Product[i][4],&Product[i][5])!=EOF)
                             {
                                 if(strcmp(Product[i][1],sid)==0)
				                     {
			                            c=1;
                                    fprintf(src,"%30s%10s%10s%10s$%10s\n",Product[i][1],Product[i][2],Product[i][3],Product[i][4],Product[i][5]);
                                    printf("\t\t\t<>______________________________________________<>\n");
									         printf("%30s%10s%10s%10s$%10s\n",Product[i][1],Product[i][2],Product[i][3],Product[i][4],Product[i][5]);																																				 							
						               }						 	
                              }																						 																																																									 																																					  
						            fclose(fpshop);
						            fclose(src);																																																  																																																	   
						           if(c==0)
						           {
						  		        printf("Search Not found!!\n");																																								  	
						            }else
					               printf("Search found!!!\n");	 	 		
			                  }break;
					            case 4:
					            {	
										
									 	int m;    	
										int d=0;
										int i=0;
										int n=0;  			 																																																																																																															  	
	  			  	 					char temp[100];
         			            fpshop=fopen("SHOP.txt","r");															 																																	 	
					               while(fscanf(fpshop," %s%s%s%s%s ",&Product[i][1],&Product[i][2],&Product[i][3],&Product[i][4],&Product[i][5])==5)
								      {i++;} 
										n=i;
									   fclose(fpshop);																											  																																																																																										   																																																																																																																																																																												 																																																																																																					 																																																																																																									  							 					    
										   for(i=0;i<n;i++)
											{
											 for(j=i+1;j<n;j++)
											  {
									         if(strcmp(Product[i][2],Product[j][2])>0)
                                    {	
               	                            strcpy(temp,Product[i][1]);
											strcpy(Product[i][1],Product[j][1]);
											strcpy(Product[j][1],temp);	
											
											strcpy(temp,Product[i][2]);
											strcpy(Product[i][2],Product[j][2]);
											strcpy(Product[j][2],temp);	
											
											strcpy(temp,Product[i][3]);
											strcpy(Product[i][3],Product[j][3]);
											strcpy(Product[j][3],temp);	
											
											strcpy(temp,Product[i][4]);
											strcpy(Product[i][4],Product[j][4]);
											strcpy(Product[j][4],temp);	
											
											strcpy(temp,Product[i][5]);
											strcpy(Product[i][5],Product[j][5]);
											strcpy(Product[j][5],temp);
											d=1;				 																										 															 	
                                    }
											  }
										   }
										   fpshop=fopen("SHOP.txt","w");
										   for(i=0; i<n; i++)
											{
										     fprintf(fpshop,"%s %s %s %s %s ",Product[i][1],Product[i][2],Product[i][3],Product[i][4],Product[i][5]);							 												  
										   }	  
										 fclose(fpshop);				 																		  																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																												  																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																														 			 
										if(d==0)
										{
										 	printf("\t\t\t\n Error to Sort!!!\n");	  																																																																																																																			  					
									   }
										else if(d==1)
										{
										  	printf("\t\t\t Sort Successful.....\n");																 																				  					  		  	  																																																																																																																																																																																																																																																																																																																																																																																											
										} 					 		  	 			
				               }break;				 		  	 			
					            case 5:
									{
	 	               
							         FILE *dfp;
                             char d_id[4];
                             int b=0;
                             int i=0;
                             dfp=fopen("DELETE.txt","w");
                             fpshop=fopen("SHOP.txt","r");
                             printf("Input ID to Delete.....");scanf("%s",&d_id);
				                 while(fscanf(fpshop," %s%s%s%s%s ",&Product[i][1],&Product[i][2],&Product[i][3],&Product[i][4],&Product[i][5])!=EOF)
					              { 
                                if(strcmp(Product[i][1],d_id)==0)
                                {
					                    b=1;																																										  																																																													 	
					                 }
					                 else
                                {
				                       fprintf(dfp,"%30s%10s%10s%10s%10s\n",Product[i][1],Product[i][2],Product[i][3],Product[i][4],Product[i][5]);			 																																																																																																														
		                           }																																																																													
				  	               }
						           fclose(fpshop);
						           fclose(dfp);
						           remove("SHOP.txt");
						           rename("DELETE.txt","SHOP.txt");
						           if(b==0)
									  {
					  	              printf("Delete Not Complete...\n");		  								 																																																																																																																																															           	
									  }
						           else 
									  {
									  	printf("Delete Complete..\n");				  																																																																																																																																																																																																																																																																																																																																																																																																																																						  	
									  }
			                  }break;
					            case 6:
					            {
									 	int u=0;     	
                              char u_id[5];  	 																																																																																																																																															
	                           FILE *update;
		                        update=fopen("UPDATE.txt","w");
                              fpshop=fopen("SHOP.txt","r");
			                     printf("Input ID to Update....");scanf("%s",&u_id);
                              int i=0;																	 																																																																																																																																				 
					               while(fscanf(fpshop," %s%s%s%s%s ",&Product[i][1],&Product[i][2],&Product[i][3],&Product[i][4],&Product[i][5])!=EOF)
						            {
                                 if(strcmp(Product[i][1],u_id)==0)
					                  {
											 																                   	
	                                 printf("\t\t\t PRODUCT #%d\n",i+1);
				                        printf("\t\tInput New Book ID = ");fflush(stdin);scanf("%s",&Product[i][1]);fflush(stdin);
			                           printf("\t\tInput New Book Name = ");scanf("%s",&Product[i][2]);
	                                 printf("\t\tInput New Book QTY = ");scanf("%s",&Product[i][3]);fflush(stdin);
		                              printf("\t\tInput New Book Price = ");scanf("%s",&Product[i][4]);
								            printf("\t\tInput New Status = ");scanf("%s",&Product[i][5]); 
                                    u=1;				 	 			 																									 																																																																																																																	 	
						               }
									   	fprintf(update,"%30s%10s%10s%10s%10s\n",Product[i][1],Product[i][2],Product[i][3],Product[i][4],Product[i][5]);						 			 																										 																																																																																																																		
						            }
						           fclose(fpshop);
						           fclose(update);
						           remove("SHOP.txt");
						           rename("UPDATE.txt","SHOP.txt");
									   if(u==0)
										{
										 	printf("\t\t\t\nError to Update!!!");	  																																																																																																																			  					
									   }
										else printf("\t\t\t Update Successful.....");		 	  	
				               }break;
					            case 8:
					            {
					 	   	 		//		Back
			                  }break;
									case 7:
									{
                             system("Color 2");
                             Header_shop();	   
                             fpcshop=fopen("SHOP2.txt","r");
                             if(fpcshop==NULL)
                             {
                                printf("\t\t\tError To Opening File..!!\n");			
                             }  								 
                               while(fscanf(fpcshop," %s%s%s%s%s ",Product[i][1],Product[i][2],Product[i][3],Product[i][4],Product[i][5])!=EOF)
                              {
                                 
										  	printf("\t\t\t<>______________________________________________<>\n");																											                      
                                 printf("%30s%10s%10s%10s$%10s\n",Product[i][1],Product[i][2],Product[i][3],Product[i][4],Product[i][5]);		 	
                              }
                             fclose(fpcshop);		 																																																																																																																																																																																								
								   }break;			 
             	           default:printf("Error Option!!!\n");
				           }
							  printf("\n\t\tPress C to Continue and Press X to Exit....");scanf("%s",&answer); 													  																																																																																																																																																																																							 
                     }while(strcmpi(answer,"C")==0 && strcmpi(answer,"X")!=0);
			         }break;
				     case 2:
			         {
                   do
			            { 
							  FILE *fphstaff;  
                       system("cls");
                       system("Color E");
                       int x1=36;
                       int y1=4;
                       Sstaff();
                       gotoxy(x1,y1++);printf(":::>> OPTION <<:::");
                       gotoxy(x1,y1++);printf("(1)<---> Input");
                       gotoxy(x1,y1++);printf("(2)<---> Show");
                       gotoxy(x1,y1++);printf("(3)<---> Search");
                       gotoxy(x1,y1++);printf("(4)<---> Sort");
                       gotoxy(x1,y1++);printf("(5)<---> Delete");
                       gotoxy(x1,y1++);printf("(6)<---> Update");
                       gotoxy(x1,y1++);printf("(7)<---> History");
                       gotoxy(x1,y1++);printf("(8)<---> Back");
                       gotoxy(x1,y1++);printf("Please Chose Option...");scanf("%d",&op1);
                       system("cls");
                       switch(op1)
                        {
          	              case 1:
        		               {
 		 	                     system("Color 3");
							         fphstaff=fopen("STAFF1.txt","a");        
       		                  fpstaff=fopen("STAFF.txt","a");
		         	            if(fpstaff==NULL)
			                     {
			 	                    printf("\t\tError To Create File..!!\n");			
                              }
		                        printf("\t\t\tEnter Number Of Staff = ");scanf("%d",&n1);
		                        for(i=0;i<n1;i++)
		                        {
                                 printf("\t\t\t STAFF #%d\n",i+1);
			                        printf("\t\tInput Staff ID = ");fflush(stdin);scanf("%s",&Staff[i][1]);fflush(stdin);
                                 printf("\t\tInput Staff Name = ");scanf("%s",&Staff[i][2]);
                                 printf("\t\tInput Staff Gender = ");scanf("%s",&Staff[i][3]);
                                	printf("\t\tInput Staff Position = ");scanf("%s",&Staff[i][4]);fflush(stdin);
                                 printf("\t\tInput Staff Salary = ");scanf("%s",&Staff[i][5]);fflush(stdin);
                                 printf("\t\tInput Staff Phone = ");scanf("%s",&Staff[i][6]);fflush(stdin);
                                 printf("\t\tInput Staff Address = ");fflush(stdin);gets(Staff[i][7]);
			                        fprintf(fpstaff,"%10s%15s%15s%15s%15s%15s%13s\n",Staff[i][1],Staff[i][2],Staff[i][3],Staff[i][4],Staff[i][5],Staff[i][6],Staff[i][7]);
										  	fprintf(fphstaff,"%10s%15s%15s%15s%15s%15s%13s\n",Staff[i][1],Staff[i][2],Staff[i][3],Staff[i][4],Staff[i][5],Staff[i][6],Staff[i][7]);																																								 	                       
	                           }
										  printf("\n\t\t\tSave Complete!!!\n");       
					              fclose(fpstaff);
									  fclose(fphstaff);    
                           }break;
                           case 2:
              	            {
                              system("Color 2");
           		  	            Header_staff();	   
        		                  fpstaff=fopen("STAFF.txt","r");
	         	              if(fpstaff==NULL)
			                    {
			 	                    printf("\t\t\tError To Opening File..!!\n");			
                             }  								 
			                    while(fscanf(fpstaff," %s%s%s%s%s%s%s ",&Staff[i][1],&Staff[i][2],&Staff[i][3],&Staff[i][4],&Staff[i][5],&Staff[i][6],&Staff[i][7])!=EOF)
									  	{
											printf("     <>____________________________________________________________________________________________<>\n");																									                      
                                 printf("%10s%15s%15s%15s%15s$%15s%13s\n",Staff[i][1],Staff[i][2],Staff[i][3],Staff[i][4],Staff[i][5],Staff[i][6],Staff[i][7]);				 	
		                        }
						           fclose(fpstaff);																								  	    
		                     }break;
					            case 3:
				               {
				 	           																							 	
					 	           FILE *src1;
						           int c1=0;																		 											
						           int i=0;
									  char sid1[10];																			  											
                             src1=fopen("SEARCH1.txt","w");
                             fpstaff=fopen("STAFF.txt","r");
						           printf("Input ID to Search...");scanf("%s",&sid1);
									  Header_staff();									  																															     								 
						           while(fscanf(fpstaff," %s%s%s%s%s%s%s ",&Staff[i][1],&Staff[i][2],&Staff[i][3],&Staff[i][4],&Staff[i][5],&Staff[i][6],&Staff[i][7])!=EOF)
                             {
                                 if(strcmp(Staff[i][1],sid1)==0)
				                     {
			                            c1=1;
                                    fprintf(src1,"%10s%15s%15s%15s%15s%15s%13s\n",Staff[i][1],Staff[i][2],Staff[i][3],Staff[i][4],Staff[i][5],Staff[i][6],Staff[i][7]);	
                                    printf("     <>____________________________________________________________________________________________<>\n");
									         printf("%10s%15s%15s%15s%15s%15s%13s\n",Staff[i][1],Staff[i][2],Staff[i][3],Staff[i][4],Staff[i][5],Staff[i][6],Staff[i][7]);																																				 							
						               }						 	
                              }																						 																																																									 																																					  
						            fclose(fpstaff);
						            fclose(src1);																																																  																																																	   
						           if(c1==0)
						           {
						  		        printf("Search not found!!\n");																																								  	
						            }else
					               printf("Search found!!!\n");	 	 		
			                  }break;
					             case 4:
					            {	
										
									   	
										int d1=0;
										int i=0;
										int n1=0;  			 																																																																																																															  	
	  			  	 					char temp1[100];
         			            fpstaff=fopen("STAFF.txt","r");															 																																	 	
					               while(fscanf(fpstaff," %s%s%s%s%s%s%s ",&Staff[i][1],&Staff[i][2],&Staff[i][3],&Staff[i][4],&Staff[i][5],&Staff[i][6],&Staff[i][7])==7)
								      {i++;} 
										n1=i;
									   fclose(fpstaff);																											  																																																																																										   																																																																																																																																																																												 																																																																																																					 																																																																																																									  							 					    
										   for(i=0;i<n1;i++)
											{
											 for(j=i+1;j<n1;j++)
											  {
									         if(strcmp(Staff[i][2],Staff[j][2])>0)
                                    {	
               	                        strcpy(temp1,Staff[i][1]);
                                    	strcpy(Staff[i][1],Staff[j][1]);
                                    	strcpy(Staff[j][1],temp1);
                                    	
                                    	strcpy(temp1,Staff[i][2]);
                                    	strcpy(Staff[i][2],Staff[j][2]);
                                    	strcpy(Staff[j][2],temp1);
                                    	
                                    	strcpy(temp1,Staff[i][3]);
                                    	strcpy(Staff[i][3],Staff[j][3]);
                                    	strcpy(Staff[j][3],temp1);
                                    	
                                    	strcpy(temp1,Staff[i][4]);
                                    	strcpy(Staff[i][4],Staff[j][4]);
                                    	strcpy(Staff[j][4],temp1);
                                    	
                                    	strcpy(temp1,Staff[i][5]);
                                    	strcpy(Staff[i][5],Staff[j][5]);
                                    	strcpy(Staff[j][5],temp1);
                                    	
                                    	strcpy(temp1,Staff[i][6]);
                                    	strcpy(Staff[i][6],Staff[j][6]);
                                    	strcpy(Staff[j][6],temp1);
                                    	
                                    	strcpy(temp1,Staff[i][7]);
                                    	strcpy(Staff[i][7],Staff[j][7]);
                                    	strcpy(Staff[j][7],temp1);
										d1=1;					 																										 															 	
                                    }
											  }
										   }
										   fpstaff=fopen("STAFF.txt","w");
										   for(i=0; i<n1; i++)
											{
										     fprintf(fpstaff,"%s %s %s %s %s %s %s ",Staff[i][1],Staff[i][2],Staff[i][3],Staff[i][4],Staff[i][5],Staff[i][6],Staff[i][7]);							 												  
										   }	  
										 fclose(fpstaff);				 																		  																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																												  																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																														 			 
										if(d1==0)
										{
										 	printf("\t\t\t\n Error to Sort!!!\n");	  																																																																																																																			  					
									   }
										else if(d1==1)
										{
										  	printf("\t\t\t Sort Successful.....\n");																 																				  					  		  	  																																																																																																																																																																																																																																																																																																																																																																																											
										} 					 		  	 			
				               }break;			 		  	 		
					            case 5:
					            {
	 	                       FILE *dfp1;
                             char d_id1[4];
                             int b=0;
                             int i=0;
                             dfp1=fopen("DELETE1.txt","w");
                             fpstaff=fopen("STAFF.txt","r");
                             printf("Input ID to Delete.....");scanf("%s",&d_id1);
				                 while(fscanf(fpstaff," %s%s%s%s%s%s%s ",&Staff[i][1],&Staff[i][2],&Staff[i][3],&Staff[i][4],&Staff[i][5],&Staff[i][6],&Staff[i][7])!=EOF)
					              { 
                                if(strcmp(Staff[i][1],d_id1)==0)
                                {
					                    b=1;																																										  																																																													 	
					                 }
					                 else
                                {
				                       fprintf(dfp1,"%10s%15s%15s%15s%15s%15s%13s\n",Staff[i][1],Staff[i][2],Staff[i][3],Staff[i][4],Staff[i][5],Staff[i][6],Staff[i][7]);			 																																																																																																														
		                           }																																																																													
				  	               }
						           fclose(fpstaff);
						           fclose(dfp1);
						           remove("STAFF.txt");
						           rename("DELETE1.txt","STAFF.txt");
						           if(b==0)
									  {
					  	              printf("Delete Not Complete...\n");		  								 																																																																																																																																															           	
									  }
						           else printf("Delete Complete..\n");						 																																																																																																																										  				
			                  }break;
					            case 6:
					            {
								int u=0;     	
                              char u_id1[5];  	 																																																																																																																																															
	                           FILE *update1;
		                        update1=fopen("UPDATE1.txt","w");
                              fpstaff=fopen("STAFF.txt","r");
			                     printf("Input ID to Update....");scanf("%s",&u_id1);
                              int i=0;																	 																																																																																																																																				 
					               while(fscanf(fpstaff," %s%s%s%s%s%s%s ",&Staff[i][1],&Staff[i][2],&Staff[i][3],&Staff[i][4],&Staff[i][5],&Staff[i][6],&Staff[i][7])!=EOF)
						            {
                                 if(strcmp(Staff[i][1],u_id1)==0)
					                  {
											 																                   	
	                                printf("\t\t\t NEW STAFF #%d\n",i+1);
				                       printf("\t\tInput Staff ID = ");fflush(stdin);scanf("%s",&Staff[i][1]);fflush(stdin);
                                 printf("\t\tInput Staff Name = ");scanf("%s",&Staff[i][2]);
                                 printf("\t\tInput Staff Gender = ");scanf("%s",&Staff[i][3]);
                                	printf("\t\tInput Staff Position = ");scanf("%s",&Staff[i][4]);fflush(stdin);
                                 printf("\t\tInput Staff Salary = ");scanf("%s",&Staff[i][5]);fflush(stdin);
                                 printf("\t\tInput Staff Phone = ");scanf("%s",&Staff[i][6]);fflush(stdin);
                                 printf("\t\tInput Staff Address = ");fflush(stdin);gets(Staff[i][7]);
			                         
												u=1;				 	 			 																									 																																																																																																																	 	
						               }
									     fprintf(update1,"%10s%15s%15s%15s%15s%15s%13s\n",Staff[i][1],Staff[i][2],Staff[i][3],Staff[i][4],Staff[i][5],Staff[i][6],Staff[i][7]);							 			 																										 																																																																																																																		
						            }
						           fclose(fpstaff);
						           fclose(update1);
						           remove("STAFF.txt");
						           rename("UPDATE1.txt","STAFF.txt");
									   if(u==0)
										{
										 	printf("\t\t\t\nError to Update!!!");	  																																																																																																																			  					
									   }
										else printf("\t\t\t\nUpdate Successful.....");		 	  	
				               }break;
					            case 8:
					            {
					 	   	 		// Back;
			                  }break;
									case 7:
									{
                             system("Color 2");
                             Header_staff();	   
                             fphstaff=fopen("STAFF1.txt","r");
                             if(fphstaff==NULL)
                             {
                                printf("\t\t\tError To Opening File..!!\n");			
                             }  								 
                               while(fscanf(fphstaff," %s%s%s%s%s%s%s ",&Staff[i][1],&Staff[i][2],&Staff[i][3],&Staff[i][4],&Staff[i][5],Staff[i][6],Staff[i][7])!=EOF)
                              {
                                 //fprintf(fphstaff,"%30s%10s%10s%10s%10s%10s\n",Staff[i][1],Staff[i][2],Staff[i][3],Staff[i][4],Staff[i][5],Staff[i][6]);
					  		            printf("     <>____________________________________________________________________________________________<>\n");																								                      
                                 printf("%10s%15s%15s%15s%15s%15s%13s\n",Staff[i][1],Staff[i][2],Staff[i][3],Staff[i][4],Staff[i][5],Staff[i][6],Staff[i][7]);		 	
                              }
                             fclose(fphstaff);		 																																																																																																																																																																																								
								   }break;			 
             	           default:printf("Error Option!!!\n");
				           }
							  printf("\n\t\tPress C to Continue and Press X to Exit....");scanf("%s",&answer); 													  																																																																																																																																																																																							  
                     
                     }while(strcmpi(answer,"C")==0 && strcmpi(answer,"X")!=0);
					 }break;
                case 3:
				    {
                   do
			         { 
                     int x10=36;
                     int y10=4;
                    system("cls");
   	              int op3;	
   					  sel_order();        
                    gotoxy(x10,y10++);printf("[1] <<--->> Show Product");					  		 				  																																																	  																																																																																										
	                 gotoxy(x10,y10++);printf("[2] <<--->> Sell Product");
        	           gotoxy(x10,y10++);printf("[3] <<--->> Order\n");
				        gotoxy(x10,y10++);printf("[4] <<--->> Show order");
						  gotoxy(x10,y10++);printf("[5] <<--->> Cancel order");
						  gotoxy(x10,y10++);printf("[6] <<--->> Confirm order");		
						  gotoxy(x10,y10++);printf("[7] <<--->> Show Sell");
						  gotoxy(x10,y10++);printf("[8] <<--->> Back");		  	 	  																																																											  		  	  			  																																																																																																																																											
				        gotoxy(x10,y10++);printf("Please Chose Option.....");scanf("%d",&op3);
				        system("cls");
						  switch(op3)
				        {
	 	                  case 1:
			              {
			              	system("cls");
				              system("Color 2");
           		  	            Header_shop();	   
        		                  fpshop=fopen("SHOP.txt","r");
	         	              if(fpshop==NULL)
			                    {
			 	                    printf("\t\t\tError To Opening File..!!\n");			
                             }  								 
			                    while(fscanf(fpshop," %s%s%s%s%s ",&Product[i][1],&Product[i][2],&Product[i][3],&Product[i][4],&Product[i][5])!=EOF)
									  	{
											printf("\t\t\t<>______________________________________________<>\n");																											                      
                                 printf("%30s%10s%10s%10s$%10s\n",Product[i][1],Product[i][2],Product[i][3],Product[i][4],Product[i][5]);					 	
		                        }
						           fclose(fpshop);									 														  	
                        }break;
                        case 2:
                        {  
                            //int 
                            system("cls");
				                system("Color E");
                               fflush(stdin);
         			            printf("Input Costomer Name : ");gets(Sell[n][1]);fflush(stdin);
         			            printf("Input Qty : ");scanf("%s",&Sell[n][2]);
							   	  again: 
								       printf("Input Book ID  : ");scanf("%s",&Sell[n][3]);fflush(stdin);
										 
										 	  				 							       
									
			                       if(strcmpi(Sell[n][3],"B")==0)
			                        break;
			                        int h=0;
			                       fpshop=fopen("SHOP.txt","r");
			                       m=fopen("market.txt","w");
			                       h=0;
			                       while(fscanf(fpshop," %s%s%s%s%s ",&Product[i][1],&Product[i][2],&Product[i][3],&Product[i][4],&Product[i][5])!=EOF)
			                       {
			                         if(strcmp(Product[i][1],Sell[n][3])==0 && strcmp(Product[i][5],"normal")==0)
                                   { 
//	                                   a[i]=atoi(Product[i][3]);
//			                           b[i]=atoi(Sell[n][3]);
//			                           total[i]=a[i]-b[i];
//			                           strcpy(Product[i][3],total[i]);
			                          strcpy(Product[i][5],"sold");
			                          h=1;
			                         }
			                         fprintf(m,"%30s%10s%10s%10s%10s\n",Product[i][1],Product[i][2],Product[i][3],Product[i][4],Product[i][5]); 
			                      }
			                        
			                        
			                      fclose(fpshop);
			                      fclose(m);
			                      remove("SHOP.txt");
			                      rename("market.txt","SHOP.txt");
			                if(h==0){
			                gotoxy(1,13);system("cls");
							printf("\n\n\nNo product");
							printf("\nPress B/b to back\n");
			                gotoxy(1,13);				            
              			    gotoxy(1,7);
			                goto again;
			                }
			                printf("Enter Date : ");fflush(stdin);gets(Sell[n][4]);
			                system("cls");
			                strcpy(Product[i][5],"sold");
			                sl=fopen("SELL.txt","a");
			                fprintf(sl," %s %s %s %s ",Sell[n][1],Sell[n][2],Sell[n][3],Sell[n][4]);
			                fclose(sl);                                      
                       }break;
				         	case 3:
                        {  
                               fflush(stdin);

         			             printf("Input Customer Name : ");gets(Sell[n][1]);fflush(stdin);
                               printf("Input Book QTY: ");gets(Sell[n][2]);
                                printf("Input Book ID  : ");scanf("%s",&Sell[n][3]);
                         
			                       if(strcmp(Sell[n][2],"B")==0)
			                        break;
			                        int h=0;
			                       fpshop=fopen("SHOP.txt","r");
			                       m=fopen("market.txt","w");
			                       h=0;
			                       while(fscanf(fpshop," %s%s%s%s%s ",&Product[i][1],&Product[i][2],&Product[i][3],&Product[i][4],&Product[i][5])!=EOF)
			                       {
			                         if(strcmp(Product[i][1],Sell[n][3])==0 && strcmp(Product[i][5],"normal")==0)
	                              { 
			                          strcpy(Product[i][5],"order");
			                          h=1;
			                         }
			                         fprintf(m,"%30s%10s%10s%10s%10s\n",Product[i][1],Product[i][2],Product[i][3],Product[i][4],Product[i][5]); 
			                      }
			                      fclose(fpshop);
			                      fclose(m);
			                      remove("SHOP.txt");
			                      rename("market.txt","SHOP.txt");
			                if(h==0){
			                gotoxy(1,13);system("cls");
							printf(" \n\n\n No product\n");
			                printf("Prss B/b back to option\n");
			                gotoxy(1,13); 					            
              			    gotoxy(1,7);
			                goto again;
			                }
			                printf("Enter Date : ");fflush(stdin);gets(Sell[n][4]);
			                system("cls");
			                strcpy(Product[i][5],"order");
			                rd=fopen("ORDER.txt","a");
			                fprintf(rd," %s %s %s %s ",Sell[n][1],Sell[n][2],Sell[n][3],Sell[n][4]);
			                fclose(rd);                                      
                       }break;
                       case 4:{
						     printf("\n<<<<<<Show Order>>>>>>>>\n");
						     printf("%10s%10s%10s%20s\n","C_Name","QTY","P_ID","Date");
						     rd=fopen("ORDER.txt","r");
						     while(fscanf(rd," %s%s%s%s ",&Sell[n][1],Sell[n][2],Sell[n][3],Sell[n][4])==4){
						     	printf("%10s%10s%10s%20s\n",Sell[n][1],Sell[n][2],Sell[n][3],Sell[n][4]);
							 }
							 getch();
							 fclose(rd);
					   }break;
					   case 5:{
					   	  char del[20];int h=0;
					   	  fflush(stdin);
					   	  printf("Input Id to cancel order:  ");gets(del);
					   	  fpshop=fopen("SHOP.txt","r");
					   	  m=fopen("market.txt","w");
					   	  h=0;
					   	  while(fscanf(fpshop," %s%s%s%s%s ",&Product[i][1],&Product[i][2],&Product[i][3],&Product[i][4],&Product[i][5])!=EOF)
			                       {
			                         if(strcmp(Product[i][1],del)==0 && strcmp(Product[i][5],"order")==0)
	                              {
			                          strcpy(Product[i][5],"normal");
			                          h=1;
			                         }
			                         fprintf(m,"%30s%10s%10s%10s%10s\n",Product[i][1],Product[i][2],Product[i][3],Product[i][4],Product[i][5]); 
			                      }
			                      fclose(fpshop);
			                      fclose(m);
			                      remove("SHOP.txt");
			                      rename("market.txt","SHOP.txt");
			                if(h==0){
			                gotoxy(1,13);system("cls");
							printf("\n\n\nNo product");
			                printf("\nPress B/b to back");
			                gotoxy(1,1);
								 				            
              			    gotoxy(1,7);
			                goto again;
			                }
			                printf("Enter Date : ");fflush(stdin);gets(Sell[n][1]);
			                strcpy(Product[i][5],"normal");
			                fpshop=fopen("SHOP.txt","a");
			                fclose(fpshop);                             
					         }break;
				            case 6:{          
                             fflush(stdin);

         			             printf("Input Customer Name : ");gets(Sell[n][1]);fflush(stdin);
         			             printf("Input Book QTY: ");gets(Sell[n][2]);
                               printf("Input Book ID  : ");scanf("%s",&Sell[n][3]);
                         
			                       if(strcmp(Sell[n][3],"B")==0)
			                       break;
			                       int h=0;
			                       fpshop=fopen("SHOP.txt","r");
			                       m=fopen("market.txt","w");
			                       h=0;
			                       while(fscanf(fpshop," %s%s%s%s%s ",&Product[i][1],&Product[i][2],&Product[i][3],&Product[i][4],&Product[i][5])!=EOF)
			                       {
			                         if(strcmp(Product[i][1],Sell[n][3])==0 && strcmp(Product[i][5],"order")==0)
	                              {
			                          strcpy(Product[i][5],"sold");
			                          h=1;
			                         }
			                         fprintf(m,"%30s%10s%10s%10s%10s\n",Product[i][1],Product[i][2],Product[i][3],Product[i][4],Product[i][5]); 
			                      }
			                      
			                      fclose(fpshop);
			                      fclose(m);
			                      remove("SHOP.txt");
			                      rename("market.txt","SHOP.txt");
			                if(h==0){
			                gotoxy(1,13);system("cls");
							printf("\n\n\n No product\n");
							printf("Press B/b to back\n");
			                gotoxy(1,13);
								 				            
              			    gotoxy(1,7);
			                goto again;
			                }
			                printf("Enter Date : ");fflush(stdin);gets(Sell[n][4]);
			                strcpy(Product[i][5],"sold");
			                sl=fopen("SELL.txt","a");
			                fprintf(sl," %s %s %s %s ",Sell[n][1],Sell[n][2],Sell[n][3],Sell[n][4]);
			                fclose(sl);                                                                
					   }break;
					   case 7:{
					   	      printf("\n<<<<<<Show Sell>>>>>>>>\n");
						     printf("%10s%10s%10s%20s\n","S_Name","QTY","S_P_ID","Date");
						     sl=fopen("SELL.txt","r");
						     while(fscanf(sl," %s%s%s%s ",&Sell[n][1],Sell[n][2],Sell[n][3],Sell[n][4])==4){
						     	printf("%10s%10s%10s%20s\n",Sell[n][1],Sell[n][2],Sell[n][3],Sell[n][4]);
							 }
							 getch();
							 fclose(sl);
						
					   }break;
				       case 8:{
				       	//
						
					   }break;
              }
            int x3=30;
		      int y3=30;				 						   
            gotoxy(x3,y3++);printf("Press C/c Continue to Main Program and Press X/x to Exit....");scanf("%s",&answer);
           }while(strcmpi(answer,"C")==0 && strcmpi(answer,"X")!=0);
         }break;
         case 4:
         {
             exit(0);
         }break;
         case 5:
         {
		     system("cls");
		     system("Color 84");
		     int x=29;
		     int y=12; 		   	
		     gotoxy(x,y);printf("||>><< THANK YOU FOR PAY ATTENTION >><<||"); 		   	
         }break; 
         default:printf("\n\t\tError Option!!!\n");  
			}
		 int x3=30;
		 int y3=26;				 						   
       gotoxy(x3,y3++);printf("Press C/c Continue to Main Program and Press X/x to Exit....");scanf("%s",&answer);
	   }while(strcmpi(answer,"C")==0 && strcmpi(answer,"X")!=0);
	}else
	  {
		  int x2=30;
 	     int y2=13;
	     gotoxy(x2,y2++);printf("Incorrect Password!!");
 	     gotoxy(x2,y2++);printf("Try again!!");
	  }  
   }else
	  {
	     int x=33;
        int y=13; 
        gotoxy(x,y++);printf("Incorrect User Name!!");
        gotoxy(x,y++);printf("Try Again!!!");   	
     }
     int x=33;
     int y=20;
     gotoxy(x,y++);printf("Press C/c to Login Press X/x to Stop....");scanf("%s",&answer);
  }while(strcmpi(answer,"C")==0 && strcmpi(answer,"X")!=0);
}
