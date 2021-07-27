---
title: Oversigt over konfiguration af Kreditor
description: I denne artikel beskrives de sider, som du kan bruge til at konfigurere grundlæggende og valgfri funktioner for Kreditor. Der beskrives også de installationstrin, du skal fuldføre, før du begynder at konfigurere Kreditor.
author: abruer
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "24671"
- intro-internal
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d42b3aa5b692a300a4a2cb3eb64c9a014aa52f9e
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/03/2021
ms.locfileid: "6339078"
---
# <a name="configure-accounts-payable-overview"></a>Oversigt over konfiguration af Kreditor

[!include [banner](../includes/banner.md)]

I denne artikel beskrives de sider, som du kan bruge til at konfigurere grundlæggende og valgfri funktioner for Kreditor. Der beskrives også de installationstrin, du skal fuldføre, før du begynder at konfigurere Kreditor.

## <a name="prerequisites-for-accounts-payable-setup"></a>Forudsætninger for konfiguration af kreditorer

Inden du kan konfigurere kreditorer, skal du fuldføre følgende konfiguration:

-   I Finans:
    -   Hvis du vil bruge betalingskladder, skal du konfigurere betalingskladderne.
    -   Hvis du planlægger at køre valutakursreguleringer, skal du oprette valutakoder på siden Valutaer, konfigurere valutakurstyper på siden Valutakurstyper og konfigurere valutakurser på siden Valutakurser.
-   I Kontant- og bankstyring skal du konfigurere bankkonti, der skal bruges med betalingsmetoder.

## <a name="setup-pages-for-accounts-payable"></a>Opsætning af sider for kreditor

Du kan bruge følgende sider til at konfigurere de grundlæggende funktioner i Kreditor for hver juridisk enhed. De viste sider vises i den rækkefølge, som det anbefales at konfigurere dem i. Du kan gøre konfigureringsprocessen nemmere ved at oprette skabeloner fra de første poster, du opretter. I en skabelon bliver der typisk indtastet værdier i mange felter for at afspejle de egenskaber, som organisationen ønsker at anvende for en bestemt type kreditor.
1.  På siden Betalingsbetingelser skal du definere de betalingsbetingelser, du knytter til salgsordrer, indkøbsordrer, debitorer og kreditorer, og som bestemmer forfaldsdatoer for fakturaer. Du kan finde flere oplysninger under [Definere kreditorbetalingsgebyrer](tasks/define-vendor-payment-fees.md).
2.  På siden Betalingsmåder – kreditorer skal du oprette og vedligeholde oplysninger om, hvordan organisationen betaler sine kreditorer.
3.  På siden Kreditorgruppe skal du oprette og vedligeholde grupper af kreditorer, der deler vigtige parametre for bogføring, udligning og betaling, rapportering og budgettering.
4.  På siden Kreditorposteringsprofiler skal du definere, hvordan kreditorposter bogføres i finansmodulet.
5.  På siden Kreditorparametre kan du konfigurere de standardindstillinger, der anvendes, hvis en mere specifik indstilling ikke er angivet, parametre for forskellige typer funktioner og forskellige nummerserier for kreditorer.
6.  På siden Formularopsætning kan du definere de forskellige dokumenter, der er relateret til kreditorer, og som organisationen bruger til at holde styr på tilgange fra kreditorer og til at angive årsager til betalingsflowet til kreditorer.
7.  På siden Kreditorer kan du oprette og vedligeholde kreditorkonti og også de skattemyndigheder, som din organisation indberetter moms til.

## <a name="optional-setup-pages-for-accounts-payable"></a>Valgfri opsætningssider for Kreditor
Ud over de grundlæggende funktioner har kreditor andre funktioner, du kan konfigurere.

De ekstra opsætningssider er organiseret efter funktioner.

**Politikker**
-   På siden Politik for kreditorfaktura kan du angive politikker for kreditorfakturaer.

**Fakturasammenholdelse**

-   På siden Tolerancer for fakturatotaler kan du angive tolerancer for sammenholdelse af fakturatotaler.
-   På siden Sammenholdelsespolitik kan du angive politikker for tovejs- og trevejssammenholdelse.
-   På siden Pristolerancer kan du angive tolerancer for salgspriser.
-   På siden Pristolerancegrupper for vare kan du angive tolerancegrupper for varepriser.
-   På siden Pristolerancegrupper for kreditor kan du angive tolerancegrupper for leverandørpriser.
-   På siden Gebyrtolerancer kan du angive tolerancer for gebyrer.

