---
title: Synkroniserar fält för ursprungliga CRM-anslutningar
description: Lär dig hur ni kan effektivisera er integrering med CRM genom att strategiskt välja de CRM-fält som Marketo Engage ska använda. Utför datamappningsövningen för att identifiera de fält som behövs för en smidig CRM-synkronisering som hjälper sälj- och marknadsföringsteam att hålla sig uppdaterade.
role: Admin
level: Beginner
doc-type: Article
solution: Marketo Engage
duration: 0
last-substantial-update: 2024-05-04T00:00:00Z
jira: KT-14811
thumbnail: KT-14811.jpeg
exl-id: 42b7ca3d-e445-4c11-ad3d-d4e70c101c8e
source-git-commit: 4ea2f60e2bfa658add920c947f5455fe0572ce04
workflow-type: tm+mt
source-wordcount: '1569'
ht-degree: 0%

---

# Synkroniserar fält för ursprungliga CRM-anslutningar

Använder du Salesforce eller Microsoft Dynamics i din organisation? I så fall kan ni med Marketo Engage CRM-kontakter (t.ex. Salesforce, Microsoft Dynamics och Veeva) samordna marknadsförings- och säljaktiviteter genom att smidigt dela relevant information mellan Marketo Engage och CRM. Innan du konfigurerar den inledande CRM-synkroniseringen måste du identifiera de fält som du vill synkronisera mellan de två systemen för att din Marketo Engage-databas ska vara ren.

Lär dig mer om hur du utför den här övningen med bästa praxis som Adobe Professional Services föreslår. Följ med för att förstå standardfält och anpassade fält och dokumentera deras relationer mellan Marketo Engage och din CRM.

## Identifiera fält som ska synkroniseras innan du integrerar CRM med Marketo Engage

När du integrerar CRM med Marketo Engage behöver du förmodligen inte synkronisera alla CRM-fält till Marketo Engage. Att vara strategisk i de fält ni behöver kan hjälpa Marketo Engage att bearbeta dataflödet effektivare.

Den inledande synkroniseringen mellan Marketo Engage och CRM-systemet skapar automatiskt associationer för de flesta befintliga standardfält (t.ex. e-post, förnamn/efternamn, företag). Dessutom synkroniserar anslutningsprogrammet [Anpassade fält](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/field-management/custom-field-type-glossary){target="_blank"} för dina leads, kontakter, konton och säljprojekt genom att skapa nya fält i Marketo Engage som automatiskt mappas till dessa fält från CRM.

Att identifiera och organisera de fält som du vill synkronisera från CRM innan du utför den första synkroniseringen är ett viktigt steg i konfigurationsprocessen för Native Connector. Vi hänvisar till detta som en dataordlisteövning, som hjälper dig att minimera antalet dubblettfält som skapas och som gör att efterföljande ommappningssteg går så smidigt som möjligt. Den här övningen omfattar vanligtvis indata från marknadsförings- och säljteam samt CRM-administratören för att säkerställa att endast relevanta fält synkroniseras med din Marketo Engage-instans.

## Så här skapar du din datamordlista

I allmänhet är det bästa sättet att bara synkronisera CRM-fält som behövs i marknadsföringssyfte. Börja med den här övningen för att ordna fälten från CRM som måste mappas till Marketo Engage och kör den första CRM-synkroniseringen korrekt första gången.

