---
title: Gemte standardvisninger for Supply Chain Management
description: Dette emne beskriver de gemte standardvisninger, der er tilgængelige, og forklarer, hvordan de aktiveres.
author: kamaybac
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 943eee819c08704212ceb5e02921c36e7f1032dc
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777833"
---
# <a name="standard-saved-views-for-supply-chain-management"></a>Gemte standardvisninger for Supply Chain Management

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management indeholder adskillige gemte visninger, som du kan aktivere og bruge efter behov. Nogle af disse gemte standardvisninger er optimeret og navngivet til en bestemt rolle eller opgave (f.eks. "Kvalitetskontrol" eller "Modtagelse"). Andre er optimeret, så de kun inkluderer de felter og indstillinger, som Microsoft-brugsstatistikken angiver, at der oftest bruges af kunder. Disse gemte visninger kaldes typisk *forenklede* visninger. Dette emne beskriver de gemte standardvisninger, der er tilgængelige, og forklarer, hvordan de aktiveres og tilpasses.

Du kan få detaljerede oplysninger om, hvordan du arbejder med gemte visninger, herunder standardvisninger, når du har aktiveret dem, under [Gemte visninger](../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json).

## <a name="customizing-the-standard-saved-views"></a>Tilpasse de gemte standardvisninger

Du kan tilpasse de gemte standardvisninger på samme måde, som du kan tilpasse dine egne gemte visninger. Men når du tilpasser en gemt standardvisning, anbefales det på det kraftigste, at du gemmer den tilpassede version under et nyt navn. Ellers kan tilpasningerne overskrives, når du opdaterer Supply Chain Management.

Du kan finde flere oplysninger om, hvordan du tilpasser og omdøber gemte visninger, i [Gemte visninger](../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json).

## <a name="available-saved-views-and-how-to-enable-them"></a>Tilgængelige gemte visninger, og hvordan de aktiveres

Hvis du vil bruge funktionen for gemte visninger, uanset om du vil bruge de gemte standardvisninger, skal du aktivere funktionen *Gemte visninger* i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

De resterende afsnit i dette emne indeholder tabeller, der beskriver de gemte standardvisninger, som aktuelt er tilgængelige for hvert relevant modul. Hver tabel viser navnet på hver enkelt gemt visning – den side, du kan finde den på, og en beskrivelse af den. Hver tabel viser også navnet på den funktion, der indeholder den gemte visning. Du kan få vist en gemt standardvisning i systemet ved at aktivere den angivne funktion i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="saved-views-for-the-inventory-management-module"></a>Gemte visninger for modulet Lagerstyring

I følgende tabel beskrives de gemte visninger, der er tilgængelige for modulet Lagerstyring.

| Side | Visningsnavn | Få vist beskrivelsen | Funktionsnavn |
|---|---|---|---|
| Beholdningsliste | Finans | Denne forenklede visning giver dig mulighed for at fokusere på økonomiske oplysninger, når du administrerer den tilgængelige lagerbeholdning. | Gemte visninger for Lagerstyring (aktiveret som standard fra og med version 10.0.21.) |
| Beholdningsliste | Kvalitetskontrol | Denne forenklede visning giver dig mulighed for at fokusere på kvalitetskontrol, når du administrerer den tilgængelige lagerbeholdning. | Gemte visninger for Lagerstyring (aktiveret som standard fra og med version 10.0.21.) |
| Beholdningsliste | Modtagelse | Denne forenklede visning giver dig mulighed for at fokusere på tilgangsoperationer, når du administrerer den tilgængelige lagerbeholdning. | Gemte visninger for Lagerstyring (aktiveret som standard fra og med version 10.0.21.) |
| Beholdningsliste | Forsendelse | Denne forenklede visning giver dig mulighed for at fokusere på forsendelsesoperationer, når du administrerer den tilgængelige lagerbeholdning. | Gemte visninger for Lagerstyring (aktiveret som standard fra og med version 10.0.21.) |
| Transaktioner | Forenklet | Denne forenklede visning giver dig mulighed for at gennemse lagerstatus, uden at blive villedt af økonomiske oplysninger og andre felter, der bruges mindre ofte. | Gemte visninger for Lagerstyring (aktiveret som standard fra og med version 10.0.21.) |
| Flytteordrer | Forsendelse | Denne forenklede visning giver dig mulighed for at fokusere på forsendelsesoperationer, når du administrerer flytteordrer. | Gemte visninger for Lagerstyring (aktiveret som standard fra og med version 10.0.21.) |
| Flytteordrer | Modtagelse | Denne forenklede visning giver dig mulighed for at fokusere på modtagelsesoperationer, når du administrerer flytteordrer. | Gemte visninger for Lagerstyring (aktiveret som standard fra og med version 10.0.21.) |
| Flytteordrer | Kvalitetskontrol | Denne forenklede visning giver dig mulighed for at fokusere på kvalitetskontrol, når du administrerer flytteordrer. | Gemte visninger for Lagerstyring (aktiveret som standard fra og med version 10.0.21.) |
| Flytteordrer | Finans | Denne forenklede visning giver dig mulighed for at fokusere på økonomiske oplysninger, når du administrerer flytteordrer. | Gemte visninger for Lagerstyring (aktiveret som standard fra og med version 10.0.21.) |

