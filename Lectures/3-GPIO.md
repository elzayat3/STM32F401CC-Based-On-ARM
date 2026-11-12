
---


## 1-How to write clean code

![[Pasted image 20261110113202.png]]

بلاش تعمل الUL علشان بتختلف من الWINDOWS للSTM32 

انا بعملها على الWINDOWS علشان الunit test 

![[Pasted image 20261110113739.png]]

![[Pasted image 20261110114051.png]]

![[Pasted image 20261110114134.png]]



## 2-How to validate input

![[Pasted image 20261110114526.png]]

![[Pasted image 20261110114621.png]]


## 3-Testing

![[Pasted image 20261110115053.png]]


الcritical اي حد هيستخدم الكود ده هتطلعه المشكلة 
الmajor مشكلة هتطلع تحت سيناريو معين مش دائما هتطلع 
الminor مشكلة موجودة بس مش مأثره اوي على الsystem زي الcheck على الindex بتاع الarray 

انت بتعمل test ضد حاجة اسمها requirements 

الunit test بتاكد انه الfunction شغاله صح على الwindows بتاعي 

الvalidation مش بيكون موصل debugger 

الsystem validation test مش بيشوفوا S.W ممكن يجيب Decoder يركبوه على الmotor ويشوفوا زي ما هما عايزين ولا لا 

بيشوفوا الsystem spec بشوفوه ب react صح ولا لا 


![[Pasted image 20261110121257.png]]

الunity دي عبارة عن platform تخليك تطلع ال.exe بدل ال.hex او .elf بشتغل الكود على اللابتوب 

الTC قصده هنا test case 

الASSERT بتتاكد انه الاتنين INPUT زي بعض 

بيطلع HTML Report يقلك انه فيه مشكلة لو حصلت مشكلة

ال positive scenario لما ادخل الinput صح 

ال negative scenario لما ادخل الinput غلط 

انا بكتب الunit test ده في document

## 4-GPIO 

![[Pasted image 20261110122303.png]]

![[Pasted image 20261110122613.png]]

![[Pasted image 20261110122628.png]]

![[Pasted image 20261110123859.png]]

![[Pasted image 20261110123914.png]]

![[Pasted image 20261110124022.png]]


![[Pasted image 20261111014530.png]]


لو الvolt بتاع الpin اكبر من ال2.3 هيطلع الVDD على الOUTPUT لو العكس هيطلع الVSS

انا هحتفظ على القيمة بين الThreshold 

لو حصل spicks في الvolt مش هتبان معايا ده هدف الschmitt trigger 

![[Pasted image 20261111015550.png]]

![[Pasted image 20261111015632.png]]

![[Pasted image 20261111020031.png]]




