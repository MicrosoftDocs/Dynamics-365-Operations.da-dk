---
title: Modulet Billedliste
description: Dette emne omhandler billedlistemoduler for social deling og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
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
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 485d0714927cef5a292fd1beee826a90e9233e35
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479429"
---
# <a name="image-list-module"></a>Modulet Billedliste

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emne omhandler billedlistemoduler for social deling og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Med billedlistemodulet er det nemt at føje en samling (matrix) af billeder til webstedssider. Hvert billede i matricen kan konfigureres med afsnitstekst og URL-adresser til links. Billedlistemodulet er bedst egnet til at vise varemærkelogoer eller lister, der indeholder logoer.

> [!IMPORTANT]
> - Billedlistemodulet er tilgængeligt i Commerce-modulbiblioteket fra og med Dynamics 365 Commerce version 10.0.20-udgaven.
> - Billedlistemodulet aktiveres med temaet Adventure Works.

I følgende illustration vises et eksempel, hvor et billedlistemodul viser en liste over tekst, der omfatter logoer på en B2C-webstedsside (Business-to-Consumer) for Adventure Works.

![Eksempel på et billedlistemodul, hvor der vises en liste over tekst, der indeholder logoer](./media/Image_list.PNG)

I følgende illustration vises et eksempel, hvor et billedlistemodul viser varemærkelogoer på en B2B-webstedsside (Business-to-Business) for Adventure Works.

![Eksempel på et billedlistemodul, der viser varemærkelogoer](./media/Image_list_B2B.PNG)

## <a name="image-list-module-properties"></a>Egenskaber for billedlistemodul

| Egenskabsbetegnelse | Værdier | Betegnelse |
|---------------|--------|-------------|
| Overskrift       | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | En tekstoverskrift til billedlistemodulet. |
| Billedliste    | Billeder, tekst og URL-adresser | De enkelte elementer i matricen er et billede, som ledsages af afsnitstekst og en URL-adresse. |

## <a name="add-an-image-list-module-to-a-new-page"></a>Føje et billedlistemodul til en ny side

Hvis du vil føje et billedlistemodul til en ny side og angive de påkrævede egenskaber i Commerce-webstedsgeneratoren, skal du følge disse trin.

1. Gå til **Skabeloner**, og åbn marketingskabelonen for webstedets startside (eller opret en ny marketingskabelon).
1. På pladsen **Hoved** på standardsiden skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Billedliste** og derefter vælge **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.
1. Gå til **Sider**, og åbn webstedets startside (eller opret en ny startside ved hjælp af marketingskabelonen).
1. Vælg pladsen **Hoved** på standardsiden, vælg ellipseknappen (**...**), og vælg derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge **Billedliste** og derefter vælge **OK**.
1. Tilføj en overskrift (for eksempel **Vores mærker**) i egenskabsruden for billedlistemodulet.
1. Tilføj et billedlisteelement, og angiv et billede, noget afsnitstekst og en URL-omdirigeringsadresse.
1. Tilføj og konfigurer yderligere billedlistemoduler efter behov.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.
1. Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Adventure Works-tema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
