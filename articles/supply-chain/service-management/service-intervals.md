---
title: Intervaller for service
description: Serviceintervallet angiver den frekvens, hvormed serviceordrelinjer oprettes til serviceaftalelinjer, når du opretter serviceordrer.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5766d8ce1fa382f3f014e160d311b2dfab2bf774
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216269"
---
# <a name="service-intervals"></a>Intervaller for service

[!include [banner](../includes/banner.md)]

Serviceaftaleintervallet angiver den frekvens, hvormed serviceordrelinjer oprettes til serviceaftalelinjer, når du opretter serviceordrer automatisk.

Når du opretter serviceordrer automatisk, oprettes serviceordrelinjer i henhold til det interval, du har angivet for serviceaftalelinjen, fra startdatoen for aftalelinjen.

Hvis feltet **Interval** i en serviceaftalelinje på siden **Serviceaftaler** er tomt, er linjen en engangshændelse, og den bruges ikke gentagne gange til at oprette serviceordrer.

## <a name="example"></a>Eksempel

Dette eksempel viser, hvordan et serviceinterval påvirker serviceaftalelinjer og serviceordrelinjer på en serviceordre.

### <a name="create-a-service-agreement"></a>Oprette en serviceaftale

Først skal du oprette en serviceaftale og vælge **Efter serviceaftale** i indstillingen **Kombinere serviceordrer**.

1. Klik på **Serviceaftaler**
2. Klik på **Serviceaftale** i gruppen **Ny** under fanen **Serviceaftale** i **Handlingsrude** for at oprette en ny serviceaftale.
3. Indtast en beskrivelse, vælg et projekt i feltet **Projekt-id**, og angiv en dato i feltet **Startdato**.
4. I feltet **Kombinere serviceordrer** skal du vælge **Efter serviceaftale**.

Du har nu oprettet følgende serviceaftale:

| Project      | Startdato                                                                         |
|--------------|------------------------------------------------------------------------------------|
| Dit projekt | Den dato, du har angivet for projektet. I dette eksempel bruges den aktuelle dato. |

### <a name="create-a-service-agreement-line"></a>Oprette en serviceaftalelinje

Derefter skal du oprette en serviceaftalelinje med posteringstypen **Time**.

For at fuldføre denne del af eksemplet skal du oprette et serviceinterval på 10 dage på siden **Intervaller for service**. 

1. Vælg den serviceaftale, du netop har oprettet. 
2. I oversigtspanelet **Linjer** skal du klikke på knappen **Tilføj** for at oprette en ny linje i nederste rude på siden **Serviceaftaler**.
3. Vælg **Time** i feltet **Transaktionstype**.
4. Vælg den arbejder, der skal udføre serviceydelsen, i feltet **Arbejder**.
5. Vælg intervallet på 10 dage i feltet **Serviceinterval**.

Nu har du oprettet en serviceaftalelinje med følgende oplysninger:

| Posteringstype | Igangsæt dato                               | Serviceinterval |
|------------------|------------------------------------------|------------------|
| Time             | Dags dato.                        | Hver 10. dag    |
| Arbejdstråd           | Arbejder, der vil udføre serviceydelsen. |                  |

Der er ikke angivet et tidsvindue for linjen. 

### <a name="create-planned-service-orders"></a>Oprette planlagte serviceordrer

Du kan nu oprette planlagte serviceordrer og serviceordrelinjer for den kommende måned.

1. På siden **Serviceaftaler** skal du klikke på **Planlagte serviceordrer** under fanen **Levér** i **Handlingsrude**.
2. På siden **Oprette serviceordrer** skal du indtaste dags dato i feltet **Fra-dato**, og i feltet **Til-dato** skal du indtaste en dato en måned fra dags dato.
3. Indstil **Time**-skyderen til **Ja**. 
4. Klik på **OK**.

Da der ikke er nogen gruppering i serviceordren (defineret af indstillingen **Efter serviceaftale** i feltet **Kombinere serviceordrer**), oprettes der en serviceordrelinje pr. serviceordre.

### <a name="service-orders-created"></a>Oprettede serviceordrer

Der er oprettet tre serviceordrelinjer inden for den tidsramme, du har angivet i dialogboksen **Opret serviceordrer**. Du kan få vist serviceordrelinjerne på siden **Serviceaftaler** (**Handlingsrude** \> fanen **Levér** \>**Vis**-knappen).

## <a name="related-topics"></a>Relaterede emner

[Oprette serviceintervaller](set-up-service-intervals.md)  

