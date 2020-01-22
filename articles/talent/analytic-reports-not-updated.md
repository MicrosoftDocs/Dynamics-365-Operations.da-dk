---
title: Analyserapporter opdateres ikke
description: I dette emne beskrives, hvad du skal gøre, hvis en kundes dataændringer ikke vises i nogen af kundens arbejdsområder.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fc2e6259a8f9d17dc0f7652f207acfa53da76a8d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898567"
---
# <a name="analytic-reports-are-not-updated"></a>Analyserapporter opdateres ikke

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
