---
title: Gitteregenskaber
description: I dette emne beskrives flere stærke funktioner i gitterkontrolelementet. Den nye gitterfunktion skal være aktiveret, hvis der skal være adgang til disse egenskaber.
author: jasongre
manager: AnnBe
ms.date: 02/10/2020
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
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7136edba828bf97b6e0c8d2a698b884640d680e5
ms.sourcegitcommit: 880f617d1d6e95eccbed762c7ea04398553c2ec0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036259"
---
# <a name="grid-capabilities"></a>Gitteregenskaber

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Det nye gitterkontrolelement omfatter en række nyttige og effektive funktioner, der kan bruges til at forbedre brugernes produktivitet, oprette mere interessante visninger af dine data og få meningsfuld indsigt i dine data. Denne artikel dækker følgende funktioner: 

-  Beregner totaler
-  Gruppering af data
-  Skrive forud i forhold til systemet
-  Evaluere matematiske udtryk 

## <a name="calculating-totals"></a>Beregner totaler
I Finance and Operations-apps har brugerne mulighed for at få vist totaler nederst i numeriske kolonner i gitre. Disse totaler vises i en sektion med sidefod nederst i gitteret. 

### <a name="showing-the-grid-footer"></a>Visning af gitterets sidefod
Der er et sidefodsområde i bunden af alle tabelgitre i Finance and Operations-apps. Sidefoden kan vise værdifulde oplysninger, der er relateret til de data, der vises i gitteret. Her er nogle eksempler på sådanne oplysninger:

- Antallet af markerede rækker i tabellen (når der er valgt mere end én post)
- Samlede beløb nederst i konfigurerede og numeriske kolonner
- Antallet af rækker i datasættet 

Denne sidefod er som standard skjult, men den kan let aktiveres. Hvis du vil have vist sidefoden for et gitter, skal du højreklikke på kolonneoverskriften i gitteret og vælge indstillingen **Vis sidefod**. Når sidefoden er aktiveret for et bestemt gitter, vil denne indstilling blive husket, indtil brugeren vælger at skjule sidefoden, hvilket kan gøres ved at højreklikke på en kolonneoverskrift og vælge **Skjul sidefod**.  Bemærk, at handlingen **Vis sidefod/Skjul sidefod** forventes at få ny placering i en senere opdatering. 

### <a name="specifying-columns-with-totals"></a>Angive kolonner med totaler
I øjeblikket vil ingen kolonner blive konfigureret til at vise totaler som standard. Dette betragtes i stedet for som en aktivitet til engangsopsætning, der svarer til at justere kolonnebredden i gitre. Når du har angivet, at du vil have vist totaler for en kolonne, vil denne indstilling blive husket, næste gang du besøger siden.  

Du kan konfigurere en kolonne på to måder for at vise en total: 

- Højreklik i den kolonne, som du ønsker at se en total for, og vælg dernæst **Total for denne kolonne**. Denne handling resulterer i tre hændelser:

    1. Sidefoden bliver synlig. 
    2. Din præference om at få vist en total for denne kolonne gemmes. 
    3. En beregning af totaler for denne kolonne og alle andre kolonner, som du tidligere har konfigureret for at få vist totaler, indledes. Den tid, der kræves for at få vist en total, afhænger af størrelsen på det datasæt, du vil beregne totalen for.

- Når sidefoden er synlig, skal du vælge **Vis tabel** i sidefodsområdet nederst i den kolonne, du vil have vist en total for. Hvis der ikke er nogen konfigurerede kolonner, vil knappen **Vis total** være tilgængelig for alle numeriske kolonner. 

    Når der er konfigureret mindst én kolonne til totaler, er knapperne **Vis total** kun tilgængelige, når der peges eller fokuseres. Ved at vælge **Vis total** gemmer du din præference for at få vist en total i denne kolonne, således at præferencen anvendes under fremtidige besøg på siden. I sidefoden er denne status angivet med en tankestreg, der vises i kolonnen. (Hvis datasættet er lille nok, vises totalen i stedet med det samme.)

