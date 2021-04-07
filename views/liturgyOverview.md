# liturgy Overview/Settings View

Egy konkrét nap egy konkrét liturgiáinak adatai / beállításai / összefoglalója. A liturgia legyártásánál is ehhez jutunk el, de gyakran a kiválsztás folyamatában extra kérdések is vannak ez előtt. Ez után már csak a konkrét [liturgy view ](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.4z2jqlkchash)jön.

**Alap adatok**, amiket nem lehet módosítani. (Legfeljebb törölni és újat csinálni.):

- dátumi

- dőpont

- liturgia típusa (see: [choose liturgy type](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.6cwabmc0rgqw))

- nyelv választása amikor lehet. (várhatóan modulonként készül majd). Default: az app nyelve az [app-settings](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.fvmxvlofvf63)-ben. see: [m-i18n](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.g23gobg8o366)

  > Todo: Mit tegyen, ha az app nyelve litván, de a választott papszentelés csak magyarul érhető el.

  A további adatok és beállítások nagyban függnek hogy milyen liturgia típusról ill. altípusról van szó. 



A további beállítások / megjelenítendők eltér(het)nek a liturgia típustól függően. Következik pár liturgia specifikus részlet:



## mass overview 

- Legördülő listából kiválaszthatja, hogy milyen mise legyen. A lista elején szerepelnek liturgikus nap lehetőségei ([m-igenaptár](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.5uusvmtsj8nl)) (például köznap vagy fakultatív emléknap) majd az [extra misék](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.tuyp4zs6rxh6): a három fejléc először ([rituális](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.a3qafcq6jb80), [különféle szükségletekre](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.k0utu0n2l86b), [votív](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.y6k6escr4ind)). Rá kattintás esetén ezek lenyílnak. A második szintek (pl. 2.2.) fejlécként jelennek meg és harmadik szintig minden - ami lehetséges adott időben / le van fejlesztve. (Mindegyik lista az [m-igenaptár](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.5uusvmtsj8nl) alapján előszűrt.)

- Ha a listából kiválasztáshoz vannak kérdések akkor azok megjelennek ezen a nézeten. Talán nem felugró új ablakban, hanem beépülve. (Például: férfi vagy női szerzetes? Egy vagy több?)

  > Todo: az alábbiak sorrendjét lehet át kell nézni.

- olvasmányok

  - hosszú vagy rövid szöveg választása, csak ha van rá lehetőség
  - választási lehetőség pl. nagyböjt iii, iv, v. vasárnapján lehet A évből mindig
  - emléknapnál választható a szent olvasmánya és a köznap olvasmánya isvan hogy csak egyik választható, akkor azt (pl. pünkösd vigília, vagy pünkösd, lásd olvasmányoskönyv vasárnap b év, p 175, c év 178, a év 218)kiírjuk akkor is, ha nem választható. [apps-settings](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.fvmxvlofvf63)ben állítható a default
    pl: “Köznapi olvasmányok: Ter 37,3-4.12-13a.17b-28  Zsolt 104   Mt 21,33-43.45-46” - Linkkel, ami a [liturgy view](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.4z2jqlkchash)-ban odaugrik ahova kell.

- honnan vegye a misét, ha választható: pl. vértanú vagy szerzetes

  - default: mindig az első. *Kérdés: inkább random mindig?*
  - legyen mindig kiírva: “mise a szerzetesekről”

- melyik prefáció legyen, ha választható

  - default: mindig az első. *Kérdés: inkább random mindig?*
  - legyen mindig kiírva: “prefáció: Húsvét IV (a feltámadás öröme)”

- melyik kánon legyen (vigyázat! valamelyik kánon meghatározza a prefációt)

  - default: ünnep rangja alapján: I, II, III, IV

  - legyen mindig kiírva: “kánon: VIIa”

    > Todo: a defaultot meghatározni rendesen.

- lesz-e extra, ha lehetne: balázs áldás, körmenet, ételszentelés, hamvazkodás, stb.

  - default lesz

  - csak akkor legyen kiírva, ha van olyan opció hogy lesz

  - forrás: [m-praerator](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.acw5runa3m21). 

    > Todo: azért soroljuk fel itt is.

  

- [m-prédikáció](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.zc50y4hvw581) esetén mindig írja ki, hogy talált-e prédikáció és ha nem, akkor lehessen választani.

- [m-hívekkönyörgése ](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.vnvieity497o)esetén mindig írja ki, hogy talált-e könyörgéseket. ha igen, akkor mi a fájl neve, ha nem, akkor lehessen választani

- [m-hirdetések](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.xd6x2xm484ek) esetén mindig írja ki, hogy talált-e könyörgéseket. ha igen, akkor mi a fájl neve, ha nem, akkor lehessen választani

- [m-énekrend ](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.nky42fikc1ha)esetén írja ki röviden az énekrendet, ha van. link/gomb a módosításhoz (külön app)

  

