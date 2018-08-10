---
title: "Regulere lagerbeholdninger på lagerstedet (grundlæggende lagerstyring)"
description: "Denne fremgangsmåde fører dig gennem processen med at oprette og bogføre en lagerreguleringsjournal for at justere lagerbeholdningerne af varer på lageret."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9ca5841fe857990cae8d9551ccf79c3c0fd490ae
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a>Regulere lagerbeholdninger på lagerstedet (grundlæggende lagerstyring)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde fører dig gennem processen med at oprette og bogføre en lagerreguleringsjournal for at justere lagerbeholdningerne af varer på lageret. Du skal have oprettet et lagerjournalnavn for lagerreguleringer, før du begynder på dette. Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data. Disse opgaver udføres normalt af en lagermedarbejder.


## <a name="create-an-inventory-adjustment-journal"></a>Oprette en lagerreguleringsjournal
1. Gå til Lagerstyring > Kladdeposteringer > Elementer > Lagerregulering.
2. Klik på Ny.
3. Klik på rullelisten i feltet Navn for at åbne opslaget.
4. På listen skal du klikke på det lagerreguleringsjournalnavn, du vil bruge.
    * Nogle andre felter udfyldes baseret på opsætningen af det lagerreguleringsjournalnavn, du vælger.  
5. Klik på OK.

## <a name="create-journal-lines"></a>Oprette journallinjer
1. Klik på Ny.
2. Marker feltet Varenummer på listen.
3. Vælg en vare i feltet Varenummer. Hvis du bruger demodatafirmaet USMF, kan du skrive 'D0001'.
4. Klik på rullelisten i feltet Sted for at åbne opslaget.
5. Vælg et sted på listen.
6. Klik på rullelisten i feltet Lagersted for at åbne opslaget.
7. Vælg et lagersted på listen.
    * Hvis du har valgt et element med Lokalitet som en obligatorisk dimension, skal du angive lokaliteten her.  
8. Angiv et tal i feltet Antal.
    * Feltet Kostpris angiver kostprisen pr. enhed for lagertilgange. Hvis omkostningen ikke er defineret for varenummeret, eller hvis du vil ændre den manuelt, skal du gøre det her.  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a>Kontrollere og bogføre lagerreguleringsjournalen.
1. Klik på Valider.
2. Klik på OK.
3. Klik på Bogfør.
    * Når du bogfører denne kladdetype, bogføres en lagertilgang eller -afgang, lagerniveauet og -værdien ændres, og der genereres finansposteringer.  
4. Klik på OK.
5. Luk formularen.
6. Luk siden.

