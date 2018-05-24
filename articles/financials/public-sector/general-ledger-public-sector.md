---
title: Finans i den offentlige sektor
description: "I dette emne beskrives de finansfunktioner, som er tilgængelige for den offentlige sektor."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AdvancedLedgerEntry, JournalizingDefinition, LedgerDerivedFinHierarchies, LedgerFundType, LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 27211
ms.assetid: d737c743-e224-4a30-b4c3-e9568eaddd8c
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d6927eced6b7c36f89a958800b6e1e6aed1d178f
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="general-ledger-in-the-public-sector"></a>Finans i den offentlige sektor

[!include [banner](../includes/banner.md)]

I dette emne beskrives de finansfunktioner, som er tilgængelige for den offentlige sektor.

<a name="how-do-general-ledger-parameters-need-to-be-set-for-public-sector-organizations"></a>Hvordan skal Finansparametre indstilles til offentlige organisationer?
--------------------------------------------------------------------------------

De fleste Finansparametre angives på samme måde for offentlige og private organisationer. Der er desuden offentlige parametre, der bruges til årsafslutningsprocessen i forbindelse med midler. Indstil disse parametre på siden **Finansparametre** i afsnittet **Finans** i **Årsafslutning**-oversigtspanelet:

-   Vælg **Opret ultimoposteringer ved overførsel** for at generere ultimo- og startsaldoposterne. Når dette er valgt, sletter systemet i efterfølgende kørsler af denne proces posteringer fra tidligere kørsler og genererer nye ultimo- og startposter. Hvis dette ikke er valgt, beregner systemet nettoændringen og generere kun den pågældende transaktion for ultimoposter og startsaldi. **Bemærk**! Denne indstilling kræver brug af bogføringsdefinitioner. Hvis du vil vide mere, kan du se under [Bogføringsdefinitioner i den offentlige sektor](posting-definitions-public-sector.md).
-   Vælg **Brug dimensionen Middel til årsafslutningsposteringer** til at aktivere den offentlige version af siden **Primoposter**.
-   Vælg **Brug dimensionen Middel til at overføre indkøbsordrer** til at give mulighed for at angive indstillinger for behandling af årsafslutningen for specifikke midler.

Hvis du vil vide mere om årsafslutningsprocessen for midler, skal du se under [Årsafslutningen i den offentlige sektor](year-end-processing-public-sector.md).

## <a name="what-fund-classes-and-fund-types-are-available"></a>Hvad middelklasser og middeltyper er tilgængelige?
Middelklasserne offentlig, privat, formueforvaltning er tilgængelige for offentlige organisationer, sammen med en klasse af typen Notat. Du skal oprette de middeltyper, organisationen har brug for. Hvis du vil vide mere, kan du se under [Midler i den offentlige sektor](funds-public-sector.md).

## <a name="how-are-financial-dimensions-used-with-funds"></a>Hvordan bruges økonomiske dimensioner med midler?
Middeltal bruges som dimensionsværdier i økonomiske kontonumre, hvor en dimension er knyttet til et middel. Offentlige organisationer kræver normalt afstemte poster for økonomiske dimensioner, der er relateret til midler.

## <a name="what-is-the-easiest-way-to-adjust-or-reverse-ledger-entries"></a>Hvad er den nemmeste måde at justere eller tilbageføre posterne?
Du kan bruge avancerede finansposter til at oprette, tilpasse og tilbageføre finansposter. For eksempel kan avancerede finansposter bruges til at ompostere udgifter, hvis fakturaer fejlagtigt er blevet bogført til den forkerte konto eller det forkerte projekt. Hvis du vil vide mere, skal du se [Avancerede finansposter i den offentlige sektor](advanced-ledger-entries-public-sector.md) og [Bogføringsdefinitioner i den offentlige sektor](posting-definitions-public-sector.md).

## <a name="why-should-i-use-posting-definitions"></a>Hvorfor bruge bogføringsdefinitioner?
Du kan bruge bogføringsdefinitioner til at oprette reskontrokladdelinjer til kildetransaktioner, der opfylder de valgte kriterier – f.eks. til at generere flere, afstemte finansposter baseret på attributter, som f.eks. transaktionstyper og konti. Bogføringsdefinitioner indeholder detaljeret kontrol med Finans-opdateringer, der er oprettet af kildedokumenter, i modsætning til almindeligt anvendte opdateringer af posteringsprofiler. Bogføringsdefinitioner til Finans er påkrævede, hvis du bruger avancerede finansposter. Bogføringsdefinitioner bruges i forbindelse med ultimobehandling af finanskonti. Bogføringsdefinitioner kan bruges til afslutning af konti til pengebalancer eller overførsel af årets resultat på basis af middelklassen og kontoens afslutningstype. Det er et krav, at der bruges bogføringsdefinitioner ved afslutning af finanskonti og til overførsel af saldi til primoperioden i det nye regnskabsår. Hvis du vil vide mere, kan du se under [Bogføringsdefinitioner i den offentlige sektor](posting-definitions-public-sector.md).

## <a name="how-do-i-collect-and-analyze-data-to-meet-the-common-governmentwide-accounting-classification-cgac-requirements"></a>Hvordan indsamler og analyserer jeg data for at opfylde CGAC-krav (Governmentwide Accounting Classification)?
Du kan bruge afledte finansielle hierarkier til at indsamle og analysere data for bogførte transaktioner for bestemte tal i hovedkonto, fuld kontonumre og økonomiske dimensionsværdier. Du kan finde flere oplysninger under [Afledte finansielle hierarkier i den offentlige sektor](derived-financial-hierarchies-public-sector.md).

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Finans](../general-ledger/general-ledger.md)