**Arbejdsgang**

-   På siden Kreditorarbejdsgange kan du angive arbejdsgangekonfigurationer for kladdegodkendelser og indkøbsrekvisitioner.

**Årsager**

-   På siden Kreditorårsager kan du angive årsagskoder.

**Tillæg**

-   På siden Gebyrkode kan du angive koder for de gebyrer, der bruges i indkøbsordrer.
-   På siden Kreditorgebyrgruppe kan du oprette og vedligeholde gebyrgrupper for kreditorer.
-   På siden Varegebyrgrupper kan du oprette og vedligeholde gebyrgrupper for varer.
-   På siden Automatiske gebyrer kan du definere de gebyrer, der automatisk knyttes til ordrer.

**Supplerende varer**

-   På siden Supplerende varegrupper – Kreditor kan du oprette og vedligeholde supplerende varegrupper for kreditorer.
-   På siden Supplerende varegrupper – Lager kan du oprette og vedligeholde supplerende varegrupper for varer.

**Fordeling**

-   På siden Leveringsbetingelser kan du oprette og vedligeholde betingelserne for en vares overførsel fra sælger til køber.
-   På siden Leveringsmåder kan du oprette og vedligeholde de transportmåder, der bruges, når en ordre leveres fra sælger til køber.
-   På siden Destinationskoder kan du oprette og vedligeholde identifikatorer og beskrivelser for leveringsdestinationer.

**Formularer**

-   På siden Formularnoter kan du oprette den standardtekst, der vises på diverse sider.
-   På siden Formsorteringsparametre kan du konfigurere sorteringsrækkefølgen for rekvisitioner, tilgangslister, følgesedler og fakturaer.
-   På siden Opsætning af udskriftsstyring kan du angive udskrifts- og administrationsoplysninger for originaler og kopier af siderne.

**Betalinger**

-   På siden Kasserabat kan du konfigurere og administrere betingelserne for at opnå kasserabatter. Kasserabatkoderne knyttes til kreditorer og anvendes på indkøbsordrer.
-   På siden Betalingsplaner kan du oprette betalingsplaner, der bruges til administration af ratebetalinger til kreditorer.
-   På siden Betalingsdage kan du definere de betalingsdage, der bruges til beregning af forfaldsdatoer, og angive betalingsdage for en bestemt ugedag eller dag i måneden.
-   På siden Betalingsgebyr kan du oprette og vedligeholde gebyrer, der er knyttet til kreditorer.
-   På siden Betalingsinstruktion kan du oprette og vedligeholde betalingsinstruktioner.

**Statistik**

-   På siden Definitioner af forældelsesperioder kan du konfigurere brugerdefinerede intervaller, der bruges til at analysere forfaldsfordelingen af kreditorkonti.
-   På siden Forretningsområde kan du oprette koder for de forretningsområder, der er knyttet til kreditorer.

**1099-skat**

-   På siden **1099-felter** kan du bekræfte og opdatere de minimumbeløb, der skal rapporteres til de interne skattemyndigheder (IRS), baseret på de seneste myndighedskrav.

## <a name="optional-setup-for-other-modules"></a>**Valgfri konfiguration til andre moduler**
**Virksomhedsadministration**

-   På siden Nummerserier kan du konfigurere nummerseriegrupper med fakturanumre.
-   På følgende sider kan du definere adresseoplysninger:
    -   Adresseopsætning
    -   NAF-koder
    -   Import af postnumre

**Økonomi**

-   På siden Økonomiske dimensioner kan du konfigurere de økonomiske dimensioner.
-   På følgende sider kan du konfigurere momsoplysninger:
    -   Momskoder
    -   Momsgrupper
    -   Varemomsgrupper
    -   Kontogruppe
    -   Momsfritagelseskoder
    -   Momsjurisdiktionsområder
    -   Momsmyndigheder
    -   Momsafregningsperioder

**Kontant- og bankstyring**

-   På siden Betalingsformålskoder kan du konfigurere nationalbankens formålskoder.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]