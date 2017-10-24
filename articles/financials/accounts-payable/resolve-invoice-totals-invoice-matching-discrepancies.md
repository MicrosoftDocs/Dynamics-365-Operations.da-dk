---
title: "Løse afvigelser under matchning af fakturatotaler"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3f7e1261838866688c97529b0edfa1354034247b
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a>Løse afvigelser under matchning af fakturatotaler

[!include[banner](../includes/banner.md)]




En type validering af fakturasammenholdelse er matchning af fakturatotaler. For at angive, at systemet skal udføre matchning af fakturatotaler skal du på siden **Kreditorparametre** på fanen **Fakturavalidering** angive indstillingen **Afstem fakturatotaler** til **Ja**. 

Du kan bruge matchning af fakturatotaler til at sikre, at de samlede fakturabeløb ikke afviger fra forventede beløb med mere end en acceptabel afvigelse. Seks totaler er sammenlignet på siden **Fakturatotalers tilsvarende oplysninger**. Hvis en af totalerne afviger fra de forventede tilsvarende indkøbsordretotal, markeres en matchningafvigelse. 

For at gennemgå den faktura, der er matchningafvigelse for totaler, skal du i arbejdsområdet **Kreditorfakturapostering** klikke på flisen **Ventende fakturaer**. Derefter skal du i handlingsruden på fanen **Gennemse** klikke på **Tilsvarende oplysninger**. Hvis der er konstateret matchningsafvigelser, vises der advarselsikoner ud for fakturabeløbet. Du kan få vist flere detaljer om totaler ved at få vist tilsvarende oplysninger for fakturatotaler. 

Når du har identificeret afvigelse, kan det være nødvendigt at kontakte kreditoren, hvis du mener, at oplysningerne på fakturaen er forkerte. Afhængigt af den indgåede aftale med kreditoren, kan du gøre en af følgende:

-   Accepter prisforskellen og bogfør fakturaen, der har matchningafvigelser. Systemet kan konfigureres til at kræve godkendelse, inden den kan bogføre, hvis der er matchningafvigelser. I så fald du skal godkende matchningafvigelsen og eventuelt indtaste en kommentar til godkendelse. Du kan derefter vælge at bogføre fakturaen.
-   Revider fakturabeløbet med det forventede beløb, og bogfør fakturaen.
-   Anmod om fuld kredit og en ny, rettet faktura fra kreditoren.

Yderligere oplysninger finder du i [Undersøge eller løse undtagelser](tasks/research-resolve-exceptions.md).



