![[Pasted image 20250116002206.png]]
![[Pasted image 20250116002303.png]]
filtered 
انك متعرفش هوا مقفول ولا مفتوح 

![[Pasted image 20250116002435.png]]

-------------------------------------------------------------------


![[Pasted image 20250116002452.png]]

![[Pasted image 20250116002535.png]]
ده الdomain 
![[Pasted image 20250116002545.png]]
ده التوب لفل دومين

![[Pasted image 20250116002634.png]]

-------------------------------------------------------------------------------

![[Pasted image 20250116002655.png]]

![[Pasted image 20250116002710.png]]

-------------------------------------------------------------------------------

![[Pasted image 20250116002759.png]]
-------------------------------------------------------------------


![[Pasted image 20250116002852.png]]

-------------------------------------------------------------------------------
![[Pasted image 20250116002948.png]]

![[Pasted image 20250116004741.png]]

الفرق بين الudp والtcp 

UDP:-
اسرع و ميضمنلكش ان كل المعلومات هتوصل.
How is it fast?
Because it doesn't care if you get the message it just keep sending stuff and doesn't wait for verify like TCP.
since it doesn't verify so maybe some message will be lost. 

-------------------------------------------------------------------------------
 TCP:-
 Reliable how?
 it makes sure that your data is received, HOW?
 عن طريق حاجه اسمها Three-way hand shake.
 what is that ?
 for setting up connection before start exchanging data.
 1- sends synchronization message (sync message) to ur pc from the website u want to access.
 2-ur pc responds with Synchronization Acknowledgement message (Sync ACK message).
 3-then websites responds with ACK message.
 these steps have to happen so we make connection.

security is better in TCP than UDP.

-------------------------------------------------------------------------------

TCP isn't good for real time interactions.
عكس ال
UDP its better for real time interactions.

-------------------------------------------------------------------------------
What does websites use UDP or TCP?
Both!

-------------------------------------------------------------------------------
 
![[Pasted image 20250116005452.png]]

-------------------------------------------------------------------------------
![[Pasted image 20250116005603.png]]
![[Pasted image 20250116005629.png]]


-------------------------------------------------------------------------------
Ipv4
تم تسميتها v4 عشان بتتكون من 4 خانات 192.168.1.1 -> 255-0 => بيدينا حوالي 4 مليار و300 مليون IP


-------------------------------------------------------------------------------
ipv6
عملو ده عشان دلوقتي بقا في اجهزه كتير جداا وكل جهاز لازم يبقي في IP ليه خاص الpublic IP
فا دلوقتي بوجود الversion ده دلوقتي بيتوفر IPs كتيييير نقدر نوفرها للأجهزه
وده الشكل الاخير لل IP versions مش هيبقي فيه version 8 وكدا

1-255 => 0000-ffff

=> 2F01:90A8:0000:0000:9EFC:3101

لأن تكون الارقام مع الحروف كدا هيرمي معاك حوالي 700 تريليون IP فا مظنش هنحتاج كل ده 
 والشكل الفوق لو ملقتش اصفار في النص اعرف ان فيه اصفار بس شالوها وحاطوها كدا.

=>2F01:90A8::9EFC:3101


-------------------------------------------------------------------------------

CIDR:-
المفروض بيحدد عدد الIPS الفي الشبكه الواحده يعني الشبكه تقدر تاخد كام IP من كام لكام والشده وكدا 

CIDR 
بيسموه
Sub Net mask => 192.168.1.0/24
ازاي تعرف ان دي شبكه مش IP هتلاقي مدام اخر رقم 0 اعرف انها شبكه مش IP
وفيه CIDR calculators علي النت عشان تعرف تحسب فيه كام IP علي الشبكه 
في الحاله دي هيطلع 254 IP علي الشبكه 
الزيرو محجوز و ال 255 محجوز عشان كدا مش ضمنهم
0=> network , 255=>broadcast

-------------------------------------------------------------------------------

Switches
blah blah blah
for more information come inbox <3

-------------------------------------------------------------------------------
Routers 
مسئوله انه توزع IPS للأجهزه المتوصله بيها 
وفي الشركات لو قدرت تخترق الrouter فا ساعتها كدا يعتبر هكرت الشركه كلها وتقدر توصل لكل المعلومات
والIp بتاع الrouter في الغالب بيبقي => 192.168.1.1 
فا ممكن تعمل عليه attacks زي DHCP Starving وزي Man in the middle attack.

