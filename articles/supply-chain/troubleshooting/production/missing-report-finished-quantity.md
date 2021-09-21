---
title: Opdateringen af færdigmeldingen mislykkes, hvis der mangler et antal
description: Hvis du forsøger at færdigmelde en produktionsordre, mens der rapporteres antallet af fejl, men ikke når tid eller materialeantal rapporteres, er der fejl ved færdigmeldingen af opdateringen.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7785549c47063727f2749749940c1a96a351e70f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475875"
---
# <a name="report-as-finished-update-fails-with-a-missing-quantity-error"></a>Opdateringen af færdigmeldingen mislykkes, hvis der mangler et antal

## <a name="symptoms"></a>Symptomer

Forsøg af færdigmelde en produktionsordre, mens du rapporterer antallet af fejl, men ikke mens du rapporterer tid eller materialeantal. Opdateringen af færdigmeldingen vil mislykkes, når du forsøger at afslutte produktionsordren, og du får vist følgende fejlmeddelelse:

> Færdigmeldingsantal mangler.

## <a name="resolution"></a>Løsning

Du kan ikke rapportere antallet af fejl i en produktionsordre, medmindre du også rapporterer antallet af varer.
