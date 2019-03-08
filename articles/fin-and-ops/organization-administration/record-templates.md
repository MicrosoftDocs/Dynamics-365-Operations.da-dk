---
title: Postskabeloner
description: Denne artikel introducerer begrebet postskabeloner, og forklarer, hvordan de kan bruges til at oprette poster, der deler oplysninger.
author: pvillads
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 426fd8fafec061b649cbb31109ffe8fabc24917d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "323565"
---
# <a name="record-templates"></a>Postskabeloner

[!include [banner](../includes/banner.md)]

Denne artikel introducerer begrebet postskabeloner, og forklarer, hvordan de kan bruges til at oprette poster, der deler oplysninger.

Med postskabeloner kan du hurtigere oprette poster i Microsoft Dynamics 365 for Finance and Operations. Du kan kun oprette postskabeloner for nogle af posttyperne i Microsoft Dynamics 365 for Finance and Operations.

Forestil dig f.eks., at du indtaster lejeoplysninger for et biludlejningsfirma, der er placeret i San Francisco. Da de fleste af kunderne sandsynligvis er fra San Francisco-området, ville det være rart, hvis du automatisk kunne udfylde værdier i felterne **Stat**, **Land** og **By** på udlejningsblanketten.

> [!NOTE]
> Du kan kun anvende skabeloner for de områder i Finance and Operations, du har adgang til. Men du får vist alle skabelontitler, der er synlige, når du opretter en ny post, og det samme gør andre brugere, hvis du opretter skabeloner, der er tilgængelige for alle brugere. Det bør du have med i dine overvejelser, når du navngiver skabeloner. Undgå f.eks. at bruge navne, der indeholder ord som "provision", hvis det er fortroligt, at nogle medarbejdere i virksomheden, har provisionsbaseret løn.

Når en eller flere skabeloner, som du har adgang til, findes til en bestemt form, og du forsøger at oprette en ny post i formen, vises siden **Vælg en skabelon til**. Når du vælger en skabelon på listen, oprettes den nye post, som indeholder standardoplysninger, der er baseret på den skabelon, du har valgt. Hvis du ikke vil bruge skabeloner, når du opretter nye poster, skal du markere afkrydsningsfeltet **Spørg ikke igen** på siden **Vælg en skabelon for**. Hvis du vil have vist dialogboksen til valg af skabeloner igen, skal du højreklikke på en post, klikke på **Postoplysninger** og derefter klikke på **Vis skabelonvalg**.
