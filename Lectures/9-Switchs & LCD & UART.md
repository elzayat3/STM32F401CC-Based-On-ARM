
---


## 1-Switch

![[Pasted image 20261121171730.png]]



![[Pasted image 20261121171949.png]]


![[Pasted image 20261121171959.png]]



## 2-LCD 

![[Pasted image 20261121185803.png]]

الكهرباء اللي بتخلي الLCD تنور بتكون AC ده معناه انه فيه ميكرو جوه بيتحكم بده 

![[Pasted image 20261121185949.png]]

![[Pasted image 20261121190013.png]]


![[Pasted image 20261121190023.png]]

![[Pasted image 20261121190202.png]]

IR --> Instruction register 

DR ---> Data register 

![[Pasted image 20261121190333.png]]

![[Pasted image 20261121190417.png]]

![[Pasted image 20261121190513.png]]

![[Pasted image 20261121190812.png]]

```c
#include <stdio.h>

int main(void) {
    char buffer[100];

    int age = 20;
    char name[] = "Ahmed";

    snprintf(buffer, sizeof(buffer),
             "My name is %s and I am %d years old",
             name, age);

    printf("%s\n", buffer);

    return 0;
}
```

![[Pasted image 20261121191213.png]]

![[Pasted image 20261121191231.png]]

![[Pasted image 20261121191317.png]]

![[Pasted image 20261121191330.png]]