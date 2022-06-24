---
title: Nyheder eller ændringer i Dynamics 365 Supply Chain Management 10.0.25 (april 2022)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management 10.0.25.
author: kamaybac
ms.date: 03/14/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 1fa2ec6e21026552a4f14a67188db0720d3feae5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850780"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10025-april-2022"></a>Nyheder eller ændringer i Dynamics 365 Supply Chain Management 10.0.25 (april 2022)

[!include [banner](../includes/banner.md)]

Denne artikel viser funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management version 10.0.25. Denne version har et build-nummer på 10.0.1149 og er tilgængelig som følger:

- **Forhåndsversion:** Februar 2022
- **Generel tilgængelighed af version (selvopdatering):** Marts 2022
- **Generel tilgængelighed af version (automatisk opdatering):** April 2022

## <a name="features-included-in-this-release"></a>Funktioner, der er inkluderet i denne version

Følgende tabel anfører de funktioner, der er inkluderet i denne version. Vi opdaterer muligvis denne artikel for at medtage funktioner i det build, som er foretaget, efter denne artikel blev udgivet.

| Funktionsområde | Funktion | Flere oplysninger | Aktiveret af   |
|---|---|---|---|
| Lager&nbsp;og&nbsp;logistik | [Forbedringer for farlige materialer](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/hazardous-materials-enhancements) | Kommer snart | Funktionsstyring:<br>*Forbedringer for farlige materialer* |
| Lager&nbsp;og&nbsp;logistik | [Pakkearbejde for pakkestationer](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/packing-work-packing-stations) | Kommer snart | Funktionsstyring:<br>*Pakkearbejde for pakkestationer* |
| Lager&nbsp;og&nbsp;logistik | [Scanne stregkoder på lagerstedet ved hjælp af GS1-formatstandarder](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1-stregkoder og QR-koder](../warehousing/gs1-barcodes.md) | Funktionsstyring:<br>*Scan GS1-stregkoder* |
| Fremstillingsvirksomhed | [Materialeforbrug og reservationer i grænsefladen for produktionsudførelse](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/material-consumption-reservations-production-floor-execution-interface) | [Sådan anvender arbejdere grænsefladen til kørsel af produktion](../production-control/production-floor-execution-use.md) | Funktionsstyring:<br>*(Forhåndsversion) Registrer materialeforbrug i grænsefladen for produktionsudførelse (ikke-WMS)*<br><br>Og/eller:<br><br>Funktionsstyring:<br>*(Forhåndsversion) Registrer materialeforbrug i grænsefladen for produktionsudførelse (WMS-aktiveret)* |
| Fremstillingsvirksomhed | [Registrere materialeforbrug på skalaenheder](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/register-material-consumption-scale-units) | [Produktionsarbejdsbyrder for sky- og kantskaleringsenheder](../cloud-edge/cloud-edge-workload-manufacturing.md) | Funktionsstyring:<br>*Registrer materialeforbrug på mobilappen på en skalaenhed* |
| Planlægning | [Vedligeholdelse af centraliseret kalender for planlægningsoptimering](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-centralized-calendar-maintenance) | [Kalendere og varedisponering](../master-planning/supply-chain-calendars-master-planning.md) | Aktiveret som standard |
| Planlægning | [Forslag til planlægningsoptimering for at optimere eksisterende forsyning](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-suggestions-optimize-existing-supply) | [Handlingsmeddelelser](../master-planning/action-messages.md) | Aktiveret som standard |
| Planlægning | Planlagte ordrer forenklet | [Planlagte ordrer forenklet](../master-planning/planning-optimization/planned-orders-simplified.md ) | Funktionsstyring:<br>*Planlagte ordrer forenklet* |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsforbedringer, der er inkluderet i denne version

