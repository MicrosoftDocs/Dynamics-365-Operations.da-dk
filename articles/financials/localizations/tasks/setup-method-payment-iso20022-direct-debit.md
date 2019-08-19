---
title: Opret betalingsmåde til ISO20022 direkte debet
description: Denne procedure viser, hvordan du kan konfigurere kundebetalingsmåden for ISO20022 Direct Debit eller en anden betalingstype ved hjælp af elektronisk rapportering.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d3c6d8157803e0a8d33520a0cd64fb725e8c9a3
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848641"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a>Opret betalingsmåde til ISO20022 direkte debet

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du kan konfigurere kundebetalingsmåden for ISO20022 Direct Debit eller en anden betalingstype ved hjælp af elektronisk rapportering. 



Før du udfører denne opgave, skal du konfigurere eksportformatkonfigurationer og betalingskonti.



Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF.



Det er den tredje procedure af fem, der illustrerer kundens betalingsproces ved hjælp af konfigurationer af elektronisk rapportering.

1. Gå til Debitor > Betalingsopsætning > Betalingsmetoder.
2. Brug Quick Filter til at finde poster. Filtrer f.eks. efter feltet Betalingsmåde med værdien "ELECTRONIC".
3. Klik på Rediger.
4. I feltet Betalingskonto skal du specificere værdierne "DEMF OPER".
5. Udvid sektionen Filformater.
6. Vælg Ja i feltet Generisk elektronisk indberetning.
7. Skriv eller vælg en værdi i feltet Eksportér formatkonfiguration.
    * Vælg ISO20022 Direct debit (DE) på listen.  Hvis listen er tom, betyder det, at der ikke er nogen importeret og aktiv eksportformatkonfiguration for kundebetaling.  
8. Vælg Ja i feltet Kræv bemyndigelse.
    * Vælg parameteren Kræv bemyndigelse for formater for debitorbetalinger, der kræver, at der medtages bemyndigelse i betalingsmeddelelsen, f.eks. SEPA Direct Debit.  
9. Klik på Gem.

