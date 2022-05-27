---
title: Tillæg i transportstyring
description: I dette emne forklares det, hvordan transportgenererede gebyrer skal knyttes til en gebyrkode.
author: Weijiesa
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e54c94baeba487ccd8fe26e58d3e891e5e3a1088
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672592"
---
# <a name="transportation-management-miscellaneous-charges"></a>Tillæg i transportstyring

[!include [banner](../includes/banner.md)]

Som med alle tillæg skal transportgenererede gebyrer knyttes til en gebyrkode. Ellers føjes de ikke tilbage til ordren som et tillæg. **Gebyrkode** bestemmer, hvordan tillægget beregnes i forhold til ordren og ordrelinjen, hvor det tilføjes.

Gå til **Transportstyring > Opsætning > Vurdering > Tillæg** for at definere de kvalifikationskriterier, der bestemmer, hvornår en bestemt **Gebyrkode** anvendes på et gebyr.

Der skal være mindst én opsætning for hver relevante **Gebyrmodul**-indstilling (*Debitor* og *Kreditor*), hvor **Tillægstype** angives til *Ingen*. Hvis dette mangler, føjes tillægget *ikke* til ordren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]