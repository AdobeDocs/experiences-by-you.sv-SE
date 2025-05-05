---
title: Skapa ett dataflödesdiagram för att förstå er Marketing Tech Stack
description: Lär dig hur du skapar ett diagram över"lead- och datakällor" för att förstå datauniversum, för att kunna granska och åtgärda instansen på ett effektivt sätt.
feature-set: Marketo Engage
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00Z
jira: KT-13877
thumbnail: KT-13877.jpeg
hide: false
exl-id: 088bdcf1-4e49-44a7-ac78-a03742ff680b
source-git-commit: 1205848b1985a99b91f9d4d25e1a79f0df379589
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# Skapa ett dataflödesdiagram för att förstå er marknadsföringsteknologi

Som administratör som tar över en [!DNL Marketo Engage]-instans som har varit aktiv i flera år, är det som en uppgift som är omöjlig att granska och rensa instansen effektivt. När Kelly Jo Horton, [!DNL Adobe] [!DNL Marketo Champion] (2019) gick in i en väletablerad instans tog hon sig an den här utmaningen genom att [skapa ett diagram över&quot;Lead and data sources&quot; ](https://nation.marketo.com/t5/employee-blogs/understand-your-marketing-technology-and-data-create-this/ba-p/296774){target="_blank"} för att bekanta sig med datavohela. I den här självstudiekursen får du lära dig hur du skapar ett eget dataflödesdiagram genom att bygga vidare på de exempel som Kelly Jo Horton har delat. Lär känna ditt MarTech-ekosystem!

## Varför skapa ett arkitekturdiagram för den ärvda instansen?

1. **Bekanta dig med den marknadsföringsteknologi du ärvt från en Live-instans.** Alla marknadsföringsoperationsansvariga/plattformsOperations-hanterare uppmuntras att göra den här övningen när de börjar på ett nytt företag. Med den här processen kan administratörsanvändare se hela bilden av data och aktiviteter som skickas från externa integreringar till [!DNL Marketo Engage] och enkelt felsöka API-felen.
2. **Bekanta dig med viktiga intressenter som hanterar externa integreringar.** Ett tips som Kelly Jo Horton använder för att snabbt identifiera intressenter är att referera till listan med API-användare.
   1. **Navigera till fliken Integration>LaunchPoint i avsnittet Admin.** Läs mer om hur du navigerar till fliken LaunchPoint: [Skapa en anpassad tjänst för användning med REST API](https://experienceleague.adobe.com/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api.html?lang=sv-SE){target="_blank"}.
   2. Sök efter API-användningsstatistik efter API-användare på fliken Integrering > Webbtjänster i API Call Information. Genom att klicka på API-anropsnumret kan du visa de specifika enskilda anrop som görs av varje användare.

## Hur man gör detta visuella dataflödesdiagram

### Steg 1: Aktuellt tillståndsdiagram

Skapa ett diagram för aktuellt läge. Här är ett exempel:

![Aktuellt statusdiagram](/help/marketo-tutorial-inherited-instance/_assets/data-flow-diagram/Current_State_Lead_Data_Sources_KellyJo_Horton.png){align="center"}


### Steg 2: Diagram över framtida tillstånd

Skapa ett diagram för framtidens tillstånd som kan användas när tekniska och systemrelaterade färdplaner presenteras för icke-tekniska intressenter. Här är ett exempel:

![Framtida tillståndsdiagram](/help/marketo-tutorial-inherited-instance/_assets/data-flow-diagram/Future-State-Lead-Data-Sources-KellyJo-Horton.png){align="center"}

### Steg 3: Teknisk version

Skapa en teknisk version som visar detaljer som API-användarnamnet för varje integrering, en kort beskrivning av den typ av data som skickas till [!DNL Marketo Engage] eller hämtas från [!DNL Marketo Engage] samt ett detaljdiagram över eventuella mellanliggande programflöden och utlösare.  Här är ett exempel:

![Teknisk version](/help/marketo-tutorial-inherited-instance/_assets/data-flow-diagram/Lead-Data-Source-Diagram-KellyJo-Horton.png){align="center"}


## Vad kommer härnäst?

**Kom igång med exempel:**
Ladda ned ett av exempeldiagrammen för dataflöde för att kartlägga det aktuella läget för er marknadsföringsteknologi, dataflöde, person och person, eller skapa ett diagram för hela datamängden från grunden när ni granskar instansen:


<table style="table-layout:fixed">
   <tr>  
      <td style="border: 0;">
      <div style="text-align: center;">
          <a href="./_assets/downloads/Current_Future_State_Lead_Data_Sources.zip">
            <strong> Aktuellt läge och framtida tillstånd </strong>
         </a>
      </div>
      </td>
      <td style="border: 0;">
      <div style="text-align: center;">
         <a href="./_assets/downloads/Detailed_Layers_by_Functional_Category_Stacked_Technologies.zip">
         <strong> Detaljerade lager efter funktionskategori </strong>   
         </a>
      </div>
      </td>
      <td style="border: 0;">
         <div style="text-align: center;">
         <a href="./_assets/downloads/Lead_Data_Source.zip">
           <strong> Lead and Data Source Flow </strong>  
         </a>
         </div>
       </td> 
       <td style="border: 0;">
         <div style="text-align: center;">
         <a href="./_assets/downloads/Simple_World_Class_Stage_Stack.zip">
          <strong> Förenklat diagram </strong>  
         </a>
         </div>
        </td>  
   </tr>
   <tr>
    <td style="border: 0;">
         <div>
          <img alt="Diagram över aktuellt läge och framtida tillstånd" src="./_assets/Thumbnail_Current-Future State Lead_Data Sources_KellyJo_Horton.png"/>
         </a>
      </div>
      </td>
      <td style="border: 0;">
         <div>
         <a href="./_assets/downloads/Detailed_Layers_by_Functional_Category_Stacked_Technologies.zip">
         <img alt="Detaljerade lager efter funktionskategoridiagram" src="./_assets/Thumbnail_Detailed_Layers_by_Functional_Category_Stacked_Technologies_KellyJo_Horton.png" />
       </a>
         </div>
      </td>
       <td style="border: 0;">
         <div>
            <a href="./_assets/downloads/Lead_Data_Source.zip">
         <img alt="Lead och data - Source Flow Diagram" src="./_assets/Thumbnail_Lead-Data Source Diagram_KellyJo_Horton.png" />
         </a>
         </div>
      </td>
     <td style="border: 0;">
         <div>
            <a href="./_assets/downloads/Simple_World_Class_Stage_Stack.zip">
             <img alt="Förenklat diagram" src="./_assets/Thumbnail_Simple_World_Class_Stage_Stack.png" />
         </a>
         </div>
      </td>
</table>

Det här är några verktyg som du kan använda: draw.io (Google Docs), [!DNL Adobe] XD, Figma, Gliffy (in Confluence)

**Vad händer om det redan finns arkitekturdiagram?** nya teammedlemmar kan ha olika perspektiv. Det är värdefullt att ha nya [!DNL Marketo Engage]-administratörer som utför den här övningen som en del av deras introduktionsprocess och delar den med andra.

## Författare

**Kelly Jo Horton**\
[!DNL Adobe] Marketo Champion (2019)
*Senior Client Partner på Etumos*

![Kelly Jo Horton](/help/marketo-tutorial-inherited-instance/_assets/authors/Customer_Author_Kelly_Jo_Horton.png){width="30%"}

**Amy Chiu**
*Adobe &amp; Retention Marketing Manager,[!DNL Adobe]*

(/help/marketo-tutorial-inherited-instance/_assets/authors/[!DNL Adobe]_Author_Amy_Chiu.png){width=30%}
