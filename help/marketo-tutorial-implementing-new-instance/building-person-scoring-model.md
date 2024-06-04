---
title: Skapa personbedömningsmodeller för program i Marketo Engage
description: Med Adobe Marketo Engage kan du bygga upp din poängmodell(er) från grunden. Innan du går direkt i Marketo Engage för att bygga upp dina poängprogram måste du skapa viktiga poängfält som Demografisk poäng, Beteendepoäng och Total Person Score. Läs mer om de strategier som används av Marketo Engage Champions för att utveckla bedömningsmodeller som företaget behöver.
role: Admin
level: Beginner
doc-type: Article
solution: Marketo Engage
duration: 0
last-substantial-update: 2024-05-04T00:00:00Z
jira: KT-14810
thumbnail: KT-14810.jpeg
source-git-commit: 47ab8875bc4e41595cd40550330e43a88357b68d
workflow-type: tm+mt
source-wordcount: '2111'
ht-degree: 0%

---

# Bygga en personbedömningsmodell

Personpoäng hjälper er att identifiera de personer som är mest engagerade i ert företag och som är er idealiska kundprofil, så att ni kan dela dessa leads med säljteamet och göra avslut! Tillsammans med säljarna avgör du vilka leads du vill ge dem genom att använda ett lead/person-poängprogram i Adobe Marketo Engage. Detta kan antingen bestämmas genom ett minimum av beteendebedömning, demografiska poängsättning eller både och.

I den här självstudiekursen ska vi gå igenom tre övningar som föreslås av Marketo Engage Champions Christina Zuniga och Katja Keesom. Följ vidare för att avgöra vilka aktiviteter och egenskaper som är viktiga indikatorer på att en potentiell kund är intresserad av att köpa (beteendebedömning) och att de är rätt för dig (demografiska poäng), och ta hänsyn till nyanserna på olika marknader.

## Varför utveckla och använda en personbedömningsmodell?

Du kanske har många leads i din databas, men hur vet du vilka som är redo att köpa produkter och tjänster nu? I takt med att er marknadsföringsorganisation försöker optimera ledningskvaliteten och säljberedskapen är det här som poängmodellen kommer till sin rätt.

Genom att poängsätta personer i din Marketo Engage-databas kan du mäta hur kvalificerade dina genererade leads är och ange kriterier för när de är redo för försäljning. På så sätt kan säljteamet fokusera på de leads som troligen kommer att stängas medan marknadsföringsteamet fortsätter att vårda de andra personerna i databasen via sina marknadsföringsprogram.

## Utövning 1 - Bestämma köparens intresse med beteendepoäng

Beteendepoängen ger ett numeriskt värde till spårbara åtgärder som en potentiell kund vidtar som visar intresse för era produkter och tjänster och avsikter att köpa. Om du till exempel besöker webbplatsen kan det visa sig intressant att besöka prissidan. Om du däremot besöker yrkessidan kan det tyda på att personen inte kommer att köpa produkten.

**Steg 1** - Gör en lista över aktiviteter som är viktiga för din försäljningsprocess eller som är värdefulla för din organisation. Det kan vara praktiskt att samarbeta med säljarna för att fastställa vilka aktiviteter som indikerar att en lead har avsikt att köpa, vilket hjälper er att anpassa villkoren efter försäljningen och prioritera baserat på deras observationer av avslutade avtal. Här följer några förslag på frågor som du kan ställa till ditt säljteam:

* Vilka aktiviteter tyder på att det är bra eller dåligt som leder dig?
* Vilken typ av innehåll som används av ett lead har en starkare avsikt att köpa?

**Steg 2** - Visa en lista över åtgärder som tyder på att en potentiell kund inte är intresserad av din produkt. Se till att lista aktiviteter som kan spåras via Marketo Engage.

**Exempel 1a - Aktiviteter som anger avsikt att köpa**

| **Verksamheter som anger avsikten att köpa** | **Verksamheter som anger att man inte har för avsikt att köpa** |
| --- | --- |
| Besök prissidan | Ingen interaktion de senaste 90 dagarna |
| Delta i en årlig kundhändelse | Besök karriärsidan |
| Registrera dig för webbinarium | Avbeställ |
| Ladda ned rapporten |     |
| Fyll i demoformulär för begäran |     |

**Steg 3** - Analysera och välj ett tröskelvärde för försäljning.

