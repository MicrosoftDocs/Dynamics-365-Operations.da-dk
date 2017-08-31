--- 
title: "Oprette og bogføre en fritekstfaktura for en debitor i den offentlige sektor (Danmark)"
description: "Denne procedure hjælper dig med at oprette og bogføre en fritekstfaktura for en debitor ved hjælp af elektronisk OIOUBL-fakturering."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Denmark
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 3455ea54cb79e21b39dd901b398563a680248c21
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-post-a-free-text-invoice-for-a-public-sector-customer-denmark"></a>Oprette og bogføre en fritekstfaktura for en debitor i den offentlige sektor (Danmark)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure hjælper dig med at oprette og bogføre en fritekstfaktura for en debitor ved hjælp af elektronisk OIOUBL-fakturering. 



Den blev oprettet ved hjælp af demodatafirmaet USMF med primær adresse for en juridisk enhed i Danmark.



Det er den fjerde af seks procedurer, der viser den afsluttende proces til oprettelse af e-fakturaer ved hjælp af elektroniske rapporteringskonfigurationer. Den er baseret på OIOUBL-e-fakturaen, der er fælles for Danmark, Østrig og Norge. Du kan finde mindre forskelle for andre landespecifikke e-fakturaimplementeringer, som spansk eller italiensk, i tilgængelige WIKI-artikler.



Før du kan udføre denne procedure, skal du udføre følgende procedurer: 'Importere elektroniske rapporteringskonfigurationer for elektronisk OIOUBL-fakturering', 'Konfigurere elektronisk OIOUBL-fakturering' og 'Konfigurere en debitorkonto til elektronisk OIOUBL-fakturering'.

1. Gå til Debitor > Fakturaer > Alle fritekstfakturaer.
2. Klik på Ny.
3. Indtast eller vælg en værdi i feltet Kundekonto.
    * En kunde, der er valgt til fritekstfakturaen, skal være aktiveret til elektronisk fakturering.  
4. Vælg en visning for overskrift for fritekstfaktura.
5. Udvid afsnittet Kunde.
6. Skriv en værdi i feltet Debitorrekvisition.
7. Skriv en værdi i feltet Kundereference.
8. Indtast eller vælg en værdi i feltet Kontakt.
9. Vælg en visning for fritekstfakturalinjer.
10. Markér den valgte række på listen.
11. Indtast en værdi i feltet Beskrivelse.
12. Angive de ønskede værdier i feltet Hovedkonto.
13. Angiv et tal i feltet Enhedspris.
14. Klik på Bogfør.
15. Klik på OK.

## <a name="generate-an-oioubl-electronic-invoice"></a>Oprette en elektronisk OIOUBL faktura
1. Klik på Send.
2. Klik på Oprindelig.
    * Du kan kontrollere jobstatus og hente den faktiske fil på siden Elektroniske rapporteringsjob.  


