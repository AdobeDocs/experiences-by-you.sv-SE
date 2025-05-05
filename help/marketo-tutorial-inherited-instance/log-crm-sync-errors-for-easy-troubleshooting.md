---
title: Logga CRM-synkroniseringsfel för enkel felsökning
description: Lär dig hur du använder en logg med CRM Sync-fel för att undersöka CRM-synkroniseringsproblem och få det att fungera smidigt.
feature-set: Marketo Engage
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00Z
jira: KT-13875
thumbnail: KT-13875.jpeg
hide: false
exl-id: 6a38f5dd-5d25-43d8-a1d3-e75ab396e555
source-git-commit: 1205848b1985a99b91f9d4d25e1a79f0df379589
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---

# Logga CRM-synkroniseringsfel för felsökning

Som [!DNL Marketo Engage]-administratör bör kontrollen av om din instans är synkroniserad med CRM vara en nyckeldel av din [dagliga rutin](https://nation.marketo.com/t5/champion-program-blogs/my-marketo-morning-routine-tips-for-driving-marketing-operation/ba-p/247508){target="_blank"}. Medan avsnittet [Meddelanden](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/notification-types.html?lang=sv-SE){target="_blank"} (finns i det övre högra hörnet av [!DNL Marketo Engage] -gränssnittet) är där du börjar hitta och undersöka vanliga synkroniseringsproblem, finns det ett proffstips som kan hjälpa dig att hantera instansens hälsa på ett organiserat sätt. [!DNL Adobe] Marketo Champion (2019-2022), Amy Goldfine rekommenderar administratörsanvändare att föra en logg över CRM Sync-fel för att underlätta felsökning.

![Skärmbild på fliken Synkroniseringsfel](/help/marketo-tutorial-inherited-instance/_assets/Marketo_Engage_Admin_Salesforce_Sync_Errors_Tab.png)

## Varför registrera CRM-synkroniseringsfel?

Genom att logga CRM-synkroniseringsfelen kan [!DNL Marketo Engage]-administratörer granska problem och trender med CRM-administratörerna för att åtgärda grundorsaken. Följ stegen nedan för att dokumentera dina CRM-synkroniseringsproblem för din instans.

## Spara en logg över CRM-synkroniseringsfel

Innan du börjar hämtar du loggmallen [Synkroniseringsfel i CRM](/help/marketo-tutorial-inherited-instance/_assets/downloads/Adobe-Marketo-Engage_CRM-Sync-Error-Log-Template.xlsx).

**Steg 1:** Gå till avsnittet *[!UICONTROL Admin]* i [!DNL Marketo Engage]. Under *[!UICONTROL Integration]* klickar du på *[!DNL Salesforce]*, *[!DNL Microsoft Dynamics]* eller *[!DNL Veeva]*, beroende på vilken [!DNL CRM] du använder, och sedan på fliken *[!UICONTROL Sync Errors]*.

**Steg 2:** Du kan välja att [exportera poster med fel som en [!DNL CSV] fil via [!UICONTROL Filter]-panelen](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/salesforce-sync/salesforce-sync-errors.html?lang=sv-SE#filter-sync-errors){target="_blank"}. Om du bara har några timmar på dig kan du kopiera och klistra in direkt från fliken *[!UICONTROL Sync Errors]*.

**Steg 3:** Observera datumet då felet inträffade.

**Steg 4:** Ange antalet personposter som påverkas av felet. (Ibland genererar CRM endast ett fel för en person. Ibland finns det många som har samma fel på en gång.)

**Steg 5:** Observera e-postadressen till en person som påverkas av felet. Detta gör det enkelt för dig att referera till och diskutera felen med CRM-administratören.

**Steg 6:** Klistra in länkar till personposten i [!DNL Marketo Engage] och [!UICONTROL CRM Lead/Contact]-posten för den personen.

**Steg 7:** I den sista kolumnen klistrar du in den faktiska texten för felet.

## Vad kommer härnäst?

**Identifiera felkoder:** Om du vill förstå felkoderna ska du leta upp beskrivningarna i utvecklardokumentationen [Svarsnivåtabellen för felkoder](https://developers.marketo.com/rest-api/error-codes/#response_level_error_codes){target="_blank"} och hitta de vanligaste stegen för att åtgärda felen.

## Författare

**Amy Goldfine**\
[!DNL Adobe] Marketo Champion(2019-2022)
*Grundare, MarketingOpsAdvice.com*

![Amy Goldfine](/help/marketo-tutorial-inherited-instance/_assets/authors/Customer_Author_Amy_Goldfine.png){width="25%"}

**Amy Chiu**
*Adobe &amp; Retention Marketing Manager på[!DNL Adobe]*

![Amy Chiu](/help/marketo-tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width="25%"}
