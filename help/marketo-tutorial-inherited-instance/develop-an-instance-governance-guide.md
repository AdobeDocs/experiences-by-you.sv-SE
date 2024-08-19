---
title: Utveckla en instansstyrningsguide med dokumentation
description: Lär dig hur du skapar och underhåller dokumentation och ändringslogg för din [!DNL Marketo Engage] instans.
feature-set: Marketo Engage
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00Z
jira: KT-14103
thumbnail: KT-14103.jpeg
hide: false
exl-id: e127b84d-ef92-4527-a0e6-a36af35b7ee0
source-git-commit: 1205848b1985a99b91f9d4d25e1a79f0df379589
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# Utveckla en instansstyrningsguide med dokumentation

När du går in i en äldre [!DNL Marketo Engage]-instans har den ofta en utmaning att sakna aktuell funktionell och teknisk dokumentation. Som administratör är det ett viktigt ansvar att fastställa riktlinjer för att säkerställa korrekt instansstyrning som du inte kan missa. Det är en av de kritiska strategierna för att [öka effektiviteten när du arbetar i en etablerad [!DNL Marketo Engage] instans](https://nation.marketo.com/t5/champion-program-blogs/3-tips-to-increase-your-efficiency-in-an-inherited-instance/ba-p/247582).

Den här stegvisa självstudiekursen som kommer från [!DNL [!DNL Adobe] Marketo Champion] (2018), Nick Hajdin, vägleder dig genom den här processen för att skissera instanskonfigurationen, dokumentera dina primära operativa program och underhålla en [!DNL changelog] för att tillämpa en strikt styrningsprincip.

## Utveckla en instansstyrningsguide för din ärvda instans

Detaljerad dokumentation och en [!UICONTROL Changelog] är avgörande för effektiv hantering och kunskapsöverföring i [!DNL Marketo Engage]-instansen. Genom att hålla reda på ändringar och beslut som du har fattat under instanskonfigurationen kan du:

1. Utbilda interna användare enklare på ett skalbart sätt.
2. Bygg mer effektivt i [!DNL Marketo Engage] på lång sikt.
3. Behåll hälsa och hygien i instansen genom att gå framåt så att du slipper lägga timmar på att gräva i e-postmeddelanden, [granskningsspår](https://experienceleague.adobe.com/docs/marketo/using/product-docs/administration/audit-trail/audit-trail-overview.html) och [aktivitetsloggar](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person.html) för att få kontext.
4. Spara tid när du överför [!DNL Marketo Engage]-kunskaper till en ny [!DNL Marketo Engage]-administratör om ditt team upplever någon omsättning.

## [!DNL Marketo Engage] styrningsguide 101

En styrningsguide fungerar som en källa till sanning för instansens konfiguration och systemdesignkraven. Nyckelinformation som rekommenderas i det här dokumentet är:

* Program-/mappstrukturer
* Behörighet för användare och roll
* Kommunikationsbegränsningar
* Styrningsstandarder
* Intern användarutbildning innan de får åtkomst till plattformen

## Utveckla och underhålla en styrningsguide för din [!DNL Marketo Engage]-instans

### Steg 1: Identifiera din aktuella styrningsguide och dokumentation

* **Jag kan inte hitta någon dokumentation för min ärvda instans:** Om du nyligen har startat en ny roll och inte kan hitta någon dokumentation för den ärvda instansen **går du till steg 2** och kommer igång med en hämtningsbar mall som vi tillhandahöll.
* **Jag har dokumentation om filen:** Grattis, det här är ett bra tecken! Se till att de är relevanta för att se när den senaste ändringen görs. Om det inte underhålls aktivt av dina teammedlemmar rekommenderar vi att du uppdaterar dem och informerar dina interna användare om hur de håller det uppdaterat.

### Steg 2: Identifiera de element som ska inkluderas i [!DNL Marketo Engage]-dokumentationen och [!DNL Changelogs]

Formatet varierar från en molnbaserad plattform till ett delat dokument. Du kan utforma det format som passar din organisations behov. [Här är en enkel dokumentation och en Excel-mall för ändringsloggar](/help/marketo-tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx) som innehåller viktiga element som du kan komma igång med. Bland dessa finns:

* Dokumentation
   * Programmallsnamn
   * Kanal
   * Skapad den
   * Skapad av
   * Programmets syfte
   * Status
   * Länk till programmall
   * Anteckning
* Changelog
   * Programmallsnamn
   * Ändringsdatum
   * Uppdaterat av
   * Uppdateringssyfte
   * Upplevelse före ändring (inkludera länkar/skärmbilder)
   * Upplevelse efter ändring (inkludera länkar/skärmbilder)
   * URL till program

### Steg 3: Identifiera och dokumentera det aktuella läget för de primära operativa programmen

Börja med att identifiera de viktigaste operativa programmen med påverkan på prenumerationsnivå. Exempel är datahantering [!DNL Campaign], Lead Lifecycle, Lead Scoring, [!DNL CRM] Sync och Deliverability.

För varje identifierat operativt program dokumentera dess nuvarande status. Detta innehåller information om programmets syfte, konfiguration, associerade smarta kampanjer och integrering med andra verktyg (om tillämpligt).

### Steg 4: Tvinga underhåll av [!UICONTROL Changelog]

Nästa steg är att upprätta en strikt styrningsprincip för din [!DNL Marketo Engage]-instans som kräver [!UICONTROL Changelog]-underhåll. Denna policy säkerställer att alla uppdateringar som görs av de operativa programmen i hela instansen dokumenteras noggrant.

Undervisa teamet om vikten av dessa dokument och hur man får tillgång till och uppdaterar dem på rätt sätt. Det kan vara praktiskt att tilldela ansvarsområden för att underhålla ändringsloggen, så att ett fåtal utsedda medlemmar i Marketing Operation-teamet eller administratörer konsekvent registrerar ändringar och tillhandahåller godkännanden.

### Steg 5: Centralisera dokumentation

Skapa en central plats eller databas för lagring av all dokumentation som hör till din [!DNL Marketo Engage]-instans. Det kan vara en delad enhet, en dedikerad mapp eller ett molnbaserat system.

### Steg 6: Granska och uppdatera

Schemalägg regelbundna granskningar av din dokumentation för att säkerställa att den är korrekt och aktuell. Den kan lätt förbises under upptagna tider. Ställ in påminnelser i din kalender proaktivt för att säkerställa att ditt team regelbundet uppdaterar för att återspegla ändringar eller optimeringar i de operativa programmen.

## Vad kommer härnäst?

Kom igång genom att hämta den här [enkla mallen](/help/marketo-tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx).

Följ stegen ovan för att utveckla din styrningsguide och dokumentation. När du arbetar med processen bör du tänka på följande regler:

**Uppdatera befintlig dokumentation:**
Det är viktigt att hålla dokumentationen uppdaterad. Om det inte har ändrats de senaste 3 åren sparar du tid på att granska din dokumentation medan du granskar instansen.

**Dela och träna:**
Dela din dokumentation och [!DNL changelog] med relevanta teammedlemmar och lär dem hur de uppdaterar dessa register.

**Periodisk granskning:** anger tid för att granska och underhålla dem under året för att inkludera nya ändringar, optimeringar eller justeringar när de inträffar.

Genom att underhålla omfattande och aktuell dokumentation för din [!DNL Marketo Engage]-instans sparar du tid och arbete på lång sikt och underlättar effektiv instanshantering.

### Författare

**Nick Hajdin**
[!DNL [!DNL Adobe] Marketo Champion] (2018)
*[!DNL Digital Technology Senior Manager at Accenture]*

![Nick Hajdin](/help/marketo-tutorial-inherited-instance/_assets/authors/Customer_Author_Nicholas_Hajdin.png){width="30%"}

**Amy Chiu**
*Adobe &amp; Retention Marketing Manager,[!DNL Adobe]*

![Amy Chiu](/help/marketo-tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width=30%}
