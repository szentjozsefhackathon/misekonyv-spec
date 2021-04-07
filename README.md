# misekonyv-spec
A Digitális Misekönyv (és további liturgikus alkalmazások) specifikációja

A digitális misekönyv egy saját hardverrel és szoftverrel rendelkező e-ink kijelzős kütyü ami római katolikus papoknak, diakónusnak és igeliturgiákat végzőnek segít abban, hogy a kütyün kívül semmilyen más liturgikus könyvet ne kelljen magukkal vinniük, valamint a liturgia helyszínén már ne kelljen lapozgatni, hanem az előzetes beállítások alapján egybe megmutatja a liturgia teljes menetét (ha kell akkor a hivatalos megjegyzésekkel és opciókkal). Ez 10-12 db 300-800 oldalas könyv kiváltását jelenti. Lásd még: http://misekonyv.hu

Tartalmaz mindenféle szentmisét, keresztelés, házasság, és temetési liturgiákat. (Későbbiekben még bérmálás, papirendek, stb. stb. Lásd: [choose liturgy type](views/chooseLiturgyType.md) Az alkalmazás hasonlít az [*iMassal*hoz ](http://www.imissal.com/)abban, hogy a szentmise minden szövege benne van és akár más imák is. Viszont inkább úgy működik mint a [*zsolozsma* ](https://lh.kbs.sk/hu/default.htm)alkalmazás: egészen offline és az adott napi beállítások alapján egyetlen képernyőre vágja össze az aktuális liturgia minden részét. Illetve nem egyetlen app, hanem egy launcher + meghatározott alkalmazások gyűjteménye, melyek között kiemelkedő maga a misekönyv alkalmazás. 

- [Célközönség](target.md)
- [Szóhasználat definíciói](definitions.md)
- [Az ajánlatkérés scope-ja](inquiry.md)

Programozandó részek
- [A Launcher](thelauncher.md)

# Nézetek

> TODO: Wireframek készítése még szükséges.

- (current) [dateView](views/date.md) (default / kezdőképernyő)
- [chooseLiturgyTypeView](views/chooseLiturgyType.md)
- [liturgyView](views/liturgy.md)
- [liturgyOverviewView](views/liturgyOverview.md)
- [weekView](views/week.md)



# Követelmények

Az alábbiakban sok-sok követelmény hangzik el. A jobb átláthatóság és talán a fejlesztést is segítő módon modulokba van szedve. A végfelhasználónak erről semmit nem kell tudnia. A modulok nem kapcsolhatóak külön ki vagy be, nem is kell kódban sem szétválniuk, bár talán érdemes.


## Szíve lelke
- Naptár: [m/calendar](modules/calendar.md) ([must](definitions.md#priorities))
- Liturgikus naptár: [m/liturgicalCalendar](modules/liturgicalCalendar.md) ([must](definitions.md#priorities))
## Liturgikus modulok
- Szentmise
- Húsvét
- Igeliturgia
- Házasság
- Keresztség
- Elsőáldozás
- Bérmálás
- Betegek kenete
- Temetés Funeral liturgy
- Gyászmise
- Szent Rendek
- Templomszentelés
- Preorátor
## Egyéb modulok
- N. szűrő
- Homília
- Export: [m/export](modules/export.md) ([should](definitions.md#priorities))
- Google Naptár Szinkronizáció: [m/googleCalendarSnyc](modules/googleCalendarSnyc.md)  ([should](definitions.md#priorities))
- Kották: [m/melodies](modules/melodies.md) ([could](definitions.md#priorities))
- Minialklamazások: [m/widgets](modules/widgets.md) ([could](definitions.md#priorities))
- Képernyőkímélő: [m/screenSaver](modules/screenSaver.md) ([should / won't](definitions.md#priorities))
- Énekrend: [m/musicListing](modules/musicListing.md) ([won't](definitions.md#priorities))
- Hírdetések: [m/announcements](modules/announcements.md) ([won't](definitions.md#priorities))
- Hívek könyörgése: [m/prayersOfTheFaithful](modules/prayersOfTheFaithful.md) ([won't](definitions.md#priorities))

