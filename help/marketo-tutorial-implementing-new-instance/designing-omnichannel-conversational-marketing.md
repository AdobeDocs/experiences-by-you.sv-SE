---
title: Design Conversational Marketing för flera kanaler med Dynamic Chat
description: Kom snabbt igång med att utforma konversationsmarknadsföring med Adobe Dynamic Chat, den inbyggda konversationskanalen i Adobe Marketo Engage. I den här självstudiekursen finns användbara recept som kan användas för att implementera exempel på t.ex. bokning av försäljningsmöten, webbplatsinnehållsengagemang och event/webbinarier-marknadsföring.
role: Admin
level: Beginner
doc-type: Article
solution: Marketo Engage
duration: 0
last-substantial-update: 2024-05-23T00:00:00Z
jira: KT-14814
exl-id: 160dfb25-9f54-4dce-a08a-4a8d3c4c5368
source-git-commit: 1205848b1985a99b91f9d4d25e1a79f0df379589
workflow-type: tm+mt
source-wordcount: '1409'
ht-degree: 0%

---

# Designa flerkanalsmarknadsföring med Dynamic Chat

Marknadsförare, er webbplats är oumbärlig för att generera leads, öka konverteringarna och snabba upp säljcyklerna. Genom att engagera besökarna i realtid på er webbplats kan ert säljteam kvalificera köpare effektivare. Adobe Dynamic Chat, den inbyggda chattkanalen i din Adobe Marketo Engage-prenumeration, gör att du kan automatisera konversationer för att utöka Marketo Engage.

I den här självstudiekursen beskrivs tankeprocessen och de primära användningsfall som Sara Barriuso, Marketing Operations Manager på Cornerstone OnDemand, har delat med sig av under Learn from Your Peers. Hon förklarade hur hennes organisation använde Dynamic Chat för att maximera Marketo Engage.

## Integrera konversationsengagemang i er strategi för efterfrågegenerering

Besökarna kan hitta en anledning till att de surfar på webbplatsen. De kanske söker innehåll på dina produkter eller tjänster eller söker efter kontaktinformation för att tala med dina säljare. De kan också vara era kunder som vill ha mer produktinformation. Med chatt kan era webbplatsbesökare själva serva och självkvalificera sig om de är redo att tala med ert säljteam.

När Sara Barriuso implementerade Dynamic Chat ritades hon av den sömlösa integrationen med Marketo Engage och de [fördefinierade aktivitetsutlösarna](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/dynamic-chat-activities){target="_blank"} som aktiverar Marketo Engage-program och vice versa. Hon utvecklade sina samtalsstrategier med tre målgruppssegment i åtanke:

1. Okända prospects: erbjuder aktivt demonstrationssamtal för att generera nya leads.
2. Kända leads/kunder: förläng besökarnas tid att surfa på innehåll och erbjuda demonstrationssamtal för att generera merförsäljning och korsförsäljningsmöjligheter.
3. Prospekt/kunder: skapa personaliserade upplevelser genom att utöka arbetet med marknadsföringskampanjer.


## Viktiga användningsexempel för att börja skapa dialogrutor

För att genomföra dessa strategier har Sara byggt upp sina Dynamic Chat-dialoger kring följande användningsfall:

1. Standarddialogruta för att spara alla: ge ett första alternativ till alla besökare och vägleda dem för att utföra sina uppgifter mer effektivt.

2. Marknadsföring av event- och webbinarieregistrering: locka besökare till webbplatsen att registrera sig för event och webbinarier för att snabbare komma in på köpfasen.

3. Utöka engagemanget i kampanjer: erbjud ytterligare kontext eller åtgärda potentiella frågor när besökare bläddrar i innehåll på webbplatsen.

Låt oss se hur dessa användningsexempel fungerar när Sara visar sin process, från att kartlägga konversationsflödet till att konfigurera dialogrutorna och målinriktningen i Dynamic Chat och Marketo Engage.

### Använd fall 1: Standarddialogruta för att fånga alla webbplatsbesökare

