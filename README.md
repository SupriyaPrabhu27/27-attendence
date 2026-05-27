# 27-attendence
## SUPRIYA PRABHU 
## 21224240165
1. Write a program to read a string and count the number of vowels using a separate function.
```
#include <stdio.h>

int countVowels(char str[])
{
    int i, count = 0;

    for(i = 0; str[i] != '\0'; i++)
    {
        char ch = str[i];

        if(ch=='a' || ch=='e' || ch=='i' || ch=='o' || ch=='u' ||
           ch=='A' || ch=='E' || ch=='I' || ch=='O' || ch=='U')
        {
            count++;
        }
    }

    return count;
}

int main()
{
    char str[100];

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    printf("Number of vowels = %d", countVowels(str));

    return 0;
}
```
## output
<img width="1629" height="878" alt="image" src="https://github.com/user-attachments/assets/740983a6-fc85-4ecb-86e4-8de4b54a366e" />


3. Write a function to reverse a string without using library functions like strrev().
```
#include <stdio.h>

void reverseString(char str[])
{
    int i, length = 0;
    char temp;

    while(str[length] != '\0')
    {
        length++;
    }

    length--;  

    for(i = 0; i < length; i++, length--)
    {
        temp = str[i];
        str[i] = str[length];
        str[length] = temp;
    }
}

int main()
{
    char str[100];

    printf("Enter a string: ");
    scanf("%[^\n]", str);

    reverseString(str);

    printf("Reversed string = %s", str);

    return 0;
}
```
## output
<img width="1456" height="886" alt="image" src="https://github.com/user-attachments/assets/d056e095-87aa-4edc-9fd9-f31132a03d14" />


5. Write a program to check whether a given string is palindrome or not using functions.
```
#include <stdio.h>

int isPalindrome(char str[])
{
    int i, length = 0;

    while(str[length] != '\0')
    {
        length++;
    }

    for(i = 0; i < length / 2; i++)
    {
        if(str[i] != str[length - i - 1])
        {
            return 0;
        }
    }

    return 1;
}

int main()
{
    char str[100];

    printf("Enter a string: ");
    scanf("%s", str);

    if(isPalindrome(str))
        printf("Palindrome");
    else
        printf("Not Palindrome");

    return 0;
}
```
## output
<img width="1430" height="849" alt="image" src="https://github.com/user-attachments/assets/179996a7-7507-450c-a936-033a48e3f4da" />


7. Write a function to calculate the length of a string manually.
  ```
#include <stdio.h>

int stringLength(char str[])
{
    int i = 0;

    while(str[i] != '\0')
    {
        i++;
    }

    return i;
}

int main()
{
    char str[100];

    printf("Enter a string: ");
    scanf("%[^\n]", str);

    printf("Length of string = %d", stringLength(str));

    return 0;
}
```
## output
<img width="1447" height="799" alt="image" src="https://github.com/user-attachments/assets/607f4379-53d7-488b-975b-5cbe2bd70828" />


9. Write a function to count the number of words in a sentence.
```
#include <stdio.h>

int countWords(char str[])
{
    int i, words = 1;

    for(i = 0; str[i] != '\0'; i++)
    {
        if(str[i] == ' ' && str[i+1] != ' ')
        {
            words++;
        }
    }

    return words;
}

int main()
{
    char str[100];

    printf("Enter a sentence: ");
    scanf("%[^\n]", str);

    printf("Number of words = %d", countWords(str));

    return 0;
}
```
## output
<img width="1248" height="786" alt="image" src="https://github.com/user-attachments/assets/390a3022-0d78-43ef-8341-2dddcb0bfe3d" />
