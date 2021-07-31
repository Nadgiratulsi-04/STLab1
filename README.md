Design, develop, code and run the program in any suitable language to solve the commission problem. Analyze it from the perspective of equivalence class testing, derive different test cases, execute these test cases and discuss the test results. 
Equivalence Classes are as follows: 
L1 = { locks: 1<=locks<=70} 
L2 = { locks=-1} 
S1 = { stocks: 1<=stocks<=80} 
B1 = { barrels: 1<=barrels<=90}
Algorithm:
STEP 1: Define lockPrice=45.0, stockPrice=30.0, barrelPrice=25.0 
STEP2: Input locks 
STEP3: while(locks!=-1)  input device uses -1 to indicate end of data goto STEP 12 
STEP4:input (stocks, barrels) 
STEP5: compute lockSalaes, stockSales, barrelSales and sales 
STEP6: output(“Total sAles:” sales) 
STEP7: if (sales > 1800.0) goto STEP 8 else goto STEP 9 
STEP8:
 commission=0.10*1000.0; 
commission=commission+0.15 * 800.0; 
commission = commission + 0.20 * (sales-1800.0) 
STEP9: if (sales > 1000.0) goto STEP 10 else goto STEP 11 
STEP10: commission=0.10* 1000.0; 
commission=commission + 0.15 * (sales-1000.0) 
STEP11: Output(“Commission is $”, commission) 
STEP12: exit


//Program to solve the above given problem statement
#include<stdio.h> 
 
int main() 
{ 
int locks, stocks, barrels, t_sales, flag = 0; 
float commission; 

printf("Enter the total number of locks"); 
scanf("%d",&locks); 
if ((locks <= 0) || (locks > 70)) 
{ 
flag = 1; 
} 
printf("Enter the total number of stocks"); 
scanf("%d",&stocks); 
if ((stocks <= 0) || (stocks > 80)) 
{ 
flag = 1; 
} 
printf("Enter the total number of barrelss"); 
scanf("%d",&barrels); 
if ((barrels <= 0) || (barrels > 90)) 
{ 
flag = 1; 
} 
if (flag == 1) 
{ 
printf("invalid input"); 
getch(); 
exit(0); 
} 
t_sales = (locks * 45) + (stocks * 30) + (barrels * 25); 
if (t_sales <= 1000) 
{ 
commission = 0.10 * t_sales; 
} 
else if (t_sales < 1800) 
{ 
commission = 0.10 * 1000; 
commission = commission + (0.15 * (t_sales - 1000)); 
} 
else 
{ 
commission = 0.10 * 1000; 
commission = commission + (0.15 * 800); 
commission = commission + (0.20 * (t_sales - 1800)); 
} 
printf("The total sales is %d \n The commission is %f",t_sales, commission); 
getch(); 
return 0; 
}  
