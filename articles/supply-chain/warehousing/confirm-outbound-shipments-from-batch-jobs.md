---
title: Bekræfte udgående forsendelser fra batchjob
description: Denne artikel beskriver, hvordan du opretter et batchjob, der automatisk bekræfter udgående overførselsordre forsendelser, der er til klar til afsendelse.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 00749a69b17b0064290d7b41ccb2171386716302
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875095"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Bekræfte udgående forsendelser fra batchjob

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du opretter et batchjob, der automatisk bekræfter udgående overførselsordre forsendelser, der er til klar til afsendelse. Det batchjob, der er beskrevet her, gælder kun for flytteordreforsendelser, ikke for salgsordrer.

## <a name="turn-the-confirm-outbound-shipments-from-batch-jobs-feature-on-or-off"></a>Aktivere eller deaktivere funktionen Bekræft udgående forsendelser fra batchjob

Hvis du vil bruge den funktionalitet, der er beskrevet i denne artikel, skal funktionen *Bekræft udgående forsendelser fra batchjob* være aktiveret for systemet. Fra og med Supply Chain Management version 10.0.21 er denne funktion som standard aktiveret. Fra og med Supply Chain Management version 10.0.25 er denne funktion obligatorisk og kan ikke deaktiveres. Hvis du kører en version, der er ældre end 10.0.25, kan administratorer slå denne funktion til eller fra ved at søge efter funktionen *Bekræft udgående forsendelser fra batchjob* i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]