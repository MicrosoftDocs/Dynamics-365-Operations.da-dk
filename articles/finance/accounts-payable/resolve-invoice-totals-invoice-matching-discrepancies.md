---
title: Oversigt over løsning af afvigelser under sammenholdelse af fakturatotaler
description: Du kan bruge matchning af fakturatotaler til at sikre, at de samlede fakturabeløb ikke afviger fra forventede beløb med mere end en acceptabel afvigelse.
author: abruer
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 63413,  ""intro-internal
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.form: VendTotalPriceTolerance
ms.openlocfilehash: fa248622a21b0571b08c97eff507ee1035daa7f9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268581"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching-overview"></a>Oversigt over løsning af afvigelser under sammenholdelse af fakturatotaler

[!include [banner](../includes/banner.md)]

En type validering af fakturasammenholdelse er matchning af fakturatotaler. For at angive, at systemet skal udføre matchning af fakturatotaler skal du på siden **Kreditorparametre** på fanen **Fakturavalidering** angive indstillingen **Afstem fakturatotaler** til **Ja**. 

Du kan bruge matchning af fakturatotaler til at sikre, at de samlede fakturabeløb ikke afviger fra forventede beløb med mere end en acceptabel afvigelse. Seks totaler er sammenlignet på siden **Fakturatotalers tilsvarende oplysninger**. Hvis en af totalerne afviger fra de forventede tilsvarende indkøbsordretotal, markeres en matchningafvigelse. 

For at gennemgå den faktura, der er matchningafvigelse for totaler, skal du i arbejdsområdet **Kreditorfakturapostering** klikke på flisen **Ventende fakturaer**. Derefter skal du i handlingsruden på fanen **Gennemse** klikke på **Tilsvarende oplysninger**. Hvis der er konstateret matchningsafvigelser, vises der advarselsikoner ud for fakturabeløbet. Du kan få vist flere detaljer om totaler ved at få vist tilsvarende oplysninger for fakturatotaler. 

Når du har identificeret afvigelse, kan det være nødvendigt at kontakte kreditoren, hvis du mener, at oplysningerne på fakturaen er forkerte. Afhængigt af den indgåede aftale med kreditoren, kan du gøre en af følgende:

-   Accepter prisforskellen og bogfør fakturaen, der har matchningafvigelser. Systemet kan konfigureres til at kræve godkendelse, inden den kan bogføre, hvis der er matchningafvigelser. I så fald du skal godkende matchningafvigelsen og eventuelt indtaste en kommentar til godkendelse. Du kan derefter vælge at bogføre fakturaen.
-   Revider fakturabeløbet med det forventede beløb, og bogfør fakturaen.
-   Anmod om fuld kredit og en ny, rettet faktura fra kreditoren.

Yderligere oplysninger finder du i [Undersøg/Løs undtagelser](tasks/research-resolve-exceptions.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
