# nFilter = Az "N."-ek feloldása

Liturgiák szövegeiben előfordul, hogy konkrét név helyett egy piros N. betű áll. Plédául: “[...] N. pápánkről, N. püspökünkről és az egész papságról.” Ezeket kell automatikusan kitölteni megfelelő adattal.

- A liturgiákban szereplő összes piros N. betűt helyettesítse be a felhasználó által megadott szöveggel. Ha nincs ilyen, maradjon meg piros N.-nek.

- Javaslat: a szövegforrásban (see: [Adatbázis - szövegforrás](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.kz5p7s6kd98w)) valamilyen módon legyen jelezve, hogy ez milyen N. betű. (Például: pápa, püspök(ök), elhunyt(ak), jegyesek, elsőáldozók, stb.)

- Az egyes liturgia előállításakor kell rákérdezzen ezekre az adatokra (see: [liturgy overview view](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.drdnoaqmzos7)). Egy részük (pápa, püspök) default értékkel is rendelkezik az [app-settings](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.fvmxvlofvf63)-ben. A lehetséges N-ek (a pápán és püspökökön) túl jelenleg az [Extra misék](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.tuyp4zs6rxh6) struktúrjából derül ki.

  > Todo: Szentek N. ezése esetén valahogy tudni kell rövidítettet is csinálni. Mert időnként baromi hosszú a szentek akármilyének nevei.

- A [hívek könyörgésé](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.5bwixieinq6t)ben is lehetnek N.-es részek. Akár pápás, főpásztoros. Akár elhunytért. Akár szentek esetén 

  > Todo: ezeket a lehetséges N-eket konkrétan összeírni. Talán az egyes modulokhoz.



|                                          |        |
| ---------------------------------------- | ------ |
| [priority](../definitions.md#priorities) | should |
| dependency                               | ?      |
| [v/appSettings](../views/appSettings.md) | -      |

