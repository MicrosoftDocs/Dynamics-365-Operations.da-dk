---
title: Fejlfinding af analyserapporter
description: I denne artikel beskrives det, hvad du skal gøre, hvis en kundes dataændringer ikke vises i nogen af kundens arbejdsområder.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8dab12213e9730e72aede70c5b5d1368ef77664e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053533"
---
# <a name="troubleshoot-analytic-reports"></a>Fejlfinding af analyserapporter

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Udsted**

En kundes dataændringer vises ikke under **Analyse**-fanerne i nogen af kundens arbejdsområder.

**Årsag**

Som standard opdateres Microsoft Power BI-rapporter hver fjerde time inden for fristerne for batchjobbet Installer måling.

**Løsning**

Dette problem er muligvis kun et spørgsmål om timing. Følg disse trin for at starte batchjobbet og opdatere analysearbejdsområderne.

1. Åbn siden **Batchjob** på **Systemadministration \> Links \> Batchjob \> Batchjob**. Du kan også bruge funktionen Søg og skrive **Batchjob**.
1. Find jobbet **Installer måling** på listen.
1. Vælg **Rediger** øverst på siden, og indstil den planlagte startdato/-klokkeslæt til en værdi, der opdaterer analysen, så den er tættere på det aktuelle tidspunkt.

![Batchjob](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]