---
title: Oprette dimensioner og importere dimensionsmedlemmer
description: Driftsregnskab er et uafhængigt modul, der kræver masterdata fra andre moduler.
author: ShylaThompson
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 610a9302610af7a074a91dfc2a8c87725b0a1a82
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009487"
---
# <a name="create-dimensions-and-import-dimension-members"></a>Oprette dimensioner og importere dimensionsmedlemmer

[!include [banner](../includes/banner.md)]

Driftsregnskab er et uafhængigt modul, der kræver data fra andre moduler. Disse data er kategoriseret som følgende:

-  Omkostningselementer
-  Omkostningsobjekter
-  Statistiske dimensioner

Et **omkostningselement** svarer til et omkostningsrelevant element i kontoplanen. Et **omkostningsobjekt** svarer til alle typer økonomiske dimensioner, f.eks. produkter, bærere og projekter, du vil vurdere, allokere omkostninger til eller måle direkte. En **statistisk dimension** og dens medlemmer bruges til registrering af ikke-pengemæssige poster. Statistiske dimensionsmedlemmer kan bruges som fordelingsbasis i omkostningsdistribution og omkostningsfordeling. 

I følgende diagram illustreres de dimensioner, der bruges i forbindelse med driftsregnskab.

[![Dimensioner for omkostningsregnskab](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)

Når dataene importeres til driftsregnskab, kan du bruge dem til at oprette forskellige perspektiver, der giver indsigt for ledere på alle niveauer i organisationen. Følgende emner indeholder oplysninger om oprettelse af dimensioner og import af dimensionsmedlemmer. 

-  [Dimensioner for omkostningselement](cost-elements.md)
-  [Oprette omkostningselementer](./tasks/create-cost-elements.md)
-  [Dimensioner for omkostningsobjekt](cost-objects.md)
-  [Knytte dimensionsmedlemmer for omkostningselement til et fælles sæt dimensionsmedlemmer](map-cost-elements-dimension-members.md)
-  [Tilknytte en dimension for omkostningselement](./tasks/map-cost-element-dimension.md)
-  [Skabeloner for statistiske dimensionsmedlemmer og providere af statistiske målinger](statistical-measure-provider-template.md)








[!INCLUDE[footer-include](../../includes/footer-banner.md)]