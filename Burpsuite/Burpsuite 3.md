Intruder & Turbo intruder
فايدته انه بيعمل fuzzing , brute forcing.

![[Pasted image 20250305142825.png]]
تعمل add و العلامه البتظهر دي بتبقي علي المكان الهيتعمل عليه fuzzing.

![[Pasted image 20250305142950.png]]
لو معاك wordlist وعايز تستخدمها فا بتيجي هنا وتعمل load وتختار المكان الفيه ال wordlist بتاعتك.
![[Pasted image 20250305143033.png]]
هتلاقيها اتضافت في ال list التحت وتختار منها.

![[Pasted image 20250305143123.png]]
دلوقتي العلامات دي بيتعملها encoding فا لو مش عايزهم يتعملهم encoding بتشيل العلامه من علي البوكس ده.![[Pasted image 20250305143157.png]]


![[Pasted image 20250305143639.png]]
في صفحات بيبقي فيها حاجه اسمها prompt login ابحث عن شكلها المهم يعني انها بيبقي ليها حاجه في الheader اسمها authorization بتبقي المفروض انها encoded بالbase64 ونت لما بتيجي تعمل fuzzing فا لازم التيكست يتحول يتعمله encode لل base64 بتختار الطريقه في ال payload processing وتعمل add
![[Pasted image 20250305143832.png]]
وتختار الencode بطريقه الbase64.
![[Pasted image 20250305143855.png]]


--------------------------------------------------------------------------
![[Pasted image 20250305143933.png]]
فيه حاجه اسمها الturbo intruder وهيا نسخه محدثه من الintruder بتشتغل بالبايثون.

![[Pasted image 20250305144017.png]]
عشان تستخدمها بتبقي كدا.

![[Pasted image 20250305144048.png]]
هتلاقيها فتحت معاك كود مكتوب بالبايثون.
ولو دوست فوق علي القايمه ساعتها هيطلعلك حاجات الاكثر استخداما او هوا الهنستخدمه هيبقي الbasic الهوا بيعمل fuzzing.

![[Pasted image 20250305144139.png]]

![[Pasted image 20250305144156.png]]
بعد ما تدوس عليه هيفتحلك الكود وهيبقي مكتوب المسار بس تاخد بالك ان ده مسار لينكس وده المفروض المسار بتاع الwordlist الهتستخدمها.

--------------------------------------------------------------------------
![[Pasted image 20250305144357.png]]
الاتاك ده نفترض مثلا انك في موقع وبيديك كوبون خصم 20% بيبقي اكيد استخدام وحيد مره واحده فا انت بقي بتبعت الريكويست بتاعت استخدام الكوبون ده وبتخليه يبعت طلب استخدام الكوبون ده اكتر من مره دفعه واحده فا الموقع بيبقي مش عارف اي ده فا بيقفبل الكوبونات دي وبتلاقيها عمل الكوبون اكتر من مره فا مره علي مره لو الحاجه مثلا 1300 دولار هتلاقيها ببلاش او سعرها قل جدا وهكذا.

![[Pasted image 20250305144742.png]]
هنا بتحدد عدد ريكويستات الهتتبعت للموقع في الثانيه.

![[Pasted image 20250305144818.png]]
بتقفش طلب الapply للكوبون وتبعته لل intruder عشان تنفذ الاتاك.

![[Pasted image 20250305144905.png]]
انا مش هلمس حاجه من الريكويست عشان انا مش بعمل fuzzing بس وتنفذ الاتاك.
![[Pasted image 20250305144948.png]]
تعمل اتاك وتستني تشوف هينفع ولا لا.
الاتاك اسمه race condition.

--------------------------------------------------------------------------
![[Pasted image 20250305145134.png]]
الfuzzing بقي مش هنعمل add وكدا زي الintruder المكان العايزين نعمل فيه fuzzing نحط فيه s%.
بس كدا.
