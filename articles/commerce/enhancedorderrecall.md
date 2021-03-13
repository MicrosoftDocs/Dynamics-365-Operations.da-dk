---
title: Handling for tilbagekald af ordre i POS
description: Dette emne indeholder en beskrivelse af de funktionsegenskaber, der er tilgængelige på forbedrede sider med tilbagekaldsordrer i POS.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 21e8045d754006345f5ad68e1e67579386c6df4a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010068"
---
# <a name="recall-order-operation-in-pos"></a>Handling for tilbagekald af ordre i POS

[!include [banner](includes/banner.md)]

Handlingen **Tilbagekald af ordre** i Commerce POS indeholder har opdaterede søge- og filtreringsfunktioner for ordren samt ordrespecifikke oplysninger. Denne funktion er tilgængelig i Commerce version 10.0.15 og nyere.

Hvis du vil aktivere denne funktion, skal du deaktivere **Forbedret handling for ordretilbagekald i POS**-funktionen i arbejdsområdet **Funktionsstyring** i Commerce Headquarters. Når du har aktiveret funktionen, bør du overveje at opdatere [skærmlayout](pos-screen-layouts.md) i POS for at udnytte nogle af de ændrede muligheder.

Konfigurationen af handlingsknappen **Tilbagekald ordre** giver organisationer mulighed for at implementere handlingen med en foruddefineret skærm.

![Konfiguration af knapmatrix](media/recallorderbuttongrid.png)

Der findes følgende skærmindstillinger.
- **Ingen** – Denne indstilling installerer handlingen uden en bestemt visning. Når en bruger åbner handlingen med denne konfiguration, vil de blive bedt om at søge efter og finde ordrer eller vælge fra et foruddefineret ordrefilter.
- **Ordrer, der skal opfyldes** – Når en bruger starter handlingen, køres der automatisk en forespørgsel for at søge efter og få vist en liste over ordrer, der skal opfyldes af butikken. Disse ordrer er konfigureret til butiksafhentning eller butiksafsendelse, og linjerne i disse ordrer er endnu ikke plukket eller pakket.
- **Ordrer, der skal afhentes** – Når en bruger starter handlingen, køres der automatisk en forespørgsel for at søge efter og få vist en liste over ordrer, der er konfigureret til afhentning i brugerens aktuelle butik.
- **Ordrer, der skal leveres** – Når en bruger starter handlingen, køres der automatisk en forespørgsel for at søge efter og få vist en liste over ordrer, der er konfigureret til levering fra brugerens aktuelle butik.

Når du starter handlingen **Tilbagekald ordre** fra POS, hvis visningen er konfigureret til **Ingen**, kan brugeren søge efter og hente ordrer på en af følgende måder.
- Scan ordrestregkoder. Dette søger efter match i felter med ordrenummer, kanalreference og kvitterings-id.
- Vælg ikonet **Søg efter ordrer** eller **Søg og filtrer** på applinjen for at bruge filtreringsmekanismen til at finde ordrer, der opfylder filterkriterierne.
- Vælg mellem et foruddefineret filter fra rullemenuen **Vis ordrer** (ordrer, der skal opfyldes, ordrer, der skal afhentes, eller ordrer, der skal leveres).

![RecallOrderMainMenu](media/recallordermain.png)

Når søgekriterierne er anvendt, vises der en liste over tilsvarende salgsordrer i programmet.

![RecallOrderDetail](media/orderrecalldetail.png)

En bruger kan vælge en ordre på listen for at få vist flere detaljer. I panelet med oplysninger i højre side af skærmen vises der oplysninger om den valgte ordre, herunder ordrelinjedetaljer, leveringsdetaljer og oplysninger om opfyldning.

Fra applinjen kan en bruger vælge en operation. Afhængigt af status for ordren er det ikke sikkert, at bestemte handlinger er aktiveret.

- **Returner** – Udfører en returnering for en eller flere fakturaer, der er relateret til den valgte kundeordre.

- **Annuller** – Udsted en fuld annullering af den valgte salgsordre.

- **Opfyld** – Overfører brugeren til siden med ordreopfyldning, som er filtreret for den valgte ordre. Det er kun de ordrelinjer, der er åbne for opfyldelse af brugerens butik for den valgte ordre, der vises.

- **Rediger** – Giver brugerne mulighed for at foretage ændringer i den valgte kundeordre.

- **Afhent** – Starter afhentningsflowet, hvilket giver brugeren mulighed for at vælge de produkter, der skal afhentes, og opretter salgsposteringen for afhentning.
