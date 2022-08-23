---
title: Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø
description: Denne artikel indeholder oplysninger om, hvordan der oprettes Azure Data Lake Storage-forbindelse mellem en Gen 2-løsning og et Dynamics 365 Commerce-miljøs enhedslager. Dette er et påkrævet trin, før du aktiverer produktanbefalinger.
author: bebeale
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: d7995e826a838796f714ced2f30220201a157f93
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284739"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø

[!include [banner](includes/banner.md)]

Denne artikel indeholder oplysninger om, hvordan der oprettes Azure Data Lake Storage-forbindelse mellem en Gen 2-løsning og et Dynamics 365 Commerce-miljøs enhedslager. Dette er et påkrævet trin, før du aktiverer produktanbefalinger.

I Dynamics 365 Commerce-løsningen aggregeres de data, der er nødvendige for at beregne anbefalinger, produkter og transaktioner i miljøets enhedslager. For at gøre disse data tilgængelige for andre Dynamics 365-tjenester, f.eks. dataanalyse, business intelligence og personlige anbefalinger, er det nødvendigt at knytte miljøet til en kundeejet Azure Data Lake Storage Gen2-løsning.

Når trinnene ovenfor er udført, afspejles alle kundedata i miljøets Enhedslager automatisk i kundens Azure Data Lake Storage Gen2-løsning. Når anbefalingerfunktioner er aktiveret via arbejdsområdet til funktionsstyring i Commerce headquarters, får anbefalingerne adgang til samme Azure Data Lake Storage Gen2-løsning.

Under hele processen forbliver kundernes data beskyttede og under deres kontrol.

## <a name="prerequisites"></a>Forudsætninger

Et Dynamics 365 Commerce-miljøs enhedslager skal være tilknyttet en Azure Data Lake Gen Storage Gen2-konto og tilhørende tjenester.

Du kan finde flere oplysninger om Azure Data Lake Storage Gen2 og opsætning af samme i [den officielle dokumentation for Azure Data Lake Storage Gen2](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Konfigurationstrin

I dette afsnit beskrives de konfigurationstrin, der er nødvendige for at aktivere Azure Data Lake Storage Gen2 i et miljø, da det angår produktanbefalinger.
Du kan få en mere detaljeret oversigt over de trin, der er nødvendige for at aktivere Azure Data Lake Storage Gen2 i [Gøre enhedslager tilgængelig som en Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Aktivér Azure Data Lake Storage i miljøet

1. Log på miljøets administrationsportal.
1. Søg efter **Systemparametre**, og gå til fanen **Dataforbindelser**. 
1. Angiv **Aktivér Data Lake-integration** til **Ja**.
1. Angiv derefter følgende nødvendige oplysninger:
    1. **Program-id** // **Programhemmelighed** // **DNS-navn** – Er nødvendig for oprette forbindelse til KeyVault, hvor Azure Data Lake Storage-hemmeligheden er gemt.
    1. **Hemmeligt navn** – Det hemmelige navn, der er gemt i KeyVault, og som bruges til at godkende med Azure Data Lake Storage.
1. Gem ændringerne i øverste venstre hjørne af siden.

Følgende billede viser et eksempel på en Azure Data Lake Storage-konfiguration.

![Eksempel på Azure Data Lake Storage-konfiguration.](./media/exampleADLSConfig1.png)

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

![Eksempel på enhedslager med automatisk opdatering aktiveret.](./media/exampleADLSConfig2.png)

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
