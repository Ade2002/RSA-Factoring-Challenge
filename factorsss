#include <stdio.h>
#include <stdlib.h>

void factorize(int number, int *factor1, int *factor2){

    // using bruteforce to split number
    for (int i = 2; i < number ; i++){

        // check if i is a prime number or not
        // if solve is an integer 
        if (number % i == 0) {
            int solve = number / i;
            *factor1 = solve;
            *factor2 = i;
            break;
        }
    }

}

int main(int argc, char *argv[]){

  FILE *fptr;
  int number, number1, number2;
  


   // use appropriate location if you are using MacOS or Linux
   fptr = fopen(argv[1],"r");

   if(fptr == NULL)
   {
      printf("Error!");   
      exit(1);             
   }

   // breaking rsa with bruteforce
 

    while (fscanf(fptr, "%d", &number) != EOF ) {
    factorize(number, &number1, &number2);
    printf("%i, %i \n", number1, number2);
    }
   
   

   fclose(fptr);

   return 0;

}
