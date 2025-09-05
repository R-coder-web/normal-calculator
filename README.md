# normal-calculator

#include <stdio.h>
#include <math.h>
double division(double,double);
double modulus(int,int);
void print_menu();

int main(){
    int choice;
    double first,second,result;
    while(1){
            print_menu();

scanf("%d",&choice);
if(choice==7){
    break;
}
if(choice<1 ||choice>7){
    fprintf(stderr,"invalid menu choice,");
    continue;
}
printf("\nplease,enter your first number: ");
scanf("%lf",&first);
printf("\nnow,enter your second number: ");
scanf("%lf",&second);
switch(choice)
{

case 1: //addition
    result=first+second;
    break;
    case 2://substract
        result=first-second;
    break;
case 3: //multiply
    result=first*second;
    break;
case 4: //divide
    result=division(first,second);
    break;
case 5: //modulas
    result=modulus(first,second);
    break;
      case 6: //power
          result=pow(first,second);
    break;

} 
if (!isnan(result)){
printf("\nresult of operation is :%.2f",result);}
}
return 0;

}
double division(double a,double b){
    if(b==0){
      fprintf(stderr,"invalid argument for division");
      return NAN;
    }
    else{
        return(a/b);
    }
}
double modulus(int a,int b){
    if(b==0){
      fprintf(stderr,"invalid argument for modulus");
      return NAN;
    }
    else{
        return(a%b);
    }
}
void print_menu(){
    printf("\n\n--------------------------");
printf("\nwelcome to simple calculator: \n");
printf("\nchoose of the following options: ");
printf("\n1.addition");
printf("\n2.substract");
printf("\n3.multiply");
printf("\n4.divide");
printf("\n5.modulas");
printf("\n6.power");
printf("\n7.exit");
printf("\n now ,enter your choice: ");
}
