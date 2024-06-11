---
title: Building Data Culture and a Better Solution Design Reference
description: Revolutionera datastrategin och ge teamet möjlighet att skapa ett enhetligt dokument för Solution Design Reference (SDR). Eliminera luckor i mätningen och främja en samverkansbaserad datakultur genom stegvisa metoder.
feature: Implementation Basics
topic: Administration
role: User
level: Experienced
doc-type: Article
duration: 72000
last-substantial-update: 2024-04-25T00:00:00Z
jira: KT-15338
thumbnail: KT-15338.jpeg
exl-id: 99fcf68f-5698-4270-9055-ab224e6323a1
source-git-commit: b2e05ff39e065691dda530ed17762a55cf2e6778
workflow-type: tm+mt
source-wordcount: '1647'
ht-degree: 0%

---

# Bygga upp en datamultur och skapa en bättre referens för lösningar

_Revolutionera datastrategin och ge teamet möjlighet att skapa ett enhetligt dokument för Solution Design Reference (SDR). Eliminera luckor i mätningen och främja en samverkansbaserad datakultur genom stegvisa metoder._

Det är äntligen dags. Du har samlat en heltäckande SDR En SDR är den guide du använder för att implementera mått och mått. Du har definierat vad de kallas, när de avfyrar, och dina utvecklare älskar det. Du gick igenom hela driftsättningsprocessen, skrev accepteringskriterier, gick igenom era sprintar, testade den och det är klart! Din instans av [!DNL Adobe Analytics] bör få marknadsförings- och produktteam att fira allt eftersom de fördjupar sig i data, få nya avslöjanden om era kunder och hitta alla områden med framgång och, ja, områden med mindre framgång. Men du hör inte de samtal du förväntade dig.

Från ett team hör ni klagomål som:

&quot;Varför kan jag inte räkna ut konverteringsgraden på den här tratten?&quot;

&quot;Varför finns det inte en mätmetod för det här?&quot;

&quot;Jag behöver fler detaljer! Enbart ett mätresultat räcker inte. Det finns minst tre olika dimensioner som jag behöver för att förstå prestandan. Varför satte du inte in dem?&quot;

Men det är det andra laget som är en ännu större anledning till oro. Från dem hör du ingenting alls. Och ännu värre är att du ser diagram som är tydligt tagna från din gamla analyslösning (den som inte längre underhålls och som varje dag går längre in i en svamp av tillbakadragna och smutsiga data). En känsla av besvär fyller dig när du tänker på vilka beslut som kan fattas med den ursprungliga röran.

_Vad gick fel?_

_Varför finns det brister i mätningen?_

_Varför tar inte dina teammedlemmar till sig det här?_

Jag börjar med att släppa av dig lite. Det finns _alltid_ kommer att bli lite revision. Om er webbplats eller tillämpning är tillräckligt komplex för att behöva en företagsanalyslösning är det garanterat så att ni missar något. Men i det här fallet missade du inte tillräckligt för att förklara mätbristerna jag beskriver.

Det som gick fel är mycket svårare att lägga in i ett kalkylblad. I grund och botten missade du den första chansen att skapa en samarbetskultur för data när du byggde SDR.

Jag vill gå igenom en metod som mina kollegor och jag har utvecklat för att både skapa en bättre SDR med färre luckor och få slutanvändarna att investera (och till och med ibland entusiastiska) i sin nya förekomst av [!DNL Adobe Analytics]. Låt oss gå igenom hur och varför du bör överväga den här metoden.

## Hur

_Läs mer om mätkonferensen. Använd en trattmappning för att visualisera varje steg i planen. Skapa dummypaneler som kan granskas som en grupp. Skapa en dataordlista för användare._

### Mätkonferensen

1. Samla era intressenter, antingen personligen eller praktiskt taget, med målet att ta reda på vad ni ska mäta. Mötet bör innehålla några chefer.
1. Låt redan få tydliga exempel på notislappar som intäkter, försäljning eller leads, så mäts nyckeltal (KPI) som du vet. Upprepa med dimensioner som inloggningsläge, produktkategorier eller söktermer.
1. Låt alla lägga in egna anteckningar och gruppera efter behov.
1. Be folk att rösta på de som de tycker är viktiga. Detta är ett obegränsat antal röster eftersom alla dessa mått och dimensioner antagligen är viktiga.
1. För alla mätvärden och dimensioner som har låga röster, låt de intressenter som frågade efter dem förklara varför de här komponenterna skulle användas. Om det finns ett bra användningssätt bör du behålla dessa komponenter. Om det finns ett bättre sätt att hämta data, eller om ingen kan förklara hur dessa data kan användas, eller om det finns en annan bra anledning att ta bort mätvärden och dimensioner, gör du det.
1. Lägg till dessa värden och dimensioner i SDR för en inledande granskning av de intressenter som var närvarande.

### Trattmappningen

1. Få en visualisering av alla funktioner, steg för steg med alla lägen.
1. Med designers och produktchefer kan du gå igenom varje steg och diskutera vad alla anser vara lyckat i den processen. Är det konverteringsgraden? Väljer den en viss bana? Använder den vissa funktioner?
1. Ställ frågor om vilka mätvärden och dimensioner som krävs för att förstå hur tratten fungerar i varje steg i tratten och i hela processen.
1. Ovanför varje steg i tratten lägger du till mått och mått som mäts i det steget, inklusive beräknade värden.
1. I början av varje tratt skriver du de rapporter som finns på kontrollpanelen och som produktchefen kan använda för att spåra prestandan. Dessa rapporter innehåller [utfallsrapport](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow), [aktuell månad](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges), [trendkonverteringsgrader](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/visualizations/line)och något mer specifikt för den tratten.
1. Lägg till de nya mätvärdena och måtten som du har upptäckt i SDR och skicka dem till intressenterna för en andra granskning.

