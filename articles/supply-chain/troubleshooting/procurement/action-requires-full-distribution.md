---
title: Du kan kun udføre en indkøbsordrehandling for fuldt distribuerede linjenumre
description: Du kan kun udføre en indkøbsordrehandling for fuldt distribuerede linjenumre
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 1ef2a938a2a17bc2dbf38d09918eabdbccca8a28
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475942"
---
# <a name="you-can-only-complete-a-purchase-order-action-for-fully-distributed-line-numbers"></a>Du kan kun udføre en indkøbsordrehandling for fuldt distribuerede linjenumre

## <a name="symptom"></a>Symptom

Du kan kun udføre en indkøbsordrehandling for fuldt distribuerede linjenumre.

## <a name="cause"></a>Årsag

Dette problem kan opstå på grund af inkonsistens i indkøbsordrefordeling.

## <a name="resolution"></a>Løsning

Hvis du vil løse dette problem og nulstille indkøbsordren til en *Kladde*-tilstand, skal du gå til **Indkøb og forsyning \> Periodiske opgaver \> Oprydning \> Nulstil indkøbsordrefordeling**. Du kan finde flere oplysninger i følgende blogindlæg: [Løse fejl i indkøbsordrefordeling i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).
