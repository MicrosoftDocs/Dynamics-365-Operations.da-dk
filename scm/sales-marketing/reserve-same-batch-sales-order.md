---
title: Reserver den samme batch til en salgsordre
description: I denne artikel beskrives det, hvordan du konfigurerer et produkt til at tillade reservation af lager i forhold til et enkelt batch af lageret.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: a24e5c2972ae1581de43ebcb448ed34bafdc0ad5
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017


---

# <a name="reserve-the-same-batch-for-a-sales-order"></a>Reserver den samme batch til en salgsordre

[!include[banner](../includes/banner.md)]


I denne artikel beskrives det, hvordan du konfigurerer et produkt til at tillade reservation af lager i forhold til et enkelt batch af lageret.

Hvis du reserverer fra samme batch, kan du reservere lager til en salgsordrelinje i forhold til en enkelt lagerbatch. En kunde, der f.eks. bestiller tapet, kan anmode om, at hele ordren skal bestilles fra det samme batch eller parti for at undgå, at rullerne er forskellige. Hvis du vil konfigurere et produkt, så den anvender den samme batchreservation, skal følgende indstillinger være aktive i den varemodelgruppe, sporingsdimensionsgruppe og lagringsdimensionsgruppe, du knytter til produktet.

-   **Varemodelgrupper** – For varemodelgruppen skal felterne **Valg af samme batch** og **Konsolider krav** være valgt for feltgruppen **Reservation** for lagerpolitikker.
-   **Sporingsdimensionsgrupper** – For sporingsdimensionsgruppen skal feltet **Disponer pr. dimension** være valgt for batchnummeret.
-   **Lagringsdimensionsgrupper** – For lagringsdimensionsgruppen skal feltet **Disponer pr. dimension** være valgt for **Lokation** og **Lagersted**.

Når du reserverer lager til et produkt på en salgsordrelinje, der er konfigureret til valg af samme batch, forsøger Microsoft Dynamics 365 for Finance and Operations at reservere den mængde, der er bestilt fra en enkelt lagerbatch. Der tages også højde for eventuelle specifikke krav til batchattributter. Hvis antallet ikke kan opfyldes fra en enkelt batch, vises siden **Konflikt ved reservation af samme batch**. Denne side beskriver problemerne og de handlinger, du kan udføre for at fortsætte reservationen. Følgende betingelser kan forhindre, at batchen kan reserveres:

-   Dispositionskoden for batchen har **Spær reservation** for salg angivet til **Blokeret**.
-   Batchen er udløbet på baggrund af udløbsdatoen og eventuelle salgbare dage for debitor. Varen kan stadig reserveres, hvis varemodelgruppen for varen er angivet til FEFO-datokontrolleret, og hvis sidste holdbarhedsdato er angivet under Kriterier for plukning.
-   Batchen har ikke tilstrækkelige hyldelevetidsdage tilbage baseret på udløbsdatoen og sidste holdbarhedsdato samt eventuelle salgbare dage for debitor.





