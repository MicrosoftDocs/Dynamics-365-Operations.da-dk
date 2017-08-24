--- 
title: Behandle rykkere
description: "Denne procedure viser, hvordan du kan oprette, udskrive og bogføre rykkere."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 58dc6176f54a33eda47604b65f5580c21a93fcd7
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="process-collection-letters"></a>Behandle rykkere

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du kan oprette, udskrive og bogføre rykkere. Denne opgave bruger demofirmaet USMF.


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Konfigurere et rykkerforløb i en posteringsprofil
1. Gå til Kredit og inkasso > Opsætning > Debitorposteringsprofiler.
2. Klik på Rediger.
    * Vælg et rykkerforløb på rullelisten. Hvis du ikke vil oprette rykkere for transaktioner med denne posteringsprofil, skal du lade feltet være tomt.  
    * Under fanen Tabelbegrænsninger kan du ændre den måde, som rykkere behandles på. Hvis dette felt er indstillet til Ja, oprettes rykkerne for denne posteringsprofil.  
3. Luk siden.

## <a name="create-collection-letters"></a>Opret rykkere
1. Gå til Kredit og inkasso > Rykker > Opret rykkere.
    * Du skal vælge de posteringstyper, du vil rykke for. Alle åbne transaktioner for disse typer medtages i beregningen.  
2. Vælg en indstilling i feltet Rykker.
3. Angiv datoen for rykkeren.
    * Der findes to posteringsprofilindstillinger: Konto – Brug den posteringsprofil, der er tildelt kundekontoen for hver rentenota.   Vælg – Brug den posteringsprofil, som du vælger i feltet Posteringsprofil.  
    * Vælg en posteringsprofil, hvis du har ændret "Anvend posteringsprofil fra" til Vælg.  
4. Udvid posterne for at inkludere sektion.
5. Klik på Filtrér.
6. Angiv Kunde-id i feltet Kriterier. Indtast for eksempel "US-001".
7. Klik på OK.
8. Klik på OK.

## <a name="print-collection-letters"></a>Udskrive rykkere
1. Gå til Kredit og inkasso > Rykker > Gennemse og behandl alle rykkere.
2. Vælg "Oprettet" i feltet Status.
3. Vælg "Ikke udskrevet" i feltet Udskrevet.
4. Klik på Udskriv.
5. Klik på Rykkernota.
6. Udvid posterne for at inkludere sektion.
7. Angiv skæringsdatoen for bogføringer
8. Klik på OK for at udskrive rykkeren.

## <a name="post-the-collection-letter"></a>Bogføre rykkeren
1. Klik på Bogfør.
2. Angiv rykkerens bogføringsdato.
3. Udvid posterne for at inkludere sektion.
4. Klik på OK.
5. Vælg "Bogført" i feltet Status.
6. Vælg en indstilling i feltet Udskrevet.


