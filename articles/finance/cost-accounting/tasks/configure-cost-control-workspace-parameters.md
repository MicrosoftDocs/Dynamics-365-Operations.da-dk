---
title: Konfigurere arbejdsområdeparametre for omkostningsstyring
description: Du kan bruge denne procedure til at konfigurere arbejdsområdet Omkostningsstyring, så ledere på forskellige niveauer i organisationen kan få indsigt i deres omkostningsobjekter, f.eks. bærere og produktgrupper.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c46d77a632b0d2939d9a9f561e7c761845169629
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144467"
---
# <a name="configure-cost-control-workspace-parameters"></a>Konfigurere arbejdsområdeparametre for omkostningsstyring

[!include [banner](../../includes/banner.md)]

Du kan bruge denne procedure til at konfigurere arbejdsområdet Omkostningsstyring, så ledere på forskellige niveauer i organisationen kan få indsigt i deres omkostningsobjekter, f.eks. bærere og produktgrupper. USP2-demofirmaet blev brugt til at oprette denne registrering.

1. Gå til Omkostningsregnskab > Opsætning > Konfiguration af arbejdsområde for omkostningsstyring.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn.
4. Skriv en værdi i feltet Beskrivelse.
5. Vælg Ja i feltet Publiceret.
    * Hvis du vælger Ja for denne indstilling, kan brugere, der er tildelt en af disse roller, se rapporten i arbejdsområdet Omkostningsstyring: regnskabschef, bogholder, bogholderimedarbejder eller omkostningsobjektcontroller. Hvis du vælger Nej for denne indstilling, er det kun brugere, der er tildelt en af disse roller, der kan se rapporten i arbejdsområdet Omkostningsstyring: regnskabschef, bogholder eller bogholderimedarbejder.  
6. Udvid datafiltreringssektionen.
7. Indtast eller vælg en værdi i feltet Omkostningskontrolenhed.
8. Skriv eller vælg en værdi i feltet Oprindelig budgetversion.
9. Indtast eller vælg en værdi i feltet Dimensionshierarki for omkostningselement.
10. Indtast eller vælg en værdi i feltet Dimensionshierarki for omkostningsobjekt.
11. Udvid sektionen Tildel beregningsposter.
12. Klik på Ny.
13. Markér den valgte række på listen.
14. Indtast eller vælg en værdi i feltet Regnskabskalenderperiode.
15. Indtast eller vælg en værdi i feltet Aktuel version.
16. Udvid sektionen Regnskabsperioder pr. kolonne.
17. Vælg Ja i feltet Aktuel periode.
18. Udvid sektionen Kolonner, der skal vises for omkostninger.
19. Vælg Ja i feltet Anlægsaktiv.
20. Vælg Ja i feltet Variabel omkostning.
21. Vælg Ja i feltet Totalomkostning.
22. Klik på Gem.
23. Luk siden.
24. Gå til Omkostningsregnskab > Arbejdsområder > Omkostningsstyring.
25. Vælg en opgørelse for at få vist faste, variable, samlede og ikke-klassificerede omkostninger for de valgte regnskabsperioder.
26. Indtast eller vælg en værdi i feltet Regnskabskalenderperiode.
27. Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.
    * Når du har valgt et dimensionshierarki for omkostningsobjekt, kan du udvide dimensionshierarkiet for omkostningselement for at få vist de ønskede omkostningsværdier. For eksempel kan du udvide hierarkiet for at få vist værdien i Produktionsomkostninger.  

