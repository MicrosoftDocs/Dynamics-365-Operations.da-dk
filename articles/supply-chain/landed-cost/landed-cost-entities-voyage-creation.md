---
title: Enheder til rejseoprettelse
description: Denne artikel indeholder oplysninger om dataenheder til ruteoprettelse, som grupperer de dataenheder, der skal bruges til at oprette en arbejdsrute.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: cb2e2f53942015caf9462692515f24deb9689aed
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873892"
---
# <a name="voyage-creation-entities"></a>Ruteoprettelsesenheder

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

Dataenhederne til ruteoprettelse grupperer de dataenheder, der skal bruges til at oprette en arbejdsrute. Du eller din speditør kan bruge disse dataenheder til at oprette rute, forsendelsescontainer, folio og rutelinjeposter, der refererer til eksisterende indkøbs- eller overførselsordrelinjer.

## <a name="voyages-itmtableentity"></a>Ruter (ITMTableEntity)

Ruten repræsenterer rejsen for indgående varer og fungerer som det højeste omkostningsområde i Landingsomkostninger. Den indeholder oplysninger på overskriftsniveau, der er relateret til fartøjet, oprindelseshavnen og destinationshavnen. Denne funktion understøttes af enheden `ITMTableEntity`. Følgende tabel indeholder de felter og tilknytninger, der udgør denne enhed.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Leveringsmåde | ITMTable.DlvModeId | Nvarchar(10) | Nej | Nej |
| Mægler adviseret | ITMTable.ITMBrokerAdvised | Datetime | Nej | Nej |
| Kundeaftale | ITMTable.ITMCustomerAppointment | Datetime | Nej | Nej |
| Leveret på lagersted | ITMTable.ITMDelAtWarehouse | Datetime | Nej | Nej |
| Leveringsinstruktioner | ITMTable.ITMDeliveryInstructions | Datetime | Nej | Nej |
| Afrejsedato | ITMTable.ITMDepartureDate | Datetime | Nej | Nej |
| Frigivne varer | ITMTable.ITMGoodsReleased | Datetime | Nej | Nej |
| Dato for lokal transport | ITMTable.ITMLocalTransportDate | Datetime | Nej | Nej |
| Klokkeslæt for lokal transport | ITMTable.ITMLocalTransportTime | Int | Nej | Nej |
| Oprindelig fragtseddel er afsendt | ITMTable.ITMOriginalBOLSebt | Datetime | Nej | Nej |
| Originaldokumenter modtaget. | ITMTable.ITMOriginalDocsReceived | Datetime | Nej | Nej |
| Status for indkøbsordre | ITMTable.ITMPurchStatus | Int | Nej | Nej |
| Bekræftelsesdato | ITMTable.ITMVerificationDate | Datetime | Nej | Nej |
| Toldindgangs-id | ITMTable.ShipCustomsEntryId | Nvarchar(20) | Nej | Nej |
| Afsendelsesdato | ITMTable.ShipDate | Datetime | Nej | Nej |
| Beskrivende tekst | ITMTable.ShipDescription | Nvarchar(60) | Nej | Nej |
| Dokumenter modtaget | ITMTable.ShipDocReceived | Int | Nej | Nej |
| Forventet leveringsdato | ITMTable.ShipEstDlvDate | Datetime | Nej | Nej |
| ETA på forsendelseshavn | ITMTable.ShipEstPortDate | Datetime | Nej | Nej |
| Fra havn | ITMTable.ShipFromPort | Nvarchar(20) | Nej | Nej |
| Speditørluftfragtbrev/fragtseddel | ITMTable.ShipHAWB | Nvarchar(20) | Nej | Nej |
| Fragt | ITMTable.ShipId | Nvarchar(20) | **Ja** | **Ja** |
| Reservationsreference | ITMTable.ShipIdExternal | Nvarchar(20) | Nej | Nej |
| Ruteskabelon | ITMTable.ShipJourneyId | Nvarchar(20) | Nej | Nej |
| Lokal speditør | ITMTable.ShipLocalForwarder | Nvarchar(20) | Nej | Nej |
| Masterluftfragtbrev/fragtseddel | ITMTable.ShipMAWB | Nvarchar(20) | Nej | Nej |
| Mål | ITMTable.ShipMeasurement | Numeric(32, 6) | Nej | Nej |
| Måleenhed | ITMTable.ShipMeasurementUnit | Int | Nej | Nej |
| Antal paller | ITMTable.ShipNoOfPallets | Int | Nej | Nej |
| Ventende fragt | ITMTable.ShipPending | Int | Nej | Nej |
| Kommentarer | ITMTable.ShipRemarks | Nvarchar(MAX) | Nej | Nej |
| Udlejning | ITMTable.ShipRental | Int | Nej | Nej |
| Fragtstatus | ITMTable.ShipStatusId | Nvarchar(20) | Nej | Nej |
| Optælling i tal | ITMTable.ShipTallyInNumber | Nvarchar(20) | Nej | Nej |
| Til havn | ITMTable.ShipToPort | Nvarchar(20) | Nej | Nej |
| Værdiansættelsesdato | ITMTable.ShipValuationDate | Datetime | Nej | Nej |
| Fragtfirma | ITMTable.ShipVendAccount | Nvarchar(20) | Nej | Nej |
| Fartøj | ITMTable.ShipVesselId | Nvarchar(20) | Nej | **Ja** |
| Eksternt fragt-id | ITMTable.ShipVoyage | Nvarchar(20) | Nej | Nej |