دلوقتي مثلا احنا في الشركه فا الجهاز بيفتح الrouter بيديله IP محفوظ عنده في DHCP pool بنظام
DHCP SERVER 
بيبقي موجود في الrouter هوا البيوزع الIPS من 0-255 او علي حسب الشركه يعني 
وال DHCP بيبقي توزيع الIPS فيه عشوائي بالكامل.

-------------------------------------------------------------------------------
Fire Wall 
الشبكه عشان فيه حاجه تحميها يبقي لازم يتحطلها fire wall 
الfire wall بيبقي عباره عن شويه protocols شويه خورزميات معموله software محطوط علي جهاز 
اول لما حد بيبتدي يهجم علي الشركه هوا بيوقفه 
بيوقفه عن طريق حاجات انا وفرتها للfire wall اكنه bodyguard 
بديله مواصفات معينه لو لاقاها مثلا فا ساعتها يوقف الهجوم بناءا علي المواصفات دي الانا اديتهاله

-------------------------------------------------------------------------------
Access Point
هوا جهاز ال router العندنا في البيت 
البيوزع النت يعني 
lvl 1 Main router
lvl 2 Switches 
lvl 3 the device that connected to the switch (access point)

-------------------------------------------------------------------------------
Active Directory 
هو الcontroller الخاص بالشبكه
هوا البيحدد الصالحيات لكل جهاز انه يaccess علي انهي فايلات لو عندك شركه فا اكيد في ملفات ليها علاقه بالماليات والhr والموظفين وهكذا فا اكيد مش اي حد هيدخل علي اي حاجه فا لازم تحدد صالحيات

مثلا بتوع ال IT بينزلو نسخه تانيه من windows اسمها windows server وبيثبتو عليها active directory عشان يظبطو الصالحيات وهكذا.

-------------------------------------------------------------------------------
Load Balancer
![[Pasted image 20250116013951.png]]
![[Pasted image 20250116014032.png]]
دلوقتي لو الload balancer مش موجود وكان علطول الclient متوصل بالسيرفر ساعتها منغيره ممكن ال client بدل ما يبعت طلب ويبعت الف طلب او اكتر عمتا  ساعتها السيرفر مش هيستحمل ويكراش
او ممكن مثلا السيرفر اخره 4 الاف client ودخله 6 الاف client ساعتها بردو هيكراش ويقع 
فا ساعتها بتيجي بقي فكره عمل الload balancer انه بيوزع ال clients علي السرفرات الموجوده بالتساوي عشان متعملش crash.
وحوار الطلبات الكتير وكدا اسمه DDOS ATTACK.

-------------------------------------------------------------------------------
![[Pasted image 20250116020046.png]]
 مكسل اكتب المهم الشهاده دي مجانيه وفايدتها انه بتشفر الداتا البتتنقل عن طريق الانترنت 

وهما الشهادتين دول القديمه SSL والجديده TLS وتقدر تتطلبها عادي online .

-------------------------------------------------------------------------------
![[Pasted image 20250127155744.png]]
Network sniffing means:
التجسس والتنصت يعني تقعد وسط الشبكه تعرف اي البيحصل وكدا.

Network interface  card (NIC):
ده المسئول بتوصيل النت في جهاز (كارته النت) البيدخل المعلومات لجهازك وكدا.
![[Pasted image 20250127155926.png]]
وده شكله. والكابل المتوصل ده اسمه ether net cable.
اما لو كان متوصل بالوافاي ده بنسميه ال W-LAN.
![[Pasted image 20250127160056.png]]
الكارت ده بيبقي فيه 2 modes .
First Mode:-
بيدخل الانترنت للجهاز من بره بالطريقه المعتاده الهوا الmanaged mode الهوا بياخد من الواي فاي بيدخل في الجهاز.
2nd Mode:
ده البنستخدمه في الاختراق ده بيخلي الكارت بتاعك من كارت عادي لكارت تصنت بيقعد في وسط الشبكه
يشوف البيانات الرايحه والجايه.
بنسمي البيانات الرايحه والجايه Packets,وكل packet بيبقي جواها frames بنتصت علي كدا دول بقا.
ومن الخصائص انك ممكن تعمل شبكه وهميه توهم بيها القدامك انها شبكه حقيقيه ولو دخل عليها ساعتها تقدر تخترقه.

