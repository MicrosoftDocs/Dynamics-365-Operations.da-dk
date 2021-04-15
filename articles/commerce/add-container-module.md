---
title: Modulet Container
description: Dette emne omhandler containermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8e1d2d600a00ab71348fbef2bc2f30cc53bc5314
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797785"
---
# <a name="container-module"></a>Container-modul

[!include [banner](includes/banner.md)]

Dette emne omhandler containermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Et containermodul er et modul, der indeholder andre moduler, som det er vært for. Det primære formål med et containermodul er, via de egenskaber, der er angivet for det, at definere layoutet af de moduler, det indeholder. De pågældende moduler kan f. eks. vises ved siden af hinanden i et layout med to, tre, fire eller seks kolonner. De kan også være begrænset til containerens bredde, eller de kan udfylde skærmen. Der kan også føjes en overskrift til alle containermoduler.

Der understøttes tre containermoduler: container, container med 2 pladser og container med 3 pladser. Der kan placeres moduler af enhver type i disse containere. 

> [!NOTE] 
> Det anbefales, at du altid placerer moduler i et containermodul, så de kan begrænses til containerens bredde.

## <a name="examples-of-container-modules-in-e-commerce"></a>Eksempler på containermoduler i e-handel

- En webstedsopretter ønsker et layout med tre kolonner, hvor der vises tre moduler ved siden af hinanden. Derfor bruger webstedsopretteren et containermodul med tre pladser i containeren.
- En webstedsopretter ønsker et layout med seks kolonner, hvor der vises seks moduler ved siden af hinanden. Derfor bruger webstedsopretteren en containertype med seks kolonner.
- En webstedsopretter vil placere et modul på en side, men vil ikke have, at det udfylder skærmen. Derfor føjer webstedsopretteren modulet til et containermodul og angiver egenskaben for containerens **Bredde** til **Tilpas til container**.

Det følgende billede viser et eksempel på et containermodul, der indeholder et karruselmodul i Commerce-webstedsgeneratoren. I dette eksempel angives egenskaben **Bredde** for containermodulet til **Udfyld skærm**.

![Eksempel på et containermodul](./media/ecommerce-container.PNG)

## <a name="container-module-properties"></a>Egenskaber for containermodul

| Egenskabsbetegnelse     | Værdier | Beskrivende tekst |
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

1. Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.
1. I dialogboksen **Ny skabelon** skal du under **Skabelonnavn** angive **Containerskabelon** og derefter klikke på **OK**.
1. På pladsen **Brødtekst** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. dI dialogboksen **Tilføj modul** skal du vælge modulet **Standardside** og derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den. 
1. Gå til **Sider**, og vælg **Ny** for at oprette en ny side.
1. I dialogboksen **Vælg en skabelon** skal du vælge den videoafspillerskabelon, du har oprettet. Under **Sidenavn** skal du angive **Containerside** og derefter vælge **OK**.
1. På pladsen **Hoved** på den nye side skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.
1. Angiv egenskaben **Antal kolonner** til **1** og egenskaben **Bredde** til **Fyld container** i egenskabsruden for containermodulet.
1. På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Indholdsblok** og derefter **OK**.
1. Konfigurer overskriften, billedet og layoutet i egenskabsruden for indholdsblokmodulet.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden. Der vises ét funktionsmodul, der er tilpasset til containermodulets bredde.
1. Rediger værdien af egenskaben **Antal kolonner** til **3** i egenskabsruden for containermodulet.
1. Føj yderligere to indholdsblokmoduler til containermodulet, og konfigurer dem.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden. Der vises nu tre indholdsblokmoduler ved siden af hinanden.
1. Når du har opnået det ønskede layout, skal du vælge **Udfør redigering** for at tjekke siden ind og derefter vælge **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over modulbibliotek](starter-kit-overview.md)

[Harmonikamodul](add-accordion.md)

[Fanemodul](add-tab.md)

[Karruselmodul](add-carousel.md)

[Tekstblokmodul](add-content-rich-block.md)

[Boksmodul til køb](add-buy-box.md)

[Indkøbskurvsmodul](add-cart-module.md)

[Betalingsmodul](add-checkout-module.md)

[Overskriftsmodul](author-header-module.md)

[Sidefodsmodul](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]