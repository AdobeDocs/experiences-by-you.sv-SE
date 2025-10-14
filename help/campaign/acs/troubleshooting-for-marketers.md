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
exl-id: 1f27e284-73e3-4f28-988e-51163775eec8
source-git-commit: 02e3a6dfa59df45113242bd8e874e18e9e1efd58
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---

# Felsökning för marknadsförare: 5 Vanliga arbetsflödes- och leveransfel

Av: [Suraj Patra](https://www.linkedin.com/in/suraj-p-51612053/){target="_blank"}, Senior Consultant, Meijer

Som Senior Engineer och Customer Expert på [!DNL Adobe] Experience Cloud-produkter de senaste fem åren ger jag företagsanvändare på [Meijer](https://www.meijer.com/){target="_blank"}, en amerikansk supercenter som grundades 1934, möjlighet att köra komplexa marknadsförings- och transaktionskampanjer med ACS. Några projekt som jag har arbetat med är anpassade kampanjer för att lagra erbjudanden och beställningsinformation för personalisering, integrerade med [!DNL Adobe] Audience Manager, och kundinsikter för segmentförtäring.

Under min tid med ACS har jag råkat ut för fel som kan vara tidskrävande och frustrerande att lösa. Att veta de vanligaste felen kan bidra till snabbare problemlösning och öka produktiviteten. Här nedan hittar jag felsökningstips som hjälper dig att effektivt åtgärda liknande fel som de inträffar.

## Felmatchningsfel för datatyp

**Felkod:**
`PGS-220000 PostgreSQL error: ERROR: operator does not exist: character varying = bigint`

**Orsak:**
Den här typen av fel visas i ett arbetsflöde när du försöker stämma av med fält av olika datatyper. Om du till exempel överför en fil med hjälp av en inläsningsfil som har ett strängfält, och du försöker att koppla strängfältet till ett profilfält som har datatypen int.

![data-type-mismatch-error](/help/_assets/kt-13256/data-type-mismatch.png)

**Lösning:**
Ändra datatypen för fältet i aktiviteten &quot;Läs in fil&quot; till den som du matchar med. Öppna aktiviteten Läs in fil. Gå till fliken&quot;COLUMN DEFINITION&quot; och ändra datatypen för det önskade fältet.


![data-type-mismatch-solution](/help/_assets/kt-13256/data-type-mismatch-solution.png)

## Personalization-leveransfel

**Felkod:**
`The schema for profiles specified in the transition ('') is not compatible with the schema defined in the delivery template ('nms:recipient'). They should be identical.`

**Orsak:**
Det här felet visas när du skickar ett e-postmeddelande till en adress, men e-postmeddelandet eller någon annan identifierare inte är avstämd mot en profil. Om du vill skicka en e-postkommunikation ska e-postmeddelandet eller identifieraren alltid vara länkade till en profil.

![arbetsflöde med avstämningsaktivitet](/help/_assets/kt-13256/del-persn-error-wf.png)

**Lösning:**
Det måste finnas ett gemensamt ID från den inlästa filen med mottagartabellen. Den här gemensamma nyckeln kopplar inläsningsfilen till mottagartabellen inom avstämningsaktiviteten. E-postmeddelanden kan inte skickas till poster som inte finns i mottagarregistret, vilket kräver det här avstämningssteget i arbetsflödet. Då stämde du av den inkommande inläsningsfilaktiviteten med en identifierare som e-post-ID från profilen. Schemat `nms:recipient` refererar till profiltabellen och om inkommande poster stäms av med profilen blir det tillgängligt under e-postförberedelsen.

Se skärmbilden för avstämningsaktiviteten som visas nedan.

![arbetsflöde med avstämningsdetaljer](/help/_assets/kt-13256/del-persn-error-wf-solution.png)

Läs mer om [avstämning](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/data-management-activities/reconciliation.html?lang=sv-SE).

## Fel i datamängd för gemensamt fält

**Felkod:**
`The document types of inbound events (''and'') are incompatible (step 'Exclusion'). Unable to perform the operation. `

**Orsak:**
Problemet inträffar när **exkluderingsaktiviteten** används i ACS-arbetsflöden, när en exkludering baserat på ID:t utförs, när den primära uppsättningen och den exkluderade uppsättningen inte har samma fältnamn.


![Fel i datauppsättning för vanligt fält](/help/_assets/kt-13256/dataset-error.png)

**Lösning:**

Det finns två sätt att lösa det här felet:

1. Använd samma fältnamn i både primär och exkluderad och använd fältet som ID

   ELLER

2. Använd exkluderingsmetoden JOINS för att välja det fält som du vill exkludera posterna från.

![Allmänt fel i fältdatauppsättning - Lösning &#x200B;](/help/_assets/kt-13256/dataset-error-solution.png)

## Ignorerat fältnamn

**Felkod:**
`XTK-170036 Unable to parse expression 'i__name'`

**Orsak:**

Felpunkter kan förekomma i en **anrikningsaktivitet**. En av de vanligaste visas nedan.

![Fältnamn utelämnade fel](/help/_assets/kt-13256/field-name-dropped-error.png)

Det här händer när du redigerar ett uttrycksnamn i aktiviteten manuellt. Bilden visar att uttrycket har ändrats från `name ` till `i__name`.

**Lösning:**

Du kan lösa det här felet på tre sätt:

1. Ändra tillbaka namnet till det uttryck som ursprungligen fanns.

2. Om du vill använda ett nytt namn ändrar du värdena i **anrikningsaktiviteten**.

3. Om du inte kommer ihåg vad som har ändrats är det bästa valet att återskapa aktiviteten.

## Tillfälligt tabellsläppningsfel 

**Felkod:**
`XTK-170024 The temporary schema "temp:deliveryEmail1" is not defined in the current context.`

**Orsak:**
Detta är ett vanligt fel i komplicerade arbetsflöden som innefattar anrikning eller annan aktivitet. Det betyder antagligen att vissa aktivitetsarbetsflöden inte sparas korrekt vid flera ändringar av arbetsflödet.

![Temporärt tabellsläppt fel &#x200B;](/help/_assets/kt-13256/temp-table-dropped-error.png)

**Lösning:**
Det finns många sätt att åtgärda det här felet, så det finns ingen enkel korrigering. Om det är ett enkelt arbetsflöde är det bättre att konfigurera om aktiviteten. I ett komplicerat arbetsflöde är det bättre att kopiera arbetsflödesaktiviteterna till ett nytt arbetsflöde, spara och köra om dem.
