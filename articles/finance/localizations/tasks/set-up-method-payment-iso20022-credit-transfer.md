---
title: Konfigurere en betalingsmetode for ISO20022-kreditoverførsler
description: Denne procedure viser, hvordan du kan konfigurere kreditorbetalingsmåden for ISO20022-kreditoverførsel eller en anden betalingstype ved hjælp af elektronisk rapportering for at generere en fil.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92bc314e69628f2a287ba7c9a7c2d3d73a0bfd33
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988096"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>Konfigurere en betalingsmetode for ISO20022-kreditoverførsler

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du kan konfigurere kreditorbetalingsmåden for ISO20022-kreditoverførsel eller en anden betalingstype ved hjælp af elektronisk rapportering for at generere en fil. 

Før du udfører denne opgave, skal du konfigurere eksportformatkonfigurationer og betalingskonti.

Denne opgave blev oprettet ved hjælp af DEMF-demodatafirmaet.

Det er den tredje procedure af fem, der illustrerer kreditors betalingsproces ved hjælp af konfigurationer af elektronisk rapportering. Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.

1. Gå til Kreditor > Opsætning af betaling > Betalingsmåder.
2. Brug Quick Filter til at finde poster. Filtrer f.eks. efter feltet Betalingsmåde med værdien "SEPA CT".
3. Klik på Rediger.
4. Vælg "Total" i feltet Periode.
5. Vælg Elektronisk betaling i feltet Betalingstype.
6. Udvid sektionen Filformater.
7. Vælg Ja i feltet Generisk elektronisk indberetning.
8. Skriv eller vælg en værdi i feltet Eksportér formatkonfiguration.
    * Vælg værdien ISO20022-overførsel (DE) på listen. Hvis listen er tom, betyder det, at der ikke er nogen importeret og aktiv eksportformatkonfiguration for kreditorbetaling.  
9. Vælg "Bank" i feltet Kontotype.
10. I feltet Betalingskonto skal du specificere værdierne "DEMF OPER".
11. Klik på Gem.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]