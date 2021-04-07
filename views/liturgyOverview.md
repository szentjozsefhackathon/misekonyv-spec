# liturgyOverviewView

Egy konkrét nap egy konkrét liturgiáinak adatai / beállításai / összefoglalója. A liturgia legyártásánál is ehhez jutunk el, de gyakran a kiválsztás folyamatában extra kérdések is vannak ez előtt. Ez után már csak a konkrét [v/liturgy](liturgy.md) jön.

**Alap adatok**, amiket nem lehet módosítani. (Legfeljebb törölni és újat csinálni.):

- dátumi

- dőpont

- liturgia típusa (see: [v/chooseLiturgyType](chooseLiturgyType.md))

- nyelv választása amikor lehet. (várhatóan modulonként készül majd). Default: az app nyelve az  [v/appSettings](appSettings.md)ben. see: [m/i18n](../modules/i18n.md)

  > Todo: Mit tegyen, ha az app nyelve litván, de a választott papszentelés csak magyarul érhető el.

  A további adatok és beállítások nagyban függnek hogy milyen liturgia típusról ill. altípusról van szó. 



A további beállítások / megjelenítendők eltér(het)nek a liturgia típustól függően. Következik pár liturgia specifikus részlet:



## mass overview 

- Legördülő listából kiválaszthatja, hogy milyen mise legyen. A lista elején szerepelnek liturgikus nap lehetőségei ([m/liturgicalCalendar](../modules/liturgicalCalendar.md)) (például köznap vagy fakultatív emléknap) majd az [extra misék](../modules/mass.md#extra-misék): a négy fejléc először (rituális, különféle szükségletekre, votív, gyász). Rá kattintás esetén ezek lenyílnak. A második szintek (pl. 2.2.) fejlécként jelennek meg és harmadik szintig minden - ami lehetséges adott időben / le van fejlesztve. (Mindegyik lista az [m/liturgicalCalendar](../modules/liturgicalCalendar.md) alapján előszűrt.)

- Ha a listából kiválasztáshoz vannak kérdések akkor azok megjelennek ezen a nézeten. Talán nem felugró új ablakban, hanem beépülve. (Például: férfi vagy női szerzetes? Egy vagy több?)

  > Todo: az alábbiak sorrendjét lehet át kell nézni.

- olvasmányok

  - hosszú vagy rövid szöveg választása, csak ha van rá lehetőség
  - választási lehetőség pl. nagyböjt iii, iv, v. vasárnapján lehet A évből mindig
  - emléknapnál választható a szent olvasmánya és a köznap olvasmánya isvan hogy csak egyik választható, akkor azt (pl. pünkösd vigília, vagy pünkösd, lásd olvasmányoskönyv vasárnap b év, p 175, c év 178, a év 218)kiírjuk akkor is, ha nem választható.  [v/appSettings](appSettings.md)ben állítható a default
    pl: “Köznapi olvasmányok: Ter 37,3-4.12-13a.17b-28  Zsolt 104   Mt 21,33-43.45-46” - Linkkel, ami a [v/liturgy](liturgy.md)ban odaugrik ahova kell.

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

  - forrás: [m/praeorator](../modules/praeorator.md). 

    > Todo: azért soroljuk fel itt is.

  

- [m/homily](../modules/homily.md) esetén mindig írja ki, hogy talált-e prédikáció és ha nem, akkor lehessen választani.

- [m/announcements](../modules/announcements.md) esetén mindig írja ki, hogy talált-e hirdetéseket. ha igen, akkor mi a fájl neve, ha nem, akkor lehessen választani

- [m/prayersOfTheFaithful](../modules/prayersOfTheFaithful.md) esetén mindig írja ki, hogy talált-e könyörgéseket. ha igen, akkor mi a fájl neve, ha nem, akkor lehessen választani

- [m/musicListing](../modules/musicListing.md) esetén írja ki röviden az énekrendet, ha van. link/gomb a módosításhoz (külön app)

  

- mise típustól függő string, amit a naptár címsorában is tárolunk

  - szimpla mise esetén intenció (azaz egy név vagy nevek, hogy kikért mondjuk a misét, lehet benne extra szimbólum min a kereszt)
  - az [m/export](../modules/export.md) miséknél a leírásban ott van, hogy hol mi a kérdés. lehet több is! (ezeket befolyásolhatja a kánon is. )
  - [m/googleCalendarSync](../modules/googleCalendarSync.md) esetén fontos ezt menteni

- ### további beállítások 

  (legördülő lista, mindegyik [v/appSettings](appSettings.md) default-al rendelkezik, legördülve és kiemelve/jelölve, ha a default-tól eltérő értékre van állítva. esetleg fejlécekkel csoportosítva)

  - általános megjelenítés: teljes (rubrikákkal), egyszerű (rubrikák nélkül, de minden szó), minimalista (hiszekegy első sora, Miatyánk egy sorban, stb.)

    - Figyelem! A minimalistánál is feliratrakattintva kinyíljon a teljes. (azaz legyen pánik gomb). Nem kell talán külön felirat csak erre.
    - Az olvasmányok (olvasmány/szentlecke/evangélium) esetén is számít ez a három szintű beállítás. See: [d/readings](../dataschemas/readings.md).
      - teljes: minden. az is az evangéliumnál, hogy “az úr legyen veletek”
      - egyszerű: a dőlt betús “bevezető magyarázó szöveg” és “rövid bevezető” nem jelenik meg. Se “az úr legyen veletek”.
      - minimalista: csak “Felszólítás” és “text”. Lezárás sem kell.
    - Zsoltároknál is számít ez a három szintű beállítás: See: [d/readings](../dataschemas/readings.md).
      - teljes: teljes. válasz minden vers után ismételve
      - egyszerű: válasz csak egyszer az elején
      - minimalilsta: tónus és ref nélkül. csak egy válasz és utána a sok vers. ha van zárójeles, akkor attól még az benne marad.
    - Állelujánál is számít ez a három szintű beállítás: See: [d/readings](../dataschemas/readings.md).
      - teljes
      - egyszerű = minimalista: csak a “text”
    - Hívek könyörgésénél az egyetemes könyörgéseknél. See: [d/prayersOfTheFaithful](../dataschemas/prayersOfTheFaithful.md)
      - teljes: mindig suffix is és válasz is.
      - egyszerű: mint a könyvben: első után csak rövidített válasz
      - minimalista: a válasz csak egyszer. magyarországon úgy sem. suffix nélkül. “pap” “lektor” feliratok nélkül.

    

  - dallamok megjelenítése ([m/melodies](../modules/melodies.md)): enum(teljes, normál, nem)

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
    - [m/export](../modules/export.md) esetén ide egy export gomb valahova.

    *Todo: mit kezdjünk azzal, hogy illegális dátum - liturgy - type összeállítás van?*

    

  - egyházmegye azaz püspök

  - extra fícsör? : sine popolo /normál / koncelebráció ? -> rubrika magyarázatok másznak a helyükre. de kell ez? ad ez annyit?

  - Geolokalizáció: hol vagyok

    - Válasz érték: Egyházmegye és püspöke.
    - Általános beállításoknál: magam beírom, vagy lokáció alapján próbálkozzon. Ja, de nincs GPS benne. Szóval ez később.

