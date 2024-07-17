---
title: Skapa standardiserade kodmallar
description: För en baslinjeimplementering (d.v.s. vad ditt företag anser att nyckeltal måste ha för alla [!DNL Adobe Analytics] platser) bör din organisation ha en enda implementeringsmetod där det är möjligt.
solution: Analytics
feature-set: Analytics
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10532.jpg
kt: 10532
exl-id: edd3df73-6d1a-4a26-a984-810cc7dd382f
source-git-commit: 058d26bd99ab060df3633fb32f1232f534881ca4
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# Skapa standardiserade kodmallar

**VAD:** För en grundläggande implementering (d.v.s. vad ditt företag anser att nyckeltal måste ha för alla [!DNL Adobe Analytics] -platser) bör din organisation ha en enda implementeringsmetod där det är möjligt. Använd till exempel samma datalagerstruktur för olika webbplatser och dra nytta av samma tagghanteringsregel/anpassade kod för att hämta information som interna sökningar eller besökarprofilinformation.

**VARFÖR:** Om du har en repeterbar och skalbar baslinjeimplementering blir det enkelt att lägga till nya element eller nya webbplatser/appar, vilket är en smidig och enkel åtgärd, samtidigt som implementeringen är rensad och enkel att felsöka. Genom att använda en enhetlig metod blir det också enklare för nya administratörer och utvecklare att komma ut på webben och förstå vad de arbetar med.

**HUR:** Använd en mall för ett format som ska skickas till utvecklare när en ny webbplats eller taggningsförbättring är online. Vanligtvis fungerar ett orddokument bra där du kan göra en disposition av följande objekt:

* Variabler implementeras, deras syfte och när de ska anges. Exempel:

| AA-variabel | Beskrivning | Ange när/var | Ange hur |
|--- |--- |--- |--- |
| eVar8 | Interna söknyckelord | Vid landning av intern sida för sökresultat | datalager |
| event8 | Antal interna sökningar | Vid landning av intern sida för sökresultat | Startregel |

* Detaljinfo om hur du ställer in. Här anger du eventuella datalagerobjekt som behövs och deras syntax samt eventuella TMS-regler som behöver konfigureras och information om regelkonfigurationen.
* Testfall för att säkerställa att de täcks av kvalitetskontrollen och alla variabler som du förväntar dig att se i ett lyckat testfall. Ange vilken implementering som ska ingå när utvecklaren testar den här förbättringen.

Helst behöver det här dokumentet bara ändras för nästa webbplats där du uppdaterar grunderna som egenskapsnamn, sidnamnskonvention osv. Du behöver inte förnya hjulet varje gång, och du kan spara mer tid.

## Författare

Det här dokumentet skrevs tillsammans av:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digital [!DNL Analytics] Platform Manager på NortonLifeLock
[!DNL Adobe Analytics] Champion

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, Senior Consultant på [!DNL Adobe]
