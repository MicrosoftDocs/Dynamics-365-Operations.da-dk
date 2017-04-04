---
title: "Løse afvigelser under matchning af fakturatotaler"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 1fd606817b06a05b9abaaedf20ea9872bd7edd5d
ms.openlocfilehash: a54b05bba2549a42f24b8425c9ee418c576d056a
ms.lasthandoff: 03/31/2017


---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a>Løse afvigelser under matchning af fakturatotaler



En type validering af fakturasammenholdelse er matchning af fakturatotaler. For at angive, at systemet skal udføre matchning af fakturatotaler skal du på siden **Kreditorparametre** på fanen **Fakturavalidering** angive indstillingen **Afstem fakturatotaler** til **Ja**. 

Du kan bruge matchning af fakturatotaler til at sikre, at de samlede fakturabeløb ikke afviger fra forventede beløb med mere end en acceptabel afvigelse. Seks totaler er sammenlignet på siden **Fakturatotalers tilsvarende oplysninger**. Hvis en af totalerne afviger fra de forventede tilsvarende indkøbsordretotal, markeres en matchningafvigelse. 

For at gennemgå den faktura, der er matchningafvigelse for totaler, skal du i arbejdsområdet **Kreditorfakturapostering** klikke på flisen **Ventende fakturaer**. Derefter skal du i handlingsruden på fanen **Gennemse** klikke på **Tilsvarende oplysninger**. Hvis der er konstateret matchningsafvigelser, vises der advarselsikoner ud for fakturabeløbet. Du kan få vist flere detaljer om totaler ved at få vist tilsvarende oplysninger for fakturatotaler. 

Når du har identificeret afvigelse, kan det være nødvendigt at kontakte kreditoren, hvis du mener, at oplysningerne på fakturaen er forkerte. Afhængigt af den indgåede aftale med kreditoren, kan du gøre en af følgende:

-   Accepter prisforskellen og bogfør fakturaen, der har matchningafvigelser. Systemet kan konfigureres til at kræve godkendelse, inden den kan bogføre, hvis der er matchningafvigelser. I så fald du skal godkende matchningafvigelsen og eventuelt indtaste en kommentar til godkendelse. Du kan derefter vælge at bogføre fakturaen.
-   Revider fakturabeløbet med det forventede beløb, og bogfør fakturaen.
-   Anmod om fuld kredit og en ny, rettet faktura fra kreditoren.



