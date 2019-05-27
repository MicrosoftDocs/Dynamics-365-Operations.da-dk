---
title: Opsætte momsmyndigheder
description: Momsmyndighederne er enheder, som opkrævet moms skal være indrapporteret og betalt til.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 909433a04c1185039938f6233b30c235e7b8ed8b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549504"
---
# <a name="set-up-sales-tax-authorities"></a>Opsætte momsmyndigheder

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

