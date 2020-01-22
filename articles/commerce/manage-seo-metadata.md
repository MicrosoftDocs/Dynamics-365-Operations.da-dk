---
title: Administrere SEO-metadata
description: I dette emne beskrives, hvordan du administrerer SEO-metadata (søgemaskineoptimering) i Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 3ea06713af69659c205686a971393892fa584072
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945714"
---
# <a name="manage-seo-metadata"></a>Administrere SEO-metadata

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du administrerer SEO-metadata (søgemaskineoptimering) i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

SEO-metadata for et websted kan administreres ved hjælp af webstedsoversigter og sidemetadata.
    
## <a name="site-maps"></a>Webstedsoversigter

En webstedsoversigt er en maskinlæsbar liste i XML-format over siderne på dit websted. Det er meningen, at den skal forbruges af søgemaskiner, så de kan give bedre søgeresultater fra dit websted. Webstedsoversigter kan bruges manuelt af søgemaskiner eller publiceres i en robots.txt-fil.

Dynamics 365 Commerce understøtter automatisk generering af webstedsoversigter. Webstedoversigter opdateres automatisk, når sider publiceres og annulleres.

### <a name="turn-on-site-map-generation"></a>Aktivere generering af webstedsoversigt

1. Log på værktøjet til oprettelse af websider.
1. Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.
1. Vælg **Administration af websted** i navigationsruden til venstre.
1. Kontroller, at indstillingen **Oversigter over websted er aktiveret** er slået til.

## <a name="page-metadata"></a>Sidemetadata

Med Dynamics 365 Commerce kan du administrere SEO-metadata for individuelle sider. Du kan få vist og redigere disse oplysninger i sektionen **SEO-egenskaber** i en sidecontainer. Følgende egenskaber for SEO-metadata understøttes:

- Stilling
- Beskrivelse
- SEO-nøgleord
- Aria-labels
- noindex
- nofollow
- noarchive
- nocache
- noOpenDirectoryProject
- nosnippet
- noImageIndex
- unavailableAfter

### <a name="modify-page-metadata"></a>Rediger sidemetadata

Hvis du vil redigere sidemetadata, skal du følge disse trin.

1. Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.
1. Vælg **Sider** i navigationsruden til venstre.
1. Vælg startsiden for at åbne den i sideeditoren.
1. Vælg **Check ud** i handlingsruden.
1. Udvid **Standardmetatags** i egenskabsruden til højre.
1. Hvis du vil tilføje en ny metatag, skal du vælge **Tilføj** og derefter angive den pågældende tag i feltet.

    Hvis du vil fjerne en eksisterende metatag, skal du vælge skraldespandsymbolet til højre for den.

1. Vælg **Gem**, og vælg derefter **Tjek ind**.
1. Angiv **Opdaterede metatags** i feltet **Kommentarer**, og vælg derefter **OK**.
1. Vælg **Eksempel** for at få vist din side. Når du er færdig, skal du lukke eksempelfanen for at vende tilbage til oprettelsesværktøjet.
1. Vælg **Publicer**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Redigere en eksisterende webstedsside](modify-existing-page.md)

[Tilføje en ny webstedsside](add-new-page.md)

[Vælge sidelayout](select-page-layouts.md)

[Gemme, få vist og udgive en side](save-preview-publish-page.md)

[Forbedre en produktside](enrich-product-page.md)

[Forbedre en kategorilandingsside](enrich-category-page.md)

[Bekræft tilgængelighed af sideindhold](verify-accessibility.md)