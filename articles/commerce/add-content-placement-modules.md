---
title: Indholdsplaceringsmodul
description: Dette emne omhandler indholdsplacerings- og element for indholdsplacering-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785294"
---
# <a name="content-placement-module"></a>Indholdsplaceringsmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne omhandler indholdsplacerings- og element for indholdsplacering-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Et indholdsplaceringsmodul er en særlig container, som andre moduler kan placeres i i et bestemt layout. Indholdsplaceringsmoduler understøtter følgende modultyper som underordnede moduler: element for indholdsplacering, velkomstelement for konto, ordreelement for konto, ønskelisteelement for konto og profilelement for konto.

Indholdsplaceringsmoduler udleder data fra de underordnede moduler, som de understøtter. Derfor kan indholdsplaceringsmoduler bruges på forskellige måder, afhængigt af de moduler der føjes til det.

Element for indholdsplacering-moduler bruger både billeder og tekst til at vise kampagner, politikker og produktfunktioner. Et element for indholdsplacering-modul kan f.eks. bruges på en hjemmeside til at vise butikkens politikker eller leveringsoplysninger. Element for indholdsplacering-moduler styres af data fra CMS-indholdsstyringssystemet (Content Management System) og kan placeres på en hvilken som helst side. De kan dog kun bruges inde i et indholdsplaceringsmodul.

## <a name="examples-of-content-placement-modules-in-e-commerce"></a>Eksempler på indholdsplaceringsmoduler i e-handel

* Indholdsplaceringsmoduler, der indeholder elementer for indholdsplacering-moduler, kan bruges på en hjemmeside eller på marketingsider til at vise produktfunktioner, kampagner, butikspolitikker, leveringsoplysninger samt andre oplysninger gennem både billeder og tekst.
* Indholdsplaceringsmoduler, der indeholder element for indholdsplacering-moduler, kan bruges på sider med produktdetaljer til at vise produktfunktioner.
* Indholdsplaceringsmoduler, der indeholder velkomstelement for konto- eller ordreelement for konto-moduler, kan bruges på sider til kontostyring.

## <a name="content-placement-module-properties"></a>Egenskaber for indholdsplaceringsmodul

| Egenskabsbetegnelse | Værdi | Beskrivelse |
|---------------|-------|-------------|
| Bredde         | **Tilpas til container** eller **Udfyld skærm** | Hvis værdien er angivet til **Tilpas til container**, begrænses varerne inde i indholdsplaceringsmodulet til indholdsplaceringsmodulets bredde. Hvis værdien er angivet til **Udfyld skærm**, begrænses varerne ikke til indholdsplaceringsmodulets bredde, men kan gå i fuldskærmstilstand. |

## <a name="content-placement-item-module-properties"></a>Egenskaber for element for indholdsplacering-modul

| Egenskabsbetegnelse | Værdi | Beskrivelse |
|---------------|-------|-------------|
| Overskrift       | Overskriftstekst og overskriftskoder (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Hvert indholdsplaceringsmodul kan have en overskrift. Egenskaben **Overskrift** understøtter overskriftskoder. Som standard bruges overskriftskoden **H2**, men den kan ændres efter behov for at opfylde tilgængelighedskravene. |
| Afsnit     | Afsnitstekst | Indholdsplaceringsmoduler understøtter afsnitstekst i RTF-format. Nogle grundlæggende RTF-funktioner understøttes, f. eks. fed, understreget og kursiv tekst samt hyperlinks. Nogle af disse funktioner kan tilsidesættes af det sidetema, der anvendes på modulet. |
| Billede         | Billedfil | Der kan knyttes et billede til teksten. |
| Binding          | URL-adresse for link og linktekst | Der kan føjes et link til teksten for at omdirigere brugerne til en bestemt side. |
| Feltstørrelse     | Et tal mellem **1** og **12** | Denne egenskab definerer for hvert element for indholdsplacering det antal pladser, som elementet skal udfylde i indholdsplaceringsmodulet. Den maksimale størrelse på indholdsplaceringsmodulet er 12 pladser. Hvis den samlede feltstørrelse for de første *n* elementer i indholdsplaceringsmodulet overstiger 12 pladser, ombrydes elementerne til næste række. |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a>Føje et indholdsplaceringsmodul, der indeholder et element til indholdsindsættelse, til en side

Hvis du vil føje et indholdsplaceringsmodul, der indeholder et element for indholdsindsættelse-modul, til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Opret en skabelon med navnet **indholdsplaceringsskabelon**.
1. Tilføj et indholdsplaceringsmodul på pladsen **Hoved** på standardsiden.
1. Tilføj et element for indholdsplacering-modul i indholdsplaceringsmodulet.
1. Tjek skabelonen ind, og publicer den.
1. Brug den indholdsplaceringsskabelon, som du netop har oprettet, til at oprette en side med navnet **Indholdsplaceringsside**.
1. Tilføj et indholdsplaceringsmodul på pladsen **Hoved** på den nye side.
1. Tilføj et element for indholdsplacering-modul i indholdsplaceringsmodulet.
1. Vælg et billede, tilføj en overskrift, tilføj et afsnit, tilføj et link, angiv URL-adressen for linket, og angiv feltstørrelsen til **6** i egenskabsruden for element for indholdsplacering-modulet.
1. Gentag trin 7 og 8 for at tilføje et andet element for indholdsplacering-modul med samme feltstørrelse.
1. Gem siden, og se en forhåndsvisning af den. Der vises nu to elementer for indholdsplacering ved siden af hinanden. Du kan justere egenskaben **Feltstørrelse** for hvert element for indholdsplacering-modul eller tilføje flere moduler for at opnå det ønskede layout.
1. Tjek siden ind, og publicer den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Påmindelsesmodul](add-alert.md)

[Karruselmodul](add-carousel.md)

[Indholdsrig blok-modul](add-content-rich-block.md)

[Funktionsmodul](add-feature-module.md)

[Hero-modul](add-hero-module.md)

[Videoafspillermodul](add-video-player.md)
