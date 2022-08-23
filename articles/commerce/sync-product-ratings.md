---
title: Synkroniser produktvurderinger i Dynamics 365 Commerce
description: Denne artikel beskriver, hvordan du synkroniserer produktvurderinger i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 7946bcaa9c6f318115640c6b20b00554a117dd38
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282017"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a>Synkroniser produktvurderinger i Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du synkroniserer produktvurderinger i Microsoft Dynamics 365 Commerce.

Hvis du vil bruge produktvurderinger i omni-kanaler som f.eks. på POS og i callcentre, skal produktvurderinger fra vurderings- og anmeldelsestjenesten importeres til Commerce-kanalens database. Når produktvurderinger stilles til rådighed i omni-kanaler, kan de hjælpe kunder indirekte under deres interaktioner med salgsmedarbejdere.

Denne artikel beskriver følgende opgaver:

1. Konfigurer **Synkroniseringsjob for produktvurderinger** som et batchjob for at synkronisere produktvurderinger fra **Tjenesten Vurderinger og anmeldelser**.
1. Kontrollere, at batchjobbet til synkronisering af produktvurderinger er fuldført.
1. Gøre produktvurderinger tilgængelige ved POS.

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a>Konfigurere et batchjob for at synkronisere produktvurderinger

> [!IMPORTANT]
> Før du går i gang, skal du kontrollere, at version 10.0.6 eller nyere af Dynamics 365 Commerce er installeret.

### <a name="initialize-the-commerce-scheduler"></a>Initialisere Commerce-planlægger

Hvis du vil initialisere Commerce-planlæggeren, skal du følge disse trin.

1. Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-planlægger \> Initialiser Commerce-planlægger**. Du kan også søge efter "Initialiser Commerce-planlægger".
1. I dialogboksen **Initialiser Commerce-planlægger** skal du kontrollere, at indstillingen **Slet eksisterende konfiguration** er angivet til **Nej**, og vælg derefter **OK**.

### <a name="verify-the-retailproductrating-subjob"></a>Kontrollere RetailProductRating-underjobbet

Udfør følgende trin for at kontrollere, om **RetailProductRating**-underjobbet findes:

1. Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-planlægger \> Planlæggerunderjob**. Du kan også søge efter "Planlæggerunderjob".
1. Find eller søg efter **RetailProductRating**-underjobbet på listen over underjob.

I følgende illustration vises et eksempel på siden detaljer om underjob i Commerce.

