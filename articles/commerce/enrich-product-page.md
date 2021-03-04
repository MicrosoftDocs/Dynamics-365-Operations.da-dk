---
title: Forbedre en produktside
description: Dette emne indeholder en beskrivelse af, hvordan du kan forbedre en produktside i Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12508a80c440894ec6e2073b5e550846480e6c45
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411004"
---
# <a name="enrich-a-product-page"></a>Forbedre en produktside


[!include [banner](includes/banner.md)]

Dette emne indeholder en beskrivelse af, hvordan du kan forbedre en produktside i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Webstedet bruger som standard en generisk side til at vise produktdata. Denne side indeholder de grundlæggende oplysninger om produktet og de kontrolelementer, der skal bruges for at sælge det. Du kan dog supplere de oplysninger, der kommer fra Commerce Scale Unit, med yderligere billeder eller tekst til et bestemt produkt. Denne proces kaldes forbedring af produktsiden.

I mange tilfælde skal du bruge en bestemt form for yderligere indhold til dine produkter. Når du går til **Retail og Commerce** i oprettelsesværktøjet, får du vist en liste over produkter fra den kanal, der er tildelt til webstedet. På denne liste angiver kolonnen **Forbedret**, om produktsiden for et produkt er blevet forbedret. Hvis der vises en markering i kolonnen, findes der en produktside, der er blevet forbedret, for produktet. Hvis der ikke vises en markering, bruges standardproduktsiden og -indholdet til produktet. Du kan gennemse både forbedrede og ikke-forbedrede produktsider ved at vælge et produktnavn på listen.

## <a name="enrich-a-product-page"></a>Forbedre en produktside

Følg disse trin for at forbedre en produktside.

1. Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.
1. Vælg **Produkter** i navigationsruden til venstre.
1. Vælg et produkt, der ikke har en forbedret produktside.
1. Vælg **Forbedre en produktside** i handlingsruden.
1. Vælg **PDP-skabelon**, og vælg derefter **OK**.
1. Udvid **Hoved**-pladsen i dispositionstræet for siden til venstre.
1. Vælg ellipseknappen (**...**) til **Hoved**-pladsen, og vælg derefter **Tilføj modul**.
1. Vælg **Container 2**, og vælg derefter **OK**.
1. Vælg ellipseknappen til **Container 2**, og vælg derefter **Tilføj modul**.
1. Vælg **Funktion**, og vælg derefter **OK**.
1. Angiv den opdaterede beskrivelse af produktet i feltet **RTF** i egenskabsruden til højre.
1. Angiv overskriftstekst i feltet **Overskrift**, og vælg derefter **OK**.
1. Vælg **Gem**, og vælg derefter **Afslut redigering**.
1. Angiv **Forbedrede et produkt** i feltet **Kommentarer**, og vælg derefter **OK**.
1. Hvis du vil se en forhåndsvisning af den forbedrede produktside, skal du vælge **Forhåndsvisning**. Når du er færdig, skal du lukke eksempelfanen for at vende tilbage til oprettelsesværktøjet.
1. Vælg **Publicer**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Redigere en eksisterende webstedsside](modify-existing-page.md)

[Tilføje en ny webstedsside](add-new-page.md)

[Vælge sidelayout](select-page-layouts.md)

[Administrere SEO-metadata](manage-seo-metadata.md)

[Gemme, få vist og udgive en side](save-preview-publish-page.md)

[Forbedre en kategorilandingsside](enrich-category-page.md)

[Bekræft tilgængelighed af sideindhold](verify-accessibility.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]