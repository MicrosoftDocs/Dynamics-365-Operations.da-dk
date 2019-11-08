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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8bb54864c8d0a57510b4d47b00aed60c5be95512
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174804"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>Konfigurere en betalingsmetode for ISO20022-kreditoverførsler

[!include [task guide banner](../../includes/task-guide-banner.md)]

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
