![[Pasted image 20250303174556.png]]
دي الواجهه الرئيسيه بتاعت البرنامج لما بتفتحه.
دلوقتي في الdashboard هتلاقي الحاجات المتعلقه بالscan هتلقي:
1- الlive scan وده اول لما تدخل الموقع بيبدأ الburp يعمله scan من نفسه ويطلع الثغرات الفيه.
2- بتلاقي الscan العادي الانت بتحدده بقا بتعمل new scan وتحط الموقع العايز تعمله scan.

--------------------------------------------------------------------------

![[Pasted image 20250303175120.png]]
اول حاجه الTask type 
1- الlive audit وده بيدور في الموقع علي ثغره معينه حاجات معينه وكدا.
2-الlive passive crawl ده بيدعبس في الموقع عشان يلاقي مثلا ملفات مخفيه parameters والعمليه دي اسمها crawling.

تاني حاجه الtools scope
1-الproxy ده البيوقف الطلبات بتاعت الموقع وكداز
2-الrepeater ده البنستقبل عليه الريكويست عشان نعدلها وما الي ذلك.
3-الintruder بنستخدمه عشان الfuzzing او الbrute forcing.

تالت حاجه ال URL scope 
وافضل خيار ممكن تحطه فيهم هوا الsuite scope عشان ت scan علي حسب الurl المحطوط وكدا وهنعرف ازاي بعدين.

رابع حاجه الDeduplication 
عشان لو لقي حاجه متكرره وكدا يفكسلها.


![[Pasted image 20250303175706.png]]
فيه بردو الscan configuration عشان تخلي الscan اقوي واحسن تعدل عليه وكدا
![[Pasted image 20250303175757.png]]
حاجه زي الaudit الفحص يتم ازاي فا مثلا بتخليه through, normal.

![[Pasted image 20250303175946.png]]
وده بردو تعدل عليه تختار الخيارين دول.

![[Pasted image 20250303180101.png]]
بتدول علي التلات نقط وتعمل الsettings لكل سكان شغال عشان يشتغل ب اقوي حاجه وهكذا.

كل الفوق ده بالنسبه للlive scan.

--------------------------------------------------------------------------
ندخل بقي علي الscan العادي.

![[Pasted image 20250303180156.png]]

![[Pasted image 20250303180233.png]]
لما تدوس علي الweb app scan يطلعلك ده وده المكان الهتحط فيه ال urls العايز تعملها scan.


![[Pasted image 20250303180313.png]]
الconfigurations:-
1-الlightweight ده بيعمل scan كدا علي السريع ياخدله حوالي 15 mins .
2- الfast سريع اه اينعم هياخد ساعه بس بيدور بردو علي الثغرات وكدا.
3- الbalanced وده بقي بين الاتنين بياخد حبه ساعات حلوين.
4- الdeep ده بقي اكتر واحد يطول ممكن يقعد ايام عشان بيدور علي كل الثغرات في الموقع حته حته.

افضل حاجه في كل دول هيا ال balanced.


![[Pasted image 20250303180928.png]]
ده بقي بتستخدمه في حاله انك معاك login password وكدا عشان تسهل عمليه الscan علي موقع معين.

![[Pasted image 20250303181051.png]]
ال scan الانت بتعمله ممكن يتعبك في حته بسبب انه بيتط علي الرامات حبه فا لو الرامات عندك مش عاليه او حلوه كفايه فا هيرخم عليك الرامات هنا بنتكلم علي انها تعدي العشرين.
وفي الجهه التانيه بردو هيتقل علي النت بتاعك عشان هيستخدمه في ال scan.
في حاله انه عمل scan وهيظهر الvulernabilites في الدواير التحت دي الحمره يعني critical والبرتقاني medium والblue يعني low و الgray يعني informative.
والنواتج بتظهر في المنطقه الفي النص.


![[Pasted image 20250303181456.png]]
دلوقتي لو بتscan  علي تارجت معين وكدا فا لو لقي ملفات بيبنالك هنا وبيبعت هوا  ريكويست وبيشوف لو فيه response عشان ساعات الموضوع مهم وممكن تلاقي keys او كدا.


![[Pasted image 20250303181659.png]]
ده بقي الscope البتديه للأداه عشان تقولها تدور فيه ومتطلعش براه 
![[Pasted image 20250303181735.png]]
وبتعمل include subdomains عشان لو الموقع ليه subdomains يبقو من ضمن الscope بردو.
![[Pasted image 20250303181808.png]]


![[Pasted image 20250303181922.png]]
ممكن بردو تشغل ال advanced scope control فا مثلا لو حبيت تحط موقع في الscope ممكن تكتب حاجه منها واحده مش الurl كله وكمان ممكن تكتب كوماندات regex لو حابب وهكذا.

--------------------------------------------------------------------------
![[Pasted image 20250303182135.png]]
دي صفحه الproxy هنا بتوقف الطلبات البتبعتها للمواقع طبعا زي ما عارفين بتشغل الfoxy proxy وبتلقط الريكويست قبل ما يتنفذ في الموقع

![[Pasted image 20250303182224.png]]
بيظهر بالشكل ده وتقدر بعد كدا بعد ما تدوس عليه right click تبعته للrepeater عشان تعدل علي الريكويست.

وقبل ما نروح للrepeater تبقي عارف انك لو عايز تعدي الrequest بتعمل forward ولو عايزه متروحش فا بتعمل drop
![[Pasted image 20250303182455.png]]
وممكن تعمل forward all للريكويستات كلها عشان كلهم يعدو.

لو الfoxy proxy مضايقك او مش عايز يشتغل او حاجه 
![[Pasted image 20250303182626.png]]
ممكن تدويس علي كلمه open browser وهيفتحلك browser مخصوص صحاب الاداه عاملينه عشان يعمل intercept للركويستات.

![[Pasted image 20250303183346.png]]
والhistory ده عشان كل حاجه تمت في الاداه تبانلك.

![[Pasted image 20250303190635.png]]
لما تيجي تعمل filter تقدر تعمل كذا حاجه ومنهم لو عايزها بس يطلع ال requests الفيها parameters بس.

--------------------------------------------------------------------------

![[Pasted image 20250303190838.png]]
هنا في اعدادات الproxy عارفين ان احنا شغالين علي port 8080.

![[Pasted image 20250303190922.png]]
هنا مثلا بتقوله انت بتوقف الطلب بنائا عن اي فا مثلا نختار اخر واحده وفي الاغلب هيا الهنستخدمها عشان يوقف الحاجات الفي الscope الاحنا عايزينه.

![[Pasted image 20250303191414.png]]
حاجه تانيه الطبيعي في الاداه انها بتوقف الطلب وهوا رايح احنا لو فعلنا الخيار ده هتوقفه وهوا راجع الresponse يعني.

![[Pasted image 20250303191531.png]]
ودي بردو فعل اخر واحده هنتعرف علي الsebsocket بعدين هيا المفروض حاجه بتبعت بين المواقع والapi بس هنعرفها بعدين.


![[Pasted image 20250303191651.png]]
دلوقتي لو فعلت التلات حاجات دول في حاجات مخفيه هتبتدي تظهر في المواقع لو فيه حاجات مخفيه.
زي كدا
![[Pasted image 20250303191723.png]]
بعد كدا ممكن نبقي نحقن في الاماكن دي فا الافضل انك تفتحها.


![[Pasted image 20250303191956.png]]
ودي حاجه اسمها match and replace هنتعرف عليها بعدين.
