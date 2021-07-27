---
title: Parametre, der ikke bruges af planlægningsoptimering
description: Dette emne viser de parametre, som planlægningsoptimering i øjeblikket ikke overvejer under driften.
author: crytt
ms.date: 6/29/2021
ms.topic: article
ms.search.form: ReqParameters, ReqGroup, ReqItemTable, ReqPlanSched, EcoResProductDetailsExtended, InventItemOrderSetup, WorkCalendarTable, PdsDispositionMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-29
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4d459f4de67f26f36aabcbde015988132e957601
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361328"
---
# <a name="parameters-not-used-by-planning-optimization"></a>Parametre, der ikke bruges af planlægningsoptimering

[!include [banner](../../includes/banner.md)]

Dette emne viser de parametre, som planlægningsoptimering i øjeblikket ikke overvejer under driften. Planlægningstjenesten kan springe en parameter over, for eksempel fordi relaterede funktioner endnu ikke understøttes. Alternativt kan parameteren være forældet på grund af funktionelle ændringer.

I følgende afsnit vises de parametre, som planlægningsoptimering ikke bruger på bestemte sider. De forklarer også, hvorfor de enkelte parametre ikke bruges.

## <a name="master-planning-parameters-page"></a>Siden Varedisponeringsparametre

Planlægningsoptimering bruger ikke følgende parametre eller indstillinger på siden **Varedisponeringsparametre**:

- Fanen **Generelt**:

    - **Aktuel prognoseplan** – Afventer understøttelse af *Prognose*.
    - **Aktuel statisk behovsplan** – Afventer understøttelse af *Kopiér statisk til dynamisk plan*.
    - **Aktuel dynamisk behovsplan** – Afventer understøttelse af *Kopiér statisk til dynamisk plan*.
    - **Kopiér den komplette og opdaterede statiske behovsplan til den dynamiske behovsplan** – Afventer understøttelse af *Kopiér statisk til dynamisk plan*.
    - **Starttid for beregnede forsinkelser** – Afventer understøttelse af *Beregnede forsinkelser*.
    - **Brug dynamiske negative dage** – Planlægningsoptimering bruger altid tilgangen *Dynamiske negative dage*.
    - **Dags dato-kalender** – Afventer understøttelse af *Planlægning*.
    - **Brug af cache** – I konfigurationen af Microsoft Azure-abonnementet håndteres performancepoint.
    - **Antal opgaver i bundt med hjælpefunktioner** – I konfigurationen af Azure-abonnementet håndteres performancepoint.
    - **Forbehandling: Filtrér automatisk efter elementer med direkte behov** – I konfigurationen af Azure-abonnementet håndteres performancepoint.
    - **Efterbehandling: Filtrér automatisk efter elementer med direkte behov** – I konfigurationen af Azure-abonnementet håndteres performancepoint.
    - **Antal ordrer i autorisationsbundt** – I konfigurationen af Azure-abonnementet håndteres performancepoint.
    - **Antal tråde** – I konfigurationen af Azure-abonnementet håndteres performancepoint.
    - **Timeoust for planlægningsproces i minutter** – I konfigurationen af Azure-abonnementet håndteres performancepoint.
    - **Starttidspunkt for planlægning** – Afventer understøttelse af *Planlægning*.

- Fanen **Ordreforslag**:

    - **Tilgangstidspunkt** – Afventer understøttelse af *Planlægning*.
    - **Produktion** – Afventer understøttelse af *Planlægning*.
    - Felter i sektionen **Projekt** – Afventer understøttelse af *Planlægning*.

- Fanen **Standardopdatering**:

    - **Opdater afmærkning** – Afventer understøttelse af *Autorisation*.
    - **Stop autorisation, hvis der opstår en fejl** – Afventer understøttelse af *Autorisation*.
    - **Gruppér efter leverandør** – Afventer understøttelse af *Autorisation*.
    - **Gruppér efter købergruppe** – Afventer understøttelse af *Autorisation*.
    - **Gruppér efter købsaftale** – Afventer understøttelse af *Autorisation*.
    - **Gruppér efter periode** – Afventer understøttelse af *Autorisation*.
    - **Søg efter købsaftale** – Afventer understøttelse af *Autorisation*.
    - **Gruppér efter planlægningsprioritet** – Afventer understøttelse af *Autorisation*.
    - **Gruppér efter periode** – Afventer understøttelse af *Autorisation*.

## <a name="coverage-groups-page"></a>Siden Disponeringsgrupper

Planlægningsoptimering bruger ikke følgende parametre eller indstillinger på siden **Disponeringsgrupper**:

