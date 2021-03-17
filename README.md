# Function1
Function1
### 1

#include <stdio.h>
int main()
{
  char str[1000], rev[1000];
  int i, j, count = 0;
  scanf("%s", str);
  printf("\nString Before Reverse: %s", str);
  //finding the length of the string
  while (str[count] != '\0')
  {
    count++;
  }
  j = count - 1;

  //reversing the string by swapping
  for (i = 0; i < count; i++)
  {
    rev[i] = str[j];
    j--;
  }

  printf("\nString After Reverse: %s", rev);
}

### 2

#include <string.h>
 
int stringcompare(char *s1,char *s2)
{
	int i,c=0;
	if(strlen(s1)==strlen(s2))
    {
    	for(i=0;s2[i];i++)  
        {
        	if(s1[i]==s2[i])
        	 c++;
 	    }
 	    if(c==i)
          return 1;
          
    }
    return 0;
     
 	
}
int main()
{
 
    char s1[1000],s2[1000],c;  
 
    printf("Enter  string1: ");
    gets(s1);
    printf("Enter  string2: ");
    gets(s2);
    c=stringcompare(s1,s2);
    if(c)
        printf("0");
    else
        printf("1");
    
	return 0;
    
}

### 3

#include <stdio.h>
#include <string.h>
#define MAX 30

char comparestrings(char string1[MAX],char string2[MAX])
{
  char var = '0';
  int i;
  for(i=0;i<MAX;i++)
  {
    if ( string1[i]!= string2[i]){
      var = string1[i];
      break;
    }
  }
  return var;
}

### 4

#include <stdio.h>
#include <string.h>
#define MAX 30

int palindrome(char string[MAX])
{
  int i;
  int len=strlen(string);
  for(i=len-1; i>=0; i--){
//    printf(" %c %c\n",string[len-i-1],string[i]);
    if(string[len-i-1]!=string[i]){
      return 0;
    }
  }
  return 1;
}
int main(void) {
  
  printf("the value of palindrome is %d\n",palindrome("14563"));

  return 0;
}

### 5

#include <stdio.h>
#include <string.h>
#include <stdlib.h>

#define MAX 30

char *nv(char *cad) {
    char *cadt = malloc(strlen(cad)+1);
    int j = 0;
        for (int i=0; i<strlen(cad); i++) {
            switch (cad[i]) {
                case 'a': break;
                case 'A': break;
                case 'e': break;
                case 'E': break;
                case 'i': break;
                case 'I': break;
                case 'o': break;
                case 'O': break;
                case 'u': break;
                case 'U': break;
                default:
                cadt[j] = cad[i];
                j++;
            }
        }
    cadt[j] = '\0';
    return cadt;
}

int main() {
    char leer[MAX];
    printf("Write your string:\n");
    scanf("%s", &leer);
    char *cadf = nv(leer);
    printf("Consonats: %s\n", cadf);
    free(cadf);
    return 0;
}
