
---


## 1-callback function 

![[Pasted image 20261113192205.png]]

![[Pasted image 20261113192416.png]]


اول bit في الaddress بتاع الfunction هيا مش بتمثل address هيا بتمثل flag for thumb لو الprocessor حاول يعمل fetch ل address وملقاش الواحد ده موجود هيروح يعمل hard fault على طول اللي بيحط ال1 ده هو الlinker 
## 2-Sync & Async function

![[Pasted image 20261113195004.png]]


الsync لازم لما هيا هتعمل return هتعرف انها خلصت الشغل اللي المفروض تعمله 

الAsync لو الblocking او الsync بتاخد وقت كبير اوي وقتها هتحتاج الAsync


## 3-APCS

![[Pasted image 20261113201131.png]]


الBL فيها limitation علشان تشتغل بسرعة ب one instruction هيعرف يعمل branch على قد 16MB بس وده بيكون near address 

لو انا بعمل call ل function في الRAM الفرق بيكون كبير 

لو الaddress بعيد هتلاقي الcompiler بيشتغل ب ins تانيه اسمها BX

دي بتعمل CALL للvar address 

لو هروح مثلا لل0x20000000 محتاج اعمله save في الr12 

الBL طبعا اسرع 

![[Pasted image 20261113202729.png]]


![[Pasted image 20261113202811.png]]


![[Pasted image 20261113202850.png]]

![[Pasted image 20261113202951.png]]


![[Pasted image 20261113203101.png]]


![[Pasted image 20261113203142.png]]



## 4-NVIC

![[Pasted image 20261113203749.png]]



![[Pasted image 20261113203836.png]]


![[Pasted image 20261113203948.png]]

ال0X08000000 ده جواه ال0X08000200

الvector ده عبارة عن array of addresses 


![[Pasted image 20261113204117.png]]

![[Pasted image 20261113204133.png]]


![[Pasted image 20261113204201.png]]

![[Pasted image 20261113204438.png]]


![[Pasted image 20261113204650.png]]


![[Pasted image 20261113204915.png]]

![[Pasted image 20261113205015.png]]


اللي فوق يمين هتتخزن في الLR علشان وانا راجع اعرف انا راجع على ايه 

![[Pasted image 20261113210457.png]]

الBASE_PRI لو جالي اي IRQ فوق ال10 مش هيشتغل اي حاجه تحت ال10 هتشتغل الDEFAULT بتاعه zero 

اللي فوق لو شغله هيشغل اتنين int بس الNMI & Hard fault 

خد بالك هنا مش هيعمل jump على الreset handler لو عملت reset 

لو حصل hard fault وانا قافل الhard fault هنا هيخش في حاجة اسمها save mode بstuck بيوقف execution اصلا ويعمل set لل flag بتاع الhard fault 

ممكن اعملها انه اروح انفذ instruction غلط مثلا او اعمل exception جوه الexception 

لو انا رحت للvector table وخليت الISR كلها NULL هيديك Exception ويوقف تنفيذ 

![[Pasted image 20261113211628.png]]

![[Pasted image 20261113212231.png]]

![[Pasted image 20261113212308.png]]

