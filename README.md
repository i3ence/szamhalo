#Számítógépes hálózatok definíciók kidolgozás 2015-16/1 félév

forrás:
+ peet91: számhálók definíció kidolgozás 2014 (elte.sharq.hu)
+ előadás diái (http://people.inf.elte.hu/acszolta/computer_networks)
+ wikipedia (https://en.wikipedia.org/wiki/Revocation_list, https://en.wikipedia.org/wiki/Congestion_window, https://en.wikipedia.org/wiki/IPv4_subnetting_reference, https://en.wikipedia.org/wiki/IPv6_address)

1. Hány réteget különböztet meg az Tannenbaum-féle hibrid rétegmodell?
	+ 5 félét.

2. Sorolja fel az ARPANET alapjául szolgáló három hálózatot.
	+ RAND, NPL, CYCLADES

3. Mi az “Open System Interconnection Reference Model”?
	+ Open System Interconnection Reference Model: Röviden OSI referencia modell, amely egy 7 rétegű standard, koncepcionális modellt definiál kommunikációs hálózatok belső funkcionalitásaihoz. (ISO/IEC 7498-1)

4. Mik a fõbb funkcionalitásai az ISO/OSI modell fizikai rétegének?
	+ Első a 7-ből. Bitek átvitele, definiálja az eszköz és a fizikai közeg kapcsolatát, protokollt határoz meg két fizikai kapcsolatban álló eszköz (node) közötti kapcsolat felépítéséhez.

5. Mik a fõbb funkcionalitásai az ISO/OSI modell megjelenítési rétegének rétegének?
	+ 6. réteg a 7-ből. Kontextus kezelése az alkalmazási rétegen futó folyamatok között, az kódolások egyeztetése/illesztése.

6. Mit jelent a hálózatok esetén az adatok burkolása?
	+ Hogy a továbbítandó adatra az egyes rétegeken történő áthaladás során különböző rétegspecifikus header-ök rakódnak, amelyek által az adat beburkolásra kerül a továbbítás során.

7. Mit jelent a „Black-box” megközelítés a kapcsolatokra?
	+ Azt jelenti, hogy az adott csomópont belső működésének ismerete nélkül, kizárólag annak be- és kimenetét ismerve tekintünk rájuk.

8. Mi az a PAN?
	+ Personal Area Network - személyi hálózat - nagyon alacsony kiterjedésű hálózat, amely létrejöhet perifériák és gép, valamint gép és gép között, a lényeg, hogy ~1m-es a processzorközi távolság

9. Mi az a WAN?
	+ Wide Area Network - nagykiterjedésű hálózat, amely nagyobb területet fed le, jellemzően városok, országok közötti kommunikációt valósít meg.

10. Mi az a MAN?
	+ Metropolitan Area Network - Városi hálózat (LAN < MAN < WAN).

11. Definiálja a hálózati sávszélességet?
	+ Az adat átviteléhez elérhető vagy felhasznált kommunikációs erőforrás mérésére szolgáló mennyiség, amelyet bit per másodpercben szoktak kifejezni.

12. Definiálja a jel sávszélességet?
	+ Jel feldolgozás esetén az egymást követő frekvenciák legnagyobb és legkisebb eleme közötti különbséget nevezik jel sávszélességnek. Tipikusan Hertz-ben mérik.

13. Definiálja a átviteli késleltetést?
	+ Az az időtartam, amely egy csomag összes bitjének az átviteli csatornára tételéhez szükséges.
	Jelölése: d_T.

14. Definiálja a propagációs késést?
	+ Az az időtartam, amely a jelnek szükséges ahhoz, hogy a küldőtől megérkezzen a címzetthez.
	Jelölése: d_prop vagy d.

15. Mi a hálózati hoszt?
	+ Olyan eszköz, amely egy számítógépes hálózattal áll összeköttetésben. Egy hoszt információkat oszthat meg, szolgáltatást és alkalmazásokat biztosíthat a hálózat további csomópontjainak.

16. Mi az átviteli csatorna?
	+ Az a közeg, amelyen a kommunikáció folyik a résztvevő hosztok között. Ez a közeg lehet egy koaxális kábel, a levegő, optikai kábel, stb.

17. Mik azok a TLDs-ek?
	+ Top Level Domains
	klasszikusok: .com, .edu, .gov, .mil, .org, .net
	később keletkeztek: .aero, .museum, .xxx
	~250 TLDs a különböző ország kódoknak
	  + Két betű (mint például .au, .hu), 2010-től plusz nemzetközi karakterek (például kínai)
	  + Több elüzletisedett, például a .tv (Tuvalu)
	  + Példa domén hack-ekre: instagr.am (Örményország), goo.gl (Grönland)

18. A névfeloldásnál mit neveznek iteratív lekérdezésnek?
	+ Ha a névszerver adja vissza a választ vagy legalább azt, hogy kitől kapható meg a következő válasz.

	+ Válasz után nem kell semmit tenni a kéréssel a névszervernek.
	+ Könnyű magas terhelésű szervert építeni.

19. A névfeloldásnál mit neveznek rekurzív lekérdezésnek?
	+ Ha a névszerver végzi el a névfeloldást, és  tér vissza a válasszal.

	+ Lehetővé teszi a szervernek a kliens terhelés kihelyezését a kezelhetőségért.
	+ Lehetővé teszi a szervernek, hogy a kliensek egy csoportja felett végezzen cachelést, a jobb teljesítményért.
	+ (18-19 az ea alapján van, de szerintem nem ok)

20. Mit nevezünk munkamenetnek az ISO/OSI referencia modellben?
	+ Egy munkamenet (Session) a egymással összefüggő hálózati interakciók sorozata egy alkalmazási feladat elvégzése során.
	+ Példák: Egy weblap több erőforrást is behozhat. Egy Skype hívás szintén érinthet képet, hangot, chat-et.

21. Mit nevezünk DNS átverésnek?
	+ Egy támadó a névszerver cache-ébe a hamis hozzárendelést juttat be a DNS protokoll használatán keresztül.

22. Mit nevezünk statikus weboldalnak?
	+ Tartalma nem változik csak manuális átszerkesztéssel.

23. Mit nevezünk dinamikus weboldalnak?
	+ Valamilyen kód végrehajtásaként keletkezik, mint például: javascript, PHP, vagy mindkettő egyszerre.

24. Mi az a PLT? Mire használják?
	+ Page Load Time, azon időtartam, ami a kattintás, és az oldal betöltése között eltelik.
	+ Több tényezőtől is függhet: oldal/tartalom struktúrájától, a HTTP (és TCP) protokolltól, a hálózati RTT-től és a sávszélességtől.

25. Mik azok a DNS erõforrás rekordok? Mit tárolnak?
	+  DNS erőforrás rekordokba tárolják a zónára vonatkozó információkat.
	+ SOA: Hatáskör kezdete, zóna kulcsparamétereivel rendelkezik.
	+ A: Egy hoszt IPv4-es címe.
	+ AAAA: Egy hoszt IPv6-es címe.
	+ CNAME: Egy alias kanonikus neve.
	+ MX: A levelező kiszolgáló a doménre nézve.
	+ NS: A domén névszervere vagy delegált aldomén.

26. Mi a Trust Anchor? Mire használják?
	+ TODO

27. Mi az Certificate Revocation List? Hol használják?
	+ Webes biztonságnál alkalmazzák, publikus kulcsok visszavonására. A CRL visszavont tanúsítványok, sorozatszámok listája.

28. Mi a Content Delivery Network? Mire nyújt megoldást?
	+ A népszerű tartalmak a kliensekhez közel helyezése.
	+ Terhelés elosztása, torlódások elkerülése, felhasználói élmény javítása.

29. Mik a p2p hálózatok legfontosabb jellemzõi?
	+ Nincs szerver.
	+ A kommunikáció peer-ek között folyik és önszerveződő.
	+ Skálázási problémák merülnek fel.

30. Mi a szerepe egy peer-nek egy p2p hálózatban?
	+ Feltöltés a többiek segítésére.
	+ Letöltés saját magának.

31. Mit nevezünk choke peer-nek?
	+ Olyan peer, aki korlátozza a letöltést más peer-ek részére.

32. Mi az a seed peer?
	+ Olyan speciális peer, aki rendelkezik a letöltendő fájl összes darabjával.

33. Mire szolgál az állapot nélküli tûzfal?
	+ Statikus szűrő szabályokat valósít meg.
	+ Engedélyezhető/tiltható vele sokféle szolgáltatás és hálózati cél is.
	+ Általában UDP/TCP portokat használ. (például  a 23-as TCP port tiltása a telnet letiltására)

34. Mire szolgál az állapot alapú tûzfal?
	+ Állapot alapú csomagszűrést valósít meg, amely a csomagváltást nyomon követi.
	+ NAT példa: „A TCP csomagok fogadása egy belső hoszt csatlakozása után.”

35. Mire szolgál az alkalmazás réteg tûzfal?
	+ Alkalmazásokra és tartalmakra alapuló szabályokat valósít meg. (például víruskeresés a csomagokban)
	+ Az csomagok vizsgálata magasabb rétegek emulálásával, például az alkalmazás üzenetek újra összegyűjtésével.

36. Mi az a DeMilitarized Zone? Mire szolgál?
	+ A tűzfal és az internet közötti réteg.
	+ Web szerverek, email szerverek, chat szerverek elhelyezése.
	+ A fertőzések tovább terjedésének meggátolására.

37. Mire szolgál a TCP protokoll? Mik a fõbb jellemzõi?
	+ megbízható adatfolyam létrehozása két végpont között;
	+ az alkalmazási réteg adatáramát osztja csomagokra;
	+ a másik végpont a csomagok fogadásról nyugtát küld;

38. Mire szolgál az UDP protokoll? Mik a fõbb jellemzõi?
	+  egyszerű nem megbízható szolgáltatás csomagok küldésére;
	+ az alkalmazási réteg határozza meg a csomag méretét;
	+ az inputot egy datagrammá alakítja;

39. Mit neveznek adási ablaknak?
	+ TODO

40. Mit neveznek vételi ablaknak?
	+ TODO

41. Mi a CRC? Mire használható?
	+ Hálózatok, tárolóegységek körében használt hibajelző kód.
	+ A küldő az adatokhoz polinomosztással ( x^rM(x)/G(x) ) ellenőrzőértéket rendel. Fogadáskor a vevő elvégzi az osztást ( (T(x)+E(x))/G(x) ) a generátorpolinommal. Ha nem 0 eredményt kap, hiba történt.

42. Hogyan történik egy TCP kapcsolat felépítése? Mik a lépései?
	+  Rendszerint kliens szerver kapcsolat van.
	+ Ez esetben a felépítés 3 TCP csomaggal történik.
	+ Az MSS is átvitelre kerül az első SYN-szegmensben.
	+ ![TCP kapcsolat felepitese](/images/42tcp.png)

43. Mit jelent az RTO, és hol használják?
	+ Retransmission Timeout, szabályozza az időközt a küldés és egy duplikátum újraküldése között, ha egy nyugta kimarad.
	+ TCP esetén használják.

44. Mi a TCP Nagle algoritmus mûködési alapelve?
	+ Kis csomagok nem kerülnek addig küldésre, amíg nyugták hiányoznak.
	  + egy csomag kicsi, ha az adathossz < MSS
	+ Ha a korábban küldött csomag nyugtája megérkezik, küldi a következőt

45. Mi az a "slow start" TCP esetén?
	+ exponenciális növekedés (hisztórikus elnevezés: korábban még aggresszívebb sémák)

46. Mi az a torlódási ablak? Mire szolgál?
	+ TCP esetén megszabja az átmenő adatok méretét a küldő irányából.
	+ Célja, hogy elkerüljük a fogadó túlterhelését

47. Mi az gyors újraadás TCP Tahoe esetén?
	+ Fasy Retransmit (diáknál Reno alatt a def)
	+ ha ugyanazon csomaghoz 3 nyugta-duplikátum, azaz 4 azonos nyugta, érkezik (angolul triple duplicate ACK),
	+ újraküldi az elveszett csomagot, egyidejűleg slow start fázisba lép

48. Mit jelenthet az ha három azonos nyugta érkezik egymás után?
	+ Fasy Retransmit (diáknál Reno alatt a def)
	+ ha ugyanazon csomaghoz 3 nyugta-duplikátum, azaz 4 azonos nyugta, érkezik (angolul triple duplicate ACK),
	+ újraküldi az elveszett csomagot, egyidejűleg slow start fázisba lép

49. Mi az AIMD torlódás kerülési stratégia lényege?  
	+ Additive Increase Multiplicative Decrease

50. Mit nevezünk torlódásnak TCP esetén?
	+ Ha a terhelés túl nagy, túlcsordulnak a pufferek, csomagok vesznek el, újra kell küldeni, drasztikusan nő a válaszidő. Ezt a torlódásnak nevezzük.

51. Mikor nevezünk egy torlódás kerülési algoritmust hatékonynak?
	+ Egy jó torlódáselkerülési (angolul congestion avoidance) stratégia a hálózat terhelését a könyök közelében tartja...

52. Mikor nevezünk egy torlódás kerülési algoritmust fairnek?
	+ ...Emellett fontos, hogy minden résztvevőt egyforma rátával szolgáljunk ki.

53. Mi a forgalomirányító algoritmusok definiciója?
	+ A hálózati réteg szoftverének azon része, amely azért a döntésért felelős, hogy a bejövő csomag melyik kimeneti vonalon kerüljön továbbításra.
	+ A folyamat két jól-elkülöníthető lépésre bontható fel:
	  + Forgalomirányító táblázatok feltöltése és karbantartása.
		+ Továbbítás.

54. Mi a statikus forgalomirányító algoritmusok fõ jellemzõje?
	+ Offline meghatározás, betöltés a router-ekbe induláskor.

55. Mi az adaptív forgalomirányító algoritmusok fõ jellemzõje?
	+ A topológia és rendszerint a forgalom is befolyásolhatja a döntést.

56. Mi a hierarchikus forgalomirányítás lényege?
	+ A router-eket tartományokra osztjuk. A saját tartományát az összes router ismeri, de a többi belső szerkezetéről nincs tudomása.
	+ Nagy hálózatok esetén többszintű hierarchia lehet szükséges. Például: tartományok kerületekbe osztása, a kerületeket zónákba osztjuk, a zónákat osztályokba szervezzük, etc.

57. Mit nevezünk adatszórásnak vagy broadcasting-nak?   
	+ Egy csomag mindenhová történő egyidejű küldése.

58. Mit nevezünk többesküldésnek vagy multicasting-nak?
	+ Egy csomag meghatározott csoporthoz történő egyidejű küldése.

59. Mi a többcélú forgalomirányítás lényege?
	+ Csomagban van egy lista a rendeltetési helyekről, amely alapján a router-ek eldöntik a vonalak használatát, mindegyik vonalhoz készít egy másolatot és belerakja a megfelelő célcím listát. (multidestination routing)

60. Mire szolgál a DF bit az IPv4 fejlécében?
	+ „ne darabold” flag a router-eknek (Don't Fragment)
61. Mire szolgál a MF bit az IPv4 fejlécében?
	+ „több darab” flag minden darabban be kell legyen állítva, kivéve az utolsót. (More Fragments)

62. Mire szolgál a szolgálat típusa mezõ az IPv4 fejlécében?
	+ szolgálati osztályt jelöl (3-bites precedencia, 3 jelzőbit [D,T,R])

63. Mire szolgál az élettartam (TTL) mezõ az IPv4 fejlécében?
	+ Másodpercenként kellene csökkenteni a mező értékét, minden ugrásnál csökkentik eggyel az értékét.

64. Mi az IPv4 cím és hogyan ábrázoljuk?
	+  Minden hoszt és minden router az Interneten rendelkezik egy IP-címmel, amely a hálózat számát és a hoszt számát kódolja. (egyedi kombináció)
	+ 4 bájton ábrázolják az IP-címet.

65. Mi az IPv6 cím és hogyan ábrázoljuk?
	+ IP protokoll új verziója, nagyobb címtartomány, közvetlen végponti címezhetőséggel
	+ Ábrázolás: 128 biten, pl. 2001:0db8:85a3:0000:0000:8a2e:0370:7334 (nullák elhagyhatók)

66. Milyen speciális IPv4 címek vannak?
	+ x.x.x.0: hálózat azonosító
	+ x.x.x.255: hálózat broadcast címe

67. Mi az alhálózati maszk és mire szolgál?
	+ Bitmaszk, amivel feloszthatjuk az IP azonosítót a hálózat és a hoszt azonosítójára.

68. Mire szolgál az ICMP protokoll?
	+ Internet Control Message Protocol
	+ Feladata:  Váratlan események jelentése.

69. Mire szolgál az ARP protokoll?
	+ Address Resolution Protocol
	+ Feladata:  Az IP cím megfeleltetése egy fizikai címnek.

70. Mi az RARP? Mire használják?
	+ Reverse Address Resolution Protocol
	+ Feladata: A fizikai cím megfeleltetése egy IP címnek.

71. Mi az BOOTP? Mire használják?
	+ Bootstrap Protocol
	+ Feladata: Egy kliens használhatja, hogy címet kapjon a konfigurációs szervertől.

72. Mi az DHCP? Mire használják?
	+ Dynamic Host Configuration Protocol
	+ Feladata: Automatikus címkiosztás a hosztoknak.

73. Mi az a gerinchálózat? Hol használják és mire?
	+ Backbone Network
	+ Hálózati infrastruktúra része, különféle hálózatokat köt össze, ezzel biztosíva at információáramlást a hálózatok közt.

74. Mely 3 féle összeköttetést és hálózatot támogatja az OSPF?
	+ Kétpontos vonalak két router között.
	+ Többszörös hozzáférésű hálózatok adatszórási lehetőséggel.
	+ Többszörös hozzáférésű hálózatok adatszórási lehetőség nélkül.

75. Milyen úttípusok léteznek az OSPF logikája szerint?
	+ területen belüli
	+ területek közötti
	+ AS-ek közötti

76. Mit nevez a BGP csonka hálózatnak?
	 + Amelyeknek csak egyetlen összeköttetésük van a BGP gráffal.

77. Mit nevez a BGP többszörösen bekötött hálózatnak?
	+ Amelyeket használhatna az átmenő forgalom, de ezek ezt megtagadják.

78. Mit nevez a BGP tranzit hálózatnak?
	+  Amelyek némi megkötéssel, illetve általában fizetség ellenében, készek kezelni harmadik fél csomagjait.

79. Soroljon fel 4 vezetékes átviteli közeget. (8!)
	+ Mágneses adathordozók
	+ Sodort érpár
	+ Koaxális kábel
	+ Fényvezető szálak

80. Mit nevezünk frekvenciának? Mi a mértékegysége és hogyan jelölik?
	+ Elektromágneses hullám másodpercenkénti rezgésszáma.
	+ Jelölés: f
	+ Mértékegység: Hertz (Hz)

81. Soroljon fel 3 elektromágneses tartományt.
	+ Rádióhullám
	+ Mikrohullám
	+ Infavörös sugarak
	+ Röntgensugarak

82. Soroljon fel 4 vezeték nélküli átviteli közeget. (13!)
	+ Rádiófrekvenciás átvitel
	+ Mikrohullámú átvitel
	+ Infravörös és milliméteres hullámú átvitel
	+ Látható fényhullámú átvitel

83. Mi a szimbólumráta és az adatráta? Mi a mértékegységük?
	+ Baud – Szimbólumok száma másodpercenként
	+ Adatráta – Bitek száma másodpercenként

84. Soroljon fel 3 óraszinkronizációs módszert.
	+ Explicit órajel
	+ Kritikus időpontok
	+ Szimbólum kódok

85. Mi az önütemezõ jel? Mire használható?
	+ Külön órajel szinkronizáció nélkül dekódolható jel.
	+ Szinkronizációnál szimbólumkód esetén használható.

86. Mi a digitális kódok leírásának 3 fõ jellemzõje?
	+ Mi történik egy szignál intervallum
		+ elején?
		+ közepén?
		+ végén?

87. Mi az alapsáv?
	+ Baseband
	+ A digitális jel direkt árammá vagy feszültséggé alakulm a jel minden frekvencián átvitelre kerül.
	+ Átviteli korlátok

88. Mi a szélessáv?
	+ Broadband
	+ Széles frekvencia tartományban történik az átvitel.

89. Mi az amplitúdó moduláció?
	+ Az s(t) szignált a szinusz görbe amplitúdójaként kódoljuk.

90. Mi a frekvencia moduláció?
	+ Az s(t) szignált a szinusz görbe frekvenciájában kódoljuk.

91. Mi a fázis moduláció?
	+  Az s(t) szignált a szinusz görbe fázisában kódoljuk.

92. Mit nevezünk BER-nek? Mire használják?
	+ Bit Error Rate - Bithiba gyakoriság
	+ A hibásan fogadott bitek részaránya.

93. Milyen tényezõktõl függ a BER?
	+ a jel erőségétől,
	+ a zajtól,
	+ az átviteli sebességtől,
	+ a felhasznált módszertől.

94. Mi a CDMA?
	+ Code Division Multiple Access
	+ A harmadik generációs mobiltelefon hálózatok alapját képezi (IS-95 szabvány)
	+ Minden állomás egyfolytában sugározhat a rendelkezésre álló teljes frekvenciasávon
	+ Feltételezi, hogy a többszörös jelek lineárisan összeadódnak.
	+ Kulcsa: a hasznos jel kiszűrése

95. Mi az a Walsh mátrix? Mire használható?
	+ CDMA szinkron esetben a Walsh mátrix oszlopai vagy sorai egyszerű módon meghatároznak egy kölcsönösen ortogonális töredék sorozat halmazt.
	+ ![Walsh-matrix](/95www Walshy com.png)

96. Az adatkapcsolati réteg milyen jól definiált interfészeket biztosít a hálózati réteg felé?
	+ nyugtázatlan összeköttetés alapú szolgálat
	+ nyugtázott összeköttetés nélküli szolgálat
	+ nyugtázott összeköttetés alapú szolgálat (3 fázis)

97. Milyen módszereket ismer a keretezésre az adatkapcsolati rétegben?
	+ karakterszámlálás
	+ kezdő és végkarakterek karakterbeszúrással
	+ kezdő és végjelek bitbeszúrása
	+ fizikai rétegbeli kódolás-sértés

98. Hogyan mûködik a karakterszámlálás?
	+ A keretben lévő karakterek számának megadása a keret fejlécében lévő mezőben
	+ A vevő adatkapcsolati rétege tudni fogja a keret végét
	+ Probléma: nagyon érzékeny a hibára a módszer

99. Hogyan mûködik a karakterbeszúrás?
	+ Különleges bájtok a keret elejének és végének jelzésére
	+ Korábban két speciális bájtot használtak, manapság megegyeznek, aminek neve jelző bájt (angolul flag byte)
	+ Adatfolyamban szereplő speciális bájtokhoz ESC bájt használata (bájt beszúrás)

100. Hogyan mûködik a bitbeszúrás?
	+ Minden keret egy speciális bitmintával kezdődik (flag bájt, 01111110)
	+ Minden egymást követő 5 hosszú folytonos 1-es bit sorozat után beszúr egy 0-át

Mi az egyszerû bithiba definiciója?
Definiálja a csoportos bithibát!
Definiálja egy tetszõleges S kódkönyv Hamming távolságát?
Mi az a Hamming korlát?
Milyen összefüggés ismeretes egy tetszõleges kódkönyv a Hamming távolsága és hibafelismerõ képessége között?
Milyen összefüggés ismeretes egy tetszõleges kódkönyv a Hamming távolsága és hibajavitási képessége között?
Mi a kódráta és a kód távolság? Milyen a rátája és távolsága egy jó kódkönyvnek?
CRC esetén mit lehet mondani hibajelzõ képességérõl, ha a generátor polinom x+1 többszöröse?
Mutassa be röviden a korlátozás nélküli szimplex protokollt!
Mutassa be röviden a szimplex megáll-és-vár protokollt!
Mutassa be röviden a csúszóablak protokollt!
Mi az N-visszalépéses stratégia lényege?
Mi a szelektív ismétléses stratégia lényege?
Hogyan épül fel egy HDLC keret?
Milyen keret típusokat használnak a HDLC-ben?
A felügyelõ kereteknek milyen altípusai vannak?
A csatorna kiosztásra mik a legelterjedtebb módszerek?
Röviden mutassa be a frekvenciaosztásos nyalábolás módszerét.
Röviden mutassa be az idõosztásos nyalábolás módszerét.
A csatorna modellben mit nevezünk ütközésnek?
Hogyan mûködik az egyszerû ALOHA protokoll?
Hogyan mûködik a réselt ALOHA protokoll?
Hogyan mûködik az 1-perzisztens CSMA protokoll?
Hogyan mûködik az nem-perzisztens CSMA protokoll?
Hogyan mûködik az p-perzisztens CSMA protokoll?
Hogyan mûködik az alapvetõ bittérkép eljárás?
Hogyan mûködik a bináris visszaszámlálás protokoll?
Milyen kábelezési topológiákat támogat az Ethernet szabvány?
Miért van szükség a maximális keretméretre?
Miért van szükség a minimális keretméretre?
Mutassa be a minimális keretméretre vonatkozó általános képletet.
Mik a kettes exponenciális visszalépés algoritmus lépései?
Mutassa be a rejtett állomás problémáját.
Mutassa be a megvilágított állomás problémáját.
Mik a MACA protokoll leglényegesebb lépései?
Mit nevezünk ad hoc hálózatnak.
Mi a Network Allocation Vector?
Mit neveznek Short Inter Frame Spacing-nek?
Mit neveznek DCF Inter Frame Spacing-nek?
Mit neveznek PCF Inter Frame Spacing-nek?
Mit neveznek Extended Inter Frame Spacing-nek?
Mi a bridge, és mire használják?
Mi a repeater, és mire használják?
