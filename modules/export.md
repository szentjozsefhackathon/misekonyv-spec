Export
===
Amikor éppen [v/liturgy](../views/liturgy.md) nézetben vagyunk, akkor a [v/menu](../views/menu.md)ből az egész liturgiát lehessen kiexportálni és standard megosztási lehetőségekkel pl. emailben elküldeni. 

- Egyetlen fájllá generálás amiben már nincsenek interaktív elemek. (Pl. [m/melodies](melodies.md) esetén nincs hangjegy ikon.)
- Fájlformátum: 
  - docx/rtf ([should](../definitions.md#priorities)) - Mert sokszor utólag még szeretnék módosítani a megjelenést és kihúznak felesleges részeket.
  - pdf ([should](../definitions.md#priorities)) - Hogy legyen meg tényleg szépen is.

- #### pagebreak ([should](../definitions.md#priorities))
    Külön figyelni kell arra, hogy az oldaltörések a lehető legoptimálisabban legyen. Ugyanúgy mint a [v/liturgy](../views/liturgy.md) nézetben. Részeletes leírás ott.

|||
| --- | --- |
| [priority](../definitions.md#priorities) | should |
| dependency | [m/mass](mass.md) |
| [v/appSettings](../views/appSettings.md) | - |