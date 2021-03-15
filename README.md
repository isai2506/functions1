## Exercise 1

    #include <stdio.h>
    #include <string.h>
 
    int main()
    {
      char str1[100], tmp;
      int l, lind, rind,i;

      printf("Enter a word : ");
      scanf("%s", str1);
      l = strlen(str1);

      lind = 0;
      rind = l-1;
    
          for(i=lind;i<rind;i++)
       {
       tmp = str1[i];
       str1[i] = str1[rind];
       str1[rind] = tmp;
       rind--;
       }
 
       printf("Inverted string is: %s\n\n", str1);
      }

## Exercise 2
