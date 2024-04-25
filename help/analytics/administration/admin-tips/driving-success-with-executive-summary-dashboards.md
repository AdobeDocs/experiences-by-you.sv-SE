---
title: Skapa framgångsrika statuspaneler med chefssammanfattning
description: Cheferna saknar ofta aktuell och relevant information för sina webbplatser och appar, beroende på månadsvisa Excel-diagram eller drunkning av detaljdata. Lösningen - en sammanfattande kontrollpanel för chefer.
solution: Analytics
feature-set: Analytics
feature: Admin Tools
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-15T00:00:00Z
jira: KT-13216
thumbnail: KT-13216.jpeg
exl-id: ea446e58-d9f2-4a21-aa9b-71aa548016e2
source-git-commit: aff0b385ce3ba9c31245e26f0b14cc201ea57fb9
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 0%

---

# Skapa framgångsrika statuspaneler med chefssammanfattning

_Cheferna saknar ofta aktuell och relevant information för sina webbplatser och appar, beroende på månadsvisa Excel-diagram eller drunkning av detaljdata. Lösningen: Experience Manager Cloud Managerarketo EngagExecutive Summary Dashboard._

Jag vill att du tänker köra från Seattle till San Francisco. Vägledning, det är ganska enkelt. Gå på I-5 South i tolv till sexton timmar så är du där. Enkelt, eller hur? Nu vill jag att du ska tänka dig att jag har placerat en karta över din instrumentpanel, och jag säger att när resan är slut får du en instrumentpanel som visar din hastighet, dina bränslenivåer och tillryggalagda avstånd:

![Stolpdiagram.png](assets/bar-graph.png)

Om du granskar diagrammet kan du lägga märke till några saker:

1. Hastigheten varierade avsevärt, överskred den tillåtna hastighetsbegränsningen vid vissa punkter och låg vid andra punkter på grund av t.ex. Portlands trafik

1. Det tillryggalagda avståndet är statiskt i timmar 6-9

1. Det beror på att ditt bränsle sjönk till 0 % och du var tvungen att vänta på hjälp från vägarna för att ta sig genom Portland och fylla upp din gastank

En sådan resa vore uppenbarligen olycklig, oförutsägbar och farlig. Det är inte ett sätt att köra. Du behöver kontinuerlig information om hastighet, tillryggalagd sträcka och bränslenivåer för att kunna göra kontinuerliga justeringar av hur du kör. Det råder ingen tvekan om att en rimlig person skulle rippa ut kartongen från kontrollpanelen och regelbundet kontrollera, vilket skulle radera timmar från resan, nästan eliminera risken för att gasen tar slut och hålla dig i rätt hastighet för att undvika en fortkörningsbot.

Så varför accepterar så många chefer detta som ett rimligt sätt att sköta sina webbplatser och appar?

Många chefer har inte tillgång till aktuell, relevant information som behövs för att vidta åtgärder i tid. De får i stället ett däck en gång i månaden med statistik som exporterats från [!DNL Adobe Analytics] i Excel, diagram och sedan i en PowerPoint. Om en influensapunkt inträffar tidigt i månaden kommer de inte att få veta om den förrän i början av nästa månad, långt efter att de kan ställa frågor eller vidta åtgärder. Anpassade aviseringar är också ett bra alternativ, men vi vet alla hur en exekels e-postinkorg ser ut.

Ni vill att cheferna ska ha tillräckligt med data för att veta när deras uppmärksamhet behövs, inte så mycket att de slänger händerna i frustration. Om du kommer med ett meddelande från en produktägare eller marknadschef om att en chef vill veta mer om en avvikelse så stöter du på den ljuva fläcken.

Det är här som den sammanfattande kontrollpanelen kommer in som det glada mediet. Vi vet att mobilstyrkortet är bra för en snabb incheckning när du är ute på språng, men en instrumentpanel för sammanfattning kan göra det enkelt för chefer att gräva lite djupare när de sitter på sina skrivbord. Mobil styrkort kan varna dem om ett problem, men den verkställande sammanfattningsinstrumentpanelen låter dem sedan förstå tillräckligt för att ställa rätt frågor från rätt personer.

De flesta chefer har ungefär tre nyckeltal som de är djupt oroade över. Inom detaljhandeln kan det vara beställningar, intäkter och AOV. För B2B, leads, lead-kvalitet och konverteringsgrad. Tjänsterna kan vara intresserade av besök, besök och återkommande besökare. Vad de än är så sätter du dem i stora, feta siffror med en årsomgång och ett diagram. Visualiseringen av nyckelmätningssammanfattningen gör detta så enkelt:

![Zooma in panel](assets/zoom-in-panel.png)

Lägg in historiska data för samma tre mätvärden så att det blir enkelt att se långsiktiga trender:

![linjediagram.png](assets/line-graph.png)

Lägg till några listrutor för det som är viktigt för er organisation. Jag tycker att enhetstyp och marknadsföringskanal oftast är bra val:

![Social [!DNL Campaign]s.png](assets/social-campaigns.png)

Båda är viktiga generellt, men som alltid måste du se till att det du väljer är relevant för din webbplats eller app.

Längst ned lägger du till några detaljer. Jag tycker att sidprestanda ofta är populärt hos chefer, men nyckeln är att den är under det förgångna. De kan söka efter den om de vill ha den, men i annat fall har de data de behöver ställa frågor direkt:

![Stor kontrollpanel.png](assets/large-dashboard.png)

Med den här slutprodukten i handen behöver du bara:

- Utbilda dina chefer i hur de läser det

- Lär dem hur man använder filtren

- Utbilda dem i en grundövning

- Ta lite kaffe och förbered dig, för när de har fått datatillstånd kommer cheferna att komma till dig med en massa frågor

Sammanfattningsvis ger de sammanfattande kontrollpanelerna löpande och relevant information för att fatta beslut i rätt tid. Månadsartiklar med Excel-diagram är otillräckliga och för mycket detaljerade data kan överväldigande chefer. Ett lyckligt medium är att fokusera på de tre viktigaste nyckeltalen med historiska data och nedsättningar för relevanta faktorer. Genom att utbilda chefer i hur de använder kontrollpanelen kan de fatta välgrundade beslut och ställa frågor. Instrumentpaneler för sammanfattningar kan förbättra prestanda för webbplatser och appar och öka framgången.

## Författare

Det här dokumentet har skrivits av:

![Gitai Ben-Ammi](assets/gitai-headshot-150.jpg)

**Gitai Ben-Ammi**, rektor konsult på Concentrix Catalyst

[!DNL Adobe Analytics] Champion
