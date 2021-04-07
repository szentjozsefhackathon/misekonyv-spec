# readings = Olvasmányok 

Az [Adatbázis - szövegforrás](https://docs.google.com/document/d/1yxp0r2gVRcalQ8xiSsZ1fPsDkON7amSRdyOulyMM_Rg/edit?ts=606cc879#heading=h.kz5p7s6kd98w)hoz segítségül formai definíciók, a nyomtatott könyvek alapján. 

- Nem kötelező érvényű adatstruktúra. 

```json
{ 
"összetett azonosító": "advent, 1. hét, hétfő [lehet ez dátum is ünnepek esetén, meg sok minden]",
"olvasmányok" : [ 
      [ 
          {
            "olvasmány/szentlecke/evangélium" : "olvasmány [generálható a “ref”-ből]",
            "ref" : "Iz 2, 1-5",
            "intelem bevezető magyarázó szöveg" : "A próféta azzal vigasztalta a népet …. [sortörés lehetséges]",
            "felszólítás": "OLVASMÁNY Izajás próféta könyvéből [generálható a “ref”-ből]",
            "rövid bevezető" : "Eljövendő országában minden népet összegyűjt az Úr",
            "text" : "Izajásnak, Ámosz fiának látomása…” [bekezdések, versek, dőlt, kiemelt]",
            "lezárás": "Ez az isten igéje [generálható az “olvasmány/szentlecke/evangélium”-ból]"
          },
          {
            "orDescription": " “A” évben a következőt olvashatjuk az előbbi olvasmány helyett:",
            "orGépi": " if year = “A”  [valahogy a gép tudja értelmezni ezt az opciósságot]",
            "olvasmány/szentlecke/evangélium" : "olvasmány",
            "ref" : "...",
            "bevezető magyarázó szöveg" : "...",
            "felszólítás": "...",
            "rövid bevezető" : "...",
            "text" : "...",
            "lezárás": "..."
          } 
      ],
      { 
            "olvasmány/szentlecke/evangélium" : "olvasmány",
            "ref" : "Mt 8,5-11.15-18",
            "bevezető magyarázó szöveg" : "...",
            "felszólítás": "...",
            "rövid bevezető" : "...",
            "text" : "...",
            "lezárás": "..."	
      }
	],
"válaszos zsoltár" : {
    "ref": 	"121, 1-2. 3-4a. (4b-5. 6-7.) 8-9",
    "tónus":	"7 b. tónus [Lehet ilyen is: “1 D2. tónus.”]",
    "válasz" : "Isten házába indulunk, * örömtől dobban a szívünk [fontos az aláhúzás, csillag, kereszt, esetleg dőlt betű. Az énekléshez adnak útmutatót]",
    "válaszRef": "1. vers [másutt: “Vö: 7.vers”",
    "versek" : [ 
      {
      	"text": "Örvendeztem, amikor azt mondták nekem, * az Úr házába megyünk. \n
      Íme, itt állunk már kapuid előtt, * kapuid előtt, ó Jeruzsálem. [azaz aláhúzott, dőlt, csillag, kereszt, új sor (akár több is)"  
      }, 
  		{
      	"text" : "...",
      	"optional": "true [vannak zájójelben versek időnként. ha egymás után több, azt egybe kell venni]"
      }
    ]
},
"alleluja [nagyböjt kivételével]" : {
    "dallam" : "2. szám” [nem azonos a tónussal bár kapcsolatban vannak]",
    "tónus" : "2. tónus", 
    "ref" : "Vö. Zsolt 7ö, 4",
    "text": "… [itt is csillag, kereszt, aláhúzás, dőlt]"
},
"evangélium előtti vers [nagyböjtben]" : {
	"Todo": "ezt átgondolni. Mert túl sok opciót sem jó egyszerre megadni. Lásd: Olvasmányoskönyv köznapokra I, p148" 
}
}
```

A text formázása:

- általában sima <p></p> (első sor behúzása, előtte-utána nincs térköz) megoldja
- de van amikor fordítva: verses szerű rész, ahol a két soros ütemben mindig a második kell legyen kicsit behúzva legyen. Kérdés: *ott <p class="poem"> legyen?*
  Lásd pl. : évközi 25. hét szombat ii. év, (olvasmányoskönyv köznapok II, p519).
- vagy van, amikor egymás után sok behúzott kell. ezt megoldja jelenleg, ha soronként <p></p>, de nem elegáns. Például: évközi 26. hét, ii. év (olvasmányoskönyv köznapok II, p526)
- Sőt a verses szerű részen belül is lehetnek bekezdések, megint másmilyen behúzással: pl évközi idő 33. hét, kedd, I. év. (Olvasmányoskönyv köznap II, p727)
- További változatnak tűnik: évközi 34. hét, szerda, II. év. (Olvasmányoskönyv köznap II, p 767)
- Idézet kiemelve előtte utána térközzel: b év húsvéthétfő olvasmányoskönyv vasárnap b év p144
- be + behúzás. talán új: gyümölcsoltó boldogasszony (olvasmányoskönyv, vasárnap, b év, p354
- Dőlt betűs beszúrások, de csak nagyon ritkán.
  - Virágvasárnap (Olvasmányos könyv, vasárnap b év, p 92, Cév p93, a év p139 - A felvezés itt más! (Evanglium xy könyvéből helyett: “A mi urunk jézus krisztus kínszenvedése x y szerint)
  - Nagypénteken (Olvasmányos könyv, vasárnap a év p 156, b év, p 115, c év p115) (Evanglium xy könyvéből helyett: “A mi urunk jézus krisztus kínszenvedése x y szerint)
  - plusz ezeknél: “(Most térder borulunk és egy keveset csendben időzünk.)”



Fontos, hogy az olvasmányok, alleluja, zsoltár, zsoltár válasza(!), vagy az egész egység

- Tartalmazhat több elemet is. Ezek olykor szabadon választottak, olykor conditional, olykor conditional-al szabadon választhatóak.
  - Extra conditional: húsvét vasárnap “Vagy más evangélium, este mondott szentmisére” Olvasmányoskönyv, vasárnap, a év 182, b év, p140, c év 141 (és lehet mondani a vigília evangéliumát is), 
- Lehetnek hivatkozások is valahol másutt definiált elemre. Például nagyböjt iii. iv, v. vasárnapján: “vagy vehető minden az A évről [ottani nagyböjt v. vasárnapjáról]”. Vagy december 17-től 24-ig a standard alleluja mellett van naponként egy-egy ami szabadon választható. (Lásd Olvasmányoskönyv köznapokra p87)

Fontos, hogy az olvasmányok bármelyik tartalmazhat hosszabb és rövidebb formát.

Kérdés: évközi időben köznapokra I. évben és II. évben különbözik az olvasmány/szentlecke és a zsoltár, de azonos az alleluja és az evangélium. Szedjük két külön fájlba, vagy legyen inkább egy “inYear1” és “inYear2” opciós szétválasztás?