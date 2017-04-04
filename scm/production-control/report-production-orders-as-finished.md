---
title: "Færdigmelde produktionsordrer"
description: "Færdigmeldingen er et trin i produktionen. På dette stadium er en færdigvare rapporteret og flyttes fra produktionsordren til lageret."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 19a777a8e58e3c8b848e878956b457a4a730f6e2
ms.lasthandoff: 03/31/2017


---

# <a name="report-production-orders-as-finished"></a>Færdigmelde produktionsordrer

Færdigmeldingen er et trin i produktionen. På dette stadium er en færdigvare rapporteret og flyttes fra produktionsordren til lageret.

Når en mængde af de færdige varer færdigmeldes på en produktionsordre, opdateres den som disponibel i lagret. Delmængder af den oprindeligt planlagte ordremængde kan færdigmeldes. Det er også muligt at indberette fejlmængder med en tilknyttet årsag til fejlen, når mængder færdigmeldes. Når produktionsordren når fasen Færdigmeldt, angives det, at ingen yderligere mængder færdigmeldes på produktionsordren.
Følgende egenskaber er også knyttet til processen **Færdigmelding**:
-   Det er muligt at konfigurere forbrug af råvarer og tid, der er proportional med den rapporterede mængde (baglænstræk)
-   Lægge på lager-arbejde kan oprettes for varer, der er aktiveret for lagerprocesser.
-   Den planlagte eller standardkostværdi for de færdige varer kan konfigureres til at blive rapporteret til finanskonti.
-   En kvalitetsordre kan oprettes for den rapporterede mængde baseret på konfigurationen af en kvalitetstilknytning.

Mængden, der er rapporteret til outputplaceringen. Lagerstedsarbejde genereres derefter for at flytte mængden fra outputplaceringen til den endelige destination, der er defineret af lokalitetsdirektivet for lægge på lager-arbejdet.

-   En kvalitetsordre kan oprettes, når en produktionsordre meldes færdig, hvis der er oprettet en kvalitetstilknytning.

## <a name="set-a-production-order-to-reporting-as-finished"></a>Konfigurer en produktionsordre, der skal færdigmeldes
Du kan konfigurere en produktionsordres status til **Færdigmelding** gennem den almindelige funktion til opdatering af produktionsordrer, gennem rute- eller jobkortkladder eller ved hjælp af kladden **Færdigmelding**. Du kan også opdatere fasen til **Færdigmelding** via siderne jobkortterminal og jobkortenhed, når du rapporterer på det sidste job i produktionsordren. Endelig kan du aktivere indstillingen **Færdigmelding** som en proces for lagerstedets håndholdte enhedsløsning.  


