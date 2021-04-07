# liturgicalCalendar

A mozgó és naptári ünnepeket sorát és rétegeit rendezi egybe és követi le azok egymásra hatását és így kiböki, hogy adott bármilyen napon milyen ünnepek vannak és lehetségesek. 

A cél, hogy tudja a gép és a felhasználó is az aznapi liturgiák legfontosabb. Gyakorlatilag egy örök direktórium kell hibák nélkül: https://issuu.com/malezi/docs/dir2021_jav_2020-12-02 

A szentmise szövegeinek összeállítása a liturgikus naptár alapján történik. Ez határozza meg, hogy melyik év van (A/B/C, I-II), milyen időszak van (évközi, adventi, karácsonyi, nagyböjti, húsvéti, pünkösdi, *+ egyéb*). A fix ünnepeken kívül mozgó ünnepek is vannak, és ezek bizonyos szabályok szerint hatnak egymásra (felülírják, vagy az alsóbbrendű átkerül eggyel, ha éppen nem üti ott valami). Ezek alapján mutatja, hogy milyen ünnep/emléknap/stb. van, az milyen fokozatot jelent. Illetve van-e valamilyen különleges esemény ami módosítja a mise egy részét (hamvazkodás, Balázs-áldás, körmenet). Vagy akár egészen saját liturgia van (nagycsütörtök, nagypéntek, feltámadás). Adott napon belül is lehet többféle liturgia karácsonykor és húsvétkor (éjféli mise, pásztorok miséje, karácsonyi mise; feltámadási szertartás, húsvéti ünnepi mise). Van, hogy a naptár végeredménye több opciót kínál fel (pl. fakultatív emléknapok), ami közül a felhasználó választhat szabadon. Valamint általában - ha az előbbiek közül valami nem tiltja - akkor lehet szabadon választani votív misék közül, vagy gyászmisét, *stb.*

A liturgikus naptárnak több rétege van, amik felülírhatnak alattuk lévő naptárakat:

- római, központi naptár
- Magyarországon azaz az MKPK területén érvényés liturgikus naptár. Ez eltér(het) konkrét ünnepek fokozatában és helyében is. Valamint vízkereszt és az Úr napja lehet a napján vagy vasárnap a megfelelő szabályozás szerint. *Ezzel párhuzamos például az erdélyi római egyházmegyék liturgikus naptára*. 
- Egyes egyházmegyéknek van egy-két saját főünnepük. *Ezek az előző naptárban vannak definiálva és az opcióknál jelennek meg, hogy “ünnep” vagy “Váci egyházmegyében főünnep”. Minden részük lehet saját.*
- Szerzetesrendeknek lehet saját naptárjuk pár arrébb rakott vagy másszinten megemlékezett ünneppel. 

Ezek rendszerét a **Misekönyv pontosan definiálja** 

**Technikai extrák**

- Könnyen lehessen a kódhoz új naptára hozzátenni. (Például egy megfelelően formázott xml vagy json fájlal.)

  A naptárfunkcióra jól működő példa adatokkal: https://github.com/breviar-sk/Liturgia-hodin-online A honlapján xml kimenetben lekérhető az ünnep. 

  Ezek alapján tudjuk, hogy mi a liturgikus szín, van-e dicsőség, van-e hiszekegy, mik az olvasmányok, a könyörgések, mely prefációk közül lehet választani, milyen idő van (ami befolyásol pár részt), stb. 

  Minden elemhez a kódba égetve lehet extra üzenetet tenni, *pl. “Szegények világnapja”. De fontos, hogy lehessen olyat ami évre pontosan konkrét dátumhoz kötött, mert más évben lehet máskor lesz. Akkor küldünk új frissítést. Ilyen pl. az “Ökumenikus imahét kezdete”.* 

  Ezek tudása egyértelműen nélkülözhetetlen. Viszont több módon megszerezhető (és csak kiegészítnei kell):

  - Ideiglenesen használhatjuk az zsolozsma online változatánák xml outputját, az tökéletesen határozza meg a napot. Viszont internet kell hozzá.

  - A zsolozsma android alkalmazásba bekerülhet (megkérhetjük őket / megírjuk nekik), hogy androidon alkalmazás az alkalmazástól megszerezze az infókat. Minek két kódot írni?

  - Ebbe az alkalmazásba bekerül a teljes naptár feldolgozó funkció.

    Több féle szinten megoldható (pl. előre egy évre begépelve, vagy öröknaptár leprogramozva), de léte nélkülözhetetlen.

    

|                                          |                                                              |
| ---------------------------------------- | ------------------------------------------------------------ |
| [priority](../definitions.md#priorities) | must                                                         |
| dependency                               | -                                                            |
| [v/appSettings](../views/appSettings.md) | A felhasználni kívánt liturgikus naptárak kiválasztása.<ul><li>Magyarországi \| *Kérdés: erdélyi, felvidéki, stb. kicsit külön? Valószínűleg igen.</li><li>*Egyházmegye kiválasztása. (Lényegében csak a bazilika felszentelése és védőszent. De legyen meg szépen külön-külön mind.)</li><li>Szerzetesközösség saját naptára. </li></ul>(Default: nincs.) |

