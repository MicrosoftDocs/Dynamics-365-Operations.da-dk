---
title: Aktivér produktanbefalinger
description: I dette emne beskrives, hvordan du kan lave produktanbefalinger, der er baseret på kunstig intelligens-maskinel læring (AI-ML), som er tilgængelig for Microsoft Dynamics 365 Commerce-kunder.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 694e5a451b8e25f3729364dfaed0adc7d242f2fe
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404203"
---
# <a name="enable-product-recommendations"></a>Aktivér produktanbefalinger

[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du kan lave produktanbefalinger, der er baseret på kunstig intelligens-maskinel læring (AI-ML), som er tilgængelig for Microsoft Dynamics 365 Commerce-kunder. Yderligere oplysninger om lister over produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Forhåndscheck af anbefalinger

Før du aktiverer, skal du vide, at produktanbefalingerne kun understøttes for Commerce-kunder, som har overført deres lager for at bruge Azure Data Lake Storage. 

Følgende konfigurationer skal aktiveres i administrationen, før du aktiverer anbefalinger:

1. Kontrollér, at Azure Data Lake Storage er købt og godkendt i miljøet. Du kan få flere oplysninger i [Kontrollér, at Azure Data Lake Storage er købt og godkendt i miljøet](enable-ADLS-environment.md).
2. Sørg for, at opdatering af enhedslageret er automatiseret. Du kan finde flere oplysninger i [Sørg for, at opdatering af enhedslageret er automatiseret](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
3. Bekræft, at Azure AD-identitetskonfiguration indeholder en indtastning til anbefalinger. Du kan få flere oplysninger om, hvordan denne handling udføres, nedenfor.

Derudover skal du kontrollere, at RetailSale-målinger er aktiveret. Du kan få mere at vide om denne opsætning i [Arbejde med målpunkter](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).

## <a name="azure-ad-identity-configuration"></a>Azure AD-identitetskonfiguration

Dette trin er obligatorisk for alle kunder, der kører en IaaS-konfiguration (Infra-Structure as a Service). For kunder, der kører på service fabric (SF), skal dette trin være automatisk, og det anbefales, at man kontrollerer, at indstillingen er konfigureret som forventet.

### <a name="setup"></a>Konfiguration

1. Fra administrationen skal du søge efter siden **Azure Active Directory-programmer**.
2. Kontrollér, om der findes en post for "RecommendationSystemApplication-1".

Hvis posten ikke findes, skal du tilføje en ny post med følgende oplysninger:

- **Klient-id** – d37b07e8-dd1c-4514-835d-8b918e6f9727
- **Navn** – RecommendationSystemApplication-1
- **Bruger-id** – RetailServiceAccount

Gem og luk siden. 

## <a name="turn-on-recommendations"></a>Aktivere anbefalinger

Benyt følgende fremgangsmåde for at aktivere produktanbefalinger.

1. Gå til **Retail og Commerce &gt; Produktanbefalinger &gt; Anbefalingsparametre**.
1. Vælg **Anbefalingslister** på listen over delte parametre.
1. Vælg **Ja** i indstillingen **Aktivér anbefalinger**.

![Slå anbefalinger til](./media/enablepersonalization.png)

> [!NOTE]
> Denne procedure starter processen til oprettelse af produktanbefalingslister. Der kan tage op til flere timer, før listerne er tilgængelige og bliver vist på POS eller i Dynamics 365 Commerce.

## <a name="configure-recommendation-list-parameters"></a>Konfigurere parametre for anbefalingslister

Den AI-ML-baserede produktanbefalingsliste angiver som standard foreslåede værdier. Du kan ændre de foreslåede standardværdier, så de passer til dit firmas flow. Hvis du vil vide mere om, hvordan du ændrer standardparametrene, skal du gå til [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Vise anbefalinger på POS-enheder

Når anbefalingerne er aktiveret i Commerce-administrationen, skal anbefalingspanelet føjes til kontrolelementets POS-skærm ved hjælp af layoutværktøjet. Du kan få mere at vide om denne proces i [Føje et kontrolelement med anbefalinger til posteringsskærmen på POS-enheder](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Aktivere tilpassede anbefalinger

I Dynamics 365 Commerce kan detailhandlere gøre personligt tilpassede produktanbefalinger tilgængelige. På denne måde kan personlige anbefalinger indarbejdes i den online kundeoplevelse og på salgsstedet (POS). Når tilpasningsfunktionen er slået til, kan systemet tilknytte en brugers købs- og produktoplysninger for at generere individuelle produktanbefalinger.

Du kan få flere oplysninger om tilpassede anbefalinger i [Aktivere personlige anbefalinger](personalized-recommendations.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktanbefalinger](product-recommendations.md)

[Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktivere tilpassede anbefalinger](personalized-recommendations.md)

[Fravælge tilpassede anbefalinger](personalization-gdpr.md)

[Tilføje produktanbefalinger på POS](product.md)

[Føje anbefalinger til transaktionsskærmen](add-recommendations-control-pos-screen.md)

[Justere resultater for AI-ML-anbefalinger](modify-product-recommendation-results.md)

[Oprette overvågede anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Oprette anbefalinger med demonstrationsdata](product-recommendations-demo-data.md)

[Ofte stillede spørgsmål om produktanbefalinger](faq-recommendations.md)

