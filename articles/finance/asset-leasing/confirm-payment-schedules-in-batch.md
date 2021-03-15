---
title: Bekræft betalingsplaner for aktivleasing i en batch
description: Dette emne forklarer, hvordan du kan bekræfte flere betalingsplaner i en batch.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9c680ea16e9f64107fde081c7e7763697356dcc1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971372"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a>Bekræft betalingsplaner for aktivleasing i en batch

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du kan bekræfte flere betalingsplaner i en batch. Betalingsplaner bekræftes enten på grundlag af en leasing-til-leasing eller via bekræftelsesbatchprocessen. En kladdepostering kan kun bogføres i forhold til en leasing, der har en bekræftet betalingsplan. Bekræftelse af betalingsplanen fungerer som endelig godkendelse af de økonomiske oplysninger for leasingaftalen. Alle fremtidige ændringer af de økonomiske oplysninger for leasingaftalen, f. eks. betalinger og leasingperioden, udgør en justering af rettigheder og bør behandles på denne måde.

Benyt følgende fremgangsmåde for at bekræfte flere betalingsplaner.

1. Gå til det **Aktivleasing \> Periodisk \> Bekræftelsesbatch**.
2. På siden **Bekræftelsesbatch** skal du vælge **Bekræftelsesbatch**.
3. Filtrer efter de bøger, du vil bekræfte, i dialogboksen, der vises.

    - Hvis du vil bekræfte alle bøgerne i en bestemt leasinggruppe, skal du vælge gruppen i feltet **Leasinggruppe**.
    - Hvis du vil bekræfte bestemte bøger, skal du vælge kartoteker i feltet **Kartoteks-id**.
    - Hvis du vil bekræfte alle kartoteker, skal du aktivere parameteren **For alle kartoteker**.

Oplysningerne for de senest bekræftede kartoteker vises på siden **Bekræftede kartoteker**. Når betalingsplanerne er bekræftet, kan de oprindelige genkendelseskladdeposteringer bogføres i forhold til rettighederne.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]