>[!NOTE]
>Om du har anpassade fält i CRM som redan har ett motsvarande anpassat fält i Marketo Engage innan den första synkroniseringen börjar, skapas ett nytt dubblettfält i Marketo Engage för CRM-fältet. Du kan mappa om CRM-fältet till det ursprungliga Marketo Engage-fältet och dölja dubblettfältet när den första synkroniseringen är klar, men du måste kontakta [Adobe kundsupport](https://experienceleague.adobe.com/en/docs/customer-one/using/home#create-a-support-ticket-with-admin-console){target="_blank"} för att göra det. Mer information finns i steg 7.

**Steg 1:** Skapa en grov lista över fält som för närvarande är tillgängliga i CRM och markera om du vill att de ska visas i Marketo Engage.

* Inkludera feedback från CRM-administratörer, marknadsförare och säljare i beslutsprocessen.
* Dokumentera API-namn och fälttyper för varje fält
* Bestäm vilken åtkomstnivå Marketo Engage ska ha för dessa fält (t.ex. skrivskyddad eller skrivskyddad)


**Steg 2:** Granska [Admin > Fälthanteringssektionen](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/field-management/view-field-mappings-between-marketo-and-salesforce){target="_blank"} i din Marketo Engage-instans för att identifiera anpassade fält som tidigare skapats direkt i systemet som du vill inkludera i synkroniseringen.

* Dokumentera API-namn och fälttyper för varje fält.
* Ange fält som redan har ett motsvarande fält i CRM.
* Ange fält som inte redan har ett motsvarande fält i CRM.


**Steg 3:** Börjar skapa dataordlistan med standardkartfälten

* Eftersom Marketo Engage använder en platt databas rekommenderar vi att du formaterar din datamordlista enligt följande:

   * Första kolumnen: fältnamn i Marketo Engage
   * Andra kolumnen: Marketo Engage API-namn
   * Tredje kolumnen: [Fälttyp för Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/field-management/custom-field-type-glossary){target="_blank"} (t.ex. Boolean, Valuta, Datum)
   * I efterföljande kolumner upprepar du CRM-objekttyperna (Lead, Contact, Account, Opportunity) med en extra kolumn för den åtkomstnivå som du vill att Marketo Engage ska ha (t.ex. Read, Write, Edit)
  <br>

  Här är ett exempel på hur det skulle se ut:
  ![Data Dictionary-tabell](/help/marketo-tutorial-implementing-new-instance/assets/data_dictionary.png){width="100%" zoomable="yes"}


* Börja med att lägga till standardfälten som automatiskt mappas för CRM:

   * [Salesforce](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/default-salesforce-field-mapping){target="_blank"}
   * [Microsoft Dynamics](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/microsoft-dynamics-sync-details/default-dynamics-field-mapping){target="_blank"}
   * [Veeva](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/veeva-crm-sync/sync-details/default-veeva-field-mapping){target="_blank"}

* Bekräfta att varje standardfält i Marketo Engage matchar det fält i CRM som du vill synkronisera med. Fältet &quot;Avbeställ&quot; i Marketo Engage kan till exempel vara fältet &quot;Avbeställ via e-post&quot; i CRM.
* Justera CRM API-namnet, behörigheterna och [datatypen](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/field-management/custom-field-type-glossary){target="_blank"} om det behövs.

**Steg 4:** Lägg till ytterligare fält i datamappningslistan

* Inkludera visningsnamn, CRM-behörighet och datatyp för varje fält.
* Om det finns ett fält i CRM men inte Marketo Engage fyller du i Marketo Engage-visnings- och API-namnen med samma värden från CRM-fältet.
* Om det finns ett fält i Marketo Engage men inte i CRM, fyller du i CRM-visningsnamnet med det önskade värdet, men låter CRM-API-namnet vara tomt tills fältet har skapats.
* Om det finns motsvarande fält i båda systemen inkluderar du dem på samma rad och anger att de måste mappas om i avsnittet &quot;Anteckningar&quot; längst till höger i ditt Data Dictionary-blad.

>[!NOTE]
>Om du planerar att skapa ett synkroniseringsfilterfält ([Salesforce](https://nation.marketo.com/t5/product-blogs/instructions-for-creating-a-custom-sync-rule/ba-p/242758){target="_blank"}) | [ Microsoft Dynamics ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/custom-dynamics-sync-filter-details/create-a-custom-dynamics-sync-filter){target="_blank"}) måste du ta med det i det här steget, men lämna API-namnen tomma tills fältet skapas i CRM.

**Steg 5:** Granska datalexikonet med CRM-administratören

* Skapa fält i CRM för dem som redan finns i Marketo Engage och uppdatera datamappningslistan med Display- och API-namnen för det nya CRM-fältet.
* Utför fältmappning mellan lead- och kontaktobjekt i CRM ([Salesforce](https://nation.marketo.com/t5/product-blogs/instructions-for-creating-a-custom-sync-rule/ba-p/242758){target="_blank"}) | [Microsoft Dynamics ](https://community.dynamics.com/blogs/post/?postid=8a91d93e-2181-45dd-a8fb-1092010bc8f1){target="_blank"}). När en lead konverteras till en kontakt säkerställer detta att fälten kan konsolideras till ett enda fält i Marketo Engage.
* Kontrollera att Marketo Sync Profile har rätt behörighet för varje fält enligt ordlistan:
   * [Ange profilbehörigheter i Salesforce](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/setup/enterprise-unlimited-edition/step-2-of-3-create-a-salesforce-user-for-marketo-enterprise-unlimited#set-profile-permissions){target="_blank"}
   * [Ange profilbehörigheter i Microsoft Dynamics](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/microsoft-dynamics-365-with-s2s-connection/step-2-of-3-set-up#create-application-user-in-microsoft){target="_blank"}
   * [Ange profilbehörigheter i veva](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/microsoft-dynamics-365-with-s2s-connection/step-2-of-3-set-up#create-application-user-in-microsoft){target="_blank"}

**Steg 6:** Utför den inledande synkroniseringen

* Se till att alla fält som du vill synkronisera med Marketo Engage har lämplig behörighet i CRM enligt dataordlistan.
* Se till att alla fält som du **inte** vill synkronisera med Marketo Engage är [dolda i Marketo Sync Profile](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/hide-a-salesforce-field-from-the-marketo-sync){target="_blank"}. Det är mycket enklare att lägga till nya fält i synkroniseringen senare än att ta bort fält som har synkroniserats oavsiktligt.
* Ansluter du CRM till fältet Synkroniseringsfilter? Om du synkroniserar med Salesforce kontaktar du Adobe kundsupport för att se till att filterfunktionen är aktiverad innan du startar den första synkroniseringen.


**Steg 7:** Granska avsnittet Fälthantering i Marketo Engage

* Bekräfta/uppdatera visnings- och API-namnen för de nya synkroniserade fälten.
* Identifiera eventuella dubblettfält som kan behöva mappas om. Duplicerade fält förekommer i några scenarier:
   * Anpassade fält i CRM skapar ett nytt (eventuellt duplicerat) fält i Marketo Engage första gången de synkroniseras om det redan finns ett motsvarande fält i Marketo Engage.
   * Anpassade fält med endast Marketo-Engage (dvs. fält som skapats direkt i Marketo Engage) och du kan ha ett motsvarande fält synkroniserat från CRM.



**Steg 8:** Kontakta Adobe kundsupport för att utföra ommappning om dubblettfält visas

* Kontakta support med följande information för fält som behöver mappas om:
   * Visnings- och API-namn för nya dubblettfält som skapas av CRM.
   * Visningsnamn för det Marketo Engage-fält som du vill mappa CRM-fältet till.
   * Se exemplet [HERE](https://nation.marketo.com/t5/knowledgebase/re-mapping-sfdc-marketo-fields/ta-p/299284){target="_blank"}.
* När ommappningen är klar granskar du API-namnen för de ommappade fälten i Marketo Engage och uppdaterar värdena i Data Dictionary-klassens &quot;API-namn&quot;-kolumn för att se till att den innehåller den mest korrekta informationen.

## Vad händer nu?

* Bygg din Data Dictionary för att ordna fälten för CRM-integrering.
* Bekanta dig med den inledande synkroniseringsprocessen för CRM

>[!BEGINTABS]

>[!TAB Salesforce]

Läs om hur Marketo Engage och Salesforce samarbetar för att synkronisera dina sälj- och marknadsföringsdata.

>[!VIDEO](https://video.tv.adobe.com/v/3424719/?learn=on)

+++**Länkar som används i videon:**

* [Förstå Salesforce-synkroniseringen](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/understanding-the-salesforce-sync){target="_blank"}

* [Lägg till Marketo-fält i Salesforce (Enterprise/Unlimited)](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/setup/enterprise-unlimited-edition/step-1-of-3-add-marketo-fields-to-salesforce-enterprise-unlimited){target="_blank"}

* [Skapa en Marketo-användare i Salesforce (Enterprise/Unlimited)](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/setup/enterprise-unlimited-edition/step-2-of-3-create-a-salesforce-user-for-marketo-enterprise-unlimited){target="_blank"}

* [Anslut Marketo och Salesforce(Enterprise/Unlimited)](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/setup/enterprise-unlimited-edition/step-3-of-3-connect-marketo-and-salesforce-enterprise-unlimited){target="_blank"}

* [Användare måste konfigurera det anslutna programmet på Salesforce-sidan innan de kan fortsätta till Marketo- och Salesforce-synkronisering.](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/log-in-using-oauth-2-0){target="_blank"}

* [Salesforce-synkroniseringsstatus](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/salesforce-sync-status){target="_blank"}

* [Dölj och visa ett fält](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/field-management/hide-and-unhide-a-field){target="_blank"}

* [Självstudiekurs: Lär dig hur du synkroniserar Marketo med ditt CRM](https://experienceleague.adobe.com/en/docs/marketo-learn/tutorials/lead-and-data-management/crm-sync-learn){target="_blank"}

+++

>[!TAB Microsoft Dynamics]

Lär dig hur synkroniseringen av Microsoft Dynamics 365 fungerar och konfigurera inställningarna på rätt sätt så att de två systemen kan kommunicera med varandra.

>[!VIDEO](https://video.tv.adobe.com/v/3424737/?learn=on)

+++**Länkar som används i videon:**

* [Förstå Microsoft Dynamics Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"}

* [Hämta Marketo Lead Management Solution](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/download-the-marketo-lead-management-solution){target="_blank"}

* [Uppdatera Marketo-lösningen för Microsoft Dynamics](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/update-the-marketo-solution-for-microsoft-dynamics){target="_blank"}

* [Bevilja medgivande för klient-ID och appregistrering](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/grant-consent-for-client-id-and-app-registration)

* [Verifiera Microsoft Dynamics Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/validate-microsoft-dynamics-sync){target="_blank"}

* [Synkroniseringsstatus](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/microsoft-dynamics-sync-details/sync-status){target="_blank"}

* [Åtgärda problem med synkronisering av Dynamics-validering](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/fix-dynamics-validation-sync-issues){target="_blank"}

* [Skapa ett synkroniseringsfilter för anpassad Dynamics](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/custom-dynamics-sync-filter-details/create-a-custom-dynamics-sync-filter.html){target="_blank"}

* [Visa URL för organisationstjänsten](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/view-the-organization-service-url){target="_blank"}

* [Redigerar fält som ska synkroniseras innan de tas bort i Dynamics](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/microsoft-dynamics-sync-details/editing-fields-to-sync-before-deleting-them-in-dynamics){target="_blank"}

* [Självstudiekurs: Lär dig hur du synkroniserar Marketo med ditt CRM](https://experienceleague.adobe.com/en/docs/marketo-learn/tutorials/lead-and-data-management/crm-sync-learn){target="_blank"}

+++

>[!ENDTABS]

### Författare

{{peter-livadas}}

{{amy-chiu}}
