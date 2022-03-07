---
title: Du kan ikke filtrere varedisponeringsvarer efter deres relaterede disponeringsgruppeværdier
description: Du kan ikke filtrere varedisponeringsvarer efter deres relaterede disponeringsgruppeværdier.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049459"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a>Du kan ikke filtrere varedisponeringsvarer efter deres relaterede disponeringsgruppeværdier

KB-nummer: 4612572

## <a name="symptoms"></a>Symptomer

Du vil filtrere de varer, der skal medtages i en varedisponeringsbatch, baseret på værdierne for relaterede poster fra varedisponeringstabellen. (Du vil f.eks. filtrere varer efter deres værdi i **kreditor**- og/eller **disponeringsgruppen**). Med filteropsætningen for batchjobbet kan du oprette en joinforbindelse fra tabellen **Varer** til tabellen **Varedisponering** og derefter angive feltværdier fra varedisponeringstabellen i forespørgslen. Men når du har fuldført denne opsætning, opretter systemet stadig ordreforslag for hele varedisponeringen, ikke kun for de varer, der svarer til de angivne feltværdier fra varedisponeringstabellen.

## <a name="resolution"></a>Løsning

Filteret for batchjobbet kan kun filtrere efter varer. Du kan føje en joinforbindelse til tabellen **Varedisponering**, men de filterindstillinger, du foretager i forhold til den pågældende tabel, påvirker ikke forespørgselsoutputtet. På kørselstidspunktet kører systemet planlægning for alle disponeringsgrupper og alle de variationer, som de filtrerede varer har. Når en vare allerede er inkluderet i kørslen, påvirker eventuelle disponeringsgrupper, der er inkluderet i varefilter A, ikke outputtet for planlægning.
