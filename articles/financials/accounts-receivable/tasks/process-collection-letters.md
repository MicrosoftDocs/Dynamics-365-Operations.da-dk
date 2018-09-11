--- 
title: Behandle rykkere
description: "Denne procedure viser, hvordan du kan oprette, udskrive og bogføre rykkere."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, SysQueryForm, CustCollectionLetterNote
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="process-collection-letters"></a>Behandle rykkere

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