### <a name="number-sequences-for-voyages"></a>Nummerserier for ruter

Den delte nummerserie til ruter styrer fordelingen af rute-id'er.

Den værdi, der overføres til dataenheden som **Rute-id** (`ShipId`), bruges til at identificere en eksisterende post til opdatering. Hvis den pågældende post ikke findes, afhænger funktionaliteten af, om den tildelte nummerserie er konfigureret til at tillade manuel indtastning:

- Hvis manuel indtastning er aktiveret, oprettes der en ny post, der bruger den overførte værdi.
- Hvis manuel indtastning ikke er aktiveret, bruges det næste nummer i den tildelte nummerserie i stedet for den overførte værdi.

Under importsessionen bevares den pladsholderværdi, der importeres som rute-id'et. Denne funktionalitet sikrer, at leveringscontainer- og rutelinjer, der refererer til pladsholderen, medtages i ruten, og at de opdateres, så de afspejler den værdi, der er tildelt fra nummerserien.

### <a name="automatic-cost-transactions"></a>Automatiske omkostningstransaktioner

Automatiske omkostninger kan føjes til en rute fra siden **Automatiske omkostninger** i Microsoft Dynamics 365 Supply Chain Management (**Landingsomkostninger \> Opsætning af efterkalkulation \> Automatiske omkostninger**). Poster til automatiske omkostninger kan også oprettes ved hjælp af dataenheder for omkostningstransaktion for hvert af de omkostningsområder, som landingsomkostninger understøtter.

Automatiske omkostninger, der konfigureres i Supply Chain Management, anvendes på ruten, når en rutelinje oprettes. Der vises ingen omkostninger for posten, før overskriftsposten er tilknyttet linjeoplysninger.

## <a name="shipping-containers-itmcontainersentity"></a>Forsendelsescontainere (ITMContainersEntity)

