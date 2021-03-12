---
title: Bogfør kladdeposteringer for transaktionsjusteringen i aktivleasing
description: I dette emne beskrives den funktion, du kan bruge til at overføre en leasingaftales portefølje til de nye regnskabsstandarder for leasing, Accounting Standards Codification Topic 842 (ASC 842) og International Financial Reporting Standard 16 (IFRS 16).
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 51ae41e22507d77f32b8b0f4685cce797fd19cff
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969547"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a>Bogfør kladdeposteringer for transaktionsjusteringen i aktivleasing

[!include [banner](../includes/banner.md)]

I dette emne beskrives de funktioner, du kan bruge til at overføre en leasingaftales oversigt til de nye kontostandarder for leasing: Accounting Standards Codification Topic 842 (ASC 842), som er standarden i Generally Accepted Accounting Principles i USA (US GAAP) og International Financial Reporting Standard 16 (IFRS 16).

Du kan finde flere oplysninger om, hvordan du konfigurerer et kartotek til overgangen til de nye standarder, i [Konfigurere leasingkartoteker](set-up-lease-books.md).

Når du opretter en kladdepostering for en overgangsregulering, genereres der en kladdepost. Denne post afspejler balancevirkningen for registrering af leasingaftaler under de nye standarder på den pågældende dato. Den relevante aktivkonto debiteres for dette beløb på denne dato, og passivkontoen krediteres. Differencen er enten debiteret eller krediteret overførte tillæg.

Hvis du vil bogføre en overgangsjustering i overensstemmelse med de nye regnskabsstandarder, skal du følge disse trin.

1. På siden **Leasingoversigt** skal du vælge en leasingaftale, og derefter **Kartoteker**.
2. Vælg **Betalingsplan** i kartoteket.
3. Vælg **Bekræft** i dialogboksen **Betalingsplan**. Luk derefter dialogboksen.
4. Vælg **Overgangsjustering**.

    > [!NOTE]
    > Der kan kun oprettes en overgangsjustering for leasingkartoteker, der er tildelt et kartotek, hvor feltet **Overgangskartoteket** er tilgængeligt. Hvis værdien i feltet **Leasingaftale påbegyndes** er senere end overførselsdatoen, opdateres værdien i feltet **Overgangsjustering** ikke.

5. Hvis du vil se kladdeposten, skal du vælge **Aktivleasingkladde**.
6. Vælg den nye kladde, og vælg derefter **Bogfør**.
