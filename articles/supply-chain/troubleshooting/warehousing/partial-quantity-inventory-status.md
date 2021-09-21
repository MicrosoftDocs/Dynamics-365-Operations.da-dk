---
title: Aktivere ændring af lagerstatus for delarbejde
description: Denne side forklarer, hvordan du opretter et menupunkt med de relevante indstillinger, så arbejdere kan foretage en ændring i lagerstatus for en delmængde af en batch.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 056ce412955808ddf126025ad917b874c54a5e62
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475854"
---
# <a name="enable-inventory-status-change-for-partial-quantity-work"></a>Aktivere ændring af lagerstatus for delarbejde

## <a name="symptoms"></a>Symptomer

Du vil foretage en ændring af lagerstatus for et delvist antal af en batch.

## <a name="resolution"></a>Løsning

Hvis du vil give arbejdere mulighed for at foretage denne ændring, kan du oprette et menupunkt til mobilappen Warehouse Management. Opret (eller rediger) et menupunkt med følgende indstillinger på siden **Menupunkter i mobilenhed**:

- **Tilstand:** *Arbejde*
- **Brug eksisterende arbejde:** *Nej*
- **Arbejdsoprettelsesproces:** *Bevægelse*
- **Vis lagerstatus:** *Ja*

Angiv de resterende felter på siden efter behov.
