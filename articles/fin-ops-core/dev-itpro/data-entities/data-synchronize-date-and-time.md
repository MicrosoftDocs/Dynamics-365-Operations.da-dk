---
title: Synkronisere dato og klokkeslæt i importjob
description: Brug UTC-tidszoner i importjob for at undgå problemer med tidszonekonverteringer.
author: Sunil-Garg
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41c0ec805a20a525989e0133e5dffb29ce3fed39
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748663"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>Synkronisere dato og klokkeslæt i importjob

[!include [banner](../includes/banner.md)]

Det er vigtigt at angive tidszonen for importjobbet til UTC-tid (Coordinated Universal Time). Der kan forekomme uventede datoer og klokkeslæt i de importerede data, hvis du bruger en anden indstilling. Uden den korrekte indstilling konverterer importprocessen UTC-datoen til det lokale format, og systemindstillingerne konverterer det igen.

Denne dobbelte konvertering bevirker, at der ændres datoer mellem programmer. Konverteringen kan f.eks. bevirke, at en medarbejders startdato er forskellig i Dynamics 365 Human Resources og Dynamics 365 Finance pga. forskelle i lokale tidszoner. Når importjobbet indstilles til UTC-tid, løses dette problem.

1. Vælg **Datastyring** i Dynamics 365 Finance and Operations.

2. Vælg **Importer projekter**, og vælg derefter projektet.

3. Vælg **CSV-Unicode** under **Kildedatoformat**.

   [![Skifte kildedatoformat til UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. Skift **Tidszone** til **UTC-tid**, og skift **Sprog** til **da-dk**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]