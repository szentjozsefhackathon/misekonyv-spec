# Calendar = Naptár

Bármely naptári naphoz tartozhat egy vagy sok liturgia. Egy-egy ilyen bejegyzéshez menteni kell az esemény nevét, megfelelő adatait (intenció, nevek, stb), extra adatokat, ha vannak. És minden beállítást is.

Ehhez használ(hat)ja a beépített android naptárat.

### f-settingsString (could)

A beállításokat standard naptári szövegmezőbe is egy max kb 8-10 karakteres stringben kódolni. A kód alapján bármelyik másik alkalmazás is fel kell tudja oldani a megfelelő beállításokat. Ez biztosíthatja több kütyü szinkronizálását [m-GCalendarSync](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.82gt9abgiysj) esetén. 

Ezért szükséges, hogy minden (!) beállítás le legyen benne mentve, ne csak a defaul-tól eltérés.

|                                          |      |
| ---------------------------------------- | ---- |
| [priority](../definitions.md#priorities) | must |
| dependency                               | -    |
| [v/appSettings](../views/appSettings.md) | -    |

