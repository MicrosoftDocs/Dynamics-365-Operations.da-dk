---
title: Moms på onlineordrer beregnes forkert
description: Denne artikel indeholder en vejledning til fejlfinding, der kan hjælpe, når moms på onlineordrer beregnes forkert, eller når momsgruppen på salgslinjen ikke er angivet korrekt.
author: Reza-Assadi
ms.date: 02/16/2022
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: eefcfc983a7b3861caa4b4362d2813082b7963a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901615"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a>Moms på onlineordrer beregnes forkert

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder en vejledning til fejlfinding, der kan hjælpe, når moms på onlineordrer beregnes forkert, eller når momsgruppen på salgslinjen ikke er angivet korrekt.

## <a name="description"></a>Betegnelse

Når der afregnes en e-handelsordre, beregnes momsen forkert, eller momsgruppen på salgslinjen angives forkert.

## <a name="resolution"></a>Løsning

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a>Konfigurere generelle momsgrupper i Commerce Headquarters

Følg disse trin for at konfigurere generelle momsgrupper i Commerce Headquarters.

1. Gå til **Moms \> Indirekte skatter \> Moms \> Momsgrupper**.
1. Vælg den momsgruppe, der skal konfigureres, i venstre navigationsrude.
1. Konfigurer momsen for momsgruppen i oversigtspanelet **Detaildestinationsbaseret moms**.

> [!NOTE]
> For forsendelse, der ikke involverer moms, der er bestemt af kundens adresse, bestemmer leveringsadressen på linjen og den destinationsbaserede moms, der er konfigureret for momsgruppen, momsgruppen. Du kan finde flere oplysninger i [Konfigurere moms for onlinebutikker, der er baseret på destinationen](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a>Konfigurere momsen for en detailbutik i Commerce Headquarters

Følg disse trin for at konfigurere momsen for en detailbutik i Commerce Headquarters.

1. Gå til **Retail og Commerce \> Kanaler \> Alle butikker**.
1. Vælg den butik, du vil konfigurere moms for.
1. Konfigurer momsoplysningerne for butikken i sektionen **Moms** i oversigtspanelet **Generelt**.

> [!NOTE]
> I forbindelse med produktafhentning fra en butik kommer momsgruppen fra den butik, der er valgt til afhentning. Du kan finde flere oplysninger i [Angivelse af andre momsindstillinger for butikker](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a>Konfigurere momsen for en kundes adresse i Commerce Headquarters

Følg disse trin for at konfigurere momsen for en kundes adresse i Commerce Headquarters.

1. Gå til **Debitorer \> Kunder \> Alle kunder**.
1. Vælg den kunde, du vil konfigurere moms for.
1. Vælg den adresse, du vil konfigurere moms for, i oversigtspanelet **Adresser**, vælg **Flere indstillinger**, og vælg derefter **Avanceret**.
1. Vælg **Momsgruppe** på oversigtspanelet **Generelt**.
1. Vælg den relevante værdi i feltet **Moms**.

> [!NOTE]
> For forsendelse, der involverer moms på kundens adresse, bestemmer linjens leveringsadresse momsgruppen. Hvis kunden afsendes til en eksisterende adresse, der allerede er konfigureret en momsgruppe, vil den eksisterende momsgruppe blive brugt. Som standard har adresser ikke en momsgruppe, når de oprettes.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere moms for onlineordrer](../sales-tax-config.md)
