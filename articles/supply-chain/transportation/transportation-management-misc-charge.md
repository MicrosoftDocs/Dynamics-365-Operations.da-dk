---
title: Tillæg i transportstyring
description: I dette emne forklares det, hvordan transportgenererede gebyrer skal knyttes til en gebyrkode.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2b703d770c7f9ea684716368cf1e7dbe5fec8710
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425098"
---
# <a name="transportation-management-miscellaneous-charges"></a>Tillæg i transportstyring

[!include [banner](../includes/banner.md)]

Som med alle tillæg skal transportgenererede gebyrer knyttes til en gebyrkode. Ellers føjes de ikke tilbage til ordren som et tillæg. **Gebyrkode** bestemmer, hvordan tillægget beregnes i forhold til ordren og ordrelinjen, hvor det tilføjes.

Gå til **Transportstyring > Opsætning > Vurdering > Tillæg** for at definere de kvalifikationskriterier, der bestemmer, hvornår en bestemt **Gebyrkode** anvendes på et gebyr.

Der skal være mindst én opsætning for hver relevante **Gebyrmodul**-indstilling (*Debitor* og *Kreditor*), hvor **Tillægstype** angives til *Ingen*. Hvis dette mangler, føjes tillægget *ikke* til ordren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]