En forsendelsescontainer repræsenterer en fysisk container, som varer transporteres i. Denne fysiske container kan f.eks. være en fragtcontainer til skibsfragt eller en enkelt palle til luftfragt. Forsendelsescontaineren inkluderer oplysninger på overskriftsniveau, der er relateret til forsendelsescontainer-id'et, forseglingsnummeret og forsendelsescontainertypen. (Forsendelsescontainertypen indeholder dimensionsoplysninger). Denne funktionalitet understøttes af enheden `ITMContainersEntity`. Følgende tabel indeholder de felter og tilknytninger, der udgør denne enhed.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Afrejsedato | ITMContainers.ITMDepartureDate | Datetime | Nej | Nej |
| Dato for lokal transport | ITMContainers.ITMLocalTransportDate | Datetime | Nej | Nej |
| Klokkeslæt for lokal transport | ITMContainers.ITMLocalTransportTime | Int | Nej | Nej |
| Oprindelig fragtrute | ITMContainers.OrigShipId | Nvarchar(20) | Nej | Nej |
| Faktisk vægt | ITMContainers.ShipActualWeight | Numeric(32, 6) | Nej | Nej |
| Mægler adviseret | ITMContainers.ShipBrokerAdvised | Datetime | Nej | Nej |
| Forsendelsescontainer | ITMContainers.ShipContainerId | Nvarchar(20) | **Ja** | **Ja** |
| Forsendelsescontainertype | ITMContainers.ShipContainerTypeId | Nvarchar(20) | Nej | Nej |
| Enhedstype | ITMContainers.ShipContainerUnitTypeId | Nvarchar(10) | Nej | Nej |
| Omregnet til leje | ITMContainers.ShipConvertedToRental | Int | Nej | Nej |
| Kundeaftale | ITMContainers.ShipCustomerAppointment | Datetime | Nej | Nej |
| Afsendelsesdato | ITMContainers.ShipDate | Datetime | Nej | Nej |
| Leveret på lagersted | ITMContainers.ShipDelAtWarehouse | Datetime | Nej | Nej |
| Leveringsinstruktioner | ITMContainers.ShipDeliveryInstructions | Datetime | Nej | Nej |
| Anvendelsesdato for undersøgelsescertifikat | ITMContainers.ShipECAppliedDate | Datetime | Nej | Nej |
| Udløbsdato for undersøgelsescertifikat | ITMContainers.ShipECExpiryDate | Datetime | Nej | Nej |
| Undersøgelsescertifikatnummer | ITMContainers.ShipECNum | Nvarchar(20) | Nej | Nej |
| Modtagelsesdato for undersøgelsescertifikat | ITMContainers.ShipECReceivedDate | Datetime | Nej | Nej |
| Forventet leveringsdato | ITMContainers.ShipEstDlvDate | Datetime | Nej | Nej |
| ETA på forsendelseshavn | ITMContainers.ShipEstPortDate | Datetime | Nej | Nej |
| Forventet lastningsdato | ITMContainers.ShipExpectedLoadingDate | Datetime | Nej | Nej |
| Fra havn | ITMContainers.ShipFromPort | Nvarchar(20) | Nej | Nej |
| Beskrivelse af varer | ITMContainers.ShipGoodsDesc | Nvarchar(60) | Nej | Nej |
| Frigivne varer | ITMContainers.ShipGoodsReleased | Datetime | Nej | Nej |
| GPS-sporingsenhed | ITMContainers.ShipGPSUnit | Nvarchar(30) | Nej | Nej |
| Speditørluftfragtbrev/fragtseddel | ITMContainers.ShipHAWB | Nvarchar(20) | Nej | Nej |
| Fragt | ITMContainers.ShipId | Nvarchar(20) | **Ja** | **Ja** |
| Ruteskabelon | ITMContainers.ShipJourneyId | Nvarchar(20) | Nej | Nej |
| Lokal speditør | ITMContainers.ShipLocalForwarder | Nvarchar(20) | Nej | Nej |
| Mål | ITMContainers.ShipMeasurement | Numeric(32, 6) | Nej | Nej |
| Måleenhed | ITMContainers.ShipMeasurementUnit | Int | Nej | Nej |
| Antal kartoner | ITMContainers.ShipNoOfCartons | Numeric(32, 6) | Nej | Nej |
| Oprindelig fragtseddel er afsendt | ITMContainers.ShipOriginalBOLSebt | Datetime | Nej | Nej |
| Originaldokumenter modtaget. | ITMContainers.ShipOriginalDocsReceived | Datetime | Nej | Nej |
| Vores forseglingsnummer | ITMContainers.ShipOurSealNum | Nvarchar(20) | Nej | Nej |
| Brugt | ITMContainers.ShipPendingUsed | Int | Nej | Nej |
| Status for indkøbsordre | ITMContainers.ShipPurchStatus | Int | Nej | Nej |
| Afkølingstype | ITMContainers.ShipRefrigerationTypeId | Nvarchar(10) | Nej | Nej |
| Kommentarer | ITMContainers.ShipRemarks | Nvarchar(MAX) | Nej | Nej |
| Udlejning | ITMContainers.ShipRental | Int | Nej | Nej |
| Kan returneres | ITMContainers.ShipReturnable | Int | Nej | Nej |
| Fragtstatus | ITMContainers.ShipStatusId | Nvarchar(20) | Nej | Nej |
| Forseglingsnummer for fragtfirma | ITMContainers.ShipTheirSealNum | Nvarchar(20) | Nej | Nej |
| Til havn | ITMContainers.ShipToPort | Nvarchar(20) | Nej | Nej |
| Bekræftelsesdato | ITMContainers.ShipVerificationDate | Datetime | Nej | Nej |
| Fartøj | ITMContainers.ShipVesselId | Nvarchar(20) | Nej | **Ja** |

