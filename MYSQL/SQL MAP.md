هيا tool موجوده نقدر نحملها بتعمل automation في الsql injection,
يعني بتلاقي ثغرات sql injection وبتعملها automation عادي جدا.
وتقدر كمان توصل للداتا  بيز ذات نفسها وتوصل للversion بتاع الداتا بيز.
الsql map موجوده علي كالي بشكل افتراضي لو مش موجوده حملها كدا.
![[Pasted image 20250218113335.png]]

--------------------------------------------------------------------------------
لاقيت موقع بقا وعايز تجرب ومتعرفش هوا مصاب بقا ولا لا بتستخدم الاداه كدا تحطلها الرابط وهيا هتقوم بالواجب.
![[Pasted image 20250218113524.png]]
![[Pasted image 20250218113535.png]]
بتشتغل وبتحاول تعمل injection.

![[Pasted image 20250218113628.png]]
ممكن تشيل الgifts دي وتحط بدالها نجمه وساعتها هيجرب في المنطقه دي بس ومش هيجرب في حاجه تانيه.

![[Pasted image 20250218113824.png]]
دلوقتي ال u- دي بنستخدمها لما الurl يبقي في parameter عشان يجرب عليه.
الdata-- دي بنستخدمها لما في الريكويست نلاقيها بالpost method وساعتها نحددله هيعمل inject فين عشان لما بتبقي في الurl ساعتها دي post method.
الcookie-- انت ممكن تحقن في الcookies فا دي بنستخدمها عشان كدا و الrandom-agent-- عشان متاخدش حظر وتقدر تكمل شغل عادي ونفس الكلام علي ال proxy و tor كلهم بنستخدمهم عشان متخدش حظر من الموقع.

![[Pasted image 20250218114150.png]]
في حاجه كمان اسمها الlevel والrisk دول لما بتعملهم علي اعلي حاجه فا الاداه ساعتها بتستخدم كل حاجه عندها.

![[Pasted image 20250218114230.png]]
حاجه اسمها a- دي بتتطلع الداتا كلها من الdatabase.
وباقي الحاجات مشروحه يعني اقرأهم شوفو بيعملو اي.
من ضمن الحاجات المهم الهيا dump او dump all بتعمل retrieve للداتا كلها بردو.


![[Pasted image 20250218114340.png]]
حاجه بتعلي من خطوره الsql map انها بتخليك تفتح shell علي جهاز الضحيه اكنك صاحب الجهاز تنفذ كوماندات وكدا.

--------------------------------------------------------------------------------
![[Pasted image 20250218114628.png]]
لو عايز تستخدم الsql map عشان تشتغل علي الrequest تاخد الريكويست كلها كوبي وتعمل file تحطها فيه.

![[Pasted image 20250218114712.png]]

![[Pasted image 20250218114722.png]]
وبعد كدا تعمل الكوماند ده عشان يستخدم الfile يعمل check عليه يعني.

![[Pasted image 20250218114825.png]]
ممكن تعمل حاجه الهيا تحط نجمه في المكان العايزه عشان يحقنه هوا بس ويفكه من باقي الحاجات.
![[Pasted image 20250218114856.png]]
هيقولك انه اكتشف نجمه عايز تحقن الحته دي بس ولا ايه وتقوله yes ويشتغل بقا.

--------------------------------------------------------------------------------
![[Pasted image 20250218115057.png]]
في امر ممكن تشتغل بيه بتديله ال url منغير الparameter وهوا بيعمل الparameters من عنده بيقعد يجربها من عنده.

![[Pasted image 20250218115150.png]]
وده بالنسبه للpost ريكويست ممكن تاخد الparameter وتحطه في single quotes كدا زي ما هوا عامل.
![[Pasted image 20250218115316.png]]
زي ما قولنا بردو تحقن الcookie ذات نفسها.

![[Pasted image 20250218115415.png]]
الحاجات دي للheaders يحقن فيها ويقعد يجرب لو عايزينه يجرب يعني.
![[Pasted image 20250218115503.png]]

--------------------------------------------------------------------------------
![[Pasted image 20250218115610.png]]
دلوقتي ساعات في urls بتبقي من غير ال id المكتوب في المثال ده بيبقي اخرك علامه الاستفاهم فا فيه tools بنستخدمها بتحاول تجيب الparameters بتاعت الurl وكدا الهما arjun و param miner والparam دي extension للburpsuite.

![[Pasted image 20250218115801.png]]
ممكن تنزلها بالpipx.
![[Pasted image 20250218115953.png]]
بتدي الاداه الرابط زي كدا.
![[Pasted image 20250218120013.png]]

![[Pasted image 20250218120337.png]]
امر بكتبهوله عشان اقوله ان الparameter هيبقي موجود في الbody مش في الrequest.
مش في الرابط يعني.
![[Pasted image 20250218120438.png]]
وده الامر بتاع الsql map عشان يجرب في الbody بردو مش في الrequest بس بتستخدمه بعد arjun عشان تكون جبت الparameter وهوا id.

![[Pasted image 20250218120557.png]]
اهوا كدا الid موجود في الbody فعلا تحت.
![[Pasted image 20250218120616.png]]
وبعد ما الsql map تقول اي الممكن تحقنه بتحطه في الحته دي وتعمل send كل ده باستخدام الburpsuite طبعا.