![Detaljer om RetailProductRating-underjobbet.](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> Hvis du ikke kan finde **RetailProductRating**-underjobbet, har du måske allerede kørt jobbet **Synkroniser produktvurderinger** og **1040 CDX**-jobbet, før du initialiserede Commerce-planlæggeren. I dette tilfælde skal du følge disse trin for at køre jobbet **Fuld datasynkronisering**.

> 1. Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-planlægger \> Kanaldatabase**. Du kan også søge efter "Kanaldatabase".
> 1. Vælg den kanaldatabase, der skal synkroniseres.
> 1. Vælg **Fuld datasynkronisering** i handlingsruden.
> 1. Vælg **1040 - produkter** i dialogboksen **Vælg en distributionsplan**, og vælg derefter **OK**.
> 1. Gentag trinnene i den forrige procedure for at kontrollere, at **RetailProductRating**-underjobbet er oprettet.

### <a name="import-product-ratings"></a>Importere produktvurderinger

Udfør følgende trin for at importere produktvurderinger til Commerce fra vurderings- og anmeldelsestjenesten.

1. Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-planlægger \> Synkroniser produktvurderingsjob**. Du kan også søge efter "Synkroniser produktvurderingsjob".
1. Vælg **Gentages** i oversigtspanelet **Kør i baggrunden** i dialogboksen **Hent produktvurderinger**.
1. Angiv et gentagelsesmønster i dialogboksen **Definer gentagelse**. (Den foreslåede værdi er to timer). Planlæg ikke en gentagelse, der er mindre end én time.
1. Vælg **OK**.
1. Angiv indstillingen **Batchbehandling** til **Ja**. Denne indstilling er med til at sikre, at du kan overvåge logfilerne og kontrollere status for batchjob, der kører.
1. Vælg **OK** for at planlægge batchjobbet.

I følgende illustration vises et eksempel på konfiguration af batchjob i Commerce.

![Konfiguration af batchjobbet Synkroniser produktvurderinger.](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a>Kontrollere, at batchjobbet til synkronisering af produktvurderinger er fuldført

Benyt følgende fremgangsmåde for at kontrollere, at batchjobbet **Synkroniser produktvurderinger** lykkedes.

1. Gå til **Retail og Commerce \> Systemadministrator \> Forespørgsler \> Batchjob** eller, hvis du bruger en ren Commerce-lagerbeholdning (SKU), **Retail og Commerce \> Forespørgsler og-rapporter \> Batchjob** i stedet. Du kan også søge efter "Batchjob".
1. Hvis du vil have vist detaljerne om batchjobbet, skal du søge efter en beskrivelse, der indeholder "Hent produktvurderinger" i kolonnen **Jobbeskrivelse**, på batchjob-listen.
1. Vælg et job-id for at få vist oplysninger om batchjobbet, f.eks. planlagt startdato/tidspunkt og gentagelsesteksten.

I følgende illustration vises et eksempel på oplysningerne om batchjobbet i Commerce, når batchjobbet er planlagt til at køre med to timers intervaller.

![Detaljer om batchjobbet Synkroniser produktvurdering.](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a>Gøre produktvurderinger tilgængelige ved POS

Vurderings- og anmeldelsesløsningen i Dynamics 365 Commerce er en omni-kanalløsning. Produktvurderinger vises dog ikke som standard ved POS. Hvis du vil hjælpe kunder i butikkerne med at se vurderinger og anmeldelser, når de bliver hjulpet af salgsassistenter, skal du aktivere produktvurderinger ved POS.

Hvis du vil aktivere produktvurderinger ved POS, skal du følge disse trin.

1. Gå til **Retail og Commerce \> Konfiguration af Commerce \> Parametre \> Commerce-parametre**. Du kan også søge efter "Commerce-parametre".
1. Vælg **Ny** under fanen **Konfigurationsparametre**.
1. Angiv et navn som f.eks **RatingsAndReviews.EnableProductRatingsForRetailStores**, og angiv værdien til **sand**.
1. Vælg **Gem**.
1. Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**. Du kan også søge efter "Distributionsplan".
1. På joblisten skal du vælge **1110** (**Global konfiguration**) og derefter vælge **Kør nu**.
1. Når jobbet er kørt korrekt, skal du kontrollere, at produktvurderinger nu vises ved POS.

I følgende illustration vises et eksempel på konfigurationen af Commerce-parametrene for at aktivere produktvurderinger ved POS.

![Konfiguration af Commerce-parametre for produktvurderinger ved POS.](media/rnr-hq-enable-ratings-in-pos.png)

I følgende illustration vises et eksempel på produktvurderinger ved POS.

![Produktvurderinger ved POS.](media/rnr-pos-catalog-ratings.png)

I følgende illustration vises et eksempel på produktvurderinger i callcenter-kanaler.

![Produktvurderinger i en callcenter-kanal.](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over vurderinger og anmeldelser](ratings-reviews-overview.md)

[Tilvælge brug af vurderinger og anmeldelser](opt-in-ratings-reviews.md)

[Administrere vurderinger og anmeldelser](manage-reviews.md)

[Konfigurere vurderinger og anmeldelser](configure-ratings-reviews.md)

[Synkronisere produktvurderinger](sync-product-ratings.md)

[Aktiver manuel udgivelse af vurderinger og gennemsyn af en redaktør](manual-publish-rating-reviews.md)

[Importere og eksportere bedømmelser og anmeldelser](import-export-reviews.md)

[Konfigurere service-til-service-godkendelse](service-to-service-auth.md)

[Ofte stillede spørgsmål til Vurderinger og anmeldelser](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
