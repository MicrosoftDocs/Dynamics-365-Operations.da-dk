---
title: Integrere med produktionsudførelsessystemer fra tredjeparter
description: Dette emne forklarer, hvordan du kan integrere Microsoft Dynamics 365 Supply Chain Management med et MES-system (produktionsudførelsessystem fra tredjepart).
author: t-benebo
ms.date: 10/01/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-01
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 14e86a49777eefefae711bfe0d756361b09d69c2
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778443"
---
# <a name="integrate-with-third-party-manufacturing-execution-systems"></a>Integrere med produktionsudførelsessystemer fra tredjeparter

[!include [banner](../includes/banner.md)]

Nogle produktionsorganisationer, der bruger Microsoft Dynamics 365 Supply Chain Management, anvender den oprindelige funktion i Dynamics 365 til at styre deres produktionsaktiviteter for maskiner, udstyr og personale. Andre produktionsorganisationer, særligt dem, der har avancerede produktionskrav, bruger i stedet et produktionsudførelsessystem fra tredjepart (MES). Organisationer kan vælge en tredjeparts MES-løsning, fordi den f.eks. er specielt tilpasset deres lodrette branche.

I den integrerede løsning automatiseres dataudvekslingen fuldstændigt og finder sted i næsten realtid. Dataene holdes derfor aktuelle i begge systemer, og der kræves ingen manuel indtastning af data. Når der f.eks. registreres materialeforbrug i MES, sikrer integrationen, at samme forbrug også registreres i Dynamics 365. Derfor er opdaterede lagerposter tilgængelige for andre vigtige processer som f.eks. planlægning og salg.

Løsningen gør det hurtigere, nemmere og billigere for Supply Chain Management-brugere at integrere med tredjeparts-MES'er. Den har følgende funktioner:

- Forretningshændelser og grænseflader, der understøtter [vigtige processer til produktionsudførelse](#processes-available-for-mes-integration)
- Et centraliseret dashboard, hvor du kan spore historikken til behandling af hændelser og lokalisere fejl og rette processer, der mislykkes

I følgende illustration vises en typisk samling forretningshændelser, processer og meddelelser, der udveksles i en integreret løsning.

![Typisk integrationsscenarie.](media/3p-mes-scenario.png "Typisk integrationsscenarie.")

## <a name="turn-on-the-mes-integration-feature"></a>Aktivere MES-integrationsfunktionen

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Produktionsstyring*
- **Funktionsnavn:** *Integration af produktionsudførelsessystem*

## <a name="processes-available-for-mes-integration"></a>Processer til MES-integration

Du kan aktivere en hvilken som helst af eller alle følgende integrationsprocesser.

| Procesnavn | Beskrivelse |
|---|---|
| Frigive produktionsordrer og produktionsordrestatus af ændringsforretningshændelser | Denne proces giver en forretningshændelse, som MES kan lytte til for at få oplysninger om de produktionsordrer, der skal produceres. Referencedata, der er relateret til produktionsordren, forventes at blive delt fra Supply Chain Management til MES via Open Data Protocol (OData) eller dataenheder. |
| Start produktionsordre | Denne proces giver Supply Chain Management oplysninger om produktionsordrer, der startes ved hjælp af MES. Den sikrer, at begge systemer har en opdateret visning af alle produktionsaktiviteter. |
| Rapportere produceret eller kasseret antal | Denne proces giver Supply Chain Management oplysninger om de gode og fejlbehæftede mængder, der rapporteres på et produktionsjob ved hjælp af MES. Det sikrer, at produktionens tilsynsførende har en opdateret visning af status for produktionsplanen. |
| Rapportere materialeforbrug | Denne proces giver Supply Chain Management oplysninger fra MES om antallet af materialer, der forbruges. Den gør opdaterede lagerposter tilgængelige for andre vigtige processer som f.eks. planlægning og salg. |
| Rapportere tidsforbrug for operationen | Denne proces giver Supply Chain Management oplysninger om den tid, der bruges til en bestemt operation. |
| Slut på produktionsordre | Denne proces informerer Supply Chain Management om, at MES har opdateret en produktionsordre til dens endelige status som *Afsluttet*. Denne status angiver, at der ikke produceres flere mængder på produktionsordren. |

## <a name="monitor-incoming-messages"></a>Overvåge indgående meddelelser

Åbn siden **Integration af produktionsudførelsessystemer** for at overvåge indgående meddelelser i systemet. Her kan du se, behandle og udføre fejlfinding af problemer.

## <a name="call-the-api"></a>Kalde API'en

Hvis du vil kalde MES-integrations-API'en, skal du sende en `POST`-anmodning til følgende URL-adresse for slutpunkt:

`/api/services/SysMessageServices/SysMessageService/SendMessage`

Indholdet af den anmodning, du sender, skal ligne følgende eksempel. Erstat værdierne for `_companyId`, `_messageType` og `_messageContent` efter behov. Du kan finde oplysninger om de forskellige meddelelsestyper, som API understøtter, og hvordan indholdet af dem designes, i næste afsnit.

```json
{
    "_companyId": "USMF",
    "_messageQueue": "JmgMES3P",
    "_messageType": "ProdProductionOrderReportFinished",
    "_messageContent":
    "{\"ProductionOrderNumber\": \"P000123\", \"ReportFinishedLines\": [{\"ItemNumber\": \"A0001\", \"ReportedGoodQuantity\": 10, \"ReportAsFinishedDate\": \"2021-01-01\"}]}"
}
```

## <a name="api-message-types-and-content"></a>API-meddelelsestyper og -indhold

Dette afsnit indeholder en beskrivelse af hver type meddelelse, der kan udveksles via MES-integrations-API.

### <a name="start-production-order-message"></a>Meddelelse om start af produktionsordre

For meddelelsen *start produktionsordre* er `_messageType`-værdien `ProdProductionOrderStart`. Følgende tabel indeholder de felter, som denne meddelelse understøtter.

| Feltnavn | Status | Type |
|---|---|---|
| `ProductionOrderNumber` | Obligatorisk | Streng |
| `StartedQuantity` | Valgfri | Kommatal |
| `StartedDate` | Valgfri | Dato |
| `AutomaticBOMConsumptionRule` | Valgfri | Fasttekst (FlushingPrincip \| Altid \| Aldrig) |

### <a name="report-as-finished-message"></a>Færdigmeldingsmeddelelse

For meddelelsen *færdigmeld* er `_messageType`-værdien `ProdProductionOrderReportFinished`. Følgende tabel indeholder de felter, som denne meddelelse understøtter.

| Feltnavn | Status | Type |
|---|---|---|
| `ProductionOrderNumber` | Obligatorisk | Streng |
| `ReportFinishedLines` | Obligatorisk | En liste over linjer (mindst én), der hver især indeholder de nyttedata, der er beskrevet i næste tabel |

Følgende tabel viser de felter, som hver linje i sektionen `ReportFinishedLines` i meddelelsen `ProdProductionOrderReportFinished` understøtter.

| Feltnavn | Status | Type |
|---|---|---|
| `LineNumber` | Valgfri | Kommatal |
| `ItemNumber` | Valgfri | Streng|
| `ProductionType` | Valgfri | Fasttekst (MainItem \| Formel \| Stykliste \| Samprodukt \| Efter_produkt \| Ingen), kan udvides |
| `ReportedErrorQuantity` | Valgfri | Kommatal|
| `ReportedGoodQuantity` | Valgfri | Kommatal|
| `ReportedErrorCatchWeightQuantity` | Valgfri | Kommatal |
| `ReportedGoodCatchWeightQuantity` | Valgfri | Kommatal |
| `AcceptError` | Valgfri |Boolesk |
| `ErrorCause` | Valgfri | Fasttekst (Ingen \| Materiale \| Maskine \| OperatingStaff), kan udvides |
| `ExecutedDateTime` | Valgfri | Dato/klokkeslæt |
| `ReportAsFinishedDate` | Valgfri | Dato |
| `AutomaticBOMConsumptionRule` | Valgfri | Fasttekst (FlushingPrincip \| Altid \| Aldrig) |
| `AutomaticRouteConsumptionRule` | Valgfri |Fasttekst (RouteDependent \| Altid \| Aldrig) |
| `RespectFlushingPrincipleDuringOverproduction` | Valgfri | Boolesk |
| `ProductionJournalNameId` | Valgfri | Streng |
| `PickingListProductionJournalNameId` | Valgfri | Streng|
| `RouteCardProductionJournalNameId` | Valgfri | Streng |
| `FromOperationNumber` | Valgfri | Heltal|
| `ToOperationNumber` | Valgfri | Heltal|
| `InventoryLotId` | Valgfri | Streng |
| `BaseValue` | Valgfri | Streng |
| `EndJob` | Valgfri | Boolesk |
| `EndPickingList` | Valgfri | Boolesk |
| `EndRouteCard` | Valgfri | Boolesk |
| `PostNow` | Valgfri | Boolesk |
| `AutoUpdate` | Valgfri | Boolesk |
| `ProductColorId` | Valgfri | Streng|
| `ProductConfigurationId` | Valgfri | Streng |
| `ProductSizeId` | Valgfri | Streng |
| `ProductStyleId` | Valgfri | Streng |
| `ProductVersionId` | Valgfri | Streng |
| `ItemBatchNumber` | Valgfri | Streng |
| `ProductSerialNumber` | Valgfri | Streng |
| `LicensePlateNumber` | Valgfri | Streng |
| `InventoryStatusId` | Valgfri | Streng |
| `ProductionWarehouseId` | Valgfri | Streng |
| `ProductionSiteId` | Valgfri | Streng |
| `ProductionWarehouseLocationId` | Valgfri | Streng |
| `InventoryDimension1` til `InventoryDimension12` | Valgfri | Streng |

De 12 udvidelige dimensioner (`InventoryDimension1` til `InventoryDimension12`) kræver tilpasning og bruges ikke altid. Du kan finde flere oplysninger om dem i [Tilføje nye lagerdimensioner via udvidelse](../../fin-ops-core/dev-itpro/extensibility/inventory-dimensions.md).

### <a name="material-consumption-picking-list-message"></a>Meddelelse om materialeforbrug (plukliste)

For meddelelsen om *materialeforbrug (plukliste)* er `_messageType`-værdien `ProdProductionOrderPickingList`. Følgende tabel indeholder de felter, som denne meddelelse understøtter.

| Feltnavn | Status | Type |
|---|---|---|
| `ProductionOrderNumber` | Obligatorisk | Streng |
| `JournalNameId` | Valgfri | Streng |
| `PickingListLines` | Obligatorisk | En liste over linjer (mindst én), der hver især indeholder de nyttedata, der er beskrevet i næste tabel |

Følgende tabel viser de felter, som hver linje i sektionen `PickingListLines` i meddelelsen `ProdProductionOrderPickingList` understøtter.

| Feltnavn | Status | Type |
|---|---|---|
| `ItemNumber` | Obligatorisk | Streng |
| `ConsumptionBOMQuantity` | Valgfri | Kommatal |
| `ProposalBOMQuantity` | Valgfri | Kommatal |
| `ScrapBOMQuantity` | Valgfri | Kommatal |
| `BOMUnitSymbol` | Valgfri | Streng |
| `ConsumptionInventoryQuantity` | Valgfri | Kommatal |
| `ProposalInventoryQuantity` | Valgfri | Kommatal |
| `ConsumptionCatchWeightQuantity` | Valgfri | Kommatal |
| `ProposalCatchWeightQuantity` | Valgfri | Kommatal |
| `ConsumptionDate` | Valgfri | Dato |
| `OperationNumber` | Valgfri | Heltal |
| `LineNumber` | Valgfri | Kommatal |
| `PositionNumber` | Valgfri | Streng |
| `IsConsumptionEnded` | Valgfri | Boolesk |
| `ErrorCause` | Valgfri | Fasttekst (Ingen \| Materiale \| Maskine \| OperatingStaff), kan udvides |

### <a name="time-used-for-operation-route-card-message"></a>Meddelelse om den tid, der bruges til operationen (rutekort)

For meddelelsen om *tid, der bruges til operation (rutekort)* er `_messageType`-værdien `ProdProductionOrderRouteCard`. Følgende tabel indeholder de felter, som denne meddelelse understøtter.

| Feltnavn | Status | Type |
|---|---|---|
| `ProductionOrderNumber` | Obligatorisk | Streng |
| `JournalNameId` | Valgfri | Streng |
| `RouteCardLines` | Obligatorisk | En liste over linjer (mindst én), der hver især indeholder de nyttedata, der er beskrevet i næste tabel |

Følgende tabel viser de felter, som hver linje i sektionen `RouteCardLines` i meddelelsen `ProdProductionOrderRouteCard` understøtter.

| Feltnavn | Status | Type |
|---|---|---|
| `OperationNumber` | Obligatorisk | Obligatorisk, heltal |
| `OperationPriority` | Valgfri | Fasttekst (Primær \| Sekundær1 \| Sekundær2 \| ... \| Sekundær20) |
| `OperationId` | Valgfri | Streng |
| `OperationsResourceId` | Valgfri | Streng |
| `Worker` | Valgfri | Streng |
| `HoursRouteCostCategoryId` | Valgfri | Streng |
| `QuantityRouteCostCategoryId` | Valgfri | Streng |
| `HourlyRate` | Valgfri | Kommatal |
| `Hours` | Valgfri | Kommatal |
| `GoodQuantity` | Valgfri | Kommatal |
| `ErrorQuantity` | Valgfri | Kommatal |
| `CatchWeightGoodQuantity` | Valgfri | Kommatal |
| `CatchWeightErrorQuantity` | Valgfri | Kommatal |
| `QuantityPrice` | Valgfri | Kommatal |
| `ProcessingPercentage` | Valgfri | Kommatal |
| `ConsumptionDate` | Valgfri | Dato |
| `TaskType` | Valgfri | Fasttekst (QueueBefore \| Konfiguration \| Proces \| Overlap \| Transport \| QueueAfter \| Byrde) |
| `ErrorCause` | Valgfri | Fasttekst (Ingen \| Materiale \| Maskine \| OperatingStaff), kan udvides |
| `OperationCompleted` | Valgfri | Boolesk |
| `BOMConsumption` | Valgfri | Boolesk |
| `ReportAsFinished` | Valgfri | Boolesk |

### <a name="end-production-order-message"></a>Meddelelse om slutning af produktionsordre

For meddelelsen *slutning af produktionsordre* er `_messageType`-værdien `ProdProductionOrderEnd`. Følgende tabel indeholder de felter, som denne meddelelse understøtter.

| Feltnavn | Status | Type |
|---|---|---|
| `ProductionOrderNumber` | Obligatorisk | Streng |
| `ExecutedDateTime` | Valgfri | Dato/klokkeslæt |
| `EndedDate` | Valgfri | Dato |
| `UseTimeAndAttendanceCost` | Valgfri | Boolesk |
| `AutoReportAsFinished` | Valgfri | Boolesk |
| `AutoUpdate` | Valgfri | Boolesk |

## <a name="receive-feedback-about-the-state-of-a-message"></a>Modtage feedback om meddelelsens tilstand

Når MES har sendt en meddelelse til Supply Chain Management, kan det være relevant, at Supply Chain Management returnerer feedback om meddelelsens tilstand. Her er nogle eksempler på situationer, hvor denne funktionsmåde kan være relevant:

- Der er ingen person, som er ansvarlig for det konstante tilsyn med MES-integrationen.
- Den person, der er ansvarlig for tilsyn med MES-integrationen, vil have besked via mail, når en meddelelse mislykkes, så de ved, at de er nødt til at gøre noget.
- MES skal vise en fejlmeddelelse for at informere produktionsoperatøren eller nogen fra it-afdelingen om, at de skal gøre noget.
- MES skal genberegne ordreplanen, når den har modtaget en fejlmeddelelse (f.eks. fordi en produktionsordre ikke kunne startes).

I disse tilfælde kan du benytte standardpåmindelsesfunktionen i Supply Chain Management. Du kan finde oplysninger om, hvordan standardbeskeder fungerer, i følgende ressourcer:

- Hjælp-emne: [Oversigt over påmindelser](../../fin-ops-core/fin-ops/get-started/alerts-overview.md)
- Video: [Indstillinger for påmindelsesregel i Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=cpzimwOjicM&ab_channel=MicrosoftDynamics365)

Du kan f.eks. konfigurere følgende påmindelser for at levere feedback om meddelelsens tilstand:

- Opret en forretningshændelse ("Send eksternt"), der bruges, når en meddelelse er *Ikke udført*.
- Send en besked og en mail til it-administrationen eller produktionschefen.