--------------------------------------------------------------------------------
![[Pasted image 20250218124306.png]]
في الburpsuite فيه extensions كتيره تقدر تحملهم وتستخدمهم ولو معاك pro بيبقي فيه extensions اكتر.

![[Pasted image 20250218124351.png]]
فيه واحد منهم القولنا عليه هنحمله الهوا الparam miner.
![[Pasted image 20250218124424.png]]
هتلاقيها في الinstalled تروح تفعلها عشان مش هتلاقيها متفعله.
![[Pasted image 20250218124519.png]]
الrequest العايز تستخدم عليها الparam miner بتدوس كل يمين وتعمل زي ما موضح في الصوره كدا.

![[Pasted image 20250218124829.png]]
ساعات الحركه دي مش بتنفع الcookie عشان المفروض الrequest كلها تروح مره واحده فا بتعمل حاجه اسمها encode  للرساله عشان الrequest تتبعت كلها مره واحدها فا بتحدد الحاجه العايز تعملها encode وتعمل ctrl+u.
![[Pasted image 20250218125340.png]]
فا بيبقي شكله كدا.

--------------------------------------------------------------------------
![[Pasted image 20250219174705.png]]
دي الtechniques بتاعت sql map ممكن تستخدم الانت عايزه لو حابب بقا تستخدم كل الtechinuques فا بتعمل الامر الاخير الهوا technique=BEUSTQ-- .
![[Pasted image 20250219174838.png]]
ل اوحبب تستخدم technique معين بتكتب الامر كدا.
![[Pasted image 20250219175155.png]]
يفضل تقول no.

بردو بدل الامر الفوق ممكن تستخدم ده 
![[Pasted image 20250219175347.png]]


![[Pasted image 20250219175840.png]]
شرح الامر ده دلوقتي ال batch عشان تجيب اصدار الsql و الrandom agent عشان ميتعملكش بلوك فا كل مره بتبعت من ip مختلف وهكذا و ال drop set cookie بقوله انك متبعتش cookie لحد اما اخلص عشان الcookies ممكن تمنعك. الbanner بردو متشغلش بالك بيه زي الbatch عشان بيجيب نوع الداتا بيز 
الthreads 10 يعني كميه الطلبات البتبعتها الاداه في الثانيه وبلاش تعلي عن كدا عشان ممكن يديلك بلوك وبعد كدا بتقول dbs -- عشان يجيبلك نوع قواعد البيانات او اسمائها.

![[Pasted image 20250219180227.png]]
شرح الامر انه مثلا عايز تجرب علي parameter معين فا بتقول p- اسم الparameter وهوا بيجرب فيه الlevel 5 يعني بشتغل الاداه علي اقوي حاجه وطبعا بتاخد وقت عشان بيجرب كل حاجه ونفس الكلام علي الrisk
دلوقتي dbms-- لو انت عرفت تجيب نوع قواعد البيانات المستخدمه في الموقع فا ممكن تحطها وبذلك هيجرب بس علي قاعده البيانات المعينه الانت حطيتها ومش هيجرب علي كلو فا هياخد وقت اقل ,الhostname مشتغلش بالك بيه وfilter بقوله خليك في الجزء ده ده في حاله بردو انك عارف الversion بتاعت قاعده البيانات و ignore code دي ساعات ونت بتيست في موقع بيقعد يطلع خطأ خطأ خطأ فا انت بتقوله ignore الاخطاء دي عشان من كتر الاخطاء ساعات الاداه بتقف والرقم 500 دي اسم كود الخطأ فا علي حسب كود الخطأ البيتكرر كتير بتحطهوله وهوا بيعمله ignore.


![[Pasted image 20250219212403.png]]
شرح الامر انه دلوقتي اي حاجه في الheader عايز تحقنها او الsql map يجرب عليها فا بتكتب الكود ده بيجرب في الcookies اول لما يلاقي واحده و host و user agent اي header عمتا وبيديلك alert اول لما يلاقي بقا حاجه.

---------------------------------------------------------------------------
![[Pasted image 20250219212610.png]]
دلوقتي في حاجها اسمها tampering يعني تخطي دلوقتي نفترض انك عملت اول كودين فا الfirewall قشفهم وادالك بلوك واحنا مش عايزين كدا فا احنا بنحاول نتخطي الfire wall ب انني مثلا زي الكود الاخير نكتب ال sLEEP كدا او نعكسهم مثلا Sleep كدا يعني تغير في شكله الكلمه عشان تعدي الfirewall تحط + هكذا.

![[Pasted image 20250219212838.png]]
الtamper يعني بيغير شكل الtechnique اللpayload بتاع الاتاك عشان ي bypass الfirewall.
![[Pasted image 20250219212937.png]]
![[Pasted image 20250219212946.png]]

عشان لو عايز توصل للscripts بتاعت الsql map الموجوده
![[Pasted image 20250219214025.png]]
بتروح هنا وتدخل علي tamper.
![[Pasted image 20250219214040.png]]
هيبقو ظاهرين بالشكل ده.
![[Pasted image 20250219214245.png]]
طريقه كتابه الكود.


--------------------------------------------------------------------------
![[Pasted image 20250219214418.png]]
اداه اسمها identywaf بتخليك تعرف الfire wall القدامك وعلي اساسه تستخدم الtamper المناسب ليه عشان تعمله bypass ابقي دور عليها في github.
![[Pasted image 20250219214544.png]]

