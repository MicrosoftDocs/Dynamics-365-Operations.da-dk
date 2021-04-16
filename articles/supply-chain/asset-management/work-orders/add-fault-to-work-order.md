---
title: Føje fejl til arbejdsordre
description: Dette emne indeholder en beskrivelse af, hvordan du kan føje fejlregistreringer til arbejdsordrer i Styring af aktiver.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0a79986e3b477865bc1816a1d28c1b7094ae3974
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809800"
---
# <a name="add-fault-to-work-order"></a>Tilføje fejl til arbejdsordre

[!include [banner](../../includes/banner.md)]



Du kan føje fejl, der er defineret i fejldesigneren, til en arbejdsordre. En eller flere fejlposter skal være tilknyttet de aktivtyper, der bruges for det aktiv, som er valgt i arbejdsordren. Yderligere oplysninger om den opsætningen finder du i [Fejlhåndtering](../setup-for-work-orders/fault-management.md).

1. Vælg **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Vælg den arbejdsordre, der skal foretages en fejlregistrering for, og vælg fanen **Arbejdsordre** i handlingsruden, og vælg **Aktivfejl** i gruppen **Aktiv**.

3. Vælg **Tilføj linje** i oversigtspanelet **Symptomer**. Et fejlserienummer indsættes automatisk i feltet **Fejl**.

4. Vælg det relevante symptom i feltet **Fejlsymptom**.

5. Vælg de relevante værdier i felterne **Fejlområde** og **Fejltype**.

6. Feltet **Fejldato** indeholder automatisk dags dato. Vælg en anden dato efter behov.

7. I oversigtspanelet **Årsager til valgt symptom** kan du tilføje en linje, der beskriver årsagen til problemet.

8. I oversigtspanelet **Løsninger til valgt symptom** kan du tilføje en linje, der beskriver en mulig løsning på problemet.

9. Vælg **Gem**.

Følgende illustration viser et eksempel på en fejlregistrering.

![Figur 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Se aktivfejl

På listen **Aktivfejl** kan du få en oversigt over alle fejl, der er registreret på aktiver.

På listesiden **Aktivfejl** kan du se en oversigt over alle fejl, der er registreret på aktiver. Vælg **Styring af aktiver** > **Forespørgsler** > **Aktivfejl** > **Aktivfejl** for at åbne siden.


## <a name="print-asset-fault-report"></a>Udskrive aktivfejlrapport

På listesiden **Alle aktiver** kan du udskrive en fejlrapport for aktiver, der viser alle fejlregistreringer og en grafisk oversigt over fejlstatistik.

1. Vælg **Styring af aktiver** > **Almindelig** > **Aktiver** > **Alle aktiver**.

2. Vælg det aktiv, fejlrapporten skal udskrives for.

3. I handlingsruden under fanen **Generelt** i gruppen **Rapporter** skal du vælge **Aktivfejl**.

4. Indsæt en bestemt periode, eller vælg en fejltype.

5. Vælg **OK** for at udskrive rapporten.

>[!NOTE]
>Du kan udskrive en fejlrapport for flere aktiver eller aktivtyper ved at vælge **Styring af aktiver** > **Rapporter** > **Aktiver** > **Aktivfejl**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]