---
title: Intervaller for service
description: Denne artikel giver et overblik over, hvordan du kan arbejde med serviceintervaller. Serviceaftaleintervallet angiver den frekvens, hvormed serviceordrelinjer oprettes til serviceaftalelinjer, når du opretter serviceordrer automatisk.
author: sorenva
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62708258ac3dca9ac03b44efdc96e3bfd643a255
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887219"
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

## <a name="related-articles"></a>Relaterede artikler

[Oprette serviceintervaller](set-up-service-intervals.md)  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]