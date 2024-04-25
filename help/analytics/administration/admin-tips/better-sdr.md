---
title: Bygga upp en datamultur och skapa en bättre referens för lösningar
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
source-git-commit: 07b28edade263aa3c85348716bd45df4a053e239
workflow-type: tm+mt
source-wordcount: '1640'
ht-degree: 0%

---


# Bygga upp en datamultur och skapa en bättre referens för lösningar

**Revolutionera datastrategin och ge teamet möjlighet att skapa ett enhetligt dokument för designreferens (SDR). Eliminera luckor i mätningen och främja en samverkansbaserad datakultur genom stegvisa metoder.**

Det är äntligen dags. Du har samlat en heltäckande SDR (Solution Design Reference). Det här är guiden som du använder för att implementera mått och mått, vad de kallas, när de avfyras och dina utvecklare älskade det. Du gick igenom hela driftsättningsprocessen, skrev accepteringskriterier, gick igenom era sprints, QAing the entire, och det är klart! Det var mycket arbete, och nu är det klart. Er instans av Adobe Analytics bör vara att få marknadsföringen och produkterna att komma upp och ner när de fördjupar sig i data, få nya avslöjanden om era kunder och hitta alla områden med framgång och, ja, områden med mindre framgång. Men du hör inte de samtal du förväntade dig.

Du hör klagomål från ett läger.

&quot;Varför kan jag inte räkna ut konverteringsgraden på den här tratten?&quot;

&quot;Varför finns det inte en mätmetod för det här?&quot;

&quot;Jag behöver mycket mer information om det här! Enbart ett mätresultat räcker inte. Det finns minst tre olika dimensioner som jag behöver för att förstå prestandan. Varför satte du inte in dem?&quot;

Men det är det andra lägret som är en ännu större anledning till oro. Från dem hör du ingenting alls. Men ännu värre är att du ser diagram som är mycket tydligt tagna från er gamla analyslösning, du vet, den som inte längre underhålls, och varje dag går allt längre in i en svamp av tillbakadragna och smutsiga data. En känsla av bedrövelse fyller dig när du tänker på de beslut som kan fattas i den röran.

Vad gick fel? Varför finns det brister i mätningen? Varför tar inte dina teammedlemmar till sig det här?

Jag börjar med att släppa av dig lite. Det finns *alltid* kommer att bli lite revision. Om er webbplats eller app är tillräckligt komplex för att behöva en företagsanalyslösning är det i princip säkert att ni kommer att sakna någonting. Men inte tillräckligt för att förklara mätbristerna här. Det som gick fel är mycket svårare att lägga in i ett kalkylblad. Du missade chansen att skapa en datakultur i samarbete samtidigt som du skapade SDR. Jag vill gå igenom en metod som jag och mina kollegor har utvecklat för att både bygga en bättre SDR med färre luckor och få slutanvändarna att investera och ibland även bli entusiastiska över sin nya förekomst av Adobe Analytics. Vi går igenom hur man gör.

**Hur**

***Mätningskonferensen:***

1. Samla era intressenter, antingen personligen eller i stort sett med målet att ta reda på vad ni ska mäta. Detta bör innehålla några exekveringar.
1. Jag har redan några tydliga exempel på notislappar, t.ex. intäkter, försäljning eller leads, som är viktiga nyckeltal som du vet kommer att mätas. Upprepa med dimensioner, t.ex. inloggningsläge, produktkategorier eller söktermer.
1. Låt alla lägga in egna anteckningar och gruppera efter behov
1. Låt folk rösta på de som de tycker är viktiga. Det här är ett obegränsat antal röster eftersom alla dessa mått och dimensioner kanske är viktiga.
1. För alla som har låga röster, låt de intressenter som frågade efter dem förklara vad de kommer att använda dem till. Om det finns ett bra användningsexempel, håll det i. Om det finns ett bättre sätt att få fram data, kan de inte förklara hur det går att agera, eller det finns en annan bra anledning att utelämna den, slå den ur styrelsen.
1. Lägg till dessa värden och dimensioner i SDR för en inledande granskning av de intressenter som var närvarande

***Tratt Map***

1. Få en visualisering av alla funktioner, steg för steg med alla lägen
1. Med designers och produktchefer går du igenom varje steg och talar igenom vad de anser vara bra med den processen. Är det konverteringsgraden? Väljer den en viss bana? Använder den vissa funktioner?
1. Ställ frågor om vilka mätvärden och dimensioner som krävs för att förstå hur tratten fungerar i varje steg i tratten och i hela processen.
1. Ovanför varje steg i tratten lägger du till mått och mått som ska mätas i det steget, inklusive beräknade värden.
1. I början av varje tratt skriver du de rapporter som kommer att finnas på kontrollpanelen och som produktchefen ska använda för att spåra prestanda, t.ex. en falloutrapport, aktuell månad och trendkonverteringsgrad samt annat som är mer specifikt för den tratten.
1. Lägg till de nya mätvärdena och måtten som du har upptäckt i SDR och skicka dem till intressenterna för en andra granskning.

