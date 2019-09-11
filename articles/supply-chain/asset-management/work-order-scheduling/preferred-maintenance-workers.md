---
title: Opsæt foretrukne vedligeholdelsesarbejdere
description: Dette emne beskriver, hvordan du konfigurerer foretrukne vedligeholdelsesarbejdere i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887405"
---
# <a name="preferred-maintenance-workers"></a>Foretrukne vedligeholdelsesarbejdere

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Du kan angive en præference for, hvilke vedligeholdelsesarbejdere der skal tildeles for at afslutte arbejdsordrer under planlægning af arbejdsordrer. Brugen af denne funktion er valgfri, men den kan hjælpe dig med at vælge den mest kvalificerede vedligeholdelsesarbejder til at fuldføre et job baseret på arbejderens færdigheder og kompetencer. Derfor bruges opsætningen i **Foretrukne vedligeholdelsesarbejdere** under planlægning af arbejdsordrer til at bestemme, om en bestemt vedligeholdelsesarbejder eller arbejdergruppe skal planlægges for en arbejdsordre. Kun vedligeholdelsesarbejdere, der er tilgængelige på planlægningstidspunktet, indgår i planlægningen. Hvis opsætning for en foretrukken vedligeholdelsesarbejder stemmer overens med en arbejdsordre under planlægningen, men vedligeholdelsesarbejderen er allokeret til andre job, planlægges arbejdsordren for en anden tilgængelig vedligeholdelsesarbejder.

Før du kan konfigurere foretrukne vedligeholdelsesarbejdere, skal du først konfigurere de vedligeholdelsesarbejdere og arbejdergrupper, der skal kunne vælges. Du kan finde en beskrivelse af, hvordan du konfigurerer vedligeholdelsesarbejdere og arbejdergrupper, i [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-preferred-workers"></a>Konfigurere foretrukne arbejdere

En foretrukket vedligeholdelsesarbejder eller arbejdergruppe kan knyttes til en bestemt

- handel  
- variant af en vedligeholdelsesjobtype  
- vedligeholdelsesjobtype  
- kategori for vedligeholdelsesjobtype  
- aktiv  
- aktivtype  

eller en kombination af disse valg. Jo flere valg du foretager for den samme post, jo mere specifik bliver din opsætning.

1. Klik på **Styring af aktiver** > **Opsætning** > **Arbejdere** > **Foretrukne vedligeholdelsesarbejdere**.

2. Klik på **Ny** for at oprette en ny post.

3. Start med at oprette en "standardopsætning" for vedligeholdelsesarbejdere eller arbejdergrupper, der ikke har nogen markeringer i de felter, der vises på punktlisten ovenfor. Det betyder, at du kun foretager valg i feltet **Foretrukken vedligeholdelsesarbejdergruppe** eller i feltet **Foretrukne vedligeholdelsesarbejdere**. I nedenstående figur kan du se et eksempel i den første post, hvor "Anmodninger" er valgt som foretrukken vedligeholdelsesarbejdergruppe.

>[!NOTE]
>Standardopsætningen bruges i forbindelse med planlægningen af arbejdsordrer, hvis der ikke er angivet en mere specifik kombination, som svarer til indholdet af arbejdsordren under planlægningen af arbejdsordren.

4. Gentag trin 2 for at oprette en ny post. Foretag de nødvendige valg, afhængigt af detaljeringsniveauet for den foretrukne arbejder eller arbejdergruppe. *Eksempel:* I den sjette post i figuren nedenfor er Shawn Richardson valgt som foretrukken arbejder. Han vil automatisk blive valgt ved planlægning af en arbejdsordre, der omfatter aktivet "CH-BP1-03-02 og vedligeholdelsesjobtypen"Facilitetsvurdering ", hvis han er tilgængelig på det planlagte tidspunkt.

>[!NOTE]
>Når der vælges en foretrukken vedligeholdelsesarbejder under planlægningen af arbejdsordrer, gennemgår Styring af aktiver alle poster med **Foretrukne vedligeholdelsesarbejdere** for at søge efter et muligt match og kontrollere altid den mest specifikke kombination først. Hvis der ikke findes et match, bruges posten "standard" med et valg i enten feltet **Foretrukken vedligeholdelsesarbejdergruppe** eller feltet **Foretrukken vedligeholdelsesarbejder**.


![Figur 1](media/02-work-order-scheduling.png)

Du kan også konfigurere ansvarlige vedligeholdelsesarbejdere, der kan vælges, når der oprettes en vedligeholdelsesanmodning eller en arbejdsordre. I **Alle arbejdsordrer** og **Alle vedligeholdelsesanmodninger** kan du evt. redigere valget, hvis det er nødvendigt. Se [Ansvarlige vedligeholdelsesarbejdere](../setup-for-maintenance-requests/responsible-workers.md) for at få yderligere oplysninger.

Under planlægningen af arbejdsordren beregnes der forskellige scorer for at bestemme, hvilke arbejdere der skal udføre de job, der vedrører en arbejdsordre (disse scorer konfigureres i **Styring af aktiver** > **Planlægning af arbejdsordrer**-linket). Hvis to eller flere foretrukne vedligeholdelsesarbejdere eller ansvarlige vedligeholdelsesarbejdere har samme score under planlægningen af arbejdsordrer, vælges én arbejder tilfældigt. Ellers er det altid arbejderen med den højeste score, der tildeles til at fuldføre en arbejdsordre.

