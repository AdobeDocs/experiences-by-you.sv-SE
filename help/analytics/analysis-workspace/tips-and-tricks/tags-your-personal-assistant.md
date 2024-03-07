---
title: Taggar - din egen assistent
description: Upptäck hur
feature: Dimensions, Projects
role: User
level: Beginner, Intermediate, Experienced
doc-type: Article
duration: 36000
last-substantial-update: 2024-02-22T00:00:00Z
jira: KT-14963
thumbnail: KT-14963.jpeg
source-git-commit: 9be76d73344188d93b826d9195c10e4ee8cc3957
workflow-type: tm+mt
source-wordcount: '1427'
ht-degree: 0%

---


# Taggar - din egen assistent

_Upptäck hur #TAGS kan effektivisera er digitala analys och fungera som din egen assistent för att effektivt hitta det ni behöver. Jeff Bloomer, Adobe Analytics Champion, delar med sig av expertinsikter för att maximera verktygets potential till din fördel._

Alla kommer ihåg att spela en bra lek med taggar eller till och med gömma och söka, tillbaka när vi var barn, eller hur?

![Barn som spelar](assets/kids-playing2.jpeg)

Det bästa var när vi var de som antingen gjorde om det till en bas (tagg) eller gömde det längsta (dölj och sök) tills vi hörde någon skrika &quot;Olly Olly oxen free!&quot; (&quot;Alla I skolen vara fria&quot;, härlett från tyska: &quot;alle alle auch sind frei!&quot;).  I slutändan innebar det att alla andra antingen hade kommit till basen, hittats eller någon fick taggen &quot;det&quot;, och vi kunde fortfarande leka en annan runda!

Det viktiga är om spelet var en tagg eller om det var att gömma sig och söka. Vi spelade en rolig aktivitet där alla hittades om och om igen.

När vi övergår till våra dagliga jobb verkar det som om sökandet efter saker blir mycket mindre äventyrligt och mycket mer långsamt. Men det behöver inte vara om vi är villiga att lägga in lite arbete på första sidan.  En fras som min familj känner väl till är: &quot;Den största smärtan är självförvållad.&quot; Men även om det kan tyckas lite gammaldags nuförtiden finns det en mer känd fras som också är mycket relevant i den här situationen:&quot;En tidsstygn sparar nio.&quot; - Benjamin Franklin

Låt mig börja med att ställa en fråga nu när jag får er uppmärksamhet:


![Hur många av er](assets/how-many-of-you.jpg)

Hur många av er har gjort det här?  Du har börjat söka efter en **dimension**, **datumintervall**, **segment**, eller **beräknat mått** och du blir översvämmad av den här gigantiska listan (se **Figur 1**) av allt du INTE vill ha.  ***Analysis Workspace*** Jag tror att det är till hjälp, men i själva verket har det bara lyckats med att inte vara till hjälp alls.

![bild 1 sökning efter år](assets/tags-example-year.jpg)

*Bild 1 - Sök efter&quot;år&quot;*

Ännu bättre är att du har gått och skapat några *new* **datumintervall** och **segment**, och eftersom de är&quot;så nya&quot; tycker du att de här objekten bör vara snabba och enkla att hitta nästa gång du kommer till ***Adobe arbetsyta***. Har jag rätt?

Jag avskyr att spränga din bubbla, men försök bara gå ***Adobe Analytics*** när du just har skapat alla dina senaste små vänner, och när du kommer tillbaka, har de flesta av dem helt enkelt rymt.  Om du har tur, *kanske* en av dem stannade kvar för att vänta på dig, men resten är redan borta och leker gömma och söka.

## Skriva om regelboken

Så det har varit spelet sedan första dagen, men tänk om vi kunde ändra reglerna?

Tänk om vi kunde skapa en egen personlig assistent för att ändra reglerna för gott?

Allvarligt, det vi pratar om här är TAGS!  Det stämmer!  Det är vår vän till hashtaggen, som tidigare kallades &quot;nummer&quot; och &quot;nummertecken&quot;, precis som vi har sett det på våra telefoner.  Vi musiker kallar det &quot;vass&quot;.

För dig som *riktigt* Behöver du en påminnelse ser det ut så här: **#**

Anledningen till att vi pratar om **#tags** är för att de klumpar ihop sig till den&quot;valfria haken&quot; av&quot;tråkiga och tråkiga, blyga grejer&quot; som alla tenderar att ignorera (som beskrivningar), eftersom vi alla har så bråttom att skapa viktigare saker som, o jag vet inte -

- Arbetsyterapporter
- Segment
- Beräknade mätvärden
- Datumintervall

Ta det lugnt, folk!  Vi har sett och hört alla ursäkter för varför de hoppas över:

&quot;Åh, hej, men det är enkelt.  Jag kan alltid komma tillbaka senare och bara uppdatera de där sakerna på några lunchpauser, eller till och med medan jag sitter på en konferens och *få ordning på allt*&quot;, sa alla som ALDRIG GJORDE.

