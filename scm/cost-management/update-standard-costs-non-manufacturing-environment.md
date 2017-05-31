---
title: "Opdatere standardomkostninger i et ikke-produktionsmiljø"
description: "Denne artikel indeholder vejledning i at opdatere standardomkostninger i et ikke-produktionsmiljø."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 472b977dcffb4cadb91621586763e0fd471d5c46
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a>Opdatere standardomkostninger i et ikke-produktionsmiljø

[!include[banner](../includes/banner.md)]


Denne artikel indeholder vejledning i at opdatere standardomkostninger i et ikke-produktionsmiljø.

I følgende retningslinjer antages det, at du bruger en tilgang med to versioner til at opdatere standardomkostning. I denne tilgang indeholder den ene efterkalkulationsversion de standardomkostninger, der oprindeligt blev defineret for den frosne periode, og den anden efterkalkulationsversion indeholder de trinvise opdateringer. De enkelte opdateringer angives som en omkostningspost i den anden efterkalkulationsversion, og den aktiveres til sidst. Der kan også bruges en tilgang med én version, hvor der gøres brug af det sæt standardomkostninger, der oprindeligt blev defineret. I tilgangen med to versioner skal du definere en anden efterkalkulationsversion. Her er retningslinjerne for, hvordan denne efterkalkulationsversion skal defineres:

-   Tildel efterkalkulationstypen **Standardomkostninger**.
-   Tildel et beskrivende id, der angiver indholdet af efterkalkulationsversionen, f.eks. **2016-OPDATERINGER**.
-   Sørg for, at indholdet omfatter omkostningsposter.
-   Tillad, at der kan angives omkostningsposter for alle steder. Hvis du angiver et sted, kan omkostningsposter kun angives for det pågældende sted.
-   Angiv **Ingen** som beredskabsprincip. Beredskabsprincippet anvendes kun til omkostningsberegninger for producerede varer.

Hvis du vil rette, justere eller opdatere standardomkostningerne for nye varer, skal du udføre disse trin.

1.  Brug siden **Opsætning** **af efterkalkulationsversion** for at gøre det muligt at indtaste omkostningsdataene i den anden efterkalkulationsversion. Du kan vælge at forhindre aktivering af ventende omkostninger, så aktiveringen bliver tilladt, når de ventende omkostninger er fuldstændigt og korrekt defineret. Du kan også vælge at indsætte en dato i feltet **Fra dato**. Som en generel retningslinje kan du bruge datoen for, hvornår du regner med at aktivere de trinvise opdateringer. Du kan også lade feltet **Fra dato** være tomt for efterkalkulationsversionen og derefter angive en dato i feltet **Fra dato** for de enkelte omkostningsposter.
2.  Brug siden **Varepris** til at angive opdateringer som vareomkostningsposter i den anden efterkalkulationsversion.
3.  Brug rapporten **Varepriser** til at kontrollere, at vareomkostningsposterne i den anden efterkalkulationsversion er fuldstændige og nøjagtige.
4.  Brug siden **Vedligeholdelse af efterkalkulationsversion** til at skifte blokeringsflag for at tillade aktivering af ventende omkostningsposter i den anden efterkalkulationsversion.
5.  Brug siden **Aktivér priser** (som du kan åbne fra siden **Vedligeholdelse af efterkalkulationsversion**) til at aktivere alle ventende vareomkostningsposter, der er omfattet af den anden efterkalkulationsversion. Du kan også aktivere de ventende omkostningsposter for individuelle varer ved at klikke på knappen **Aktivér afventende pris(er)** på siden **Varepris**.
6.  Du kan undgå yderligere vedligeholdelse af data ved at bruge siden **Opsætning af efterkalkulationsversion** til at skifte blokeringsflag i den anden efterkalkulationsversion. Blokeringspolitikkerne vil forhindre, at der angives nye ventende omkostninger eller aktiveres ventende omkostninger.





