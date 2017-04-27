---
title: Oversigt over bankkontoudtog og betalingsafstemning for EU
description: "Dette emne indeholder en oversigt over de funktioner, du kan bruge til at afstemme betalingsoplysninger fra banker i formater, der bruges af europæiske lande."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankAccountTable, CustPaymMode, VendPaymMode
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267994
ms.assetid: 2bfb8ecc-e850-43cb-9a96-deb11716a391
ms.search.region: Belgium, Norway, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 22d93d7b3618d4f5931c6a7e39d681173734b0b9
ms.lasthandoff: 03/31/2017


---

# <a name="bank-statement-and-payment-reconciliation-overview-for-the-eu"></a>Oversigt over bankkontoudtog og betalingsafstemning for EU

[!include[banner](../includes/banner.md)]


Dette emne indeholder en oversigt over de funktioner, du kan bruge til at afstemme betalingsoplysninger fra banker i formater, der bruges af europæiske lande.

Du kan importere posteringer fra banker i Microsoft Dynamics 365 for Operations og udligner dem mod eksisterende poster. I Europa kan du gøre dette i følgende scenarier:

-   Ved import af bankkontoudtog
-   Ved import af betalinger
-   Ved import af returfiler.

## <a name="bank-statements"></a>Bankkontoudtog
Et *bankkontoudtog* eller *kontoudtog* er en oversigt over de finansielle transaktioner, der er sket i en given periode på en bankkonto, som indehaves af en virksomhed hos et pengeinstitut. Du kan importere et bankkontoudtog i Dynamics 365 for Operations. Det er vigtigt at udligne importerede posteringer med eksisterende posteringer samt kontrollere start- og slutsaldi på bankkontiene. Følgende liste indeholder de understøttede formater i Europa.

-   Europæiske filformater til avanceret bankafstemning. Du kan finde flere oplysninger under [Oversigt over avancerede bankafstemninger](../cash-bank-management/advanced-bank-reconciliation-overview.md).
-   Filformat for ISO 20022 camt.053-bankkontomeddelelse
-   Filformat for CODA-bankontoudtog. Du kan finde flere oplysninger under [CODA-bankkontoudtog](emea-bel-coda-bank-statement-import.md).

## <a name="customer-and-vendor-payments-import-and-return-messages"></a>Import- og returmeddelelser for debitor- og kreditorbetalinger
Ud over et bankkontoudtog kan banker levere bestemte meddelelser, der indeholder oplysninger om debitor- og kreditorbetalinger, som kan importeres i Dynamics 365 for Operations og afstemmes med debitor-og kreditortransaktioner. Når en virksomhed skal modtage oplysninger om posteringer af indgående debitorbetalinger fra banken, kan importformaterne bruges. For virksomheder, der bruger direkte debitering og pengeoverførsel, kan returmeddelelser modtages til opdatering af status for betalinger, der blev eksporteret tidligere. Forskellen mellem importformater og returformater er, at formålet med returneringer primært er at opdatere allerede oprettede betalingskladdelinjer (de kan være oprettet, da direkte debitering eller kreditoverførsler blev startet) i stedet for at oprette nye linjer. Nogle komplekse importformater kan også omfatte returscenarier. Følgende eksempel viser, hvordan denne fordeling bør implementeres.

##### <a name="import-formats"></a>Importformater

-   ISO 20022 camt.054 bankmeddelelse
-   [Nets importformat](emea-nor-nets-import-format.md) - Kompleks funktion til norske betalingsformater
-   Importere ESR-debitorbetalinger
-   Importbetalingsformater for Sverige - BankGirot Max og BankGirot OCR-formater

##### <a name="return-formats"></a>Returformater

-   ISO 20022 pain.002 betalingsstatusrapport
-   (DNK) BetalingsserviceBasis-returformat – Returformat for kundens Betalingsservice eksportformat
-   [Importbetalingsformater for Sverige](emea-swe-payment-formats-import.md) -Bankgirot Autogiro-returneringer
-   (SVENSK) BankGirot-returnering – Returformat for kreditorbetalinger, som svarer til eksportformatet Bankgirot



