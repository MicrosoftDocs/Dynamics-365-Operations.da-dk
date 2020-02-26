---
title: Gitteregenskaber
description: I dette emne beskrives flere stærke funktioner i gitterkontrolelementet. Den nye gitterfunktion skal være aktiveret, hvis der skal være adgang til disse egenskaber.
author: jasongre
manager: AnnBe
ms.date: 01/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b49d7823f48bcc9cdbb56b87d5fa72d46ddfa15c
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019691"
---
# <a name="grid-capabilites"></a>Gitteregenskaber

[!include [banner](../includes/banner.md)]

Det nye gitterkontrolelement omfatter en række nyttige og effektive funktioner, der kan bruges til at forbedre brugernes produktivitet, oprette mere interessante visninger af dine data og få meningsfuld indsigt i dine data. Denne artikel dækker følgende funktioner: 

-  Beregner totaler
-  Gruppering af data
-  Skrive forud i forhold til systemet
-  Evaluere matematiske udtryk 

## <a name="calculating-totals"></a>Beregner totaler
I Finance and Operations-apps har brugerne mulighed for at få vist totaler nederst i numeriske kolonner i gitre. Disse totaler vises i en sektion med sidefod nederst i gitteret. 

### <a name="showing-the-grid-footer"></a>Visning af gitterets sidefod
Hvert gitter i tabelformat i Finance and Operations-apps har en sidefod nederst i gitteret, som kan vise værdifulde oplysninger, der er relateret til de data, der vises. Disse oplysninger omfatter: 
-  Antallet af markerede rækker i tabellen (når der er valgt mere end én post)
-  Samlede beløb nederst i konfigurerede numeriske kolonner
-  Antallet af rækker i datasættet 

Denne sidefod er som standard skjult, men den kan let aktiveres. Hvis du vil have vist sidefoden for et gitter, skal du højreklikke på kolonneoverskriften i gitteret og vælge indstillingen **Vis sidefod**. Når sidefoden er aktiveret for et bestemt gitter, vil denne indstilling blive husket, indtil brugeren vælger at skjule sidefoden, hvilket kan gøres ved at højreklikke på en kolonneoverskrift og vælge **Skjul sidefod**.  Bemærk, at handlingen **Vis sidefod/Skjul sidefod** forventes at få ny placering i en senere opdatering. 

### <a name="specifying-columns-with-totals"></a>Angive kolonner med totaler
I øjeblikket vil ingen kolonner blive konfigureret til at vise totaler som standard. Dette betragtes i stedet for som en aktivitet til engangsopsætning, der svarer til at justere kolonnebredden i gitre. Når du har angivet, at du vil have vist totaler for en kolonne, vil denne indstilling blive husket, næste gang du besøger siden.  

Du kan konfigurere en kolonne på to måder for at vise en total: 
1.  Højreklik på den kolonne, du er interesseret i at se en total for, og vælg **Total for denne kolonne**. Med denne handling udføres tre ting. For det første vil den gøre sidefoden synlig. For det andet vil den gemme din præference om at få vist en total for denne kolonne. For det tredje vil denne handling starte en beregning af totaler for denne kolonne og evt. andre, som du tidligere har konfigureret for at få vist totaler. Den tid, det tager at få vist en total, er direkte relateret til størrelsen på det datasæt, du sammentæller.  

2.  Når sidefoden er blevet vist, kan du også klikke på knappen **Vis total** i sidefoden nederst i den kolonne, du gerne vil have vist en total for. Hvis der ikke er nogen konfigurerede kolonner, vil knappen **Vis total** være synlig for alle numeriske kolonner. Når der er konfigureret mindst én kolonne til totaler, er knapperne **Vis total** kun tilgængelige, når der peges eller fokuseres. Denne handling gemmer blot din præference for at få vist en total i denne kolonne ved fremtidige besøg på denne side, og tilstanden er angivet af den tankestreg, der vises i kolonnen i sidefoden (eller en total vil straks blive vist, hvis datasættet er tilstrækkeligt lille).

