---
title: Rette oplysninger om lagersproing
description: Denne procedure fører dig gennem processen med at oprette og bogføre en lageroverførselskladde for at korrigere lagersporingsoplysninger.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5155ada23fe4f559c79964e6bd10d86712009d1d
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145759"
---
# <a name="correct-inventory-tracking-information"></a>Rette oplysninger om lagersproing

[!include [banner](../../includes/banner.md)]

Denne procedure fører dig gennem processen med at oprette og bogføre en lageroverførselskladde for at korrigere lagersporingsoplysninger. I dette eksempel vil vi opdatere oplysningerne for en batchstyret vare ved at ændre en forkert registreret batch til en anden batch. Du kan gennemgå denne procedure i demodatafirmaet USPI eller bruge dine egne data. Hvis du bruger dine egne data, skal du have en vare, der er batchaktiveret, og den må ikke være placeringsstyret. Du skal også have oprettet et lagerkladdenavn for lageroverførsler. Disse opgaver udføres normalt af en lagermedarbejder.


## <a name="create-an-inventory-transfer-journal"></a>Oprette en lageroverførselskladde
1. Gå til Overfør.
2. Klik på Ny.
3. Indtast eller vælg en værdi i feltet Navn.
4. Klik på OK.

## <a name="create-journal-lines"></a>Oprette journallinjer
1. Klik på Ny.
2. Indtast eller vælg en værdi i feltet Varenummer.
    * Hvis du bruger USPI, skal du vælge vare M5003.  
3. Angiv et tal i feltet Antal.
4. Klik på fanen Lagerdimensioner.
5. Indtast eller vælg en værdi i feltet Batchnummer.
6. Indtast eller vælg en værdi i feltet Lokation.
7. Indtast eller vælg en værdi i feltet Lagersted.
8. Indtast eller vælg en værdi i feltet Batchnummer.

## <a name="post-the-journal"></a>Bogfør kladden
1. Klik på Bogfør.
2. Klik på OK.

## <a name="check-tracing-information"></a>Kontrollere sporingsoplysninger
1. Klik på lager.
2. Klik på Spor.
3. Klik på OK.
    * Ved hjælp af disse sporingsoplysninger kan du spore, hvilken batch du rettede lageret fra.  Du kan også bruge siden Varesporing til at se disse oplysninger.  
4. Luk siden.

## <a name="check-inventory-transactions"></a>Kontrollere lagerposteringer
1. Klik på lager.
2. Klik på Transaktioner.
    * Her kan du se de posteringer, der blev oprettet, da du bogførte kladden.   

