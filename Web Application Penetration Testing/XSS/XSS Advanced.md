![[Pasted image 20250626235406.png]]
كالعاده بنشوف الكلمه سمعت فين في الكود ونجرب نحقن مره بتعديل الكود الفوق ومره بتعديل الكودل التحت ونجرب.

![[Pasted image 20250626235511.png]]
الشكل المتعودين عليه.

![[Pasted image 20250626235544.png]]
هنلاقيه منفعش فنخش علي الكود نشوف اي الحصل


![[Pasted image 20250626235620.png]]
هنلاقيه اتعمل encoding بال html.
هتعرف انه html بالحاجات المكتوبه زي gt الهيا المفروض greater than و ال lt الهيا less than.
لو لاقيته بيعمل كدا اعرف انه بيحول الكلام ل text عادي فا مش هتعرف تعمل inject بالطريقه دي.


![[Pasted image 20250626235845.png]]
نجرب في المكان التاني الظهر في الاسم
![[Pasted image 20250626235910.png]]
بردو هنلاقيه منفذش الكلام.

![[Pasted image 20250626235943.png]]
لو ركزنا في المثالين هنلاقيه بيعمل encode لعلامه الاكبر من والاصغر من <> فا لازم نلاقي حل
![[Pasted image 20250627000115.png]]
هناخد بالنا انه معملش encode لل "" لل دابل quote فا ساعتها نجرب نحقن جوا ال double quote ونحاول ناخد بالنا من ال double quote الهوا هيحطها واحنا نحط اي بالظبط.

![[Pasted image 20250627000309.png]]
فا كدا لما حد يضغط في مربع البحث هيطلع alert فعلا .

----------------------------------------------------------------------------------------


![[Pasted image 20250627064917.png]]
فيه حقنين بعد الheader زي ده.

وفي حاله انه لو مقفلش ال header  ساعتها بتحقن جواها مثلا.


![[Pasted image 20250627065302.png]]
شكل ل payload عشان يسجل ال cookies.


----------------------------------------------------------------
![[Pasted image 20250627065515.png]]
شكل سكريبت جافا سكريبت 
لو فصصت الكود وفهمته هتعرف ان الكلمه بردو بتسمع هنا في الكود مكان كلمه+query+ فا نحاول نحقن في المكان ده 
![[Pasted image 20250627065658.png]]
فا مثلا ده شكل payload ممكن يشتغل في الحاله دي.
الفكره انك بتقفل ال double quotes والquote وبتزود ال payload في الحته دي فا بتعمل alert
![[Pasted image 20250627065748.png]]

![[Pasted image 20250627070011.png]]
وارد بردو لو جربت تعمل search ولاقيته مش بيسمع في ال source code  ولاقيته بيسمع في الرابط ممكن تكتب payload زي ده ووارد يطلع معاك alert.

![[Pasted image 20250627070109.png]]
ووارد تلاقيه url فا بردو بتكتب نفس الpayload تجرب يمكن يطلع alert.

![[Pasted image 20250627070243.png]]
شكل تاني لحقن الروابط.

----------------------------------------------------------------------


![[Pasted image 20250627084356.png]]
بعد تحليل موقع من المواقع مثلا.
المفروض بتكتشف ان الموقع بيبعت الحاجات عن بعد بطريقه ما.
فا ساعتها بتجيب payload زي ده
![[Pasted image 20250627084634.png]]
وتعمله save as . html
في ال src بس بتغيره وتحط الموقع المصاب بالثغره او الهوا يعني شاكك انه مصاب بالثغره.
ال# مهم المفروض بيفصل الparametrs.


![[Pasted image 20250627085609.png]]
لما تلاقي بردو موقع شغال ب جافا سكريبت وشكل الكود كدا  وعلطول بتلاقي الtext بتسمع في ال script فا انت تحاول تحقن وتراعي ال semi colon و ال quotes وكدا وتحقن علطول تعمل alert.

![[Pasted image 20250627085716.png]]
![[Pasted image 20250627085725.png]]
