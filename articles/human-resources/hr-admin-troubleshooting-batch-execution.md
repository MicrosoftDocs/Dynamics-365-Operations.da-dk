---
title: Nulstille fastsiddende batchjob
description: Dette emne indeholder en forklaring på, hvordan du kan løse problemer med batchjob, der er fastlåst.
author: twheeloc
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 2602bd954daac563cbc50810c6fe0d79dc71a62b
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694985"
---
# <a name="reset-stuck-batch-jobs"></a>Nulstille fastsiddende batchjob


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Udsted

Microsoft Dynamics 365 Human Resources kan opleve problemer med batchjob, der enten sidder fast i tilstanden **Udfører** eller **Annullering**, og som ikke fuldføres.

## <a name="resolution"></a>Løsning

Når et batchjob sidder fast i tilstanden **Udfører** eller **Annullerer**, kan du nulstille statussen ved at gennemtvinge annulleringen af jobbet. Når du har annulleret det, kan du nulstille batchjobbet ved at indstille det til **Venter**-status. Det opsamles derefter igen for udførelse i næste planlagte batchkørsel.

1. Vælg siden **Links** i arbejdsområdet til **Systemadministration**, og vælg **Batchjob**.

2. Vælg det job, der skal nulstilles, på listesiden **Batchjob**.

3. Vælg **Gennemtving annullering** på handlingsbåndet, og bekræft handlingen.

   > [!NOTE]
   > Handlingen **Gennemtving annullering** er kun tilgængelig, når det valgte batchjob har status af enten **Udfører** eller **Annullerer**, og der ikke kører nogen batchudførelses- eller annulleringsprocesser for jobbet.

4. Vælg **Skift status** på handlingsbåndet.

5. Vælg **Venter** på siden **Vælg ny status**, og vælg derefter **OK**.

   ![Vælg en ny status for batchjob.](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a>Se også

[Optimere ydeevnen ved at planlægge batchjob efter arbejdstid](hr-admin-troubleshooting-batch-jobs.md)<br>
[Optimere ydeevnen med automatiske oprydningsopgaver](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
