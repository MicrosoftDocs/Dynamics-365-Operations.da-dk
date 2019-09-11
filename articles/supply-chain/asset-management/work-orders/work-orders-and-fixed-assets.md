---
title: Arbejdsordrer og anlægsaktiver
description: Dette emne beskriver arbejdsordrer og anlægsaktiver i Styring af aktiver.
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f03b7fa073c4e5338b7b5681ba7b8c9fe00a657b
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875561"
---
# <a name="work-orders-and-fixed-assets"></a>Arbejdsordrer og anlægsaktiver


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


I Styring af aktiver kan aktiver knyttes til anlægsaktiver, og du kan oprette arbejdsordrer for disse aktiver. Hvis du bruger denne funktion, kan du få en komplet oversigt over anlægsaktiver, relaterede investeringsprojekter og de omkostninger, der er registreret for investeringsprojekterne i modulet **Projektstyring og regnskab**, og modulet **Anlægsaktiver** i Dynamics 365 for Finance and Operations.

>[!NOTE]
>Feltet **Nummer på anlægsaktiv** udfyldes kun på arbejdsordrejobprojektet, hvis typen "Investering" er valgt som projekttypen for arbejdsordrejobprojektet.

![Figur 1](media/24-work-orders.png)

Følgende procedure beskriver relationen mellem aktiverne, arbejdsordrerne, arbejdsordrejobprojekter og anlægsaktiver.

1. Du opretter et aktiv, som du relaterer til et anlægsaktiv, som vist på nedenstående illustration.

![Figur 2](media/25-work-orders.png)

2. Når du opretter arbejdsordretyper (**Styring af aktiv** > **Opsætning** > **Arbejdsordrer** > **Arbejdsordretyper**), skal du oprette en arbejdsordre type til håndtering af investeringer. Se også [Arbejdsordretyper](../setup-for-work-orders/work-order-types.md).

![Figur 3](media/26-work-orders.png)

3. Når du opretter projektgrupper for arbejdsordrer (**Styring af aktiver** > **Opsætning** > **Arbejdsordrer** > **Opsætning af projekt** > **Projektgruppe**-linket), opretter du en relation mellem den arbejdsordretype, der bruges til investeringer, og den projektgruppe, der er oprettet for investeringer i modulet **Projektstyring og regnskab** (**Projektstyring og regnskab** > **Opsætning** > **Bogføring** > **Projektgrupper**).

![Figur 4](media/27-work-orders.png)

4. Når du opretter en arbejdsordre, der vedrører et anlægsaktivobjekt, skal du vælge den type arbejdsordre, der bruges til håndtering af investeringer, f.eks. "Investering".

5. Når arbejdsordren oprettes, vises den relaterede arbejdsordretype i **Alle arbejdsordrer**.

![Figur 5](media/28-work-orders.png)

6. Når arbejdsordren oprettes, oprettes det projekt, der er relateret til arbejdsordren, i **Projektstyring og regnskab** > **Alle projekter**. Du kan få vist projektrelaterede oplysninger ved at klikke på **Projekt-id**-linket i arbejdsordren (i **Styring af aktiver** skal du åbne arbejdsordren i visningen Detaljer > oversigtspanelet **Linjedetaljer** > **Generelt** > feltet **Projekt-id**).

![Figur 6](media/29-work-orders.png)

7. I **Anlægsaktiver** kan du få vist en oversigt over de projekter, der er knyttet til et anlægsaktiv (**Anlægsaktiver** > **Anlægsaktiver** > **Anlægsaktiver** > klik på anlægsaktivet i **Nummer på anlægsaktiv**-feltet > se indholdet i ruden **Relaterede oplysninger** > sektionen **Tilknyttede projekter**).

