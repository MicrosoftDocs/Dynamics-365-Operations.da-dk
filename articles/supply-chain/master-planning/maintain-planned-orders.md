---
title: Vedligehold ordreforslag
description: Dette emne indeholder oplysninger om, hvordan du administrerer planlagte ordrer. Den beskriver, hvordan du kan opdatere status for planlagte ordrer, autorisere dem og filtrere for planlagte ordre, der har samme status som en valgte planlagt ordre.
author: roxanadiaconu
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ddf2c7b4c67bec6c29387c78d1fdb021d85d702
ms.sourcegitcommit: 620e15555d176eec3905b48d5001af1c50107ce6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2019
ms.locfileid: "1993434"
---
# <a name="maintain-planned-orders"></a>Vedligehold ordreforslag

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om, hvordan du administrerer planlagte ordrer. Den beskriver, hvordan du kan opdatere status for planlagte ordrer, autorisere dem og filtrere for planlagte ordre, der har samme status som en valgte planlagt ordre.

Du kan administrere ordreforslag fra arbejdsområdet **Varedisponering**, listen **Ordreforslag** eller listerne **Produktionsordreforslag**, **Planlagte indkøbsordrer** og **Planlagt overførsel**. 

## <a name="planned-order-status"></a>Status for ordreforslag
Du kan bruge feltet **Status** til at registrere status. Følgende værdier bruges:

-   Når varedisponering opretter ordreforslag, har ordreforslagene statussen **Ubehandlet**.
-   Hvis du vælger ikke at autorisere et ordreforslag, kan du tildele det statussen **Fuldført**.
-   Hvis du vil autorisere et ordreforslag, kan du ændre status til **Godkendt**. Ordreforslag med **Godkendt** status respekteres af varedisponeringen, så de ændres eller slettes ikke. 

## <a name="firming-planned-orders"></a>Autorisering af ordreforslag 
Når ordreforslag autoriseres, oprettes rigtige ordrer. Disse kaldes også *frigivne* eller *åbne ordrer*. Når et ordreforslag er autoriseret, flyttes det til ordresektionen i det relevante modul.

Du kan vælge to autorisationsindstillinger på siden **Ordreforslag**:

-   **Autoriser** – Dette autoriserer et eller flere valgte ordreforslag.
-   **Autoriser alle** – Dette autoriserer alle ordreforslag i filteret. Når du bruger **Autoriser alle**, behøver du ikke vælge ordreforslaget, da alle ordreforslag i filtret autoriseres. Denne indstilling kan være nyttig, hvis du skal autorisere et stort antal ordreforslag.

> [!NOTE]
> Du kan spore et ordreforslag, der er autoriseret, fra **Autorisationshistorik** under **formen Ordreforslag > Vis > Autorisationshistorik**.

## <a name="parallelize-firming"></a>Parallel autorisation
Hvis du planlægger at autorisere mange ordrer på samme tid, kan parallelisering af afviklingen forbedre kørselstiden eller ydeevnen. Denne indstilling er tilgængelig, når der autoriseres flere ordreforslag med enten **Autoriser** eller **Autoriser alle**. Følgende parametre er tilgængelige:

-   **Paralleliser autorisation** – Hvis den er **Ja**, vil autorisationsprocessen blive parallel med det antal tråde, der er defineret i **Antal tråde**.
-   **Antal tråde** – Styrer antallet af tråde, der bruges til at parallelisere autorisationsprocessen. Parameteren vises kun, når **Paralleliser autorisation** er angivet til **Ja**.


<a name="additional-resources"></a>Yderligere ressourcer
--------

[Behovsplaner](master-plans.md)



