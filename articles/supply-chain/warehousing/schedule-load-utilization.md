---
title: Planlæg lastningsudnyttelse
description: I dette emne beskrives, hvordan du kan oprette og planlægge belastningen for et lagersted.
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15f3735f79671ac41789d39a5473722a5f35fde0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "332029"
---
# <a name="schedule-load-utilization"></a>Planlæg lastningsudnyttelse

[!include[banner](../includes/banner.md)]

Du kan planlægge lastningsudnyttelse for udvalgte lokationstyper, og du kan også oprette prognoser for den aktuelle og fremtidige belastning. Du kan oprette prognoser for belastningen på en eller flere lokationer, for lastningsenheder (zone eller lagersted) eller for en kombination af en zone og et lagersted.

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a>Planlægge og få vist belastning for et lagersted eller en lokation

For at planlægge belastningen for lokationer, lagersteder eller zoner, skal du oprette en pladsudnyttelseskonfiguration og knytte den til en behovsplan.

I pladsudnyttelseskonfigurationen skal du bruge lokationstyper, f.eks. **Bulkvarelokation** og **Plukplads**, til at angive, hvordan pladsudnyttelsen skal planlægges. Du også angive en lagringslastningstilstand, f.eks **Zone**.

Prognosen for fremtidig pladsudnyttelse er baseret på oplysninger, der er beregnet på den tilknyttede behovsplan. Behovsplaner anslår ressourceplanlægningen for indgående og udgående ordrer for produktion og operationer. Prognosen over tilgængelig plads er baseret på forholdet mellem pladsudnyttelseskonfigurationen og den valgte behovsplan.

Ved hjælp af belastningstilstanden, du valgte i opsætning af pladsudnyttelse, kan du angive, om belastningen skal anslås for hvert enkelt lagersted eller zone, eller om prognosen skal indeholde oplysninger om både lagersteder og zoner. Du kan også angive, om blokerede lagersteder skal udelukkes fra beregningen af lastningsudnyttelsen.

Du kan planlægge pladsudnyttelsen ved at generere rapporten **Lagerstedslastningsudnyttelse**. Når du opretter denne rapport, kan du angive, om lastningsudnyttelsen skal anslås for hver lokation eller på tværs af lokationer eller for den valgte lastningsenhed, f.eks. zone eller lagersted.

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a>Oprette en pladsudnyttelsesopsætning for et lagersted

1. Vælg **Lagerstyring** \> **Opsætning** \> **Overvågning af lagersted** \> **Pladsudnyttelse**.
2. Vælg **Ny** for at oprette en pladsudnyttelsesopsætning. Angiv et id og et navn til den nye konfigurationen.
3. I feltet **Lagerlastningstilstand** skal du vælge, om oversigten over pladsudnyttelse skal vise oplysninger pr. lagersted, zone eller lagersted og zone.
4. Vælg **Ja** i indstillingen **Udelad spærrede adresser** for at udelade spærrede lagerplaceringer i beregningen af ledig plads. Du kan blokere en lagerstedsplacering for input og output ved at angive en blokeringsårsag for lokationen i feltet **Indlagring spærret** eller **Udlagring spærret** i oversigtspanelet **Andet** på siden **Lagerlokationer**.
5. I oversigtspanelet **Lokationstype** skal du vælge de lokationstyper, der skal medtages i beregningen af pladsudnyttelsen. Du skal vælge mindst én lokationstype til prognosen.

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a>Knytte en pladsudnyttelsesopsætning til til en behovsplan

1. Vælg **Lagerstyring** \> **Periodiske opgaver** \> **Planlæg lastningsudnyttelse**.
2. Vælg en behovsplan i feltet **Behovsplan**.
3. I feltet **Antal dage** skal du angive antallet dage, der skal medtages i prognosen over aktuelle og fremtidige arbejdsbyrder.
4. I feltet **Pladsudnyttelse** skal du vælge den pladsudnyttelsesopsætning, der skal bruges til at anslå den aktuelle og fremtidige arbejdsbelastning.

### <a name="specify-the-load-utilization-projection-and-view-information"></a>Angive lastningsudnyttelseprognose og få vist oplysninger

1. Vælg **Lagerstyring** \> **Forespørgsler og rapporter** \> **Fysiske lagerrapporter** \> **Lagerstedslastningsudnyttelse**.
2. I feltet **Vis efter** skal du vælge niveauet for pladsudnyttelseprognoser:

    - **Lokation** – Vælg denne indstilling for at anslå pladsudnyttelsen pr. lokation. Denne prognose er nyttig, hvis du f.eks. vil have vist alle lagersteder for en lokation, så du kan afstemme udnyttelse af pladsen mellem lagerstederne.
    - **Lastningsenhed** – Vælg denne indstilling for at anslå pladsudnyttelsen for zoner eller lagersteder. Den tilgængelige plads anslås herefter i overensstemmelse med den værdi, du valgte i feltet **Lagerlastningstilstand** på siden **Pladsudnyttelse**, da du oprettede pladsudnyttelsesopsætningen.

3. Benyt en af følgende fremgangsmåder, afhængigt af den værdi du valgte i forrige trin:

    - Hvis du valgte **Lokation** i feltet **Vis efter**, er feltet **Lokation** tilgængeligt. Vælg en eller flere lokationer, der skal medtages i prognosen.
    - Hvis du valgte **Lastningsenhed** i feltet **Vis efter**, er feltet **Lastningsenhed** tilgængeligt. Vælg lastningsenheden.

4. I feltet **Lastningstype** skal du vælge **Enhed** eller **Vægt** for at angive den lagerdriftsenhed, der skal anslås plads for.
5. I feltet **Opsætning af pladsudnyttelse** skal du vælge den pladsudnyttelsesopsætning, som prognosen skal baseres på.
