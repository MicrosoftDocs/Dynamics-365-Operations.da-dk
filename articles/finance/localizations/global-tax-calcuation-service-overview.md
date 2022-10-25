---
title: Oversigt over momsberegning
description: Denne artikel forklarer det overordnede område og funktionerne til momsberegning.
author: EricWangChen
ms.date: 09/08/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.search.form: TaxIntegrationTaxServiceParameters
ms.openlocfilehash: cafc4c7089e0c042fc65c1e3fd21f8f1e930b785
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689878"
---
# <a name="tax-calculation-overview"></a>Oversigt over momsberegning

[!include [banner](../includes/banner.md)]

Momsberegning er en særdeles skalerbar flerdimensional tjeneste, som gør det muligt for det globale momsprogram at automatisere og forenkle fastlæggelse og beregning af moms. Momsprogrammet kan konfigureres fuldt ud. De elementer, der kan konfigureres, omfatter, men er ikke begrænset til, den momspligtige datamodel, momskode, matrix for anvendelse af moms og momsberegningsformlen. Momsprogrammet kører på Microsoft Azure-kerneserviceplatformen og tilbyder moderne teknologi og eksponentiel skalerbarhed.

Momsberegning integreres med Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Senere vil det også blive integreret i Dynamics 365 Project Operations, Dynamics 365 Commerce og andre programmer fra første part og tredjepart.

> [!IMPORTANT]
> Når du aktiverer Momsberegning, kan der udføres visse handlinger på relaterede data i et andet datacenter end det datacenter, der vedligeholder dine tjenestedata. Gennemse [Vilkår og betingelser](https://go.microsoft.com/fwlink/?linkid=2156043), før du aktiverer Momsberegning. Det er vigtigt for os at beskytte dine personlige oplysninger. Du kan få mere at vide ved at læse vores [erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=521839).

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
- Brasilien
- Canada
- Europa
- Frankrig
- Indien
- Japan
- Sydafrika
- Schweiz
- Forenede Arabiske Emirater
- Storbritannien
- United States

> [!NOTE]
> Momsberegning understøtter ikke tidligere version af Dynamics 365, f.eks. Dynamics AX 2012 eller installationer af Dynamics 365 i lokale miljøer.

## <a name="versions"></a>Versioner
Det anbefales, at du importerer og indstiller konfigurationen af momsberegning med den version, der svarer til din version af Finance eller Supply Chain Management.

| Version af Finance eller Supply Chain Management | Version af momskonfiguration               |
| --------------- | --------------------------------------- |
| 10.0.31         | Konfiguration af momsberegning 40.56.240 |
| 10.0.30         | Konfiguration af momsberegning 40.55.239 |
| 10.0.29         | Konfiguration af momsberegning 40.55.236 |
| 10.0.28         | Konfiguration af momsberegning 40.54.234 |
| 10.0.27         | Konfiguration af momsberegning 40.54.234 |


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

Følgende tabel indeholder de posteringer, der understøttes i den tilsvarende version.

| Version | Transaktioner |
|---------|--------------|
| 10.0.29 | Periodiske kladder |
| 10.0.28 | Kreditorbetalingskladde<br> Debitorbetalingskladde | 
| 10.0.26 | Finanskladder<br> kreditorfakturakladde |
| 10.0.23 | Fritekstfaktura |
| 10.0.21| Sales<br><ul><li>Salgstilbud</li><li>Salgsordre</li><li>Bekræftelse</li><li>Plukliste</li><li>Følgeseddel</li><li>Salgsfaktura</li><li>Kreditnota</li><li>Returordre</li><li>Overskrift til diverse gebyrer</li><li>Linje til diverse gebyrer</li></ul>Indkøb<br><ul><li>Indkøbsordre</li><li>Bekræftelse</li><li>Tilgangsliste</li><li>Produktkvittering</li><li>Indkøbsfaktura</li><li>Overskrift til diverse gebyrer</li><li>Linje til diverse gebyrer</li><li>Kreditnota</li><li>Returordre</li><li>Indkøbsrekvisition</li><li>Diverse gebyrer til indkøbsrekvisitionslinje</li><li>Tilbudsanmodning</li><li>Diverse gebyrer i overskrift til tilbudsanmodning</li><li>Diverse gebyrer i linje til tilbudsanmodning</li></ul>Lagerbeholdning<ul><li>Flytteordre – send</li><li>Flytteordre – modtag</li></ul>|

## <a name="supported-countriesregions"></a>Understøttede lande/områder

Momsberegning kan køres med understøttede funktioner til lokalisering. Den følgende tabel indeholder en liste over lande/områder for den primære adresse for den juridiske enhed.

| Version | Land/område |
|---------|----------------|
| 10.0.26 | - Kina <br>- Tjekkiet<br>- Spanien |
| 10.0.24 | Mexico |
| 10.0.23 | - Thailand <br>- Japan <br>- Malaysia <br>- Singapore |
| 10.0.22 | - Australien<br>- Bahrain <br>- Canada<br>- Egypten <br>- Hong Kong SAR <br>- Kuwait <br>- New Zealand <br>- Oman <br>- Qatar <br>- Saudi-Arabien <br>- Sydafrika <br>- Forenede Arabiske Emirater |
| 10.0.21 | - Østrig <br>- Belgien <br>- Danmark <br>- Estland <br>- Finland <br>- Frankrig <br>- Tyskland <br>- Ungarn <br>- Island <br>- Irland <br>- Italien <br>- Letland <br>- Litauen <br>- Nederlandene <br>- Norge <br>- Polen <br>- Sverige <br>- Schweiz <br>- Storbritannien <br>- United States |

Hvis et land/område ikke er lokaliseret af Microsoft, kan Momsberegning også aktiveres og køres med andre globale funktioner.

## <a name="related-resources"></a>Tilknyttede ressourcer

[Start her med momstjeneste](./global-get-started-with-tax-calculation-service.md)

[Flere momsregistreringsnumre](./emea-multiple-vat-registration-numbers.md)

[Understøttelse af momsfunktion til flytteordre](./tasks/tax-feature-support-for-transfer-order.md)

[Sådan bygger du udvidelse i momstjeneste](./tax-service-add-data-fields-tax-integration-by-extension.md)
