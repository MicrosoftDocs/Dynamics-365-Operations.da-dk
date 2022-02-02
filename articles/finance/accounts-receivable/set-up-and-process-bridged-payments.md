---
title: Konfigurere og behandle mellembetalinger
description: I dette emne beskrives, hvordan du kan konfigurere og behandle kunders mellembetalinger. En mellembetaling er en betaling, der bogføres i finans i to trin.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, VendPaymMode, LedgerJournalTable, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1418e573f34fadcf0bebc7232d847ee7e9768b
ms.sourcegitcommit: 5bfd6511d710deb539b4030eb0e9c48d25513595
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/19/2022
ms.locfileid: "8014034"
---
# <a name="set-up-and-process-bridged-payments"></a>Konfigurere og behandle mellembetalinger

[!include [banner](../includes/banner.md)]

En mellembetaling er en betaling, der bogføres i finans i to trin. Denne metode bruges typisk, når betalingsmåden er angivet til **Bank**, og du kun skal bogføre transaktioner på bankkontoen, når transaktionen er clearet i banken. Du kan dog også bruge den til en finanskonto. I dette tilfælde flytter systemet beløbet fra én hovedkonto til en anden hovedkonto, når mellemkonteringen behandles.

Du kan oprette mellembetalinger fra enten Kreditor eller Debitor. Selvom dette emne forklarer, hvordan du kan konfigurere mellemkontering for Debitor, er trinnene for kreditortransaktioner næsten ens.

## <a name="set-up-bridging-posting"></a>Konfigurere mellemkontering

Hvis du vil bruge mellemkontering, skal du konfigurere en eller flere betalingsmåder, så de bruger **Mellemkontering** som metode. Du skal derefter vælge en mellemkonto.

1. Gå til **Debitor &gt; Opsætning af betaling &gt; Betalingsmetoder**.
2. Vælg en eksisterende betalingsmåde, som du vil aktivere mellemkontering for. Du kan også oprette en ny betalingsmåde.
3. Markér afkrydsningsfeltet **Mellemkontering**.
4. I feltet **Mellemkonto** skal du vælge den hovedkonto, som betalinger skal bogføres på, før de cleares på bankkontoen.
5. Luk siden.

## <a name="process-and-transfer-bridging-posting"></a>Behandle og overføre mellemkontering

Følg disse trin for at oprette og behandle processen for mellemkontering.

1. Gå til **Debitor &gt; Betalinger &gt; Debitorbetalingskladde**.
2. Vælg **Ny** for at oprette en kladde.
3. Vælg et navn i feltet **Navn**.
4. Tilføj linjer i debitorbetalingskladden, og vælg den betalingsmåde, der er konfigureret til mellemkontering.
5. Bogfør kladden. Posteringerne bogføres på den hovedkonto, som du valgte i feltet **Mellemkonto** i den foregående procedure.

Når posteringerne er clearet i banken, og du vil overføre betalingen fra mellemkontoen til den betalingskonto, der er angivet for betalingsmåden, skal du følge disse trin.

1. Gå til **Finans &gt; Kladdeposteringer &gt; Finanskladder**.
2. Vælg **Ny** for at oprette en kladde.
3. Vælg et navn i feltet **Navn**.
4. Vælg **Linjer** for at åbne kladdeoplysningerne.
5. Vælg **Funktioner &gt; Vælg transaktioner med mellempostering**.
6. Markér alle betalinger, der er clearet, og vælg derefter **Acceptér**.
7. Bogfør kladden.
