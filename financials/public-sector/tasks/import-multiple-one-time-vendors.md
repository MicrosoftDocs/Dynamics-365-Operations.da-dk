--- 
title: Importere og oprette engangskreditorer og -fakturaer i den offentlige sektor
description: "Når der ikke kræves godkendelse eller en aftale i form af en indkøbsordre, kan du oprette en faktura for en ny kreditor, som du ikke har nogen regelmæssige relationer med, samtidig med at du opretter en post for kreditoren."
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
ms.search.industry: Public sector
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: eba32df87c96cb7eeae2766dfdd2efd08a9a5ec2
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="import-and-create-multiple-one-time-vendors-and-invoices-in-the-public-sector"></a>Importere og oprette engangskreditorer og -fakturaer i den offentlige sektor

[!include[task guide banner](../../includes/task-guide-banner.md)]

Når der ikke kræves godkendelse eller en aftale i form af en indkøbsordre, kan du oprette en faktura for en ny kreditor, som du ikke har nogen regelmæssige relationer med, samtidig med at du opretter en post for kreditoren. Denne procedure er oprettet med PSUS-demodatafirmaet i den offentlige sektor partition.

1. Gå til Kreditor > Periodiske opgaver > Importer engangskreditorer og fakturaer.
2. Søg efter og vælg den csv-fil, der indeholder leverandøroplysninger.
3. Klik på rullelisten i feltet Kontostruktur for at åbne opslaget.
4. Find og vælg den ønskede post på listen.
5. Klik på OK.
    * Kreditor- og fakturaoplysningerne er importeret. Hvis der er fejl, bliver der udskrevet en rapport, og du skal rette alle de angivne poster i importfilen og derefter importere filen igen.  
6. Gå til Kreditor > Periodiske opgaver > Behandl engangskreditorer og fakturaer.
    * Der søges efter dublerede kreditornavne eller Federal Tax Id.  Vigtigt! Hvis du vælger ikke at behandle dublerede kreditorer, behandles de relaterede fakturaer heller ikke. Du kan manuelt oprette en faktura ved hjælp af oplysningerne i CSV-filen.    
7. Klik på OK.