***Kontrollpanelerna för förhandsgranskning***

1. Använd Funnel Map som guide för att skapa dummies-paneler.
1. Det ska finnas en övergripande vy, till exempel en instrumentpanel för sammanfattning av den verkställande informationen och instrumentpaneler för varje kanal.
1. Det kommer också att finnas mer specifika för din webbplats eller app, till exempel produktprestanda eller innehållsprestanda.
1. Distribuera dessa till relevanta intressenter och få feedback om designen.
1. Begär uppdateringar och om nya mått eller mått behövs lägger du till dem i SDR:n.
1. Skicka de uppdaterade förhandsvisningspanelerna och SDR för en slutgranskning.

***Verktyg för datadekryptering***

1. Skapa en datamordlista. SDR är till för dina utvecklare. Dataordlistan är till för slutanvändarna. Gör det läsbart för slutanvändare så att de enkelt kan hitta tillgängliga data och veta hur de ska använda dem. Slutanvändarna bör vara de sista godkännarna av detta.
1. Anteckningar. I alla organisationer finns det vissa datum som räknas varje år och andra som kommer att komma fram. Se till att ni samlar in relevanta data från era intressenter och lägger till dem som anteckningar för att öka förståelsen för de data de ser.
1. Kuration. Om din SDR är stor kan den vara överväldigande. Förlamning av valet gäller inte bara dina kunder. Se vad som är viktigt för varje grupp av användare och jämför de element de kommer att se.

**Varför**

***För att få***

Detta är uppenbart, men det finns andra effektiva sätt att skaffa sig krav. Jag har personligen använt en på en intervju, enkäter och recensioner av befintliga rapporter. Det kommer att fungera, även om jag inte tycker så bra om de metoder jag just har beskrivit. Jag tror inte att klyftan i kravsammanställningen är så stor. Den metod jag har beskrivit ger dig 95 % av vägen dit och de andra metoderna ger dig 90 % av vägen. Så, varför är det så stort?

***Att skapa dataskultur***

Med den här processen kan du

- Spark djupt funderat på hur man mäter framgång
- Skapa en känsla av ägarskap i era intressenter
- Gör det enklare för intressenter att förstå sina data

***Sparkar djupa tankar om data***

För många av era anställda är data något de konsumerar. De använder den. De analyserar det. De tänker inte så djupt på det. Vissa av dem ärvde rapporter och processer från sina föregångare som de inte har förändrat på grund av behovet av kontinuitet. De har aldrig behövt tänka på varför informationen finns.

Denna process ger dem möjlighet att *förstå* data. Fråga vad som är framgång? Hur skulle du veta om du var framgångsrik? Hur vet du vad du ska ändra om du inte lyckas? Det här är en övning som bör göras i början av skapandet av alla webbplatser, appar och produkter, men det gör det inte alltför ofta. Genom att ställa de här frågorna kan ni fördjupa deras förståelse för inte bara data, utan även deras egen produkt.

***Skapa en känsla av äganderätt till data***

Det här är inte något som man har gett ifrån sig. Det här är inte något som var ett trettio minuter långt möte för tre månader sedan. Det är inte det irriterande frågeformuläret som de blev lurade på en vecka för att svara och som de gjorde så snabbt eftersom de hade en demo att ta sig till så att de kunde få ut releasedatum. Detta är resultatet av deras djupa tanke och deras arbete med dig och deras kollegor, som de har tittat på flera gånger, gett kontinuerlig feedback och som de har godkänt efter att denna feedback har tagits med. Det är deras! Det faktum att det är användbart beror på dem. Det är *sina* data och det är processen som gjorde det till deras.

***Förstå data enklare***

Du har också visat dem hur de kommer att använda den och hur den kommer att se ut via förhandsvisningens kontrollpaneler. En ny lösning *hård*. Det finns så mycket att lära och med tanke på Adobe Analytics enorma anpassningsmöjligheter kan inlärningskurvan bli ganska brant. Du har dock tagit bort 80 % av det. Innan den första kodraden har skrivits vet era intressenter hur deras kontrollpaneler kommer att se ut. De kommer att kunna läsa dem och få mening av dem. De vet hur framgången bokstavligen ser ut eftersom de har berättat vilka mätvärden och dimensioner som definierar framgång och du har berättat för dem hur det kommer att visualiseras för dem. Den faktiska instrumentpanelen är en uppdatering, inte en skrämmande ny inlärningsåtgärd.

Det här är inte det snabbaste sättet att få ihop en SDR. Det är mycket arbete och kräver en hel del samordning av tidsplanerna, särskilt eftersom det är viktigt att du har några chefer i mixen. I slutänden är en företagsanalyslösning en enorm investering i tid och pengar, och du vill vara säker på att acceptansen och nöjdheten är hög. Den här metoden går långt i riktning mot att få det att hända.

**Upphovsman**

Det här dokumentet har skrivits av:

![gitai-headshot](assets/gitai-headshot-150.jpg)

Gitai Ben-Ammi, Business Architecture Associate Manager på Accenture

Adobe Analytics Champion

