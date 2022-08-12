---
title: Opdatere den sammensatte bankkladdeenhed
description: Denne artikel indeholder en liste over de trin, der skal bruges til at føje det ekstra felt BankTransactionType til den sammensatte BankJournalEntity.
author: angelad116
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f8bf3bbcbd8036015757799a2e58b23fd9bd2b38
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151604"
---
# <a name="update-the-bank-journal-composite-entity"></a>Opdatere den sammensatte bankkladdeenhed

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en liste over de trin, der skal bruges til at føje det ekstra felt BankTransactionType til den sammensatte BankJournalEntity.

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
