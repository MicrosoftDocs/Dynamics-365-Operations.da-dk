---
title: Vedligeholde stregkodetyper
description: Denne procedure viser, hvordan du opretter en ny stregkodedefinition, som derefter kan bruges som en del af pluklisterapporten.
author: perlynne
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 45323206550d1b0ed66d89f4be7b995c60af63fc
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="maintain-bar-code-types"></a>Vedligeholde stregkodetyper

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter en ny stregkodedefinition, som derefter kan bruges som en del af pluklisterapporten. Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data. Hvis du bruger USMF, kan du bruge eksempelværdier, der vises. Disse opgaver udføres normalt af en lagerchef.

1. Gå til Stregkoder.
2. Klik på Ny.
3. Skriv en værdi i feltet Stregkodeopsætning.
4. Skriv en værdi i feltet Beskrivelse.
5. Vælg en indstilling i feltet Stregkodetype.
    * Hvis du bruger USMF, kan du vælge "Kode 39".  
6. Angiv et tal i feltet Størrelse.
7. Angiv et tal i feltet Maksimumlængde.
8. Klik på Gem.
9. Luk siden.
10. Gå til Parametre til lager- og lokationsstyring.
11. Indtast eller vælg en værdi i feltet Stregkodeopsætning.
    * Vælg den stregkodeopsætning, som du oprettede før, men vær opmærksom på, at stregkodeformatet skal svare til formatet for det entydige id for den posttype, der bruges i processen. For eksempel bør stregkodeformatet til plukruter være samme format som til plukrutereferencen, der typisk er en nummerserie.  
12. Klik på Gem.
13. Luk siden.

