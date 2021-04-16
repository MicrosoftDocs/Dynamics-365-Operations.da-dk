---
title: Konfigurere moms for onlineordrer
description: Dette emne giver en oversigt over valg af momsgrupper for forskellige onlineordretyper i Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 68b7e59a1e1ea18bdcd4e7a9117e4892407f40ff
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791841"
---
# <a name="configure-sales-tax-for-online-orders"></a>Konfigurere moms for onlineordrer

[!include [banner](includes/banner.md)]

Dette emne giver en oversigt over valg af momsgrupper for forskellige onlineordretyper. 

Din e-handelskanal vil måske understøtte valgmuligheder som levering eller afhentning af onlineordrer. Om moms kan anvendes afhænger af den indstilling, som dine onlinebrugere vælger. Når en kunde på et websted vælger at købe en vare online og får den leveret til en adresse, bestemmes momsen på basis af kundens indstilling for momsgruppen for leveringsadressen. Når en kunde vælger at afhente en købt vare i en butik, bestemmes momsen ud fra indstillingen for afhentningsbutikkens momsgruppe. 

## <a name="orders-shipped-to-a-customer-address"></a>Ordrer, der sendes til en kundeadresse 

Generelt defineres moms på onlineordrer, der sendes til kundeadresser, af destinationen. Hver momsgruppe har en konfiguration for moms, der er baseret på en detaildestination, hvor forretningen kan definere destinationsoplysninger, som f.eks. land/område, stat, region og by i en hierarkisk struktur. Når en onlineordre afgives, bruger Commerce-momsprogrammet leveringsadressen for alle linjevarer i ordren og finder momsgrupper med tilsvarende destinationsbaserede momskriterier. F.eks. kan momsprogrammet for en onlineordre med leveringsadresse for en linjevare i San Francisco, Californien, finde momsgruppen og momskoden for Californien og derefter beregne skatten for hvert linjeelement tilsvarende.  

## <a name="customer-based-tax-groups"></a>Kundebaserede momsgrupper

I Commerce Headquarters er der to steder, hvor kundemomsgrupper kan konfigureres:

- **Kundens profil**
- **Kundens leveringsadresse**

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a>Hvis en kundes profil har en konfigureret momsgruppe

En kundeprofilpost i Headquarters kan have en konfigureret momsgruppe, men til onlineordrer bruges den momsgruppe, der er konfigureret i en kundeprofil, ikke af momsprogrammet. 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a>Hvis en kundes leveringsadresse har en konfigureret momsgruppe

Hvis der er konfigureret en momsgruppe for en kundes leveringsadressepost, og der leveres en onlineordre (eller linjevare) til kundens leveringsadresse, vil den momsgruppe, der er konfigureret i kundens adressepost, blive brugt af momsprogrammet til momsberegninger.

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a>Konfigurere en momsgruppe for en kundes leveringsadressepost

Hvis du vil konfigurere en momsgruppe for en kundes leveringsadressepost i Commerce Headquarters, skal du følge disse trin.

1. Gå til **Alle debitorer**, og vælg derefter den ønskede debitor. 
1. I oversigtspanelet **Adresser** skal du vælge den ønskede adresse og derefter vælge **Flere indstillinger \> Avanceret**. 
1. Angiv momsværdien efter behov under fanen **Generelt** på siden **Administrer adresser**.

> [!NOTE]
> Momsgruppen defineres ved hjælp af leveringsadressen for ordrelinjen, og den destinationsbaserede moms konfigureres i selve momsgruppen. Du kan finde flere oplysninger i [Konfigurere moms for onlinebutikker, der er baseret på destinationen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

## <a name="order-pickup-in-store"></a>Ordreafhentning i butik

For ordrelinjer, hvor der er angivet afhentning i butik eller ved fortovskant, anvendes momsgruppen fra den valgte afhentningsbutik. Du kan finde flere oplysninger om, hvordan du konfigurerer momsgruppen for en bestemt butik, i [Angive andre momsindstillinger for butikker](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

> [!NOTE]
> Når en ordrelinje afhentes i en butik, vil en kundes indstillinger for adressemoms (hvis de er angivet) blive ignoreret af momsprogrammet, og afhentningsbutikkens momskonfiguration vil blive anvendt. 

## <a name="additional-resources"></a>Yderligere ressourcer

[Momsoversigt](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[Momsberegningsmetoder i feltet Grundlag](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[Tildeling og tilsidesættelser af moms](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[Indstillinger for beregning af hele beløbet og intervaller for momskoder](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[Beregning af momsfritagelse](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]