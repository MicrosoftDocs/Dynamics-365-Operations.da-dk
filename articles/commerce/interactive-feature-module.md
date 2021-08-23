---
title: Interaktivt funktionsmodul
description: Dette emne omhandler interaktive funktionsmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
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
ms.openlocfilehash: 5b18a29ce43e69ec0578602535f21e52388fe3d04ac14673bbdefed9ec8ea161
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749844"
---
# <a name="interactive-feature-module"></a>Interaktivt funktionsmodul

[!include [banner](includes/banner.md)]

Dette emne omhandler interaktive funktionsmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Interaktive funktionsmoduler er modul af mosaiklignende moduler, som kan bruges til at markedsføre flere produktkategorier eller produktmærker ved hjælp af en kombination af billeder og tekst. En detailbutik kan for eksempel føje et interaktive funktionsmodul til startsiden for et e-handelswebsted for at promovere mest solgte kategorier. Det interaktive funktionsmodul ligner modulet Feltliste, men det har et andet layout og forskellige interaktionsfunktioner.

Hvert af de interaktive funktionsmoduler er en samling af interaktive funktionselementmoduler. Alle funktionselementmoduler styres af data fra CMS (Content Management system). Det afhænger ikke af andre moduler eller data fra Commerce Headquarters. De interaktive funktionsmodul kan tilføjes på alle sider på websteder, hvor en forhandler ønsker at markedsføre eller vise noget (for eksempel produkter, kategorier eller mærker).

> [!IMPORTANT]
> - Det interaktive funktionsmodul er tilgængeligt fra og med Dynamics 365 Commerce version 10.0.20-udgaven.
> - Det interaktive funktionsmodul aktiveres med Adventure Works-temaet.

I følgende illustration vises et eksempel på et interaktivt funktionsmodul på Adventure Works-webstedssiden.

![Et eksempel på et interaktivt funktionsmodul på Adventure Works-webstedssiden](./media/Feature.PNG)

## <a name="interactive-feature-module-and-themes"></a>Interaktivt funktionsmodul og temaer

Det interaktive funktionsmodul kan understøtte forskellige layout og typografier, der er baseret på et tema. I Adventure Works-temaet har det interaktive funktionsmodul for eksempel et layout med to kolonner, der viser animationseffekter, når en webstedsbruger peger på de enkelte elementer. Det interaktive funktionsmodul er optimeret til et lige antal billeder, der er arrangeret i et layout med to kolonner.

## <a name="interactive-feature-module-properties"></a>Egenskaber for interaktivt funktionsmodul

| Egenskabsbetegnelse | Værdier | Betegnelse |
|---------------|--------|-------------|
| Overskrift       | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | En tekstoverskrift til det interaktive funktionsmodul. |

## <a name="interactive-feature-item-module-properties"></a>Egenskaber for interaktivt funktionselementmodul

| Egenskabsbetegnelse | Værdier | Betegnelse |
|---------------|--------|-------------|
| Billede         | Billedfil | Et billede, der repræsenterer et produkt eller en kategori. Billedet kan overføres til mediebiblioteket i Commerce Site Builder, eller der kan bruges et eksisterende billede. |
| Overskrift       | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Som standard bruges **H2** overskriften, men koden kan ændres efter behov for at opfylde tilgængelighedskravene. |
| Afsnit     | Afsnitstekst | Modulet understøtter afsnitstekst i RTF-format. Nogle grundlæggende RTF-funktioner understøttes, f. eks. hyperlinks og fed, understreget og kursiv tekst. Nogle af disse funktioner kan tilsidesættes af det sidetema, der anvendes på modulet. |
| Binding          | Linktekst, URL-adresse for link, ARIA-mærkat (Accessible Rich Internet Applications) og **Åbn link under ny fane** | Modulet understøtter et eller flere links til "handlingsplaner". Hvis der tilføjes et link, er linktekst, en URL-adresse og en ARIA-mærkat påkrævet. ARIA-mærkater skal være beskrivende for at imødekomme tilgængelighedskravene. Links kan konfigureres, så de åbnes under en ny fane. |

## <a name="add-an-interactive-feature-module-to-a-new-page"></a>Føje et interaktivt funktionsmodul til en ny side

Hvis du vil føje et interaktivt funktionsmodul til en ny side og angive de påkrævede egenskaber i Commerce-webstedsgeneratoren, skal du følge disse trin.

1. Gå til **Skabeloner**, og åbn marketingskabelonen for webstedets startside (eller opret en ny marketingskabelon).
1. På pladsen **Hoved** på standardsiden skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Interaktiv funktion** og derefter vælge **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.
1. Gå til **Sider**, og åbn webstedets startside (eller opret en ny startside ved hjælp af marketingskabelonen).
1. Vælg pladsen **Hoved** på standardsiden, vælg ellipseknappen (**...**), og vælg derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** under **Vælg moduler** skal du vælge modulet **Interaktiv funktion** og derefter vælge **OK**.
1. Tilføj en overskrift i egenskabsruden for det interaktive funktionsmodul.
1. Vælg ellipseknappen (**...**) i pladsen **Interaktiv funktion**, og vælg derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Interaktiv funktionselement** og derefter vælge **OK**.
1. Tilføj et billede, en overskriftstekst, en afsnitstekst og en URL-adresse i egenskabsruden for det interaktive funktionselementmodul.
1. Tilføj og konfigurer yderligere interaktive funktionselementmoduler efter behov.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.
1. Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Adventure Works-tema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
