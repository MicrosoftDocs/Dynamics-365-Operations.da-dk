---
title: Samme samhandelsaftale, som blev valgt ved oprettelse af salgsordrelinjer
description: Hvis der er mere end én samhandelsaftale defineret en given dato, vil den samhandelsaftale, der har den laveste pris, altid blive valgt, når der oprettes salgsordrelinjer.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a586a399fb349965b972191bec1271651bec5fcb
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475909"
---
# <a name="if-two-trade-agreements-exist-for-overlapping-dates-the-same-one-is-always-selected"></a>Hvis der findes to samhandelsaftaler for overlappende datoer, vælges den samme altid

## <a name="symptoms"></a>Symptomer

Hvis der er defineret to samhandelsaftaler for samme periode eller overlappende perioder, ser den samme samhandelsaftale ud til at blive valgt, hver gang du opretter salgsordrelinjer, der indeholder de pågældende varer.

## <a name="resolution"></a>Løsning

Hvis der er mere end én samhandelsaftale for en given dato, vil den samhandelsaftale, der har den laveste pris, altid blive valgt. Du kan finde flere oplysninger ved at hente følgende hvidbog: [Samhandelsaftaler i Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).
