# 📺 TV Dashboard Plattegrond - Buitenzorg

Welkom bij het **TV Dashboard Buitenzorg**! Deze narrowcasting web-applicatie projecteert live de bezetting over de officiële plattegrond van het scoutcentrum. Ontworpen om 24/7 op een groot scherm in de receptie of stafruimte te draaien.

## 🌟 Wat doet deze app?
De app tekent dynamische, verschuivende labels over de plattegrond. Door op de achtergrond continu te koppelen met het Labelbooking systeem, weet het scherm exact wie er op welk veld staat, wie er nog moet komen, en wie de dienstdoende kampstaf is.

## ✨ Features

* **Gelijke Kleurenlogica als Mobiel:** Spreekt dezelfde taal als de Terrein App.
  * 🔴 **Rood:** Groep is te laat (incheck/uitcheck).
  * 🟧 **Oranje:** To-do voor vandaag (komt aan of vertrekt vandaag).
  * 🟩 **Groen:** Succesvol ingecheckt.
  * ⬜ **Grijs:** Gepland in de toekomst.
  * ⬜ **Wit (Leeg label):** Terrein is momenteel vrij.
* **Kampstaf Overlay:** Links bovenin zweeft een strak label dat automatisch de voornamen toont van de stafleden die op die dag zijn ingeroosterd.
* **Anti-Overlap Algoritme:** Zelfs als er drie groepen op het Beverbos en Eekhoorntjesbos staan, berekent de app de posities opnieuw zodat de bordjes als een net stapeltje onder elkaar schuiven en altijd perfect leesbaar blijven.
* **Schone Namen & Slimme Tijden:** Boekingsnummers worden verborgen.
* **Interactieve Kalender & Actueel-knop:** Klik op de datum om snel een specifiek weekend in de toekomst te bekijken. Met de knop "Actueel" springt het scherm direct terug naar "Nu" en hervat het de live-klok logica.
* **Volledig Scherm Modus (⛶):** Verbergt browserbalken voor een echte TV-weergave.

## ⚙️ Configuratie & Kalibratie (Nieuwe kaart?)
Omdat de app over een statische afbeelding tekent, moeten de coördinaten (percentages) in de code vastgelegd worden (inclusief *Paul's Plekje*). 
Mocht er een nieuwe plattegrond komen, gebruik dan de ingebouwde kalibratietool:
1. Open de TV app in een browser en voeg `?edit=true` toe aan de URL (bijv. `jouwwebsite.nl/tv.html?edit=true`).
2. Je muis verandert in een dradenkruis.
3. Klik exact in het midden van het veld op de kaart.
4. Er verschijnt direct een pop-up met de juiste `{ top: "...", left: "..." }` code om in `tv.html` te plakken.

---
*Gemaakt met ❤️ voor de staf van Scoutcentrum Buitenzorg.*