## <a name="saved-views-for-the-master-planning-module"></a>Gemte visninger for modulet Varedisponering

I følgende tabel beskrives de gemte visninger, der er tilgængelige for modulet Varedisponering.

| Side | Visningsnavn | Få vist beskrivelsen | Funktionsnavn |
|---|---|---|---|
| Ordreforslag: Siden med oplysninger om ordreforslag | Forenklet | Denne forenklede visning indeholder kun de felter, der oftest bruges til at arbejde med oplysninger om et enkelt ordreforslag. På denne måde giver den et hurtigere overblik og en strømlinet arbejdsproces. | Gemte visninger for ordreforslag |
| Ordreforslag: Listensiden over ordreforslag | Forenklet | Denne forenklede visning indeholder kun de felter, der oftest bruges til at arbejde med listen over ordreforslag. På denne måde giver den et hurtigere overblik og en strømlinet arbejdsproces. | Gemte visninger for ordreforslag |

## <a name="saved-views-for-the-procurement-and-sourcing-module"></a>Gemte visninger for modulet Indkøb og forsyning

I følgende tabel beskrives de gemte visninger, der er tilgængelige for modulet Indkøb og forsyning.

| Side | Visningsnavn | Få vist beskrivelsen | Funktionsnavn |
|---|---|---|---|
| Indkøbsordredetaljer | Ordreoprettelse | Denne forenklede visning er optimeret til oprettelse af nye indkøbsordrer. | Gemte visninger af indkøbsordrer |
| Indkøbsordredetaljer | Lagerstyring | Denne forenklede visning er optimeret til at udføre lagerrelaterede aktiviteter, f.eks. opfølgning på lagerbeholdning, der er modtaget, modtagelse af lagerbeholdning, kontrol af nettobehov og regulering af ordreantal. | Gemte visninger af indkøbsordrer |
| Indkøbsordredetaljer | Økonomistyring | Denne forenklede visning er optimeret til at udføre finansrelaterede aktiviteter, som f.eks. fakturering og kontrol af priser, totaler og gebyrer. | Gemte visninger af indkøbsordrer |
| Indkøbsordredetaljer | Ordregodkendelse | Denne forenklede visning er optimeret til godkendelse af indkøbsordrer. | Gemte visninger af indkøbsordrer |

## <a name="saved-views-for-the-product-information-management-module"></a>Gemte visninger for modulet Administration af produktoplysninger

I følgende tabel beskrives de gemte visninger, der er tilgængelige for modulet Administration af produktoplysninger.

| Side | Visningsnavn | Få vist beskrivelsen | Funktionsnavn |
|---|---|---|---|
| Listen Frigivne produkter | Produktoprettelse | En forenklet sidevisning, der kun indeholder de felter, der oftest bruges ved oprettelse af produkter. | Gemte visninger for frigivne produkter (aktiveret som standard fra og med version 10.0.21.) |
| Frigivne produktdetaljer | Produktoprettelse | En forenklet sidevisning, der kun indeholder de felter, der oftest bruges ved oprettelse af produkter. | Gemte visninger for frigivne produkter (aktiveret som standard fra og med version 10.0.21.) |
| Frigivne produktdetaljer | Administration af logistikoplysninger | En forenklet sidevisning, der kun indeholder de felter, der oftest bruges ved administration af logistikoplysninger for produkter. | Gemte visninger for frigivne produkter (aktiveret som standard fra og med version 10.0.21.) |
| Frigivne produktdetaljer | Administration af købsoplysninger | En forenklet sidevisning, der kun indeholder de felter, der oftest bruges ved administration af indkøbsoplysninger for produkter. | Gemte visninger for frigivne produkter (aktiveret som standard fra og med version 10.0.21.) |
| Frigivne produktdetaljer | Administration af salgsoplysninger | En forenklet sidevisning, der kun indeholder de felter, der oftest bruges ved administration af salgsrelaterede oplysninger for produkter. | Gemte visninger for frigivne produkter (aktiveret som standard fra og med version 10.0.21.) |

