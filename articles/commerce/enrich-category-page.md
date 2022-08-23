---
title: Forbedre en kategorilandingsside
description: Denne artikel omhandler forbedring af kategorisider i Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: e3397ffee9b32f3d3efedea38255f88daee5233c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282155"
---
# <a name="enrich-a-category-landing-page"></a>Forbedre en kategorilandingsside

[!include [banner](includes/banner.md)]

Denne artikel omhandler forbedring af kategorisider i Dynamics 365 Commerce.

Commerce angiver en landingsside for den standardkategori, der bruges, når der vises kategoridata. En standardkategoriside indeholder de påkrævede elementer, f.eks. afgrænsere, kategoriseret produktplacering, sorteringsindstillinger, en oversigt over valgmuligheder og kontrolelementer til sideinddeling. 

Men i stedet for at bruge standardkategorisiden kan du bruge en "forbedret" kategorilandingsside, der har mere indhold og mere specifikke elementer. En typisk forbedring kan omfatte tilføjelse af kategorispecifikt marketingindhold på kategorisiden. Dette indhold kan omfatte produktplacering på tværs af kategorier med henblik på tillægssalg, redaktionelle lister, billeder, videoer og anden tekst. Du kan enten redigere standardkategorisiden eller definere en anden kategoriside for en bestemt kategori.

![Forbedre en kategorilandingsside.](./media/CategoryLandingPages.png)

I Commerce-webstedsgeneratoren indeholder siden **Produkter** en liste over kategorier fra den kanal, der er tildelt webstedet. Hvis status **Forbedret** er valgt for en kategoriside, er den pågældende kategoriside blevet forbedret. Ellers bruges standardkategorisiden og standardindholdet til kategorien. Du kan gennemse både de forbedrede og de ikke-forbedrede kategorisider for en kategori ved at vælge kategorinavnet.

Benyt følgende fremgangsmåde for at forbedre en kategoriside.

1. Vælg navnet på den kategori, du vil forbedre kategorisiden for, på siden **Produkter**. Standardkategorisiden for den valgte kategori åbnes i sideeditoren.
2. Vælg **Forbedring af kategoriside**.
3. Vælg en skabelon til den forbedrede kategoriside. Hvis du kun foretager mindre ændringer, kan du vælge standardkategorisiden. Du kan også vælge en bestemt skabelon for kategorisiden. Når du vælger skabelonen, åbnes sideeditoren, og den valgte skabelon bruges til at oprette en ny kategoriside for den valgte kategori. Siden er checket ud til dig, og du kan nu foretage dine ændringer.

> [!NOTE]
> Moduler, der bruger kategorispecifikationsdata, bruger dataene fra den valgte kategori. Indstillingerne for den skabelon, du vælger, bestemmer, hvilke ændringer du kan foretage.

## <a name="additional-resources"></a>Yderligere ressourcer

[Redigere en eksisterende webstedsside](modify-existing-page.md)

[Tilføje en ny webstedsside](add-new-page.md)

[Vælge sidelayout](select-page-layouts.md)

[Administrere SEO-metadata](manage-seo-metadata.md)

[Gemme, få vist og udgive en side](save-preview-publish-page.md)

[Forbedre en produktside](enrich-product-page.md)

[Bekræfte tilgængelighed af sideindhold](verify-accessibility.md)

[Oprette dynamiske e-handelssider baseret på URL-parametre](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
