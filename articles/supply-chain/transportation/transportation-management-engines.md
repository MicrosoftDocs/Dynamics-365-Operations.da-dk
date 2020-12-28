---
title: Transportstyringsprogrammer
description: Transportstyringsprogrammer definerer den logik, der bruges til at oprette og behandle transportsatser i Transportstyring.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSGenericEngine, TMSMileageEngine, TMSRateEngine, TMSTransitTimeEngine, TMSZoneEngine, TMSFreightBillTypeAssignment, TMSZoneMaster, TMSEngineParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab6667ac02ca55eeb093fa5854a962ac4357aaac
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424997"
---
# <a name="transportation-management-engines"></a>Transportstyringsprogrammer

[!include [banner](../includes/banner.md)]

Transportstyringsprogrammer definerer den logik, der bruges til at oprette og behandle transportsatser i Transportstyring. 

Et transportstyringsprogram beregner opgaver som f.eks. fragtmandens transportgebyr. Programsystemet gør det muligt at ændre beregningsstrategier ved kørsel baseret på data i Supply Chain Management. Et transportstyringsprogram minder om en plug-in, der er relateret til en bestemt fragtfirmakontrakt.

## <a name="what-engines-are-available"></a>Hvilke programmer er tilgængelige?
Følgende tabel viser de transportstyringsprogrammer, der er tilgængelige.

| Transportstyringsprogram | Beskrivelse                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Satsprogram**                  | Beregner satser.                                                                                                                                                                                                                                                                                                           |
| **Generisk program**               | Enkle hjælpeprogrammer, der bruges af andre programmer, der ikke kræver data fra Supply Chain Management, for eksempel et fordelingsprogram. Fordelingsprogrammer bruges til at reducere de endelige omkostninger for transport til bestemte ordrer og linjer baseret på dimensioner, f.eks. volumen og vægt. |
| **Program til kørte kilometer**               | Beregner transportafstanden.                                                                                                                                                                                                                                                                                     |
| **Program til transittid**          | Beregner den tid, det tager at rejse fra start- til slutdestinationen.                                                                                                                                                                                                                                       |
| **Zoneprogram**                  | Beregner zonen baseret på den aktuelle adresse og beregner antallet af zoner, der skal krydses for at kunne rejse fra adresse A til adresse B.                                                                                                                                                                    |
| **Fragtbrevstype**            | Standardiserer fragtfaktura- og fragtbrevslinjerne og bruges til automatisk sammenholdelse af fragtbreve.                                                                                                                                                                                                                |


<a name="what-engines-must-be-configured-to-rate-a-shipment"></a>Hvilket program skal være konfigureret for at vurdere en forsendelse?
---------------------------------------------------

For at bedømme en forsendelse ved hjælp af et bestemt fragtfirma skal du konfigurere flere transportstyringsprogrammer. **Satsprogram** er påkrævet, men andre transportstyringsprogrammer kan være nødvendige for at understøtte **Satsprogram**. For eksempel kan **Satsprogram** bruges til at hente data fra **Program til kørte kilometer** for at beregne satsen baseret på afstanden mellem kilden og destinationen.

## <a name="whats-required-to-initialize-a-transportation-management-engine"></a>Hvad er påkrævet for at initialisere et transportstyringsprogram?
Et transportstyringsprogram kræver, at du konfigurerer initialiseringsdataene, hvis programmet skal fungere på en bestemt måde. Konfigurationen kan omfatte følgende typer af data:
-   Referencer til andre transportstyringsprogrammer. Du kan finde flere oplysninger i konfigurationseksemplet i dette afsnit.
-   Referencer til .NET-typer, der anvendes af transportstyringsprogrammet.
-   Enkle konfigurationsdata.

I de fleste tilfælde kan du klikke på knappen **Parametre** i konfigurationsformularerne til transportstyringsprogrammet for at konfigurere initialiseringsdataene. **Eksempel på konfiguration af et satsprogram, der refererer til et kørselsprogram** Følgende eksempel viser den konfiguration, der kræves til et satsprogram, der er baseret på .NET-programtypen Microsoft.Dynamics.Ax.Tms.Bll.MileageRateEngine og refererer til et kørselsprogram.

