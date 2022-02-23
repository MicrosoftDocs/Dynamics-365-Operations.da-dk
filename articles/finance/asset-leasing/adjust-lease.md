---
title: Justere leasingaftaler
description: Emnet forklarer, hvordan du justerer en leasingaftale. Det kan være nødvendigt at foretage en justering, hvis betingelserne for leasingaftalen ændres, leasingaftalen forlænges, eller andre betingelser ændres.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9d1c6e20e72fb2816c32e71e8921a94724ae5656
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441772"
---
# <a name="adjust-leases"></a>Justere leasingaftaler

[!include [banner](../includes/banner.md)]

Emnet forklarer, hvordan du justerer en leasingaftale. Det kan være nødvendigt at foretage en justering, hvis betingelserne for leasingaftalen ændres, leasingaftalen forlænges, eller andre betingelser ændres. Aktivleasing er i overensstemmelse med retningslinjerne for, at Accounting Standards Codification Topic 842 (ASC 842) og International Financial Reporting Standard 16 (IFRS 16) omhandler redigering af leasingaftaler. ASC-842-20-15-1 definerer en leasingændring, som enhver ændring af vilkårene og betingelserne i en kontrakt, der medfører en ændring i omfanget af eller overvejelser i forbindelse med en leasingaftale. Punkt 39 i IFRS 16 angiver, at en af modtagerne skal regulere leasingforpligtelsen, så den afspejler ændringer af betalinger af leasingaftalen.

For organisationer, der overholder ASC 842 eller IFRS 16, revurderes en leasingaftale, så den afspejler en ændring i den nuværende værdi af de fremtidige minimums leasingbetalinger (PVFMLP). Hvis PVFMLP øges, vil den oprettede kladdepost være en debitering af kontoen for brugsretsaktivet (ROU) og en kreditering af leasingforpligtelsen for forskellen mellem den nye PVFMLP og den tidligere PVFMLP. Hvis PVFMLP reduceres, vil kladdeposteringen være et debetbeløb af leasingforpligtelsen og en kreditering til ROU-aktivet for forskellen.

Hvis reguleringen reducerer ROU-aktivet til under 0 (nul), krediteres resten med den bogføringskonto for leasingændringer, der er angivet på siden **Leasingsaftalens bogføringskonti**. Systemkontiene for disse transaktioner og andre reguleringsposter, f. eks. klassificeringsændringer, indledende direkte omkostninger, leasingincitamenter, forudbetalinger og faste omkostninger, der opstår i forbindelse med leasingændringer.

Hvis du vil have en specifik vejledning i transaktioner for leasingregulering, anbefales det, at du ser i IFRS 16 og ASC 842.

Følg disse trin for at justere en leasingaftale. De ændrede data opdaterer leasingplanerne, når processen til oprettelse af en planlægningsproces er kørt.

1. Gå til **Aktivleasing \> Leasingaftaler \> Leasingoversigt**.
2. Vælg den leasingaftale, der skal justeres, og vælg **Regulér leasingaftale** på siden **Leasingoversigt**.
3. Indtast de nye oplysninger for den justerede leasingaftale på siden **Justér leasingaftale**.

    Bemærk, at siden **Justér leasingaftale** ligner siden **Tilføj leasingsaftale**. Ligesom den startdato, du angiver, når du tilføjer en leasingaftale, bestemmes, hvornår den nye leasingaftale begynder, bestemmer feltet **Ændret den** på siden **Justér leasingaftale**, hvornår den justerede leasingaftale starter. Denne dato kan ikke ligge efter startdatoen på betalingsplanlinjerne.

    > [!NOTE]
    > Felterne **ROU-overvejelser** gælder for reguleringen af leasingaftalen. Hvis ingen af de indledende direkte omkostninger, leasingincitamenter, forudbetalinger eller faste omkostninger knyttes til den ændrede leasingaftale, skal du lade disse felter være tomme. De oprindelige beløb gælder ikke for den opdaterede leasingaftale. Eventuelle yderligere omkostninger, der er påløbet, når leasingaftalen ændres, skal angives på siden **Justér leasingaftale**.
    > 
    > En leasinggiver kan f.eks. give $1.000 incitament for at acceptere en forlængelse af en leasingaftale. Hvis du i dette tilfælde justerer leasingaftalen til kontoen for forlængelsen, skal du skrive **1.000** i feltet **Leasingincitamenter**. Hvis der ikke er nogen incitamenter knyttet til leasingjusteringen, skal du fjerne alle værdier, der tidligere er angivet i dette felt. Den samme logik anvendes på andre ROU-overvejelser.

    Betalingsplanlinjerne for den justerede leasingaftale skal oprettes på et muligt grundlag. Betalingsplanlinjer, der er oprettet på et muligt grundlag, kan ikke starte, før leasingændringerne træder i kraft.

    De følgende trin er næsten identiske med de trin, der først anerkendes som en leasingaftale.