![[Pasted image 20250127160743.png]]
عشان نعمل attack اسمه man in the middle attack. هنعرف اكتر عنه كمان حبه.

![[Pasted image 20250127160820.png]]
اداه مهمه هنستخدمها في شغلنا عشان نشوف الpackets الرايحه والجايه علي الشبكه.![[Pasted image 20250127160927.png]]

wlan0 
لو لقتها يعني في الwireshark اعرف انه ده الmangment mode.
mon
يعني monitor mode.
![[Pasted image 20250127161031.png]]

![[Pasted image 20250127161233.png]]
في البرنامج لو  حابب تشوف protocol معين بتكتب اسمه في الsearch وبيظهرلك وكدا تتقدر تتنسط علي الprotocol الانت عايزه.
![[Pasted image 20250127161434.png]]
في المواقع الhttp تقدر بسهوله تتجسس علي البيانات البتتبعت للسيرفر وتبتقي في خانه الpost زي ما موضح في الصوره وفي حاله تسجيل الضحيه في البرنامج تقدر تعرف الpassword والusernname كما ما هوا موضح كدا.

-------------------------------------------------------------------------------
ال Osi Model.

![[Pasted image 20250204105422.png]]

![[Pasted image 20250204105429.png]]

هنمشي بالترتيب ونعرف المفروض الداتا او طريقه عمل ال OSI Model.
واول حاجه:
 ال application layer بنبتدي من عندها وده يعتبر ال interface / portal للبرامج المحتاجه نت زي ال ويب ابليكشن او الويب براوزر و الاونلاين فيديو جيمز, فا ساعتها بقا الحاجات دي بتعمل engage لل app layer و تعتبر gateway للlayer البعديها.
تاني حاجه:
بناخد الداتا الجايه من ال app layer ونعديها علي ال layer البعديها الهيا ال presentation layer ونظبط الداتا دي ب format معروف لكل الاجهزه الموجوده علي الكوكب عشان تتعرض تبقي presentable بمعني دلوقتي لو الملف الترفع صوره فا ساعتها بنخليها JPG او مثلا الملف الاترفع بنخليه PDF , HTML دي الحاجات الpresentable المفروض ان كل الاجهزه متعارفه عليه او ال web عموما عشان كدا تقدر تفتح الصور عادي باستخدام اي browser او ال pdfs.
وطبعا في ال layer دي بردو بنعمل Encryption للداتا عشان نحمي الداتا البتتنقل ومنخليش الهكر يشوف الحاجات دي و طبعا بنأمن الtraffic عن طريق الشهادات الهيا SSL, TLS.
تالت حاجه:
نروح للsession layer و خلينا نقول ان هوا ال بيحافظ علي ال connection بين الابليكشن بتاعك و السيرفر (الbrowser مثلا) العايزين الداتا توصله , ولما خلاص الداتا توصل هوا بيفصل الconnection.
وعشان نعمل الconnections دي بنستخدم protocols معينه من اشهرها ال 
L2TP => Layer 2 tunnling protocol. ===> هتشوفه علي طول في ال vpn connections.
RTCP => remote transport control protocol. ===> بيساعد في تنظيم ال phone calls.
H.245 => بيساعد في تنظيم ال video calls.
وكمان ممكن نستخدم proxies وفي الغالب بسنتخدمها لو عايزين نخفي نفسنا واحنا علي النت.

كدا ال 3 layers الاحنا شرحناهم دول بيبقو تحت مسمي واحد في ال TCP Model الهوا ال Application layer.

