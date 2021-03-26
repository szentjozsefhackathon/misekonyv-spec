GoogleCalendarSnyc = Szinkronizálás Google Naptárral
===
Fontos fícsör, hogy a plébánián használt Google Naptárba elég az irodán beírni, hogy pl. május 2-án 10 órakor "Temetés: Kovács Ernőné, Katika (Jenő atya)" és a kütyün a [v/date](../views/date) nézetben máris ott van a 10 órás esemény mellett a temetés ikonja és a [v/liturgyOverview](../views/liturgyOverview.md) nézetben az elhunyt neve már ki van töltve.

- Legegyszerűbb megoldásnak használhatjuk a klasszikus Google Naptárat a kütyün. Ott kell beállítani hogy a helyi naptár szinkronizálva legyen.
- Valahol jelezzük az alkalmazásban (lehet a [v/date](../views/date) nézet alja, vagy a [v/menu](../views/menu), vagy inkább a [v/appSettings](../views/appSettings)), hogy mikor volt utoljára szinkronizálva a naptár, hogy feltűnjön ha probléma van.
- A jelzett helyről legyen kattintásra eljutás a megfelelő rendszer beállításokhoz. Ha ott többet is kell kattinthatni, akkor legyen magyarázó leírás előbb.
- Legyen ezen a jelzett helyen egy "Szinkronizálás most" gomb is. Ez vagy rögtön szinkronizáljon, vagy vigyen a megfelelő rendszer részhez (magyarázó szöveggel).

>TODO: Átgondolni és megírni, hogy esetleg minden kütyüt eladás előtt kézzel fel kell konfigurálni? De a konkrét Google Accountba nem fogunk tudni belépni.


Mivel így külső forrás is tudja módosítani a naptárat ezért fontos, hogy 
- az alkalmazás [m/calendar](calendar.md) modulja tudjon mit kezdeni a nem megfelelő elnevezésű naptáreseményeknél

- #### settingsInString (won't)
    Ha az alkalmazás képes lenne egy egy liturgiának minden mentett adatát (lásd: [v/liturgyOverview](../views/liturgyOverview.md)) valami tömör stringbe összefoglalni, akkor azt el lehetne menteni a naptár leírásának a végén. Ezzel pedig megoldható, hogy több külülönálló kütyün pontosan ugyan azok a liturgiák tudjanak futni.

|||
| --- | --- |
| [priority](../definitions.md#priorities) | should |
| dependency | [m/calendar](calendar.md) |
| app-settings | Általános ki és bekapcsolás. |
|| A szinkronizált naptár kiválasztása. (Valószínűbb, hogy a [m/calendar](calendar.md) modulban kell naptárat választani és a Google Calendar alkalmazásba beállítani, hogy az a konkrét naptár szinkronizálva legyen.)|
|| A szinkronizálás gyakoriságát is a rendszer / Google Calendar beállításoknál kell megadni. |