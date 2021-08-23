---
title: Oprette en rentekode med et interval
description: Rentekoder kan konfigureres til at beregne forskellige rentebeløb baseret på et interval af værdier.
author: ShivamPandey-msft
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b20870ade99dd48e72c8aa63f563bc51dc93bd9601d309c474af93cee6eddedb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771842"
---
# <a name="create-an-interest-code-with-a-range"></a>Oprette en rentekode med et interval

[!include [banner](../../includes/banner.md)]
Rentekoder kan konfigureres til at beregne forskellige rentebeløb baseret på et interval af værdier. Denne procedure viser, hvordan du kan tilføje en rentekode og føje et interval til den.

1. Gå til Kredit og inkasso > Rente > Konfigurer rentekoder.
2. Klik på Ny.
3. Angiv navnet på rentekoden i feltet Rentekode.
4. Angiv en beskrivelse af rentekoden i feltet Beskrivelse.
5. Vælg Måned.
6. Udvid afsnittet Indtjeninger.
7. Udvid sektionen Indtjeninger pr. valuta.
8. I feltet Finansbogføringskonto skal du specificere de ønskede værdier.
9. Vælg 'Måneder' i feltet Rente efter interval.
10. Klik på Tilføj.
11. Angiv en beskrivende for denne valuta og dette interval i feltet Beskrivelse.
12. Klik på Gem.
13. Klik på Afgrænsninger.
14. Klik på Ny.
15. Angiv Fra-værdien som 0, og angiv derefter den renteprocent pr. måned, der skal bruges til at beregne renten. I vores eksempel er det 1.5.
16. Klik på Ny.
17. Angiv den næste Fra-værdi som 4, hvilket er den første måned, hvor du skal beregne et nyt rentebeløb.
18. Angiv den renteprocent pr. måned, der skal bruges til at beregne renten, der starter i måned 4. I vores eksempel er det 2,0.
19. Klik på Ny.
20. Angiv den næste Fra-værdi som 7, hvilket er den næste måned, hvor du skal beregne et nyt rentebeløb.
21. Angiv den renteprocent pr. måned, der skal bruges til at beregne renten, der starter i måned 7. I vores eksempel er det 2,5.
22. Klik på Luk for at afslutte konfigurationen.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]