- mise típustól függő string, amit a naptár címsorában is tárolunk

  - szimpla mise esetén intenció (azaz egy név vagy nevek, hogy kikért mondjuk a misét, lehet benne extra szimbólum min a kereszt)
  - az [extra ](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.tuyp4zs6rxh6)miséknél a leírásban ott van, hogy hol mi a kérdés. lehet több is! (ezeket befolyásolhatja a kánon is. )
  - [m-GCalendarSync](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.82gt9abgiysj) esetén fontos ezt menteni

- ### további beállítások 

  (legördülő lista, mindegyik [app-settings ](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.fvmxvlofvf63)default-al rendelkezik, legördülve és kiemelve/jelölve, ha a default-tól eltérő értékre van állítva. esetleg fejlécekkel csoportosítva)

  - általános megjelenítés: teljes (rubrikákkal), egyszerű (rubrikák nélkül, de minden szó), minimalista (hiszekegy első sora, Miatyánk egy sorban, stb.)

    - Figyelem! A minimalistánál is feliratrakattintva kinyíljon a teljes. (azaz legyen pánik gomb). Nem kell talán külön felirat csak erre.
    - Az olvasmányok (olvasmány/szentlecke/evangélium) esetén is számít ez a három szintű beállítás. See: [Olvasmányok](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.gkajf8a8b7vr). 
      - teljes: minden. az is az evangéliumnál, hogy “az úr legyen veletek”
      - egyszerű: a dőlt betús “bevezető magyarázó szöveg” és “rövid bevezető” nem jelenik meg. Se “az úr legyen veletek”.
      - minimalista: csak “Felszólítás” és “text”. Lezárás sem kell.
    - Zsoltároknál is számít ez a három szintű beállítás: See: [Olvasmányok](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.gkajf8a8b7vr). 
      - teljes: teljes. válasz minden vers után ismételve
      - egyszerű: válasz csak egyszer az elején
      - minimalilsta: tónus és ref nélkül. csak egy válasz és utána a sok vers. ha van zárójeles, akkor attól még az benne marad.
    - Állelujánál is számít ez a három szintű beállítás: See: [Olvasmányok](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.gkajf8a8b7vr). 
      - teljes
      - egyszerű = minimalista: csak a “text”
    - Hívek könyörgésénél az egyetemes könyörgéseknél. See: [Egyetemes könyörgések](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.5bwixieinq6t)
      - teljes: mindig suffix is és válasz is.
      - egyszerű: mint a könyvben: első után csak rövidített válasz
      - minimalista: a válasz csak egyszer. magyarországon úgy sem. suffix nélkül. “pap” “lektor” feliratok nélkül.

    

  - dallamok megjelenítése ([m-dallamok](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.et6efnsz4kvu)): enum(teljes, normál, nem)

    - teljes: sorról sorra mindenhol ahol lehetséges ott a kotta. például zsoltár minden soránál.
    - normál: zsoltároknál csak első sornál, utána már 
    - nem kellnem: nincs kotta

    

  - hiszekegy közül: 1, 2, mindkettő (pánik gombbal mindkettő)

  - bevezető szertartás: 1, 2, mindegyik (pánik gombbal mindegyik)

  - uram irgalmazz: konkrétan valamelyik / mindegyik (pánik gombra mindegyik)

  - “íme hitünk szent titka”: konkrét / mindegyik (pánik gombra mindegyik)

  - záróáldás extra-e. (ennek beállítása esetén az összefoglaló oldalon megjelenik, hogy ez be van állítva!)

  - elbocsátás (pánik gombra mindegyik)

  - püspök megnevézes. string, amiben szabadon hosszabban is lehet írni, mert a koadjutorok is megemlíthetőek. (elvileg lehetne az egyházmegyéből, de biztosabb így) (jó, ha így is tudják állítani, mert van hogy csak egy-két nap másutt, és akkor jól jön, hogy át lehet állítani csak egy misére)

    > Todo: mi van itt még?

  - alul/végén:

    - mentés. *Kérdés: vagy mindig mentsünk automatikusan? inkább az!*
    - törlés (kicsit külön a többitől, de legyen rá lehetőség)
    - [m-export](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.lbiyxb6w3e1k) esetén ide egy export gomb valahova.

    *Todo: mit kezdjünk azzal, hogy illegális dátum - liturgy - type összeállítás van?*

    

  - egyházmegye azaz püspök

  - extra fícsör? : sine popolo /normál / koncelebráció ? -> rubrika magyarázatok másznak a helyükre. de kell ez? ad ez annyit?

  - Geolokalizáció: hol vagyok

    - Válasz érték: Egyházmegye és püspöke.
    - Általános beállításoknál: magam beírom, vagy lokáció alapján próbálkozzon. Ja, de nincs GPS benne. Szóval ez később.

