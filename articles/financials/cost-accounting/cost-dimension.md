---
title: Oprette dimensioner og importere dimensionsmedlemmer
description: "Driftsregnskab er et uafhængigt modul, der kræver masterdata fra andre moduler."
author: YuyuScheller
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0fb276e7d62e2f7c02934e74741c8cf74778fc12
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="create-dimensions-and-import-dimension-members"></a>Oprette dimensioner og importere dimensionsmedlemmer

[!include[banner](../includes/banner.md)]

Driftsregnskab er et uafhængigt modul, der kræver data fra andre moduler. Disse data er kategoriseret som følgende:

-  Omkostningselementer
-  Omkostningsobjekter
-  Statistiske dimensioner

Et **omkostningselement** svarer til et omkostningsrelevant element i kontoplanen. Et **omkostningsobjekt** svarer til alle typer økonomiske dimensioner, f.eks. produkter, bærere og projekter, du vil vurdere, allokere omkostninger til eller måle direkte. En **statistisk dimension** og dens medlemmer bruges til registrering af ikke-pengemæssige poster. Statistiske dimensionsmedlemmer kan bruges som fordelingsbasis i omkostningsdistribution og omkostningsfordeling. 

I følgende diagram illustreres de dimensioner, der bruges i forbindelse med driftsregnskab.

[![Dimensioner for omkostningsregnskab](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)

Når dataene importeres til driftsregnskab, kan du bruge dem til at oprette forskellige perspektiver, der giver indsigt for ledere på alle niveauer i organisationen. Følgende emner indeholder oplysninger om oprettelse af dimensioner og import af dimensionsmedlemmer. 

-  [Dimensioner for omkostningselement](cost-elements.md)
-  [Oprette omkostningselementer (Opgaveguide)](./tasks/create-cost-elements.md) (opgave guide)
-  [Dimensioner for omkostningsobjekt](cost-objects.md)
-  [Oprette omkostningselementer (Opgaveguide)](./tasks/create-cost-objects.md) (opgave guide)
-  [Knytte dimensionsmedlemmer for omkostningselement til et fælles sæt dimensionsmedlemmer](map-cost-elements-dimension-members.md)
-  [Tilknytte en dimension for omkostningselement (Opgaveguide)](./tasks/map-cost-element-dimension.md)
-  [Skabeloner for statistiske dimensionsmedlemmer og providere af statistiske målinger](statistical-measure-provider-template.md)






