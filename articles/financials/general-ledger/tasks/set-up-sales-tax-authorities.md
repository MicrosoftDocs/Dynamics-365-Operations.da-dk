--- 
title: "Opsætte momsmyndigheder"
description: "Momsmyndighederne er enheder, som opkrævet moms skal være indrapporteret og betalt til."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: e0d8b87e23932ce843791778f65eb77240cc28f4
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-sales-tax-authorities"></a>Opsætte momsmyndigheder

[!include[task guide banner](../../includes/task-guide-banner.md)]

Momsmyndighederne er enheder, som opkrævet moms skal være indrapporteret og betalt til. Du kan betale moms til myndigheden direkte eller via en kreditorkonto, som du opretter til momsmyndigheden. Hvis du gør dette, kan firmaet bruge de almindelige betalingsmetoder, så alle beløb betales til momsmyndigheden til tiden. Hvis du ikke opretter momsmyndigheden som kreditor, skal en eller anden sørge for, at beløbet betales manuelt til momsmyndigheden på forfaldsdatoen. Denne opgave bruger demofirmaet USMF.

1. Gå til Moms > Indirekte skatter > Moms > Momsmyndigheder.
2. Klik på Ny.
3. Skriv en værdi i feltet Momsmyndighed.
4. Skriv en værdi i feltet Navn.
5. Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.
6. Find og vælg den ønskede post på listen.
7. Klik op linket i den valgte række på listen.
8. Vælg rapportlayoutet for dit land/område, hvis der er et tilgængeligt. Hvis de viste rapportlayout ikke svarer til kravene fra momsmyndigheden, kan du bruge standardlayoutet.
9. Angiv værdier i formen Afrunding og felterne Afrunding for at angive, hvordan det samlede afgiftsbeløb til betaling skal afrundes. Enhver afrundingsdifference bogføres til Konti til automatiske posteringer, der er oprettet i Finans.
10. Angiv et tal i feltet Afrunding.
11. Klik på Gem.