### Kontrollpanelerna för förhandsgranskning

1. Skapa dummies-paneler med hjälp av trattchemat.
1. Det ska finnas en övergripande vy, som [Instrumentpanel för sammanfattning](driving-success-with-executive-summary-dashboards.md)och kontrollpaneler för varje kanal.
1. Det kommer också att finnas mer specifika för din webbplats eller app, till exempel produktprestanda eller innehållsprestanda.
1. Distribuera dessa till relevanta intressenter och få feedback om designen.
1. Begär uppdateringar och om nya mått eller mått behövs lägger du till dem i SDR:n.
1. Skicka de uppdaterade förhandsvisningspanelerna och SDR för en slutgranskning.

### Datademokratiseringsverktyg

1. Skapa en dataordlista. SDR är till för dina utvecklare, men dataordlistan är till för dina slutanvändare. Gör den läsbar så att alla enkelt kan se vilka data som är tillgängliga och veta hur de används. Slutanvändarna bör vara de sista godkännarna av detta.
1. Anteckna. I alla organisationer finns det vissa datum som räknas varje år och andra som kommer att komma fram. Se till att ni samlar in relevanta datum från era intressenter och lägger till dem som anteckningar för att öka förståelsen för de data de ser.
1. Kuratera. Om din SDR är stor kan den vara överväldigande. Förlamning av valet gäller inte bara dina kunder. Se vad som är viktigt för varje grupp av användare och jämför de element de kommer att se.

## Varför

_Lär dig mer om att samla in krav, bygga upp en datakultur, få djupare insikter om data, skapa en känsla av ägandeskap om data och förenkla data._

### Samla in krav

Det är uppenbart att insamlingskraven är uppfyllda, men det finns flera effektiva sätt att göra det. Jag har använt personliga intervjuer, enkäter och recensioner av befintliga rapporter. Dessa strategier fungerar, men inte så bra som de metoder som jag just beskrivit. Jag anser dock inte att skillnaden mellan metoderna för att samla in krav är betydande. Den metod jag har beskrivit ger dig 95 % av vägen dit och de andra metoderna ger dig 90 % av vägen.

Så vad är _varför_?

### Bygg datakultur

I den här processen:

* Spark djupt funderat på hur man mäter framgång
* Skapa en känsla av ägarskap i era intressenter
* Gör det enklare för intressenter att förstå sina data

### Spark-genomgång av data

För många av era anställda är data något de konsumerar. De använder den. De analyserar det. De tänker inte så djupt på det. Vissa ärver rapporter och processer från sina föregångare, men har inte ändrat dem för kontinuitetens skull. De behövde kanske aldrig tänka på _varför_ av uppgifterna.

Denna process ger dem möjlighet att _förstå_ data. Frågor som: Vad är framgång? Hur skulle du veta om du var framgångsrik? Hur vet du vad du ska ändra om du inte lyckas? Dessa frågor måste besvaras i början av skapandet av alla webbplatser, tillämpningar och produkter - men alltför ofta gör de det inte. Genom att ställa de här frågorna kan du fördjupa en persons förståelse för inte bara data, utan även deras produkt.

### Skapa en känsla av ägarskap över data

En känsla av ägandeskap är inte något som en person lätt förvärvar. Det finns inte på det 30 minuter långa mötet där jag var med för tre månader sedan. Det skapas inte av det irriterande frågeformuläret som de besvarat för snabbt på grund av andra viktiga arbetsproblem som demos och releasedatum.

Äganderätt är produkten av någons djuplodande tanke och deras arbete med dig och dina kollegor. Det är det de har tittat på flera gånger, gett kontinuerlig feedback och vad de har godkänt efter att den feedback de fått har lagts in. Det är deras! Det faktum att det är användbart beror på dem. Det är _sina_ data och det är den processen som gjorde det till deras.

### Förenkla informationen

Du har också visat dem hur de kommer att använda processen och hur den kommer att se ut genom [förhandsgranska instrumentpaneler](#the-preview-dashboards). En ny lösning _hård_. Det finns så mycket att lära sig och med tanke på den enorma anpassningsförmågan hos [!DNL Adobe Analytics]kan inlärningskurvan bli brant. Du har dock tagit bort 80 % av det. Innan den första kodraden har skrivits vet era intressenter hur deras kontrollpaneler kommer att se ut. De kommer att kunna läsa dem och få mening av dem. De vet hur framgången bokstavligen ser ut eftersom de har berättat vilka mätvärden och dimensioner som definierar framgången. Och du har berättat för dem hur framgången kommer att visualiseras. Den faktiska instrumentpanelen är en uppdatering, inte en skrämmande ny inlärningsåtgärd.

Det här är inte nödvändigtvis det snabbaste sättet att få ihop SDR. Det är mycket arbete och kräver mycket samordning av tidsplanerna, särskilt eftersom det är viktigt att du har några chefer i mixen. I slutändan är dock en företagsanalyslösning en stor investering i tid och pengar, och du vill vara säker på att acceptansen och nöjdheten är hög. Den här metoden går långt i riktning mot att få det att hända.

**Upphovsman**

Det här dokumentet har skrivits av:

![gitai-headshot](assets/gitai-headshot-150.jpg)

Gitai Ben-Ammi, Business Architecture Associate Manager på Accenture

[!DNL Adobe Analytics] Champion