### <a name="voyage-id-validation"></a>Validering af rute-id

Forsendelsescontainer-id'et styres ikke af en nummerserie. Det er kun entydigt i konteksten af den rute, det bruges i.

Hvis forsendelsescontainerenheden (`ITMContainersEntity`) skal bruges uafhængigt af ruteenheden (`ITMTableEntity`), skal værdien af **Rute-id** (`ShipId`) svare til en eksisterende post i rutetabellen. Ellers mislykkes importen.

Hvis forsendelsescontainerenheden (`ITMContainersEntity`) og ruteenheden (`ITMTableEntity`) bruges som del af samme importsession, skal ruteenheden komme før oprettelsen af en forsendelsescontainer. Ellers kan værdien af **Rute-id** (`ShipId`) ikke valideres korrekt. Hvis der bruges en pladsholderværdi for **Rute-id** (`ShipId`), kan tilknytningen kun oprettes, hvis den samme pladsholder bruges som værdien af **Rute-id** (`ShipId`) i forsendelsescontainerenheden.

### <a name="other-field-validations"></a>Andre feltvalideringer

Følgende tabel viser de felter i tabellen for forsendelsescontainere (`ITMContainers`), der er valideret i forhold til tabellerne til opsætning af Landingsomkostninger. Den viser også dataenheder for Landingsomkostninger, som en speditør kan bruge til at aflæse de eksisterende værdier og sikre, at der modtages gyldige værdier i dit miljø.

| Felt i tabellen ITMContainers | Dataenhed for landingsomkostninger |
|---|---|
| Forsendelsescontainertype | ITMShippingContainerTypeEntity |
| Beskrivelse af varer | ITMGoodsDescriptionEntity |
| Afkølingstype | ITMShippingContainerRefrigerationTypeEntity |

## <a name="folios-itmfolioentity"></a>Folioer (ITMFolioEntity)

