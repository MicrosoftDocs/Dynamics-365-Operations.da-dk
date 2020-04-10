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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc6aeb39591c68cae78537faa077010d68628b02
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144760"
---
# <a name="set-up-sales-tax-authorities"></a>Opsætte momsmyndigheder

[!include [banner](../../includes/banner.md)]

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

