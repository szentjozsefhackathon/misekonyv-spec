# (current) dateView = Adott naphoz tartozó kezdő oldal

Középen egymás alatt ezek:

- Dátum
  - A nap dátuma. 
    - Ha ma, akkor írja is, hogy ma.
    - Date pickerrel változtatható VAGY jobbra-balra húzogatással. *Kérdés: melyik legyen. Mindkettő?*
    - Át lehet ugorni a [v/week](week.md)ba
  - Liturgikus leírása a napnak ([m/liturgicalCalendar](../modules/liturgicalCalendar.md))
    - Milyen ünnep/ünnepek vannak aznap. Választható esetén mind. Egymás utáni sorokban.
      - Ünnep neve, súlya (FÜ, Ü, E, e, stb.), színe(i)
      - (Nem szükséges: olvasmányok, közös részek helyei, stb.)
    - Ha másnap minimum Ünnep van, akkor egy sor, hogy “Előeste: “ és utána helyzettől függően ilyesmi: “minden a vasárnapról”.
    - Olykor extra szöveg megjelnítése
      - [m/praeorator](../modules/praeorator.md)ból az önálló vagy misekiegészítés változatra felhívjuk a figyelmet: “Ezen a napon szokás a terménybetakarítási ájtatosság”. (Aztán a [v/liturgyOverview](liturgyOverview.md)ban felkínálja a lehetőséget.)Naptár adatok, avagy a már felvett liturgiák soronként / egyféle táblázatban ([m/calendar](../modules/calendar.md)). 
      - kezdés ideje
      - liturgia típusa: a  [v/chooseLiturgyType](chooseLiturgyType.md)ban leírt opciók közül
      - egy megfelelő adata a liturgiának: pl. szentmisénél intenció, nászmisénél a pár neve, temetésnél az elhunyt neve, stb.
      - beállítások/részletek gomb. Ezen keresztül lehet eljutni a liturgia megkezdéséhez. Átvisz a [v/liturgyOverview](liturgyOverview.md)ra.
      - Ha a [m/calendar](../modules/calendar.md).f-gcalendarsync akkor kellhet ide “liturgia csatolása” gomb. Ikonja a liturgia típusa szerint való, ha a névből rájön. Ha nem, akkor a [v/chooseLiturgyType](chooseLiturgyType.md)n keresztül.
      - *Todo: mit kezdjünk azzal, hogy illegális dátum - liturgy - type összeállítás van?
      - ***Kérdés: legyen-e itt több adat.* 
        - ***Egyszerű “egyéb infó / komment” mező?**
        - ~~Pl. szentmisénél, hogy melyik. Olvasmányoknál az szentírási hely, stb.~~
      - *Új liturgia hozzáadása (*Kérdés: legalul?*): 
        - a  [v/chooseLiturgyType](chooseLiturgyType.md) legfőbb ikonjai (mise, nászmise, keresztelő, temetés), majd egy “több” ikon amire a többi lehetőség is elöjön egy nagy ikon sort / sorokat képezbe.
        - Ikonok amikre kattintva új liturgiát lehet létrehozni. Kattintva végig megy a liturgiák elkészítése kérdéseken és úgy jut el a [v/liturgyOverview](liturgyOverview.md)ba.
      - A használt naptárak megjelenítése kicsivel, hogy hamar észrevegyük, ha más az egyházmegye, vagy a szerzetesi be van kapcsolva. Például: “Magyarország - Szombathelyi egyházmegye, Ferences naptár” ([m/liturgicalCalendar](../modules/liturgicalCalendar.md) ). Kattintásra bejön az [v/appSettings](appSettings.md) fókuszálva az adott naptárválasztóhoz.

