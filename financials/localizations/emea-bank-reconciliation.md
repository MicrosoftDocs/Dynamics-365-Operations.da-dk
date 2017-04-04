---
title: "Bank opgørelse og betaling afstemning oversigt for EU"
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

# <a name="bank-statement-and-payment-reconciliation-overview-for-the-eu"></a>Bank opgørelse og betaling afstemning oversigt for EU

Dette emne indeholder en oversigt over de funktioner, du kan bruge til at afstemme betalingsoplysninger fra banker i formater, der bruges af europæiske lande.

Du kan importere posteringer fra banker og udligner disse posteringer mod eksisterende poster i Microsoft Dynamics 365 for operationer. I Europa, kan du gøre dette i følgende scenarier:

-   Import af bankkontoudtog
-   Import af betalinger.
-   Import af return filer.

## <a name="bank-statements"></a>Bankkontoudtog
A *bank sætningen* eller *konto sætningen* er en oversigt over de finansielle transaktioner, der er opstået i en given periode på en bankkonto, som indehaves af en virksomhed med en finansiel institution. Du kan importere et bankkontoudtog i Dynamics 365 for operationer. Det er vigtigt at udligne importerede posteringer med eksisterende transaktioner samt kontrollere åbne- og slutdatoer saldoen på bankkontiene. Følgende liste indeholder de understøttede formater i Europa.

-   Avanceret afstemning Europa-filformater. Yderligere oplysninger finder du [Avanceret oversigt over afstemning af bank](../cash-bank-management/advanced-bank-reconciliation-overview.md).
-   ISO 20022 camt.053 meddelelsen filen bankkontoudtogsformat
-   Filformat til CODA-bank-sætning. Yderligere oplysninger finder du [CODA-bankkontoudtog](emea-bel-coda-bank-statement-import.md).

## <a name="customer-and-vendor-payments-import-and-return-messages"></a>Debitor- og kreditorbetalinger importere og returnere meddelelser
Ud over et bankkontoudtog kan banker give bestemte meddelelser, der indeholder oplysninger om debitor- og kreditorbetalinger, som kan importeres til Dynamics 365 for operationer og afstemmes med debitor-og kreditortransaktioner. Når en virksomhed skal modtage oplysninger om indgående betalinger debitorposteringer fra banken, kan import-formater bruges. Virksomheder, der bruger direkte debitering og pengeoverførsel, kan returnere meddelelser modtages for at opdatere status for betalinger, der tidligere blev eksporteret. Forskellen mellem import formater og returnere formater er, at returnerer henvender primært for at opdatere allerede oprettet kladdelinjer til debitorbetalinger (de kan oprettes når direkte debitering eller kreditering overførsel blev startet) i stedet for at oprette nye linjer. Nogle komplekse import formater kan også indeholde returværdien scenarier. Følgende eksempel viser, hvordan denne fordeling bør gennemføres.

##### <a name="import-formats"></a>Importere formater

-   ISO 20022 camt.054 bank meddelelse
-   [Redskaber importere formater](emea-nor-nets-import-format.md) -kompleks funktion til norske betalingsformater
-   Importere ESR debitorbetalinger
-   Importere betalingsformater for Sverige - BankGirot Max og BankGirot OCR-formater

##### <a name="return-formats"></a>Returnere formater

-   ISO 20022 pain.002 betaling statusrapport
-   (DNK) BetalingsserviceBasis-returformat – Returner format til kunden Betalingsservice eksportformat
-   [Importere betalingsformater for Sverige](emea-swe-payment-formats-import.md) -Bankgirot Autogiro returnerer
-   (SVENSK) BankGirot tilbage – kreditorbetalinger returnere format, som svarer til eksportformatet Bankgirot

