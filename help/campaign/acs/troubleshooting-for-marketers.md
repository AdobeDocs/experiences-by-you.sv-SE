---
title: Felsökning för marknadsförare
description: Att veta de vanligaste felen kan bidra till snabbare problemlösning och öka produktiviteten. Dessa felsökningstips hjälper dig att effektivt åtgärda liknande fel som de inträffar.
solution: Campaign Standard
feature-set: Campaign
feature: Workflows
role: User
level: Beginner, Intermediate, Experienced
doc-type: Article
last-substantial-update: 2023-05-18T00:00:00Z
jira: KT-13256
thumbnail: KT-13256.jpeg
source-git-commit: 0fc67f48deb78d5a66d485093d1837cbeee7c4d4
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---

# Felsökning för marknadsförare: 5 Vanliga arbetsflödes- och leveransfel

Efter: [Suraj Patra](https://www.linkedin.com/in/suraj-p-51612053/){target="_blank"}, Senior Consultant, Meijer

Som tekniker och kundexpert på [!DNL Adobe] De fem senaste Experience Cloud-produkterna har jag gjort det möjligt för företagsanvändare på [Meijer](https://www.meijer.com/){target="_blank"}, en amerikansk supercenterkedja som grundades 1934, för att genomföra komplexa marknadsförings- och transaktionskampanjer med ACS. Några projekt som jag har arbetat med är anpassade kampanjer för att lagra erbjudanden och beställa detaljer för personalisering, integrerade med [!DNL Adobe] Audience Manager och kundinsikter om segmentförtäring.

Under min tid med ACS har jag råkat ut för fel som kan vara tidskrävande och frustrerande att lösa. Att veta de vanligaste felen kan bidra till snabbare problemlösning och öka produktiviteten. Här nedan hittar jag felsökningstips som hjälper dig att effektivt åtgärda liknande fel som de inträffar.

## Felmatchningsfel för datatyp

**Felkod:**
`PGS-220000 PostgreSQL error: ERROR: operator does not exist: character varying = bigint`

**Orsak:**
Den här typen av fel visas i ett arbetsflöde när du försöker stämma av med fält av olika datatyper. Om du till exempel överför en fil med hjälp av en inläsningsfil som har ett strängfält, och du försöker att koppla strängfältet till ett profilfält som har datatypen int.

![data-type-mismatch-error](/help/_assets/kt-13256/data-type-mismatch.png)

**Lösning:**
Ändra datatypen för fältet i aktiviteten &quot;Läs in fil&quot; till den som du matchar med. Öppna aktiviteten Läs in fil. Gå till fliken&quot;COLUMN DEFINITION&quot; och ändra datatypen för det önskade fältet.


![datatyp-mismatch-solution](/help/_assets/kt-13256/data-type-mismatch-solution.png)

## Leveranspersonaliseringsfel

**Felkod:**
`The schema for profiles specified in the transition ('') is not compatible with the schema defined in the delivery template ('nms:recipient'). They should be identical.`

**Orsak:**
Det här felet visas när du skickar ett e-postmeddelande till en adress, men e-postmeddelandet eller någon annan identifierare inte är avstämd mot en profil. Om du vill skicka en e-postkommunikation ska e-postmeddelandet eller identifieraren alltid vara länkade till en profil.

![arbetsflöde med avstämningsaktivitet](/help/_assets/kt-13256/del-persn-error-wf.png)

**Lösning:**
Det måste finnas ett gemensamt ID från den inlästa filen med mottagartabellen. Den här gemensamma nyckeln kopplar inläsningsfilen till mottagartabellen inom avstämningsaktiviteten. E-postmeddelanden kan inte skickas till poster som inte finns i mottagarregistret, vilket kräver det här avstämningssteget i arbetsflödet. Då stämde du av den inkommande inläsningsfilaktiviteten med en identifierare som e-post-ID från profilen. The `nms:recipient` schemat refererar till profiltabellen och när inkommande poster stäms av mot profilen blir den tillgänglig under e-postförberedelsen.

Se skärmbilden för avstämningsaktiviteten som visas nedan.

![arbetsflöde med avstämningsdetaljer](/help/_assets/kt-13256/del-persn-error-wf-solution.png)

Läs mer om [avstämning](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/data-management-activities/reconciliation.html?lang=en).

## Fel i datamängd för gemensamt fält

**Felkod:**
`The document types of inbound events (''and'') are incompatible (step 'Exclusion'). Unable to perform the operation. `

**Orsak:**
Problemet inträffar när **exkluderingsaktivitet** i ACS-arbetsflöden, när du utför ett undantag baserat på ID, när den primära uppsättningen och den uteslutna uppsättningen inte har samma fältnamn.


![Fel i datamängd för gemensamt fält](/help/_assets/kt-13256/dataset-error.png)

**Lösning:**

Det finns två sätt att lösa det här felet:

1. Använd samma fältnamn i både primär och exkluderad och använd fältet som ID

   ELLER

2. Använd exkluderingsmetoden JOINS för att välja det fält som du vill exkludera posterna från.

![Allmänt fel i fältdatauppsättning - Lösning ](/help/_assets/kt-13256/dataset-error-solution.png)

## Ignorerat fältnamn

**Felkod:**
`XTK-170036 Unable to parse expression 'i__name'`

**Orsak:**

Felpunkter kan uppstå i en **anrikningsverksamhet**. En av de vanligaste visas nedan.

![Ignorerat fältnamn](/help/_assets/kt-13256/field-name-dropped-error.png)

Det här händer när du redigerar ett uttrycksnamn i aktiviteten manuellt. Bilden visar att uttrycket har ändrats från `name `till `i__name`.

**Lösning:**

Du kan lösa det här felet på tre sätt:

1. Ändra tillbaka namnet till det uttryck som ursprungligen fanns.

2. Om du vill använda ett nytt namn ändrar du värdena i **anrikningsverksamhet**.

3. Om du inte kommer ihåg vad som har ändrats är det bästa valet att återskapa aktiviteten.

## Tillfälligt tabellsläppningsfel 

**Felkod:**
`XTK-170024 The temporary schema "temp:deliveryEmail1" is not defined in the current context.`

**Orsak:**
Detta är ett vanligt fel i komplicerade arbetsflöden som innefattar anrikning eller annan aktivitet. Det betyder antagligen att vissa aktivitetsarbetsflöden inte sparas korrekt vid flera ändringar av arbetsflödet.

![Tillfälligt tabellsläppningsfel ](/help/_assets/kt-13256/temp-table-dropped-error.png)

**Lösning:**
Det finns många sätt att åtgärda det här felet, så det finns ingen enkel korrigering. Om det är ett enkelt arbetsflöde är det bättre att konfigurera om aktiviteten. I ett komplicerat arbetsflöde är det bättre att kopiera arbetsflödesaktiviteterna till ett nytt arbetsflöde, spara och köra om dem.
