---
title: Refunderbare gebyrer beregnes forkert på baggrund af det returnerede antal
description: Dette emne indeholder en vejledning til fejlfinding, der kan hjælpe, når kassereren ser forkerte refunderbare gebyrer i POS for det antal varer, der returneres.
author: gvrmohanreddy
ms.date: 03/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c8ecaa0cb73d06ac66b57cce815264e841a2259b
ms.sourcegitcommit: 94ebdaae6dc996b205ac78ed546e38f91f4f46ed
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/28/2022
ms.locfileid: "8490210"
---
# <a name="refundable-charges-are-miscalculated-based-on-the-quantity-returned"></a>Refunderbare gebyrer beregnes forkert på baggrund af det returnerede antal

[!include [banner](../../includes/banner.md)]

Dette emne indeholder en vejledning til fejlfinding, der kan hjælpe, når kassereren ser forkerte refunderbare gebyrer i POS for det antal varer, der returneres.

## <a name="description"></a>Beskrivelse

En kunde returnerer en del af antallet af de varer, der blev købt til en salgsordre med refunderbare gebyrer på linjeniveau. I stedet for at vise en delvis refusion viser POS dog alle gebyrer som refunderbare.

En kunde køber f.eks. et antal på fem varer til $5 pr. vare til samlet gebyr på $25. Kunden returnerer derefter tre af de fem varer. Kassereren får dog vist et $25 beløb, der kan refunderes, i POS i stedet for det forventede $15 refunderbare gebyr for de tre varer, der er returneret.

## <a name="resolution"></a>Løsning

### <a name="turn-on-the-enable-refunding-charges-based-on-the-refunded-quantity-feature"></a>Funktionen Aktivér refusionsgebyrer på basis af det refunderede antal

Fra og med Microsoft Dynamics 365 Commerce version 10.0.26 giver Funktionen **Aktivér refusionsgebyrer på basis af det refunderede antal** mulighed for refundering på linjeniveau baseret på det antal varer, der er returneret.

Hvis du vil aktivere funktionen **Aktivér refusionsgebyrer på basis af det refunderede antal** i Commerce-hovedkontoret, skal du følge disse trin.

1. Åbn arbejdsområdet **Funktionsstyring** (**Systemadministrator \> Arbejdsområder\> Funktionsstyring**).
1. Søg efter og vælg funktionen **Aktivér refusionsgebyrer på basis af det refunderede antal** på listen over tilgængelige funktioner.
1. Vælg **Aktivér nu** i højre rude.
