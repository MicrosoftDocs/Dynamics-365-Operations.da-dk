---
title: Lokalisere fejl i indkøbs- og forsyningsarbejdsgange
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med indkøbs- og forsyningsarbejdsgange.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: e8274890c581fffc7330538430c9b2ba060041bc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999097"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a>Lokalisere fejl i indkøbs- og forsyningsarbejdsgange

Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med indkøbs- og forsyningsarbejdsgange.

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a>Fejl ved genafsendelse af en indkøbsordre til arbejdsgangen efter en ændring: "Ændringer af indkøbsordre X er kun tilladt i kladdetilstand, når ændringsstyring er aktiveret"

Dette problem opstår kun, hvis indkøbsordren var i en *Bekræftet* tilstand, før du anmodede om ændringer. Hvis du anmoder om ændringer, mens indkøbsordren er i *Godkendt* tilstand, kan arbejdsgangen behandles uden fejl.

### <a name="error-description"></a>Fejlbeskrivelse

Følgende fejl opstår i arbejdsgangen, når en indkøbsordre sendes igen efter en ændring:

> Stoppet (fejl): X++ undtagelse: Ændringer af indkøbsordre PO0000569 er kun tilladt i kladdetilstand, når ændringsstyring er aktiveret ved<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

### <a name="issue-resolution"></a>Problemløsning

Dette problem kan opstå på grund af inkonsistens i indkøbsordrefordeling.

Hvis du vil løse dette problem og nulstille indkøbsordren til en *Kladde*-tilstand, skal du gå til **Indkøb og forsyning \> Periodiske opgaver \> Oprydning \> Nulstil indkøbsordrefordeling**. Du kan finde flere oplysninger i følgende blogindlæg: [Løse fejl i indkøbsordrefordeling i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Problemet vil blive løst i [denne artikel i Microsoft Knowledge Base (KB)](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>En eller flere regnskabsfordelinger er enten overfordelt eller underfordelt.

Dette problem kan opstå på grund af inkonsistens i indkøbsordrefordeling.

Hvis du vil løse dette problem og nulstille indkøbsordren til en *Kladde*-tilstand, skal du gå til **Indkøb og forsyning \> Periodiske opgaver \> Oprydning \> Nulstil indkøbsordrefordeling**. Du kan finde flere oplysninger i følgende blogindlæg: [Løse fejl i indkøbsordrefordeling i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a>Hvis en leveringsrest annulleres på en indkøbsordre, hvor ændringsstyring er aktiveret, går indkøbsordren til en bekræftet tilstand.

### <a name="issue-description"></a>Problembeskrivelse

I forbindelse med en indkøbsordre, der er underlagt ændringsstyring, og hvis den eneste anmodede ændring er at annullere en leveringsrest på en eller flere af linjerne, går indkøbsordren direkte til en *Bekræftet* tilstand, når den godkendes, og der oprettes ikke en kladde.

### <a name="issue-resolution"></a>Problemløsning

Annullering af en leveringsrest påvirker ikke indholdet af bekræftelsesjournalen. Denne funktionalitet skal bruges, når linjen er blevet delvist modtaget, og restantallet skal annulleres i procestrinnet, når indkøbsordren er blevet bekræftet af leverandøren.

Hvis dette skal afspejles i indkøbsordrebekræftelsen, skal antallet justeres på indkøbsordrelinjen, så bekræftelsen bliver påkrævet. Hvis der ikke er modtaget noget på linjen, kan du også fjerne antallet. I dette tilfælde er ny bekræftelse påkrævet.

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a>Annullerede indkøbsordrer vises på kladdelisten i arbejdsområdet til forberedelse af indkøbsordrer.

### <a name="issue-description"></a>Problembeskrivelse

Når du har annulleret indkøbsordrer, der er i en *Bekræftet* tilstand, vises de annullerede indkøbsordrer stadig på listen over kladdeindkøbsordrer i arbejdsområdet **Forberedelse af indkøbsordre**.

### <a name="issue-resolution"></a>Problemløsning

Dette problem opstår kun ved indkøbsordrer, der er omfattet af en ændringsstyring. Det sker, fordi annulleringen betragtes som en ændring, der skal godkendes. Godkendelsen kan foretages automatisk af systemet. Derfor er processen at sende den annullerede indkøbsordre til godkendelsesarbejdsgangen, så den kan gå til en *Godkendt* tilstand. På dette tidspunkt vises indkøbsordren ikke længere på listen over kladdeindkøbsordrer i arbejdsområdet **Forberedelse af indkøbsordre**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]