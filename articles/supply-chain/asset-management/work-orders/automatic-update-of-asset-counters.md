---
title: Automatisk opdatering af aktivtællere
description: I dette emne beskrives automatisk opdatering af aktivtællere i Styring af aktiver.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a3814a575fbe4379b59723f269d83379a253ede71962c0c82b5f4cc55d36e6c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738289"
---
# <a name="automatic-update-of-asset-counters"></a>Automatisk opdatering af aktivtællere

[!include [banner](../../includes/banner.md)]

Du kan finde oplysninger om manuel registrering af aktivtællere under [Manuel opdatering af aktivtællere](../work-orders/manual-update-of-asset-counters.md). Du kan finde oplysninger om, hvordan du konfigurerer aktivtællere, i [Tællere](../setup-for-objects/counters.md).

Tællerværdier kan også opdateres automatisk fra produktionsregistreringer, baseret på produktionstimer eller produktionsantal (det producerede antal). Denne opdatering udføres på siden **Opdater aktivtællere**. Du kan opdatere et eller flere aktiver ved at indstille én parameter, **Fra-dato**. Denne parameter angiver startdatoen for produktionsregistreringer (produktionstimer eller produktionsantal). Med andre ord angives den dato, hvor tællerværdierne skal opdateres fra.

Alle aktiver, der er relateret til en ressource *og* har aktivtællere, som er konfigureret til at blive opdateret på produceret antal eller produktionstimer, medtages i en automatisk opdatering. Der oprettes nye tællerværdier.

For tællere, der er baseret på produktionsantallet, omfatter antallet både det antal, der er gyldigt, og det antal fejl, der er registreret. Hvis den enhed, der bruges til registrering af produktionsantal, er forskellig fra den enhed, der bruges på tælleren, omregnes antallet, så det svarer til tællerenheden.

Som nævnt ovenfor kan automatiske tællere opdateres fra produktionsregistreringer. Det aktiv, som du automatisk vil opdatere tællere for, skal derfor være relateret til en ressource (maskine). Når der er registreret producerede antal eller produktionstimer på ressourcen, kan du opdatere de relaterede aktivtællere.

1. Vælg **Styring af aktiver** > **Periodisk** > **Aktiver** > **Opdater aktivtællere**.

2. Vælg startdatoen for den automatiske opdatering i feltet **Fra-dato**.

    >[!NOTE]
    >Datoen i dette felt er datoen for "igangværende arbejde" fra **Ruteposteringer** (**Produktionsstyring** > **Forespørgsler og rapporter** > **Produktion** > **Ruteposteringer** > **Fysisk dato**-felt).

3. I oversigtspanelet **Poster, der skal indgå** kan du vælge bestemte aktiver, aktivtyper eller ressourcer til den automatiske opdatering. Vælg **filter**, og foretag de relevante valg.

4. I oversigtspanelet **Kør i baggrunden** kan du konfigurere automatisk opdatering som et batchjob efter behov.

    I illustrationen nedenfor vises et eksempel på dialogboksen **Opdater aktivtællere**.

    ![Figur 1.](media/12-work-orders.png)

5. Vælg **OK**. 

Når den automatiske opdatering aktivtælleren er fuldført, kan du få vist de tællerregistreringer, der er relateret til aktivet på siden **Aktivtællere**. Vælge **Styring af aktiver** > **Almindelig** > **Aktiver** > **Alle aktiver**, vælg aktivet, og vælg derefter **Tællere** i handlingsrudegruppen **Forebyggende** under fanen **Aktiv**.

På siden **Aktivaggregeret værdi** kan du få en oversigt over den seneste registrering, der er oprettet på alle tællertyper på alle aktiver. Vælg **Styring af aktiver** > **Forespørgsler** > **Aktiver** > **Aktivaggregeret værdi**. Denne side ligner siden **Aktivtællere**, men du kan ikke tilføje eller redigere registreringer. Den er kun til gennemsyn.

I illustrationen nedenfor vises et eksempel på siden **Aktivaggregeret værdi**.

![Figur 2.](media/13-work-orders.png)

Vær opmærksom på følgende punkter:

- Du kan stadig oprette manuelle tællerværdiregistreringer for tællertyper, der opdateres automatisk. Se afsnittet [Manuel opdatering af aktivtællere](../work-orders/manual-update-of-asset-counters.md) for at få yderligere oplysninger.

- Du kan oprette tællere, der er relateret til en anden tæller. I dette tilfælde opdateres relaterede tællere automatisk, når en tæller opdateres. Du kan finde flere oplysninger om, hvordan du konfigurerer relaterede tællere, i [Tællere](../setup-for-objects/counters.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]