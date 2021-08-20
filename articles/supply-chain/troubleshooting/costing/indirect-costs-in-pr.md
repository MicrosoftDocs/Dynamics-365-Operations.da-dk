---
title: Rapporten Indirekte omkostninger under afvikling omfatter slettede produktionsordrer
description: Rapporten Indirekte omkostninger under afvikling indeholder oplysninger om produktionsordrer, der er delvist behandlet og senere slettet.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 817802f1f2ad3ab07f35c28d3e833a14cd02cf8b9705c576325dc83933a0c6de
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751763"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>Rapporten Indirekte omkostninger under afvikling omfatter slettede produktionsordrer

KB-nummer: 4612748

## <a name="symptoms"></a>Symptomer

Rapporten **Indirekte omkostninger under afvikling** indeholder oplysninger om produktionsordrer, der er delvist behandlet og senere slettet.

## <a name="resolution"></a>Løsning

Når du tilbagefører en produktionsordre, tilbageføres også alle posteringerne for den pågældende produktionsordre. Når du sletter produktionsordren, består alle posteringer, der er relateret til den, i reskontrotabellerne og finansmodulet. Rapporterne vil vise posteringerne i reskontrotabellerne. For den specifikke produktionsordre skal nettoværdien være 0,00.
