---
title: Aktivere ADLS i et Dynamics 365 Commerce-miljø
description: Dette emne forklarer, hvordan du aktiverer og tester Azure Data Lake Storage (ADLS) for et Dynamics 365 Commerce-miljø, som er en forudsætning for, at du kan aktivere produktanbefalinger.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ba428765babb9ca7566da7a457368959b1c29083
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259742"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a>Aktivere ADLS i et Dynamics 365 Commerce-miljø

[!include [banner](includes/banner.md)]

Dette emne forklarer, hvordan du aktiverer og tester Azure Data Lake Storage (ADLS) for et Dynamics 365 Commerce-miljø, som er en forudsætning for, at du kan aktivere produktanbefalinger.

## <a name="overview"></a>Oversigt

I Dynamics 365 Commerce-løsningen spores alle produkt- og transaktionsoplysninger i miljøets enhedslager. For at gøre disse data tilgængelige for andre Dynamics 365-tjenester, f.eks. dataanalyse, business intelligence og personlige anbefalinger, er det nødvendigt at knytte miljøet til en kundeejet Azure Data Lake Storage Gen 2-løsning (ADLS).

Da ADLS er konfigureret i et miljø, spejles alle nødvendige data fra enhedslageret, mens de stadig er beskyttet og under kundens kontrol.

Hvis produktanbefalinger eller personlige anbefalinger også er aktiveret i miljøet, vil stakken med produktanbefalinger blive tildelt adgang til den dedikerede mappe i ADLS for at hente kundens data og beregne anbefalinger baseret på den.

## <a name="prerequisites"></a>Forudsætninger

Kunderne skal have ADLS konfigureret i et Azure-abonnement, som de ejer. Dette emne dækker ikke købet af et Azure-abonnement eller opsætningen af en ADLS-aktiveret lagerkonto.

Du kan finde flere oplysninger om ADLS i [ADLS officiel dokumentation](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Konfigurationstrin

I dette afsnit beskrives de konfigurationstrin, der er nødvendige for at aktivere ADLS i et miljø, da det angår produktanbefalinger.
Du kan få en mere detaljeret oversigt over de trin, der er nødvendige for at aktivere ADLS, i [Gøre enhedslager tilgængelig som en Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-adls-in-the-environment"></a>Aktivere ADLS i miljøet

1. Log på miljøets administrationsportal.
1. Søg efter **Systemparametre**, og gå til fanen **Dataforbindelser**. 
1. Angiv **Aktivér Data Lake-integration** til **Ja**.
1. Angiv **Foretag sivende opdatering af Data Lake** til **Ja**.
1. Angiv derefter følgende nødvendige oplysninger:
    1. **Program-id** // **Programhemmelighed** // **DNS-navn** – skal bruges til at oprette forbindelse til KeyVault, hvor ADLS-hemmeligheden opbevares.
    1. **Hemmeligt navn** – det hemmelige navn, der er gemt i KeyVault og bruges til at godkende med ADLS.
1. Gem ændringerne i øverste venstre hjørne af siden.

Følgende billede viser et eksempel på en ADLS-konfiguration.

![Eksempel på ADLS-konfiguration](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a>Test ADLS-forbindelsen

1. Test forbindelsen til KeyVault ved hjælp af linket **Test Azure Key Vault**.
1. Test forbindelsen til ADLS ved hjælp af linket **Test Azure Storage**.

> [!NOTE]
> Hvis testene ikke lykkes, skal du dobbelttjekke, at alle KeyVault-oplysningerne, der er tilføjet ovenfor, er korrekte, og derefter prøve igen.

Når test af forbindelsen er gennemført korrekt, skal du aktivere automatisk opdatering af enhedslageret.

Følg disse trin for at aktivere automatisk opdatering af enhedslager.

1. Søg efter **Enhedslager**.
1. Gå til posten **RetailSales** på listen til venstre, og vælg **Rediger**.
1. Sørg for, at **Automatisk opdatering er aktiveret** er angivet til **Ja**, vælg **Opdater**, og vælg derefter **Gem**.

Følgende billede viser et eksempel på enhedslager med automatisk opdatering aktiveret.

![Eksempel på enhedslager med automatisk opdatering aktiveret](./media/exampleADLSConfig2.png)

ADLS er nu konfigureret for miljøet. 

Hvis det ikke allerede er fuldført, skal du følge trinnene for [aktivering af produktanbefalinger og tilpasning](enable-product-recommendations.md) for miljøet.

## <a name="additional-resources"></a>Yderligere ressourcer

[Gøre enhedslager tilgængelig som en data lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[Oversigt over produktanbefalinger](product-recommendations.md)

[Aktivér produktanbefalinger](enable-product-recommendations.md)

[Aktivere tilpassede anbefalinger](personalized-recommendations.md)

[Fravælge tilpassede anbefalinger](personalization-gdpr.md)

[Tilføje produktanbefalinger på POS](product.md)

[Føje anbefalinger til transaktionsskærmen](add-recommendations-control-pos-screen.md)

[Justere resultater for AI-ML-anbefalinger](modify-product-recommendation-results.md)

[Oprette overvågede anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Oprette anbefalinger med demonstrationsdata](product-recommendations-demo-data.md)

[Ofte stillede spørgsmål om produktanbefalinger](faq-recommendations.md)
