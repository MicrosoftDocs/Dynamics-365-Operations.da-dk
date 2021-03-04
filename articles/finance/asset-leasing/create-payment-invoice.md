---
title: Oprette betalingsfakturaer
description: Dette emne forklarer, hvordan du opretter månedlige leasingfakturaer. Du kan oprette fakturaer for individuelle leasingaftaler, eller du kan bruge en batchproces til at oprette dem for flere leasingaftaler.
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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 32618814d00cb1e1f1082169a64b187cce1e76b4
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441747"
---
# <a name="create-payment-invoices"></a>Oprette betalingsfakturaer

[!include [banner](../includes/banner.md)]

Du kan oprette månedlige fakturaer for individuelle leasingaftaler, eller du kan bruge en batchproces til at oprette dem for flere leasingaftaler. Følgende procedure viser, hvordan du opretter en individuel leasingbetalingspost, når parameteren **Betal til kreditor** på siden **opsætning af leasingkartotek** er aktiveret.

1. På siden **Leasingoversigt** skal du vælge en leasingaftale, og derefter **Kartoteker \> Betalingsplan**.
2. Vælg den betaling, der skal foretages, og vælg derefter **Opret kladde**. Du får vist en meddelelse, der angiver, at der er oprettet en kladde mod den valgte betaling.
3. Vælg **Fakturakladder**, og vælg derefter den faktura, der skal betales.
4. Gennemse kladdeposteringen på fanen **Linjer**, før du bogfører den til Finanskladde.

    > [!NOTE]
    > Som standard vil de kreditorfakturalinjer, der oprettes, bruge kreditorposteringsprofilen fra siden **Kreditorparametre**.

5. Vælg den korrekte kladde, og vælg derefter den faktura, der skal betales.

    I dette eksempel er parameteren **Betal til kreditor** i leasingkartoteket aktiveret. Fakturaen vil derfor være i fakturakladden. Afsnittet **Oversigt** indeholder en oversigt over kladdeposteringen, og afsnittet **Linjer** indeholder oplysninger om de faktiske kladdelinjer.

    > [!NOTE]
    > Hvis parameteren **Betal til kreditor** er deaktiveret, vises betalingskladdeposterne på siden **Aktivleasing** for leasingkartoteket, og systemet opretter en post for aktivleasing i stedet for en faktura. Betalingsposten for leasing bogføres til det kladdenavn, der er angivet i feltet **Månedlig leasingkladde**.

6. Når posteringen er bogført, kan du få vist posteringsoplysningerne og bære ansvarsværdien for leasingforpligtelserne ved at vælge **Ansvarsposteringer** i leasingkartoteket.

    Afkrydsningsfeltet i betalingsplanen **Kladde bogført** er markeret i betalingsplanen, og linjen viser fakturakladdenummeret. Når en betalingskladde og en post for den pågældende kladde er oprettet, skal du tilbageføre posten, før den kan oprettes igen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]