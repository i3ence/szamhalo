#Számítógépes hálózatok definíciók kidolgozás 2015-16/1 félév

forrás:
+ peet91: számhálók definíció kidolgozás 2014 (elte.sharq.hu)
+ előadás diái (http://people.inf.elte.hu/acszolta/computer_networks)
+ wikipedia (https://en.wikipedia.org/wiki/Revocation_list, https://en.wikipedia.org/wiki/Congestion_window, https://en.wikipedia.org/wiki/IPv4_subnetting_reference, https://en.wikipedia.org/wiki/IPv6_address, etc.)

1. Hány réteget különböztet meg a Tannenbaum-féle hibrid rétegmodell?
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
	+ Metropolitan Area Network - Városi hálózat (PAN < LAN < MAN < WAN).

11. Definiálja a hálózati sávszélességet?
	+ Az adat átviteléhez elérhető vagy felhasznált kommunikációs erőforrás mérésére szolgáló mennyiség, amelyet bit per másodpercben szoktak kifejezni.

12. Definiálja a jel sávszélességet?
	+ Jel feldolgozás esetén az egymást követő frekvenciák legnagyobb és legkisebb eleme közötti különbséget nevezik jel sávszélességnek. Tipikusan Hertz-ben mérik.

13. Definiálja az átviteli késleltetést?
	+ Az az időtartam, amely egy csomag összes bitjének az átviteli csatornára tételéhez szükséges.
	Jelölése: d_T (alsóindex).

14. Definiálja a propagációs késést?
	+ Az az időtartam, amely a jelnek szükséges ahhoz, hogy a küldőtől megérkezzen a címzetthez.
	Jelölése: d_prop vagy d.

15. Mi a hálózati hoszt?
	+ Olyan eszköz, amely egy számítógépes hálózattal áll összeköttetésben. Egy hoszt információkat oszthat meg, szolgáltatást és alkalmazásokat biztosíthat a hálózat további csomópontjainak.

16. Mi az átviteli csatorna?
	+ Az a közeg, amelyen a kommunikáció folyik a résztvevő hosztok között. Ez a közeg lehet egy koaxális kábel, a levegő, optikai kábel, stb.

17. Mik azok a TLDs-ek?
	+ Top Level Domains
	+ klasszikusok: .com, .edu, .gov, .mil, .org, .net
	+ később keletkeztek: .aero, .museum, .xxx
	+ ~250 TLDs a különböző ország kódoknak
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
	+ A küldő az adatokhoz polinomosztással ( (x^r M(x)) / G(x) ) ellenőrzőértéket rendel. Fogadáskor a vevő elvégzi az osztást ( (T(x)+E(x))/G(x) ) a generátorpolinommal. Ha nem 0 eredményt kap, hiba történt.

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
	+ Fast Retransmit (diáknál Reno alatti ez a def)
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
	+ ![Walsh-matrix](/images/95www Walshy com.png)

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

101. Mi az egyszerû bithiba definiciója?
	+ az adategység 1 bitje nulláról egyre avagy egyről nullára változik.
	+ ![egyszeru bithiba](/images/101ebhiba.png)

102. Definiálja a csoportos bithibát!
	+  Burst Error – Az átviteli csatornán fogadott bitek egy olyan folytonos sorozata, amelynek az első és utolsó szimbóluma hibás, és nem létezik ezen két szimbólummal határolt részsorozatban olyan m hosszú részsorozat, amelyet helyesen fogadtunk volna a hiba burst-ön belül.
	+ ![burst hiba](/images/102bhiba.png)

103. Definiálja egy tetszõleges S kódkönyv Hamming távolságát?
	+ Legyen S egyenlő hosszú bitszavak halmaza, ekkor S Hamming távolsága az alábbi:
	+ ![hamming tavolsag](/images/103hamming.png)
	+ Jelölés: d(S).

104. Mi az a Hamming korlát?
	+ ![hamming korlat](/images/104hammingkorlat.png)

105. Milyen összefüggés ismeretes egy tetszõleges kódkönyv a Hamming távolsága és hibafelismerõ képessége között?
	+ Azaz d bit hiba felismeréséhez a megengedett keretek halmazában legalább d+1 Hamming távolság szükséges.

106. Milyen összefüggés ismeretes egy tetszõleges kódkönyv a Hamming távolsága és hibajavitási képessége között?
	+ d bit hiba javításához a megengedett keretek halmazában legalább 2d+1 Hamming távolság szükséges

107. Mi a kódráta és a kód távolság? Milyen a rátája és távolsága egy jó kódkönyvnek?
	+ ![kod rata](/images/107rata.png)
	+ ![kod tavolsag](/images/107tavolsag.png)
	+ A jó kódoknak a rátája és a távolsága is nagy.

108. CRC esetén mit lehet mondani hibajelzõ képességérõl, ha a generátor polinom x+1 többszöröse?
	+Ha G(x) az x+1 többszöröse, akkor minden páratlan számú hiba felismerhető.

109. Mutassa be röviden a korlátozás nélküli szimplex protokollt!
	+ Környezet:
	  + Mind az adó, mind a vevő hálózati rétegei mindig készen állnak
	  + A feldolgozási időktől eltekintünk
	  + Végtelen puffer-területet feltételezünk
	  + Az adatkapcsolati rétegek közötti kommunikációs csatorna sosem rontja vagy veszíti el a kereteket

	+ Protokoll:
	  + Résztvevők: küldő és vevő
	  + Nincs sem sorszámozás, sem nyugta
	  + Küldő végtelen ciklusban küldi kifele a kereteket folyamatosan
	  + A vevő kezdetben várakozik az első keret megérkezésére, keret érkezésekor a hardver puffer tartalmát változóba teszi és az adatrészt továbbküldi a hálózati rétegnek.

110. Mutassa be röviden a szimplex megáll-és-vár protokollt!
	+ Környezet:
		+ mind az adó, mind a vevő hálózati rétegei mindig készen állnak
		+ A vevőnek ∆t időre van szüksége a bejövő keret feldolgozására (nincs pufferelés és sorban állás sem)
		+ Az adatkapcsolati rétegek közötti kommunikációs csatorna sosem rontja vagy veszíti el a kereteket

	+ Protokoll:
		+ résztvevők: küldő és vevő
		+ küldő egyesével küldi kereteket és addig nem küld újat, még nem kap nyugtát a vevőtől
		+ a vevő kezdetben várakozik az első keret megérkezésére, keret érkezésekor a hardver puffer tartalmát változóba teszi és az adatrészt továbbküldi a hálózati rétegnek, végül nyugtázza a keretet.

111. Mutassa be röviden a csúszóablak protokollt!
	+  Egy adott időpontban egyszerre több keret is átviteli állapotban lehet.
	+ A fogadó n keretnek megfelelő méretű puffert allokál.
	+ A küldőnek legfeljebb n, azaz ablak méretnyi, nyugtázatlan keretet küldése engedélyezett.
	+ A keret sorozatbeli pozíciója adja a keret címkéjét. (sorozatszám)

	+  A küldő nyilvántartja a küldhető sorozatszámok halmazát. (adási ablak)
	+ A fogadó nyilvántartja a fogadható sorozatszámok halmazát. (vételi ablak)
	+ A sorozatszámok halmaza minden esetben véges.
	+ K bites mező esetén: [0..2^K −1 ].
	+ A adási ablak minden küldéssel szűkül, illetve nő egy nyugta érkezésével.

112. Mi az N-visszalépéses stratégia lényege?
	+ Az összes hibás keret utáni keretet eldobja és nyugtát sem küld róluk.
	+ Mikor az adónak lejár az időzítője, akkor újraküldi az összes nyugtázatlan keretet, kezdve a sérült vagy elveszett kerettel.

113. Mi a szelektív ismétléses stratégia lényege?
	 + A hibás kereteket eldobja, de a jó kereteket a hibás után puffereli.
	 + Mikor az adónak lejár az időzítője, akkor a legrégebbi nyugtázatlan keretet küldi el újra.

114. Hogyan épül fel egy HDLC keret?
	+  cím mező
	 	+ több vonallal rendelkező terminálok esetén van jelentősége,
		+ pont-pont kapcsolatnál parancsok és válaszok megkülönböztetésére használják
	+ vezérlés mező
		+ sorszámozás, nyugtázás és egyéb feladatok ellátására
	+ adat mező
		+ tetszőleges hosszú adat lehet
	+ ellenőrző összeg mező
		+ CRC kontrollösszeg a CRC-CCITT generátor polinom felhasználásával
	+ FLAG bájt a keret határok jelzésére

115. Milyen keret típusokat használnak a HDLC-ben?
	+ Információs
	+ Felügyelő
	+ Számozatlan

116. A felügyelõ kereteknek milyen altípusai vannak?
	+ 0. típus – nyugtakeret (RECEIVE READY);
	+ 1. típus – negatív nyugtakeret (REJECT);
	+ 2. típus – VÉTELRE NEM KÉSZ, amely nyugtáz minden keretet a Következőig ((RECEIVE NOT READY))
	+ 3. típus – SZELEKTÍV ELUTASÍTÁS, amely egy adott keret újraküldésére szólít fel (SELECTIVE REJECT)

117. A csatorna kiosztásra mik a legelterjedtebb módszerek?
 	+ statikus módon (FDM, TDM)
	+ dinamikus módon
		+ verseny vagy ütközés alapú protokollok (ALOHA, CSMA, CSMA/CD)
		+ verseny-mentes protokollok (bittérkép-alapú protokollok, bináris visszaszámlálás)
		+ korlátozott verseny protokollok (adaptív fa protokollok)

118. Röviden mutassa be a frekvenciaosztásos nyalábolás módszerét.
	+ N darab felhasználót feltételezünk, a sávszélet N egyenlő méretű sávra osztják, és minden egyes sávhoz hozzárendelnek egy felhasználót.
	+ Következésképpen az állomások nem fogják egymást zavarni.
	+ Előnyös a használata, ha fix számú felhasználó van és a felhasználók nagy forgalmi igényt támasztanak.
	+ Löketszerű forgalom esetén használata problémás.

119. Röviden mutassa be az idõosztásos nyalábolás módszerét.
	+ N darab felhasználót feltételezünk, az időegységet N egyenlő méretű időrésre – úgynevezett slotra – osztják, és minden egyes réshez hozzárendelnek egy felhasználót.
	+ Löketszerű forgalom esetén használata nem hatékony.

120. A csatorna modellben mit nevezünk ütközésnek?
	+ Ha két keret egy időben kerül átvitelre, akkor átlapolódnak, és az eredményül kapott jel értelmezhetetlenné válik.

121. Hogyan mûködik az egyszerû ALOHA protokoll?
	+  A felhasználó akkor vihet át adatot, amikor csak szeretne.
	+ Ütközés esetén véletlen ideig várakozik az állomás, majd újra próbálkozik.

122. Hogyan mûködik a réselt ALOHA protokoll?
	+ Az idő diszkrét, keretidőhöz igazodó időszeletekre osztásával az ALOHA rendszer kapacitása megduplázható. (1972, Roberts)
	+ A csatorna terhelésének kis növekedése is drasztikusan csökkentheti a médium teljesítményét

123. Hogyan mûködik az 1-perzisztens CSMA protokoll?
	+ Vivőjel érzékelés van, azaz minden állomás belehallgathat a csatornába.
	+ Folytonos időmodellt használ a protokoll
	+ Algoritmus:
		+ Keret leadása előtt belehallgat a csatornába:
			+ Ha foglalt, akkor addig vár, amíg fel nem szabadul. Szabad csatorna esetén azonnal küld. (perzisztens)
			+ Ha szabad, akkor küld.
		+ Ha ütközés történik, akkor az állomás véletlen hosszú ideig vár, majd újrakezdi a keret leadását

124. Hogyan mûködik az nem-perzisztens CSMA protokoll?
	+ Vivőjel érzékelés van, azaz minden állomás belehallgathat a csatornába.
	+ Folytonos időmodellt használ a protokoll
	+ Mohóság kerülése
	+ Algoritmus:
		+ Keret leadása előtt belehallgat a csatornába:
			+ Ha foglalt, akkor véletlen ideig vár (nem figyeli a forgalmat), majd kezdi előröl a küldési algoritmust. (nemperzisztens)
			+ Ha szabad, akkor küld.
		+ Ha ütközés történik, akkor az állomás véletlen hosszú ideig vár, majd újrakezdi a keret leadását.

125. Hogyan mûködik az p-perzisztens CSMA protokoll?
	+ Vivőjel érzékelés van, azaz minden állomás belehallgathat a csatornába.
	+ Diszkrét időmodellt használ a protokoll
	+ Algoritmus:
		+ Adás kész állapotban az állomás belehallgat a csatornába:
			+ Ha foglalt, akkor vár a következő időrésig, majd megismétli az algoritmust.
			+ Ha szabad, akkor p valószínűséggel küld, illetve 1-p valószínűséggel visszalép a szándékától a következő időrésig. Várakozás esetén a következő időrésben megismétli az algoritmust. Ez addig folytatódik, amíg el nem küldi a keretet, vagy amíg egy másik állomás el nem kezd küldeni, mert ilyenkor úgy viselkedik, mintha ütközés történt volna.
		+ Ha ütközés történik, akkor az állomás véletlen hosszú ideig vár, majd újrakezdi a keret leadását.

126. Hogyan mûködik az alapvetõ bittérkép eljárás?
	+ Az ütköztetési periódus N időrés
	+ Ha az i-edik állomás küldeni szeretne, akkor a i-edik versengési időrésben egy 1-es bit elküldésével jelezheti. (adatszórás)
	+ A versengési időszak végére minden állomás ismeri a küldőket. A küldés a sorszámok szerinti sorrendben történik meg.
	+ alapvető bittérkép eljárás hátránya, hogy az állomások számának növekedésével a versengési periódus hossza is nő

127. Hogyan mûködik a bináris visszaszámlálás protokoll?
	+ Minden állomás azonos hosszú bináris azonosítóval rendelkezik.
	+ A forgalmazni kívánó állomás elkezdi a bináris címét bitenként elküldeni a legnagyobb helyi értékű bittel kezdve. Az azonos pozíciójú bitek logikai VAGY kapcsolatba lépnek ütközés esetén. Ha az állomás nullát küld, de egyet hall vissza, akkor feladja a küldési szándékát, mert van nála nagyobb azonosítóval rendelkező küldő.

128. Milyen kábelezési topológiákat támogat az Ethernet szabvány?
	+ Lineáris
	+ Gerincvezetékes
	+ Fa
	+ Szegmentált

129. Miért van szükség a maximális keretméretre?
	+ A szabvány készítésének idején drága volt a memória. A magasabb felső határ több memóriát igényelt volna.

130. Miért van szükség a minimális keretméretre?
	+ A maximális késleltetés és a CSMA/CD algoritmus közötti összefüggés miatt

131. Mutassa be a minimális keretméretre vonatkozó általános képletet.
	+ A maximális késleltetés és a CSMA/CD algoritmus közötti összefüggés miatt a keret elküldése minimum 2τ időre van szükség, ahol τ a két legtávolabbi állomás közötti késleltetést jelöli.

132. Mik a kettes exponenciális visszalépés algoritmus lépései?
	+ Az első ütközés után minden állomás 0 vagy 1 időrésnyit várakozik.
	+ Az i-edik ütközés után minden állomás [0..min (2^i −1; 1023)] egész intervallumból véletlenszerűen kiválasztott időrésnyi ideig várakozik.
	+ A 16-odik próbálkozás után a vezérlő bedobja a törölközőt, és hibajelzést küld a számítógépnek.

133. Mutassa be a rejtett állomás problémáját.
	+ A forgalmaz B-nek. Ha C belehallgat a csatornába, akkor nem hallja A adását, ezért tévesen arra következtethet, hogy elkezdhet sugározni. C elkezdi a küldést, akkor B-nél interferencia lép fel, és az A által küldött keret tönkre megy.
	+ ![rejtett allomas](/images/133rejtett.png)

134. Mutassa be a megvilágított állomás problémáját.
	+  B forgalmaz A-nak. Ha C belehallgat a csatornába, akkor hallja B adását, ezért tévesen arra következtethet, hogy nem kezdhet sugározni D-nek, pedig ez csak a B és C közötti tartományban tenné lehetetlenné a keretek vételét
	+ ![megvialgitott allomas](/images/134megvilagitott.png)

135. Mik a MACA protokoll leglényegesebb lépései?
	+ A küld B-nek egy felkérést: RTS keret.
	+ B küld A-nak egy választ: CTS keret.
	+ A küldi B-nek az adatot a CTS megérkezését követően.

136. Mit nevezünk ad hoc hálózatnak.
	+ Vezeték nélküli LAN egyik lehetséges elrendezési módja, melynél nincs bázisállomás, tehát az eszközök között közvetlen, központosítatlan kapcsolat van.

137. Mi a Network Allocation Vector?
	+ NAV. DCF (Distributed Coordination Function) esetén, a csatornát lefoglaló vektor, mely magában foglalja az ACK-t is.

138. Mit neveznek Short Inter Frame Spacing-nek?
	+ Lehetővé teszi, hogy a rövid párbeszédet folytató felek lehessenek az elsők.

139. Mit neveznek DCF Inter Frame Spacing-nek?
	+ Ezen intervallum lejárta után, akkor bármely állomás próbálkozhat, azaz versengés lesz.

140. Mit neveznek PCF Inter Frame Spacing-nek?
	+ Az SIFS intervallum után mindig pontosan egy állomás jogosult a válaszadásra, ha ezt nem tudja kihasználni, és eltelik ez az PIFS intervallum is, akkor a bázis állomás küldhet egy „beacon frame”-et vagy egy lekérdező keretet.

141. Mit neveznek Extended Inter Frame Spacing-nek?
	+ Ezt az időközt csak olyan állomások használhatják, amelyek épp egy hibás vagy ismeretlen keretet vettek, és ezt kívánják jelenteni.

142. Mi a bridge, és mire használják?
	+ Kettő vagy tobb LAN összekapcsolására szolgáló eszköz.

143. Mi a repeater, és mire használják?
	+ Analóg eszköz, amely két kábelszegmenshez csatlakozik. Az átvitel közben legyengült jelek újragenerálására használják. Nem végez intelligens forgalomirányítást.

#Feleletválasztós minta

* Rendelje a ************* fogalmat az TCP/IP rétegmodell megfelelõ rétegéhez.

<<<<<<< HEAD
ALKALMAZÁSI RÉTEG (Application layer) (https://en.wikipedia.org/wiki/Category:Application_layer_protocols)
	+ HTTP, BitTorrent, munkamenet
=======
+ ALKALMAZÁSI RÉTEG (Application layer) (https://en.wikipedia.org/wiki/Category:Application_layer_protocols)
	+ HTTP, DHCP, BitTorrent, munkamenet
>>>>>>> origin/master

+ SZÁLLÍTÓI RÉTEG (Transport layer) (https://en.wikipedia.org/wiki/Category:Transport_layer_protocols)
	+ SOCKET

<<<<<<< HEAD
HÁLÓZATI RÉTEG (Internet layer) (https://en.wikipedia.org/wiki/Category:Internet_layer_protocols)
	+ DHCP, ICMP, forgalomirányítas, split horizon, routing table, BGP
=======
+ HÁLÓZATI RÉTEG (Internet layer) (https://en.wikipedia.org/wiki/Category:Internet_layer_protocols)
	+ ICMP, forgalomirányítas, split horizon, routing table, BGP
>>>>>>> origin/master

+ KAPCSOLATI RÉTEG (Link layer/Network Access/Network Interface) (https://en.wikipedia.org/wiki/Category:Link_protocols)
	+ Ethernet, PPP, 10Base5, 10Base-F, 10Base2, 10Base-F,  (MACAW, NAV, RTS, CTS, backward learning ?)


* A ********** réteg hányadik rétege az ISO/OSI referencia modellnek?
	+ 7 - Alkalmazási
	+ 6 - Megjelenítési
	+ 5 - Munkamenet
	+ 4 - Szállítási
	+ 3 - Hálózati
	+ 2 - Adatkapcsolati
	+ 1 - Fizikai


* Mi az FTP protokoll alapértelmezett portja?
	+ 21

* Mi az DNS protokoll alapértelmezett portja?
	+ 53

* Hány darab klasszikus TDLs létezik? (TLDs???)
	+ 6 (.com, .edu, .gov, .mil, .org, .net)  (wikipedia szerint .int is)

* Mondjon egy nem klasszikus TDLs-t?
	+ .aero, .museum, .xxx
	+ .hu, .tv, ...

* Hány bájtos egy UDP fejléc?
	+ 8 byte

* A standard TCP fejlécben hány darab jelzõ bitet használnak?
	+ 6 (URG, ACK, PSH, RST, SYN, FIN)

* Hány bájton ábrázolható egy IPv6-os cím?
	+ 128 bit = 16 byte

* Az IPv6 protokollban hány darab kiegészítõ fejrész lehetséges?
	+ 6

* Hány domén név létezik a „root” névszerverekhez?
	+ 13

* Hány elosztott „root” névszerver instancia létezik?
	+ 250


#Számolós feladatok (?)

	* Ha feltételezzük, hogy a kódszavaink egy kódkönyvben egy darab paritás bittel vannak kiegészítve, akkor mekkora a kódkönyvünk Hamming-távolsága?
	* Ha van egy S kódkönyvünk, amelyben a Hamming-távolsága 3, akkor az alábbiak közül melyik a helyes állítás?
	* Tekintsünk az adatkapcsolati rétegben egy bájt alapú protokollt, melyben a keretek egy jelzõ bájttal kezdõdnek és végzõdnek, és a protokoll bájt beszúrást használ. Tudjuk, hogy összesen 8 keretet továbbítunk, amelyek összesített hossza –a médiumon áthaladó bájtok száma– 4096 bájt. Továbbá tudjuk azt is, hogy az átvitelre szánt eredeti ipdatagramban pontosan 45 ESC és pontosan 30 FLAG bájt fordult elõ. Mekkora méretû volt a datagram a keretezés és bájt beszúrás elõtt?
	* Ha 16-bites CRC polinomot használunk, akkor mennyi redundáns bittel kell kiegészítenünk az eredeti adatot?
	* A fellépõ ütközések feloldására adaptív fa bejárást használva legrosszabb esetben hány versengési idõrésre lesz szükség, ha az állomások száma 2^n?
	* Hány hosztot képes kezelni maximálisan az a hálózat, amelynek címe 135.46.56.0/19?
	* Hogyan befolyásolja a minimális keretméretet egy Ethernet hálózatban, ha a két legtávolabbi hoszt távolsága 33%-kal meg nõ?
	* Hogyan befolyásolja a minimális keretméretet egy Ethernet hálózatban, ha a sávszélesség 33%-kal le csökken?
	* Egy szimbólum átviteléhez szükséges idõ 10 µs. Mekkora a szimbólumráta? Mekkora az adatráta, ha 16 szimbólumot használunk?
	* Egy küldõ egy üvegszál kábelen egy fényszignált küld PS teljesítménnyel. Tegyük fel, hogy a fogadónál ennek a szignálnak legalább PS/100 teljesítménnyel kell megérkezni ahhoz, hogy fel tudja ismerni. A kábelben a szignál teljesítményének csökkenése kilométerenként 8%. Milyen hosszú lehet a kábel?
