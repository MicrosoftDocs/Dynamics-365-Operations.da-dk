---
title: Udelukke produkter, der har specifikke livscyklustilstande
description: Dette emne forklarer, hvordan du kan udelukke produkter baseret på deres livscyklustilstand, når planlægningsoptimeringsfunktionen bruges.
author: ChristianRytt
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 371d98eefa482fc3e430f2f0977ddffb9dd0d30e
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645085"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a>Udelukke produkter, der har specifikke livscyklustilstande

[!include [banner](../../includes/banner.md)]

Frigivne produkter og frigivne produktversioner indeholder feltet **Status for produktlivscyklus**. I dette felt kan du blandt andet kontrollere, hvilke produkter der indgår i varedisponeringen. Du kan tilføje, fjerne og redigere livscyklustilstande efter behov ved at gå til **Administration af produktoplysninger \> Konfiguration \> Status for produktlivscyklus**. For hver produktlivscyklustilstand skal du angive indstillingen **Er aktiv for planlægning** til *Ja*, hvis produkter, der har den pågældende tilstand, skal medtages under varedisponeringen. Når indstillingen er angivet til *Nej*, udelukkes de tilknyttede produkter og varianter fra alle varedisponeringer og alle beregninger på styklisteniveau.

Frigivne produkter og varianter, hvor feltet **Produktets livscyklustilstand** er tomt, behandles, som om der er en produktlivscyklustilstand, hvor indstillingen **Er aktiv for planlægning** angivet til *Ja*. De vil med andre ord blive medtaget under varedisponeringen.

> [!NOTE]
> For at undgå unødvendige leveringsforslag anbefaler vi på det kraftigste, at du knytter alle forældede frigivne produkter og varianter sammen med en produktlivscyklustilstand, hvor indstillingen **Er aktiv for planlægning** er angivet til *Nej*. Denne fremgangsmåde er særlig vigtig, når du arbejder med produktkonfigurationsvarianter, der ikke kan genbruges, fordi den vil hjælpe med at forhindre spild.

## <a name="related-resources"></a>Tilknyttede ressourcer

Yderligere oplysninger om produktlivscyklustilstand finder du under [Oversigt over produktlivscyklustilstand](../../pim/product-lifecycle.md).

Du kan finde detaljerede oplysninger om, hvordan du kan bruge statusser for produktlivscyklus til at udelukke produkter fra varedisponering og beregning af styklisteniveau, under [Oprette en status for produktlivscyklus for at udelukke produkter fra varedisponering](../../pim/tasks/exclude-products-master-planning.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]