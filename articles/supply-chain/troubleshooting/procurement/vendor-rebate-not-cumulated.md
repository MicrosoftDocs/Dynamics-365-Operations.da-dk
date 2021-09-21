---
title: En leverandørrabat bliver ikke akkumuleret på basis af fakturaer
description: En leverandørrabat bliver ikke akkumuleret på basis af fakturaer
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 9d4596a7351969bf181982a24ea1dcc6f5732831
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475947"
---
# <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>En leverandørrabat bliver ikke akkumuleret på basis af fakturaer

## <a name="symptoms"></a>Symptomer

Hvis fakturaer, der er bogført, har forskellige forfaldsdatoer, afspejles disse fakturaer ikke i de leverandørrabatter, der genereres af dem.

## <a name="resolution"></a>Løsning

Forfaldsdatoen tages ikke i betragtning, når leverandørrabatten beregnes. Overvej at tilpasse systemet, så forfaldsdatoen og relationen til fakturaen er mere synlig i forhold til den faktiske leverandørrabat.