En folio repræsenterer en gruppering af varer i en forsendelsescontainer til brug ved toldangivelser. Folioen indeholder oplysninger på overskriftsniveau, der er relateret til toldmægleren, og en beskrivelse af varerne. Denne funktion understøttes af enheden `ITMFolioEntity`. Følgende tabel indeholder de felter og tilknytninger, der udgør denne enhed.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Mægler adviseret | ITMFolioTable.ShipBrokerAdvised | Datetime | Nej | Nej |
| Kontrolnummer for last | ITMFolioTable.ShipCargoControlNumber | Nvarchar(20) | Nej | Nej |
| Kundeaftale | ITMFolioTable.ShipCustomerAppointment | Datetime | Nej | Nej |
| Toldmægler | ITMFolioTable.ShipCustomsBroker | Nvarchar(20) | Nej | Nej |
| Told-id | ITMFolioTable.ShipCustomsId | Nvarchar(60) | Nej | Nej |
| Virksomhed | ITMFolioTable.ShipDataArea | Nvarchar(4) | Nej | **Ja** |
| Leveret på lagersted | ITMFolioTable.ShipDelAtWarehouse | Datetime | Nej | Nej |
| Leveringsinstruktioner | ITMFolioTable.ShipDeliveryInstructions | Datetime | Nej | Nej |
| Dokumenter modtaget | ITMFolioTable.ShipDocReceived | Int | Nej | Nej |
| Forventet leveringsdato | ITMFolioTable.ShipEstDlvDate | Datetime | Nej | Nej |
| ETA på forsendelseshavn | ITMFolioTable.ShipEstPortDate | Datetime | Nej | Nej |
| Eksportør | ITMFolioTable.ShipExporterId | Nvarchar(20) | Nej | Nej |
| Navn | ITMFolioTable.ShipExporterName | Nvarchar(60) | Nej | Nej |
| Databasedato | ITMFolioTable.ShipFolioDate | Datetime | Nej | Nej |
| Folio | ITMFolioTable.ShipFolioId | Nvarchar(20) | **Ja** | **Ja** |
| Fra havn | ITMFolioTable.ShipFromPort | Nvarchar(20) | Nej | Nej |
| Beskrivelse af varer | ITMFolioTable.ShipGoodsDesc | Nvarchar(60) | Nej | Nej |
| Frigivne varer | ITMFolioTable.ShipGoodsReleased | Datetime | Nej | Nej |
| Speditørluftfragtbrev/fragtseddel | ITMFolioTable.ShipHAWB | Nvarchar(20) | Nej | Nej |
| Fragt | ITMFolioTable.ShipId | Nvarchar(20) | Nej | **Ja** |
| Mål | ITMFolioTable.ShipMeasurement | Numeric(32, 6) | Nej | Nej |
| Måleenhed | ITMFolioTable.ShipMeasurementUnit | Int | Nej | Nej |
| Antal kartoner | ITMFolioTable.ShipNoOfCartons | Numeric(32, 6) | Nej | Nej |
| Oprindelig fragtseddel er afsendt | ITMFolioTable.ShipOriginalBOLSebt | Datetime | Nej | Nej |
| Originaldokumenter modtaget. | ITMFolioTable.ShipOriginalDocsReceived | Datetime | Nej | Nej |
| Status for indkøbsordre | ITMFolioTable.ShipPurchStatus | Int | Nej | Nej |
| Kommentarer | ITMFolioTable.ShipRemarks | Nvarchar(MAX) | Nej | Nej |
| Fragtstatus | ITMFolioTable.ShipStatusId | Nvarchar(20) | Nej | Nej |
| Tarifkode | ITMFolioTable.ShipTariffCode | Nvarchar(10) | Nej | Nej |
| Til havn | ITMFolioTable.ShipToPort | Nvarchar(20) | Nej | Nej |
| Værdiansættelsesdato | ITMFolioTable.ShipValuationDate | Datetime | Nej | Nej |
| Bekræftelsesdato | ITMFolioTable.ShipVerificationDate | Datetime | Nej | Nej |
| Leverandørkonto | ITMFolioTable.VendAccount | Nvarchar(20) | Nej | Nej |

### <a name="number-sequences-for-folios"></a>Nummerserier til folioer

Nummerserien til folioer styrer fordelingen af folio-id'er.

Den værdi, der overføres til dataenheden som **Folio-id** (`FolioId`), bruges til at identificere en eksisterende post til opdatering. Hvis den pågældende post ikke findes, afhænger funktionaliteten af, om den tildelte nummerserie er konfigureret til at tillade manuel indtastning:

- Hvis manuel indtastning er aktiveret, oprettes der en ny post, der bruger den overførte værdi.
- Hvis manuel indtastning ikke er aktiveret, bruges det næste nummer i den tildelte nummerserie i stedet for den overførte værdi.

Under importsessionen bevares den pladsholderværdi, der importeres som folio-id'et. Denne funktionalitet sikrer, at rutelinjer, der refererer til pladsholderen, er korrekt tilknyttet, og at de opdateres, så de afspejler den værdi, der er tildelt fra nummerserien.

### <a name="field-validations"></a>Feltvalideringer

Feltet **Beskrivelse af varer** i foliotabellen (`ITMFolioTable`) valideres i forhold til tabellen for opsætning af Landingsomkostninger med samme navn. En speditør kan bruge dataenheden for Landingsomkostninger `ITMGoodsDescriptionEntity` til at aflæse de eksisterende værdier og sikre, at der modtages gyldige værdier i dit miljø.

## <a name="voyage-lines-for-purchase-orders-itmpurchaselineentity"></a>Rutelinjer til indkøbsordrer (ITMPurchaseLineEntity)

