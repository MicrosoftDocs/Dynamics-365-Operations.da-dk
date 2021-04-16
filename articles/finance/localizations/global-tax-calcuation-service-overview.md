---
title: Momsberegningstjeneste (forhåndsversion)
description: Dette emne forklarer det overordnede område og funktionerne for tjenesten til momsberegning.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818218"
---
# <a name="tax-calculation-service-preview"></a>Momsberegningstjeneste (forhåndsversion)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Tjenesten til momsberegning er en særdeles skalerbar flerdimensional tjeneste, som gør det muligt for det globale momsprogram at automatisere og forenkle fastlæggelse og beregning af moms. Momsprogrammet kan konfigureres fuldt ud. De elementer, der kan konfigureres, omfatter, men er ikke begrænset til, den momspligtige datamodel, momskode, matrix for anvendelse af moms og momsberegningsformlen. Momsprogrammet kører på Microsoft Azure-kerneserviceplatformen og tilbyder moderne teknologi og eksponentiel skalerbarhed.

Tjenesten til beregning af moms kan integreres med Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Senere vil det også blive integreret i , Dynamics 365 Project Operations, Dynamics 365 Commerce og andre programmer fra første part og tredjepart.

Tjenesten til momsberegning er et Microsoft-baseret momsprogram, der tilbyder eksponentiel skalerbarhed. Du kan få hjælp til at udføre følgende opgaver:

- Konfigurer momsberegningstjenesten via Regulatory Configuration Service (RCS). RCS er en udvidet version af ER-designeren (Elektronisk rapportering) og er tilgængelig som en enkeltstående tjeneste.
- Konfigurer momsmatrixen til automatisk at bestemme momskoder og -satser.
- Konfigurer momsmatrixen til automatisk at bestemme momsregistreringsnummer.
- Konfigurer momsberegningsdesigneren for at definere formler og betingelser.
- Del momsfastsættelses- og -beregningsløsningen på tværs af juridiske enheder.

Hvis du vil bruge tjenesten til momsberegning, skal du installere tilføjelsesprogrammet Momsberegningstjeneste fra dit projekt i Microsoft Dynamics Lifecycle Services (LCS). Fuldfør derefter opsætningen i RCS, og aktivér tjenesten til momsberegning i Finance og Supply Chain Management. Du kan finde flere oplysninger i [Start her med momstjeneste](https://go.microsoft.com/fwlink/?linkid=2138482).

## <a name="availability"></a>Tilgængelighed

Tjenesten til momsberegning er kun tilgængelig i sandkassemiljøer og for udvalgte kunder via et offentligt forhåndsversionsprogram. Senere vil den blive generelt tilgængelig for alle kunder og i produktionsmiljøer.

Der vil fortsat blive leveret nye funktioner i tjenesten til momsberegning. Du skal derfor sørge for ofte at læse den sidste nye dokumentation for at få mere at vide om dækning og området af understøttede funktioner.

Tjenesten til momsberegning implementeres i følgende Azure-geografiske områder. Den vil også blive implementeret i flere Azure-geografiske områder baseret på kundernes behov:

- United States
- Europa
- Frankrig
- Storbritannien

> [!NOTE]
> Tjenesten til momsberegning understøtter ikke implementering i det lokale miljø af Dynamics 365. Den understøtter heller ikke tidligere versioner, f.eks. Dynamics AX 2012.

## <a name="feature-highlights"></a>Fremhævning af funktioner

- En konfigurerbar momsmatrix til automatisk at bestemme og beregne moms
- Understøttelse af flere momsregistreringsnumre
- Understøttelse af flytteordre til fastlæggelse og beregning af moms
- Understøttelse af flytteordre til fastlæggelse af flere momsregistreringsnumre

## <a name="supported-transactions"></a>Understøttede transaktioner

Tjenesten til momsberegning kan aktiveres via juridisk enhed og transaktion. Følgende transaktioner understøttes:

- Salgsproces

    - Salgstilbud
    - Salgsordre
    - Bekræftelse
    - Plukliste
    - Følgeseddel
    - Salgsfaktura
    - Kreditnota
    - Returordre
    - Overskrift til diverse gebyrer
    - Linje til diverse gebyrer

- Indkøbsproces

    - Indkøbsordre
    - Bekræftelse
    - Tilgangsliste
    - Produktkvittering
    - Indkøbsfaktura
    - Overskrift til diverse gebyrer
    - Linje til diverse gebyrer
    - Kreditnota
    - Returordre
    - Indkøbsrekvisition
    - Diverse gebyrer til indkøbsrekvisitionslinje
    - Tilbudsanmodning
    - Diverse gebyrer i overskrift til tilbudsanmodning
    - Diverse gebyrer i linje til tilbudsanmodning

- Lagerproces

    - Flytteordre – send
    - Flytteordre – modtag

## <a name="related-resources"></a>Tilknyttede ressourcer

[Start her med momstjeneste](https://go.microsoft.com/fwlink/?linkid=2138482)

[Flere momsregistreringsnumre](https://go.microsoft.com/fwlink/?linkid=2153387)

[Understøttelse af momsfunktion til flytteordre](https://go.microsoft.com/fwlink/?linkid=2153388)

[Sådan bygger du udvidelse i momstjeneste](https://go.microsoft.com/fwlink/?linkid=2138483)
