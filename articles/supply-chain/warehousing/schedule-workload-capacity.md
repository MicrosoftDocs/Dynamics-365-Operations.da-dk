---
title: "Planlægge arbejdsbyrdekapacitet"
description: "I dette emne beskrives, hvordan du opretter og planlægger arbejdsbyrdekapaciteten for arbejdere på et lagersted eller for hele lagerstedet."
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69b9c5590e6f9311696bbbed2e63a6eeba2a90bf
ms.openlocfilehash: 1b93cfaf098b4cff3e72ee9bb599eadfdac2a9b9
ms.contentlocale: da-dk
ms.lasthandoff: 05/03/2018

---

# <a name="schedule-workload-capacity"></a>Planlægge arbejdsbyrdekapacitet

[!include[banner](../includes/banner.md)]

Du kan planlægge arbejdsbyrdekapacitet for lagersteder, og du kan også planlægge de aktuelle og fremtidige arbejdsbyrder for medarbejderne på de forskellige lagersteder. Du kan planlægge arbejdsbyrden for hele lagerstedet, eller du kan planlægge arbejdsbyrden separat for indgående og udgående arbejdsbyrder.

Hvis du vil planlægge arbejdsbyrdeoutput for udvalgte lagersteder, skal der være behovsplanlægningsdata tilgængelige for de pågældende lagersteder. Du kan finde flere oplysninger under [Behovsplaner](../master-planning/master-plans.md).

## <a name="schedule-and-view-workloads-for-a-warehouse"></a>Planlægge og se arbejdsbyrder for et lagersted.

Hvis du vil planlægge arbejdsbyrdekapacitet for et lagersted, skal du oprette en arbejdsbyrdeopsætning for et eller flere lagersteder og derefter knytte arbejdsbyrdeopsætningen til en behovsplan. I arbejdsbyrdekapacitetsopsætningen kan du definere grænser for vægt eller volumen for indgående og udgående transaktioner. Du kan også konfigurere mere end en opsætning for hvert lagersted og derefter tilknyttet opsætningen med forskellige behovsplaner. Du kan f.eks. bruge denne fremgangsmåde til at tilpasse sæsonbestemte ændringer til arbejdsstyrken.

Hvis medarbejderne på et lager arbejder med transaktioner for indgående og udgående arbejdsbyrder, kan du konfigurere lagerkapacitetsopsætningen, så arbejdsbyrden vises anslået i en samlet visning.

Hvis du vil planlægge og få vist arbejdsbyrden for lagersteder, skal du fuldføre følgende opgaver:

1. Opret en arbejdsbyrdekapacitetsopsætning, og definer arbejdsbyrdekapacitetsbegrænsningerne for et eller flere lagersteder.
2. Knyt arbejdsbyrdekapacitetsopsætningen til en behovsplan for at oprette arbejdsbyrdeprognoser og angive, hvor længe planerne gælder.

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a>Oprette en arbejdsbyrdekapacitetsopsætning for et lagersted

1. Vælg **Lagerstyring** \> **Opsætning** \> **Overvågning af lagersted** \> **Arbejdsbyrdekapacitet**.
2. Vælg **Ny** i handlingsruden for at oprette en arbejdsbyrdekapacitetsopsætning.
3. Vælg **Ny** i oversigtspanelet **Lagersteder**, og indtast derefter værdier på linjen for at knytte et lager med arbejdsbyrdekapacitetsopsætningen.
4. Marker afkrydsningsfeltet **Kombineret indgående og udgående arbejdsbyrde**, hvis rapporten **Arbejdsbyrdekapacitet** skal vise den samlede arbejdsbyrde for indgående og udgående transaktioner i én visning.
5. Vælg de typer indgående og udgående transaktionstyper, som arbejdsbyrdebegrænsningerne skal gælde for, i oversigtspanelet **Transaktionstyper**.

    > [!NOTE]
    > Du skal vælge mindst én transaktionstype for både den indgående arbejdsbyrde og den udgående arbejdsbyrde.

#### <a name="define-limits-for-volume-or-weight"></a>Definere grænser for volumen eller vægt

Du kan konfigurere grænser for volumen eller vægt på baggrund af de begrænsninger, der er relevante for lagerstedets medarbejdere. De angivne grænser medtages i arbejdsbyrdekapacitetsplanlægningen, som du kan se i rapporten **Arbejdsbyrdekapacitet**.

Hvis du vil oprette planer med oplysninger om volumen og vægt for varer, skal standardvolumen af en lagervare og vægten af en lagervare angives for alle produkter. De påkrævede felter er tilgængelige i følgende feltgrupper i oversigtspanelet **Styr lager** på siden **Frigivne produktdetaljer**:

- Ekspederes
- Fysiske dimensioner
- Måleenheder for vægt

Hvis disse oplysninger ikke angives korrekt, du får vist en meddelelse, når du genererer rapporten **Arbejdsbyrdekapacitet**. I rapporten kan du derefter dykke ned for at identificere de manglende oplysninger, der stadig skal angives, for at den fremtidige arbejdsbyrde kan planlægges.

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a>Knytte en arbejdsbyrdekapacitetsopsætning til en behovsplan

1. Vælg **Lagerstyring** \> **Periodisk** \> **Planlæg arbejdsbyrde**.
2. I feltet **Behovsplan** skal du vælge den behovsplan, der skal bruges til prognoser for arbejdsbyrde.
3. I feltet **Antal dage** skal du angive antallet dage, der dækkes arbejdsbyrdeplanen.
4. I feltet **Arbejdsbyrde** skal du vælge den arbejdsbyrdeopsætning, der skal tilknyttes behovsplanen.

### <a name="view-workload-capacity"></a>Få vist arbejdsbyrdekapacitet

1. Vælg **Lagerstyring** \> **Forespørgsler og rapporter** \> **Fysiske lagerrapporter** \> **Arbejdsbyrdekapacitet**.
2. I feltet **Antal kolonner** skal du angive antallet af kolonner, der skal vises i rapporten.
3. I feltet **Ordretype** skal du vælge **Planlagt og bekræftet**, **Planlagt** eller **Bekræftet** for at angive den type ordrer, der skal anslås i rapporten.
4. I feltet **Lastningstype** skal du vælge en belastningstype for at angive, om arbejdsbyrdekapaciteten skal planlægges for paller, volumen eller vægt.
5. I feltet **Arbejdsbyrdekapacitet** skal du vælge en arbejdsbyrdekapacitetsopsætning.

