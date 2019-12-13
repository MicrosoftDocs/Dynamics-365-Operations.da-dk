---
title: Synkroniser produktvurderinger i Dynamics 365 Retail
description: Dette emne beskriver, hvordan du synkroniserer produktvurderinger i Microsoft Dynamics 365 Retail.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: db5a4e1f78797d20ded2274cc99bef422fd50acc
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698159"
---
# <a name="sync-product-ratings-in-dynamics-365-retail"></a>Synkroniser produktvurderinger i Dynamics 365 Retail

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du synkroniserer produktvurderinger i Microsoft Dynamics 365 Retail.

## <a name="overview"></a>Oversigt

Hvis du vil bruge produktvurderinger i omni-kanaler som f.eks. på POS og i opkaldscentre, skal produktvurderinger fra vurderings- og anmeldelsestjenesten importeres til detailkanalens database. Når produktvurderinger stilles til rådighed i omni-kanaler, kan de hjælpe kunder indirekte under deres interaktioner med salgsmedarbejdere.

Dette emne beskriver følgende opgaver:

1. Konfigurere et Retail-batchjob for at importere produktvurderinger.
1. Kontrollere, at batchjobbet til synkronisering af produktvurderinger er fuldført.
1. Gøre produktvurderinger tilgængelige ved POS.

## <a name="configure-a-retail-batch-job-to-import-product-ratings"></a>Konfigurere et Retail-batchjob for at importere produktvurderinger

> [!IMPORTANT]
> Før du går i gang, skal du kontrollere, at version 10.0.6 eller nyere af Retail er installeret.

### <a name="initialize-the-retail-scheduler"></a>Initialisere Retail planlægger

Hvis du vil initialisere Retail planlægger, skal du følge disse trin.

1. Gå til **Retail \> Konfiguration af hovedkontor \> Retail planlægger \> Initialiser Retail-planlægger**. Du kan også søge efter "Initialiser Retail-planlægger".
1. I dialogboksen **Initialiser Retail-planlægger** skal du kontrollere, at indstillingen **Slet eksisterende konfiguration** er angivet til **Nej**, og vælg derefter **OK**.

### <a name="verify-the-retailproductrating-subjob"></a>Kontrollere RetailProductRating-underjobbet

Udfør følgende trin for at kontrollere, om **RetailProductRating**-underjobbet findes:

1. Gå til **Retail \> Konfiguration af hovedkontor \> Retail planlægger \> Planlæggerunderjob**. Du kan også søge efter "Planlæggerunderjob".
1. Find eller søg efter **RetailProductRating**-underjobbet på listen over underjob.

I følgende illustration vises et eksempel på siden detaljer om underjob i Retail.

