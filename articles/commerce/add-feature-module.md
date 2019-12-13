---
title: Funktionsmodul
description: Dette emne omhandler funktionsmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785277"
---
# <a name="feature-module"></a>Funktionsmodul 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne omhandler funktionsmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Et funktionsmodul bruges til markedsføring af produkter eller kampagner via en kombination af billeder og tekst. En forhandler kan f. eks. føje et funktionsmodul til en side med produktdetaljer for at fremhæve produktets funktioner.

Et funktionsmodul styres af data fra CMS (Content Management system). Det er et separat modul, der ikke er afhængige af andre moduler på siden. Et funktionsmodul kan placeres på alle sider på websteder, hvor en forhandler ønsker at markedsføre eller vise noget (f. eks. produkter, salg eller funktioner).

## <a name="examples-of-feature-modules-in-e-commerce"></a>Eksempler på funktionsmoduler i e-handel

Et funktionsmodul kan bruges på følgende sider:

- På en side med produktdetaljer til visning af produktfunktioner
- På startsiden til visning af produkter
- På en kategoriside til fremhævning af en produktkategori

## <a name="feature-module-properties"></a>Egenskaber for funktionsmodul

| Egenskabsbetegnelse     | Værdier | Beskrivelse |
|-------------------|--------|-------------|
| Billede             | Billedfil | Der kan bruges et billede til markedsføring af produktet eller kampagnen. Der kan overføres et billede til billedgalleriet, eller der kan bruges et eksisterende billede. |
| Overskrift           | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Alle funktionsmoduler kan have en overskrift. Overskrift koden **H2** bruges som standard til overskriften. Koden kan dog ændres, så den opfylder tilgængelighedskravene. |
| Afsnit         | Afsnitstekst | Funktionsmoduler understøtter afsnitstekst i RTF-format. Nogle grundlæggende RTF-funktioner understøttes, f. eks. fed, understreget og kursiv tekst samt hyperlinks. Nogle af disse funktioner kan tilsidesættes af det sidetema, der anvendes på modulet. |
| Binding              | Linktekst, URL-adresse for link, ARIA-mærkat (Accessible Rich Internet Applications) og **Åbn link under ny fane** | Funktionsmoduler understøtter et eller flere links til "handlingsplaner". Hvis der tilføjes et link, er linktekst, en URL-adresse og en ARIA-mærkat påkrævet. ARIA-mærkater skal være beskrivende for at imødekomme tilgængelighedskravene. Links kan konfigureres, så de åbnes under en ny fane. |
| Billedplacering   | **Højre**, **Venstre**, **Øverst**eller **Nederst** | Denne egenskab definerer placeringen af billedet i forhold til teksten. Hvis **Højre** f.eks. er valgt, vises billedet til højre for teksten. |
| Størrelse af billedkolonne | En værdi mellem **1** og **12** | Denne egenskab definerer billedets størrelse i forhold til teksten. Størrelsen udtrykkes som et antal kolonner på siden. Der er 12 kolonner på en side. Billedet og teksten har som standard samme størrelse (seks kolonner hver). Størrelsen kan dog justeres efter behov. |

## <a name="add-a-feature-module-to-a-new-page"></a>Føje et funktions til en ny side 

Hvis du vil føje et funktionsmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Gå til **Skabeloner**, og opret en sideskabelon med navnet **funktionsskabelon**.
1. Tilføj et funktionsmodul på pladsen **Hoved** på standardsiden.
1. Tjek skabelonen ind, og publicer den.
1. Brug den funktionsskabelon, som du netop har oprettet, til at oprette en side med navnet **funktionsside**.
1. Vælg pladsen **Hoved** på standardsiden, vælg ellipseknappen (**...**), og vælg derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** under **Vælg moduler** skal du vælge et funktionsmodul og derefter vælge **OK**.
1. Vælg funktionsmodulet i dispositionstræet til venstre.
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

[Hero-modul](add-hero-module.md)

[Videoafspillermodul](add-video-player.md)
