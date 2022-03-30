---
title: Konfigurere betalingsplaner med skatteallokering
description: Dette emne forklarer, hvordan du konfigurerer betalingsplaner med fordeling af kildeskat (TDS – Tax Deducted at Source).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 31ecf2e6fa4d3d37c3d5332dc1d5592bf1a99bad
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2022
ms.locfileid: "8408084"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>Konfigurere betalingsplaner med skatteallokering

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du konfigurerer betalingsplaner med fordeling af kildeskat (TDS – Tax Deducted at Source).

1. Gå til **Kreditor \> Betalingsopsætning \> Betalingsplaner**.

    [![Siden Betalingsplaner.](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)

2. Vælg **Ny** i handlingsruden for at oprette en betalingsplan, og angiv de krævede oplysninger.
3. Vælg den metode, der skal bruges til at fordele betalingen for betalingsplanen, i feltet **Fordeling**:

    - Sum
    - Fast beløb
    - Fast antal
    - Specificeret

    Feltet **Fordeling af A-skat** viser skattefordelingsmetoden for betalingsplanen. Hvis du vælger **Total** i feltet **Fordeling**, angives feltet **Fordeling af A-skat** automatisk til **Total**. Hvis du vælger **Fast beløb**, **Fast antal** eller **Angivet** i feltet **Fordeling**, angives feltet **Fordeling af A-skat** automatisk til **Proportionalt**.

    > [!NOTE]
    > Hvis feltet **Fordeling af A-skat** er angivet til **Total**, beregnes betalingsraterne baseret på det bruttobeløb, som omfatter skattebeløbet. Hvis feltet **Fordeling af A-skat** er angivet til **Proportionalt**, beregnes betalingsraterne baseret på nettofakturabeløbet, efter skattebeløbet er fratrukket.

4. Angiv de øvrige krævede oplysninger, og luk derefter siden.
