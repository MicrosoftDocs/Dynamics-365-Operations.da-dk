---
title: Hvor er varen brugt?
description: Dette emne forklarer, hvordan du får en oversigt over, hvor en vare bruges i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: 84ab803aedf5b803b6c5f39ff1907726335cb45d
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918320"
---
# <a name="item-where-used"></a>Hvor er varen brugt?

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Du kan foretage en beregning for en bestemt vare for at få en oversigt over, hvor i Styring af aktiver varen er brugt. Resultaterne viser den kontekst, som varen er blevet brugt i, i løbet af dens levetid. Siden **Hvor er varen brugt?** kan åbnes fra hovedmenuen i Styring af aktiver, og den kan også åbnes fra følgende sider:

[Aktivstykliste](../objects/object-BOM.md)

[Reservedele i aktivtypestandarder](../setup-for-objects/object-types.md)

[Varebudget på standardbudget for vedligeholdelsesjobtype](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

[Vedligeholdelsesprognose for arbejdsordre](../work-orders/maintenance-forecasts.md)

[Indkøbsrekvisition for arbejdsordre](../work-orders/procurement.md)

[Arbejdsordreindkøb](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a>Oprette en beregning af, hvor en vare er brugt

1. Klik på **Styring af aktiver** > **Forespørgsler** > **Hvor er varen brugt?**, eller vælg knappen **Hvor er varen brugt?** på en af de ovennævnte sider.

2. Vælg i dialogboksen **Hvor er varen brugt?** den vare, der skal foretages en beregning for, i feltet **Varenummer**.

3. Du kan bruge feltet **Niveau** til at angive, hvor detaljerede varelinjerne skal være i forbindelse med arbejdssteder. Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle varelinjer for et arbejdssted på det øverste niveau. Derfor kan relationen/antallet på en linje være opsummeret fra arbejdssteder, der er placeret på et lavere niveau. Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle varelinjer på alle de arbejdsstedsniveauer, de er relateret til.

4. Vælg "Ja" på de knapper i sektionen **Medtag**, du vil medtage i beregningen.

5. Klik på **OK** for at starte beregningen.

6. Under fanen **Hvor er varen brugt?** > handlingsrudegrupperne **Sammenlæg pr.** skal vælge de relevante knapper for at få vist det nødvendige detaljeringsniveau i beregningen. De valgte handlingsrudeknapper er fremhævet. Klik på en knap for at aktivere eller deaktivere den.

7. Hvis du vil have vist de dimensioner, der vedrører varen, skal du klikke på **Vis dimensioner** og vælge de dimensioner, der skal vises.

I nedenstående figur kan du se et eksempel på en beregning af Hvor er varen brugt? for varenummer "1000".

![Figur 1](media/12-controlling-and-reporting.png)

