---
title: Modulet Container
description: Dette emne omhandler containermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 22a09b61fbe3bd1cca96011d3fb81a12ef1bc844
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697054"
---
# <a name="container-module"></a>Modulet Container

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne omhandler containermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Et containermodul er et modul, der indeholder andre moduler, som det er vært for. Det er den mest generiske container, der bruges i Dynamics 365 Commerce. Det primære formål med et containermodul er, via de egenskaber, der er angivet for det, at definere layoutet af de moduler, det indeholder. De pågældende moduler kan f. eks. vises ved siden af hinanden i et layout med to, tre, fire eller seks kolonner. De kan også være begrænset til containerens bredde, eller de kan udfylde skærmen. Der kan også føjes en overskrift til alle containermoduler.

Der findes tre standardtyper af containermoduler: container, container med to pladser og container med tre pladser. Der kan placeres moduler af enhver type i disse containere. Der findes også særlige typer containermoduler, f. eks. karrusel, indholdsrig blok, indholdsplacering, indkøbsvogn, betaling, købefelt, sidehoved og sidefod. Disse containere har bestemte formål, og det er kun bestemte understøttede modultyper, der kan placeres i dem.

Det anbefales, at du placerer moduler i en container, så de kan begrænses til containerens bredde.

## <a name="examples-of-container-modules-in-e-commerce"></a>Eksempler på containermoduler i e-handel

- En webstedsopretter ønsker et layout med tre kolonner, hvor der vises tre moduler ved siden af hinanden. Derfor bruger webstedsopretteren et containermodul med tre pladser i containeren.
- En webstedsopretter ønsker et layout med seks kolonner, hvor der vises seks moduler ved siden af hinanden. Derfor bruger webstedsopretteren en containertype med seks kolonner.
- En webstedsopretter vil placere et modul på en side, men vil ikke have, at det udfylder skærmen. Derfor føjer webstedsopretteren modulet til et containermodul og angiver egenskaben for containerens **Bredde** til **Tilpas til container**.

## <a name="container-module-properties"></a>Egenskaber for containermodul

| Egenskabsbetegnelse     | Værdier | Beskrivelse |
|-------------------|--------|-------------|
| Overskrift           | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Der kan angives en valgfri overskrift til containeren. Overskrift koden **H2** bruges som standard til overskriften. Koden kan dog ændres, så den opfylder tilgængelighedskravene. |
| Bredde             | **Tilpas til container** eller **Udfyld skærm** | Hvis værdien er angivet til **Tilpas til container** (standardværdien), begrænses modulerne i containeren til containerens bredde. Hvis værdien er angivet til **Udfyld skærm**, begrænses modulerne ikke til containeren, men kan udfylde skærmen. |
| Antal kolonner | **1**, **2**, **3**, **4**, **6** eller **12** | Denne egenskab definerer antallet af kolonner i containeren. En container kan indeholde op til 12 kolonner. |

## <a name="container-with-2-slots"></a>Container med 2 slots

Containertypen med to pladser er optimeret til et layout med to kolonner. Denne type container har to pladser, der giver mulighed for at få vist de moduler, den indeholder, ved siden af hinanden.

Yderligere egenskaber kan bruges til at optimere layoutet til forskellige visningsporte (mobilenheder, tablets, computere osv.). De enkelte kolonners bredde kan defineres for hver visningsport. Følgende indstillinger for kolonnebredde er tilgængelige:

- **75 %/25 %** – det første modul har kolonnebredden 75 %, og det andet modul har kolonnebredden 25 %. Der findes også en indstilling på **25 %/75 %**.
- **50 %/50 %** – begge moduler har samme kolonnebredde.
- **67 %/33 %** – det første modul har kolonnebredden 67 %, og det andet modul har kolonnebredden 33 %. Der findes også en indstilling på **33 %/67 %**.
- **100 %** – begge moduler har fuld kolonnebredde. Derfor stables modulerne lodret i en enkelt kolonne. Selvom dette layout med én kolonne går imod hensigten med en container med to pladser, kan det være at foretrække for nogle visningsporte (f. eks. ekstrasmå visningsporte som mobilenheder).

### <a name="container-with-2-slots-properties"></a>Container med egenskaber for to pladser

| Egenskabsbetegnelse                   | Værdier | Beskrivelse |
|---------------------------------|--------|-------------|
| Overskrift                         | Overskriftstekst og overskriftskode | Der kan angives en valgfri overskrift til containeren. |
| Konfiguration af ekstra lille visningsport | **25 %/75 %**, **75 %/25 %**, **50 %/50 %**, **67 %/33 %**, **33 %/67 %** eller **100 %** | Denne egenskab definerer layoutet for ekstrasmå visningsporte. |
| Konfiguration af lille visningsport   | **25 %/75 %**, **75 %/25 %**, **50 %/50 %**, **67 %/33 %**, **33 %/67 %** eller **100 %** | Denne egenskab definerer layoutet for små visningsporte, f.eks. mobilenheder. |
| Konfiguration af mellemstor visningsport  | **25 %/75 %**, **75 %/25 %**, **50 %/50 %**, **67 %/33 %**, **33 %/67 %** eller **100 %** | Denne egenskab definerer layoutet for mellemstore visningsporte, f.eks. tablets. |
| Konfiguration af stor visningsport   | **25 %/75 %**, **75 %/25 %**, **50 %/50 %**, **67 %/33 %**, **33 %/67 %** eller **100 %** | Denne egenskab definerer layoutet for store visningsporte, f.eks. computere. |

