---
title: Kan ikke bogføre følgeseddel for en stoppet salgsordrelinje
description: Du kan ikke bogføre følgeseddel for en stoppet salgsordrelinje
author: smithanataraj
ms.date: 03/07/2022
ms.topic: article
ms.search.form: WHSLoadTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2022-03-07
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 115cfe79e075eb36f73203818acdbb5e31fc0bad
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462847"
---
# <a name="cant-post-packing-slip-for-a-stopped-a-sales-order-line"></a>Kan ikke bogføre følgeseddel for en stoppet salgsordrelinje

Fejlkode: SYS13203

## <a name="symptoms"></a>Symptomer

Når du forsøger at bogføre en følgeseddel for en last, vises følgende fejlmeddelelse:

> Det er ikke muligt at bogføre følgesedlen, når en salgsordrelinje stoppes efter bekræftelse af den udgående forsendelse. Et antal kan ikke plukkes.

## <a name="cause"></a>Årsag

En eller flere af de relaterede salgsordrelinjer kan være stoppet, hvilket betyder, at systemet forhindrer yderligere behandling af den pågældende salgsordre. Det kan bl.a. betyde, at systemet ikke bogfører en følgeseddel for ordren.

En bruger kan f.eks. have valgt at stoppe en eller flere ordrelinjer, fordi kunden har tilbagekaldt og annulleret sin ordre. Hvis den udgående forsendelse allerede er blevet bekræftet, vil forsendelsen, der indeholder salgsordren, imidlertid allerede fysisk have forladt lagerstedet, hvilket betyder, at standsning af salgsordrelinjerne ikke vil have nogen virkning. Da det ikke længere er muligt fysisk at standse forsendelsen, kan du lige så godt undlade at standse linjer, så du kan bogføre følgesedlen. Derefter skal du håndtere den annullerede ordre som en returnering.

## <a name="resolution"></a>Løsning

Hvis du vil kunne bogføre følgesedlen, skal du kontrollere, at ingen af de relevante salgsordrelinjer er stoppet, ved at følge nedenstående fremgangsmåde.

1. Gå til **Alle salgsordrer \> Salg og marketing \> Alle salgsordrer**.
1. Find og åbn den salgsordre, du har problemer med.
1. I oversigtspanelet **Salgsordrelinjer** skal du vælge en salgsordrelinje.
1. Åbn fanen **Generelt** i oversigtspanelet **Linjedetaljer**, og kontrollér, at feltet **Stoppet** er angivet til *Nej*.
1. Fortsæt arbejdet, indtil alle de relevante salgslinjer ikke længere er stoppet.
1. Prøv igen at bogføre følgesedlen for lasten eller salgsordren.
