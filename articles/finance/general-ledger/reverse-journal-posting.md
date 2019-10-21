---
title: Tilbageføre kladdebogføring
description: I dette emne beskrives funktioner, der giver mulighed for at tilbageføre bilag fra bilagstransaktionslisten eller fra økonomikladder.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248579"
---
# <a name="reverse-journal-posting"></a>Tilbageføre kladdebogføring

[!include [banner](../includes/banner.md)]

Dette emne indeholder en beskrivelser af Microsoft Dynamics 365 Finance-funktioner, der giver dig mulighed for at tilbageføre en hel kladde eller tilbageføre et eller flere bilag fra listen med bilagstransaktioner, uanset deres oprindelse. 

## <a name="reversing-journals"></a>Tilbageføre kladder

Du kan tilbageføre kladdelinjer enkeltvist. Med tilbageførsel af kladdebogføring kan du også tilbageføre en hel økonomikladde. Sådan tilbagefører du en kladde: 
- Åbn økonomikladden, og filtrer på bogførte kladder
- Klik på menuen Tilbagefør øverst på siden.
- Du kan se det samlede antal bilag og bilagslinjer samt det samlede beløb for de linjer, der tilbageføres
- Vælg Ja for at bruge de eksisterende transaktionsdatoer eller nej for at angive en ny. I nogle tilfælde kan perioden for den oprindelige transaktion være lukket, så du skal angive en ny transaktionsdato for tilbageførslen.
- Hvis du har valgt Nej, skal du angive en transaktionsdato for tilbageførslen. 
- Indtast en kommentar, der skal føjes til den tilbageførte transaktion
- Klik på knappen Tilbagefør

Transaktionerne tilbageføres. 

Hvis antallet af bilagslinjer overstiger 100 linjer, køres tilbageførslen ved hjælp af batchprocessen. Du kan gennemse resultaterne af tilbageførslen ved at få vist kommentarerne i batchjobbet, der blev kørt. Alle fejl vil blive angivet i batchjobbets historik.

Hvis antallet af bilagslinjer er 100 linjer eller mindre, køres tilbageførselsprocessen med det samme. Resultaterne vises i en dialogboks, der viser eventuelle bilag, der ikke kunne tilbageføres, og årsagen til, at de ikke kunne tilbageføres. Klik på OK for at lukke dialogboksen.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Tilbageførsel af bilag fra listen over bilagstransaktioner. 

Du kan også tilbageføre bilag fra **bilagstransaktionslisten** på tværs af alle reskontroer. Derudover kan du tilbageføre mere end ét bilag ad gangen. 

Sådan tilbagefører du et eller flere bilag: 
- Klik på menuen Tilbagefør øverst på siden.
- Du kan se det samlede antal bilag og bilagslinjer samt det samlede beløb for de linjer, der tilbageføres
- Vælg Ja for at bruge de eksisterende transaktionsdatoer eller nej for at angive en ny. I nogle tilfælde kan perioden for den oprindelige transaktion være lukket, så du skal angive en ny transaktionsdato for tilbageførslen.
- Hvis du har valgt Nej, skal du angive en transaktionsdato for tilbageførslen. 
- Indtast en kommentar, der skal føjes til den tilbageførte transaktion
- Klik på knappen Tilbagefør

Transaktionerne tilbageføres. 

Hvis antallet af bilagslinjer overstiger 100 linjer, køres tilbageførslen ved hjælp af batchprocessen. Du kan gennemse resultaterne af tilbageførslen ved at få vist kommentarerne i batchjobbet, der blev kørt. Alle fejl vil blive angivet i batchjobbets historik.

Hvis antallet af bilagslinjer er 100 linjer eller mindre, køres tilbageførselsprocessen med det samme. Resultaterne vises i en dialogboks, der viser eventuelle bilag, der ikke kunne tilbageføres, og årsagen til, at de ikke kunne tilbageføres. Klik på OK for at lukke dialogboksen.

