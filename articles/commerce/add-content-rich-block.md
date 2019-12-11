---
title: Indholdsrig blok-modul
description: Dette emne omhandler indholdsrig blok-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785415"
---
# <a name="content-rich-block-module"></a>Indholdsrig blok-modul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne omhandler indholdsrig blok-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Et indholdsrig blok-modul er en særlig container, der ét eller flere indholdsrig blok-elementer kan placeres i. Indholdsrig blok-moduler bruges til tekstindhold på en side. Det kan både være oplysninger og kampagneindhold.

Indholdsrig blok-moduler styres af data fra CMS-indholdsstyringssystemet (Content Management System) og kan placeres på en hvilken som helst side. De er separate moduler, der ikke er afhængige af sidekontekst eller andre moduler.

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a>Eksempler på indholdsrig blok-moduler i e-handel

Indholdsrig blok-moduler kan bruges på følgende måder:

* Til at få vist produktfunktioner på en side med produktdetaljer.
* Til oplysninger på en hvilken som helst side. De kan f. eks. indeholde en beskrivelse af fordelene ved fordelskundeprogrammer, leverings- og returneringspolitikker, besvarelse af ofte stillede spørgsmål eller oplysninger om indholdet af "Om os".
* Til tilføjelse af brugerdefinerede meddelelser på en side med produktdetaljer (f. eks. "Gratis levering af ordrer over $50").
* For ansvarsfraskrivelser og kontaktoplysninger på sider med produktdetaljer, indkøbsvognsider, betalingssider og andre sider (f. eks. "Levering og returnering sker i henhold til butikkens politikker").

## <a name="content-rich-block-module-properties"></a>Egenskaber for indholdsrig blok-modul

| Egenskabsbetegnelse     | Værdi                                 | Egenskab |
|-------------------|---------------------------------------|----------|
| Antal kolonner | Et tal mellem **1** og **4**     | Antallet af kolonner i en indholdsrig blok. Der kan være op til fire kolonner. |
| Bredde             | **Tilpas til container** eller **Udfyld skærm** | Hvis værdien er angivet til **Tilpas til container**, begrænses varerne i containeren til containerens bredde. Hvis værdien er angivet til **Udfyld skærm**, begrænses varerne ikke til containerbredden, men kan gå i fuldskærmstilstand. Du kan ændre værdien for at opnå det ønskede layout. |

## <a name="content-rich-block-item-module-properties"></a>Egenskaber for element for indholdsrig blok-modul

| Egenskabsbetegnelse | Værdi          | Beskrivelse |
|---------------|----------------|-------------|
| Afsnit     | Afsnitstekst | Den tekst, der følger med alle elementer for indholdsrig blok. Nogle grundlæggende RTF-funktioner understøttes, f. eks. fed, understreget og kursiv tekst. |

## <a name="add-a-content-rich-block-module-to-a-page"></a>Føje et indholdsrigt blokmodul til en side

Hvis du vil føje et indholdsrig blok-modul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Opret en sideskabelon med navnet **Indholdsskabelon**.
1. Tilføj et indholdsrig blok-modul på pladsen **Hoved** på standardsiden.
1. Tjek skabelonen ind, og publicer den.
1. Brug den indholdsskabelon, som du netop har oprettet, til at oprette en side med navnet **Indholdsside**.
1. Tilføj et indholdsrig blok-modul på pladsen **Hoved** på den nye side.
1. Angiv antallet af kolonner til **2**i egenskaberne for indholdsrig blok-modulet.
1. Vælg **Tilføj et modul**i indholdsrig blok-modulet, og tilføj et element for indholdsrig blok (f. eks. **element1**).
1. Tilføj afsnitstekst i det nye element for indholdsrig blok.
1. Vælg **Tilføj et modul**i indholdsrig blok-modulet, og tilføj et element for indholdsrig blok (f. eks. **element2**).
1. Tilføj afsnitstekst i det nye element for indholdsrig blok.
1. Gem siden, og se ændringerne. Der vises to RTF-blokke i en visning med to kolonner.
1. Tjek siden ind, og publicer den.

> [!NOTE]
> Hvis du tilføjer et tredje element for indholdsrig blok, stables det under de to elementer, som du tidligere har tilføjet. Hvis du ændrer antallet af kolonner og elementer i beholderen, kan du opnå forskellige layout for tekstindhold.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Påmindelsesmodul](add-alert.md)

[Karruselmodul](add-carousel.md)

[Indholdsplaceringsmodul](add-content-placement-modules.md)

[Funktionsmodul](add-feature-module.md)

[Hero-modul](add-hero-module.md)

[Videoafspillermodul](add-video-player.md)