Hvis du laver en fejl og ikke længere vil have vist en total i en bestemt kolonne, skal du højreklikke på kolonnen og vælge **Skjul total** eller vælge knappen **Skjul total** i sidefoden i den pågældende kolonne. Denne præference vil også blive gemt til fremtidige besøg på siden. 

### <a name="calculating-totals"></a>Beregner totaler
Når du kommer til en side, hvor sidefoden er synlig, og der allerede er konfigureret kolonner for totaler, vises totalerne muligvis ikke i sidefoden. Funktionsmåden afhænger af størrelsen af datasættet på siden. Hvis datasættet er tilstrækkeligt lille, vises totaler automatisk sammen med antallet af rækker i datasættet. Hvis der er bindestreger i sidefoden under de kolonner, du har konfigureret til totaler, er datasættet for stort til, at systemet kan vise totaler med det samme, og der skal udføres en eksplicit handling for at beregne totalerne. Det gør du ved at klikke på knappen **Beregn** i sidefoden eller højreklikke på en kolonne, du vil beregne totalen for, og vælge **Total for denne kolonne**.  

Hvis beregningen tager for lang tid, kan du annullere operationen ved at klikke på knappen **Annuller**. Nogle gange vil datasættet imidlertid være for stort til at kunne beregne totaler (en begrænsning, der er pålagt af organisationen), og du vil i stedet blive mindet om at filtrere dine data mere.

Totaler opdateres automatisk, efterhånden som du opdaterer, sletter eller opretter rækker i datasættet.  

## <a name="grouping-data"></a>Gruppering af data
Forretningsbrugere har ofte brug for at udføre ad hoc-analyse af data. Dette kan gøres ved at eksportere data til Microsoft Excel, og ved brug af pivottabeller tillader funktionen **Gruppering** i gitre i tabelform brugere at organisere deres data på interessante måder i Finance and Operations-apps. Da denne funktion udvider funktionen **Totaler**, giver **Gruppering** også mulighed for at få meningsfuld indsigt i dataene ved at levere subtotaler på gruppeniveau.

Hvis du vil bruge denne funktion, skal du højreklikke på den kolonne, du vil gruppere efter, og vælge **Gruppér efter denne kolonne**. Denne handling sorterer dataene efter den valgte kolonne, føjer en ny Gruppér efter-kolonne til starten af gitteret og indsætter "overskriftsrækker" i starten af hver gruppe. Disse kolonneoverskrifter indeholder følgende oplysninger om hver enkelt gruppe: 
-  Dataværdi for gruppen 
-  Kolonneetiket. Dette vil være særligt nyttigt, når der understøttes flere niveauer af gruppering.  
-  Antallet af datarækker i denne gruppe
-  Subtotaler for enhver kolonne, der er konfigureret til at vise totaler

Når [Gemte visninger](saved-views.md) er aktiveret, kan denne gruppering gemmes via tilpasning som del af en visning for at få hurtig adgang, når du næste gang besøger siden.  

Hvis du vælger **Gruppér efter denne kolonne** i en anden kolonne, erstattes den oprindelige gruppering, da kun grupperingsniveau understøttes i 10.0.9/Platform Update 33.

Hvis du vil fortryde gruppering i et gitter, skal du højreklikke på grupperingskolonnen og vælge **Opdel gruppe**.  


## <a name="evaluating-math-expressions"></a>Evaluere matematiske udtryk
Som en produktivitet-booster kan brugeren angive matematiske formler i numeriske celler i et gitter i stedet for at skulle udføre beregningen i en app uden for systemet. Du kan f.eks. angive **=15\*4** og tabulere ud af feltet. Systemet evaluerer udtrykket og gemmer værdien "60" for feltet.

Hvis du vil have systemet til at genkende en værdi som et udtryk, skal du starte værdien med et lighedstegn (**=**). Yderligere oplysninger om de understøttede operatorer og syntaks finder du under [Understøttede matematiske symboler](http://redhivesoftware.github.io/math-expression-evaluator/#supported-maths-symbols).  
