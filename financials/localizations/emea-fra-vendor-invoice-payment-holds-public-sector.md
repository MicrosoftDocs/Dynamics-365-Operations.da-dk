---
title: Kreditorbetaling af faktura indeholder i den offentlige sektor i Frankrig
description: "De almindelige processer, der vedrører kreditorspærringer for faktura betalingen i Microsoft Dynamics &quot;AX 7&quot; er suppleres for franske enheder i den offentlige sektor. Dette emne beskriver kreditors faktura indeholder funktionerne bruges af den offentlige sektor i Frankrig."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27331
ms.assetid: 09ece137-e8fd-41ec-ae46-dc922b327999
ms.search.region: France
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 834db5eba21908589ab72e40cfc82bc4cc7cc0a3
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-invoice-payment-holds-in-the-public-sector-in-france"></a>Kreditorbetaling af faktura indeholder i den offentlige sektor i Frankrig

De almindelige processer, der er relateret til faktura betalingen kreditorspærringer i Microsoft Dynamics 365 for operationer er suppleres for franske enheder i den offentlige sektor. Dette emne beskriver kreditors faktura indeholder funktionerne bruges af den offentlige sektor i Frankrig.

<a name="set-up-rules-for-vendor-invoice-payment-holds"></a>Konfigurer regler for faktura betalingen kreditorspærringer
---------------------------------------------

Regler for faktura betalingen kreditorspærringer er angivet på den **Hold** oversigtspanelet på den **betalingsbetingelser** side. Hver regel har tre dele:

-   En brugerrolle, som bogholder, Account manager eller controller. Kun brugere, der er tildelt den angivne rolle kan holde eller frigive en betaling under de angivne betalingsbetingelser.
-   Det mindste antal dage, der skal føjes til betaling af fakturaen forfaldsdato, når en bruger med den valgte rolle frigiver ventepositionen.
-   Det maksimale antal gange, en bruger med den valgte rolle kan indeholde en betaling på hver faktura. **Tip**: Angiv mange 9999 så ubegrænset kapacitet.

For eksempel på Netto 30 betalingsbetingelsen, kan du oprette to regler, én for revisorer og én til direktører. Reglen for revisorer tilføjer mindst 30 dage til at fakturabetalingen forfalder dato, hvor hold frigives, og tillader maksimalt 3 indeholder på en faktura. Reglen for direktører tilføjer mindst 15 dage til betaling af fakturaen forfaldsdato, med højst 10 ventepositioner på en faktura.

## <a name="when-can-i-place-and-release-vendor-invoice-payment-holds"></a>Hvornår kan jeg placere og slippe faktura betalingen kreditorspærringer?
Ventepositioner kan anbringes og udgivet i følgende situationer:

-   Betalingsbetingelser skal konfigureres for en kreditorfaktura, eller for alle kreditorfakturaer for en bestemt kreditor, før du kan placere en venteposition.
-   For at placere eller frigive en venteposition, skal du være tildelt en brugerrolle, hvor reglerne er sat op til betaling ventepositioner.
-   Hvis et hold er aktiv for en kreditor, kan du frigive en venteposition for en faktura for den samme leverandør. Først skal du frigive hold for kreditoren.
-   Du kan ikke frigive en venteposition, medmindre du er den bruger, der placerede hold, eller du er tildelt til den samme brugerrolle som den bruger, der placerede hold.
-   Du kan ikke bogføre en kreditorfaktura, hvis det er en betaling, hold. Hold skal først frigives.

## <a name="where-do-i-place-and-release-vendor-invoice-payment-holds"></a>Hvor placerer og Frigiv kreditorbetaling af faktura jeg har?
### <a name="for-a-vendor"></a>For en kreditor
Placer eller frigive en betalingsspærring for alle fakturaer for den valgte leverandør på den **kreditorposteringer** side eller **udligne posteringer** side. Hvis du markerer en betalingsspærring for en kreditor, omfatter dette hold alle eksisterende fakturaer for den pågældende kreditor. Hvis du slipper en betalingsspærring for en kreditor, indeholder denne udgivelser betalingen hold kun for de kreditorfakturaer, der ikke har individuelle betaling. For eksempel skal du markere individuelle betaling ventepositioner på to forskellige kreditorfakturaer for samme leverandør. Senere kan du placere en betalingsspærring for den pågældende kreditor. Hvis du senere frigiver betalingsspærring for den pågældende leverandør, udgives ikke enkelte lastrum til to kreditorfakturaerne.

### <a name="for-a-vendor-invoice"></a>For en kreditorfaktura

Placer eller frigive en betalingsspærring for en enkelt faktura på de **kreditorfaktura** side eller **udligne posteringer** side.

### <a name="for-a-posted-vendor-invoice"></a>For en bogført kreditorfaktura

Placer eller frigive en betalingsspærring for en kreditorfaktura, der er bogført på de **fakturajournal** side.

### <a name="for-all-vendor-invoices-associated-with-a-purchase-order"></a>For alle kreditorfakturaer, der er knyttet til en indkøbsordre

Placer eller frigive en betalingsspærring for kreditorfakturaer, der er tilknyttet en indkøbsordre på den **udligne posteringer** side.

## <a name="can-i-settle-an-invoice-that-is-on-hold"></a>Kan jeg udligne en faktura, der er i venteposition?
Hvis du er tildelt til den samme brugerrolle som den bruger, der placerede hold, kan du rydde hold fra den **udligne posteringer** side og udligne kreditorfakturaen. Når du placerer en betalingsspærring, den **fakturere betalingsspærring** indstilling vælges automatisk på de **betaling** tab af den **udligne posteringer** side. Dette forhindrer, at en kreditorfaktura udlignes, før spærringen er frigivet.


