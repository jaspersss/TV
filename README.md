# 📺 TV Dashboard Plattegrond - Buitenzorg

Welkom bij de repository van het **TV Dashboard Buitenzorg**! Deze web-applicatie is speciaal ontworpen als *Narrowcasting* oplossing: een interactief, live bijwerkend scherm voor in de stafruimte of bij de receptie van het scoutcentrum. Met één blik op het grote scherm zie je direct de actuele bezetting van alle velden en gebouwen op de plattegrond.

## 🌟 Wat doet deze app?
De app projecteert dynamische labels over de officiële plattegrond van Buitenzorg (`Plattegrond 2025-2.jpg`). Door op de achtergrond live te koppelen met het Labelbooking systeem (via iCal), weet de TV exact welke groep er op welk veld staat. 

Het is een direct verlengstuk van de beheerders: check je een groep in via de admin? Dan kleurt het bordje op de TV in de gang automatisch groen!

## ✨ Features
* **Kleurgecodeerde Statussen:** * 🟩 **Groen:** De groep is aanwezig (Status: *Ingecheckt*).
  * 🟧 **Oranje:** Het veld is gereserveerd, maar de groep is er nog niet (of moet nog inchecken).
  * ⬜ **Wit:** Het veld is vrij.
* **Slimme Tijd-logica:** Wisselt een veld vandaag van eigenaar? De TV kijkt naar de exacte kloktijd om op het juiste moment de naam op het bordje te veranderen. Kijk je naar morgen of volgende week? Dan neemt hij 14:00 uur als peilmoment.
* **Anti-Overlap Algoritme:** Zelfs als er drie groepen op velden staan die dicht bij elkaar liggen (zoals het Eekhoorntjesbos, Buizerdbos en Beverbos), berekent de app automatisch de posities opnieuw zodat de bordjes als een net stapeltje onder elkaar schuiven en altijd leesbaar blijven.
* **Volledig Scherm Modus (⛶):** Met één druk op de knop rechtsboven verdwijnen alle browserbalken (Chrome/Edge/Safari) voor een perfecte, afleidingsvrije TV-weergave.
* **Auto-Refresh:** Het scherm kan dagenlang aan blijven staan. Het ververst stilletjes op de achtergrond elke 5 minuten én reset zichzelf automatisch rond middernacht naar de nieuwe "Vandaag".

## 🖥️ Gebruik op een TV-scherm
Dit dashboard is een **Single Page Application (SPA)** en draait volledig in de browser.
1. Open de url van deze pagina op de browser van je Smart-TV, of op een mini-pc/Raspberry Pi die aan het scherm is gekoppeld.
2. Klik rechtsboven op de **⛶ (Fullscreen)** knop.
3. Gebruik eventueel de pijltjes (◀ ▶) om alvast vooruit te blikken naar de bezetting van aankomend weekend.

## ⚙️ Configuratie & Kalibratie Tool
Omdat de app over een statische afbeelding (`Plattegrond 2025-2.jpg`) heen tekent, moeten de GPS-coördinaten (percentages) van de velden in de code worden vastgelegd. Dit zit al in de code, maar mocht je in de toekomst een **nieuwe plattegrond** uploaden, dan kun je de velden heel makkelijk opnieuw uitlijnen:

1. Open de TV app in je browser op een computer en zet `?edit=true` achter de URL (bijv. `jouwwebsite.nl/tv.html?edit=true`).
2. Je muis verandert in een dradenkruis.
3. Klik exact in het midden van het veld op de kaart.
4. Er verschijnt een pop-up met de nieuwe, pixel-perfecte coördinaten (bijv. `{ top: "36.9%", left: "23.4%" }`).
5. Kopieer deze en plak ze in het `mapCoordinates` blok bovenaan in de `<script>` sectie van `tv.html`.

## 🛠️ Techniek
- **Talen:** HTML5, CSS3, en Vanilla JavaScript (ES6).
- **Geen externe database:** Alles wordt *on-the-fly* berekend in het geheugen van de browser.
- **Proxy Racing:** Haalt data via 3 proxy-servers tegelijk op om CORS-blokkades te omzeilen met de hoogst mogelijke snelheid.

---
*Gemaakt met ❤️ voor de staf van Scoutcentrum Buitenzorg.*
