Cross-site request forgery 
![[Pasted image 20250628082608.png]]
باختصار تقدر بيها تغير ال username او الpassword او الname او ال address الخاص بالشخص 
لازم الشخص يخش علي الموقع بتاع الattacker عشان الثغره دي تتم

هحاول اكتب الانا فهمته
دلوقتي الهكر بيعمل موقع بيبقي clone للموقع الاصلي الريكويست بتاعت تغير الشيء تحديدا

يعني دلوقتي انا كهكر بدخل اعمل ريكويست طلب يعني اني اغير ال gmail بتاعي وكدا فا بعمل intercept للريكويست ده واخده لنفسي واعمل drop للريكويست.


![[Pasted image 20250628215905.png]]
![[Pasted image 20250628215938.png]]
![[Pasted image 20250628215949.png]]
![[Pasted image 20250628220000.png]]
المفروض لو عملت send فا هيطلع معاك ال response انه اتغير خلاص بس احنا مش عايزين كدا احنا هنعمل website يغير مكاني الemail بتاع الvictim.
![[Pasted image 20250628220049.png]]
في النسخه المدفوعه من burpsuite بتوفرلك الخيار ده وتقدر تعمل صفحه علطول بنفسها.
![[Pasted image 20250628221908.png]]
![[Pasted image 20250628221916.png]]
وزي ما قولت نتأكد انك عملت drop للريكويست عشان ميتبعتش.

![[Pasted image 20250628221942.png]]
وتشوف الايميل اتغير ولا متغيرش هنلاقيه متغيرش عشان عملت drop.

![[Pasted image 20250628222043.png]]
فكره الكود اني بقول للصفحه الاحنا بنحاول نخترقها انها تغير الايميل بتاع الضحيه لل email بتاع الهكر.![[Pasted image 20250628222152.png]]
بنعمله save as html.
![[Pasted image 20250628222216.png]]
اول لما ادوس submit 
![[Pasted image 20250628222254.png]]
هنلاقيه اتغير.


-------------------------------------------------------------------------------------
طب ازاي المواقع بتحمي نفسها من الاتاك ده والاتاك بيحصل بسبب عمتا ال programmer بتاع الموقع مش من الuser.

المواقع بتحط حاجه اسمها csrf poc الهيا CSRF Proof of Concept.
الهيا بتمنع ان اي حد يروح للموقع الا من خلال الموقع بتاعهم يعني لما حد يبعت للسيرفر يتأكدو فعلا ان الريكويست طلعه من الموقع بتاعهم مش من حته تانيه.
والحاجات البتتأكد اسمها CSRF referer او CSRF Token.
![[Pasted image 20250628224750.png]]
شكل ال token بتبقي ازاي في الrequest.
![[Pasted image 20250628225049.png]]
عشان تعمل bypass للtoken مثلا فا بتجرب اصلا تمسحها تشوفه هيعمل check عليها ولا لا تجرب تغيير القيمه بتاعت ال token يعني تنقص حرف وتبدل مكانه وهكذا لو طلع بردو بيعمل check تحاول تجرب حاجات تانيه.
![[Pasted image 20250628225238.png]]
تمسحه خالص
وتغيير ال request method من post ل GET.
![[Pasted image 20250628225310.png]]
![[Pasted image 20250628225316.png]]
![[Pasted image 20250628225321.png]]
لما تعمل send هتلاقيه غير فعلا وعمله bypass.

![[Pasted image 20250628225635.png]]
وبتعمل بقا generate ل صفحه ال html و ترفعها علي ال exploit server بتاعك وكدا انت هكرت الموقع.
