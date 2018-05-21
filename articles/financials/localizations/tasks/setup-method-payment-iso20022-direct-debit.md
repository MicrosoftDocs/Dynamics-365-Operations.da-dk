--- 
title: Konfigurere en betalingsmetode for ISO20022 Direct Debit
description: "Denne procedure viser, hvordan du kan konfigurere kundebetalingsmåden for ISO20022 Direct Debit eller en anden betalingstype ved hjælp af elektronisk rapportering."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 3a884837ab0b5a1f4211532969619b54206bbef4
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-method-of-payment-for-iso20022-direct-debit"></a>Konfigurere en betalingsmetode for ISO20022 Direct Debit

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


