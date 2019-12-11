---
title: Hero-modul
description: Dette emne omhandler hero-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785379"
---
# <a name="hero-module"></a>Hero-modul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne omhandler hero-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Et hero-modul bruges til markedsføring af produkter eller kampagner via en kombination af billeder og tekst. En forhandler kan f. eks. tilføje et hero-modul til startsiden på et e-handels-websted for at markedsføre et nyt produkt og tiltrække kundernes opmærksomhed.

Et hero-modul styres af data fra CMS (Content Management system). Det er et separat modul, der ikke er afhængige af andre moduler på siden. Et hero-modul kan placeres på alle sider på websteder, hvor en forhandler ønsker at markedsføre eller vise noget (f. eks. produkter, salg eller funktioner).

## <a name="examples-of-hero-module-in-e-commerce"></a>Eksempler på hero-moduler i e-handel

- Et hero-modul kan bruges på startsiden for et e-handels-websted til at fremhæve kampagner og nye produkter.
- Et hero-modul kan bruges på siden med produktdetaljer til at vise produktoplysninger.
- Der kan placeres flere hero-moduler i et karruselmodul for at fremhæve flere produkter eller kampagner.

## <a name="hero-module-properties"></a>Egenskaber for hero-modul

| Egenskabsbetegnelse  | Værdier | Beskrivelse |
|----------------|--------|-------------|
| Billede          | Billedfil | Der kan bruges et billede til at vise et produkt eller en kampagne. Der kan overføres et billede til billedgalleriet, eller der kan bruges et eksisterende billede. |
| Overskrift        | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Alle hero-moduler kan have en overskrift. Overskrift koden **H2** bruges som standard til overskriften. Koden kan dog ændres, så den opfylder tilgængelighedskravene. |
| Afsnit      | Afsnitstekst | Hero-moduler understøtter afsnitstekst i RTF-format. Nogle grundlæggende RTF-funktioner understøttes, f. eks. fed, understreget og kursiv tekst samt hyperlinks. Nogle af disse funktioner kan tilsidesættes af det sidetema, der anvendes på modulet. |
| Binding           | Linktekst, URL-adresse for link, ARIA-mærkat (Accessible Rich Internet Applications) og **Åbn link under ny fane** | Hero-moduler understøtter et eller flere links til "handlingsplaner". Hvis der tilføjes et link, er linktekst, en URL-adresse og en ARIA-mærkat påkrævet. ARIA-mærkater skal være beskrivende for at imødekomme tilgængelighedskravene. Links kan konfigureres, så de åbnes under en ny fane. |
| Placering af tekst | **Øverst til venstre**, **Øverst til højre**, **Øverst centreret**, **Nederst til venstre**, **Nederst til højre**, **Nederst i midten**, **Centreret til venstre**, **Centreret til højre** eller **Centreret centreret** | Denne egenskab definerer placeringen af billedet i forhold til teksten. Hvis **Højre** f.eks. er valgt, vises billedet til højre for teksten. |
| Teksttema     | **Lys** eller **Mørk** | Der kan defineres et farveskema for teksten på basis af baggrundsbilledet. Hvis billedet f. eks. har en mørk baggrund, kan der anvendes et lyst tema for at gøre teksten mere synlig og for at overholde tilgængelighedskravene til farvekontrast. |
| Graduering       | **Sand** eller **Falsk** | Der kan anvendes en graduering på billedet til at overholde tilgængelighedskravene til farvekontrast. |

## <a name="add-a-hero-module-to-a-new-page"></a>Føje et hero-modul til en ny side

Hvis du vil føje et hero-modul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Gå til **Skabeloner**, og opret en sideskabelon med navnet **hero-skabelon**.
1. Tilføj et hero-modul på pladsen **Hoved** på standardsiden.
1. Tjek skabelonen ind, og publicer den.
1. Brug den hero-skabelon, som du netop har oprettet, til at oprette en side med navnet **hero-side**.
1. Vælg pladsen **Hoved** på standardsiden, vælg ellipseknappen (**...**), og vælg derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** under **Vælg moduler** skal du vælge hero-modulet og derefter vælge **OK**.
1. Vælg hero-modulet i dispositionstræet til venstre.
1. Vælg **Tilføj et billede** i egenskabsruden til højre. Vælg derefter et eksisterende billede, eller overfør et nyt billede.
1. Vælg **Overskrift**.
1. Tilføj overskriftsteksten i dialogboksen **Overskrift**, vælg overskriftsniveauet, og vælg derefter **OK**.
1. Tilføj tekst efter behov under **RTF-tekst**.
1. Vælg **Tilføj handlingslink**.
1. Tilføj linktekst, en URL-adresse og en ARIA-mærkat for linket i dialogboksen **Handlingslink**, og vælg derefter **OK**.
1. Gem siden, og se dine ændringer.
1. Tjek siden ind, og publicer den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Påmindelsesmodul](add-alert.md)

[Karruselmodul](add-carousel.md)

[Indholdsrig blok-modul](add-content-rich-block.md)

[Indholdsplaceringsmodul](add-content-placement-modules.md)

[Funktionsmodul](add-feature-module.md)

[Videoafspillermodul](add-video-player.md)
