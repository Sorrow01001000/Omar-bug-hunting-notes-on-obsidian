![[Pasted image 20250202051725.png]]
اسمه Network File System وهوا بديل لبروتوكول SMP.
بينقل فايلات بردو وبسمح بالaccess للfiles الموجوده علي الشبكه طلاما هيا موجود في الlocal storage.
بيشتغل علي port 111,2049.
![[Pasted image 20250202051931.png]]
بيبقي بين ال client والسيرفر والاول قبل ما يبعت بيتأكد ان الclient عنده الصحليات عشان يتبعتله الملف ده.


![[Pasted image 20250202052017.png]]
ال nfs بيشتغل عن طريق حاجه اسمها RPC ده اسم الserviece.
والserviece دي مش بتشتغل مع حاجه غير الNFS.
بتتحكم في الfiles وهيا رايحه وراجعه وكدا.

-------------------------------------------------------------------------------
الvulnerabilities 
![[Pasted image 20250202052232.png]]
اول حاجه - الاصدارات القديمه بتاعت NFS التشفير فيها ضعيف جداا.
تاني حاجه- تقدر تنفذ علي spooffing او MITM.
تالت حاجه- بيحصل misconfiguration ساعات فا تقدر تديلك permission لsensitive data.
رابع حاجه- الdos attack.

-------------------------------------------------------------------------------
اول سيناريو معانا
![[Pasted image 20250202075801.png]]
واخطر سيناريو ال Unauthorized Access.
لأن السيناريو ده بياخد كوبي من الملفات كلها الفي السيرفر ويحطها عندك.

![[Pasted image 20250202075911.png]]
ساعتها بتستخدم الامر ده في حاله ان الport 111,2049 شغالين وتنزل نسخه من الملفات عندك.
![[Pasted image 20250202090824.png]]
لو طلعلك الأمرين دول ساعتها النجمه هيا الانا عايزها .
النجمه دي معانا ان الfile shared لكل الناس.
وده معناه انك تقدر تنزله علي الجهاز .

![[Pasted image 20250202091351.png]]
وده بردو أمر عشان تنزل الملف الانت عايزه من علي الport لجهازك
![[Pasted image 20250202091422.png]]
هنا بيبقا اسم الملف الانت عايز تنزله.

--------------------------------------------------------------------------------

![[Pasted image 20250202091505.png]]
تاني سيناريو ممكن تعمل data interception.
بتحاول تتجسس علي الشبكه بالtcpdumb يا اما الwireshark.

-------------------------------------------------------------------------------
تالت سيناريو 
![[Pasted image 20250202093217.png]]
انك تعمل dos attack عن طريق الامر ده.

-------------------------------------------------------------------------------

![[Pasted image 20250203015411.png]]
بتستخدم showmount عشان تعرف الحاجات الهناك.

![[Pasted image 20250203015547.png]]
و mount عشان تنزلها. 

![[Pasted image 20250203021503.png]]
لو نزلت الملفات ومش باينه غير الownership بتاعت الملف عن طريق الامر وممكن تبقي هيا دي المشكله عشان تشوف الملفات.

-------------------------------------------------------------------------------
