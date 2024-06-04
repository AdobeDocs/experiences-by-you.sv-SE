---
title: Organisera en ny instans och upprätta namnkonventioner
description: Lär dig hur du skapar en bra organisation i din Marketo Engage-instans så att framtida marknadsförare i din organisation enkelt kan navigera bland programmen, ändra resurserna och hämta rapporter.
role: Admin
level: Beginner
doc-type: Article
duration: 0
last-substantial-update: 2024-05-03T00:00:00Z
jira: KT-14813
thumbnail: KT-14813.jpeg
source-git-commit: 849a0022ea3a64ad964c9d2fc368b4b79b9c0cfa
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 0%

---

# Organisera en ny instans och upprätta namnkonventioner

Som administratör som implementerar en ny instans i Marketo Engage lägger du grunden så att framtida marknadsförare i organisationen enkelt kan navigera genom instansen. Om du bekantar dig med trädmappens struktur och namnkonventioner håller du instansen uppdaterad och kan förbereda dig för att lyckas på lång sikt. Den här självstudiekursen innehåller exempel som rekommenderas av Adobe och Marketo Engage Champion (2019-2020), Natalie Kremer, som kan hjälpa dig [ordna mapparna och namnge resurserna på ett konsekvent sätt](https://nation.marketo.com/t5/champion-program-blogs/keep-marketo-engage-organized-with-folders-and-naming/ba-p/245630){target="_blank"}.

## Varför är det nödvändigt att strukturera mappar och tillämpa namnkonventioner?

Genom att hålla ordning i instansen blir det enkelt för dig och dina kollegor att hålla reda på kampanjer, program och resurser samt rapportera programresultat. Om du vill ordna navigeringsträdet i instansen och bygga i skala bör du använda [mappar](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/understanding-folders){target="_blank"}, [standardnamnkonventioner](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/programs/working-with-programs/best-practice-how-to-organize-your-programs#naming-schemes){target="_blank"}och funktioner som [kloning](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/programs/working-with-programs/best-practice-how-to-organize-your-programs#cloning){target="_blank"}.

## Organisera en Marketo Engage-instans

>[!VIDEO](https://video.tv.adobe.com/v/3421577/?quality=12&learn=on)

### Steg 1 - Konfigurera en mappstruktur för att ordna dina program

Det första steget för att ordna instansen är att [konfigurera en mappstruktur](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/create-new-campaign-folder.html) lagra program och resurser på ett enkelt och ordnat sätt.

Här följer några snabba tips när du strukturerar mapparna i trädet:

* Bevara en platt mappstruktur för upptäckbarhet.
* Strukturera dina mappar så att de återspeglar din organisations teamstruktur (t.ex. region eller team) eller initiativ (t.ex. nyhetsbrev).
* Lägg in tidsbaserade etiketter som möjliggör sökbarhet och signalerar lämplig tidpunkt för arkivering (t.ex. 2024).
   * Administratörer rekommenderas att arkivera mappar minst en gång per år. Om du använder ett årligt mappnamn kan du enkelt inaktivera smarta kampanjer i realtid och arkivera hela mappen i slutet av året.

Nedan finns mappexempel på hur man implementerar dessa tips.

**Mappnamn i träd**

>[!BEGINTABS]

>[!TAB Marknadsföringsaktiviteter]

![Marknadsföringsaktiviteter för mappar](/help/marketo-tutorial-implementing-new-instance/assets/folders-marketing-activities.png)

>[!TAB Design Studio]

![Mappdesign Studio](/help/marketo-tutorial-implementing-new-instance/assets/folders-design-studio.png)

>[!TAB Databas]

![Mappdatabas](/help/marketo-tutorial-implementing-new-instance/assets/folders-database.png)

>[!ENDTABS]

### Steg 2 - Skapa mappar i programmen

Nu ska vi använda mappstrukturen på programnivå. Det är en god vana att lagra de lokala resurserna i undermappar så att du kan hålla programmen uppdaterade och ge interna användare möjlighet att ändra eller rapportera om programmen på ett effektivt sätt. Vanliga undermappar är e-post, landningssidor, smarta kampanjer, listor, rapporter osv.

**Mappnamn inuti program**
* Kampanjer - *Mapp för alla kampanjer som hanterar interaktioner och statusspårning.*
* Lokala resurser - *Mapp för alla resurser som är specifika för programmet.*
   * E-post
   * Landningssidor
   * Smarta kampanjer
   * Listor - *Behövs endast när det finns programspecifika listor.*
   * FORMS - *Krävs endast när det finns programspecifika Forms; de flesta Forms är Global Assets.*
   * Rapporter - *Behövs endast när det finns programspecifika rapporter.*

### Steg 3 - Skapa namnkonventioner för program och resurser

När du har mappstrukturen i trädet vill du ge programmen och resurserna ett konsekvent namn. Detta är när det skulle vara praktiskt att standardisera namnkonventioner för att skala upp namnprocessen internt. Här är några komponenter som du kan använda för att skapa en namnkonvention som säkerställer sökbarheten:

* Programtypsförkortning - e-post, innehåll, struktur, webbinarium osv.
* Kategori - Typ av program - fristående e-post, nyhetsbrev osv.
* Datum - startdatum för program
* Kort beskrivning - kortfattad beskrivning av programmet

Låt oss nu lägga in värdena i formeln och generera programnamnen för olika programtyper.

#### Programnamnsformel

| **Förkortning av programtyp** | **YYYY** | **\-** | **MM** | **\-** | **DD (valfritt)** | **Kategori** | **\-** | **Kort beskrivning av programmet** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| EM - Skicka e-post (e-postprogram) | YYYY | \- | MM | \- | DD (valfritt) | Kategori | \- | Kort beskrivning av programmet |
| NL - nyhetsbrev | YYYY | \- | MM | \- | DD (valfritt) | Kategori | \- | Kort beskrivning av programmet |
| ENG - Engagement Program | YYYY | \- | MM | \- | DD (valfritt) | Kategori | \- | Kort beskrivning av programmet |
| WBN - webbinarium | YYYY | \- | MM | \- | DD (valfritt) | Kategori | \- | Kort beskrivning av programmet |
| IW - interaktivt webbinarium | YYYY | \- | MM | \- | DD (valfritt) | Kategori | \- | Kort beskrivning av programmet |
| TS - Tradeshow | YYYY | \- | MM | \- | DD (valfritt) | Kategori | \- | Kort beskrivning av programmet |
| LE - Live Event (Roadshow) | YYYY | \- | MM | \- | DD (valfritt) | Kategori | \- | Kort beskrivning av programmet |
| UG - Användargrupp | YYYY | \- | MM | \- | DD (valfritt) | Kategori | \- | Kort beskrivning av programmet |
| WC - Webbplatsinnehåll | YYYY | \- | MM | \- | DD (valfritt) | Kategori | \- | Kort beskrivning av programmet |
| CS - Innehållssyndikering | YYYY | \- | MM | \- | DD (valfritt) | Kategori | \- | Kort beskrivning av programmet |
| LI - Importera lista | YYYY | \- | MM | \- | DD (valfritt) | Kategori | \- | Kort beskrivning av programmet |
| OA - Online Advertising | YYYY | \- | MM | \- | DD (valfritt) | Kategori | \- | Kort beskrivning av programmet |
| PPC - Betala per klick | YYYY | \- | MM | \- | DD (valfritt) | Kategori | \- | Kort beskrivning av programmet |

| **Exempel** |
| --- |
| ES 2023-10 Gated Content - XYX Whitepaper |
| WC-2023-10 - Monthly Webinar - ABC Case Study |

#### Formel för namngivning av tillgångar

Om du går en nivå ned till att namnge resurser är det bäst att du inte upprepar programnamnet och använder korta och generiska identifierare för framtida kloningsanvändning. Här följer några snabba tips som du kan tänka på:

* Numrera resurserna baserat på deras sekvens i programprocessen.
* Använd &quot;-&quot; (bindestreck) för att separera namnkomponenterna i stället för &quot;.&quot;(punkt) eller &quot;\_&quot;(understreck).
   * Varför? Marketo Engage använder en punkt för att skilja programnamnet från kampanjnamnet. Om du använder &quot;\_&quot; kan du inte se den när resursen är hyperlänkad.
* Använd standardakronymer i resursnamnen för att korta ned referensen och ändå göra det enkelt att identifiera.

Med dessa tips kommer vi att använda för följande resurser och skapa formler för att generera namn:

##### Namnge resurser baserat på sekvens i programprocessen

| **Sekvens i programprocess** | **\-** | **Beskrivning** |
| --- | --- | --- |
| 01 | \- | Beskrivning |
| 02 | \- | Beskrivning |
| 03 | \- | Beskrivning |

| **Exempel: Smart List** |
| --- |
| 01-Skicka e-post |
| 02-Öppnad |
| 03-klickad |
| 04-ifyllt formulär |
| 05-Påverkade (lyckade program) |
| 06-Avbeställ |

##### Namnge resurserna med en förkortning av resurstypen

| **Förkortning av tillgångstyp** | **Resurstyp** | **\-** | **Beskrivning av mål** |
| --- | --- | --- | --- |
| LP - landningssida | LP | \- | Beskrivning av mål |
| E-post - e-post (utgående) | E-POST | \- | Beskrivning av mål |
| VARNING - E-postavisering | VARNING | \- | Beskrivning av mål |
| WF - Webbformulär | WF | \- | Beskrivning av mål |
| EXCL - Uteslutningslista | EXCL | \- | Beskrivning av mål |
| SLST - smart lista | SLST | \- | Beskrivning av mål |
| LST - statisk lista | LST | \- | Beskrivning av mål |

| **Exempel** |
| --- |
| LP-registrering |
| LP-TackYou |
| EMAIL - utgående |
| EMAIL - nyhetsbrev |
| EMAIL-Invitation |
| E-POST-påminnelse |
| EXCL-Konkurrenter |

##### Namnge de nedladdningsbara filerna (.pdf) med en förkortning av resurstypen

| **Resurstyp** | **Innehållsbeskrivning** | **\-** | **Förkortning av tillgångstyp** | **.** | **PDF** |
| --- | --- | --- | --- | --- | --- |
| WP - rapport | Innehållsbeskrivning | \- | WP | . | PDF |
| CS - Fallstudie | Innehållsbeskrivning | \- | CS | . | PDF |
| DS - Datablad | Innehållsbeskrivning | \- | DS | . | PDF |

| **Exempel: hämtningsbara PDF-filer** |
| --- |
| XYZ-Gadget-DS.pdf |
| Acme-Company-CS.pdf |
| How-XYZ-Gadgets-make-life-easier-WP.pdf |

>[!CAUTION]
>
>När du namnger filer i exemplen ovan ska du inte använda blanksteg och undvika understreck &quot;\_&quot;

## Vad händer nu?

* Hämta kalkylbladet: [Marketo Engage organisations- och namngivningskonventioner](./assets/adobe-marketo-engage-organization-and-naming-conventions.xlsx){target="_blank"} som har stöd för att skapa mappstrukturen och namnkonventioner.
* När du har hittat de nödvändiga komponenterna i den vanliga namnkonventionen bör du överväga att skapa formler i en Google-mall eller i Microsoft Excel. För framtida bruk behöver du bara ange dina värden i kalkylbladet för att generera programnamnen.
* När ni väl har anpassat er efter en övergripande mappstruktur är det dags att fundera igenom de mallar ni behöver utifrån de vanligaste användningsfallen och de vanligaste förfrågningarna som teamet får. Börja sedan att skapa din första programmall. Läs vidare för att komma igång med [Adobe Marketo Engage programmallar](https://business.adobe.com/blog/how-to/get-started-with-marketo-engage-program-templates){target="_blank"}.

### Författare

{{natalie-kremer}}

{{amy-chiu}}