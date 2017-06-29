---
title: Opdater den sammensatte enhed Bankkladde
description: "Brug følgende trin til at føje det ekstra felt BankTransactionType til den sammensatte BankJournalEntity."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 43413aad9d537e518f7276ccab11ce01d23cf13f
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="update-the-bank-journal-composite-entity"></a>Opdater den sammensatte enhed Bankkladde

[!include[banner](../includes/banner.md)]


Brug følgende trin til at føje det ekstra felt BankTransactionType til den sammensatte BankJournalEntity.

Brug følgende trin til at føje det ekstra felt BankTransactionType til den sammensatte BankJournalEntity.

1.  Kompilerer og synkroniserer følgende sammensatte bankkladdeobjekter, objekter, og midlertidige tabeller:
    -   Sammensat enhed\\BankJournalEntity
    -   Enhed\\BankJournalHeaderEntity
    -   Enhed\\BankJournalLineEntity
    -   Tabel\\BankJournalHeaderStaging
    -   Tabel\\BankJournalLineStaging

2.  Datastyring\\dataprojekter
    -   Vis typen **Banktransaktion**på **Kildedata-**layout.
        -   Kildedataformat = XML-element
        -   Enhedsnavn = Bankkladde
        -   Upload datafilen = ny version af SampleBankJournalCompositeEntity.xml
        -   Klik på **Ja** for at overskrive den eksisterende fil.
        -   Klik på **Ja** for at oprette en tilknytning fra grunden.
        -   Kontrollér, at bankposteringstypen er tilknyttet.
            -   Klik på **Vis tilknytning** på linjeenhed.
            -   Kontrollér, at bankposteringstypen er knyttet fra Kilde til Midlertidig.

3.  Importér det nye udtog.





