---
title: Forbedre en kategorilandingsside
description: Dette emne omhandler forbedring af kategorisider i Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4ab152dff0925f9c816419083577b5272ac813be
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945771"
---
# <a name="enrich-a-category-landing-page"></a>Forbedre en kategorilandingsside

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne omhandler forbedring af kategorisider i Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Commerce angiver en landingsside for den standardkategori, der bruges, når der vises kategoridata. En standardkategoriside indeholder de påkrævede elementer, f.eks. afgrænsere, kategoriseret produktplacering, sorteringsindstillinger, en oversigt over valgmuligheder og kontrolelementer til sideinddeling. 

Men i stedet for at bruge standardkategorisiden kan du bruge en "forbedret" kategorilandingsside, der har mere indhold og mere specifikke elementer. En typisk forbedring kan omfatte tilføjelse af kategorispecifikt marketingindhold på kategorisiden. Dette indhold kan omfatte produktplacering på tværs af kategorier med henblik på tillægssalg, redaktionelle lister, billeder, videoer og anden tekst. Du kan enten redigere standardkategorisiden eller definere en anden kategoriside for en bestemt kategori.

![Forbedre en kategorilandingsside](./media/CategoryLandingPages.png)

I oprettelsesværktøjet indeholder siden **Produkt** en liste over kategorier fra den kanal, der er tildelt til webstedet. Hvis status **Forbedret** er valgt for en kategoriside, er den pågældende kategoriside blevet forbedret. Ellers bruges standardkategorisiden og standardindholdet til kategorien. Du kan gennemse både de forbedrede og de ikke-forbedrede kategorisider for en kategori ved at vælge kategorinavnet.

Benyt følgende fremgangsmåde for at forbedre en kategoriside.

1. Vælg navnet på den kategori, du vil forbedre kategorisiden for, på siden **Produkter**. Standardkategorisiden for den valgte kategori åbnes i sideeditoren.
2. Vælg **Forbedring af kategoriside**.
3. Vælg en skabelon til den forbedrede kategoriside. Hvis du kun foretager mindre ændringer, kan du vælge standardkategorisiden. Du kan også vælge en bestemt skabelon for kategorisiden. Når du vælger skabelonen, åbnes sideeditoren, og den valgte skabelon bruges til at oprette en ny kategoriside for den valgte kategori. Siden er checket ud til dig, og du kan nu foretage dine ændringer.

> [!NOTE]
> Moduler, der bruger kategorispecifikationsdata, bruger dataene fra den valgte kategori.
>
> Indstillingerne for den skabelon, du vælger, bestemmer, hvilke ændringer du kan foretage.

## <a name="additional-resources"></a>Yderligere ressourcer

[Redigere en eksisterende webstedsside](modify-existing-page.md)

[Tilføje en ny webstedsside](add-new-page.md)

[Vælge sidelayout](select-page-layouts.md)

[Administrere SEO-metadata](manage-seo-metadata.md)

[Gemme, få vist og udgive en side](save-preview-publish-page.md)

[Forbedre en produktside](enrich-product-page.md)

[Bekræft tilgængelighed af sideindhold](verify-accessibility.md)
