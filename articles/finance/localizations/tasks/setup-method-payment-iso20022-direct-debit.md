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
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2cd5c174b0f3e3e15678513cecade020705beda
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982123"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a>Opret betalingsmåde til ISO20022 direkte debet

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]