---
title: Udsende arbejdsordre
description: Dette emne beskriver, hvordan du udsender en arbejdsordre i Styring af aktiver.
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
ms.openlocfilehash: 3b1621cf0f1e47d7bd5fe2fa0b41fbcd61f14def
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887199"
---
# <a name="dispatch-work-order"></a>Udsende arbejdsordre

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Du kan planlægge en arbejdsordre eller arbejdsordrejob til én arbejder ved hjælp af funktionen **Udsend**.

1. Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Vælg arbejdsordren på listen.

3. Klik på **Udsend** under fanen **Generelt**.

4. Vælg arbejderen i feltet **Arbejder** i dialogboksen **Planlæg arbejdsordre**.

5. I feltet **Planlæg timer** kan du indsætte forventede arbejdstimer i tilfælde af, at arbejdstimerne er forskellige fra budgetterede timer.

6. I feltet **Planlagt start** kan du redigere startdato og -tidspunkt, hvis det er nødvendigt.

7. Hvis planlægningsprocessen skal overholde kapacitetsbegrænsningerne for ressourcer, der allerede er planlagt på andre job, skal du sørge for, at til/fra-knapperne **Aktiv**, **Værktøj** og **Arbejder** er indstillet til "Ja". Hvis du vil have vist detaljerede oplysninger om planlægningsprocessen, skal du vælge "Ja" på knappen **Detaljeret**. Det betyder, at der vises detaljerede oplysninger om de beregnede scorer for arbejdsordren i infologgen.

8. Vælg "Ja" på til/fra-knappen **Ignorer tidsplan** at ignorere lukkede dage i kalenderen (gælder for aktiv, arbejder og værktøjer). Vælg "Ja" på til/fra-knappen **Ignorer planlagt udførelse** for at ignorere begrænsninger, der muligvis er valgt på arbejdsordren vedrørende planlægning. Se afsnittet [Planlagt udførelse](../setup-for-work-orders/scheduled-execution.md) for at få oplysninger om opsætningen af planlagt udførelse.

9. Klik på **OK**. Arbejdsordrens livscyklustilstand opdateres automatisk til den "Planlagte" livscyklustilstand, der er angivet for **Styring af aktiver** > **Opsætning** > **Arbejdsordrer** > **Livscyklusmodeller**.

I figuren herunder vises et eksempel på udsendelsesvalg i dialogboksen **Planlægning arbejdsordre**.

![Figur 1](media/04-work-order-scheduling.png)

>[!NOTE]
>Hvis du vil slette tidsplanen på en arbejdsordre, skal dette gøres ved at vælge arbejdsordren i **Alle arbejdsordrer** og klikke **Slet tidsplan** under fanen **Generelt**. Husk at opdatere arbejdsordrens livscyklustilstand manuelt, hvis du sletter tidsplanen.
