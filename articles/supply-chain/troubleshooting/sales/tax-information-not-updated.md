---
title: Momsoplysninger opdateres ikke, hvis salgsordrelokationen ændres
description: Hvis stedet, lagerstedet eller leveringsadressen ændres på et salgsordrehoved, opdateres momsoplysningerne ikke for linjerne. Det skal du gøre manuelt.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 77a73a787ff8a174c575f3b4f75694ded45d5712
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475908"
---
# <a name="tax-information-isnt-updated-if-location-on-a-sales-order-header-is-changed"></a>Oplysningerne om moms opdateres ikke, hvis placeringen på et salgsordrehoved ændres

## <a name="symptoms"></a>Symptomer

Hvis stedet, lagerstedet eller leveringsadressen ændres på et salgsordrehoved, opdateres momsoplysningerne ikke for linjerne.

## <a name="resolution"></a>Løsning

Denne funktionsmåde er tilsigtet. Problemet opstår, fordi leveringsadressen, stedet og lagerstedet ikke ændres automatisk på linjeniveau. Du skal opdatere dem manuelt.
