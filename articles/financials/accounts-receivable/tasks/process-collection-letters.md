---
title: Behandle rykkere
description: Denne procedure viser, hvordan du kan oprette, udskrive og bogføre rykkere.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 8a3f74d2891c050294e089eae14ba2386449d7c9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549623"
---
# <a name="process-collection-letters"></a>Behandle rykkere

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du kan oprette, udskrive og bogføre rykkere. Denne opgave bruger demofirmaet USMF.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Konfigurere et rykkerforløb i en posteringsprofil
1. Gå til **Kredit og inkasso > Opsætning > Debitorposteringsprofiler**.
2. Klik på **Rediger**.
3. Vælg et rykkerforløb på rullelisten. Hvis du ikke vil oprette rykkere for transaktioner med denne posteringsprofil, skal du lade feltet være tomt.  
4. Udvid fanen Tabelbegrænsninger for at ændre den måde, som rykkere behandles på. Hvis dette felt er indstillet til **Ja**, oprettes rykkerne for denne posteringsprofil.  

## <a name="create-collection-letters"></a>Opret rykkere
1. Gå til **Kredit og inkasso > Rykker > Opret rykkere**.
2. Vælg de transaktionstyper, du vil rykke for. Alle åbne transaktioner for disse typer medtages i beregningen.  
2. Vælg en indstilling i feltet **Rykker**.
3. Angiv datoen for rykkeren.
4. Vælg en posteringsprofil, hvis du har ændret **Anvend posteringsprofil fra** til **Vælg**. Der er to indstillinger for posteringsprofiler:   
   - **Konto** – Brug den posteringsprofil, der er tildelt debitorens konto for hver rentenota.   
   - **Vælg** – Brug den posteringsprofil, som du vælger i feltet **Posteringsprofil**.  
5. Udvid sektionen **Poster, der skal indgå**.
6. Klik på **Filtrér**.
7. Angiv et debitor-id i feltet **Kriterier**. Indtast for eksempel "US-001".
8. Klik på **OK**.
9. Klik på **OK**.

## <a name="print-collection-letters"></a>Udskrive rykkere
1. Gå til **Kredit og inkasso > Rykker > Gennemse og behandl alle rykkere**.
2. Vælg **Oprettet** i feltet **Status**.
3. Vælg **Ikke udskrevet** i feltet **Udskrevet**.
4. Klik på **Udskriv**.
5. Klik på **Rykkernota**.
6. Udvid sektionen **Poster, der skal indgå**.
7. Angiv skæringsdatoen for bogføringer.
8. Klik på **OK** for at udskrive rykkeren.
9. Bogfør rykkeren.
   1. Klik på **Bogfør**.
   2. Angiv rykkerens bogføringsdato.
   3. Udvid sektionen **Poster, der skal indgå**.
   4. Klik på **OK**.
   5. Vælg **Bogført** i feltet **Status**.
   6. Vælg en indstilling i feltet **Udskrevet**.

## <a name="control-collection-letters-at-the-customer-level"></a>Styre rykkere på debitorniveau
Du kan også konfigurere rykkere på debitorniveau, så rykkerkoden for hver postering spores, mens rykkerbehandlingen baseres på niveauet for den enkelte rykker, der er gemt for debitoren. Enkeltrykkeren indeholder alle posteringer, der er forfaldne for debitoren. Da respitdagene nu spores på debitorniveau, bliver den næste rykker ikke sendt, før antallet af respitdage er overskredet for den næste rykker i rækkefølgen, selvom posteringer er forfaldne, efter at den sidste rykker blev sendt. Denne indstilling reducerer det antal rykkere, du skal sende pr. debitor. 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>Konfigurere debitor for at styre rykkere på debitorniveau
1.  Gå til **Kredit > Opsætning > Debitorparametre**, og klik på fanen **Rykkere**. 
2.  Rediger værdien i **Opret rykker pr.** til **Debitor**. 
3.  Gå til **Kredit og inkasso > Rykker > Gennemse og behandl alle rykkere**. Der genereres kun én rykker for en debitors samlede forfaldne posteringer.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Ignorere betalinger og kreditnotaer ved beregning af rykkerkoden
Hvis du medtager betalinger og kreditnotaer i de posteringer, der skal medtages i rykkerne, har du muligvis betalinger eller kreditnotaer, der udløser en rykker. Du kan styre, hvordan betalinger og kreditnotaer styrer rykkerkoden ved at ændre værdien af parameteren **Ignorere betalinger og kreditnotaer ved beregning af rykkerkoden**. 

Gør følgende for at ignorere betalinger og kreditnotaer ved beregning af rykkerkoden.
1. Gå til **Kredit > Opsætning > Debitorparametre**, og klik på fanen **Rykkere**. 
2. Vælg **Ja** for **Ignorere betalinger og kreditnotaer ved beregning af rykkerkoden**.
