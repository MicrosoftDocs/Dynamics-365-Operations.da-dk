---
title: Vedligeholdelsesstatus
description: I dette emne forklares, hvordan du beregner vedligeholdelsesstatus i Styring af aktiver.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f3d6f86c5052c845c9c8aad1e4437f4196f78b50
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808610"
---
# <a name="maintenance-status"></a>Vedligeholdelsesstatus

[!include [banner](../../includes/banner.md)]

 

I Styring af aktiver kan du foretage en oversigtsberegning for en specifik periode til nye, aktive og fuldførte aktiviteter for vedligeholdelsesanmodninger, arbejdsordrer og vedligeholdelsesnedetid. Du kan også se antallet af fuldførte betingelsesvurderinger for den samme periode. Brug denne beregning til at få et overblik over arbejdsbyrder i forbindelse med indgående og fuldførte vedligeholdelsesanmodninger og arbejdsordrer.

## <a name="make-a-maintenance-status-calculation"></a>Foretage en beregning af vedligeholdelsesstatus

1. Klik på **Styring af aktiver** > **Forespørgsler** > **Vedligeholdelsesstatus**.

2. I dialogboksen **Beregn status** skal du vælge det tidsinterval, du vil foretage beregningen for, i felterne **Fra-dato** og **Til-dato**.

3. Du kan bruge feltet **Niveau** til at angive, hvor detaljerede vedligeholdelseslinjerne skal være i forbindelse med arbejdssteder. 

  Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle vedligeholdelseslinjer for et arbejdssted på det øverste niveau, og derfor kan status på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau. 
  
  Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle vedligeholdelseslinjer på alle de arbejdsstedsniveauer, de er relateret til.

4. Klik på **OK** for at starte beregningen.

5. Klik på **Sammenlæg pr.**-knapper for at få vist det nødvendige detaljeringsniveau i beregningen. De valgte **Sammenlæg pr.**-knapper er fremhævet. Klik på en knap for at aktivere eller deaktivere den.

6. Husk at klikke på knappen **Opdater** for at opdatere beregningen, hver gang du foretager ændringer ved at aktivere eller deaktivere **Sammenlæg pr.**-knapper eller ved at foretage en beregning for en ny periode.

7. Klik på **Status**, hvis du vil oprette en ny vedligeholdelsesstatusberegning.

>[!NOTE]
>De resultater, der vises i **Vedligeholdelsesstatus**, omfatter kun vedligeholdelsesanmodninger og arbejdsordrer, der har en faktisk startdato og -klokkeslæt. Slutdato og -klokkeslæt kan være tomt.

## <a name="example-1"></a>Eksempel 1

I nedenstående skærmbillede er knapperne **År** og **Måned** aktiveret. Når disse indstillinger for **Sammenlæg pr.** er valgt, får du et generelt overblik på månedlig basis af arbejdsbyrde og gennemløb i forbindelse med vedligeholdelsesanmodninger og arbejdsordrer. 

![Eksempel på månedlig arbejdsbyrde](media/13-controlling-and-reporting.png)

## <a name="example-2"></a>Eksempel 2

I skærmbilledet nedenfor er der tilføjet oplysninger om arbejdssteder. Nu er det muligt at sammenligne arbejdsbyrder og gennemløb på tværs af arbejdssteder, som kan repræsentere geografiske placeringer, fabrikker eller arbejdsområder. 

![Eksempel på månedlig arbejdsbyrde med arbejdssteder](media/14-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]