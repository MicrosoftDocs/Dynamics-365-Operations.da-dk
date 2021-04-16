---
title: Overføre reskontro til Finans
description: Dette emne beskriver egenskaber i Microsoft Dynamics 365 Finance, der er relateret til processen for overførsel af reskontro i finansmodulet.
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: d43b96176c51d12c35383da75bf65a1ad92f84c6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815278"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Overføre reskontro til Finans

[!include [banner](../includes/banner.md)]

Dette emne indeholder en beskrivelse af de egenskaber i Microsoft Dynamics 365 Finance, der er knyttet til reglerne for overførsel af batches for kladdeposteringer af reskontro.

I version 8.1 blev der foretaget ændringer for at tillade overførsel af regler, der udfasede den **synkrone** indstilling. Du kan finde flere oplysninger under [Fjernede eller udfasede funktioner for Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).

Følgende indstillinger er tilgængelige for overførsel af reskontrobatches. 

 - Asynkron – Denne indstilling planlægger straks overførslen af reskontroregnskabsposter til Finans. Finansbilaget registreres, så snart ressourcer der er ledige ressourcer til at behandle denne anmodning på serveren. 

- Planlagt batch – Denne indstilling vil tilføje de reskontroregnskabsposter, der overføres til behandlingskøen i finansmodulet, hvor posterne skal behandles i den modtagne ordre. Finansbilaget registreres på det planlagte tidspunkt, hvis der er ledige ressourcer til at behandle dette batchjob på serveren. 
 
I version 10.0.8 er der sket forbedringer af ydeevnen for indstillingen Asynkron. Denne funktion er aktiveret under funktionsnavnet **Overførsel af reskontro til Finans med performance-optimering**. 
 
Denne funktionalitet forbedrer overførslen af data fra reskontro til Finans. Processen kan være mere effektiv, og den grupperer sæt med mindre transaktioner, der skal overføres. Det giver en mere effektiv brug af batchserveren. Denne funktionalitet kræver, at batchserveren konfigureres, er online og fungerer, for at den asynkrone overførselsindstilling kan fungere. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]