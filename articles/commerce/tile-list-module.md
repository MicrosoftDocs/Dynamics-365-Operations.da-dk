---
title: Feltlistemodul
description: Dette emne omhandler feltlistemoduler for social deling og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 2da3c0415e996cadb5261d90c6353aa28bff3abb
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479428"
---
# <a name="tile-list-module"></a>Feltlistemodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emne omhandler feltlistemoduler for social deling og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Et feltlistemodul er en samling af felter i en karousel. Det bruges til markedsføring af produktkategorier eller produktmærker via billeder og tekst. En detailbutik kan for eksempel føje et feltlistemodul til startsiden for et e-handelswebsted for at promovere alle de mest solgte kategorier.

Feltlistemodulet styres af data fra CMS (Content Management system). Det afhænger ikke af andre moduler eller data fra Commerce Headquarters. Feltlistemodulet kan tilføjes på alle sider på websteder, hvor en forhandler ønsker at markedsføre eller vise noget (for eksempel produkter, kategorier eller mærker).

I følgende illustration vises et eksempel på et feltlistemodul og feltmoduler på Adventure Works-webstedssiden.

![Et eksempel på et feltlistemodul og feltmoduler på Adventure Works-webstedssiden](./media/Tile_list.PNG)

> [!IMPORTANT]
> Feltlistemodulet er tilgængeligt fra og med Dynamics 365 Commerce version 10.0.20-udgaven.
> Feltlistemodulet aktiveres med temaet Adventure Works.

## <a name="tile-list-modules-and-themes"></a>Feltlistemoduler og temaer

Feltlistemodulet kan understøtte forskellige layout og typografier, der er baseret på et tema. I Adventure Works-temaet viser felterne for eksempel animationseffekter, når en webstedsbruger peger på dem. Hvert tema kan indeholde flere egenskaber for feltliste- og feltmodulerne. Temaudviklere kan også oprette yderligere layout til feltliste- og feltmodulerne.

## <a name="tile-list-module-properties"></a>Egenskaber for feltlistemodul

| Egenskabsbetegnelse | Værdier | Betegnelse |
|---------------|--------|-------------|
| Overskrift       | Overskriftstekst og overskriftskode | En tekstoverskrift til feltlistemodulet. |

## <a name="tile-module-properties"></a>Egenskaber for feltmodul

| Egenskabsbetegnelse | Værdier | Betegnelse |
|---------------|--------|-------------|
| Billede         | Billedfil | Et billede kan bruges til at vise et produkt eller en kategori. Billedet kan overføres til mediebiblioteket i Commerce Site Builder, eller der kan bruges et eksisterende billede. |
| Overskrift       | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Som standard bruges **H2** overskriften, men koden kan ændres efter behov for at opfylde tilgængelighedskravene. |
| Afsnit     | Afsnitstekst | Modulet understøtter afsnitstekst i RTF-format. Nogle grundlæggende RTF-funktioner understøttes, f. eks. hyperlinks og fed, understreget og kursiv tekst. Nogle af disse funktioner kan tilsidesættes af det sidetema, der anvendes på modulet. |
| Binding          | Linktekst, URL-adresse for link, ARIA-mærkat (Accessible Rich Internet Applications) og **Åbn link under ny fane** | Moduler understøtter et eller flere links til "handlingsplaner". Hvis der tilføjes et link, er linktekst, en URL-adresse og en ARIA-mærkat påkrævet. ARIA-mærkater skal være beskrivende for at imødekomme tilgængelighedskravene. Links kan konfigureres, så de åbnes under en ny fane. |
| Link til felt     | Linktekst, URL-adresse for link, ARIA-mærkat og vælgeren **Åbn link under ny fane** | Denne egenskab bruges til at definere et link til en "handlingsplan". Hvis der tilføjes et link, er linktekst, en URL-adresse og en ARIA-mærkat påkrævet. ARIA-mærkater skal være beskrivende for at imødekomme tilgængelighedskravene. Links kan konfigureres, så de åbnes under en ny fane.|
| Ikon          | Billede | Ud over et produkt- eller kategoribillede kan der tilføjes et ikonsymbol. Billedet af ikonsymbolet vises oven over produkt- eller kategoribilledet. |

## <a name="add-a-tile-list-module-to-a-new-page"></a>Føje et feltlistemodul til en ny side

Hvis du vil føje et feltlistemodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Gå til **Skabeloner**, og åbn marketingskabelonen for webstedets startside (eller opret en ny marketingskabelon).
1. På pladsen **Hoved** på standardsiden skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Feltliste** og derefter vælge **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.
1. Gå til **Sider**, og åbn webstedets startside (eller opret en ny startside ved hjælp af marketingskabelonen).
1. Vælg pladsen **Hoved** på standardsiden, vælg ellipseknappen (**...**), og vælg derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Feltliste** og derefter vælge **OK**.
1. Tilføj en overskrift i egenskabsruden for feltlistemodulet.
1. Vælg ellipseknappen (**...**) i pladsen **Feltliste**, og vælg derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Feltmodul** og derefter vælge **OK**.
1. Tilføj et billede, en overskrift og et billede af et ikonsymbol i egenskabsruden for feltmodulet.
1. Tilføj og konfigurer yderligere feltmoduler efter behov.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.
1. Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Adventure Works-tema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