Følgende tabel indeholder de funktionsforbedringer, der er inkluderet i denne version. Hver af disse udvidelser giver en trinvis forbedring af en eksisterende funktion. Da det kun er forbedringer, er de ikke angivet i [udgivelsesplanen](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Men for at sikre, at disse forbedringer ikke er i konflikt med dine eksisterende tilpasninger eller præferencer, er hver af dem som standard deaktiveret (medmindre andet er angivet).

Hvis du vil slå en af disse funktioner til eller fra, skal du gøre det i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funktionsnavn i funktionsstyring | Flere oplysninger |
|---|---|---|
| Lager- og lokationsstyring | (Polen) Tillad tilknytning af flere SAD-fakturaer til én indkøbsordrelinje i én SAD | Du kan bruge denne funktion til at opdele indkøbsordrelinjer og knytte dem til et enkelt administrativt dokument (SAD), når disse indkøbsordrelinjer er bogført for flere forskellige fakturaer (f.eks. for forskellige forsendelser). |
| Indkøb og forsyning | Konsolider flere indkøbsrekvisitioner til en enkelt indkøbsordre efter regnskabsdato | Med denne funktion kan flere indkøbsrekvisitioner konsolideres til en enkelt indkøbsordre, hvis de forskellige indkøbsrekvisitioner har forskellige regnskabsdatoer. Regler indkøbspolitik ved oprettelse af indkøbsordrer og efterspørgselskonsolidering kan konfigureres til at automatisere beslutningen om at gruppere rekvisitionslinjer efter regnskabsdato på indkøbsordreniveau. Konsolidering af indkøbsordrer efter regnskabsdato understøttes ikke, hvis budgetstyring er aktiveret, fordi regnskabsdatoen bruges til budgetreservationer og behæftelser. Derfor skal den beholdes under overgangen fra indkøbsrekvisition til indkøbsordre. |
| Indkøb og forsyning | Vis feltindstillinger for svar på ældre tilbudsanmodning | Denne funktion genindfører de tidligere feltindstillinger for svar på standardtilbudsanmodninger, som tidligere blev fjernet fra brugergrænsefladen. Disse indstillinger indeholder ingen funktionalitet som udgangspunkt, men de kan tilpasses, så de kan bruges efter behov. Aktivér denne funktion, hvis din organisation allerede har tilføjet funktioner til standardindstillingerne for feltet til svar på tilbudsanmodninger eller planlægger det. Når denne funktion er aktiveret, kan du få adgang til indstillingerne ved at gå til siden **Indkøbs- og forsyningsparametre**, åbne fanen **Tilbudsanmodning** og vælge **Felter til standardsvar på tilbudsanmodning**. |
| Indkøb og forsyning | Flet økonomiske dimensioner fra kreditoren med det aktive dimensionslink til økonomisk dimension på indkøbsordren | Denne funktion giver mulighed for at flette økonomiske dimensioner fra leverandører med det aktive dimensionslink til økonomisk dimension efter godkendelse af indkøbsrekvisitionen, hvis du konfigurerer et link mellem en økonomisk dimension og lagerdimensionen for lokationen. Regler for indkøbspolitik ved oprettelse af indkøbsordrer og efterspørgselskonsolidering kan konfigureres til at drive beslutningen om fletning af økonomiske dimensioner fra kreditorer med et aktivt dimensionslink til økonomisk dimension på indkøbsordrehovedniveau. |
| Produktionsstyring | (Rusland) Aktivér standardlokationskonfiguration for produktionsformel/stykliste og automatisk GTD-reservation/forbrug i produktion | Denne funktion giver mulighed for yderligere indstillinger for produktion fra importerede råmaterialer (kun russisk lokalisering):<ul><li>Mulighed for at angive den automatiske standardlokation for produktionsformler og styklister på både ressourcegrupper og lagersteder.</li><li>Automatisk reservation af råmaterialer med dimensionen *GTD-nummer*, der er aktiveret af WMS i henhold til algoritmen for reservation, der ikke er WMS. Dette gælder i tilfælde, hvor der findes en arbejdspolitik for *Råmaterialepluk* med **Metode til oprettelse af arbejde** angivet til *Aldrig*, og opsætningen af lagersted, lokation og varenummer svarer til lagerposteringerne for produktionsordren (batch).</li><li>Automatisk forbrug af råvarer efter *GTD-nummer*-dimension ved bogføring af pluklisten i overensstemmelse med den anskaffede reservation, der er beskrevet tidligere.</li></ul> |
| Lagerstedsstyring | (Forhåndsversion) Understøttelse af skalaenhed til indgående og udgående lagerstedsordrer | Denne funktion bevirker, at systemet opretter udgående lagerstedsordrer under processen for frigivelse til lagersted og opretter indgående lagerstedsordrer, når flytteordrer bogføres som afsendt. Systemet synkroniserer derefter hver indgående eller udgående lagerstedsordre efter den skalaenhed, der er ansvarlig for afsendelse eller modtagelse af ordren. Bemærk, at når du har aktiveret denne funktion, skal arbejdsbyrderne for udførelse af lagersteder opgraderes. Du kan finde flere oplysninger under [Arbejdsbelastninger i forbindelse med lokationsstyring for sky- og edge-skaleringsenheder](../cloud-edge/cloud-edge-workload-warehousing.md).<br><br>Denne funktion kræver funktionen *Afkobl læg på lager-arbejde fra ASN'er* og vil gøre det muligt at modtage flytteordrer ved hjælp af processen til modtagelse af nummerplader i mobilappen Warehouse Management. |

## <a name="feature-state-changes-in-this-release"></a>Ændringer af funktionstilstand i denne version

I følgende tabel vises de funktioner, der blev obligatoriske eller som standard var slået til i 10.0.25. Alle disse funktioner vil automatisk være aktiveret for systemet, så snart du opdaterer til 10.0.25. Obligatoriske funktioner kan ikke deaktiveres, men funktioner, der er aktiveret som standard, kan stadig deaktiveres ved hjælp af [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tabellen indeholder også funktioner, der tidligere var med i offentlig forhåndsversion, men som er blevet generelt tilgængelige i 10.0.25, hvilket betyder, at de nu anbefales til brug i produktionsmiljøer. Disse funktioner er som standard deaktiveret, medmindre andet er angivet, så du skal bruge [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere dem, hvis du vil bruge dem.

| Modul | Funktionsnavn | Funktionstilstand |
| --- | --- | --- |
| Aktivstyring | [Anvend regler for gruppering af arbejdsordrer, mens en vedligeholdelsesplan køres](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md) | Generelt tilgængelig |
| Aktivstyring | [Tællerbaserede forbedringer af vedligeholdelse](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md) | Generelt tilgængelig |
| Omkostningsstyring | [Omkostningsberegningsniveau](../cost-management/cost-calculation-level.md) | Generelt tilgængelig |
| Omkostningsstyring | Aktivér brugerdefineret batchnummeropsætning for tilbageførsel af lagerlukning | Generelt tilgængelig |
| Omkostningsstyring | [Statusdetaljer om lagerlukning](whats-new-scm-10-0-21.md) | Generelt tilgængelig |
| Omkostningsstyring | [Indstillinger for standardværdier til økonomiske dimensioner for værdiregulering af standardomkostning på lager](../cost-management/manage-standard-cost-updates.md) | Generelt tilgængelig |
| Omkostningsstyring | Rapporten Lagerværdi – oprydning i data | Til som standard |
| Omkostningsstyring | [Lagerværdirapportlager](../cost-management/inventory-value-report-storage.md) | Til som standard |
| Omkostningsstyring | Vis lagerlukningslog i gitter | Til som standard |
| Styring af tekniske ændringer | [Aktivér administration af ændringer på eksisterende produkter](../engineering-change-management/change-management-existing-products.md) | Til som standard |
| Styring af tekniske ændringer | [Styring af tekniske ændringer](../engineering-change-management/product-engineering-overview.md) | Til som standard |
| Styring af tekniske ændringer | [Tekniske beskeder til produktion](../engineering-change-management/engineering-change-management.md) | Til som standard |
| Styring af tekniske ændringer | [Forbedret attributnedarvning for Administration af tekniske ændringer](../engineering-change-management/engineering-attributes-and-search.md) | Til som standard |
| Styring af tekniske ændringer | [Administrer ændringer af formler og deres ingredienser](../engineering-change-management/manage-formula-changes.md) | Til som standard |
| Styring af tekniske ændringer | [Kontroller af produktparathed](../engineering-change-management/product-readiness.md) | Til som standard |
| Styring af tekniske ændringer | [Variantgenerering af tekniske produkter](../engineering-change-management/engineering-variants.md) | Til som standard |
| Lager- og lokationsstyring | Navigering til styklisteversion fra styklistelinjer | Obligatorisk |
| Varedisponering | [Godkendelse og konsolidering, der kan køre i batch, for planlagte bulk- og pakkebatchordrer](whats-new-scm-10-0-20.md) | Generelt tilgængelig |
| Varedisponering | Ressourceplanlægning med vedligeholdelse | Generelt tilgængelig |
| Varedisponering | Aktivér guidefunktioner til opsætning af behovsplan | Obligatorisk |
| Varedisponering | [Valg af budgetmodel på Detaljer om behovsprognose](../master-planning/manual-adjustments-baseline-forecast.md) | Obligatorisk |
| Varedisponering | [Visualisering af status for varedisponering](../master-planning/tasks/monitor-master-planning-run.md) | Obligatorisk |
| Varedisponering | [Parallel autorisation af ordreforslag](../master-planning/planning-optimization/planned-order-firming.md) | Obligatorisk |
| Varedisponering | [Autorisation af ordreforslag med filtrering](../master-planning/planning-optimization/planned-order-firming.md) | Til som standard |
| Varedisponering | [Gemte visninger for ordreforslag](saved-views-scm.md) | Til som standard |
| Indkøb og forsyning | Deaktiver knappen Nulstilling af fordeling af indkøbsrekvisition | Generelt tilgængelig |
| Indkøb og forsyning | [Aktivér nulstilling af indkøbsrelaterede arbejdsgange](whats-new-scm-10-0-20.md) | Generelt tilgængelig |
| Indkøb og forsyning | Mulighed for at bekræfte accepterede indkøbsordrer fra kreditorsamarbejde i batch | Obligatorisk |
| Indkøb og forsyning | Lukket status for købsaftale | Obligatorisk |
| Indkøb og forsyning | Føj linjer til de indkøbsordrefakturaer, der er tilknyttet en købsaftale | Til som standard |
| Indkøb og forsyning | Føj feltet Bestilt antal til siden Bogføring af produktkvittering | Til som standard |
| Indkøb og forsyning | [Tillad, at leverandører ansøger om indkøbskategorier via leverandørsamarbejde](../procurement/category-requests-from-vendors.md) | Til som standard |
| Indkøb og forsyning | Gebyrer fra og til beløb på indkøbsordrer | Til som standard |
| Indkøb og forsyning | Konfiguration af gebyrer med websted og lagersted | Til som standard |
| Indkøb og forsyning | Aktivér beregning af indkøbsafgift på basis af årstarif | Til som standard |
| Indkøb og forsyning | [Ansvarlig part for købsaftale](../procurement/purchase-agreements.md) | Til som standard |
| Indkøb og forsyning | [Gemte visninger af indkøbsordrer](saved-views-scm.md) | Til som standard |
| Administration af produktoplysninger | [Streng validering af standardordreantal](../production-control/default-order-settings.md) | Obligatorisk |
| Administration af produktoplysninger | Forbehandling af styklisterapporten for at undgå timeout | Til som standard |
| Administration af produktoplysninger | Økonomiske standarddimensioner separat ved brug af vareskabeloner | Til som standard |
| Administration af produktoplysninger | Aktivér produktdimensionsgrupper for vareskabeloner | Til som standard |
| Administration af produktoplysninger | Regenerer produktvariantnavne baseret på nomenklatur | Til som standard |
| Administration af produktoplysninger | [Forbedringer af siden Variantforslag](../pim/tasks/create-predefined-product-variants.md) | Til som standard |
| Produktionsstyring | Forbedret pluk af fastvægtantal til produktion | Generelt tilgængelig |
| Produktionsstyring | Den nye knap Stop pause er tilføjet på siden Jobkortsterminal | Obligatorisk |
| Produktionsstyring | [Aktivér automatisk generering af id-nummer ved færdigmelding i jobkortenheden](../production-control/production-floor-execution-configure.md) | Obligatorisk |
| Produktionsstyring | Aktivér delvis modtagelse af varer fra underleverandør, og løs et problem med beregning af spild for styklistelinjer af typen Leverandør | Obligatorisk |
| Produktionsstyring | [Funktion til låsning af jobkortenhed og jobkortterminal, så de kan renses](../production-control/production-floor-execution-configure.md) | Obligatorisk |
| Produktionsstyring | Forbedringer af dialogboksene Godkend og Overførselsjob | Obligatorisk |
| Produktionsstyring | [Id for færdigmelding tilføjet i jobkortenheden](../production-control/production-floor-execution-configure.md) | Obligatorisk |
| Produktionsstyring | [Udskriv etiket fra jobkortenhed](../production-control/production-floor-execution-configure.md) | Obligatorisk |
| Produktionsstyring | [Produktionsudførelse](../production-control/production-floor-execution-configure.md) | Obligatorisk |
| Produktionsstyring | [Funktion til aktivstyring af grænsefladen til produktionsudførelse](../production-control/production-floor-execution-configure.md) | Til som standard |
| Produktionsstyring | [Jobsøgning til grænsefladen til produktionen](../production-control/production-floor-execution-configure.md) | Til som standard |
| Produktionsstyring | [Tilsidesæt standardproduktionsreservation](../production-control/override-default-reservation-principle.md) | Til som standard |
| Produktionsstyring | [Vis fulde serie-, batch- og id-numre i grænsefladen til produktionsudførelse](whats-new-scm-10-0-21.md) | Til som standard |
| Salg og marketing | [Forbedringer af ydeevne for salgsordredetaljer](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | Generelt tilgængelig |
| Salg og marketing | Forbedringer af ydeevne for salgstilbudsdetaljer | Generelt tilgængelig |
| Salg og marketing | Eksportpolitik for refererede salgsordredata | Obligatorisk |
| Salg og marketing | [Politik for sletning af salgsordrer til indkøbsordrelinjer](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-purchase-order-line-deletion-policy) | Obligatorisk |
| Salg og marketing | [Eksportpolitik for refererede salgstilbud](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy)| Obligatorisk |
| Salg og marketing | [Eksportoptimering af kontaktpersondataenheden](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Til som standard |
| Salg og marketing | Aktiver opslag for introduktion til salgstilbudsdokument og dokumentkonteringsfelter | Til som standard |
| Salg og marketing | [Forbedr ydeevne for rapport med "Top 100" kunder](whats-new-scm-10-0-23.md) | Til som standard |
| Salg og marketing | Genberegn forkalkuleret debitorsaldo | Til som standard |
| Salg og marketing | [Registrering af salgsreturordrelinje med decimalpræcision med og uden fastvægt](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Til som standard |
| Salg og marketing | [Gemte visninger af salg og marketing](saved-views-scm.md) | Til som standard |
| Salg og marketing | Salgsordrebekræftelse med et enkelt klik | Til som standard |
| Lagerstedsstyring | [Skabeloner til cross-docking med lokationsvejledninger](../warehousing/planned-cross-docking.md) | Generelt tilgængelig |
| Lagerstedsstyring | [Deaktiver forventede tilgange fra kvalitetsordrer, der vælger spærret lager](../inventory/inventory-blocking.md) | Generelt tilgængelig |
| Lagerstedsstyring | Historik for modtagelse af nummerplade | Generelt tilgængelig |
| Lagerstedsstyring | [Grænseflade for materialehåndteringsudstyr](../warehousing/mhax.md) | Generelt tilgængelig |
| Lagerstedsstyring | [Afrund antal ned til nærmeste salgsenhed ved frigivelse til lagersted](whats-new-scm-10-0-19.md) | Generelt tilgængelig |
| Lagerstedsstyring | Understøttelse af skalaenhed på arbejdslister for lagerstedsapp | Generelt tilgængelig |
| Lagerstedsstyring | Etiketdetaljer om forsendelsesbølge | Generelt tilgængelig |
| Lagerstedsstyring | [Brug hurtigere API til containere, der lukker/genåbner på pakkestation](whats-new-scm-10-0-21.md) | Generelt tilgængelig |
| Lagerstedsstyring | [Valider skabeloner, der er valgt til genopfyldningsjob](whats-new-scm-10-0-20.md) | Generelt tilgængelig |
| Lagerstedsstyring | Tillad genopfyldningsskabelon at bruge eksisterende omgående genopfyldningsarbejde (på tværs af enheder) | Obligatorisk |
| Lagerstedsstyring | Automatisk tildeling af GUID'er i WHS-brugeroprettelse | Obligatorisk |
| Lagerstedsstyring | Hent produktvarianter og sporingsdimensioner i lagerappen under modtagelse af lastvare | Obligatorisk |
| Lagerstedsstyring | [Skift lagerstatus for varer, der styres af sporingsdimensioner](../inventory/inventory-statuses.md) | Obligatorisk |
| Lagerstedsstyring | [Skift arbejdspulje på arbejde](../warehousing/change-work-pool-on-work.md) | Obligatorisk |
| Lagerstedsstyring | [Klyngeplacering fuld](../warehousing/cluster-position-full.md) | Obligatorisk |
| Lagerstedsstyring | [Funktionen klynge-læg på lager](../warehousing/putaway-clusters.md) | Obligatorisk |
| Lagerstedsstyring | [Bekræft og flyt](../warehousing/confirm-and-transfer.md) | Obligatorisk |
| Lagerstedsstyring | [Bekræfte udgående forsendelser fra batchjob](../warehousing/confirm-outbound-shipments-from-batch-jobs.md) | Obligatorisk |
| Lagerstedsstyring | [Kontrollér, om der skal vises en oversigtsside med tilgange på mobilenheder](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Obligatorisk |
| Lagerstedsstyring | [Udskudt behandling af manuel lagerbevægelseshandling](../warehousing/deferred-processing-manual-inventory-movement.md) | Obligatorisk |
| Lagerstedsstyring | Tillad ikke, at der oprettes laster, der ikke opfylder kravene i skabelon til bølgelastopbygning | Obligatorisk |
| Lagerstedsstyring | [Forbedrede layouts til id-etiket](../warehousing/document-routing-layout-for-license-plates.md) | Obligatorisk |
| Lagerstedsstyring | [Evaluer alle handlinger for direktiver med flere SKU-lokationer](../troubleshooting/warehousing/evaluate-multiple-location-directive-actions.md) | Obligatorisk |
| Lagerstedsstyring | Skjul feltet Samlet værdi på siderne "Alle laster" og "Lastdetaljer" | Obligatorisk |
| Lagerstedsstyring | Konfiguration af opbygning af id-etiket | Obligatorisk |
| Lagerstedsstyring | Manuel korrektion af lastlinje for administratorer eller lignende brugere, der er tillid til | Obligatorisk |
| Lagerstedsstyring | [Placering af lokations-id](../warehousing/location-license-plate-positioning.md) | Obligatorisk |
| Lagerstedsstyring | [Blanding af produktdimension for lokation](../warehousing/location-product-dimension-mixing.md) | Obligatorisk |
| Lagerstedsstyring | Gør feltet Lagerstatus for lagerbevægelse redigerbart på mobilenhed | Obligatorisk |
| Lagerstedsstyring | Manuel udvalgstjeneste for salgslinjer for administratorer eller lignende betroede brugere | Obligatorisk |
| Lagerstedsstyring | [Undgå, at id'er for afsendte flytteordrer bliver brugt på andre lagersteder end destinationslagerstedet](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Obligatorisk |
| Lagerstedsstyring | Spørg, om tvetydige 'Lok.-/Id'-navne skal fortolkes | Obligatorisk |
| Lagerstedsstyring | [Kvalitetskontrol](../warehousing/quality-check.md) | Obligatorisk |
| Lagerstedsstyring | [Brugerindstillinger, ikoner og trinindstillinger til den nye lagerapp](../warehousing/install-configure-warehouse-management-app.md) | Obligatorisk |
| Lagerstedsstyring | [Flere lokationszoner](../warehousing/additional-location-zones.md) | Til som standard |
| Lagerstedsstyring | [Opret, og behandl overførselsordrer fra lagersteds-appen](../warehousing/create-transfer-order-from-warehouse-app.md) | Til som standard |
| Lagerstedsstyring | Aktivér hurtig validering for mobilenheder til lagersted | Til som standard |
| Lagerstedsstyring | [Maksimal udførelsestid for jobbet i lokationsstyring til oprydning i disponible poster](../warehousing/onhand-cleanup.md) | Til som standard |
| Lagerstedsstyring | [Visualisering af udgående arbejdsbyrde](../warehousing/outbound-workload-visualization.md) | Til som standard |
| Lagerstedsstyring | [Proces for hændelser for lagerapp](../warehousing/warehouse-app-events.md) | Til som standard |
| Lagerstedsstyring | [Gemt visning for lastplanlægningspanelet](saved-views-scm.md) | Til som standard |
| Lagerstedsstyring | [Gemt visning af siden med arbejdsdetaljer](saved-views-scm.md) | Til som standard |
| Lagerstedsstyring | [Gemt visning til bølgebehandling](saved-views-scm.md) | Til som standard |
| Lagerstedsstyring | [Gemte visninger til lastbehandling](saved-views-scm.md) | Til som standard |
| Lagerstedsstyring | [Gemte visninger til forsendelsesbehandling](saved-views-scm.md) | Til som standard |
| Lagerstedsstyring | [Oplysninger om bølgebatchjob](../warehousing/wave-processing.md) | Til som standard |
| Lagerstedsstyring | [Beskeder om udførelse af bølge](../warehousing/wave-execution-notifications.md) | Til som standard |

## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformsopdateringer til Finans- og driftsapps

Microsoft Dynamics 365 Supply Chain Management 10.0.25 indeholder platformopdateringer. Du kan få mere vide i [Platformsopdateringer til version 10.0.25 af Finans- og driftsapps (april 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-25.md).

### <a name="bug-fixes"></a>Fejlrettelser

Du kan finde flere oplysninger om de fejlrettelser, der er inkluderet i hver af de opdateringer, som er del af 10.0.25, ved at logge på Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=654580&dbType=3&qc=3799fa965b008dd980d27cf740e4582e6384ec6601ae8a35b7eaec6f1287a868).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 og brancheskyer: 2022 frigivelsesplan bølge 1

Vil du gerne vide mere om kommende og de senest frigivne funktioner i en af vores forretningsapps eller platforme?

Undersøg [Dynamics 365 og brancheskyer: 2022 frigivelsesplan bølge 1](/dynamics365-release-plan/2022wave1/). Vi har samlet alle oplysninger fra start til slut og top til bund i et enkelt dokument, som du kan bruge til planlægning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og udfasede Supply Chain Management-funktioner

Artiklen [Fjernede eller udfasede funktioner Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver de funktioner, der er planlagt eller skal fjernes eller udfases for Supply Chain Management.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Før en funktion fjernes fra produktet, vil du få besked om udfasning i artiklen [Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder, inden de fjernes.

For ændringer, der kun påvirker kompileringstiden, men som er binære, som er kompatible med sandkasse- og produktionsmiljøer, vil tidsrummet for udfasningen være mindre end 12 måneder. Det er typisk funktionelle opdateringer, der skal foretages i compileren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