![Detaljer om RetailProductRating-underjobbet](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> Hvis du ikke kan finde **RetailProductRating**-underjobbet, har du måske allerede kørt jobbet **Synkroniser produktvurderinger** og **1040 CDX**-jobbet, før du initialiserede Retail planlægger. I dette tilfælde skal du følge disse trin for at køre jobbet **Fuld datasynkronisering**.
>
> 1. Gå til **Retail \> Konfiguration af hovedkontor \> Retail planlægger \> Kanaldatabase**. Du kan også søge efter "Kanaldatabase".
> 1. Vælg den kanaldatabase, der skal synkroniseres.
> 1. Vælg **Fuld datasynkronisering** i handlingsruden.
> 1. Vælg **1040 - produkter** i dialogboksen **Vælg en distributionsplan**, og vælg derefter **OK**.
> 1. Gentag trinnene i den forrige procedure for at kontrollere, at **RetailProductRating**-underjobbet er oprettet.

### <a name="import-product-ratings"></a>Importere produktvurderinger

Udfør følgende trin for at importere produktvurderinger til Retail fra vurderings- og anmeldelsestjenesten.

1. Gå til **Retail \> Konfiguration af hovedkontor \> Retail planlægger \> Synkroniser produktvurderingsjob**. Du kan også søge efter "Synkroniser produktvurderingsjob".
1. Vælg **Gentages** i oversigtspanelet **Kør i baggrunden** i dialogboksen **Hent produktvurderinger**.
1. Angiv et gentagelsesmønster i dialogboksen **Definer gentagelse**. (Den foreslåede værdi er to timer). Planlæg ikke en gentagelse, der er mindre end én time.
1. Vælg **OK**.
1. Angiv indstillingen **Batchbehandling** til **Ja**. Denne indstilling er med til at sikre, at du kan overvåge logfilerne og kontrollere status for batchjob, der kører.
1. Vælg **OK** for at planlægge batchjobbet.

I følgende illustration vises et eksempel på konfiguration af batchjob i Retail.

![Konfiguration af batchjobbet Synkroniser produktvurderinger](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a>Kontrollere, at batchjobbet til synkronisering af produktvurderinger er fuldført

Benyt følgende fremgangsmåde for at kontrollere, at batchjobbet **Synkroniser produktvurderinger** lykkedes.

1. Gå til **Retail \> Systemadministrator \> Forespørgsler \> Batchjob** eller, hvis du bruger en ren detaillagerbeholdning (SKU), **Retail \> Forespørgsler og-rapporter \> Batchjob** i stedet. Du kan også søge efter "Batchjob".
1. Hvis du vil have vist detaljerne om batchjobbet, skal du søge efter en beskrivelse, der indeholder "Hent produktvurderinger" i kolonnen **Jobbeskrivelse**, på batchjob-listen.
1. Vælg et job-id for at få vist oplysninger om batchjobbet, f.eks. planlagt startdato/tidspunkt og gentagelsesteksten.

I følgende illustration vises et eksempel på oplysningerne om batchjobbet i Retail, når batchjobbet er planlagt til at køre med to timers intervaller.

![Detaljer om batchjobbet Synkroniser produktvurdering](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a>Gøre produktvurderinger tilgængelige ved POS

Vurderings- og anmeldelsesløsningen i Dynamics 365 Commerce er en omni-kanalløsning. Produktvurderinger vises dog ikke som standard ved POS. Hvis du vil hjælpe kunder i butikkerne med at se vurderinger og anmeldelser, når de bliver hjulpet af salgsassistenter, skal du aktivere produktvurderinger ved POS.

Hvis du vil aktivere produktvurderinger ved POS, skal du følge disse trin.

1. Gå til **Retail \> Opsætning af Retail \> Parametre \> Detailparametre**. Du kan også søge efter "Detailparametre".
1. Vælg **Ny** under fanen **Konfigurationsparametre**.
1. Angiv et navn som f.eks **RatingsAndReviews.EnableProductRatingsForRetailStores**, og angiv værdien til **sand**.
1. Vælg **Gem**.
1. Gå til **Detail \> Detail-it \> Distributionsplan**. Du kan også søge efter "Distributionsplan".
1. På joblisten skal du vælge **1110** (**Global konfiguration**) og derefter vælge **Kør nu**.
1. Når jobbet er kørt korrekt, skal du kontrollere, at produktvurderinger nu vises ved POS.

I følgende illustration vises et eksempel på konfigurationen af detailparametrene for at aktivere produktvurderinger ved POS.

![Konfiguration af detailparametre for produktvurderinger ved POS](media/rnr-hq-enable-ratings-in-pos.png)

I følgende illustration vises et eksempel på produktvurderinger ved POS.

![Produktvurderinger ved POS](media/rnr-pos-catalog-ratings.png)

I følgende illustration vises et eksempel på produktvurderinger i callcenter-kanaler.

![Produktvurderinger i en callcenter-kanal](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over vurderinger og anmeldelser](ratings-reviews-overview.md)

[Tilvælge brug af vurderinger og anmeldelser](opt-in-ratings-reviews.md)

[Administrere vurderinger og anmeldelser](manage-reviews.md)

[Konfigurere vurderinger og anmeldelser](configure-ratings-reviews.md)
