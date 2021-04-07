# nFilter = Az "N."-ek feloldása

Liturgiák szövegeiben előfordul, hogy konkrét név helyett egy piros N. betű áll. Plédául: “[...] N. pápánkről, N. püspökünkről és az egész papságról.” Ezeket kell automatikusan kitölteni megfelelő adattal.

- A liturgiákban szereplő összes piros N. betűt helyettesítse be a felhasználó által megadott szöveggel. Ha nincs ilyen, maradjon meg piros N.-nek.

- Javaslat: a szövegforrásban (see: [Adatformátumok és adatforrások](../README.md#adatformátumok-és-adatforrások)) valamilyen módon legyen jelezve, hogy ez milyen N. betű. (Például: pápa, püspök(ök), elhunyt(ak), jegyesek, elsőáldozók, stb.)

- Az egyes liturgia előállításakor kell rákérdezzen ezekre az adatokra (see: [v/liturgyOverview](../views/liturgyOverview.md)). Egy részük (pápa, püspök) default értékkel is rendelkezik az [v/appSettings](../views/appSettings.md)ben. A lehetséges N-ek (a pápán és püspökökön) túl jelenleg az [Extra misék](mass.md#extra-misék) struktúrjából derül ki.

  > Todo: Szentek N. ezése esetén valahogy tudni kell rövidítettet is csinálni. Mert időnként baromi hosszú a szentek akármilyének nevei.

- A [hívek könyörgésé](prayersOfTheFaithful.md)ben is lehetnek N.-es részek. Akár pápás, főpásztoros. Akár elhunytért. Akár szentek esetén 

  > Todo: ezeket a lehetséges N-eket konkrétan összeírni. Talán az egyes modulokhoz.



|                                          |        |
| ---------------------------------------- | ------ |
| [priority](../definitions.md#priorities) | should |
| dependency                               | ?      |
| [v/appSettings](../views/appSettings.md) | -      |

