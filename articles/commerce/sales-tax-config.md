---
title: Konfigurere moms for onlineordrer
description: Denne artikel giver en oversigt over valg af momsgrupper for forskellige onlineordretyper i Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 04/02/2021
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
ms.openlocfilehash: ac9fefe68663d76b3461d3209530976f66b113ba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906880"
---
# <a name="configure-sales-tax-for-online-orders"></a>Konfigurere moms for onlineordrer

[!include [banner](includes/banner.md)]

Denne artikel giver en oversigt over momsgruppevalg for forskellige onlineordretyper med enten destinationsbaserede eller kundekontobaserede momsindstillinger. 

Din e-handelskanal skal måske understøtte valgmuligheder som levering eller afhentning af onlineordrer. Om moms kan anvendes afhænger af den indstilling, som dine onlinekunder vælger. 

## <a name="destination-based-taxes-for-online-orders"></a>Destinationsbaseret moms for onlineordrer

Generelt defineres moms på onlineordrer, der sendes til kundeadresser, af destinationen. Hver momsgruppe har en konfiguration for moms, der er baseret på en detaildestination, hvor forretningen kan definere destinationsoplysninger som f.eks. land eller område, stat, region og by i en hierarkisk struktur.

### <a name="orders-delivered-to-customer-address"></a>Ordrer, der leveres til en kundeadresse

Når en onlineordre afgives, bruger Commerce-momsprogrammet leveringsadressen for alle linjevarer i ordren og finder momsgrupper med tilsvarende destinationsbaserede momskriterier. F.eks. kan momsprogrammet for en onlineordre med leveringsadresse for en linjevare i San Francisco, Californien, finde momsgruppen og momskoden for Californien og derefter beregne skatten for hvert linjeelement tilsvarende.

### <a name="order-pick-up-in-store"></a>Ordreafhentning i butik

For ordrelinjer, hvor der er angivet afhentning i butik eller ved fortovskant, anvendes momsgruppen fra den valgte afhentningsbutik. Du kan finde flere oplysninger om, hvordan du konfigurerer moms for en bestemt butik, i [Angive andre momsindstillinger for butikker](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

## <a name="customer-account-based-taxes-for-online-orders"></a>Kundekontobaseret moms for onlineordrer

Der kan være et forretningsscenarie, hvor du vil konfigurere en momsgruppe på en bestemt kundekonto i Commerce Headquarters. Der er to steder i hovedkontoret, hvor du kan konfigurere moms på en kundekonto. Hvis du vil åbne disse, skal du først gå til kundedetaljesiden ved at gå til **Retail og Commerce \> Kunder \> Alle kunder** og derefter vælge en kunde.

De to steder, hvor du kan konfigurere moms for en kundekonto, er:

- **Momsgruppe** i oversigtspanelet **Faktura og levering** på siden med kundeoplysninger. 
- **Moms** i oversigtspanelet **Generelt** på siden **Administrer adresser**. Hvis du vil derhen fra siden med kundeoplysninger, skal du vælge en bestemt adresse i oversigtspanelet **Adresser** og derefter vælge **Avanceret**.

> [!TIP]
> Hvis du kun vil anvende destinationsbaseret moms for onlinekundeordrer og undgå kundekontobaseret moms, skal du sikre dig, at feltet **Momsgruppe** er tomt i oversigtspanelet **Faktura og levering** for kundens detaljeside. Hvis du vil sikre, at nye kunder, der logger på ved hjælp af onlinekanalen, ikke arver momsgruppeindstillingerne fra standardindstillinger for kunder eller kundegrupper, skal du sikre dig, at feltet **Momsgruppe** også er tomt for standardindstillingerne for kunder og kundegrupper for onlinekanalen (**Retail og Commerce \> Kunder \> Kundegrupper**).

## <a name="determine-destination-based-tax-or-customer-account-based-tax-applicability"></a>Bestemme destinationsbaseret moms eller kundekontobaseret anvendelse af moms 

I følgende tabel forklares det, om destinationsbaseret moms eller kundekontobaseret moms anvendes for onlineordrer. 

| Kundetype | Leveringsadresse                   | Kunde > Faktura og levering > Momsgruppe? | Adresse på kundekonto i hovedkontoret? | Kundeadresse > Avanceret > Generelt > Momsgruppe?                                              | Anvendt momsgruppe      |
|---------------|------------------------------------|-----------------------------------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------|------------------------------|
| Gæst         | Manhattan, NY                      | Nej (tom)                                                | Nej (tom)                              | Nej (tom)                                                                                                   | NY (destinationsbaseret moms) |
| Logget på     | Austin, TX                          | Nej (tom)                                             | Ja                               | None<br/><br/>Ny adresse, der er tilføjet via onlinekanalen.                                                            | TX (destinationsbaseret moms) |
| Logget på     | San Francisco, CA (afhentning i butik) | Ja (NY)                                            | Ikke anvendelig                              | Ikke anvendelig                                                                                                    | CA (destinationsbaseret moms) |
| Logget på     | Houston, TX                         | Ja (NY)                                            | Ja                               | Ja (NY)<br/><br/>Ny adresse, der er tilføjet via onlinekanal, og momsgruppe, der er nedarvet fra kundekontoen. | NY (kundekontobaseret moms)  |
| Logget på     | Austin, TX                          | Ja (NY)                                            | Ja                               | Ja (NY)<br/><br/>Ny adresse, der er tilføjet via onlinekanal, og momsgruppe, der er nedarvet fra kundekontoen. | NY (kundekontobaseret moms)  |
| Logget på     | Sarasota, FL                       | Ja (NY)                                            | Ja                               | Ja (WA)<br/><br/>Angivet manuelt til WA.                                                                          | WA (kundekontobaseret moms)  |
| Logget på     | Sarasota, FL                       | Nej (tom)                                                | Ja                               | Ja (WA)<br/><br/>Angivet manuelt til WA.                                                                          | WA (kundekontobaseret moms)  |

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere moms for onlinebutikker, der er baseret på destinationen](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)

[Momsoversigt](../finance/general-ledger/indirect-taxes-overview.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Momsberegningsmetoder i feltet Grundlag](../finance/general-ledger/sales-tax-calculation-methods-origin-field.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Tildeling og tilsidesættelser af moms](../supply-chain/procurement/tasks/sales-tax-assignment-overrides.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Indstillinger for beregning af hele beløbet og intervaller for momskoder](../finance/general-ledger/whole-amount-interval-options-sales-tax-codes.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Beregning af momsfritagelse](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]