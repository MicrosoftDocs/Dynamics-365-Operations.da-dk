---
title: Behandle rykkere
description: I dette emne vises, hvordan du kan oprette, udskrive og bogføre rykkere.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 2b8ce102086535a5462d3fa0e8ac76e9ec3dd15c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441495"
---
# <a name="process-collection-letters"></a>Behandle rykkere

[!include [banner](../../includes/banner.md)]

I dette emne vises, hvordan du kan oprette, udskrive og bogføre rykkere. Denne opgave bruger demofirmaet USMF.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Konfigurere et rykkerforløb i en posteringsprofil
1. Gå til **Navigationsrude > Moduler > Kredit > Opsætning > Debitorposteringsprofiler**.
2. Klik på **Rediger**.
3. Vælg et rykkerforløb på rullelisten. Hvis du ikke vil oprette rykkere for transaktioner med denne posteringsprofil, skal du lade feltet være tomt.  
4. Udvid fanen **Tabelbegrænsninger** for at ændre den måde, som rykkere behandles på. Hvis dette felt er indstillet til **Ja**, oprettes rykkerne for denne posteringsprofil.  

## <a name="create-collection-letters"></a>Opret rykkere
1. Gå til **Navigationsrude > Moduler > Kredit > Rykker > Opret rykkere**.
2. Vælg de transaktionstyper, du vil rykke for. Alle åbne transaktioner for disse typer medtages i beregningen.  
3. Vælg en indstilling i feltet **Rykker**.
4. Angiv datoen for rykkeren i feltet **Rykkerdato**.
5. Vælg en posteringsprofil, hvis du har ændret **Anvend posteringsprofil fra** til **Vælg**. Der er to indstillinger for posteringsprofiler:   

   - **Konto** – Brug den posteringsprofil, der er tildelt debitorens konto for hver rentenota.   
   - **Vælg** – Brug den posteringsprofil, som du vælger i feltet **Posteringsprofil**.  

6. Udvid sektionen **Poster, der skal indgå**.
7. Vælg **Filter**.
8. Angiv et debitor-id i feltet **Kriterier**. Indtast for eksempel "US-001".
9. Vælg **OK**.
10. Vælg **OK**.

## <a name="print-collection-letters"></a>Udskrive rykkere
1. Gå til **Navigationsrude > Moduler > Kredit > Rykker > Gennemse og behandl alle rykkere**.
2. Vælg **Oprettet** i feltet **Status**.
3. Vælg **Ikke udskrevet** i feltet **Udskrevet**.
4. Vælg **Udskriv**.
5. Vælg **Rykkernota**.
6. Angiv skæringsdatoen for posteringerne i sektionen **Parametre**.
7. Udvid sektionen **Poster, der skal indgå**, og angiv oplysningerne for rykkernotaen.
8. Vælg **OK** for at udskrive rykkeren.
9. Bogfør rykkeren.

    1. Vælg **Bogfør**.
    1. Angiv rykkerens bogføringsdato.
    1. Udvid sektionen **Poster, der skal indgå**.
    1. Vælg **OK**.
    1. Vælg **Bogført** i feltet **Status**.
    1. Vælg en indstilling i feltet **Udskrevet**.

## <a name="control-collection-letters-at-the-customer-level"></a>Styre rykkere på debitorniveau
Hvis der oprettes rykkere på transaktionsniveau, kan der oprettes flere breve for en kunde ud fra den aldersfordelte transaktion. Hvis der vises transaktioner i forskellige brevsekvenser, genereres der separate rykkere for hver gruppe af forfaldne transaktioner for kunden. Derfor kan en individuel kunde f.eks. modtage en rykker for transaktioner, der er 60 dage forsinket, og en anden rykker for transaktioner, som er 90 dage forsinkede. 

Hver rykker knyttes også til en rykkerkode. Rykkerkoden knyttes til individuelle transaktioner og bruges til at bestemme, hvornår den næste rykker skal genereres for hver transaktion. Hvis en postering f.eks. er mere end 30 dage forsinket, bestemmer rykkerkoden, at den næste rykker sendes, når transaktionen bliver 60 dage forsinket, hvis den ikke betales før. 

Rykkere kan også konfigureres på kundeniveau. I dette tilfælde spores rykkerkoden for hver transaktion, mens rykkerbehandlingen baseres på niveauet for den enkelte rykker, der er gemt for kunden. Den enkelte rykker indeholder alle de transaktioner, der er forfaldne for kunden. Da respitdagene nu spores på kundeniveau, bliver den næste rykker ikke sendt, før antallet af respitdage er overskredet for den næste rykker i rækkefølgen, selvom posteringer er forfaldne, efter at den sidste rykker blev sendt. Denne indstilling hjælper med at reducere det antal rykkere, du skal sende pr. kunde.

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>Konfigurere debitor for at styre rykkere på debitorniveau
1.  Gå til **Navigationsrude > Moduler > Kredit > Opsætning > Debitorparametre**, og vælg fanen **Rykkere**. 
2.  Rediger værdien i **Opret rykker pr.** til **Debitor**. 
3.  Gå til **Navigationsrude > Moduler > Kredit > Rykker > Gennemse og behandl alle rykkere**. Der genereres kun én rykker for en debitors samlede forfaldne posteringer.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Ignorere betalinger og kreditnotaer ved beregning af rykkerkoden
Hvis du medtager betalinger og kreditnotaer i de posteringer, der skal medtages i rykkerne, har du muligvis betalinger eller kreditnotaer, der udløser en rykker. Du kan styre, hvordan betalinger og kreditnotaer styrer rykkerkoden ved at ændre værdien af parameteren **Ignorere betalinger og kreditnotaer ved beregning af rykkerkoden**. 

Gør følgende for at ignorere betalinger og kreditnotaer ved beregning af rykkerkoden.

1. Gå til **Navigationsrude > Moduler > Kredit > Opsætning > Debitorparametre**, og klik på fanen **Rykkere**. 
2. Vælg **Ja** for **Ignorere betalinger og kreditnotaer ved beregning af rykkerkoden**.
