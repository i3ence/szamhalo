#Számítógépes hálózatok definíciók kidolgozás 2015-16/1 félév

források: 
+ peet91: számhálók definíció kidolgozás 2014 (elte.sharq.hu)
+ előadás diái (http://people.inf.elte.hu/acszolta/computer_networks)
+ wikipedia (https://en.wikipedia.org/wiki/Revocation_list, ...)

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

(18-19 az ea alapján van, de szerintem nem ok)

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
	+ 
Mik a p2p hálózatok legfontosabb jellemzõi?
Mi a szerepe egy peer-nek egy p2p hálózatban? 
Mit nevezünk choke peer-nek? 
Mi az a seed peer? 
Mire szolgál az állapot nélküli tûzfal? 
Mire szolgál az állapot alapú tûzfal? 
Mire szolgál az alkalmazás réteg tûzfal?
Mi az a DeMilitarized Zone? Mire szolgál?
Mire szolgál a TCP protokoll? Mik a fõbb jellemzõi?
Mire szolgál az UDP protokoll? Mik a fõbb jellemzõi?
Mit neveznek adási ablaknak?
Mit neveznek vételi ablaknak?
Mi a CRC? Mire használható? 
Hogyan történik egy TCP kapcsolat felépítése? Mik a lépései? 
Mit jelent az RTO, és hol használják?
Mi a TCP Nagle algoritmus mûködési alapelve? 
Mi az a "slow start" TCP esetén? 
Mi az a torlódási ablak? Mire szolgál? 
Mi az gyors újraadás TCP Tahoe esetén? 
Mit jelenthet az ha három azonos nyugta érkezik egymás után? 
Mi az AIMD torlódás kerülési stratégia lényege?  
Mit nevezünk torlódásnak TCP esetén?
Mikor nevezünk egy torlódás kerülési algoritmust hatékonynak?
Mikor nevezünk egy torlódás kerülési algoritmust fairnek? 
Mi a forgalomirányító algoritmusok definiciója?
Mi a statikus forgalomirányító algoritmusok fõ jellemzõje?
Mi az adaptív forgalomirányító algoritmusok fõ jellemzõje?
Mi a hierarchikus forgalomirányítás lényege? 
Mit nevezünk adatszórásnak vagy broadcasting-nak?   
Mit nevezünk többesküldésnek vagy multicasting-nak? 
Mi a többcélú forgalomirányítás lényege?
Mire szolgál a DF bit az IPv4 fejlécében? 
Mire szolgál a MF bit az IPv4 fejlécében? 
Mire szolgál a szolgálat típusa mezõ az IPv4 fejlécében?
Mire szolgál az élettartam (TTL) mezõ az IPv4 fejlécében? 
Mi az IPv4 cím és hogyan ábrázoljuk? 
Mi az IPv6 cím és hogyan ábrázoljuk? 
Milyen speciális IPv4 címek vannak?
Mi az alhálózati maszk és mire szolgál? 
Mire szolgál az ICMP protokoll?
Mire szolgál az ARP protokoll?
Mi az RARP? Mire használják?
Mi az BOOTP? Mire használják?
Mi az DHCP? Mire használják? 
Mi az a gerinchálózat? Hol használják és mire? 
Mely 3 féle összeköttetést és hálózatot támogatja az OSPF? 
Milyen úttípusok léteznek az OSPF logikája szerint?
Mit nevez a BGP csonka hálózatnak? 
Mit nevez a BGP többszörösen bekötött hálózatnak?
Mit nevez a BGP tranzit hálózatnak? 
Soroljon fel 4 vezetékes átviteli közeget. (8!)
Mit nevezünk frekvenciának? Mi a mértékegysége és hogyan jelölik?
Soroljon fel 3 elektromágneses tartományt.
Soroljon fel 4 vezeték nélküli átviteli közeget. (13!)
Mi a szimbólumráta és az adatráta? Mi a mértékegységük? 
Soroljon fel 3 óraszinkronizációs módszert. 
Mi az önütemezõ jel? Mire használható?
Mi a digitális kódok leírásának 3 fõ jellemzõje? 
Mi az alapsáv? 
Mi a szélessáv? 
Mi az amplitúdó moduláció?
Mi a frekvencia moduláció?
Mi a fázis moduláció?
Mit nevezünk BER-nek? Mire használják?
Milyen tényezõktõl függ a BER?
Mi a CDMA?
Mi az a Walsh mátrix? Mire használható?
Az adatkapcsolati réteg milyen jól definiált interfészeket biztosít a hálózati réteg felé?
Milyen módszereket ismer a keretezésre az adatkapcsolati rétegben? 
Hogyan mûködik a karakterszámlálás? 
Hogyan mûködik a karakterbeszúrás? 
Hogyan mûködik a bitbeszúrás?
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