## <a name="saved-views-for-the-production-control-module"></a>Gemte visninger for modulet Produktionsstyring

I følgende tabel beskrives de gemte visninger, der er tilgængelige for modulet Produktionsstyring.

| Side | Visningsnavn | Få vist beskrivelsen | Funktionsnavn |
|---|---|---|---|
| Siden med produktionsordrens stykliste | Forenklet | Denne forenklede visning indeholder kun de felter, der oftest anvendes. På denne måde giver den et hurtigere overblik og en strømlinet arbejdsproces. | Gemte visninger for produktionsstyring (aktiveret som standard fra og med version 10.0.21.) |
| Siden med detaljer om produktionsordrer | Forenklet | Denne forenklede visning indeholder kun de felter, der oftest anvendes. På denne måde giver den et hurtigere overblik og en strømlinet arbejdsproces. | Gemte visninger for produktionsstyring (aktiveret som standard fra og med version 10.0.21.) |
| Siden med produktionsordreplukliste | Forenklet | Denne forenklede visning indeholder kun de felter, der oftest anvendes. På denne måde giver den et hurtigere overblik og en strømlinet arbejdsproces. | Gemte visninger for produktionsstyring (aktiveret som standard fra og med version 10.0.21.) |
| Listeside med produktionsordrer | Forenklet | Denne forenklede visning indeholder kun de felter, der oftest anvendes. På denne måde giver den et hurtigere overblik og en strømlinet arbejdsproces. | Gemte visninger for produktionsstyring (aktiveret som standard fra og med version 10.0.21.) |

## <a name="saved-views-for-the-sales-and-marketing-module"></a>Gemte visninger for modulet Salg og marketing

I følgende tabel beskrives de gemte visninger, der er tilgængelige for modulet Salg og marketing.

| Side | Visningsnavn | Få vist beskrivelsen | Funktionsnavn |
|---|---|---|---|
| Følgeseddelkladde | Journalgennemgang | Denne forenklede visning indeholder kun de felter, der oftest bruges til at gennemse følgeseddeljournaler. | Gemte visninger for salg og marketing |
| Salgsordre | Ordreoprettelse | Denne forenklede visning indeholder kun de felter, der oftest bruges til at oprette salgsordrer. | Gemte visninger for salg og marketing |
| Salgsordre | Ordregennemgang | Denne forenklede visning indeholder kun de felter, der oftest bruges til at gennemgå salgsordrer. | Gemte visninger for salg og marketing |
| Salgstilbud | Oprettelse af tilbud | Denne forenklede visning indeholder kun de felter, der oftest bruges til at oprette salgstilbud. | Gemte visninger for salg og marketing |

## <a name="saved-views-for-the-warehouse-management-module"></a>Gemte visninger for modulet Lokationsstyring

I følgende tabel beskrives de gemte visninger, der er tilgængelige for modulet Lokationsstyring.

| Side | Visningsnavn | Få vist beskrivelsen | Funktionsnavn |
|---|---|---|---|
| Alle laster | Indgående behandling | Denne forenklede visning indeholder kun de felter, der oftest bruges til at behandle indgående laster. | Gemte visninger til lastbehandling |
| Alle laster | Udgående behandling | Denne forenklede visning indeholder kun de felter, der oftest bruges til at behandle udgående laster. | Gemte visninger til lastbehandling |
| Alle forsendelser | Indgående behandling | Denne forenklede visning indeholder kun de felter, der oftest bruges til at behandle indgående forsendelser. | Gemte visninger til forsendelsesbehandling |
| Alle forsendelser | Udgående behandling | Denne forenklede visning indeholder kun de felter, der oftest bruges til at behandle udgående forsendelser. | Gemte visninger til forsendelsesbehandling |
| Alle bølger | Forenklet | Denne forenklede visning indeholder kun de felter, der oftest anvendes. På denne måde giver den et hurtigere overblik og en strømlinet arbejdsproces. | Gemt visning til bølgebehandling |
| Panelet Lastplanlægning | Forenklet | Denne forenklede visning indeholder kun de felter, der oftest anvendes. På denne måde giver den et hurtigere overblik og en strømlinet arbejdsproces. | Gemt visning for lastplanlægningspanelet |
| Arbejdsdetaljer | Forenklet | Denne forenklede visning indeholder kun de felter, der oftest anvendes. På denne måde giver den et hurtigere overblik og en strømlinet arbejdsproces. | Gemt visning af siden med arbejdsdetaljer |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]