* När en lead visar tillräckligt stort intresse genom att utföra några av de aktiviteter som du definierade i steg 1 och det totala poängtalet överskrider detta tröskelvärde, skickar du dem till försäljningen. Detta tröskelvärde blir helt enkelt ett tal som hjälper dig att ange ett riktmärke för poängen som du tilldelar enskilda beteenden.
* Tröskelvärdet bör vara tillräckligt stort så att en person måste slutföra flera interaktioner med ert varumärke för att kunna uppfylla det. Ett öppet e-postmeddelande är till exempel sannolikt inte en tillräcklig kvalificerare. Om du precis har börjat kan du prova att jobba med ett tröskelvärde på 100 och bygga ut din personpoäng därifrån.
* Ett högt eller lågt tröskelvärde beror på vilket leder ditt säljteam är mest intresserade av att ta emot och utveckla till affärsmöjligheter. Om du har några befintliga data om dina senaste försäljningserbjudanden kan du analysera dem och se vilka åtgärder andra har vidtagit i de lyckade avtalen. Detta kan hjälpa er att avgöra hur många kontaktpunkter som ingår i ett kvalificerat säljtips och hjälpa er att utifrån detta extrapolera vilket tröskelvärde som ska användas.

**Exempel 1b - Tröskelvärde för försäljning:**

| Genomsnittligt antal kontaktytor för kvalificerat lead | 4 |
| --- | --- |
| Tröskelvärde för överlämning av försäljning | 50 |

**Steg 4** - Tilldela ett poängvärde till varje aktivitet som listas i&quot;Exempel 1a - Aktiviteter som anger att kunden tänker köpa&quot;.

* Använd en positiv beteendepoäng för aktiviteter som indikerar intresse för att öka den potentiella kundens totala ledpoäng och en negativ poäng för att indikera ointresse.
* Använd ditt tröskelvärde från Exempel 1b - Tröskelvärde för försäljning vid leverans som riktmärke för att fastställa dina beteendepoäng i förhållande till betydelsen av deras åtgärder. Exempel: potentiella kunder som begär en demo ska gå direkt till försäljning. Det bästa är att tilldela den åtgärden ett poängvärde som motsvarar tröskelvärdet för när en potentiell kund ska lämna över en åtgärd. Samtidigt är nedladdningen av en rapport inte en lika stark indikator på köpintresset och bör därför vara värd färre poäng.

**Exempel 1c - Poängaktiviteter som anger avsikt att köpa:**

| Tröskelvärde för överlämning av försäljning = 50 poäng |     |
| --- | --- |
| Aktivitet | Poäng |
| Fylld&quot;request a demo form&quot; | +50 |
| Ingen interaktion de senaste 90 dagarna | \-10 |
| Ladda ned en rapport | +5 |
| Besök oss på ett mässor | +15 |

**Steg 5** - Kom ihåg att poängsättning är en repetitiv process! Granska och justera poängvärden och tröskelvärden kontinuerligt när ni samlar in mer data för analys.

## Utövning 2 - Identifiera rätt anpassning med demografiska resultat

Nu när du har definierat aktiviteterna som indikerar inköpsavsikt bör du slutföra poängmodellen med dina Idealiska profiler för potentiella kunder. För att identifiera om en potentiell kund är rätt lämpad för ytterligare säljsamtal är det viktigt att tilldela demografiska poäng utöver beteendepoängen så att modellen hjälper till att fastställa de bästa leads vad gäller anpassning och avsikt.

**Steg 1** - Gör en lista med egenskaper för dina idealiska prospects.

* Ta en titt på attribut som bransch, företag, avdelning och roll. Se till att dessa egenskaper motsvarar de tillgängliga demografiska fälten i Marketo Engage.
* Samarbeta med säljarna för att ta reda på vilka leads som svarar mest på säljförfrågningar och är viktiga kontakter under försäljningstillfällen.
   * Det kan vara till hjälp att analysera nyligen avslutade kundtillfällen för att se vilka egenskaper era bästa kunder har. Till exempel:
      * Genom att gå igenom stängda förlorade möjligheter för mönster kan du hitta demografiska data som du vill undvika.
      * Identifiera beslutsfattare och interna förespråkare som driver era säljsatsningar. Fördjupa dig i informationen och ta fram resultatet för en workshop med några av säljarna för att validera eller förfina slutsatserna.
   * Du kan även intervjua ditt säljteam med följande exempelfrågor:
      * Vilken avdelning är de vanligtvis engagerade med?
      * Vilka yrkesgrupper arbetar de som deltar i produktdemonstrationer och vilka är de personer som ska skriva under på köpet?

**Exempel 2a - Idealiska egenskaper för potentiella kunder**

| **Kategori** | **Idealiska egenskaper för potentiell kund** |
| --- | --- |
| Bransch | Flygindustri |
| Företagsstorlek | 100 - 999, 1 000 - 9 999 |
| Befattning | Director, Vice President, C-Level |
| Avdelning | HR |

