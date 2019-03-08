---
title: Analyserapporter opdateres ikke
description: I dette emne beskrives, hvad du skal gøre, hvis en kundes dataændringer ikke vises i nogen af kundens arbejdsområder.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "303701"
---
# <a name="analytic-reports-are-not-updated"></a>Analyserapporter opdateres ikke

[!include [banner](includes/banner.md)]

**Afgang**

En kundes dataændringer vises ikke under **Analyse**-fanerne i nogen af kundens arbejdsområder.

**Årsag**

Som standard opdateres Microsoft Power BI-rapporter hver fjerde time inden for fristerne for batchjobbet Installer måling.

**Løsning**

Dette problem er muligvis kun et spørgsmål om timing. Følg disse trin for at starte batchjobbet og opdatere analysearbejdsområderne.

1. Åbn siden **Batchjob** på **Systemadministration \> Links \> Batchjob \> Batchjob**. Du kan også bruge funktionen Søg og skrive **Batchjob**.
1. Find jobbet **Installer måling** på listen.
1. Vælg **Rediger** øverst på siden, og indstil den planlagte startdato/-klokkeslæt til en værdi, der opdaterer analysen, så den er tættere på det aktuelle tidspunkt.

![Batchjob](media/batch-jobs.png)
