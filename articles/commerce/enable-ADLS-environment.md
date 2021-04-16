---
title: Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø
description: Dette emne forklarer, hvordan du aktiverer og tester Azure Data Lake Storage for et Dynamics 365 Commerce-miljø, som er en forudsætning for, at du kan aktivere produktanbefalinger.
author: bebeale
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 61f96dae0643e3383afd91864e4c145f3b5c04c8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792601"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø

[!include [banner](includes/banner.md)]

Dette emne forklarer, hvordan du aktiverer og tester Azure Data Lake Storage for et Dynamics 365 Commerce-miljø, som er en forudsætning for, at du kan aktivere produktanbefalinger.

I Dynamics 365 Commerce-løsningen spores alle produkt- og transaktionsoplysninger i miljøets enhedslager. For at gøre disse data tilgængelige for andre Dynamics 365-tjenester, f.eks. dataanalyse, business intelligence og personlige anbefalinger, er det nødvendigt at knytte miljøet til en kundeejet Azure Data Lake Storage Gen 2-løsning.

Da Azure Data Lake Storage er konfigureret i et miljø, spejles alle nødvendige data fra enhedslageret, mens de stadig er beskyttet og under kundens kontrol.

Hvis produktanbefalinger eller personlige anbefalinger også er aktiveret i miljøet, vil stakken med produktanbefalinger blive tildelt adgang til den dedikerede mappe i Azure Data Lake Storage for at hente kundens data og beregne anbefalinger baseret på den.

## <a name="prerequisites"></a>Forudsætninger

Kunderne skal have Azure Data Lake Storage konfigureret i et Azure-abonnement, som de ejer. Dette emne dækker ikke købet af et Azure-abonnement eller opsætningen af en Azure Data Lake Storage-aktiveret lagerkonto.

Du kan finde flere oplysninger om Azure Data Lake Storage i [den officielle dokumentation for Azure Data Lake Storage Gen2](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Konfigurationstrin

I dette afsnit beskrives de konfigurationstrin, der er nødvendige for at aktivere Azure Data Lake Storage i et miljø, da det angår produktanbefalinger.
Du kan få en mere detaljeret oversigt over de trin, der er nødvendige for at aktivere Azure Data Lake Storage i [Gøre enhedslager tilgængelig som en Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Aktivér Azure Data Lake Storage i miljøet

1. Log på miljøets administrationsportal.
1. Søg efter **Systemparametre**, og gå til fanen **Dataforbindelser**. 
1. Angiv **Aktivér Data Lake-integration** til **Ja**.
1. Angiv **Foretag sivende opdatering af Data Lake** til **Ja**.
1. Angiv derefter følgende nødvendige oplysninger:
    1. **Program-id** // **Programhemmelighed** // **DNS-navn** – Er nødvendig for oprette forbindelse til KeyVault, hvor Azure Data Lake Storage-hemmeligheden er gemt.
    1. **Hemmeligt navn** – Det hemmelige navn, der er gemt i KeyVault, og som bruges til at godkende med Azure Data Lake Storage.
1. Gem ændringerne i øverste venstre hjørne af siden.

Følgende billede viser et eksempel på en Azure Data Lake Storage-konfiguration.

![Eksempel på Azure Data Lake Storage-konfiguration](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>Test Azure Data Lake Storage-forbindelsen

1. Test forbindelsen til KeyVault ved hjælp af linket **Test Azure Key Vault**.
1. Test forbindelsen til Azure Data Lake Storage ved hjælp af linket **Test Azure Storage**.

> [!NOTE]
> Hvis testene ikke lykkes, skal du dobbelttjekke, at alle KeyVault-oplysningerne, der er tilføjet ovenfor, er korrekte, og derefter prøve igen.

Når test af forbindelsen er gennemført korrekt, skal du aktivere automatisk opdatering af enhedslageret.

Følg disse trin for at aktivere automatisk opdatering af enhedslager.

1. Søg efter **Enhedslager**.
1. Gå til posten **RetailSales** på listen til venstre, og vælg **Rediger**.
1. Sørg for, at **Automatisk opdatering er aktiveret** er angivet til **Ja**, vælg **Opdater**, og vælg derefter **Gem**.

Følgende billede viser et eksempel på enhedslager med automatisk opdatering aktiveret.

![Eksempel på enhedslager med automatisk opdatering aktiveret](./media/exampleADLSConfig2.png)

Azure Data Lake Storage er nu konfigureret for miljøet. 

Hvis det ikke allerede er fuldført, skal du følge trinnene for [aktivering af produktanbefalinger og tilpasning](enable-product-recommendations.md) for miljøet.

## <a name="additional-resources"></a>Yderligere ressourcer

[Gøre enhedslager tilgængelig som en data lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[Oversigt over produktanbefalinger](product-recommendations.md)

[Aktivér produktanbefalinger](enable-product-recommendations.md)

[Aktivere tilpassede anbefalinger](personalized-recommendations.md)

[Fravælge tilpassede anbefalinger](personalization-gdpr.md)

[Aktivere anbefalinger af "Køb tilsvarende"](shop-similar-looks.md)

[Tilføje produktanbefalinger på POS](product.md)

[Føje anbefalinger til transaktionsskærmen](add-recommendations-control-pos-screen.md)

[Justere resultater for AI-ML-anbefalinger](modify-product-recommendation-results.md)

[Oprette overvågede anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Oprette anbefalinger med demonstrationsdata](product-recommendations-demo-data.md)

[Ofte stillede spørgsmål om produktanbefalinger](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
