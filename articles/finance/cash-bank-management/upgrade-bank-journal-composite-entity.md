---
title: Opdater den sammensatte enhed Bankkladde
description: Brug følgende trin til at føje det ekstra felt BankTransactionType til den sammensatte BankJournalEntity.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7e265915cf3f53a8243788b50a9374d521efbbae
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819596"
---
# <a name="update-the-bank-journal-composite-entity"></a>Opdater den sammensatte enhed Bankkladde

[!include [banner](../includes/banner.md)]

Brug følgende trin til at føje det ekstra felt BankTransactionType til den sammensatte BankJournalEntity.

Brug følgende trin til at føje det ekstra felt BankTransactionType til den sammensatte BankJournalEntity.

1.  Kompilerer og synkroniserer følgende sammensatte bankkladdeobjekter, objekter, og midlertidige tabeller:
    -   Sammensat enhed\\BankJournalEntity
    -   Enhed\\BankJournalHeaderEntity
    -   Enhed\\BankJournalLineEntity
    -   Tabel\\BankJournalHeaderStaging
    -   Tabel\\BankJournalLineStaging

2.  Datastyring\\dataprojekter
    -   Vis typen **Banktransaktion** på **Kildedata-** layout.
        -   Kildedataformat = XML-element
        -   Enhedsnavn = Bankkladde
        -   Upload datafilen = ny version af SampleBankJournalCompositeEntity.xml
        -   Klik på **Ja** for at overskrive den eksisterende fil.
        -   Klik på **Ja** for at oprette en tilknytning fra grunden.
        -   Kontrollér, at bankposteringstypen er tilknyttet.
            -   Klik på **Vis tilknytning** på linjeenhed.
            -   Kontrollér, at bankposteringstypen er knyttet fra Kilde til Midlertidig.

3.  Importér det nye udtog.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]