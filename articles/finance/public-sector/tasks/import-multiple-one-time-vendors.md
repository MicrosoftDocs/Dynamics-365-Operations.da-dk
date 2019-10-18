---
title: Importere og oprette engangskreditorer og -fakturaer i den offentlige sektor
description: Når der ikke kræves godkendelse eller en aftale i form af en indkøbsordre, kan du oprette en faktura for en ny kreditor, som du ikke har nogen regelmæssige relationer med, samtidig med at du opretter en post for kreditoren.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendImportOneTimeVendFileUpload_PSN
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Public sector
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e6996603b028ac4a55e1791ca80721f4da74fcb5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174588"
---
# <a name="import-and-create-multiple-one-time-vendors-and-invoices-in-the-public-sector"></a>Importere og oprette engangskreditorer og -fakturaer i den offentlige sektor

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

