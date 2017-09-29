---
title: Afstemme fragt i transportstyring
description: I denne artikel beskrives fragtafstemningsprocessen.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: ab7d21d7a75e2c954831a254bb339d9cf5746d9d
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017

---

# <a name="reconcile-freight-in-transportation-management"></a>Afstemme fragt i transportstyring

[!include[banner](../includes/banner.md)]


I denne artikel beskrives fragtafstemningsprocessen.

Fragtafstemning kan udføres manuelt, eller det kan indstilles til at ske automatisk. Hvis du vil bruge automatisk fragtafstemning, skal du angive en revisionsmaster, hvor du kan definere de kriterier, der bestemmer, hvilken fragtbreve der afstemmes automatisk.

## <a name="the-freight-reconciliation-process"></a>Fragtafstemningsprocessen
Fragtsatser beregnes af det satsprogram, der er knyttet til den relevante fragtmand. Når en belastning er bekræftet, oprettes der et fragtbrev, og fragtsatserne overføres til det. Fragtsatserne fordeles som diverse tillæg til det relevante kildedokument (indkøbsordre, salgsordre, og/eller flytteordre), afhængigt af den konfiguration, der bruges til den almindelige fakturering. Fragtafstemningsprocessen (der er også kaldes sammenholdelsesprocessen) kan begynde, så snart fragtfakturaen ankommer fra fragtmanden. Fakturaen kan modtages elektronisk eller på papir. Hvis fakturaen modtages på papir, kan du generere en elektronisk faktura ved at bruge fragtbrevet som skabelon. 

[![Fragtafstemningsproces](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>Manuel afstemning
Hvis du afstemmer fragt manuelt, skal du sammenholde hver fakturalinje med fragtbrevlinjen eller -linjerne for den belastning, der skal faktureres. Du udfører afstemningen på siden **Sammenholdelse af fragtbrev og faktura**. Hvis beløbet på fakturalinjen ikke stemmer overens med beløbet i fragtbrevet, skal du vælge en afstemningsårsag for forskellen. Hvis der er flere grunde til afstemning, kan du opdele uafstemte beløb på tværs af dem. Årsagen til afstemningen bestemmer, hvordan de forskellige beløb bogføres i finansmodulet. Når afstemningen af hele fakturabeløbet er behandlet, sendes den til godkendelse, og derefter bogføres kladden. I følgende illustration vises, hvordan du opretter en fragtfaktura og udfører fragtafstemning in Microsoft Dynamics 365 for Finance and Operations. 
[![Fragtafstemningsopgaver i Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)
## <a name="automatic-reconciliation"></a>Automatisk afstemning
Hvis du vil bruge automatisk afstemning, skal du angive tidsplanen for afstemningen, og de fakturaer og fragtmænd der skal bruges. Sammenholdelse af fakturalinjer og fragtbreve sker i overensstemmelse med opsætningen af revisionsmaster- og fragtbrevtypen. Når du har kørt den automatiske afstemning, skal du håndtere eventuelle fakturaer, som systemet ikke kan afstemme. Du skal derefter behandle disse fakturaer manuelt, før du kan bogføre alle fakturaer til betaling.