Rutelinjen repræsenterer en enkelt indkøbsordrelinje, der medtages i ruten. Denne relation oprettes via felterne **Indkøbsordrenummer** og **Indkøbslinjenummer**. Rutelinjen refererer til hver af de tidligere poster, der er oprettet til ruten, forsendelsescontaineren og folioen. Denne funktion understøttes af enheden `ITMPurchaseLineEntity`. Følgende tabel indeholder de felter og tilknytninger, der udgør denne enhed.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Valuta | ITMLine.CurrencyCode | Nvarchar(3) | Nej | Nej |
| Nettobeløb | ITMLine.LineAmountMST | Numeric(32, 6) | Nej | Nej |
| Indkøbslinjenummer | ITMLine.RefRecId | Numeric(32, 6) | **Ja** | Nej |
| Forsendelsescontainer | ITMLine.ShipContainerId | Int | Nej | Nej |
| Virksomhed | ITMLine.ShipDataArea | Nvarchar(20) | **Ja** | Nej |
| Deklareret antal | ITMLine.ShipDeclaredQty | Nvarchar(4) | Nej | Nej |
| Folio | ITMLine.ShipFolioId | Numeric(32, 6) | Nej | Nej |
| Fragt | ITMLine.ShipId | Nvarchar(20) | **Ja** | Nej |
| Varenummer | ITMLine.ShipItemId | Nvarchar(20) | Nej | Nej |
| Mål | ITMLine.ShipMeasurement | Nvarchar(20) | Nej | Nej |
| Måleenhed | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | Nej | Nej |
| Antal kartoner | ITMLine.ShipNoOfCartons | Int | Nej | Nej |
| Placering | ITMLine.ShipPosition | Numeric(32, 6) | Nej | Nej |
| Quantity | ITMLine.ShipQty | Int | Nej | Nej |
| Indkøbsordrenummer | ITMLine.TransRefId | Numeric(32, 6) | **Ja** | Nej |
| Enhed | ITMLine.UnitId | Int | Nej | Nej |
| Lydstyrke | ITMLine.Volume | Nvarchar(10) | Nej | Nej |
| Tykkelse | ITMLine.Weight | Numeric(32, 6) | Nej | Nej |

## <a name="voyage-lines-for-transfer-orders-itmtransferlineentity"></a>Rutelinjer til overførselsordrer (ITMTransferLineEntity)

Rutelinjen repræsenterer en enkelt overførselsordrelinje, der medtages i ruten. Denne relation oprettes via felterne **Overførselsordrenummer** og **Overførselslinjenummer**. Rutelinjen refererer til hver af de tidligere poster, der er oprettet til ruten, forsendelsescontaineren og folioen. Denne funktion understøttes af enheden `ITMTransferLineEntity`. Følgende tabel indeholder de felter og tilknytninger, der udgør denne enhed.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Valuta | ITMLine.CurrencyCode | Nvarchar(3) | Nej | Nej |
| Nettobeløb | ITMLine.LineAmountMST | Numeric(32, 6) | Nej | Nej |
| Forsendelsescontainer | ITMLine.ShipContainerId | Int | Nej | Nej |
| Virksomhed | ITMLine.ShipDataArea | Nvarchar(20) | **Ja** | Nej |
| Deklareret antal | ITMLine.ShipDeclaredQty | Nvarchar(4) | Nej | Nej |
| Folio | ITMLine.ShipFolioId | Numeric(32, 6) | Nej | Nej |
| Fragt | ITMLine.ShipId | Nvarchar(20) | **Ja** | Nej |
| Varenummer | ITMLine.ShipItemId | Nvarchar(20) | Nej | Nej |
| Mål | ITMLine.ShipMeasurement | Nvarchar(20) | Nej | Nej |
| Måleenhed | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | Nej | Nej |
| Antal kartoner | ITMLine.ShipNoOfCartons | Int | Nej | Nej |
| Placering | ITMLine.ShipPosition | Numeric(32, 6) | Nej | Nej |
| Quantity | ITMLine.ShipQty | Int | Nej | Nej |
| Overførselslinjenummer | ITMLine.TransferLineNumber | Numeric(32, 6) | **Ja** | Nej |
| Overfør ordrenummer | ITMLine.TransRefId | Numeric(32, 6) | **Ja** | Nej |
| Enhed | ITMLine.UnitId | Int | Nej | Nej |
| Lydstyrke | ITMLine.Volume | Nvarchar(10) | Nej | Nej |
| Tykkelse | ITMLine.Weight | Numeric(32, 6) | Nej | Nej |

