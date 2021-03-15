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
    #include<stdio.h>
    int main()
    {
     char s1[50], s2[50];
     int i, j, length, flag=0;

    printf("Enter first string: ");
    fgets(s1,sizeof(s1),stdin);
    printf("Enter second string: ");
    fgets(s2,sizeof(s2),stdin);

 
    for(i=0;s1[i]!='\0';i++);
    length=i;
    for(j=0;s2[j]!='\0';j++);

    if(i!=j)
    printf("1");
    else
    {
       for(i=0; i<length; i++)
     {
       if(s1[i]!=s2[i])
       {
         flag=1;
         break;
       }
     }
     if(flag==1) printf("1");
     else printf("0");
     }

    return 0;
     }
## Exercise 3

    #include <stdio.h>
    #include <stdlib.h>
    #include <string.h>

    int main(){
       char str1[80], str2[80];
       int size1,size2, i,j;
       printf ("Give the first string: ");
       scanf ("%s", str1);
       printf ("Give the second string: ");
       scanf ("%s", str2);

       size1= strlen(str1);
       size2= strlen(str2);

            for (j=0; j<size2; j++){
                for (i=0; i<size1; i++){
                if (str2[j]==str1[i])
                str1[i]=' ';
                  else if(str2[j]==str1[i])
                  printf("0");

         }
      }

     printf("%s\n", str1);

     return 0;

    }
  
  ## Exercise 4
  
     #include <string.h>
     #include <stdio.h>
 
     int main()
     {
      char s[1000];  
      int i,n,c=0;
 
       printf("Enter  the string : ");
       gets(s);
       n=strlen(s);
 
         for(i=0;i<n/2;i++)  
     {
    	if(s[i]==s[n-i-1])
    	c++;
 
 	  }
 	  if(c==i)
 	     printf("1");
      else
         printf("0");
 
 	 
     
      return 0;
     }

## Exercise 5 

    #include <stdio.h>
    #include <string.h>
    int check_vowel(char);

    int main()
    {
        char s[100], t[100];
        int c, d = 0;

        printf("Enter a string \n");
        gets(s);

        for (c = 0; s[c] != '\0'; c++) {
          if (check_vowel(s[c]) == 0) {   
           t[d] = s[c];
           d++;
      }
     }

    t[d] = '\0';

    strcpy(s, t);  

    printf("String without vowels: %s\n", s);

     return 0;
     }

     int check_vowel(char t)
     {
    if (t == 'a' || t == 'A' || t == 'e' || t == 'E' || t == 'i' || t == 'I' || t =='o' || t=='O' || t == 'u' || t == 'U')
    return 1;

    return 0;
    }