- Oversigtspanelet **Generelt**:

    - **Positive dage** – Afventer understøttelse af *Positive dage*.
    - **Forbrug disponibel lagerbeholdning** – Afventer understøttelse af *Forbrug af disponibel lagerbeholdning*.
    - **Brug den angivne stykliste- eller formelversion** – Afventer understøttelse af *Formelversioner med sam-/biprodukt*.
    - **Brug den angivne ruteversion** – Afventer understøttelse af *Efterspørgsel, der har defineret specifikke stykliste- eller rutekrav*.

- Oversigtspanelet **Handlinger**:

    - **Handlingsmeddelelse** – Afventer understøttelse af *Handlinger*.
    - **Handlingstidshorisont** – Afventer understøttelse af *Handlinger*.
    - **Udskyd margen** – Afventer understøttelse af *Handlinger*.
    - **Fremskynd margen** – Afventer understøttelse af *Handlinger*.
    - **Basisdato** – Afventer understøttelse af *Handlinger*.
    - **Fremskynd** – Afventer understøttelse af *Handlinger*.
    - **Udskyd** – Afventer understøttelse af *Handlinger*.
    - **Nedskriv** – Afventer understøttelse af *Handlinger*.
    - **Opskriv** – Afventer understøttelse af *Handlinger*.
    - **Afledte handlinger** – Afventer understøttelse af *Handlinger*.

- Oversigtspanelet **Andet**:

    - **Låsningstidshorisont (dage)** – *Låsningstidshorisont* understøttes ikke i planlægningsoptimering.
    - **Tidshorisont for udfoldning af stykliste (dage)** – Afventer understøttelse af *Planlægning*.
    - **Tidshorisont for kapacitetsplanlægning (dage)** – Afventer understøttelse af *Planlægning*.
    - **Tidshorisont for godkendte rekvisitioner (dage)** – Afventer understøttelse af *Rekvisition*.
    - **Tidshorisont for hovedplan** – Afventer understøttelse af *Prognose*.

- Oversigtspanelet **Forsinkelser**:

    - **Beregnede forsinkelser** – Afventer understøttelse af *Beregnede forsinkelser*.
    - **Tidshorisont for beregnede forsinkelser (dage)** – Afventer understøttelse af *Beregnede forsinkelser*.

## <a name="item-coverage-page"></a>Siden Varedisponering

Planlægningsoptimering bruger ikke følgende parametre eller indstillinger på siden **Varedisponering**:

- Fanen **Generelt**:

    - **Ordreforslagstype** – Planlægningsoptimering understøtter ikke indstillingen *Kanban*, afventer understøttelse af *Kanban*.
    - **Låsningstidshorisont (dage)** – *Låsningstidshorisont* understøttes ikke i planlægningsoptimering.
    - **Tidshorisont for udfoldning af stykliste (dage)** – Afventer understøttelse af *Planlægning*.
    - **Tidshorisont for kapacitetsplanlægning (dage)** – Afventer understøttelse af *Planlægning*.
    - **Tidshorisont for godkendte rekvisitioner (dage)** – Afventer understøttelse af *Rekvisition*.
    - **Opfyld minimum** – Planlægningsoptimering understøtter ikke indstillingerne *Dags dato*, *Første afgang* og *Disponeringstidshorisont*. Den bruger altid indstillingen *Dags dato + fremskaffelsestid*.
    - **Minimumsperioder** – Afventer understøttelse af *Minimumslagerniveau*.
    - **Planlægningsformel** – Afventer understøttelse af *Formelversioner med sam-/biprodukter*.
    - **Standardprioritet** – Afventer understøttelse af *Formelversioner med sam-/biprodukter*.
    - **Aktuel prioritet** – Afventer understøttelse af *Formelversioner med sam-/biprodukter*.
    - **Ændringsdato** – Afventer understøttelse af *Formelversioner med sam-/biprodukter*.
    - **Forbrug disponibel lagerbeholdning** – Afventer understøttelse af *Forbrug af disponibel lagerbeholdning*.

## <a name="master-plans-page"></a>Siden Behovsplaner

Planlægningsoptimering bruger ikke følgende parametre eller indstillinger på siden **Behovsplaner**:

- Oversigtspanelet **Generelt**:

    - **Medtag disponibel lagerbeholdning** – Afventer understøttelse af *Forbrug af disponibel lagerbeholdning*.
    - **Tilsidesæt disponibel lagerbeholdning** – Afventer understøttelse af *Forbrug af disponibel lagerbeholdning*.
    - **Forbrug disponibel lagerbeholdning** – Afventer understøttelse af *Forbrug af disponibel lagerbeholdning*.
    - **Medtag lagertransaktioner** – Afventer understøttelse af *Forbrug af disponibel lagerbeholdning*.
    - **Medtag salgstilbud** – Afventer understøttelse af *Salgstilbud*.
    - **Medtag tilbudsanmodninger** – Afventer understøttelse af *Tilbudsanmodninger*.
    - **Brug datoer for hyldelevetid** – Afventer understøttelse af *Hyldelevetid*.
    - **Medtag kontinuitetsplan** – Afventer understøttelse af *Kontinuitetsplanlægning*.
    - **Planlægningsmetode** – Afventer understøttelse af *Planlægning*.
    - **Egenskabsbegrænsning** – Afventer understøttelse af *Planlægning*.
    - **Kapacitetstidshorisont for planlægning bagud (dage)** – Afventer understøttelse af *Planlægning*.
    - **Kapacitetsbegrænsning** – Afventer understøttelse af *Planlægning*.
    - **Tidshorisont for kapacitetsbegrænsning** – Afventer understøttelse af *Planlægning*.
    - **Kapacitetsbegrænsning for flaskehalsressourcer** – Afventer understøttelse af *Planlægning*.
    - **Kapacitetstidshorisont for flaskehalsressourcer** – Afventer understøttelse af *Planlægning*.
    - **Ordreforslag** – Planlægningsoptimering bruger faste nummerserier.
    - **Session** – Planlægningsoptimering bruger faste nummerserier.
    - **Kontinuitetsplan** – Planlægningsoptimering bruger faste nummerserier.

- Oversigtspanelet **Tidshorisonter i dage**:

    - **Låsning** – *Låsningstidshorisont* understøttes ikke i planlægningsoptimering.
    - **Udfoldning** – Afventer understøttelse af *Planlægning*.
    - **Hovedplan** – Afventer yderligere understøttelse af *Prognose*.
    - **Kapacitet** – Afventer understøttelse af *Planlægning*.
    - **Kontinuitetsplan** – Afventer understøttelse af *Kontinuitetsplanlægning*.
    - **Handlingsmeddelelse** – Afventer understøttelse af *Handlinger*.
    - **Beregnede forsinkelser** – Afventer yderligere understøttelse af *Beregnede forsinkelser*.
    - **Rækkefølge** – Afventer understøttelse af *Produktion*.

- Oversigtspanelet **Beregnede forsinkelser**:

    - **Sørg for, at de planlagte ordrer ikke oprettes inden varedisponeringens kørselsdato** – Afventer understøttelse af *Beregnede forsinkelser*.
    - **Føj den beregnede forsinkelse til behovsdatoen** (i sektionen **Indkøbsordreforslag**) – Afventer understøttelse af *Beregnede forsinkelser*.
    - **Føj den beregnede forsinkelse til behovsdatoen** (i sektionen **Produktionsordreforslag**) – Afventer understøttelse af *Beregnede forsinkelser*.
    - **Føj den beregnede forsinkelse til behovsdatoen** (i sektionen **Planlagte flytteordrer**) – Afventer understøttelse af *Beregnede forsinkelser*.
    - **Føj den beregnede forsinkelse til behovsdatoen** (i sektionen **Planlagte kanban**) – Afventer understøttelse af *Beregnede forsinkelser*.

- Oversigtspanelet **Rækkefølge**:

    - **Sortér ordreforslag efter varedisponering** – Afventer understøttelse af *Rækkefølge*.
    - **Gruppetype** – Afventer understøttelse af *Rækkefølge*.
    - **Periodetype** – Afventer understøttelse af *Rækkefølge*.
    - **Antal filsæt i kampagnecyklussen** – Afventer understøttelse af *Rækkefølge*.

## <a name="released-product-details-page"></a>Siden Frigivne produktdetaljer

Planlægningsoptimering bruger ikke følgende parametreindstilling på siden **Frigivne produktdetaljer**:

- Oversigtspanelet **Tekniker**:

    - **Produktionstype** – Planlægningsoptimering understøtter ikke indstillingen *Planlægningsvare*, afventer understøttelse af *Planlægningsvarer*.

## <a name="default-order-settings-page"></a>Siden Standardindstillinger for ordre

Planlægningsoptimering bruger ikke følgende parametreindstilling på siden **Standardindstillinger for ordre**:

- Oversigtspanelet **Lager**:

    - **Leveringsdatokontrol** – Planlægningsoptimering understøtter ikke indstillingen *LE*, afventer understøttelse af *LE*.

## <a name="working-time-calendars-page"></a>Siden Arbejdstidskalendere

Planlægningsoptimering bruger ikke følgende parameter på siden **Arbejdstidskalendere**:

- **Basiskalender** – Afventer understøttelse af *Basiskalendere*.

## <a name="batch-disposition-master-page"></a>Siden Batchdispositionsmaster

Planlægningsoptimering bruger ikke følgende parameter på siden **Batchdispositionsmaster**:

- Oversigtspanelet **Opsætning**:

    - **Tilgængelig** – Afventer understøttelse af *Batchdispositionskoder*.