رابع حاجه:
ندخل في ال transport layer.
الsession layer بيبعت الdata لل transport layer فا دلوقتي عايزين نودي الداتا للسيرفر التاني بيعملها ازاي ال transport layer ؟ 
عن طريق ال protocols والهما TCP,UDP
هما دول ال 2 main transport proctols, وشرحناهم فوق.
طيب دلوقتي عايزين ن access موقع معين فا عشان نوصله فا قولنا عن طريق ال protocols, فا نفترض دلوقتي كتبنا كدا https://youtube.com ده كدا اكني بقوله انا عايز access لل ip address (server ) ده مثلا الهوا موجود علي port 443 > https ودي فايده ال port numbers عشان كدا مينفعش ميبقاش فيه port numbers ودي طريقه كمان لشكل كتابه ال اللينك الفوق > 173.194.191.167:443 فا هنلاحظ ان البورت نمبر مكتوب في الاخر وده المفروض اليتكتب بس عشان الyoutube وكدا فا هما عاملين domain name يعني مغيرين شكل ال ip ده ومدينله اسم.
وفايده ال ports انها بتخلينا ان احنا نشغل كذا service علي سيرفر واحد. والسيرفر الواحد ده ممكن يبقي كذا حاجه RDP server, SSH server ,FTB server ,gaming server , etc.

ممكن نتكلم حبه عن الports 
Total number of ports from 0 to 65,535 => 65,536 ports in total.
Port Range:-
1- well-known (0-1023):-
Reserved  for common services and protocols. 
Examples:-
TFTP: Trivial File Transfer Protocol- port 69 > UDP.
SNTP: Simple Network time Protocol - port 123 > UDP.
DHCP: Dynamic Host Configuration protocol- port 67 (server) / port 68 (Client )- UDP.
HTTP: Hyper Text Transfer Protocol-port 80 > TCP.
SMTP: Simple Mail transfer protocol - port 24 > TCP.
FTP: File Transfer Protocol - port 20 (data )/port 21 (controlled) > TCP.
DNS: Domain name system - port 53 > UDP/TCP.

2-Registered port (1024- 49151):-
Assigned to specific services or Applications by organizations.
Examples:-
Port 3306:  MYSQL Database.
port 3389: Remote Desk Protocol(RDP).

3-Dynamic or private ports (49152-65353):-
Used for temporary or custom connections, often in client-server communications.
Examples:-
when your computer connects to website, it uses a random port from this range.

Quick Facts:-
1- Ports allow multiple services to run a single device.
2- tools like Nmap are used to scan ports during Pentesting.
3- Open ports can be vulnerable entry points if not secured properly.

بس دي البيحصل في ال transport layer وعمتا وبس مش هتحتاج تعرف اظن اكتر من كدا بس لو عايز تعرف 
هكمل
المفروض العمليه دي كلها بنعمل حاجه اسمها Encapsulation للداتا فا دلوقتي الداتا بعد ما حددنا ال port الهنستخدمه عشان نبعت الداتا فا بنغلفه مثلا بالIp address الهنبعتله ويبقي attached في الhead بتاع ال layer وبما أننا في layer 4 فا اسم الداتا المتغلفه دي (segment).
بعد كدا نروح نبعت لل layer 3  واحنا عارفين ان احنا بنتعامل في layer 3 بال IPs عشان الراوترز وكدا فا دلوقتي بردو الداتا الجاتلنا دي بناخدها بنعمل بردو Encapsulation فا نغلف ال داتا الجت دي بال source IP وال destination ip الهوا الip الهنبعتله الداتا ويبقي attached بردو للlayer 3 header و بكدا بعد عمليه التغفيل هيبقي اسمه الملف المتغلف ده (Packet) والPacket ده زي ما قولنا اكنه بيدي بقا ال router direction الهوا الdest. IP.
وبعد كدا نروح ل layer 2 الهوا ال Data link هنا بنتعامل مع ال MAC addresses وبندي ال Switch directions وبتبقي attached ل layer 2 header واسم الداتا المتغلفه في ال layer ده (Frames).
وبس بعد ما غلفنا الداتا وظبطناها بنروح للphysical layer وبتتبدي الداتا تروح للسيرفر التاني عن طريق ال ethernet cables, وبنبدأ بقا ال OSI Model من تحت فا بنعمل Dencaspulate للداتا وحده واحده لحد ما توصل كامله للسيرفر.

وهي دي طريقه عمل ال OSI Model.

-------------------------------------------------------------------------------
shodan.io for ips.


-------------------------------------------------------------------------------


![[Pasted image 20250502221739.png]]

-------------------------------------------------------------------------------
![[Pasted image 20250502222112.png]]

![[Pasted image 20250502233840.png]]
