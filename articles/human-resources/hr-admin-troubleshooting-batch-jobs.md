---
title: Optimere performance ved at planlægge batchjobs efter arbejdstid
description: Dette emne forklarer, hvordan du kan løse problemer med ydeevnen med Microsoft Dynamics 365 Human Resources ved at lægge batchjob, der kører i lang tid, efter arbejdstid.
author: andreabichsel
manager: AnnBe
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: f67b4b4c20345297f186c792fe2766c686e2ddbf
ms.sourcegitcommit: bdfc84aa7f607511981c0b2f20f03fabcb773510
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/23/2020
ms.locfileid: "3500499"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Optimere performance ved at planlægge batchjobs efter arbejdstid

## <a name="issue"></a>Udsted

Microsoft Dynamics 365 Human Resources kan opleve problemer med ydeevnen, hvis batchjob, der kører i lang tid, køres i almindelig åbningstid.

## <a name="resolution"></a>Løsning

Planlæg følgende batchjob til at blive kørt uden for arbejdstid. Det anbefales også, at du gennemgår hyppigheden af batchjob, der køres ofte. Hvis det er muligt, skal du reducere gentagelsen af batchjobbet. I mange tilfælde er standardhyppigheden tilstrækkelig.

Følgende batchjob skal køre om natten eller efter arbejdstid. Sørg for at kontrollere tidszonen for disse tilbagevendende batchjob. Nogle batchjob bruger muligvis Pacific Standard Time (PST).

| Batchjob | Standardforekomst |
| --- | --- |
| Oprydning i batchjobhistorik | 1 gang om måneden |
| Oprydning i midlertidig placering for eksport | 1 gang om dagen |
| Manglende anmodning om synkronisering af Common Data Service-integration | 1 gang om dagen |
| Systemjob til databasekomprimering, der skal køre regelmæssigt uden for arbejdstid | 1 gang om dagen |
| Systemjob til genopbygning af indeks, der skal køre regelmæssigt uden for arbejdstid | 1 gang om dagen |

1. I Personale skal du vælge **Systemadministration**.

2. I panelet **Søg** skal du søge efter en af de ovennævnte kørsler.

3. Vælg **Kør i baggrunden**, og vælg derefter **Gentagelse**.

   ![Angiv gentagelse](media/talent-batch-history-cleanup-recurrence.png)

4. Under **Definer gentagelse** skal du angive **Startdato** og **Starttidspunkt**, der skal være uden for arbejdstiden eller i weekenden. Vælg **Ingen slutdato**. 

   ![Definer startdato og -tidspunkt for gentagelse](media/talent-batch-history-cleanup-define-recurrence.png)

5. Vælg **OK**.

6. Rediger andre parametre under **Kør i baggrunden** efter behov, og vælg derefter **OK**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Optimere ydeevnen med automatiske oprydningsopgaver](hr-admin-troubleshooting-batch-history.md)
