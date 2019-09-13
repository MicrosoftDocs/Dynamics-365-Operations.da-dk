---
title: Automatisk opdatering af aktivtællere
description: I dette emne beskrives automatisk opdatering af aktivtællere i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875574"
---
# <a name="automatic-update-of-asset-counters"></a>Automatisk opdatering af aktivtællere

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

I forrige afsnit beskrives manuel registrering af aktivtællere. Opsætning af aktivtællere beskrives i [Tællere](../setup-for-objects/counters.md).

Tællerværdier kan også opdateres automatisk fra produktionsregistreringer, baseret på produktionstimer eller produktionsantal. Dette gøres i **Opdater aktivtællere**. Du kan opdatere et eller flere aktiver ved at indsætte én parameter, **Fra dato**. Denne parameter angiver startdatoen for produktionsregistreringer (timer eller produceret antal), hvilket vil sige den startdato, hvorfra tællerværdier skal opdateres.

Alle aktiver, der er relateret til en ressource *og* har aktivtællere, som er konfigureret til at blive opdateret på basis af produceret antal eller produktionstimer, medtages i en automatisk opdatering, og der oprettes nye tællerværdier.

Ved tællere baseret på produktionsantal er det antal gode og fejlmeldte antal, der medtages i optællingen. Hvis den enhed, der bruges til registrering af antal, er forskellig fra den enhed, der bruges på tælleren, omregnes antallet, så det svarer til tællerenheden.

Som nævnt ovenfor kan automatiske tællere opdateres fra produktionsregistreringer. Det aktiv, som du automatisk vil opdatere tællere for, skal derfor være relateret til en ressource (maskine). Følgende beskrivelser indeholder en oversigt over opsætning og behandling af produktionsordrer (i modulet **Produktionsstyring**), der bruges som grundlag for automatisk opdatering af tællere på et aktiv i modulet **Styring af aktiver**.

Når der er registreret producerede antal eller produktionstimer på ressourcen, kan du opdatere de relaterede aktivtællere.

1. Klik på **Styring af aktiver** > **Periodisk** > **Aktiver** > **Opdater aktivtællere**.

2. Vælg startdatoen for den automatiske opdatering i feltet **Fra-dato**.

>[!NOTE]
>Datoen i dette felt er datoen for "igangværende arbejde" fra **Ruteposteringer** (**Produktionsstyring** > **Forespørgsler og rapporter** > **Produktion** > **Ruteposteringer** > **Fysisk dato**-felt).

3. Hvis du vil vælge bestemte aktiver, aktivtyper eller ressourcer til den automatiske opdatering, skal du klikke på **Filter** i oversigtspanelet **Poster, der skal indgå** og foretage de relevante valg.

4. I oversigtspanelet **Kør i baggrunden** kan du konfigurere automatisk opdatering som et batchjob efter behov.

![Figur 1](media/12-work-orders.png)

5. Klik på **OK**. Når den automatiske opdatering af aktivoptælleren er udført, kan du se de tællerregistreringer, der relateret til aktivet, i **Aktivtællere** (**Styring af aktiver** > **Generelt** > **Aktiver** > **Alle aktiver** > vælg aktiv > knappen **Tællere**).

I **Totaler for aktivtæller** kan du få en oversigt over den seneste registrering, der er oprettet på alle tællertyper på alle aktiver. Klik på **Styring af aktiver** > **Forespørgsler** > **Aktiver** > **Aktivaggregeret værdi**. Visningen minder meget om **Aktivtællere**, men du kan ikke tilføje eller redigere registreringer i **Aktivaggregeret værdi**. Den er kun til oversigten.

![Figur 2](media/13-work-orders.png)


- Det er stadig muligt at oprette manuelle tællerværdiregistreringer for tællertyper, der opdateres automatisk. Se afsnittet "Manuel opdatering af aktivtællere" for at få yderligere oplysninger.
- Du kan definere tællere, der er knyttet til en anden tæller, hvilket betyder, at når en tæller opdateres, opdateres relaterede tællere automatisk samtidigt. Se emnet [Tællere](../setup-for-objects/counters.md) vedrørende opsætning af relaterede tællere.