4. Vælg **Opret planer** for at generere den justerede betalingsplan. Du får vist en meddelelse, der angiver, at betalingsplanen er blevet oprettet for leasingaftalen.

    > [!IMPORTANT]
    > Før du vælger **Opret planer**, skal du sikre dig, at ændringsdatoen og betalingsplanlinjerne er korrekte. Sørg også for, at alle de indledende omkostninger, leasingincitamenter og forudbetalinger eller faste omkostninger kun svarer til de omkostninger, der opstår i løbet af justeringen.

5. Hvis du vil se den netop oprettede betalingsplan, skal du vælge **Kartoteker** og åbne siden **Betalingsplan**.
6. På siden **Betalingsplan** kan du redigere de justerede betalingsbeløb , før du bekræfter betalingsplanen. Vælg **Bekræft plan** for at bekræfte tidsplanen.

    Når betalingsplanen er bekræftet, oprettes den nye afskrivning for anlægsaktivet og den nye plan for leasingforpligtelser.

7. Hvis du vil se den nye plan for amortisering af leasingforpligtelser, der genereres ud fra de nye input, skal du lukke siden **Betalingsplan** og åbne siden **Amortiseringsplanen for leasingforpligtelse**.
8. Hvis du vil se den nyoprettede afskrivningsplan for anlægsaktiver, skal du åbne siden **Afskrivningsplan for aktiver** på siden **Kartotekoplysninger**.
9. Hvis du vil generere reguleringskladdeposten, skal du vælge **Funktion \> Leasingregulering**. Du modtager en meddelelse om, at reguleringskladdeposten er oprettet. 
10. Hvis du vil se kladdeposten, skal du vælge **Kladder \> Aktivleasingkladde**.
11. Hvis du vil bogføre kladdeposten, skal du markere linjen og derefter vælge **Bogfør**.

## <a name="view-lease-versions"></a>Vis leasingversioner

Hvis en leasingaftale er blevet ændret, kan du få vist de forskellige versioner af den. Du kan også se historikplanerne og de tidligere leasingaftaler.

1. Vælg den leasingaftale, der skal kopieres, på siden **Leasingoversigt**, og vælg derefter **Leasingversionshistorik** i handlingsruden.

    Hvis den valgte leasingaftale er blevet justeret, viser siden **Leasingversionshistorik** de forskellige versioner af den. Den oprindelige leasingaftale er mærket **1**, og efterfølgende versioner har en stigende numerisk rækkefølge.

    I forbindelse med en valgt leasingversion kan du få vist de økonomiske dimensioner, kontraktdetaljer, placeringer og betalingsplanlinjer.

2. Hvis du vil se historikplanerne, skal du åbne den ændrede leasingaftale fra siden **Leasingoversigt**, vælge det ønskede kartotek og derefter vælge **Versionshistorik for kartotek** i handlingsruden.
3. Vælg den ønskede version og den plan, der skal vises, på siden **Bogversion**.
