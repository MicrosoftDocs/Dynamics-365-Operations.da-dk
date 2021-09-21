---
title: Belastningsvægt kan kun indeholde positive tal
description: Når du behandler arbejde mellem lokationer, kan der opstå en fejl vedrørende belastningsvægt og opdateringen, som annulleres. Følg disse trin for at løse dette problem.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8ea1f6679a521e3e8683b8e5f18f509e98044414
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475892"
---
# <a name="load-weight-error-and-update-canceled-when-processing-work-between-locations"></a>Indlæs vægtfejl, og opdater annulleret, når der behandles arbejde mellem lokationer

## <a name="symptoms"></a>Symptomer

Hvis der er åbent arbejde, når du behandler arbejde fra pakkelokationer til midlertidige lokationer, eller fra midlertidige lokationer til dock-lokationer, får du måske vist denne fejlmeddelelse.

> feltet 'Belastningsvægt'(=-%1) kan kun indeholde positive tal. Opdateringen er afbrudt.

## <a name="resolution"></a>Løsning

Du kan løse dette problem ved at gå til **Systemadministration \> Periodiske opgaver \> Database \> Konsistenskontrol** og køre processen til **Konsistenskontrol af lagersteds lastvægt**.
