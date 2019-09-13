---
title: Vedligeholdelsesstatus
description: I dette emne forklares, hvordan du beregner vedligeholdelsesstatus i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: 516607c056125a16e075c33f3c2ad069efb396d9
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918343"
---
# <a name="maintenance-status"></a>Vedligeholdelsesstatus

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

I Styring af aktiver kan du foretage en beregning for at få vist en oversigt over nye, aktive og fuldførte vedligeholdelsesanmodninger, arbejdsordrer og vedligeholdelsesnedetid for en bestemt periode. Du kan også se antallet af fuldførte betingelsesvurderinger for den samme periode. Brug denne beregning til at få et overblik over arbejdsbyrder i forbindelse med indgående og fuldførte vedligeholdelsesanmodninger og arbejdsordrer.

## <a name="make-a-maintenance-status-calculation"></a>Foretage en beregning af vedligeholdelsesstatus

1. Klik på **Styring af aktiver** > **Forespørgsler** > **Vedligeholdelsesstatus**.

2. I dialogboksen **Beregn status** skal du vælge den periode, du vil foretage beregningen for, i felterne **Fra-dato** og **Til-dato**.

3. Du kan bruge feltet **Niveau** til at angive, hvor detaljerede vedligeholdelseslinjerne skal være i forbindelse med arbejdssteder. Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle vedligeholdelseslinjer for et arbejdssted på det øverste niveau, og derfor kan status på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau. Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle vedligeholdelseslinjer på alle de arbejdsstedsniveauer, de er relateret til.

4. Klik på **OK** for at starte beregningen.

5. I **Sammenlæg pr.**-handlingsrudegrupperne skal du klikke på de relevante knapper for at få vist det nødvendige detaljeringsniveau i beregningen. De valgte handlingsrudeknapper er fremhævet. Klik på en knap for at aktivere eller deaktivere den.

6. Husk at klikke på knappen **Opdater** for at opdatere beregningen, hver gang du foretager ændringer ved at aktivere eller deaktivere **Grupper efter...**-knapper eller ved at foretage en beregning for en ny periode.

7. Klik på **Status**, hvis du vil oprette en ny vedligeholdelsesstatusberegning.

>[!NOTE]
>De resultater, der vises i **Vedligeholdelsesstatus**, omfatter kun vedligeholdelsesanmodninger og arbejdsordrer, der har en faktisk startdato og -klokkeslæt. Slutdato og -klokkeslæt kan være tomt.

*Eksempel 1:*

I nedenstående figur er knapperne **År** og **Måned** aktiveret. Her får du et generelt overblik på månedlig basis af arbejdsbyrde og gennemløb i forbindelse med vedligeholdelsesanmodninger og arbejdsordrer. 

![Figur 1](media/13-controlling-and-reporting.png)

*Eksempel 2:*

I figuren nedenfor er der tilføjet oplysninger om arbejdssteder. Nu er det muligt at sammenligne arbejdsbyrder og gennemløb på tværs af arbejdssteder, som kan repræsentere geografiske placeringer, fabrikker eller arbejdsområder. 

![Figur 2](media/14-controlling-and-reporting.png)