Hvis du laver en fejl og ikke længere vil have vist en total i en bestemt kolonne, skal du højreklikke på kolonnen og vælge **Skjul total** eller vælge knappen **Skjul total** i sidefoden i den pågældende kolonne. Denne præference vil også blive gemt til fremtidige besøg på siden. 

### <a name="calculating-totals"></a>Beregner totaler
Når du kommer til en side, hvor sidefoden er synlig, og der allerede er konfigureret kolonner for totaler, vises totalerne muligvis ikke i sidefoden. Funktionsmåden afhænger af størrelsen af datasættet på siden. Hvis datasættet er tilstrækkeligt lille, vises totaler automatisk sammen med antallet af rækker i datasættet. Hvis der er bindestreger i sidefoden under de kolonner, du har konfigureret til totaler, er datasættet for stort til, at systemet kan vise totaler med det samme, og der skal udføres en eksplicit handling for at beregne totalerne. Det gør du ved at klikke på knappen **Beregn** i sidefoden eller højreklikke på en kolonne, du vil beregne totalen for, og vælge **Total for denne kolonne**.  

Hvis beregningen tager for lang tid, kan du annullere operationen ved at klikke på knappen **Annuller**. Nogle gange vil datasættet imidlertid være for stort til at kunne beregne totaler (en begrænsning, der er pålagt af organisationen), og du vil i stedet blive mindet om at filtrere dine data mere.

Totaler opdateres automatisk, efterhånden som du opdaterer, sletter eller opretter rækker i datasættet.  

## <a name="grouping-data"></a>Gruppering af data
Forretningsbrugere har ofte brug for at udføre ad hoc-analyse af data. Dette kan gøres ved at eksportere data til Microsoft Excel, og ved brug af pivottabeller tillader funktionen **Gruppering** i gitre i tabelform brugere at organisere deres data på interessante måder i Finance and Operations-apps. Da denne funktion udvider funktionen **Totaler**, giver **Gruppering** også mulighed for at få meningsfuld indsigt i dataene ved at levere subtotaler på gruppeniveau.

Hvis du vil bruge denne funktion, skal du højreklikke på den kolonne, du vil gruppere efter, og vælge **Gruppér efter denne kolonne**. Denne handling sorterer dataene efter den valgte kolonne, føjer en ny "Gruppér efter kolonne" til starten af gitteret og indsætter "overskriftsrækker" i starten af hver gruppe. Disse kolonneoverskrifter indeholder følgende oplysninger om hver enkelt gruppe: 
-  Dataværdi for gruppen 
-  Kolonneetiket (disse oplysninger vil især være nyttige, når der ydes støtte til grupper på flere niveauer.)
-  Antallet af datarækker i denne gruppe
-  Subtotaler for enhver kolonne, der er konfigureret til at vise totaler

Når [Gemte visninger](saved-views.md) er aktiveret, kan denne gruppering gemmes via tilpasning som del af en visning for at få hurtig adgang, når du næste gang besøger siden.  

Hvis du vælger **Gruppér efter denne kolonne** for en anden kolonne, erstattes den oprindelige gruppering, da kun et grupperingsniveau understøttes i version 10.0.9 med platformsopdatering 33.

Hvis du vil fortryde gruppering i et gitter, skal du højreklikke på grupperingskolonnen og vælge **Opdel gruppe**.  


## <a name="evaluating-math-expressions"></a>Evaluere matematiske udtryk
Som en produktivitetsbooster kan brugerne indtaste matematiske formler i numeriske celler i et gitter. De behøver ikke at foretage beregningen i en app uden for systemet. Hvis du f.eks. angiver **=15\*4** og derefter trykker på tasten **Tab** for at flytte ud af feltet, evalueres udtrykket, og værdien **60** gemmes for feltet.

Hvis du vil have systemet til at genkende en værdi som et udtryk, skal du starte værdien med et lighedstegn (**=**). Yderligere oplysninger om de understøttede operatorer og syntaks finder du under [Understøttede matematiske symboler](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).  
