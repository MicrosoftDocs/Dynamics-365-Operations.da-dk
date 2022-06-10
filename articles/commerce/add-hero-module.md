---
title: Indholdsblokmodul
description: Dette emne omhandler indholdsblokmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 85d101c73e723d246e1f6af61acb51f6d6516a79
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780353"
---
# <a name="content-block-module"></a>Indholdsblokmodul

[!include [banner](includes/banner.md)]

Dette emne omhandler indholdsblokmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Et indholdsblokmodul bruges til markedsføring af produkter eller kampagner via en kombination af billeder og tekst. En forhandler kan f.eks. føje et indholdsblokmodul til startsiden på et e-handels-websted for at markedsføre et nyt produkt og tiltrække kundernes opmærksomhed.

Et indholdsblokmodul styres af data fra CMS (Content Management system). Det er et separat modul, der ikke er afhængige af andre moduler på siden. Et indholdsblokmodul kan placeres på alle sider på websteder, hvor en forhandler ønsker at markedsføre eller vise noget (f.eks. produkter, salg eller funktioner).

## <a name="examples-of-content-block-module-in-e-commerce"></a>Eksempler på et indholdsblokmodul i e-handel

- Et indholdsblokmodul kan bruges på startsiden for et e-handels-websted til at fremhæve kampagner og nye produkter.
- Et indholdsblokmodul kan bruges på siden med produktdetaljer til at vise produktoplysninger.
- Der kan placeres flere indholdsblokmoduler i et karruselmodul for at fremhæve flere produkter eller kampagner.

## <a name="content-block-modules-and-themes"></a>Indholdsblokmoduler og temaer

Indholdsblokmoduler kan understøtte forskellige layout og typografier, der er baseret på et tema. Fabrikam-temaet understøtter f.eks. tre layoutvariationer af et indholdsblokmodul: helt, funktion og flise. Layoutet Helt viser et billede i baggrunden med tekstoverlejring. Funktionslayoutet viser et billede og tekst ved siden af hinanden. Fliselayoutet giver mulighed for flere indholdsblokke i et fliseformat.

Desuden kan temaet vise forskellige egenskaber for hvert layout. En temaudvikler kan opbygge flere layout med flere typografier vha. indholdsblokmodulet.

Følgende billede viser et eksempel på et indholdsblokmodul med et Helte-layout.

![Eksempel på et hero-modul.](./media/Hero.PNG)

Følgende billede viser et eksempel på et indholdsblokmodul med et funktionslayout.

![Eksempler på funktionsmoduler.](./media/Feature.PNG)

## <a name="content-block-module-properties"></a>Egenskaber for indholdblokmodul

| Egenskabsbetegnelse  | Værdier | Betegnelse |
|----------------|--------|-------------|
| Billede          | Billedfil | Der kan bruges et billede til at vise et produkt eller en kampagne. Der kan overføres et billede til billedgalleriet, eller der kan bruges et eksisterende billede. |
| Overskrift        | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Alle hero-moduler kan have en overskrift. Overskrift koden **H2** bruges som standard til overskriften. Koden kan dog ændres, så den opfylder tilgængelighedskravene. |
| Afsnit      | Afsnitstekst | Hero-moduler understøtter afsnitstekst i RTF-format. Nogle grundlæggende RTF-funktioner understøttes, f. eks. fed, understreget og kursiv tekst samt hyperlinks. Nogle af disse funktioner kan tilsidesættes af det sidetema, der anvendes på modulet. |
| Binding           | Linktekst, URL-adresse for link, ARIA-mærkat (Accessible Rich Internet Applications) og **Åbn link under ny fane** | Hero-moduler understøtter et eller flere links til "handlingsplaner". Hvis der tilføjes et link, er linktekst, en URL-adresse og en ARIA-mærkat påkrævet. ARIA-mærkater skal være beskrivende for at imødekomme tilgængelighedskravene. Links kan konfigureres, så de åbnes under en ny fane. |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a>Egenskaber for indholdsblokmodul, der vises af Fabrikam-temaet 

| Egenskabsnavn  | Værdier | Beskrivelse |
|----------------|--------|-------------|
| Placering af tekst | **Venstre**, **Højre**, **Midt** | Denne egenskab definerer placeringen af teksten i billedet. Den gælder kun for Helte-layoutet. |
| Teksttema     | **Lys** eller **Mørk** | Der kan defineres et farveskema for teksten på basis af baggrundsbilledet. Hvis billedet f. eks. har en mørk baggrund, kan der anvendes et lyst tema for at gøre teksten mere synlig og for at overholde tilgængelighedskravene til farvekontrast. Den gælder kun for Helte-layoutet.|
| Billedplacering       | **Venstre**, **Højre** | Denne egenskab specificerer, om billedet skal være til venstre eller højre for teksten. Den gælder kun for funktionslayoutet.  |

## <a name="add-a-content-block-module-to-a-new-page"></a>Føj et indholdsblokmodul til en ny side

Hvis du vil føje et hero-modul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Gå til **Skabeloner**, og opret en sideskabelon med navnet **Indholdsblokskabelon**.
1. Tilføj et hero-modul på pladsen **Hoved** på standardsiden.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.
1. Brug den hero-skabelon, som du netop har oprettet, til at oprette en side med navnet **Indholdsblokside**.
1. Vælg pladsen **Hoved** på standardsiden, vælg ellipseknappen (**...**), og vælg derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge hero-modulet og derefter **OK**.
1. Vælg indholdsblokmodulet i dispositionstræet til venstre.
1. Vælg **Tilføj et billede** i egenskabsruden til højre. Vælg derefter et eksisterende billede, eller overfør et nyt billede.
1. Vælg **Overskrift**.
1. Tilføj overskriftsteksten i dialogboksen **Overskrift**, vælg overskriftsniveauet, og vælg derefter **OK**.
1. Tilføj tekst efter behov under **RTF-tekst**.
1. Vælg **Tilføj link**.
1. Tilføj linktekst, en URL-adresse og en ARIA-mærkat for linket i dialogboksen **Link**, og vælg derefter **OK**.
1. Vælg layoutet **Helt**.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.
1. Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den. 

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over modulbibliotek](starter-kit-overview.md)

[Kampagnebannermodul](add-alert.md)

[Karruselmodul](add-carousel.md)

[Tekstblokmodul](add-content-rich-block.md)

[Videoafspillermodul](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
