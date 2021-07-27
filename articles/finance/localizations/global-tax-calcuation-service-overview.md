---
title: Momsberegning (prøveversion)
description: Dette emne forklarer det overordnede område og funktionerne for til momsberegning.
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bab6e0e0ea1b9fb7f598e37843b52e3ba9c7f94e
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/03/2021
ms.locfileid: "6336626"
---
# <a name="tax-calculation-preview"></a>Momsberegning (prøveversion)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Momsberegning er en særdeles skalerbar flerdimensional tjeneste, som gør det muligt for det globale momsprogram at automatisere og forenkle fastlæggelse og beregning af moms. Momsprogrammet kan konfigureres fuldt ud. De elementer, der kan konfigureres, omfatter, men er ikke begrænset til, den momspligtige datamodel, momskode, matrix for anvendelse af moms og momsberegningsformlen. Momsprogrammet kører på Microsoft Azure-kerneserviceplatformen og tilbyder moderne teknologi og eksponentiel skalerbarhed.

Beregning af moms kan integreres med Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Senere vil det også blive integreret i , Dynamics 365 Project Operations, Dynamics 365 Commerce og andre programmer fra første part og tredjepart.

> [!IMPORTANT]
> Når du aktiverer tjenesten Momsberegning, kan der udføres visse handlinger på relaterede data i et andet datacenter end det datacenter, der vedligeholder dine tjenestedata. Gennemse [Vilkår og betingelser](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md), før du aktiverer tjenesten Momsberegning. Det er vigtigt for os at beskytte dine personlige oplysninger. Du kan få mere at vide ved at læse vores [erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=521839).

Momsberegning er et mikroservicebaseret momsprogram, der tilbyder eksponentiel skalerbarhed. Du kan få hjælp til at udføre følgende opgaver:

- Konfigurer momsberegning via Regulatory Configuration Service (RCS). RCS er en udvidet version af ER-designeren (Elektronisk rapportering) og er tilgængelig som en enkeltstående tjeneste.
- Konfigurer momsmatrixen til automatisk at bestemme momskoder og -satser.
- Konfigurer momsmatrixen til automatisk at bestemme momsregistreringsnummer.
- Konfigurer momsberegningsdesigneren for at definere formler og betingelser.
- Del momsfastsættelses- og -beregningsløsningen på tværs af juridiske enheder.

Hvis du vil bruge tjenesten til momsberegning, skal du installere tilføjelsesprogrammet Momsberegningstjeneste fra dit projekt i Microsoft Dynamics Lifecycle Services (LCS). Fuldfør derefter opsætningen i RCS, og aktivér tjenesten til momsberegning i Finance og Supply Chain Management. Du kan finde flere oplysninger i [Start her med momstjeneste](./global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Tilgængelighed

Momsberegning er kun tilgængelig i sandkassemiljøer og for udvalgte kunder via et offentligt forhåndsversionsprogram. Senere vil den blive generelt tilgængelig for alle kunder og i produktionsmiljøer.

Der leveres fortsat nye funktioner, så du skal derfor sørge for ofte at læse den sidste nye dokumentation for at få mere at vide om dækning og området af understøttede funktioner.

Momsberegning implementeres i følgende Azure-geografiske områder. Den vil også blive implementeret i flere Azure-geografiske områder baseret på kundernes behov:

- United States
- Europa

> [!NOTE]
> Momsberegning understøtter ikke implementering i det lokale miljø af Dynamics 365. Den understøtter heller ikke tidligere versioner, f.eks. Dynamics AX 2012.

## <a name="feature-highlights"></a>Fremhævning af funktioner

- En konfigurerbar momsmatrix til automatisk at bestemme og beregne moms
- Understøttelse af flere momsregistreringsnumre
- Understøttelse af flytteordre til fastlæggelse og beregning af moms
- Understøttelse af flytteordre til fastlæggelse af flere momsregistreringsnumre

## <a name="supported-transactions"></a>Understøttede transaktioner

Momsberegning kan aktiveres via juridisk enhed og transaktion. Følgende transaktioner understøttes:

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

[Start her med momstjeneste](./global-get-started-with-tax-calculation-service.md)

[Flere momsregistreringsnumre](./emea-multiple-vat-registration-numbers.md)

[Understøttelse af momsfunktion til flytteordre](./tasks/tax-feature-support-for-transfer-order.md)

[Sådan bygger du udvidelse i momstjeneste](./tax-service-add-data-fields-tax-integration-by-extension.md)
