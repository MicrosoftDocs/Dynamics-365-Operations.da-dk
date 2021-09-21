---
title: Aktivér produktanbefalinger
description: I dette emne beskrives, hvordan du kan lave produktanbefalinger, der er baseret på kunstig intelligens-maskinel læring (AI-ML), som er tilgængelig for Microsoft Dynamics 365 Commerce-kunder.
author: bebeale
ms.date: 08/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4a7be82b3a40aba621693f080ff41767fdaea474
ms.sourcegitcommit: 98061a5d096ff4b9078d1849e2ce6dd7116408d1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2021
ms.locfileid: "7466310"
---
# <a name="enable-product-recommendations"></a>Aktivér produktanbefalinger

[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du kan lave produktanbefalinger, der er baseret på kunstig intelligens-maskinel læring (AI-ML), som er tilgængelig for Microsoft Dynamics 365 Commerce-kunder. Yderligere oplysninger om lister over produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Forhåndscheck af anbefalinger

1. Kontroller, at du har en gyldig Dynamics 365 Commerce-anbefalingerslicens.
1. Sørg for, at der er oprettet forbindelse mellem en enhedslager og en debitorejet Azure Data Lake Storage Gen2-konto. Du kan få flere oplysninger i [Kontrollér, at Azure Data Lake Storage er købt og godkendt i miljøet](enable-ADLS-environment.md).
1. Bekræft, at Azure AD-identitetskonfiguration indeholder en indtastning til anbefalinger. Du kan få flere oplysninger om, hvordan denne handling udføres, nedenfor.
1. Sørg for, at den daglige opdatering af enhedslageret til Azure Data Lake Storage Gen2 er planlagt. Du kan finde flere oplysninger i [Sørg for, at opdatering af enhedslageret er automatiseret](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
1. Aktivér RetailSale-målinger for enhedsbutik. Du kan få mere at vide om denne opsætning i [Arbejde med målpunkter](/dynamics365/ai/customer-insights/pm-measures).

Når trinnene ovenfor er udført, kan du aktivere anbefalinger.

## <a name="azure-ad-identity-configuration"></a>Azure AD-identitetskonfiguration

Dette trin er kun obligatorisk for alle kunder, der kører en infrastruktur som en IaaS-konfiguration (Infra-Structure as a Service). Azure AD Id-konfiguration sker automatisk for kunder, der kører på Azure Service Fabric, men det anbefales, at du kontrollerer, at indstillingen er konfigureret som forventet.

### <a name="setup"></a>Konfiguration

1. Søg efter programsiden i Commerce Headquarters **Azure Active Directory**.
1. Kontrollér, om der findes en post for **RecommendationSystemApplication-1**. Hvis der ikke findes en post, skal du oprette en ved hjælp af følgende oplysninger:

    - **Klient-id**: d37b07e8-dd1c-4514-835d-8b918e6f9727
    - **Navn**: RecommendationSystemApplication-1
    - **Bruger-id**: RetailServiceAccount

1. Gem og luk siden. 

## <a name="turn-on-recommendations"></a>Aktivere anbefalinger

Benyt følgende fremgangsmåde for at aktivere produktanbefalinger.

1. Søg efter **Funktionsstyring** i Commerce Headquarters.
1. Vælg **Alle** for at få vist en liste over tilgængelige funktioner. 
1. Skriv **Anbefalinger** i søgefeltet.
1. Vælg funktionen **Produktanbefalinger**.
1. Vælg **Aktivér nu** i ruden med egenskaber for **Produktanbefalinger**.

![Slå anbefalinger til.](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> - Denne procedure starter processen til oprettelse af produktanbefalingslister. Der kan tage op til flere timer, før listerne er tilgængelige og bliver vist på POS eller i Dynamics 365 Commerce.
> - Med denne konfiguration aktiveres alle anbefalinger ikke. Avancerede funktioner, f.eks. personaliserede anbefalinger, "shop similar look" og "lignende beskrivelse for en butik" styres af de a fokuserede poster i funktionsstyring. Du kan finde oplysninger om aktivering af disse funktioner i Commerce headquarters under [Aktivere personaliserede anbefalinger](personalized-recommendations.md), [, Aktivere "shop similar look"](shop-similar-looks.md) og [aktivere "shop similar description"-anbefalinger](shop-similar-description.md).

## <a name="configure-recommendation-list-parameters"></a>Konfigurere parametre for anbefalingslister

Den AI-ML-baserede produktanbefalingsliste angiver som standard foreslåede værdier. Du kan ændre de foreslåede standardværdier, så de passer til dit firmas flow. Hvis du vil vide mere om, hvordan du ændrer standardparametrene, skal du gå til [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).

## <a name="include-recommendations-in-e-commerce-experiences"></a>Medtag anbefalinger i e-handelserfaringer

Når du har aktiveret anbefalinger i Commerce Headquarters, er de handelsmoduler, der bruges til at vise anbefalinger af e-handelserfaringer, klar til at blive konfigureret. Du kan finde flere oplysninger under [Produktsamlingsmoduler](product-collection-module-overview.md).

## <a name="show-recommendations-on-pos-devices"></a>Vise anbefalinger på POS-enheder

Når anbefalingerne er aktiveret i Commerce headquarter, skal anbefalingspanelet føjes til kontrolelementets POS-skærm ved hjælp af layoutværktøjet. Du kan få mere at vide om denne proces i [Føje et kontrolelement med anbefalinger til posteringsskærmen på POS-enheder](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Aktivere tilpassede anbefalinger

I Dynamics 365 Commerce kan detailhandlere gøre personligt tilpassede produktanbefalinger tilgængelige. På denne måde kan personlige anbefalinger indarbejdes i den online kundeoplevelse og på salgsstedet (POS). Når tilpasningsfunktionen er slået til, kan systemet tilknytte en brugers købs- og produktoplysninger for at generere individuelle produktanbefalinger.

Du kan få flere oplysninger om tilpassede anbefalinger i [Aktivere personlige anbefalinger](personalized-recommendations.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktanbefalinger](product-recommendations.md)

[Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktivere tilpassede anbefalinger](personalized-recommendations.md)

[Aktivere anbefalinger af "Køb tilsvarende"](shop-similar-looks.md)

[Fravælge tilpassede anbefalinger](personalization-gdpr.md)

[Tilføje produktanbefalinger på POS](product.md)

[Føje anbefalinger til transaktionsskærmen](add-recommendations-control-pos-screen.md)

[Justere resultater for AI-ML-anbefalinger](modify-product-recommendation-results.md)

[Oprette overvågede anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Oprette anbefalinger med demonstrationsdata](product-recommendations-demo-data.md)

[Ofte stillede spørgsmål om produktanbefalinger](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