## Vad finns i verktygslådan

**Adobe** har till och med gjort OSS FOLK en tjänst att skapa en uppsättning #TAGS direkt i lådan, eftersom de var tvungna att börja någonstans.  Jag ska ge dig lite extra kavaetter på bara ett ögonblick, men det jag visar först kommer att ge dig den största rabatten för din buk!

Innan du skapar något av dina egna behöver du först veta hur du söker efter befintliga **taggar**:

![GIF-taggar](assets/tags-gif.gif)

Vare sig du arbetar i ett nytt eller befintligt projekt behöver du bara gå till komponentens sökfält, skriva in en #hashtag tillsammans med ett av dessa huvudtermer (se videon) och trycka på RETUR. Du kan också börja bläddra tills du hittar en identifierbar term.

FÖRSTA CAVEAT: Något att tänka på är om du håller dig till rätt namnkonventioner när du börjar skapa *egen* taggar, nästan var *kapitaliserad* tagg du ser *bör*, och jag ska vara försiktig med det ordet&quot;borde&quot;, är en **Adobe**, taggat objekt som inte finns i paketet.  Det innebär att du måste se till att alla taggar du skapar finns i **gemener**.

## Skapa en egen personlig assistent

Nu återgår vi till det jag sa om en &quot;personlig assistent&quot; tidigare.  Vad händer om jag säger att du kan börja välja några av dina favoritkomponenter och sedan bara göra dem till de ENDA du ser?

![3 skärmtaggar](assets/3-screens-tags.jpg)


1. Om du börjar markera flera komponenter (CTRL+LEFT CLICK) visas vissa ikoner högst upp.  En av dem blir TAGG-ikonen.
1. Klicka på den och sedan öppnas dialogrutan för taggar, där du kan se alla befintliga taggar som är kopplade till de komponenterna.
1. Den kommer från den här skärmen där du sedan kan tilldela **extra/ny** taggar som du kanske vill använda nu.  (Exempel: **test\_v1**)
1. Om du vill lägga till en NY tagg i en komponent trycker du bara på **ANGE** på tangentbordet innan du klickar på knappen SPARA.
1. När du sedan har tilldelat din nya TAGG kan du söka efter den genom att ange hashtag(#) och din nya TAGG.

Ursäkta, men &quot;#tag, du är den!&quot;  Du har just räddat dig mycket mindre ute i framtiden!  Nu får du se var ditt hårda arbete till slut kommer att spela.

## Sätt din personliga assistent i arbete

Säg att vi jobbar i **Resebranschen** och vi sammanställer en rapport för deras **kontorstid**.  Om vi börjar göra en sökning på bara termen&quot;TRAVEL&quot;, kan vi få mycket fler resultat än vi kan behöva.  Faktum är, om vi bara hittade på en **Arbetsyta** Även om de innehåller hälften av de resultat vi behövde skulle komponenterna fortfarande inte vara tillgängliga.

![Korsade taggar](assets/tags-example-travel.jpg)

Men om vi har jobbat med att märka **segment**, **mått** och andra relevanta **komponenter** som vi går och kanske skapa några nya samtidigt som vi skapar våra nya **arbetsyta**, har vi verkligen visat hur vi kan skriva om regelboken till vår fördel!

I det här fallet skapade jag en enkel #tag för alla dessa objekt med namnet #core.

![cha](assets/cha-ching.png)

När du fortsätter att göra detta till en del av dina arbetsvanor och förbättra dina kunskaper att göra detta om och om igen kommer du att inse att #tags blir mer som att ha en egen personlig assistent.

Vill du ha fler exempel från verkligheten? Tänk på följande:

1. Du kan till exempel hitta ett enkelt sätt att hitta **segment** och **datumintervall** for **alla kvartal** in **2023**?

   ![Real world 1](assets/real-world-1.png)

   *Ett extra tips*: Den lilla rutan till höger kan du till och med ändra sorteringsordningen till *alfabetisk*!


1. Naturligtvis använder alla **kampanjspårningskoder** i viss utsträckning.  Om du vill ha en tydlig bild av bara *din* leksaker, överväg att lägga till **#tag** till bara de kärnobjekt du verkligen behöver se och filtrera bort allt annat brus:

![Real world 2](assets/real-world-2.png)

## Gå ut och lek nu!

Visst, det var roligt som barn att gömma sig och söka, men nu är vi vuxna.  Vi har inte tid att ständigt leta efter viktiga saker, så se till att göra dig en tjänst och inte slösa mer tid på att slåss mot verktyget.  Skriv om reglerna och få verktyget att fungera åt dig.

### Tagg, du är det!


## Författare

Det här dokumentet har skrivits av:

![Jeff Bloomer](assets/jeff-bloomer.png)

**Jeff Bloomer**, Manager, Digital Analytics på Kroger Personal Finance

Adobe Analytics Champion