|          Parameter           |                                                                                  Beskrivelse                                                                                  |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <em>RateBaseAssigner</em>   | .NET-typen, der fortolker satsens grundlæggende tildelingsdata for et bestemt skema. Syntaksen for parameterværdien består af to segmenter, der er afgrænset af en lodret streg ( |
|  <em>MileageEngineCode</em>  |                       Kørselsprogramkode, der identificerer kørselsprogramposten i databasen.                        |
| <em>ApportionmentEngine</em> |                        Generisk programkode, der identificerer fordelingsprogrammet i databasen.                        |

<a name="how-is-metadata-used-in-transportation-management-engines"></a>Hvordan bruges metadata i transportstyringsprogrammer?
----------------------------------------------------------

Transportstyringsprogrammer, der er baseret på data, som er defineret i Supply Chain Management, kan bruge forskellige dataskemaer. Transportstyringssystemet gør det muligt for forskellige transportstyringsprogrammer at bruge de samme generiske, fysiske databasetabeller. For at sikre korrekt kørselsfortolkning af programdata kan du definere metadata for tabellerne i databasen. Dette reducerer omkostningerne ved at bygge nye transportstyringsprogrammer, fordi der ikke kræves yderligere tabel- og formularstrukturer i Operations.

## <a name="what-can-be-used-as-search-data-in-rate-calculations"></a>Hvad kan bruges som søgedata i satsberegninger?
De data, du bruger, når du beregner satser, styres af metadatakonfigurationen. For eksempel hvis du vil søge efter satser baseret på postnumre, skal du konfigurere metadata baseret på opslagstypen for et postnummer.

## <a name="do-all-engine-configurations-require-metadata"></a>Kræver alle programkonfigurationer metadata?
Nej, transportstyringsprogrammer, der bruges til at hente de data, som skal bruges til satsberegning fra eksterne systemer, kræver ikke metadata. Satsdataene for disse programmer kan hentes fra eksterne transportfragtsystemer, normalt via en webtjeneste. Du kan for eksempel bruge et kørselsprogram, der henter data direkte fra Bing Maps, så du ikke behøver metadata for dette program.

| **Bemærk!**                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Transportstyringsprogrammer, der leveres sammen med Supply Chain Management, er baseret på data, der hentes fra programmet. Programmer, der opretter forbindelse til eksterne systemer, leveres ikke sammen med Operations. Med den programbaserede udvidelsesmodel kan du dog bygge udvidelser med Visual Studio-værktøjer. |

## <a name="how-do-i-configure-metadata-for-a-transportation-management-engine"></a>Hvordan kan jeg konfigurere metadata til et transportstyringsprogram?
Metadata til transportstyringsprogrammer konfigureres forskelligt for de forskellige programtyper.

| Transportstyringsprogram               | Konfiguration af metadata                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Satsprogram**                                | Kræver en **satsbasistype**. Satsbasistypen indeholder metadata for satsstamdataene og satsbasens tildelingsdata. Strukturen af satsbasens metadata bestemmes af satsprogramtypen. Strukturen af satsbasens tildelingsdata bestemmes af den assigner-type for satsbasen, der er tilknyttet satsprogrammet. Du kan konfigurere satsbasistypen for satsprogrammet på siden **Satsprogram** og på siden **Satsmaster**. |
| **Zoneprogram**                                | Kræver, at metadata konfigureres direkte i zonemasteren.                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Program til transittid** og **Program til kørte kilometer** | Henter metadataene direkte fra formularen til konfiguration af kørselsprogrammet.                                                                                                                                                                                                                                                                                                                                                                                  |

  **Eksempel på metadata for et satsprogram** Transportstyringsprogrammet kræver identifikation af oprindelsesadressen, stat og land/område for destinationen og start- og slutpunkt for forsendelsen. Når du bruger disse krav, vil metadataene se ud som dataene i tabellen nedenfor. Tabellen indeholder også oplysninger om, hvilken type inputdata er påkrævet.
-   Definer disse oplysninger i **Transportstyring** &gt; **Konfiguration** på siden **Satsbasistype**.

| Forløb | Navn                          | Felttype | Datatype | Opslagstype    | Tvungen |
|----------|-------------------------------|------------|-----------|----------------|-----------|
| 1        | Oprindelse – postnummer            | Tilknytning | Streng    | Postnummer    | Markeret  |
| 2        | Destination – delstat             | Tilknytning | Streng    | Stat          |           |
| 3        | Destination – startpostnummer | Tilknytning | Streng    | Postnummer    | Markeret  |
| 4        | Destination – slutpostnummer   | Tilknytning | Streng    | Postnummer    | Markeret  |
| 5        | Destinationsland           | Tilknytning | Streng    | Land/område |           |
