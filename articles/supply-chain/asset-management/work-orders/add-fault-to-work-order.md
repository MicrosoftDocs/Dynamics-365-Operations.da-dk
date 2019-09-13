---
title: Føje fejl til arbejdsordre
description: Dette emne indeholder en beskrivelse af, hvordan du kan føje fejlregistreringer til arbejdsordrer i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875572"
---
# <a name="add-fault-to-work-order"></a>Føje fejl til arbejdsordre

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Du kan føje fejl, der er defineret i fejldesigneren, til en arbejdsordre. Det valgte aktiv i arbejdsordren skal indeholde aktivtyper, der har en eller flere fejlposter tilknyttet. Læs mere om opsætning i afsnittet [Fejlstyring](../setup-for-work-orders/fault-management.md).

1. Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Vælg den arbejdsordre, du vil foretage en fejlregistrering for, på listen, og klik på **Aktivfejl**.

3. Klik på **Tilføj linje** i oversigtspanelet **Symptomer**. Et fejlserienummer indsættes automatisk i feltet **Fejl**.

4. Vælg det relevante symptom i feltet **Fejlsymptom**.

5. Vælg **Fejlområde** og **Fejltype**.

6. Feltet **Fejldato** indeholder automatisk dags dato. Hvis det er nødvendigt, kan du vælge en anden dato.

7. I oversigtspanelet **Årsager til valgt symptom** kan du tilføje en linje, der beskriver årsagen til problemet.

8. I oversigtspanelet **Løsninger til valgt symptom** kan du tilføje en linje, der beskriver en mulig løsning på problemet.

9. Klik på **Gem**.

![Figur 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Se aktivfejl

På listen **Aktivfejl** kan du få en oversigt over alle fejl, der er registreret på aktiver.

Klik på **Styring af aktiver** > **Forespørgsler** > **Aktivfejl** > **Aktivfejl** for at åbne listen.


## <a name="print-asset-fault-report"></a>Udskrive aktivfejlrapport

På listesiden **Alle aktiver** kan du udskrive en fejlrapport for aktiver, der viser alle fejlregistreringer og en grafisk oversigt over fejlstatistik.

1. Klik på **Styring af aktiver** > **Almindelig** > **Aktiver** > **Alle aktiver**.

2. På listen **Aktiver** skal du vælge det aktiv, du vil udskrive en fejlrapport for.

3. Klik på **Aktivfejl** i sektionen **Rapporter** under fanen **Generelt**.

4. Indsæt en bestemt periode, eller vælg en fejltype.

5. Klik på **OK** for at udskrive rapporten.

>[!NOTE]
>Du kan også udskrive en fejlrapport for flere aktiver eller aktivtyper ved at klikke på **Styring af aktiver** > **Rapporter** > **Aktiver** > **Aktivfejl**.

