---
title: Oversigt over momsberegning
description: Dette emne forklarer det overordnede område og funktionerne for til momsberegning.
author: wangchen
ms.date: 11/17/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b5f9f41bdadc76064aa9aee92e27e6b504baf461
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986010"
---
# <a name="tax-calculation-overview"></a>Oversigt over momsberegning

[!include [banner](../includes/banner.md)]

Momsberegning er en særdeles skalerbar flerdimensional tjeneste, som gør det muligt for det globale momsprogram at automatisere og forenkle fastlæggelse og beregning af moms. Momsprogrammet kan konfigureres fuldt ud. De elementer, der kan konfigureres, omfatter, men er ikke begrænset til, den momspligtige datamodel, momskode, matrix for anvendelse af moms og momsberegningsformlen. Momsprogrammet kører på Microsoft Azure-kerneserviceplatformen og tilbyder moderne teknologi og eksponentiel skalerbarhed.

Beregning af moms kan integreres med Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Senere vil det også blive integreret i , Dynamics 365 Project Operations, Dynamics 365 Commerce og andre programmer fra første part og tredjepart.

> [!IMPORTANT]
> Når du aktiverer Momsberegning, kan der udføres visse handlinger på relaterede data i et andet datacenter end det datacenter, der vedligeholder dine tjenestedata. Gennemse [Vilkår og betingelser](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md), før du aktiverer Momsberegning. Det er vigtigt for os at beskytte dine personlige oplysninger. Du kan få mere at vide ved at læse vores [erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=521839).

Momsberegning er et mikrotjenestebaseret momdprogram, der tilbyder eksponentiel skalerbarhed og letter opgaverne på følgende måder:

- Automatisk fastlæggelse af den korrekte momsgruppe, varemomsgruppe og momskoder ved hjælp af en forbedret funktion.
- Understøttelse af flere momsregistreringsnumre for samme juridiske enhed, og automatisk fastlæggelse af det korrekte momsregistreringsnummer og momspligtige transaktioner.
- Understøttelse af fastlæggelse, beregning, bogføring og udligning af moms for flytteordrer.
- Definition af momsberegningsformler og -betingelser, der kan konfigureres, i overensstemmelse med dine specifikke forretningsbehov.
- Deling af momsfastsættelses- og -beregningsløsningen på tværs af juridiske enheder for at spare vedligeholdelsesarbejde og undgå fejl.
- Understøttelse af fastlæggelse af debitor- og kreditormomsregistreringsnumre.
- Fastlæggelse af supportlistekoder.
- Understøttelse af parametre for momsberegning inden for det overordnede skattemyndighedsområde.

