---
title: Fejlfinding af analyserapporter
description: Dette emne beskriver, hvordan du finder fejl og diagnosticerer problemer, hvis en kundes dataændringer ikke vises i nogen af kundens arbejdsområder.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6ea04c06858cc98b0e233b9133d9dfbebfe59fd6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067723"
---
# <a name="troubleshoot-analytic-reports"></a>Fejlfinding af analyserapporter


[!INCLUDE [PEAP](../includes/peap-2.md)]

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

![Batchjob.](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
