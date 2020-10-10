---
title: Opsæt foretrukne vedligeholdelsesarbejdere
description: Dette emne beskriver, hvordan du konfigurerer foretrukne vedligeholdelsesarbejdere i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerPreferred
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c0637609a34890360a3b81355a8d21ef1b9faf8c
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888923"
---
# <a name="set-up-preferred-maintenance-workers"></a>Opsæt foretrukne vedligeholdelsesarbejdere

[!include [banner](../../includes/banner.md)]

 

Du kan under planlægning af arbejdsordrer angive en præference for, hvilken vedligeholdelsesarbejder eller vedligeholdelsesgruppe der skal tildeles for at afslutte arbejdsordrer. Brugen af denne funktion er valgfri, men den kan hjælpe dig med at vælge den mest kvalificerede vedligeholdelsesarbejder til at fuldføre et job baseret på arbejderens færdigheder og kompetencer. Kun vedligeholdelsesarbejdere, der er tilgængelige på planlægningstidspunktet, indgår i planlægningen. Hvis opsætning for en foretrukken vedligeholdelsesarbejder stemmer overens med en arbejdsordre under planlægningen, men vedligeholdelsesarbejderen er allokeret til andre job, planlægges arbejdsordren for en anden tilgængelig vedligeholdelsesarbejder.

Før du kan konfigurere foretrukne vedligeholdelsesarbejdere, skal du først konfigurere vedligeholdelsesarbejdere og arbejdergrupper. Du kan finde en beskrivelse af, hvordan du konfigurerer vedligeholdelsesarbejdere og arbejdergrupper, under [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-preferred-workers"></a>Konfigurere foretrukne arbejdere

En foretrukket vedligeholdelsesarbejder eller arbejdergruppe kan knyttes til en eller flere af følgende:

- handel  
- variant af en vedligeholdelsesjobtype  
- vedligeholdelsesjobtype  
- kategori for vedligeholdelsesjobtype  
- aktiv  
- aktivtype  

Jo flere valg du foretager for den samme post, jo mere specifik bliver din opsætning.

1. Klik på **Styring af aktiver** > **Opsætning** > **Arbejdere** > **Foretrukne vedligeholdelsesarbejdere**.

2. Klik på **Ny** for at oprette en ny post.

3. Start med at oprette en "standard"-vedligeholdelsesarbejder eller -arbejdergruppe. Det betyder, at du kun foretager valg i feltet **Foretrukken vedligeholdelsesarbejdergruppe** eller i feltet **Foretrukne vedligeholdelsesarbejdere**. I nedenstående skærmbillede kan du se et eksempel i den første post, hvor "Anmodninger" er valgt som **Foretrukken vedligeholdelsesarbejdergruppe**.

    [!NOTE] Denne standardopsætning bruges i forbindelse med planlægningen af arbejdsordrer, hvis der ikke er angivet en mere specifik kombination, som svarer til indholdet af arbejdsordren.

4. Gentag trin 2 for at oprette en ny post. Foretag de nødvendige valg, afhængigt af detaljeringsniveauet for den foretrukne arbejder eller arbejdergruppe. 

    *Eksempel:* skærmbilledet nedenfor er Shawn Richardson valgt som foretrukken arbejder. Han vil automatisk blive valgt under planlægning af en arbejdsordre, der omfatter aktivet "CH-BP1-03-02 og vedligeholdelsesjobtypen"Facilitetsvurdering ", hvis han er ledig på det planlagte tidspunkt.

    [!NOTE] Når der vælges en foretrukken vedligeholdelsesarbejder under planlægningen af arbejdsordrer, gennemgår Styring af aktiver alle poster med **Foretrukne vedligeholdelsesarbejdere** for at søge efter et muligt match og kontrollere altid den mest specifikke kombination først. Hvis der ikke findes et match, bruges posten "standard" med et valg i enten feltet **Foretrukken vedligeholdelsesarbejdergruppe** eller feltet **Foretrukken vedligeholdelsesarbejder**.

![Figur 1](media/02-work-order-scheduling.png)

Du kan også konfigurere *ansvarlige* vedligeholdelsesarbejdere, der kan vælges, når der oprettes en vedligeholdelsesanmodning eller en arbejdsordre. I **Alle arbejdsordrer** og **Alle vedligeholdelsesanmodninger** kan du redigere valget, hvis det er nødvendigt. Se [Ansvarlige vedligeholdelsesarbejdere](../setup-for-maintenance-requests/responsible-workers.md) for at få yderligere oplysninger.

Under planlægningen af arbejdsordren beregnes der forskellige scorer for at bestemme, hvilke arbejdere der skal udføre de job, der vedrører en arbejdsordre (disse scorer konfigureres i **Styring af aktiver** > **Planlægning af arbejdsordrer**-linket). Hvis to eller flere foretrukne vedligeholdelsesarbejdere eller ansvarlige vedligeholdelsesarbejdere har samme score under planlægningen af arbejdsordrer, vælges én arbejder tilfældigt. Ellers er det altid arbejderen med den højeste score, der tildeles til at fuldføre en arbejdsordre.

