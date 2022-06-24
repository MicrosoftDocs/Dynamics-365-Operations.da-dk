---
title: Overførsel af reskontro til finans
description: Denne artikel beskriver egenskaber, der er relateret til processen for overførsel af reskontro i Finans.
author: RyanCCarlson2
ms.date: 12/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 6d9b40409089e2050dc28c21040069107b766aa0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871240"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Overførsel af reskontro til finans

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en beskrivelse af de egenskaber , der er knyttet til reglerne for overførsel af batches for reskontrokladdeposter.

I version 8.1 blev der foretaget ændringer for at tillade overførsel af regler, der udfasede den **synkrone** indstilling. Yderligere oplysninger finder du i [Fjernede eller forældede funktioner til Finans og drift](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

Følgende indstillinger er tilgængelige for overførsel af reskontrobatches:

- **Asynkron** – Overførsel af reskontroregnskabsposter til finans bliver planlagt med det samme. Finansbilaget registreres, så snart ressourcer, der er tilgængelige for behandling af anmodningen på serveren.
- **Planlagt batch** – De reskontroregnskabsposter, der skal overføres, føjes til behandlingskøen i Finans. Posterne i køen behandles i den rækkefølge, de modtages i. Hvert finansbilag opdaterer konti på det planlagte tidspunkt, hvis der er tilgængelige ressourcer til behandling af batchjobbet på serveren.

I version 10.0.8 er der sket forbedringer af ydeevnen for indstillingen **Asynkron**. Denne funktion er aktiveret under funktionsnavnet **Overførsel af reskontro til Finans med performance-optimering**.

Funktionaliteten for asynkron overførsel af reskontrobatch forbedrer overførslen af data fra reskontroen til finans. Ved at gruppere sæt mindre transaktioner og overføre transaktionerne i grupper behandler funktionaliteten transaktionerne mere effektivt. Når transaktioner grupperes, anvendes batchserverens ressourcer mere effektivt.

Asynkron overførsel af reskontrobatches kræver, at batchserveren er konfigureret, online og fungerer, da der oprettes batchopgaver til strakskørsel på batchserveren. Når funktionen **Overførsel af reskontro til Finans med performance-optimering** er aktiveret, skal systembatchjobbet **Procesautomatisering** med navnet **Systemjob til forespørgsler på procesautomatisering** også være aktiveret. Du kan finde flere oplysninger under [Procesautomatisering](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

Effektivitetsændringen på batchniveau bruger et enkelt tilbagevendende batchjob for alle juridiske enheder i systemet. Under kørslen oprettes der et nyt batchjob til behandling af de krævede poster, der endnu ikke er overført. Flere indstillinger kan styres fra siden **Procesautomatisering** i systemadministrationen. På denne side kan du redigere baggrundsprocessen, ændre frekvensen og definere en inaktiv periode.

Du kan finde flere oplysninger om procesautomatisering i [Procesautomatisering](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
