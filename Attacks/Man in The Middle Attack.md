![[Pasted image 20250129190434.png]]
![[Pasted image 20250129190529.png]]
ادوات تنفيذ الattack هما ettecap و bettercap وكلاهما موجودين علي لينكس.
فكرت الetterap انها بتعمل اعاده توجيه للرسايل الجايه من الراوتر توديها ليك وبعد كدا للكمبيوتر التاني وهكذا.
![[Pasted image 20250129190750.png]]

-------------------------------------------------------------------------------

![[Pasted image 20250129192308.png]]
عايز تفتح الاداه يا تكتب الامر ده في الterminal يا عادي اكنك بتفتح اي app وتدور علي اسمها.

![[Pasted image 20250129193038.png]]
بعد ما تفتح الاداه بتبقي ظاهره بالشكل ده بتختار علي حسب انت موصل واي فاي ولا ethernet cable 
وبعد كدا بتدوس علي علامه ال صح عشان تعمل sniffing .
الاداه مسئوله انها توقف الريكويستات الرايحه والراجعه وبعد كدا تتجسس عليهم .

![[Pasted image 20250129193212.png]]
لو عملت كدا بيبدا يعمل scan علي الشبكه ويشوف الاجهزه المتوصله علي الشبكه 
![[Pasted image 20250129193426.png]]
فا بيطلع ال list بتاع الhosts . 
بعد كدا بتروح للراوتر
![[Pasted image 20250129194222.png]]
تعمله add كدا
![[Pasted image 20250129194244.png]]

وتختار الجهاز التاني العايز تتجسسس عليه وتحتطه 
![[Pasted image 20250129194303.png]]

![[Pasted image 20250129194353.png]]
عشات تشوف الtargets الحاططتهم تعمل كدا.
![[Pasted image 20250129194415.png]]
وتختار ده هيطلعك target 1 , target 2.

![[Pasted image 20250129194455.png]]
وعشان تتبدي تتجسس تعمل كدا تدوس علي علامه الكره الارضيه دي وتعمل arp poisoning.

![[Pasted image 20250129194632.png]]
في حاله بقا ان الtargett حط معلومات حساسه هتتبدي تظهر في البرنامج

-------------------------------------------------------------------------------
الفكره بقا ان الattack ده بيحصل بس علي مواقع ال HTTP بس.

-------------------------------------------------------------------------------
المهم ونت فاتح الettercap ممكن تفتح wireshark هوا منطقي لازم تفتحه عشان تحلل البيانات البتتعبتلك وكدا وتشوف لو فيه معلومات مهمه تستفاد بيها.

-------------------------------------------------------------------------------
![[Pasted image 20250129195354.png]]
عشان نعمل الattack ده علي مواقع https كنا بنعمل downgrade للموقع من https ل http
عن طريق اداه اسمها sslstrip بس بتشتغل علي شهادات الssl القديمه وكدا بس دلوقتي كل المواقع شغاله بالشهاده الجديده ال TLS ,  ومفيش طريقه حاليا انك ت downgrade فا الattack ده مبقاش ليه فايده حاليا.

-------------------------------------------------------------------------------
![[Pasted image 20250129195800.png]]
طريقه تشغيله عشان لو احتجتها يعني.

![[Pasted image 20250129200230.png]]
وكان ممكن توجه الناس من عندك للموقع بتاعك وكدا.
بس الكلام ده كان زمان بح.

-------------------------------------------------------------------------------