**Steg 2** - Tilldela ett poängvärde till varje egenskap utifrån dess relevans i din profil för potentiella kunder. Använd positiva poäng för önskvärda egenskaper och negativa resultat för egenskaper som gör att leadet inte passar produkten bättre.

**Exempel 2b - Tilldela poäng till idealiska och oönskade egenskaper**

| **Egenskaper** | **Poäng** |
| --- | --- |
| Bransch - flygindustri | +10 |
| Bransch - tillverkning | +5 |
| Företagsstorlek - 100 - 999 | +5 |
| Företagsstorlek - 1 000 - 9 999 | +10 |
| Företag - &lt;10 | \-10 |

## Exercise 3 - Inkludera lokal flexibilitet i din poängmodell

Med de grundläggande beteendemodellerna och de demografiska poängmodellerna som du har utfört kan du ta dem till nästa nivå genom att tillåta lokal flexibilitet. Affärsvärdena kan variera på olika marknader när en organisation är global. I följande övning får du lära dig att använda poäng som återspeglar det verkliga affärsvärdet för leadaktiviteterna eller egenskaperna i olika situationer.

Föredrar du en videomaterial för den här övningen? Tune in as Marketo Engage Champion Katja Keesom demonstrerar lokal flexibilitet i poängmodellen.

