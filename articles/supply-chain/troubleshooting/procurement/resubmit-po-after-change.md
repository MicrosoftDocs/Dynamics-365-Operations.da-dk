---
title: Fejl ved gensendelse af en indkøbsordre til en arbejdsgang efter en ændring
description: Fejl ved gensendelse af en indkøbsordre til en arbejdsgang efter en ændring
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4b8465d198c440f27a4b3cc4268445e0aa450f5b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475951"
---
# <a name="error-on-resubmitting-a-purchase-order-to-a-workflow-after-a-change"></a>Fejl ved gensendelse af en indkøbsordre til en arbejdsgang efter en ændring


## <a name="symptoms"></a>Symptomer

Følgende fejl opstår i arbejdsgangen, når en indkøbsordre sendes igen efter en ændring:

> Stoppet (fejl): X++ undtagelse: Ændringer af indkøbsordre PO0000569 er kun tilladt i kladdetilstand, når ændringsstyring er aktiveret ved<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

Dette problem opstår kun, hvis indkøbsordren var i en *Bekræftet* tilstand, før du anmodede om ændringer. Hvis du anmoder om ændringer, mens indkøbsordren er i *Godkendt* tilstand, kan arbejdsgangen behandles uden fejl.

## <a name="resolution"></a>Løsning

Dette problem kan opstå på grund af inkonsistens i indkøbsordrefordeling.

Hvis du vil løse dette problem og nulstille indkøbsordren til en *Kladde*-tilstand, skal du gå til **Indkøb og forsyning \> Periodiske opgaver \> Oprydning \> Nulstil indkøbsordrefordeling**. Du kan finde flere oplysninger i følgende blogindlæg: [Løse fejl i indkøbsordrefordeling i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Problemet vil blive løst i [denne artikel i Microsoft Knowledge Base (KB)](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).