Hvis du vil bruge Momsberegning, skal du installere tilføjelsesprogrammet Momsberegning fra dit projekt i Microsoft Dynamics Lifecycle Services. Fuldfør derefter opsætningen i [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/), og aktivér momsberegning i Finance og Supply Chain Management. Du kan finde flere oplysninger i [Start her med momstjeneste](global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Tilgængelighed

Momsberegning er generelt tilgængelig i produktionsmiljøer for alle kunder fra version 10.0.21.

Der vil fortsat blive leveret nye funktioner. Kontrollér ofte den opdaterede udgivelsesplan for at få mere at vide om dækningen og omfanget af de understøttede funktioner.

Momsberegning implementeres i følgende Azure-geografiske områder. Der vil blive tilføjet flere Azure-geografier baseret på kundernes behov.

- Stillehavsområdet
- Australien
- Canada
- Europa
- Japan
- Storbritannien
- United States

> [!NOTE]
> Momsberegning understøtter ikke tidligere version af Dynamics 365, f.eks. Dynamics AX 2012 eller installationer af Dynamics 365 i lokale miljøer.

## <a name="versions"></a>Versioner
Det anbefales, at du importerer og indstiller konfigurationen af momsberegning med den version, der svarer til din version af Finance eller Supply Chain Management.

| Version af Finance eller Supply Chain Management | Version af momskonfiguration               |
| --------------- | --------------------------------------- |
| 10.0.18         | Momskonfiguration – Europe 30.12.82     |
| 10.0.19         | Konfiguration af momsberegning 36.38.193 |
| 10.0.20         | Konfiguration af momsberegning 40.43.208 |
| 10.0.21         | Konfiguration af momsberegning 40.48.215 |
| 10.0.22         | Konfiguration af momsberegning 40.48.215 |
| 10.0.23         | Konfiguration af momsberegning 40.50.221 |
| 10.0.24         | Konfiguration af momsberegning 40.50.225 |


## <a name="data-flow"></a>Dataflow

Her er en oversigt over dataflowprocessen til momsberegning. 

1. I RCS kan du få vist og importere momspligtige dokumentmodelkonfigurationer og konfigurationer af modeltilknytning. Hvis du skal udvide konfigurationer til et avanceret scenario, skal du se [Tilføje datafelter i momskonfigurationer](tax-service-add-data-fields-tax-configurations.md).
2. Opret eller vedligehold momsfunktioner i RCS. Du kan bruge momsfunktioner til at vedligeholde momssatser og regler for momspligtighed.
3. Når opsætningen af momsfunktionen er fuldført, kan du udgive momskonfigurationerne og momsfunktionerne fra RCS til det globale lager.
4. I Finance skal du vælge, hvilken version af momsfunktionens opsætning der skal bruges til en bestemt juridisk enhed.
5. I Finance og Supply Chain Management fungerer transaktioner som sædvanligt. Når Momsberegning er påkrævet, indsamler klienten oplysninger fra transaktionen, f.eks. salgsordren eller indkøbsordren, og pakker oplysningerne som nyttedata. Der sendes derefter en anmodning om beregning af momsen.
6. Momsberegningsanmodningen modtages fra klienten, og beregningen fuldføres. Momsresultatet returneres derefter til klienten.
7. Dynamics 365-klienten modtager momsresultatet og viser resultatet af momsberegningen på en momsside.

## <a name="supported-transactions"></a>Understøttede transaktioner

Momsberegning kan aktiveres via transaktioner. 

Følgende transaktioner understøttes i version 10.0.21: 

- Sales

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

- Indkøb

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

- Lager

    - Flytteordre – send
    - Flytteordre – modtag

Følgende transaktioner understøttes i version 10.0.23: 

- Fritekstfaktura

## <a name="supported-countriesregions"></a>Understøttede lande/områder

Momsberegning kan aktiveres efter juridisk enhed. 

Følgende lande/områder til en juridisk enheds primære adresse understøttes i version 10.0.21:

- Østrig
- Belgien
- Danmark
- Estland
- Finland
- Frankrig
- Tyskland
- Ungarn
- Island
- Italien
- Letland
- Litauen
- Nederlandene
- Norge
- Polen
- Sverige
- Schweiz
- Storbritannien
- USA

Følgende lande/områder til en juridisk enheds primære adresse understøttes i version 10.0.22:

- Australien
- Bahrain
- Canada
- Egypten
- Hong Kong SAR
- Kuwait
- New Zealand
- Oman
- Qatar
- Saudi-Arabien
- Sydafrika
- Forenede Arabiske Emirater

Følgende lande/områder til en juridisk enheds primære adresse understøttes i version 10.0.23:

- Thailand
- Japan
- Malaysia
- Singapore

Følgende lande/områder til en juridisk enheds primære adresse understøttes i version 10.0.24:

- Mexico

## <a name="related-resources"></a>Tilknyttede ressourcer

[Start her med momstjeneste](./global-get-started-with-tax-calculation-service.md)

[Flere momsregistreringsnumre](./emea-multiple-vat-registration-numbers.md)

[Understøttelse af momsfunktion til flytteordre](./tasks/tax-feature-support-for-transfer-order.md)

[Sådan bygger du udvidelse i momstjeneste](./tax-service-add-data-fields-tax-integration-by-extension.md)
