---
title: Tillæg i transportstyring
description: Denne artikel forklarer, hvordan transportgenererede gebyrer skal knyttes til en gebyrkode.
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
ms.openlocfilehash: 8cc4c595d8b61cb9b6c81af4bf7f03faa1a12960
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849207"
---
# <a name="transportation-management-miscellaneous-charges"></a>Tillæg i transportstyring

[!include [banner](../includes/banner.md)]

Som med alle tillæg skal transportgenererede gebyrer knyttes til en gebyrkode. Ellers føjes de ikke tilbage til ordren som et tillæg. **Gebyrkode** bestemmer, hvordan tillægget beregnes i forhold til ordren og ordrelinjen, hvor det tilføjes.

Gå til **Transportstyring > Opsætning > Vurdering > Tillæg** for at definere de kvalifikationskriterier, der bestemmer, hvornår en bestemt **Gebyrkode** anvendes på et gebyr.

Der skal være mindst én opsætning for hver relevante **Gebyrmodul**-indstilling (*Debitor* og *Kreditor*), hvor **Tillægstype** angives til *Ingen*. Hvis dette mangler, føjes tillægget *ikke* til ordren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]