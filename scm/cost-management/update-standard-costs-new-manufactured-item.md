---
title: Opdatere standardomkostninger for en ny produceret vare
description: Denne artikel indeholder en vejledning til opdatering af standardomkostninger for en ny produceret vare.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79693
ms.assetid: ba64b70f-3f4c-4373-9a7d-8fd07c45a8cf
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d8f1b5614811faad3fda15809e4e606c93e6b786
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="update-standard-costs-for-a-new-manufactured-item"></a>Opdatere standardomkostninger for en ny produceret vare

[!include[banner](../includes/banner.md)]


Denne artikel indeholder en vejledning til opdatering af standardomkostninger for en ny produceret vare. 

I følgende retningslinjer antages det, at du bruger en tilgang med to versioner til at opdatere standardomkostningerne. I denne tilgang indeholder én efterkalkulationsversion de standardomkostninger, der første blev defineret for den frosne periode, og den anden efterkalkulationsversion indeholder de trinvise opdateringer, der vedrører de nye færdigvarer. De trinvise opdateringer angives som omkostningsposter i den anden efterkalkulationsversion, og de aktiveres til sidst. I tilgangen med to versioner skal du definere en anden efterkalkulationsversion. Her er retningslinjerne for, hvordan denne efterkalkulationsversion skal defineres:

-   Tildel efterkalkulationstypen **Standardomkostninger**.
-   Tildel et tydeligt id, der angiver indholdet i efterkalkulationsversionen, f.eks. **2016-OPDATERINGER**.
-   I feltgruppen **Tillad pristype** skal du sikre dig, at **Kostpris** er indstillet til **Ja**.
-   Tillad, at omkostningsposter angives for alle steder (det vil sige, lad feltet **Sted**stå tomt). Hvis du angiver et sted, kan omkostningsposter kun angives for det pågældende sted.
-   Brug reserveprincippet **Aktiv**.

Hvis du vil tilføje nye produktionsvarer i løbet af den frosne periode, skal du følge disse trin.

1.  Brug siden **Opsætning af efterkalkulationsversion** for at gøre det muligt at indtaste omkostningsposter i den anden efterkalkulationsversion, der indeholder de trinvise opdateringer. Undgå at aktivere ventende omkostninger, hvor aktivering er tilladt, når ventende omkostninger er fuldstændigt og nøjagtigt defineret. Angiv en tom fra-dato som en politik i efterkalkulationsversionen, og angiv derefter fra-datoen, når du indtaster de enkelte omkostningsposter. Fra-datoen skal repræsentere en dato, der ligger før den dato, hvor de nye varer købes eller produceres.
2.  Brug siden **Varepris** til at indtaste omkostningsposter for nye købte varer. For de enkelte omkostningsposter skal du angive den efterkalkulationsversion, der indeholder trinvise opdateringer, og bruge en fra-dato, der ligger før den forventede produktionsdato for nye færdigvarer.
3.  Beregn omkostningerne for nye færdigvarer ved hjælp af siden **Beregning**. Åbn siden **Beregning** fra siden **Vedligeholdelse af efterkalkulationsversion** og vælg derefter den efterkalkulationsversion, der indeholder de trinvise opdateringer. Brug udvælgelseskriterierne til at angive de nye færdigvarer og eventuelle producerede komponenter. I en struktur med flere produkter kan det også være nødvendigt at angive en overordnet vare, der indeholder nye færdigvarer som en komponent. Angiv en fra-dato for beregning af styklisten, der svarer til startdatoen for produktion af de nye færdigvarer. Fra-datoen skal ligge inden for ikrafttrædelsesdatoerne for varens styklisteversion og ruteversion. **Bemærk!** En manglende omkostningspost kan angive en ny færdigvare. Beregninger af styklister kan begrænses til varer med manglende omkostninger.
4.  Kontrollér, om de beregnede omkostninger for nye færdigvarer er komplette og korrekte. Brug siden **Fuldført** til at gennemgå de beregnede omkostninger for hver vareomkostningspost og enhver infolog med advarsler. Du kan også bruge siden **Beregning** til at få vist en oversigt over de beregnede omkostninger.
5.  Brug siden **Opsætning af efterkalkulationsversion** til at skifte blokeringsflag for at tillade aktivering af ventende omkostningsposter i den anden efterkalkulationsversion.
6.  Brug siden **Aktivér priser** (som du kan åbne fra siden **Vedligeholdelse af efterkalkulationsversion**) til at aktivere alle ventende omkostningsposter i den anden efterkalkulationsversion. Du kan også aktivere de ventende omkostningsposter for individuelle varer ved at klikke på knappen **Aktivér** på siden **Varepris**.
7.  Du kan bruge siden **Opsætning af efterkalkulationsversion** til at skifte blokeringsflag i den anden efterkalkulationsversion for at undgå yderligere vedligeholdelse af data. Blokeringspolitikkerne vil forhindre, at der indtastes nye ventende omkostninger eller aktiveres ventende omkostninger.