>[!VIDEO](https://video.tv.adobe.com/v/3426914/?learn=on)

**Steg 1** - Ta aktiviteter och egenskaper från övningar 1 och 2 och för varje artikel avgöra om de varierar beroende på plats eller produktlinje.

**Exempel 3a - Signaler på globala och lokala marknader:**

| **Signal** | **Global** | **Lokal** |
| --- | --- | --- |
| Aktiviteter | <ul><li>Fylld i formuläret&quot;Begär en demo&quot;</li><li>Ingen interaktion under de senaste 90 dagarna (cirka 3 månader)</li></ul> | <ul><li>Besök oss på mässan</li><li>Ladda ned en rapport</li></ul> |
| Egenskaper | <ul><li>Avdelning</li><li>Befattning</li></ul> | <ul><li>Bransch</li><li>Företagsstorlek</li></ul> |

**Steg 2** - Definiera din poängmatris för lokala marknader:

* Ställ in en annan matris för demografiska element och beteendeelement.
* Bestäm vad som ska prioriteras så att du kan fråga efter det lokala teamets synpunkter.
* Definiera antalet värden som ska användas för att betygsätta inom dina ämnen.
* Tilldela enskilda värden genom att justera relativ avkastning med globala poäng.
* Överväg att definiera vanliga scenarier när presumtiva kunder interagerar med ert varumärke och testa er övergripande bedömning för dem.
   * En vanlig kundresa som du ser är till exempel att en person kan ange din webbplats på en innehållssida, sedan klicka igenom till en produktsida och ladda ned en broschyr. Om du vill göra dem till målgrupper med en webbinariinbjudan svarar de på den genom att registrera sig, men inte vara närvarande. Fundera på om er försäljning redan vill tala med den här personen eller inte och utvärdera om er poängmodell får dessa potentiella kunder att få rätt totalpoäng för att återspegla den nivån av intresse.

**Exempel 3b - Demografisk poängmatris:**

| **Demografisk matris** | **Prioritet 1** | **Prioritet 2** | **Prioritet 3** |
| --- | --- | --- | --- |
| Höga värden | 20 poäng | 10 poäng | 7 punkter |
| Medelvärden | 10 poäng | 7 punkter | 3 punkter |
| Låga värden | 5 punkter | 3 punkter | 1 punkt |

**Steg 3** - Samla in data från era lokala eller regionala säljteam för att få en helhetsbild. Du kommer att märka att inga individuella resultat inkluderas i exempel 3c. På så sätt kan säljteamet fokusera på det relativa värdet av de olika ämnena under granskningsprocessen. Du bör dock ha den fullständiga modellen dokumenterad som bakgrundsmaterial för andra Marketo Engage-administratörer.

* Lås det som inte kan justeras för global konsekvens (här i kolumnen Implementeringsämne).
* Markera (här i kolumnerna Prioritet och Poäng) vad som kan justeras för lokala påverkan.

**Exempel 3c - Relativt värde för poängämnen:**

<table>
 <tr>
    <th>#</th>
    <th>Implementeringsämne</th>
    <th>Demografi/beteende</th>
    <th>Ämne</th>
    <th>Prioritet</th>
    <th>Värden</th>
    <th>Scores</th>
 </tr>
 <tr>
    <td rowspan="6">1</td>
    <td rowspan="6"><b>KRÄVS</b></td>
    <td rowspan="6">Demografisk</td>
    <td rowspan="6">Bransch</td>
    <td rowspan="6"><b>2</b></td>
    <td>Teknik</td>
    <td><b>Hög</b></td>
  </tr>
  <tr>
    <td>Fashion</td>
    <td><b>Hög</b></td>
  </tr>
  <tr>
    <td>Detaljhandel</td>
    <td><b>Medel</b></td>
  </tr>  
  <tr>
    <td>Tillverkning</td>
    <td><b>Medel</b></td>
  </tr>
  <tr>
    <td>Sjukvård</td>
    <td><b>Låg</b></td>
  </tr>
  <tr>
    <td>...</td>
    <td><b>Låg</b></td>
  </tr>
<tr>
    <td rowspan="3">2</td>
    <td rowspan="3"><b>Ja</td>
    <td rowspan="3">Demografisk</td>
    <td rowspan="3">Företagsstorlek (anställda)</td>
    <td rowspan="3"><b>3</td>
    <td>&gt;1 000 anställda</td>
    <td><b>Hög</td>
  </tr>
  <tr>
    <td>250-999 anställda</td>
    <td><b>Medel</td>
  </tr>
  <tr>
    <td>1-249 anställda</td>
    <td><b>Låg</td>
  </tr>  
<tr>
    <td rowspan="3">3</td>
    <td rowspan="3"><b>Nej</b></td>
    <td rowspan="3">Beteende</td>
    <td rowspan="3">Besök webbsidan</td>
    <td rowspan="3"><b>2</b></td>
    <td>&gt;Produktinformationssidor</td>
    <td><b>Låg</b></td>
  </tr>
  <tr>
    <td>Prissättningssidor</td>
    <td><b>Medel</b></td>
  </tr>
  <tr>
    <td>Demo - begärandesida</td>
    <td><b>Hög</b></td>
  </tr>
</table>

## Vad händer nu?

* Ladda ned [träningsblad för personpoäng](./assets/build-person-scoring-model-and-local-flexibility-in-adobe-marketo-engage.docx){target="_blank} för att utveckla din poängmodell offline.
* Bygg upp din personpoäng i Marketo Engage. Kontrollera detta [självstudiekurs](https://experienceleague.adobe.com/en/docs/marketo-learn/tutorials/lead-and-data-management/lead-scoring-watch){target="_blank} och [demo](https://experienceleague.adobe.com/en/docs/events/marketo-and-mochas-recordings/2023/lead-scoring){target="_blank} för att komma igång. Du kan importera ett lead-/personbedömningsprogram [mall](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/programs/working-with-programs/import-a-program){target="_blank} från referensbiblioteket i Marketo Engage för att snabba upp programbygget.
* Skapa två versioner av poängprogrammet:
   * Ett centralt program som kör all poängsättning som inte kan uppdateras lokalt.
   * En lokal kopia med de poängsättningselement som kan konfigureras.
* Ange dina poängvärden som variabler i poängprogrammet. Detta garanterar enhetlighet även när du justerar bakgrundsmusik över tid.
   * Ett vanligt exempel på tokeniserade poäng är att ha en token för värdefulla aktiviteter som automatiskt uppfyller ditt tröskelvärde, som att begära en demo eller boka ett möte med ditt säljteam. Även om du ändrar det poängvärde som krävs för att uppnå tröskelvärdet kan du enkelt uppdatera alla värdefulla aktiviteter samtidigt genom att uppdatera en token.
* Justera din lokala smarta kampanj för varje plats:
   * Bestäm vilka demografiska aktiviteter och beteendeaktiviteter som bara ska poängsättas en gång (dvs. bransch) och vilka som ska poängsättas varje gång en potentiell kund kvalificerar sig (dvs. deltar i ett webbinarium). Detta garanterar att potentiella kontakter som triggas av ändringen av datavärdet är relevanta för försäljningen.
   * Se till att dina val utesluter varandra.
   * Uppdatera i båda flödesstegen så att personbakgrundsmusiken uppdateras på samma sätt som den demografiska poängen. På så sätt håller sig personbakgrundsmusiken till en kombination av beteendepoäng och demografiska poäng.
* Testa Smart Campaign när du är klar med att skapa programmet. Du kan till exempel gå till demoformuläret, fylla i det med ett testmeddelande och kontrollera din testpersons poäng i [Marketo Engage-databas](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started-with-marketo/quick-wins/simple-scoring#step-view-the-person-info){target="_blank}.
* När du har skapat din modell bör du överväga att skapa en avisering som ska gå till försäljning när personens poäng har nått tröskelvärdet för försäljning. Läs mer om hur du ställer in en avisering med den här [självstudiekurs](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/send-alert){target="_blank}.

### Författare

{{christina-zuniga}}

{{katja-keesom}}

{{amy-chiu}}