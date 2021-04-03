---
title: Moms på onlineordrer beregnes forkert
description: Dette emne indeholder en vejledning til fejlfinding, der kan hjælpe, når moms på onlineordrer beregnes forkert, eller når momsgruppen på salgslinjen ikke er angivet korrekt.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 421df7545e285950ef8a3c4b753c8c6dc5f26422
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585245"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a>Moms på onlineordrer beregnes forkert

[!include [banner](../../includes/banner.md)]

Dette emne indeholder en vejledning til fejlfinding, der kan hjælpe, når moms på onlineordrer beregnes forkert, eller når momsgruppen på salgslinjen ikke er angivet korrekt.

## <a name="description"></a>Betegnelse

Når der afregnes en e-handelsordre, beregnes momsen forkert, eller momsgruppen på salgslinjen angives forkert.

## <a name="resolution"></a>Løsning

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a>Konfigurere momsen for en detailbutik i Commerce Headquarters

Følg disse trin for at konfigurere momsen for en detailbutik i Commerce Headquarters.

1. Gå til **Retail og Commerce \> Kanaler \> Alle butikker**.
1. Vælg den butik, du vil konfigurere moms for.
1. Konfigurer momsoplysningerne for butikken i sektionen **Moms** i oversigtspanelet **Generelt**.

> [!NOTE]
> I forbindelse med produktafhentning fra en butik kommer momsgruppen fra den butik, der er valgt til afhentning. Du kan finde flere oplysninger i [Angivelse af andre momsindstillinger for butikker](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a>Konfigurere momsen for en kundes adresse i Commerce Headquarters

Følg disse trin for at konfigurere momsen for en kundes adresse i Commerce Headquarters.

1. Gå til **Debitorer \> Kunder \> Alle kunder**.
1. Vælg den kunde, du vil konfigurere moms for.
1. Vælg den adresse, du vil konfigurere moms for, i oversigtspanelet **Adresser**, vælg **Flere indstillinger**, og vælg derefter **Avanceret**.
1. Vælg **Momsgruppe** på oversigtspanelet **Generelt**.
1. Vælg den relevante værdi i feltet **Moms**.

> [!NOTE]
> For forsendelse, der involverer moms på kundens adresse, bestemmer linjens leveringsadresse momsgruppen. Hvis kunden afsendes til en eksisterende adresse, der allerede er konfigureret en momsgruppe, vil den eksisterende momsgruppe blive brugt. Som standard har adresser ikke en momsgruppe, når de oprettes.

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a>Konfigurere generelle momsgrupper i Commerce Headquarters

Følg disse trin for at konfigurere generelle momsgrupper i Commerce Headquarters.

1. Gå til **Moms \> Indirekte skatter \> Moms \> Momsgrupper**.
1. Vælg den momsgruppe, der skal konfigureres, i venstre navigation.
1. Konfigurer momsen for momsgruppen i oversigtspanelet **Detaildestinationsbaseret moms**.

> [!NOTE]
> For forsendelse, der ikke involverer moms på kundens adresse, bestemmer leveringsadressen på linjen og den destinationsbaserede moms, der er konfigureret for momsgruppen, momsgruppen. Du kan finde flere oplysninger i [Konfigurere moms for onlinebutikker, der er baseret på destinationen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere moms for onlineordrer](../sales-tax-config.md)
