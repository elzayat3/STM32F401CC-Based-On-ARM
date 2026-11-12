
---


## 1-Configration 

![[Pasted image 20261111030212.png]]


في الbss ليه اختار يعملها ب zero ؟ علشان هو بيروح يكتب في byte byte zero فلو 4byte وانا بكتب 1 بدل zero هيكتب 1 اربع مرات ودي مشكلة كبيرة 

## 2-Symbol table 

![[Pasted image 20261111031707.png]]

الcompiler مش عارف الmemory الحقيقة عامله ازاي 

الU الموجودة فوق دي تدل على undefine هو لحد دلوقت ميعرفش هو هيكون فين في الmemory 

الVMA هو الadress الموجود في الRAM والLMA هو الموجود في الFlash 

بيعمل كده مع VAR5 علشان يفرق بينهم بيغير اسمه في الCOMPILATION 

بحط الfunction هنا علشان لو حد عمل ليهم call 


## 3-memory sections

![[Pasted image 20261111033212.png]]

اول حاجة بيعملها الstartup code يعمل init للSP 

الno init ده حته كده في الmemory عادي بس مش بيحصل فيها overwrite بعد الreset بس خد بالك هو volatile عادي 


![[Pasted image 20261111034240.png]]


اول سطر انا بربط الvar ب r7 على طول الصح اني اكتب 

```c
var3=1000;
```

لو مفيش register كفايه انه يشتغل بيها هيديك error فخد بالك متحجزتش الregisters كلها بالطريقة دي 

![[Pasted image 20261111035107.png]]

الtable الاخير اللي طالع من الlinker فيه الphysical address 

الشخص اللي عمل الcompiler هو اللي بيديك الlanguage اللي هتكتب بيها الlinker script لو رحت لlinker script تاني ممكن تلاقي syntax مختلف لكن نفس الconcept 

![[Pasted image 20261112131738.png]]

![[Pasted image 20261112132012.png]]


![[Pasted image 20261112132929.png]]

![[Pasted image 20261112133007.png]]

![[Pasted image 20261112133026.png]]

![[Pasted image 20261112133119.png]]

![[Pasted image 20261112133159.png]]

![[Pasted image 20261112133209.png]]


![[Pasted image 20261112133429.png]]

![[Pasted image 20261112133511.png]]

![[Pasted image 20261112133607.png]]

![[Pasted image 20261112133637.png]]

![[Pasted image 20261112133718.png]]

![[Pasted image 20261112133741.png]]

![[Pasted image 20261112133808.png]]

![[Pasted image 20261112133853.png]]
![[Pasted image 20261112133916.png]]

![[Pasted image 20261112134045.png]]

بنزل هنا var في حته معينه في الmemory 

![[Pasted image 20261112134226.png]]

لو عندي bss محتاج اعرف البدايه من فين ولحد address كام علشان اصفرها 
![[Pasted image 20261112134421.png]]

عمل alias للaddress 
الاسم ده بيكون محجوز في كود الc عادي 

![[Pasted image 20261112134518.png]]

![[Pasted image 20261112134541.png]]

كانه بيعمل كده 

![[Pasted image 20261112134639.png]]

![[Pasted image 20261112134649.png]]

لو عايز احط var في مكان معين شوف الصور دي 

## 4-HLED

![[Pasted image 20261112140400.png]]

![[Pasted image 20261112140455.png]]


الpreprocessor بال '#define' عادي او بال '#' عموما 

الlinking ده لما بعمل struct وابعته ل function 

الpost بالdebugger 

![[Pasted image 20261112140817.png]]


![[Pasted image 20261112140835.png]]

## 5-Systick

![[Pasted image 20261112140844.png]]
