---
title: Arbejdsordrer og anlægsaktiver
description: Denne artikel beskriver arbejdsordrer og anlægsaktiver i Styring af aktiver.
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
ms.openlocfilehash: ed83450592d85205743c9ff1aefd0e66e5d2b90c
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111953"
---
# <a name="work-orders-and-fixed-assets"></a>Arbejdsordrer og anlægsaktiver

[!include [banner](../../includes/banner.md)]


I Styring af aktiver kan aktiver knyttes til anlægsaktiver, og du kan oprette arbejdsordrer for disse aktiver. Hvis du bruger denne funktion, kan du få en komplet oversigt over anlægsaktiver, relaterede investeringsprojekter og de omkostninger, der er registreret for investeringsprojekterne i modulet **Projektstyring og regnskab** og modulet **Anlægsaktiver** i programmer til finans og drift.

>[!NOTE]
>Feltet **Nummer på anlægsaktiv** udfyldes kun på arbejdsordrejobprojektet, hvis **Investering** er valgt som projekttypen for arbejdsordrejobprojektet.

I illustrationen herunder vises relationen mellem et investeringsprojekt i modulet **Projektstyring og regnskab** og et projekt for arbejdsordrejob.

![Figur 1.](media/24-work-orders.png)

Følgende procedure beskriver relationen mellem aktiverne, arbejdsordrerne, arbejdsordrejobprojekter og anlægsaktiver.

1. Du opretter et aktiv, som du relaterer til et anlægsaktiv.

![Figur 2.](media/25-work-orders.png)

2. Når du opretter arbejdsordretyper på siden **Arbejdsordretyper** (**Styring af aktiv** > **Opsætning** > **Arbejdsordrer** > **Arbejdsordretyper**), skal du oprette en arbejdsordre type til håndtering af investeringer. Se også [Arbejdsordretyper](../setup-for-work-orders/work-order-types.md).

![Figur 3.](media/26-work-orders.png)

3. Når du opretter projektgrupper for arbejdsordrer under fanen **Projektgruppe** på siden **Opsætning af arbejdsordreprojekt** (**Styring af aktiver** > **Opsætning** > **Arbejdsordrer** > **Opsætning af projekt**), opretter du en relation mellem den arbejdsordretype, der bruges til investeringer, og den projektgruppe, der er oprettet for investeringer på siden **Projektgrupper** i modulet **Projektstyring og regnskab** (**Projektstyring og regnskab** > **Opsætning** > **Bogføring** > **Projektgrupper**).

![Figur 4.](media/27-work-orders.png)

4. Når du opretter en arbejdsordre, der vedrører et anlægsaktivobjekt, skal du vælge den type arbejdsordre, der bruges til håndtering af investeringer, f.eks. **Investering**.

5. Når arbejdsordren oprettes, vises den relaterede arbejdsordretype på siden **Alle arbejdsordrer**.

![Figur 5.](media/28-work-orders.png)

6. Når arbejdsordren oprettes, oprettes det projekt, der er relateret til arbejdsordren, på siden **Alle projekter** i modulet **Projektstyring og regnskab** (**Projektstyring og regnskab** > **Projekter** > **Alle projekter**). Hvis du vil have vist projektrelaterede oplysninger, skal du vælge linket i feltet **Projekt-id** under fanen **Generelt** i oversigtspanelet **Linjedetaljer** i detaljevisningen for siden **Alle arbejdsordrer** i modulet **Styring af aktiver** (**Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer**).

![Figur 6.](media/29-work-orders.png)

7. Hvis du vil have vist en oversigt over de projekter, der er knyttet til et anlægsaktiv, skal du vælge **Anlægsaktiver** > **Anlægsaktiver** > **Anlægsaktiver** og derefter bruge feltet **Nummer på anlægsaktiv** til at vælge linket for anlægsaktivet for at åbne detaljevisningen. Udvid ruden **Relaterede oplysninger** i højre side af siden, og vælg oversigtspanelet **Tilknyttede projekter**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
