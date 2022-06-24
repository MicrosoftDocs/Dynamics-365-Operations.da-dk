---
title: Forbedre en produktside
description: Denne artikel indeholder en beskrivelse af, hvordan du kan forbedre en produktside i Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ad58f0324c91c7488e5eb823fa3d0e1758ec63fb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847620"
---
# <a name="enrich-a-product-page"></a>Forbedre en produktside

[!include [banner](includes/banner.md)]

Denne artikel indeholder en beskrivelse af, hvordan du kan forbedre en produktside i Microsoft Dynamics 365 Commerce.

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

[Bekræfte tilgængelighed af sideindhold](verify-accessibility.md)

[Oprette dynamiske e-handelssider baseret på URL-parametre](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
