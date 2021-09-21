---
title: Regnskabsfordelinger er enten over- eller underdistribution
description: En eller flere regnskabsfordelinger er enten overfordelt eller underfordelt.
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
ms.openlocfilehash: 7ff0172469df50da9e4272b3fa3f75001a4eb7eb
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475902"
---
# <a name="accounting-distributions-are-either-over--or-under-distributed"></a>Regnskabsfordelinger er enten over- eller underdistribution


## <a name="symptoms"></a>Symptomer

Du modtager følgende fejl:

> En eller flere regnskabsfordelinger er enten overfordelt eller underfordelt

## <a name="cause"></a>Årsag

Dette problem kan opstå på grund af inkonsistens i indkøbsordrefordeling.

## <a name="resolution"></a>Løsning

Hvis du vil løse dette problem og nulstille indkøbsordren til en *Kladde*-tilstand, skal du gå til **Indkøb og forsyning \> Periodiske opgaver \> Oprydning \> Nulstil indkøbsordrefordeling**. Du kan finde flere oplysninger i følgende blogindlæg: [Løse fejl i indkøbsordrefordeling i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).
