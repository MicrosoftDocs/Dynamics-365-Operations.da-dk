---
title: Forhåndsversion af Dynamics 365 Supply Chain Management 10.0.29 (oktober 2022)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management 10.0.29.
author: kamaybac
ms.date: 08/12/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d95cd9b55f473bed2e3fe69e63837040385f03ac
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334739"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10029-october-2022"></a>Forhåndsversion af Dynamics 365 Supply Chain Management 10.0.29 (oktober 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikel viser funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management forhåndsversion 10.0.29. Denne version har et build-nummer på 10.0.1326 og er tilgængelig i følgende plan:

- **Forhåndsversion:** august 2022
- **Generel tilgængelighed af version (selv-opdatering):** september 2022
- **Generel tilgængelighed af version (automatisk opdatering):** oktober 2022

## <a name="features-included-in-this-release"></a>Funktioner, der er inkluderet i denne version

Følgende tabel anfører de funktioner, der er inkluderet i denne version. Vi opdaterer muligvis denne artikel for at medtage funktioner i det build, som er foretaget, efter denne artikel blev udgivet.

| Funktionsområde | Funktion | Flere oplysninger | Aktiveret af   |
|---|---|---|---|
| Lager og logistik | [Fordele og reservere WMS-varer i Lagersynlighed](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/allocate-reserve-whs-items-inventory-visibility) | Kommer snart | Aktiveret som standard |
| Lager og logistik | [Forudindlæse strømlinede lagerbeholdningslister](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/query-inventory-visibility-summary-entity) | Kommer snart | Aktiveret som standard |
| Automatisering af forsyning af levering til ordre | [Automatisering af forsyning af levering til ordre](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-to-order-supply-automation) | [Automatisering af forsyning af levering til ordre](../master-planning/make-to-order-supply-automation.md) | Funktionsstyring:<br>*Automatisering af forsyning af levering til ordre* |
| Planlægning | [Se og anvende detaljeret indsigt for DDMRP](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/view-apply-detailed-insights-ddmrp) | [Oversigt over planlægning af efterspørgselsbaseret materialebehov](../master-planning/planning-optimization/ddmrp-overview.md) | Funktionsstyring:<br>*(Forhåndsversion) DDMRP til planlægningsoptimering* |
| Produktionsstyring | [Gøre færdigvarer fysisk tilgængelige før bogføring i kladder](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-finished-goods-physically-before-posting) | [Gøre færdigvarer fysisk tilgængelige før bogføring i kladder](../production-control/deferred-posting.md) | Funktionsstyring:<br>*(Forhåndsversion) Gør færdigvarer fysisk tilgængelige før bogføring i kladder* |
| Warehouse management | [Søge efter relevante data i Warehouse Mobile App](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/look-up-relevant-data-within-warehouse-mobile-app) | [Forespørge på data ved brug af omveje i Warehouse Management-mobilappen](../warehousing/warehouse-app-data-inquiry.md) | Funktionsstyring:<br>*Dataforespørgselsflow til app til Warehouse management* |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsforbedringer, der er inkluderet i denne version

Følgende tabel indeholder de funktionsforbedringer, der er inkluderet i denne version. Hver af disse udvidelser giver en trinvis forbedring af en eksisterende funktion. Da det kun er forbedringer, er de ikke angivet i [udgivelsesplanen](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Men for at sikre, at disse forbedringer ikke er i konflikt med dine eksisterende tilpasninger eller præferencer, er hver af dem som standard deaktiveret (medmindre andet er angivet).

Hvis du vil slå en af disse funktioner til eller fra, skal du gøre det i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funktionsnavn i funktionsstyring | Flere oplysninger |
|---|---|---|
| Omkostningsstyring | Optimering af samprodukt afventer prisberegning | Denne funktion løser en konflikt, som nogle gange kan forekomme, når samproduktpriser beregnes ved hjælp af flere tråde. Det bevirker, at systemet sikrer, at hver samproduktpris beregnes kun én gang. Resultatet af denne beregning bruges derefter som input til alle andre beregninger. Hvis der allerede findes en ventende pris, bruges den pågældende pris. |
| Varedisponering | Gruppér transaktioner i Planlægningsoptimering | Denne funktion kan hjælpe dig med at reducere antallet af ordreforslag, der genereres for at levere en enkelt salgsordrelinje, når du bruger Planlægningsoptimering. Når denne funktion er aktiveret, grupperer Planlægningsoptimering alle lagertransaktioner for en ordrelinje i ét enkelt krav for det fulde antal. (Denne funktionsmåde svarer til den indbyggede funktionsmåde for planlægningsprogrammet). Udbud og efterspørgsel grupperes separat. Funktionen hjælper derfor med at reducere omfanget af transaktioner, når du har opdelt transaktioner, og når du bruger dimensioner (som f.eks. batchnumre eller serienumre), der ikke er disponeringsdimensioner. |
| Indkøb og forsyning | Sæt kreditor på hold for indkøbsordrer | Du kan bruge denne funktion til at sætte en leverandør på hold i forbindelse med indkøbsordrer. Den tilføjer en ny type *Indkøbsordre* på hold, der markerer en leverandør som på hold for indkøbsordrer. Du kan ikke oprette nye indkøbsordrer for leverandører, der er på hold for indkøbsordrer, men du kan stadig fortsætte med åbne fakturaer eller betalinger for disse leverandører. |
| Salg og marketing | Beregn linjenettobeløb ved import | Denne funktion giver dig mulighed for at styre, om systemet skal genberegne linjetotaler, når du importerer data via enheden *Salgsordrelinjer*, *Salgstilbudslinjer* eller *Returordrelinjer* ved hjælp af OData eller dobbeltskrivning. Den virker kun, når der også er politikker for evaluering af samhandelsaftale, som begrænser ændringerne til feltet **Nettobeløb** for salgsordrelinjer, salgstilbudslinjer og/eller returordrelinjer. Der føjes en indstilling kaldet **Beregn linjenettobeløb** til siden **Debitor > Opsætning > Debitorparametre**. Når denne indstilling er angivet til *Ja*, genberegner systemet altid linjebeløb efter behov (uden hensyn til en politik for samhandelsaftaleevaluering af linjenettobeløbet). Når indstillingen er angivet til *Nej*, beregner systemet aldrig automatisk nettobeløbet for linjen, selvom indgående ændringer i linjeprisen, antallet og/eller rabatten kunne antyde, at linjens nettobeløb skulle genberegnes. Denne funktion aktiveres som standard og angiver først **Beregn linjenettobeløb** til *Ja*. Indstillingen *Nej* stemmer overens med systemfunktionsmåden før version 10.0.23 og er hovedsageligt med for at understøtte ældre integrationsscenarier.<br><br>Yderligere oplysninger finder du i [Genberegne nettobeløb for linjer ved import af salgsordrer, tilbud og returneringer](../sales-marketing/calc-line-net-amounts-import.md). |
| Salg og marketing | Beregn salgstotaler ved hjælp af flere tråde | Denne funktion hjælper med at forbedre ydeevnen ved at gøre systemet i stand til at bruge parallel behandling, når der beregnes salgstotaler i en batch. Funktionen føjer et nyt felt med **Antal tråde** til dialogboksen **Beregn salgstotaler**. Hvis du vælger at køre beregningen i en batch, kan du bruge dette felt til at angive det maksimale antal tråde. Hvis du angiver værdien til *0* (nul) eller *1*, bruges en enkelt tråd. Værdier over 1 aktiverer multitråd. |
| Salg og marketing | Opdater priser og rabatter, der er angivet manuelt til intern brug | Denne funktion tilføjer understøttelse af manuelle ændringspolitikker i interne ordrer. Det omfatter understøttelse af overførsel af manuelle ændringspolitikker mellem interne salgs- og indkøbsordrer. Tidligere understøttedes manuelle ændringspolitikker kun for ordrer, der ikke er interne. Når denne funktion er aktiveret, giver systemet dig mulighed for at opdatere priser og rabatter, når du har gemt ændringerne i en intern ordre. Du kan bruge denne indstilling til at vælge, om du vil anvende de nye priser og rabatoplysninger på den interne ordre eller lade ordren være uændret. |

## <a name="new-and-updated-documentation-resources"></a>Nye og opdaterede dokumentationsressourcer

Vi har for nylig tilføjet eller væsentligt opdateret følgende Hjælp-artikler. Disse artikler er ikke nødvendigvis knyttet til de nye funktioner, der er tilføjet for denne version, som vist i forrige afsnit. De kan dog hjælpe dig med at få mere ud af eksisterende funktioner.

| Funktionsområde | Nye eller opdaterede artikler |
|---|---|
| Varedisponering, LE | [Beregne leveringsdatoer for salgsordrer ved hjælp af LE](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) |
| Varedisponering, DDMRP | [Oversigt over planlægning af efterspørgselsbaseret materialebehov](../master-planning/planning-optimization/ddmrp-overview.md)<br>[Aktivere DDMRP-funktionen for systemet](../master-planning/planning-optimization/ddmrp-enable.md)<br>[Lagerpositionering](../master-planning/planning-optimization/ddmrp-inventory-positioning.md)<br>[Bufferprofil og -niveauer](../master-planning/planning-optimization/ddmrp-buffer-profile-and-levels.md)<br>[Efterspørgselsbaseret planlægning](../master-planning/planning-optimization/ddmrp-planning.md)<br>[Udførelse af visuel grafik og samarbejde](../master-planning/planning-optimization/ddmrp-visual-and-collaborative-execution.md) |
| Warehouse management | [Pakke containere til forsendelse](../warehousing/packing-containers.md)<br>[Pakkearbejde til pakning af udgående containere og behandling af forsendelser](../warehousing/packing-work.md) |

## <a name="feature-state-changes-in-this-release"></a>Ændringer af funktionstilstand i denne version

I følgende tabel vises de funktioner, der blev obligatoriske eller som standard var slået til i version 10.0.29. Alle disse funktioner vil automatisk være aktiveret for systemet, så snart du opdaterer til version 10.0.29. Obligatoriske funktioner kan ikke deaktiveres, men funktioner, der er aktiveret som standard, kan stadig deaktiveres ved hjælp af [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tabellen indeholder også funktioner, der tidligere var med i offentlig forhåndsversion, men som er blevet generelt tilgængelige i version 10.0.29. Denne ændring angiver, at funktionerne nu anbefales til brug i produktionsmiljøer. Disse funktioner er som standard deaktiverede, hvis intet andet er angivet. Hvis du vil bruge en af disse funktioner, skal du bruge [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere dem.

| Modul | Funktionsnavn | Ny funktionstilstand |
| --- | --- | --- |
| Aktivstyring | [Funktion til aktivstyring af grænsefladen til produktionsudførelse](../production-control/production-floor-execution-configure.md) | Obligatorisk |
| Omkostningsstyring | [Skift label til annullering ved lukning og regulering til tilbageførsel](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/change-terminology-inventory-closing-cancellation-inventory-closing-reverse) | Obligatorisk |
| Omkostningsstyring | Rydde op i oplysninger om styklisteberegning i krydsefterkalkulationsversioner | Obligatorisk |
| Omkostningsstyring | [Sammenlign varepriser - lager](../cost-management/compare-item-price.md) | Obligatorisk |
| Omkostningsstyring | [Omkostningsberegningsniveau](../cost-management/cost-calculation-level.md) | Til som standard |
| Omkostningsstyring | Aktivér brugerdefineret batchnummeropsætning for tilbageførsel af lagerlukning | Til som standard |
| Omkostningsstyring | [Statusdetaljer om lagerlukning](whats-new-scm-10-0-21.md) | Til som standard |
| Omkostningsstyring | [Lagerværdirapportlager](../cost-management/inventory-value-report-storage.md) | Obligatorisk |
| Omkostningsstyring | Rapporten Lagerværdi – oprydning i data | Obligatorisk |
| Omkostningsstyring | Reserveomkostningssekvens med glidende gennemsnit | Obligatorisk |
| Omkostningsstyring | Vis lagerlukningslog i gitter | Obligatorisk |
| Omkostningsstyring | Vis de varer, der ikke er fuldt udlignet med posteringer i oversigtsformat | Obligatorisk |
| Lager- og Warehouse management | Tillad tomme batchattributværdier | Obligatorisk |
| Lager- og Warehouse management | Automatisk forøgelse af linjenumre til flytteordrelinjer for lager | Obligatorisk |
| Lager- og Warehouse management | Opret flytteordre fra salgslinje. | Obligatorisk |
| Lager- og Warehouse management | Deaktivere feltet Lagerkladdelinje i arbejdsproces | Obligatorisk |
| Lager- og Warehouse management | Aktivér advarselsfunktion for parametre for styring af lagerkvalitet | Obligatorisk |
| Lager- og Warehouse management | (Kina) Udeluk fysiske tilgangs- og afgangsomkostninger fra månedlige gennemsnitlige omkostninger | Til som standard |
| Lager- og Warehouse management | [Arbejdsgang for godkendelse af lagerkladde](../inventory/inventory-journal-workflow.md) | Obligatorisk |
| Lager- og Warehouse management | [Lagring af rapporten Disponibelt lager](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/inventory-on-hand-report-storage) | Obligatorisk |
| Lager- og Warehouse management | [Gemte visninger til lagerstyring](saved-views-scm.md) | Obligatorisk |
| Lager- og Warehouse management | Annullering af flytteordre | Obligatorisk |
| Lager- og Warehouse management | Brug af måleenhed og enhedsantal i lagerkladder | Obligatorisk |
| Lager- og Warehouse management | Låse lagerkladde op | Obligatorisk |
| Fremstillingsvirksomhed | [Automatisk pluk af materialer, der er aktiveret til lagersted, til automatisk bogførte pluklister](whats-new-scm-10-0-23.md) | Generelt tilgængelig |
| Fremstillingsvirksomhed | Aktivér visning af lagerdimensioner på materialelisten for produktionsruteoperationer | Obligatorisk |
| Fremstillingsvirksomhed | [Aktivere for at angive batch- og serienumre, når der færdigmeldes fra jobkortenheden](../production-control/report-finished-job-device.md) | Til som standard |
| Fremstillingsvirksomhed | Forbedret pluk af fastvægtantal til produktion | Til som standard |
| Fremstillingsvirksomhed | [Jobsøgning til grænsefladen til produktionen](../production-control/production-floor-execution-configure.md) | Obligatorisk |
| Fremstillingsvirksomhed | [Integration af produktionsudførelsessystem](../production-control/mes-integration.md) | Til som standard |
| Fremstillingsvirksomhed | [Visningen "Min dag" til grænsefladen til produktionsudførelse](../production-control/production-floor-execution-configure.md) | Til som standard |
| Fremstillingsvirksomhed | [Kontrol af materialers tilgængelighed efter behov for produktionsordrer](whats-new-scm-10-0-24.md) | Til som standard |
| Fremstillingsvirksomhed | [Tilsidesæt standardproduktionsreservation](../production-control/override-default-reservation-principle.md) | Obligatorisk |
| Fremstillingsvirksomhed | [Registrer materialeforbrug i grænsefladen for produktionsudførelse (ikke-WMS)](../production-control/production-floor-execution-configure.md) | Generelt tilgængelig |
| Fremstillingsvirksomhed | [Rapport over fastvægtvarer fra grænsefladen for udførelse af produktionsgulv](../production-control/production-floor-execution-configure.md) | Generelt tilgængelig |
| Fremstillingsvirksomhed | [Rapport over samprodukter og biprodukter fra grænsefladen for udførelse af produktion](../production-control/production-floor-execution-configure.md) | Til som standard |
| Fremstillingsvirksomhed | [Rapport over planlægningselementer i grænsefladen til produktionsudførelse](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | Til som standard |
| Fremstillingsvirksomhed | [Gemte visninger for produktionsstyring](saved-views-scm.md) | Obligatorisk |
| Fremstillingsvirksomhed | [Vis fulde serie-, batch- og id-numre i grænsefladen til produktionsudførelse](../production-control/production-floor-execution-configure.md) | Obligatorisk |
| Fremstillingsvirksomhed | [Valider udløb af råmaterialer i forhold til planlagt forbrugsdato](whats-new-scm-10-0-23.md) | Til som standard |
| Varedisponering | [Automatisk autorisation til planlægningsoptimering](../master-planning/planning-optimization/planned-order-firming.md) | Obligatorisk |
| Varedisponering | [Godkendelse og konsolidering, der kan køre i batch, for planlagte bulk- og pakkebatchordrer](whats-new-scm-10-0-20.md) | Til som standard |
| Varedisponering | [Medtag varer med beholdning, når forbehandlingsfiltre er aktiveret](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/master-planning-include-items-on-hand-when-pre-processing-filters-are-enabled) | Til som standard |
| Varedisponering | [Uendelig kapacitetsplanlægning til planlægningsoptimering](../master-planning/planning-optimization/infinite-capacity-planning.md) | Til som standard |
| Varedisponering | [Margener for Planlægningsoptimering](../master-planning/planning-optimization/safety-margins.md) | Obligatorisk |
| Varedisponering | [Negative dage til planlægningsoptimering](../master-planning/planning-optimization/delay-tolerance.md) | Obligatorisk |
| Varedisponering | [Parallel godkendelse til justeret behovsprognose](whats-new-scm-10-0-20.md) | Obligatorisk |
| Varedisponering | [Autorisation af ordreforslag med filtrering](../master-planning/planning-optimization/planned-order-firming.md) | Obligatorisk |
| Varedisponering | [Produktionsordreforslag for planlægning af optimering](../master-planning/planning-optimization/production-planning.md) | Obligatorisk |
| Varedisponering | [Samhandelsaftaler for indkøb til planlægningsoptimering](../master-planning/planning-optimization/purchase-trade-agreement.md) | Obligatorisk |
| Varedisponering | [Gemte visninger for ordreforslag](saved-views-scm.md) | Obligatorisk |
| Indkøb og forsyning | Gebyrer fra og til beløb på indkøbsordrer | Obligatorisk |
| Indkøb og forsyning | Deaktivere knappen Nulstil for distribution af indkøbsrekvisition | Til som standard |
| Indkøb og forsyning | [Aktivér nulstilling af indkøbsrelaterede arbejdsgange](whats-new-scm-10-0-20.md) | Til som standard |
| Indkøb og forsyning | [Begræns antallet af indkøbsordrelinjer pr. batchopgave](whats-new-scm-10-0-27.md) | Til som standard |
| Indkøb og forsyning | [Flet økonomiske dimensioner fra kreditoren med det aktive dimensionslink til økonomisk dimension på indkøbsordren](whats-new-scm-10-0-25.md) | Obligatorisk |
| Indkøb og forsyning | [Bogfør registrerede antal lagerbaserede produkter og rester af ikke-lagerbaserede produkter for modtagelser og kreditorfakturaer](whats-new-scm-10-0-26.md) | Generelt tilgængelig |
| Indkøb og forsyning | [Undgå overforbrug af generelle budgetreservationer, når der er flere indkøbsrekvisitioner i arbejdsgang](whats-new-scm-10-0-21.md) | Til som standard |
| Indkøb og forsyning | [Ansvarlig part for købsaftale](../procurement/purchase-agreements.md) | Obligatorisk |
| Indkøb og forsyning | [Gemte visninger af indkøbsordrer](saved-views-scm.md) | Obligatorisk |
| Administration af produktoplysninger | Forbehandling af styklisterapporten for at undgå timeout | Obligatorisk |
| Administration af produktoplysninger | Økonomiske standarddimensioner separat ved brug af vareskabeloner | Obligatorisk |
| Administration af produktoplysninger | Aktivér produktdimensionsgrupper for vareskabeloner | Obligatorisk |
| Administration af produktoplysninger | Forbedringer af vare-stregkodeobjekt | Obligatorisk |
| Administration af produktoplysninger | Regenerer produktvariantnavne baseret på nomenklatur | Obligatorisk |
| Administration af produktoplysninger | [Gemte visninger af frigivne produkter](saved-views-scm.md) | Obligatorisk |
| Administration af produktoplysninger | [Forbedringer af siden Variantforslag](../pim/tasks/create-predefined-product-variants.md) | Obligatorisk |
| Salg og marketing | [Gebyrfordeling på en salgsordre](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/miscellaneous-charges-enhancements) | Obligatorisk |
| Salg og marketing | Ryd op i historik for salgsordreopdatering | Obligatorisk |
| Salg og marketing | [Ryd op i historik for salgsopdatering baseret på alder](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) | Obligatorisk |
| Salg og marketing | [Eksportoptimering af kontaktpersondataenheden](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Obligatorisk |
| Salg og marketing | Kopiér samlet rabatgruppe for salgskreditnota | Obligatorisk |
| Salg og marketing | [Aktiver opslag for introduktion til salgstilbudsdokument og dokumentkonteringsfelter](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Obligatorisk |
| Salg og marketing | [Forbedr ydeevne for rapport med "Top 100" kunder](whats-new-scm-10-0-23.md) | Obligatorisk |
| Salg og marketing | Medtag ventende poster i opgaver til oprydning i historik | Obligatorisk |
| Salg og marketing | Begræns antallet af salgsordrelinjer pr. batchopgave | Til som standard |
| Salg og marketing | [Begræns antallet af salgsordrer, der kan vælges til bogføring](whats-new-scm-10-0-21.md) | Obligatorisk |
| Salg og marketing | Genberegn forkalkuleret debitorsaldo | Obligatorisk |
| Salg og marketing | [Registrering af salgsreturordrelinje med decimalpræcision med og uden fastvægt](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Obligatorisk |
| Salg og marketing | [Gemte visninger for salg og marketing](saved-views-scm.md) | Obligatorisk |
| Salg og marketing | [Salgsordrebekræftelse med et enkelt klik](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/single-click-sales-order-confirmation) | Obligatorisk |
| Transportstyring | Tillad fjernelse af tilknytning mellem fragtfakturaer og fragtfakturalinjer i fraværet af en bogført kreditorfakturakladde | Til som standard |
| Transportstyring | [Aktivér oprettelse af en kreditorfakturakladde, når en fragtregning kasseres](whats-new-scm-10-0-20.md) | Til som standard |
| Transportstyring | [Forsendelse af lille pakke](../warehousing/small-parcel-shipping.md) | Obligatorisk |
| Transportstyring | [USMCA-certificering af oprindelsesdokument](../transportation/usmca-certification-of-origin.md) | Til som standard |
| Warehouse management | [Flere lokationszoner](../warehousing/additional-location-zones.md) | Obligatorisk |
| Warehouse management | [Annuller arbejde](../warehousing/cancel-warehouse-work.md) | Obligatorisk |
| Warehouse management | [Konsolider forsendelse](../warehousing/configure-shipment-consolidation-policies.md) | Obligatorisk |
| Warehouse management | [Opret, og behandl overførselsordrer fra lagersteds-appen](../warehousing/create-transfer-order-from-warehouse-app.md) | Obligatorisk |
| Warehouse management | Skabeloner til cross-docking med lokationsvejledninger | Til som standard |
| Warehouse management | [Afkobl læg på lager-arbejde fra ASN'er](whats-new-scm-10-0-21.md) | Obligatorisk |
| Warehouse management | [Udskudte læg på lager-handlinger](../warehousing/deferred-processing-manual-inventory-movement.md) | Obligatorisk |
| Warehouse management | Udskudt læg-på-lager – container | Til som standard |
| Warehouse management | Udskudt læg-på-lager behandling – aktivér for overvågningsskabelonfunktion med udløserhændelse angivet til Tidligere | Obligatorisk |
| Warehouse management | [Deaktiver forventede tilgange fra kvalitetsordrer, der vælger spærret lager](../inventory/inventory-blocking.md) | Til som standard |
| Warehouse management | Aktivér hurtig validering for mobilenheder til lagersted | Obligatorisk |
| Warehouse management | [Udvidet parser til GS1-stregkoder](../warehousing/gs1-barcodes.md) | Generelt tilgængelig |
| Warehouse management | [Fleksibel ordrebekræftet id-reservation](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Obligatorisk |
| Warehouse management | [Fleksibel reservation af dimension på lagerstedsniveau](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Obligatorisk |
| Warehouse management | [Udnyttelse af varekonsolideringslokation](../warehousing/item-consolidation-location-utilization.md) | Til som standard |
| Warehouse management | Historik for modtagelse af nummerplade | Til som standard |
| Warehouse management | [Manuel forsendelseskonsolidering](../warehousing/consolidate-shipments-manual-workbench.md) | Til som standard |
| Warehouse management | [Manuel udvalgstjeneste for overførselslinjer for administratorer eller lignende betroede brugere](whats-new-scm-10-0-28.md) | Generelt tilgængelig |
| Warehouse management | [Grænseflade for materialehåndteringsudstyr](../warehousing/mhax.md) | Obligatorisk |
| Warehouse management | [Nye sider med lastplanlægningspanel](whats-new-scm-10-0-24.md) | Generelt tilgængelig |
| Warehouse management | [Visualisering af udgående arbejdsbyrde](../warehousing/outbound-workload-visualization.md) | Obligatorisk |
| Warehouse management | [Planlagt direkte levering](../warehousing/planned-cross-docking.md) | Obligatorisk |
| Warehouse management | [Proces for hændelser for lagerapp](../warehousing/warehouse-app-events.md) | Obligatorisk |
| Warehouse management | Forbedring af forespørgsel om læg på lager-arbejdsskabelonen for samprodukt og biprodukt | Obligatorisk |
| Warehouse management | [Afrund antal ned til nærmeste salgsenhed ved frigivelse til lagersted](whats-new-scm-10-0-19.md) | Obligatorisk |
| Warehouse management | [Gemt visning for lastplanlægningspanelet](saved-views-scm.md) | Obligatorisk |
| Warehouse management | [Gemt visning af siden med arbejdsdetaljer](saved-views-scm.md) | Obligatorisk |
| Warehouse management | [Gemt visning til bølgebehandling](saved-views-scm.md) | Obligatorisk |
| Warehouse management | [Gemte visninger til lastbehandling](saved-views-scm.md) | Obligatorisk |
| Warehouse management | [Gemte visninger til forsendelsesbehandling](saved-views-scm.md) | Obligatorisk |
| Warehouse management | [Scan GS1-stregkoder](../warehousing/gs1-barcodes.md) | Generelt tilgængelig |
| Warehouse management | Etiketdetaljer om forsendelsesbølge | Obligatorisk |
| Warehouse management | [Enheder blandet på slot](whats-new-scm-10-0-21.md) | Obligatorisk |
| Warehouse management | [Brug hurtigere API til containere, der lukker/genåbner på pakkestation](whats-new-scm-10-0-21.md) | Til som standard |
| Warehouse management | [Valider skabeloner, der er valgt til genopfyldningsjob](whats-new-scm-10-0-20.md) | Til som standard |
| Warehouse management | [Hævede felter i lagerstedsapp](../warehousing/warehouse-app-promoted-fields.md) | Obligatorisk |
| Warehouse management | [Vejledninger til trin i lagerstedsapp](../warehousing/mobile-app-titles-instructions.md) | Obligatorisk |
| Warehouse management | [Placeringsstatus for lagersted](../warehousing/warehouse-location-status.md) | Obligatorisk |
| Warehouse management | [Omveje i Warehouse Management-app](../warehousing/warehouse-app-detours.md) | Til som standard |
| Warehouse management | [Oplysninger om bølgebatchjob](../warehousing/wave-processing.md) | Obligatorisk |
| Warehouse management | [Beskeder om udførelse af bølge](../warehousing/wave-execution-notifications.md) | Obligatorisk |

## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformsopdateringer til Finans- og driftsapps

Microsoft Dynamics 365 Supply Chain Management 10.0.29 indeholder platformopdateringer. Du kan få mere at vide i [Platformsopdateringer til version 10.0.29 af programmer til finans og drift (juni 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md). <!--KFM: Confirm link -->

### <a name="bug-fixes"></a>Fejlrettelser

Du kan finde flere oplysninger om de fejlrettelser, der er inkluderet i hver af de opdateringer, som er del af version 10.0.29, ved at logge på Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 og brancheskyer: 2022 frigivelsesplan bølge 1

Vil du gerne vide mere om kommende og de senest frigivne funktioner i en af vores forretningsapps eller platforme?

Undersøg [Dynamics 365 og brancheskyer: 2022 frigivelsesplan bølge 2](/dynamics365-release-plan/2022wave2/). Vi har samlet alle oplysninger fra start til slut og top til bund i et enkelt dokument, som du kan bruge til planlægning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og udfasede Supply Chain Management-funktioner

Artiklen [Fjernede eller udfasede funktioner Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver de funktioner, der er planlagt eller skal fjernes eller udfases for Supply Chain Management.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Før en funktion fjernes fra produktet, vil du få besked om udfasning i artiklen [Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder, inden de fjernes.

For ændringer, der kun påvirker kompileringstiden, men som er binære, som er kompatible med sandkasse- og produktionsmiljøer, vil tidsrummet for udfasningen være mindre end 12 måneder. Det er typisk funktionelle opdateringer, der skal foretages i compileren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
