---
title: Administrere SEO-metadata
description: Denne artikel beskriver, hvordan du administrerer SEO-metadata (søgemaskineoptimering) i Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/21/2022
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
ms.openlocfilehash: 99c28c2bff7b683f3e92dea4ba24d8bead556443
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027303"
---
# <a name="manage-seo-metadata"></a>Administrere SEO-metadata

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du administrerer SEO-metadata (søgemaskineoptimering) i Microsoft Dynamics 365 Commerce.

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
1. Vælg **Rediger** på kommandolinjen.
1. I sideeditoren øverst på sidedispositionskontrollen til venstre skal du vælge indstillingen **Vis tilstand** (gearkassesymbol) og derefter vælge **Avanceret dispositionsvisning**.
1. I dispositionsvisningen kan du udvide trækontrolelementerne for at få vist indholdet af **HTML-hoved**-plads.
1. I **HTML-hoved** plads skal du vælge det ønskede SEO-modul (f.eks. **Sideoversigt**, **Produktsideoversigt**, **Oversigt over kategoriside** eller **Metatags**).
1. I egenskabsruden til højre kan du redigere de ønskede SEO-data for det valgte SEO-modul(f.eks. **Titel**, **Beskrivelse** eller **Delebillede**).
1. Vælg **Gem**, og vælg derefter **Afslut redigering**.
1. Angiv **Opdaterede SEO-data** i feltet **Kommentarer**, og vælg derefter **OK**.
1. Vælg **Eksempel** for at få vist din side. Når du er færdig, skal du lukke eksempelfanen for at vende tilbage til oprettelsesværktøjet.
1. Vælg **Publicer**.

> [!TIP]
> Forfattere kan bruge indstillingen **Dispositionstilstand** (gearkassesymbol) øverst i venstre dispositionsstyring i sideeditoren til at skifte mellem **Grundlæggende visning af disposition** og **Avanceret dispositionsvisning**. **Grundlæggende dispositionsvisning** er standardindstillingen og filtrerer dispositionen, så den kun viser moduler i pladsen **Tekst**-HTML til en side. **Den avancerede visning** viser hele sidemodulet, herunder **HTML-hoved**, **Tekststart** og **Tekstslut**. Denne visning er nyttig, når forfattere skal redigere bestemte SEO- eller scriptmodulindstillinger for en side.

## <a name="additional-resources"></a>Yderligere ressourcer

[Redigere en eksisterende webstedsside](modify-existing-page.md)

[Tilføje en ny webstedsside](add-new-page.md)

[Vælge sidelayout](select-page-layouts.md)

[Gemme, få vist og udgive en side](save-preview-publish-page.md)

[Forbedre en produktside](enrich-product-page.md)

[Forbedre en kategorilandingsside](enrich-category-page.md)

[Bekræfte tilgængelighed af sideindhold](verify-accessibility.md)

[Oprette dynamiske e-handelssider baseret på URL-parametre](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
