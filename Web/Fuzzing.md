الfuzzing معناه انك بتدور علي ملفات مخفيه او parameters مخفيه او مكان مخفي في الريكويست وبتحاول توصله.
في اداوات بنستخدمها في الfuzzing منهم :
![[Pasted image 20250301184507.png]]
في طبعا حاجات كتير غيرهم بس دول مفضلين.
![[Pasted image 20250301184609.png]]

![[Pasted image 20250301184634.png]]
في الحاله دي مثلا جت تخمن فا طلع خطأ انه مش موجود وكدا.
![[Pasted image 20250301184702.png]]
فا هي المفروض بتحمن عشان توصل للحاجات ال200 OK.

الاداه لازم تديلها word list عشان هيا مش هتعمل fuzzing من نفسها ممكن تديها الseclist
![[Pasted image 20250301184818.png]]
الsec list فيها حاجات كتيييير للباسوردات وكدا.

![[Pasted image 20250301184957.png]]
ايام لما اشتغلنا ال DNS عشان نعمل sub domain enumeration  كان بردو استخدمنا ملف من هناك بس المرا دي هندخل علي Web-Content, هتلاقي فيها الraft وده في الغالب الملف الهنستخدمه.

![[Pasted image 20250301185148.png]]
الكوماند الاساسي في الfuff.
example:
![[Pasted image 20250301185208.png]]
هيخمن فين ؟؟ مكان كلمه FUZZ.
![[Pasted image 20250301185350.png]]
الامر ده عشاو لو عايزين نفلتر كود معين ميطلعش معانا.

![[Pasted image 20250301185647.png]]
دلوقتي نفترض عندنا 2 wordlists وعايز كل واحده تعمل fuzz علي مكان معين تعمل اي ؟ 
زي ما موضح كدا تكتب اي كلمه من عندك في الخانه العايز تعمل fuzz فيها وتحط الwordlist العايزها تfuzzمكان الكلمه المعينه البعد النقطتين وليكن في المثال بتاعنا hossam يبقي الwordlist هتfuzz مكان كلمه hossam.

![[Pasted image 20250301185901.png]]
افتكر ان فيه حاجه اسمها recursive fuzz ده عشان مثلا لو عملت fuzz فا نقلك جوا ملف والملف جواه ملف فا نقلك فيه وهكذا.


![[Pasted image 20250301190123.png]]
لو عايز تشتغل ب method معينه فا تقدر تحددها بالامر X- .

--------------------------------------------------------------------------
![[Pasted image 20250301190552.png]]
في حاله عايز يبعت في body الrequest فا بتستخدم الميثود الهتبعت فيها ويعمل fuzz فين وكدا.


--------------------------------------------------------------------------
![[Pasted image 20250301190811.png]]
دي الdirsearch وتقدر تحملها عادي ب pip3.
وهوا عنده wordlist فا فاجر.

![[Pasted image 20250301190919.png]]
وكمان ممكن تضيف wordlist عشان تخليها افجر.

![[Pasted image 20250301190950.png]]


![[Pasted image 20250301191011.png]]
لو عايز تشتغل ب method معينه.


![[Pasted image 20250301191038.png]]
دلوقتي في حاله انك لاقيت فايل ب method الpost وجيت تجرب تفتح في الموقع فا مش هيردي اصلا عشان المفروض يوصل بالpost مش بالget 

![[Pasted image 20250301191125.png]]
فا بتعمل حاجه زي كدا عشان يرجع الrequest.

\
![[Pasted image 20250301214221.png]]
وده عشان لو عايز extensions زياده غير الdefault.


--------------------------------------------------------------------------
حاجات advanced سيكا !!!

![[Pasted image 20250301214631.png]]
ده عشان ت bypass الfirewall فا بتقول علي الip ده عشان اكنك بتقوله انك local host فا متعمليش بلوك.


![[Pasted image 20250301214817.png]]
ده عشان يعمل fuzz علي الsub domains .

![[Pasted image 20250301214931.png]]
لو حبيت تستخدمها بدل الarjun .

![[Pasted image 20250301215133.png]]

![[Pasted image 20250301215305.png]]
ضيف أمر full url وهوا بيعمل fuzzing عشان يجيبلك الurls كامله بتاعت الحاجه ال لاقاها.

![[Pasted image 20250301215517.png]]