### <a name="reference-table"></a>Referencetabel

Rutelinjer oprettes via en tilknytning til en åben indgående ordrelinje. Denne linje kan være på en indkøbsordre, eller den kan være modtagelsestransaktionen i en overførselsordre. I feltet `RefTableId` i rutelinjetabellen (`ITMLine`) angives, hvilken ordretype linjen er relateret til, ved at referere til tabelnummeret. Hvis der refereres til bestemte tabelnumre i den tabel, hvor dataene oprettes, fordeles enhederne på basis af disse værdier.

Værdierne for referencetabellen (`RefTableId`) og transaktionstypen (`TransType`) er implicitte i valget af enten indkøbslinjeenheden for Landingsomkostninger eller enheden for overførselslinjen til Landingsomkostninger.

### <a name="validation"></a>Validering

En rutelinje refererer direkte til en rutepost, en forsendelsescontainerpost og en foliopost. Hvis indkøbslinjeenheden (`ITMPurchaseLinesEntity`) eller overførselslinjeenheden (`ITMPurchaseLinesEntity`) bruges uafhængigt af de enheder, der bruges til at oprette disse referenceposter, skal værdierne af **Rute-id** (`ShipId`), **Forsendelsescontainer** (`ShipContainerId`) og **Folio** (`ShipFolioId`) svare til en eksisterende post i de tilsvarende tabeller. Ellers mislykkes importen.

Hvis en af linjeenhederne bruges som del af samme importsession, skal de andre enheder komme før oprettelsen af en rutelinje. Ellers kan værdierne ikke valideres korrekt. Hvis der bruges en pladsholderværdi for rute- eller folionummer, kan tilknytningen kun oprettes, hvis den samme pladsholder bruges til rute- eller folionummeret i rutelinjeenheden.

Hvis indkøbsordre- eller overførselsordrelinjen allerede er tilknyttet en eksisterende rutelinje, oprettes den nye rutelinje ikke. Inden ordrelinjen kan tildeles en ny rute, skal den fjernes fra dens aktuelle rute.

### <a name="order-line-identification"></a>Ordrelinjeidentifikation

Rutelinjer refererer direkte til værdierne af **Post-id** (`RefRecId`), **Lagerdimensions-id** (`InventDimId`) og **Lagertransaktions-id** (`InventTransId`). Disse værdier skal ikke længere medtages, når dataenheden bruges. Ordrelinjenummeret skal nu medtages i stedet. Sammen gør ordrelinjenummeret og ordrenummeret det muligt at identificere hver af disse referenceværdier.

### <a name="voyage-line-quantity"></a>Rutelinjeantal

Da en rutelinje er direkte knyttet til en ordrelinje, kræver den værdi af **Antal** (`ShipQty`) som angives ved hjælp af enheden, at værdierne er ens. Valideringen foretages i forhold til antallet på enten indkøbsordrelinjen eller overførselslinjen. Hvis valideringen mislykkes, behandles posten ikke.

### <a name="calculated-fields"></a>Beregnede felter

De beregnede felter **Vægt** og **Volumen** accepterer de værdier, der modtages via dataenheden. Hvis der ikke er angivet værdier, bruges systemværdierne til at opdatere disse felter, hvis systemværdierne er tilgængelige. For Landingsomkostninger beregnes værdierne på følgende måde:

- *Vægt* = *Antal* × *Varens bruttovægt*
- *Volumen* = *Antal* × (*Varens bruttodybde* × *Varens bruttohøjde* × *Varens bruttobredde*)

## <a name="sequencing"></a>Rækkefølge

På grund af afhængigheder mellem tabellerne, skal ruteposten oprettes først. Rutelinjen kan først oprettes, når ruten, forsendelsescontaineren og folioerne er oprettet.

Hvis du vil oprette en rute uden valideringsadvarsler, skal systemet behandle enhederne i følgende rækkefølge:

1. Ruter (`ITMTableEntity`)
1. Forsendelsescontainere (`ITMContainersEntity`)
1. Folioer (`ITMFolioTableEntity`)
1. Rutelinjer (`ITMPurchaseLinesEntity` eller `ITMTransferLinesEntity`)
