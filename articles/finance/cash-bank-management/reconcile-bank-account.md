---
title: Afstemme en bankkonto
description: Denne artikel beskriver, hvordan du afstemmer en bankkonto.
author: angelad116
ms.date: 11/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: angelading
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 12de50f26127c54c2f82ace43487de10e7125aea
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804204"
---
# <a name="reconcile-a-bank-account"></a>Afstemme en bankkonto

[!include[banner](../includes/banner.md)]

Når du modtager et bankkontoudtog, bør du jævnligt afstemme bankposteringer for juridiske enheder med posteringerne på bankkontoudtoget.

Du kan ikke afstemme et bankkontoudtog med en bankkonto, hvis noten af de checks eller indbetalingsbilag, der vises i kontoudtoget aktuelt har statussen **Afventer annullering**. Når en evaluator har bogført eller afvist en tilbageførsel af check eller en annullering af indbetalingsbilag, er statussen ikke længere angivet som **Afventer annullering**, og du kan afstemme bankkontoen.

1. Gå til **Kontant- og bankstyring** \> **Bankkonti** \> **Bankkonti**. Vælg den bankkonto, du vil afstemme med bankkontoudtoget, og vælg derefter **Afstemme** > **Kontoafstemning**.

2. Angiv oplysninger i felterne **Dato for bankkontoudtog** og **Bankkontoudtog**. I feltet **Slutsaldo** kan du angive saldoen på bankkontoen, som den vises på bankkontoudtoget.

3. Vælg **Transaktioner** for at åbne siden **Kontoafstemning**.

4. For hver transaktion, der skal medtages i bankkontoudtoget, skal du markere afkrydsningsfeltet **Afstemt**, hvis beløbet i Dynamics 365 Finance svarer til beløbet på bankkontoudtoget. Du kan også angive eller ændre værdien i feltet **Banktransaktionstype**. Denne feltværdi er vigtigt for statistikken for bankposteringer og for visse rapporter
    

>[!NOTE]
>Du må ikke markere afkrydsningsfeltet **Afstemt** for transaktioner, der ikke findes på bankkontoudtoget. Disse posteringer vises fortsat på denne side, indtil de bliver afstemt med et fremtidigt bankkontoudtog.
>Afkrydsningsfeltet **Afstemt** er ikke tilgængeligt, hvis transaktionen har statussen **Afventer annullering**. Transaktioner kan have denne status, hvis Finance er konfigureret til at kræve, at tilbageførsler eller annulleringer skal sendes til gennemgang, før de bogføres. Når en evaluator har bogført eller afvist modposteringen eller annulleringen, er statussen ikke længere **Afventer annullering**, og du kan afstemme bankkontoen med bankkontoudtoget.


Hvis du vil markere afkrydsningsfeltet **Afstemt** for et checkinterval, der vises på bankkontoudtoget, skal du vælge **Markér checkinterval** og derefter angive intervallet.

5.  Hvis beløbet for en bankkontotransaktion ikke svarer til beløbet for transaktionen på bankkontoudtoget, skal du angive korrektionsbeløbet i feltet **Korrektionsbeløb**.
    

> [!NOTE]
> Hvis regnskabsperioden for den transaktion, der skal rettes, er lukket, kan feltet **Korrektionsbeløb** ikke bruges. I stedet skal du oprette en linje med en posteringsdato, som ligger i en åben regnskabsperiode for korrektionen. I dette tilfælde skal du tilføje de økonomiske dimensioner, der blev brugt på den oprindelige transaktion samt modkontoen.



6.  Opret transaktioner for poster, f.eks. gebyrer og renter, der fremgår af bankkontoudtoget, men som ikke er registreret i Finance. Angiv **Banktransaktionstype** og de relevante økonomiske dimensioner.

7.  Når transaktionerne på bankkontoudtoget markeres som **Afstemt**, nærmer beløbet i feltet **Ikke afstemt**, som genberegnes løbende, efterhånden som du foretager ændringer, sig nul. Når beløbet når nul, skal du vælge **Afstem konto** for at bogføre afstemningen og de transaktioner samt korrektioner, du har oprettet.
    
    Når afstemningen er bogført, kan de poster, der er blevet medtaget, ikke ændres yderligere, og de vil ikke blive vist på fremtidige kontoafstemninger.

8.  Hvis du vil have vist banktransaktioner, der endnu ikke er afstemt, skal du bruge rapporten **Ikke afstemte banktransaktioner**. Hvis du vil have vist kontoudtog for en bankkonto, skal du bruge rapporten **Bankkontoudtog**.

## <a name="cancel-bank-statement-reconciliation"></a>Annuller afstemning af bankkontoudtog 

Med funktionen **Annuller afstemning af bankkontoudtog** kan du annullere afstemning af bankkontoudtog. Hvis du vil bruge denne funktion, skal du aktivere funktionen **Annuller bankkontoudtogsafstemning** i arbejdsområdet **Funktionsstyring**. Du skal også aktivere parameteret **Tillad redigering af bankkontoudtog**. For at gøre dette skal du gå til **Kontant- og bankstyring > Opsætning > Kontant- og bankstyringsparametre > Bankafstemning**.
 
Afstemninger af bankkontoudtog kan kun annulleres i den kronologiske rækkefølge, de er indtastet i. Når en afstemning af bankkontoudtog annulleres, tilbageføres nye transaktioner og rettelser, og alle andre transaktioner markeres som ikke afstemte.
 
Hvis du vil annullere afstemning af bankkontoudtog, skal du vælge bankkontoudtoget og derefter vælge **Bankkontoudtog > Annuller bankafstemning**. På siden **Annuller bankafstemning** skal du angive **Årsagskode**, **Årsagsbemærkning** og **Dato for annullering**. Vælg **OK** for at starte annulleringen. Bemærk, at bankkontoudtogets annulleringsdato skal være den samme som eller senere end bankkontoudtogsdatoen. Når afstemningen af bankkontoudtoget er annulleret, vil feltet **Annulleringsdato** for bankkontoudtoget blive opdateret med den oplyste **Annulleringsdato**. Vælg knappen **Transaktioner** for at få vist de transaktioner, som afstemningen blev annulleret for.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
