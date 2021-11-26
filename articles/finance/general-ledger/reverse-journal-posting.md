---
title: Tilbageføre kladdebogføring
description: I dette emne beskrives funktioner, der giver mulighed for at tilbageføre bilag fra bilagstransaktionslisten eller fra økonomikladder.
author: kweekley
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb1615312e9fd1786a5a0050dda3e9e9b20fe710
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753772"
---
# <a name="reverse-journal-posting"></a>Tilbageføre kladdebogføring

[!include [banner](../includes/banner.md)]

Dette emne indeholder en beskrivelser af Microsoft Dynamics 365 Finance-funktioner, der giver dig mulighed for at tilbageføre en hel kladde eller tilbageføre et eller flere bilag fra listen med bilagstransaktioner, uanset deres oprindelse. 

Før du kan bruge en af de funktioner, der er beskrevet i dette emne, skal du aktivere dem i systemet. Administratorer kan bruge området **Funktionsstyring** til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:
 - Modul: Finans
 - Funktionsnavn: **Massetilbageførsler for flere dokumenter**

## <a name="reversing-journals"></a>Tilbageføre kladder

Du kan tilbageføre kladdelinjer enkeltvist. Med tilbageførsel af kladdebogføring kan du også tilbageføre en hel økonomikladde. Sådan tilbagefører du en kladde: 

- Filtrer på de bogførte kladder, og åbn **linjevisningen** i kladden.
- Vælg menuen **Tilbagefør** øverst på siden.
- Du kan se det samlede antal bilag og bilagslinjer samt det samlede beløb for de linjer, der tilbageføres.
- Vælg **Ja** for at bruge de eksisterende transaktionsdatoer eller **Nej** for at angive en ny. I nogle tilfælde kan perioden for den oprindelige transaktion være lukket, så du skal angive en ny transaktionsdato for tilbageførslen.
- Hvis du har valgt **Nej**, skal du angive en transaktionsdato for tilbageførslen. 
- Indtast en kommentar, der skal føjes til den tilbageførte transaktion.
- Vælg knappen **Tilbagefør**.

Transaktionerne tilbageføres. 

Hvis antallet af bilagslinjer overstiger 100 linjer, køres tilbageførslen ved hjælp af batchprocessen. Du kan gennemse resultaterne ved at få vist kommentarerne i batchjobbet. Alle transaktioner, der ikke kunne tilbageføres, vises i historikken for batchjobbet.

Hvis antallet af bilagslinjer er 100 linjer eller mindre, køres tilbageførselsprocessen med det samme. Resultaterne vises i en dialogboks med eventuelle bilag, der ikke kunne tilbageføres, og årsagen til, at de ikke kunne tilbageføres. Vælg **OK** for at lukke dialogboksen.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Tilbageførsel af bilag fra listen over bilagstransaktioner. 

Du kan også tilbageføre bilag fra **bilagstransaktionslisten** på tværs af alle reskontroer. Derudover kan du tilbageføre mere end ét bilag ad gangen. 

Sådan tilbagefører du et eller flere bilag: 

- Vælg menuen **Tilbagefør hele kladderullelisten** øverst på siden.
- Du kan se det samlede antal bilag og bilagslinjer samt det samlede beløb for de linjer, der tilbageføres.
- Vælg **Ja** for at bruge de eksisterende transaktionsdatoer eller **Nej** for at angive en ny. I nogle tilfælde kan perioden for den oprindelige transaktion være lukket, så du skal angive en ny transaktionsdato for tilbageførslen.
- Hvis du har valgt **Nej**, skal du angive en transaktionsdato for tilbageførslen. 
- Indtast en kommentar, der beskriver tilbageførselstransaktionen.
- Vælg knappen **Tilbagefør**.

Transaktionerne tilbageføres. 

Hvis antallet af bilagslinjer overstiger 100, køres tilbageførslen ved hjælp af batchprocessen. Du kan gennemse resultaterne ved at få vist kommentarerne i batchjobbet. Alle transaktioner, der ikke kunne tilbageføres, noteres i historikken for batchjobbet.

Hvis antallet af bilagslinjer er 100 linjer eller derunder, køres tilbageførselsprocessen med det samme. Resultaterne vises i en dialogboks med eventuelle bilag, der ikke kunne tilbageføres, og årsagen hertil. Vælg **OK** for at lukke dialogboksen.

Transaktioner kan kun tilbageføres, hvis de opfylder forretningsreglerne for tilbageførsel af dem. Kreditorbetalinger kan ikke tilbageføres ved hjælp af den funktion, der er beskrevet i dette emne. Kreditorbetalinger skal tilbageføres ved at følge trinnene i [Tilbageføre en kreditorbetaling](../accounts-payable/reverse-vendor-payment.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
