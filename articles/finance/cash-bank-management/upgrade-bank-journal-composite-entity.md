---
title: Opdater den sammensatte enhed Bankkladde
description: Brug følgende trin til at føje det ekstra felt BankTransactionType til den sammensatte BankJournalEntity.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 974d6b3b11df92debdec26860fd9eea00a9f2313
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188021"
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



