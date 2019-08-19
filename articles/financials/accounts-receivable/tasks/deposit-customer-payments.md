---
title: Deponere debitorbetalinger
description: Deponer debitorbetalinger.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: afbf74d1cf3dc87e97dda0873115b5c7fa49ca3d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834457"
---
# <a name="deposit-customer-payments"></a>Deponere debitorbetalinger

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deponer debitorbetalinger. Denne opgave bruger demofirmaet USMF.

1. Gå til Kreditor > Betalinger > Betalingskladde.
2. Klik på Ny.
3. Klik på rullelisten i feltet Navn for at åbne opslaget.
4. Vælg betalingskladden. 
5. Klik på Linjer.
6. Vælg den debitor, du registrerer betalingen for, i feltet Konto.
7. Angiv beløbet i betalingen i feltet Kredit.
    * Du kan vælge at undlade at udfylde beløbet og få systemet til at beregne det ved at vælge de fakturaer, der blev betalt.  
8. Indtast en værdi i feltet Betalingsreference.
    * Betalingsreferencen kunne være checknummeret for den betaling, som du indtaster. Betalingsreferencen er påkrævet, hvis betalingen skal medtages på et indbetalingsbilag.  
9. Marker afkrydsningsfeltet Brug et indbetalingsbilag.
    * Hvis betalingen skal medtages i indbetalingen, kan du ændre indstillingen til Ja.  
10. Klik på Ny.
11. Vælg kunden for den næste betaling i feltet Konto.
12. Angiv betalingsbeløbet i feltet Kredit.
13. Indtast en værdi i feltet Betalingsreference.
14. Marker afkrydsningsfeltet Brug et indbetalingsbilag.
15. Klik på Bogfør.
    * Betalinger skal bogføres, før der kan oprettes et indbetalingsbilag. Dette er for at sikre, at betalingerne ikke ændres, når der genereres et indbetalingsbilag.  
16. Klik på Funktioner.
17. Klik på Indbetalingsbilag.
18. Klik på OK.
    * Den første side bruges til at oprette et indbetalingsbilag.  
19. Klik på OK.
    * Det andet trin er at udskrive indbetalingsbilaget, men dette trin er ikke påkrævet.  