## <a name="container-with-3-slots"></a>Container med 3 slots

Containertypen med tre pladser er optimeret til et layout med tre kolonner.

Yderligere egenskaber kan bruges til at optimere layoutet for forskellige visningsporte. De enkelte kolonners bredde kan defineres for hver visningsport. Følgende indstillinger for kolonnebredde er tilgængelige:

- **33 %/33 %/3 3%** – alle tre moduler har samme kolonnebredde.
- **50 %/25 %/25 %** – det første modul har kolonnebredden 50 %, og hvert af de resterende to moduler har en kolonnebredde på 25 %. Der findes også indstillinger på **25 %/50 %/25 %** og **25 %/25 %/50 %**.
- **16 %/16 %/67 %** – hvert af de første modul har kolonnebredden 16 %, og det tredje modul har en kolonnebredde på 67 %. Der findes også indstillinger på **16 %/67 %/16 %** og **67 %/16 %/16 %**.

### <a name="container-with-3-slots-properties"></a>Container med egenskaber for tre pladser

| Egenskabsbetegnelse                   | Værdier | Beskrivelse |
|---------------------------------|--------|-------------|
| Overskrift                         | Overskriftstekst og overskriftskode | Der kan føjes en valgfri overskrift til containeren. |
| Konfiguration af ekstra lille visningsport | **33 %/33 %/33 %**, **50 %/25 %/25 %**, **25 %/50 %/25 %**, **25 %/25 %/50 %**, **16 %/16 %/67 %**, **16 %/67 %/16 %** eller **67 %/16 %/16 %** | Denne egenskab definerer layoutet for ekstrasmå visningsporte. |
| Konfiguration af lille visningsport   | **33 %/33 %/33 %**, **50 %/25 %/25 %**, **25 %/50 %/25 %**, **25 %/25 %/50 %**, **16 %/16 %/67 %**, **16 %/67 %/16 %** eller **67 %/16 %/16 %** | Denne egenskab definerer layoutet for små visningsporte, f.eks. mobilenheder. |
| Konfiguration af mellemstor visningsport  | **33 %/33 %/33 %**, **50 %/25 %/25 %**, **25 %/50 %/25 %**, **25 %/25 %/50 %**, **16 %/16 %/67 %**, **16 %/67 %/16 %** eller **67 %/16 %/16 %** | Denne egenskab definerer layoutet for mellemstore visningsporte, f.eks. tablets. |
| Konfiguration af stor visningsport   | **33 %/33 %/33 %**, **50 %/25 %/25 %**, **25 %/50 %/25 %**, **25 %/25 %/50 %**, **16 %/16 %/67 %**, **16 %/67 %/16 %** eller **67 %/16 %/16 %** | Denne egenskab definerer layoutet for store visningsporte, f.eks. computere. |

## <a name="add-a-container-module-to-a-page"></a>Føje et containermodul til en side

Hvis du vil føje et containermodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Opret en sideskabelon med navnet **containerskabelon**.
1. Tilføj et containermodul på pladsen **Hoved** på standardsiden.
1. Føj et funktionsmodul til containermodulet.
1. Tjek skabelonen ind, og publicer den.
1. Brug den containerskabelon, som du netop har oprettet, til at oprette en side med navnet **containerside**.
1. Tilføj et containermodul på pladsen **Hoved** på den nye side.
1. Angiv egenskaben **Antal kolonner** til **1** og egenskaben **Bredde** til **Tilpas til container** i egenskabsruden for containermodulet.
1. Føj et funktionsmodul til containermodulet.
1. Konfigurer en overskrift i egenskabsruden for funktionsmodulet.
1. Gem siden, og se en forhåndsvisning af den. Der vises ét funktionsmodul, der er tilpasset til containermodulets bredde.
1. Rediger værdien af egenskaben **Antal kolonner** til **3** i egenskabsruden for containermodulet.
1. Føj yderligere to funktionsmoduler til containermodulet.
1. Gem siden, og se en forhåndsvisning af den. Du kan nu se tre funktionsmoduler, der vises ved siden af hinanden.
1. Når du har opnået det ønskede layout, skal du tjekke siden ind og publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Karruselmodul](add-carousel.md)

[Indholdsrig blok-modul](add-content-rich-block.md)

[Indholdsplaceringsmodul](add-content-placement-modules.md)

[Købefeltmodul](add-buy-box.md)

[Indkøbsvognmodul](add-cart-module.md)

[Betalingsmodul](add-checkout-module.md)

[Overskriftsmodul](author-header-module.md)

[Sidefodsmodul](author-footer-module.md)
