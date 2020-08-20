/* HackerRank-Problem-solving-Pangram */
#include<stdio.h>
#include<string.h>
int main()
{
    int n,i,j,f=0;
    char a[1000];
    char b[]={'a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z'};
    scanf("\n");
    gets(a);
    n=strlen(a);
    if(n>=26)
    {
      for(j=0;j<26;j++)
      {
        f=0;
        for(i=0;a[i]!='\0';i++)
        {
            if(b[j]==a[i] || b[j]-32==a[i])
            {
                f=1;
                break;
            }
        }
            if(f==0)
            break;
      }
        if(f==0)
        printf("not pangram");
        else
        printf("pangram");
    }
    else
    printf("not pangram");
    return 0;
    
}
