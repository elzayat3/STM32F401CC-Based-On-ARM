
---


## Lecture map

1-[[#1-Modifiers]]
2-[[#2-Documents]]
3-[[#3-Registers with RCC]]
4-[[#4-RCC intro]]
5-[[#5-Reset]]

---

## 1-Modifiers 

![[Pasted image 20261106202937.png]]


حط volatile قبل الvariable اللي هتستعمله في الISR علشان ممكن الCOMPILER يشوفك مش بتعمل CALL للfunction دي يروح عامل optimization وشايله 

## 2-Documents

![[Pasted image 20261106203544.png]]

انا لو واحد هيشتري الcontroller هروح ابص على الDS واعمل لها analysis بيديك صورة سطحية عن الcontroller 

STM-->Vendor name 

32 --> الprocessor كام bit 

F-->Generic مش معمول لمجال بعينه 

4--> Cortex M4 

01--> Version 

CC--> Memory واحد للflash ووحده للRAM

![[Pasted image 20261106210547.png]]


## 3-Registers with RCC

![[Pasted image 20261106210912.png]]

الregister بيحتفظ هيا 1 ولا 0 عن طريق الflip-flop  

الflip flop دي بيكون داخل ليها الCLK والinput والstatus الstatus المقصود هنا الvalue الموجودة حاليا اللي الH.W logic بيشتغل بيها الstatus بيحصله Update عند كل raising edge 

## 4-RCC intro 

![[Pasted image 20261106211420.png]]


![[Pasted image 20261106211749.png]]

![[Pasted image 20261106211810.png]]

![[Pasted image 20261106211921.png]]


![[Pasted image 20261106211946.png]]

![[Pasted image 20261106212101.png]]

دور الCSS لو حصلت مشكلة في اي clock وهيا الsystem انه يروح على clock شغاله غالبا هتكون الHSI  
## 5-Reset

![[Pasted image 20261106213006.png]]

دي انواع الRESET وايه اللي بيخلها تحصل

الnRST هيا PIN لو عملت عليه LOW هتعمل reset

الinstruction to reset بتكون عبارة عن soft reset الexceptions بتدخللك على ISR بيكون فيها line assembly كده بيعملك reset 

انا بحتاج اعرف سبب الreset بعرفه من الRCC فيه register خاصه للكلام ده 

الDET دي function لما يحصل اي مشكلة في الsystem بنعمل call للfuncrion دي علشان نعرف سبب المشكلة 

![[Pasted image 20261106214012.png]]

الregisters بتاعت الperipheral هترجع للreset value 


