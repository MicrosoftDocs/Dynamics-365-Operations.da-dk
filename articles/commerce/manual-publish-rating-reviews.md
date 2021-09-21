---
title: Aktiver manuel udgivelse af vurderinger og vurderinger af en dag
description: Dette emne beskriver, hvordan du aktiverer manuel udgivelse af vurderinger fra et afsnit i Microsoft Dynamics 365 Commerce, og hvordan du manuelt udgiver vurderinger.
author: gvrmohanreddy
manager: annbe
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: ebf104502783cf4046dc7b265a7ecda30cf2e8cf
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472586"
---
# <a name="enable-manual-publishing-of-ratings-and-reviews-by-a-moderator"></a>Aktiver manuel udgivelse af vurderinger og vurderinger af en dag

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emne beskriver, hvordan du aktiverer manuel udgivelse af vurderinger fra et afsnit i Microsoft Dynamics 365 Commerce, og hvordan du manuelt udgiver vurderinger.

Dynamics 365 Commerce-løsningen med vurderinger bruger Azure Cognitive Services til automatisk at ændre bedømmelser og indhold og til at publicere vurderinger. Derfor behøver du ikke manuel handling for at gennemse og publicere vurderinger på dit e-handelswebsted.

Nogle virksomheder vil dog foretrække, at vurderinger gennemses og godkendes manuelt, før de publiceres. Hvis du vil aktivere manuel udgivelse af vurderinger og vurderinger fra en webside, skal du aktivere funktionen **Kræv godkendelse til vurderinger** i Commerce Site Builder.

## <a name="enable-the-require-moderator-for-ratings-and-reviews-feature-in-commerce-site-builder"></a>Aktivere funktionen Kræv vurderinger og gennemsyn i Commerce site builder

Aktivere funktionen **Kræv vurderinger og gennemsyn** i Commerce site builder ved at følge disse trin.

1. Gå til **Startside \> Anmeldelser \> Indstillinger**.
1. Angiv indstillingen **Kræv vurderinger og gennemsyn** til **Til**.

> [!NOTE]
> Hvis du aktiverer funktionen **Kræv godkendelse til vurderinger og gennemsyn**, stopper du den automatiske udgivelse af vurderinger, så manuel udgivelse nu er påkrævet. Azure Cognitive Services vil dog fortsætte med at redigere i evalueringstitler og -indhold.

<!--![Require moderator for ratings and reviews setting in Commerce site builder.](media/Ratings-reviews-settings-human-moderation.png)-->

## <a name="publish-ratings-and-reviews"></a>Udgiv vurderinger og anmeldelser

Hvis du vil aktivere manuel udgivelse af vurderinger og vurderinger fra en webside, skal du aktivere funktionen **Kræv godkendelse til vurderinger** i Commerce Site Builder.

Hvis du vil se vurderings- og anmeldelsestendenser i Commerce-webstedsgenerator, skal du følge disse trin.

1. Gå til **Anmeldelser \> Redigering**.
1. Hvis feltet **Status** for en række er angivet til **Ikke publiceret**, er vurderingen og gennemgangen i den pågældende række endnu ikke publiceret. Hvis du kun vil have vist ikke-publicerede vurderinger og gennemsyn, skal du vælge **Status: Skal gennemses** i statusfilteret over gitteret.
1. Vælg en eller flere vurderinger og gennemsyn, der har statussen **Ikke-publiceret**, og vælg derefter **Udgiv** på kommandolinjen. De valgte vurderinger og vurderinger føjes til udgivelseskøen og vises på e-handelswebstedet, når de er publiceret.

> [!NOTE]
> - Når en vurdering og evaluering er publiceret, ændres statusværdien fra **Ikke-udgivet** til en NULL-værdi (et tomt felt).
> - Hvis du vælger flere vurderinger og vurderinger med blandet status, og derefter vælger du **Udgiv**, vurderinger og vurderinger, som ikke er publiceret endnu, vil blive publiceret. Vurderinger og vurderinger, der allerede er udgivet, vil dog ikke blive publiceret igen.

I følgende illustration vises et eksempel, hvor der er valgt tre ikke-publicerede vurderinger og evalueringer på siden **Redigering** i Commerce Site Builder.

![Tre ikke-publicerede vurderinger og vurderinger, der er valgt på siden Redigering i Commerce Site Builder.](media/Ratings-reviews-publishing-reviews.png)

<!--![Dynamics 365 Commerce - Ratings and Review configuration 2](media/Ratings-reviews-published-reviews.png)-->
<!--![Status filter](media/Ratings-reviews-published-reviews-status-filter.png)-->

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over vurderinger og anmeldelser](ratings-reviews-overview.md)