Den här dialogrutan innehåller fem inledande alternativ där besökare kan välja mellan, vilket skapar en självguidad upplevelse som hjälper dem att hitta den information de behöver utifrån sin personlighet. Till att börja med kanske du vill utforska din inkorg&quot;Kontakta oss&quot; för att identifiera vanliga teman och kategorisera dem i de dialogrutealternativ som gäller för dina webbplatsbesökare. Titta på filmen och följ stegen nedan för att skapa din standarddialogruta med allt-i-ett-innehåll:

>[!VIDEO](https://video.tv.adobe.com/v/3429194/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

#### Fas 1

1. Bygg dialogrutan och skapa en testlänk.
2. Lägg till ett mål för att spåra konverteringarna (t.ex. när en demobegäran skickas).
3. Låt 2-3 personer testa det och samla in feedback.

#### Fas 2

1. I &quot;Målgrupp&quot; lägger du till en webbsidas-URL i &quot;Mål&quot; för att ange var dialogrutan ska visas.
2. Lägg till kampanjnamnet, beskrivningen, prioriteten och språket i Inställningar.
3. Klicka på Publish

>[!TAB Marketo Engage]

#### Fas 1

1. Skapa er spårning för Smart Campaign.
2. Använd utlösaren &quot;Söker efter dialog&quot; i &quot;Smart List&quot;. Använd samma mål (t.ex. demobegäran) som du använde Dialog
3. I Flow (Flow) anger du ett Change Program Status-steg för att spåra konverteringen.
4. Källan visas som &#39;dynamicChat&#39;. Du kan skapa en smart kampanj för att uppdatera källan till ett namn som passar dig.

#### Fas 2

1. Testa om spårningen av Smart Campaign när den är aktiv.

>[!ENDTABS]

#### Nivå upp: Kontobaserad marknadsföring

Du kan förbättra standarddialogen för att fånga upp alla genom att införliva branschanpassat innehåll, vilket gör konversationerna ännu mer användbara för besökarna. Du kan t.ex. föreslå branschspecifika rapporter eller fallstudier som besökarna kan hämta. Titta på filmen och följ stegen nedan för att skapa en standarddialogruta för att fånga alla för kontobaserad marknadsföring:

>[!VIDEO](https://video.tv.adobe.com/v/3429195/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

1. Klona standarddialogrutan och byt namn på den.
2. I&quot;Stream Designer&quot; anpassar du dialogmeddelanden till målindustrin (endast en ström + den första frågan).
3. Låt 2-3 personer testa dialogen och samla in feedback.
4. Skapa en testlänk och dela den.
5. I&quot;Målgrupp&quot; lägger du till en webbsideswebbadress där dialogrutan visas och uppdaterar målet till den bransch du vill använda.
6. Lägg till kampanjnamnet, prioriteten för beskrivningen och språket i Inställningar.
7. Klicka på Publish.

>[!TAB Marketo Engage]

1. Skapa er spårning för Smart Campaign och testa målet.
2. Testa spårningen av Smart Campaign igen när du har publicerat dialogrutan.

>[!ENDTABS]

### Användningsfall 2: Marknadsför event- och webbinarieregistrering

Händelser och webbinarier är populära marknadsföringstaktik som B2B-företag använder för att skapa efterfrågan. De erbjuder engagerande upplevelser och avancerad information som lockar potentiella kunder. Genom att koppla webbplatsens besökare till kommande event och webbinarier kan ni kvalificera potentiella kunder ännu snabbare. Att skapa den här dialogen är lågt både ansträngt och billigt och kan snabbt visa på framgång, vilket hjälper er att få stöd från marknadsföringsintressenter för att öka konversationsengagemanget i er flerkanalsplan. Titta på filmen och följ stegen nedan för att skapa en kampanj för event/webbinarium:

>[!VIDEO](https://video.tv.adobe.com/v/3429196/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

#### Fas 1

1. Bygg en mall för dialogrutan&quot;Händelseregistrering&quot; för användning av pågående kampanjer.

#### Fas 2

1. Klona mallen.
2. Kopiera och klistra in text i dialogrutemeddelandet för en ny händelse
3. Uppdatera UTM-parametrar som används i din händelselänk (t.ex. utm_medium=website&amp;utm_source=adobe).
4. Skapa en testlänk, klicka på&quot;Publish&quot; och dela den med den som gjorde begäran.
5. Granska och ge feedback.


>[!TAB Marketo Engage]

#### Fas 1

1. Skapa din spårning för Smart Campaign i webbseminariet/händelsemallen och testa den.

#### Fas 2

1. Lägg till kampanjnamnet i spårningen av Smart Campaign i Marketo Engage och testa det.

>[!ENDTABS]


#### Nivå upp: Registrera kända personer

Du kan ge besökarna en ännu bättre upplevelse genom att registrera dem för dina event och webbinarier utan att de behöver fylla i ett formulär. Personaliserade upplevelser skapar förtroende och visar besökarna att ni minns dem. Låt oss se hur ni kan effektivisera er dialog om event och webbinarier i praktiken.

>[!NOTE]
>Ta hänsyn till den potentiella säkerhetsrisken i vissa skyddsstater/länder och implementera denna personalisering noga genom att rådfråga ditt juridiska team.

>[!VIDEO](https://video.tv.adobe.com/v/3429197/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

1. Klona dialogrutan för kampanj för event/webbinarium.
2. I Stream Designer lägger du till frågekortet&quot;Du har tidigare delat din e-postadress med oss när användaren har svarat&quot;Ja&quot;. Vill du behålla den här för information om evenemanget?&quot;
3. Om de svarar &quot;Ja&quot; - lägg till ett meddelandekort &quot;Du får ett bekräftelsemeddelande via e-post med information om händelsen/webbinariet&quot;.
4. Om de svarar &quot;Nej&quot; - lägg till ett meddelandekort &quot;Fyll i formuläret på registreringssidan&quot;.
5. Skapa en testlänk, klicka på&quot;Publish&quot; och dela den med den som gjorde begäran.
6. Lägg till [e-post är inte tomt] på fliken Målgrupp.

>[!TAB Marketo Engage]

1. Lägg till den här nya dialogrutan i spårningen av Smart Campaign i Marketo Engage och testa den.

>[!ENDTABS]

### Användningsfall 3: Utöka engagemanget för kampanjinnehåll

Tänk dig en fängslande fönstervisning som fångar ögat och drar in dig i en butik. Om en receptionist sedan hjälper dig att välja produkter eller besvara dina frågor, kan du känna dig mer bekväm med att köpa. Om du vill återge den här upplevelsen online kan du visa Dynamic Chat-dialogrutan på webbsidor där era marknadsföringskampanjer dirigerar besökarna. När användare interagerar med webbinnehållet visar Dynamic Chat omedelbart relevanta konversationer, som föreslår ytterligare innehåll eller som åtgärdar potentiella frågor. Detta uppnås genom att utnyttja automatiseringsutlösare för att aktivera Dynamic Chat-kampanjer baserat på användarinteraktion inom Marketo Engage-program. Nu ska vi se hur vi kan ge liv åt det här användningsfallet.

>[!VIDEO](https://video.tv.adobe.com/v/3429199/?learn=on)

Utökat engagemang för kampanjinnehåll - Konfiguration:

>[!VIDEO](https://video.tv.adobe.com/v/3429200/?learn=on)

>[!BEGINTABS]

>[!TAB Dynamic Chat]

1. Generera nya leads för era kampanjer via e-post och sociala kampanjer. I det här exemplet finns hälsoindexundersökningen Talent på varumärkets webbplats.
2. Klona en befintlig dialogmall (t.ex. standarddialogrutan för att fånga upp alla) för att skapa tre dialogrutor för följande scenarier och uppdatera &quot;mål-URL&quot; på fliken &#39;Målgrupp&#39; i enlighet med detta:
   * När webbbesökarna kom från era marknadsföringskanaler och landade på er webbsida.
   * På tacksidan
   * Besökare som återvänder till webbplatsen inom 45 dagar efter att ha deltagit i marknadsföringskampanjen (återmarknadsföring)

>[!ENDTABS]

## Vad kommer härnäst?

* Kartlägg konversationsflödet i [Stream Designer](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/automated-chat/stream-designer){target="_blank"} eller ett flödesdiagram offline.
* Skapa en standarddialogruta för&quot;catch-all&quot; i Dynamic Chat.
* Aktivera konversationerna efter kampanjengagemang genom att använda automatiseringsutlösare i Marketo Engage.


## Författare

{{sara-barriuso}}

{{amy-chiu}}
