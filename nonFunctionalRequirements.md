# nonFunctionalRequirements = nem Funkcionális Követelmények

## Fejlesztői környezet

Fontos, hogy a későbbi évek során a fejlesztésbe mások is be tudjanak kapcsolódni, akár részben közösségi fejlesztéssel. Valamint, hogy elgépeléseket, naptári tévedéseket könnyen lehessen javítani. Ezért:

- Teljes forráskódot is át kell adni legalább szállításkor. 
- Javaslat: verziókövetett kód-megosztás már fejlesztés közben is. Akár mehet nyíltan github-on.



- A naptárak és szövegeket valamilyen, ember számára is olvasható, szöveges formában legyen tárolva (pl xml, json, csv) a többi kódtól elkülönítve. (See: [Adatbázis - szövegforrás](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.kz5p7s6kd98w).)
- A definiált fejlesztői környezet telepítése után néhány lépéssel (max 5) mindig le lehessen fordítani teljes értékű .apk csomaggá az alkalmazást.
- Ez a building process akadjon el, ha a szövegekben szintaktikai hiba van. És térjen vissza a hiba helyéve.
- Javaslat: már fejlesztés közben is lehetne élni ezzel a lehetőséggel és akkor a szöveg fájlok fejlesztése részben kiszervezhető. (See: [Adatbázis - szövegforrás](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.kz5p7s6kd98w).)



## Többnyelvűség - m-i18n

Bár most magyarul készül az app, de készen kell álljon a nemzetközi debütálásra három szinten is:

- Felület fordítható legyen. [app-settings](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.fvmxvlofvf63)-ben vagy külön menü pontban nyelv állítás
- A liturgiák nyelve a [liturgy overview ](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.drdnoaqmzos7)nézetben állítható legyen, ha az adott liturgiának lesz többféle nyelve.
- A kód nyelve (változók, függvények, osztályok, magyarázatok, stb.) legyen angol. (Esetleg szakszavak lehetnek latinul. :P) Hogy későbbi továbbfejlesztés és nemzetköziesítés esetén lehessen bármit.

priority: must



## Támogatott eszköz és kompatibilitás

Az eszköz *valószínűleg* az Onyx Boox Note Air/3 (10,3 inch) ill. az Onyx Boox Nova 3 / 3 Color (7,8 inch) lesz. Ezért

- Csak Android platform
- Android 10+
- A fenti 2 képernyőre kell csak optimalizálni. De legyen meg a lehetőség később más, legalább 7,8 inch képernyőre is tovább alakítani. (Azaz megjelenítés leválasztása a kód többi részéről.)
- Be legyen égetve, hogy csak a felsorolt eszközökön fut. (De ki lehessen szedni a kódból egy újabb build előtt, ha kell.)
- Alapvetően fekete-fehér (szürkeárnyalatos) e-ink kijelzőn fog működni. De álljon készen a misekönyv fekete, fehér, piros (három szín) leképezésére színes képernyőn.



## Telepítés, telepíthetőség

Mivel egyelőre kis példányszám a reális (pár száz), ezért lehetséges megoldás az is, hogy egyesével minden kütyün kézzel valaki feltelepíti a megfelelő alkalmazásokat, beállítja amit be kell és úgy csomagolja el. 

Viszont figyelembe kell venni, hogy: a Google Play telepítése valószínűleg nem megoldható a kütyün konkrét google account nélkül. Google Naptár és Dokumentumok szinkronizálásához már a felhasználó kell majd mindenképpen, mert neki kell nevet és jelszót megadnia. 

- Az első telepítéshez szabad hogy szükség legyen internetre. De a felhasználó az első használatkor már mindent elérjen offline is amire csak szüksége van. 

  

- Készüljön dokumentáció ami lépésről lépésre leírja az első telepítendőket és első beállításokat egy rutinos android felhasználó számára.
- Készüljön leírás az új felhasználók számára, hogy hogyan tudják beállítani a Google Naptárat ([m-GCalendarSync](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.82gt9abgiysj)) és Dokumentumokat ([m-prédikáció](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.zc50y4hvw581), [m-hirdetések](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.xd6x2xm484ek))



## Frissíthetőség, frissítés

Mivel várhatóan nem lesz Google Play szolgáltatás a kütyün, ezért másképp kell megoldani az app frissítését.

- Jó lenne, ha liturgikus szöveg módosulása esetén (pl. egy rosszul szerepelt egy szentnél hogy milyen közös részeket lehet használni) ne kelljen a több ezer oldalnyi szöveget egyben újra letölteni, elég legyen a szükséges módosulásokat.

  > Todo: Kitalálni és rögzíteni a frissítés lehetőségét.

- *Javaslat / Kérdés / Ötlet: mi van, ha az applikáció csak egyféle üres keret. Mintegy böngésző féle. És a háttér cloud-ról pl rest api-val húzza le a szöveg bázist (mint böngészőknél a html) és az összeállító kódot (mint böngészőknél a javascriptek). Így továbbra is minden működhet offline, de nagyon könnyű frissíteni szinten mindent. Ha ez elég stabil. (Ebben az esetben persze nagyon definiálni kell a rest api működését. Szerver van rá.)*



## Analitikai eszközök

Nem szükséges.



## Dokumentáció

A későbbi vágyott idegennyelvűsítés miatt fontos, hogy más programozók is be tudjanak majd lépni a fejlesztésbe. Ezért:

- A dokumentáció angolul történjen.
- Legyen dokumentáció. :D 

*Kérdés: hogyan kell jól megfogalmazni a dokumentáció követelményét? Csak van rá valami standard.*



## Felhasználói Kézikönyv (Dokumentáció)

Kell készüljön leírás képekkel a felhasználó számára is, hogy tudja kezelni a programot.

- Általános leírás. Nap választás. Liturgia választás. Részletek beállítása. Liturgia nézet. App beállítások. -» Minden [nézethez](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.wqe3k19v3ce) kell legyen leírás.
- Az első használatnál lévő teendők. (See: [Telepítés, telepíthetőség](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.21i1p1fg58t4))

## Support igény

> TODO: meghatározni