---
title: Bekræft udgående forsendelser fra batchjob
description: Dette emne beskriver, hvordan du opretter et batchjob, der automatisk bekræfter udgående overførselsordre forsendelser, der er til klar til afsendelse.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 48257967ce360b1d4969124411d5976b807bf9e4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996295"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Bekræft udgående forsendelser fra batchjob

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du opretter et batchjob, der automatisk bekræfter udgående overførselsordre forsendelser, der er til klar til afsendelse. Det batchjob, der er beskrevet her, gælder kun for flytteordreforsendelser, ikke for salgsordrer.

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a>Aktivere funktionen Bekræft udgående forsendelser fra batchjob

Før du kan bruge denne funktion, skal den aktiveres i dit system. Administratorer kan bruge siden [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionsstatus og aktivere den, hvis det er nødvendigt. Funktionen er angivet som:

- **Modul** - *Lokationsstyring*
- **Funktionsnavn** - *Bekræft udgående forsendelser fra batchjob*

## <a name="process-outbound-shipments"></a>Udfør behandling af udgående forsendelser

Sådan konfigureres et planlagt batchjob til at køre bekræftelse af udgående forsendelse for belastninger, der er klar til afsendelse:

1. Gå til **Lokationsstyring \> Periodiske opgaver \> Behandle udgående forsendelser**.
1. Dialogboksen **Bekræft forsendelse** åbnes. I oversigtspanelet **Medtagne poster** skal du vælge **Filtrer**.
1. Dialogboksen for forespørgselseditoren åbnes. Gå til fanen **Område**, og tilføj en række med følgende værdier:
    - **Tabel** - *Laster*
    - **Afledt tabel** - *Laster*
    - **Felt** - *Laststatus*
    - **Kriterier** - *Lastet*
1. Vælg **OK** for at vende tilbage til dialogboksen **Bekræft forsendelse**.
1. Angiv **Batchbehandling** til **Ja** i oversigtspanelet **Kør i baggrunden**.
1. Vælg **Gentagelse** i oversigtspanelet **Kør i baggrunden**.
1. Dialogboksen **Definer gentagelse** åbnes. Angiv kørselsplanen efter behov for din virksomhed.
1. Vælg **OK** for at vende tilbage til dialogboksen **Bekræft forsendelse**.
1. Vælg **OK** i dialogboksen **Bekræft forsendelse** for at føje batchjobbet til batchkøen.

Du kan finde flere oplysninger under [Oversigt over batchbehandling](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).
