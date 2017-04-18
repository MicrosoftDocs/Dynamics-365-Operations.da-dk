---
title: Konfigurere udligning
description: "Hvordan og hvornår transaktioner udlignes, kan det være indviklede emner, så det er vigtigt, at du forstår og definerer korrekte parametre for at opfylde virksomhedens behov. I denne artikel beskrives de parametre, der bruges til udligning for både Kreditor og Debitor."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 6927ed98c82f174a18d3d8821fbdb302801835c4
ms.lasthandoff: 03/31/2017


---

# <a name="configure-settlement"></a>Konfigurere udligning

Hvordan og hvornår transaktioner udlignes, kan det være indviklede emner, så det er vigtigt, at du forstår og definerer korrekte parametre for at opfylde virksomhedens behov. I denne artikel beskrives de parametre, der bruges til udligning for både Kreditor og Debitor. 

Følgende parametre påvirker, hvordan udligninger, der behandles i Microsoft Dynamics 365 for operationer. Udligning er udligning af en faktura mod en betaling eller en kreditnota. Disse parametre er placeret i området **Udligning** på siderne **Debitorparametre** og **Kreditorparametre**.

-   **Automatisk udligning** – Angiv denne indstilling til **Ja**, hvis en transaktion automatisk skal udlignes mod andre åbne poster, når den bogføres. Hvis denne indstilling er angivet til **Nej**, kan brugerne manuelt kan udligne posteringer, når de angiver betalinger eller senere ved hjælp af siden **Udligne transaktioner**.
-   **Kasserabat** – Angiv hvordan en [kasserabat håndteres, når en faktura er betalt for meget](cash-discount-handling-overpayments.md). Kasserabatten kan reduceres, kan blive behandlet som en forskel, eller det kan være på kontoen for den debitor eller kreditor for en overbetaling.
    -   **Løs** – Kasserabatbeløbet reduceres med overbetalingsbeløbet. Denne funktion bruges altid, uanset om overbetalingsbeløbet er over eller under det beløb, der er angivet i feltet **Maksimal over- eller underbetaling**.
    -   **Præcis** – Det for meget betalte beløb bogføres enten til en finanskonto til kasserabatdifference eller forbliver en saldo på debitorens eller kreditorens konto. Funktionen Præcis afhænger af, om det overbetalte beløb er mellem 0,00 og det beløb, der er angivet i feltet **Maksimal over- eller underbetaling**, eller om det overbetalte beløb er mere end beløbet for **Maksimal over- eller underbetaling**.
-   **Maksimal øredifference** – Angiv den maksimalt tilladte øredifference for udlignede transaktioner. Hvis differencen er lig med eller mindre end den øredifference, der er angivet i dette felt, bogføres differencen automatisk på finanskontoen til øredifferencer, som angivet på siden **Konti til automatisk posteringer**.
-   **Maksimal over- eller underbetaling** – Angiv det beløb, der accepteres som overbetaling eller underbetaling. Hvis du vil beregne moms af overbetalinger eller underbetalinger, skal du på siden **Økonomiparametre** klikke på **Moms** og derefter indstillingen **Moms af over- eller underbetaling**.
    -   Hvis overbetalingen eller underbetalingen resulterer i en difference, der er mindre end den difference, der er defineret i feltet **Maksimal øredifference**, bogføres øredifferencebeløbet på øredifferencekontoen.
    -   Hvis overbetalingen eller underbetalingen resulterer i en difference, der er større end den difference, der er defineret i feltet **Maksimal øredifference**, bogføres differencebeløbet på den differencekonto, der er valgt for bogføringstypen **Debitor, kasserabat** eller **Kreditor, kasserabat** på siden **Konti til automatisk posteringer**.
-   **Beregn kasserabatter for delbetalinger** – Angiv denne indstilling til **Ja** for at aktivere kasserabatter til at blive beregnet automatisk for delbetalinger.
    -   Effekten af denne indstilling afhænger af værdien i feltet **Anvend kasserabat** på siden **Udlign transaktioner**. Hvis denne indstilling er angivet til **Ja**, tages rabatten, når feltet **Anvend kasserabat** er angivet til **Normal**. Når feltet **Brug kasserabat** er angivet til **Altid**, tages kasserabatten altid uanset indstillingen i dette felt. Når feltet **Brug kasserabat** er angivet til **Aldrig**, tages kasserabatten aldrig uanset indstillingen i dette felt.
    -   Hvis denne indstilling er angivet til **Ja**, og en bruger ændrer værdien i feltet **Beløb, der skal udlignes** på siden **Udlign transaktioner**, beregnes rabatten automatisk og vises som standardangivelse i feltet **Kasserabatbeløb, der skal medtages**.
    -   Hvis denne indstilling er angivet til **Nej**, og en bruger ændrer værdien i feltet **Beløb, der skal udlignes** på siden **Udlign transaktioner**, er standardangivelsen i feltet **Kasserabatbeløb, der skal medtages** **0** (nul).
-   **Beregn kasserabatter for kreditnotaer** – Angiv denne indstilling til **Ja** for automatisk at beregne en kasserabat for kreditnotaer. I Debitor er en kreditnotatransaktion en negativ transaktion, der har en værdi i feltet **Faktura** på siden **Fritekstfaktura** eller en returnering på siden **Salgsordre**.
    -   Effekten af denne indstilling afhænger af værdien i feltet **Anvend kasserabat** på siden **Udlign transaktioner**. Hvis denne indstilling er angivet til **Ja**, er den rabat, når de *** Brug kasserabat *** er indstillet til **Normal**. Når den *** Brug kasserabat *** er indstillet til **altid**, kasserabatten altid uanset indstillingen i dette felt. Når den *** Brug kasserabat *** er indstillet til **aldrig**, kasserabatten aldrig uanset indstillingen i dette felt.
    -   Hvis denne indstilling er angivet til **Ja**, ,og en kreditnota er markeret på siden **Udlign transaktioner**, beregnes rabatten automatisk og vises som standardangivelse i feltet **Kasserabatbeløb, der skal medtages**.
    -   Hvis denne indstilling er angivet til **Nej**, og en kreditnota er markeret på siden **Udlign transaktioner**, er standardangivelsen i feltet **Kasserabatbeløb, der skal medtages** **0** (nul).
-   **Rabatmodkonti (kun AP)** – Definer den finanskonto til kasserabat, der som standard skal bruges til kontoposten for kasserabatter.
    -   **Brug hovedkonto til kreditorrabatter** – Kasserabatten bogføres til den hovedkonto, der er defineret på siden **Opsætning af kasserabat**.
    -   **Konti på fakturalinjer** – Kasserabatten bogføres på finanskontiene på den oprindelige faktura.
-   **Markér linjer til fritekstfakturaer og rentenotaer (kun AR)** – Angiv denne indstilling til **Ja** for at aktivere knappen **Markér fakturalinjer** på siderne **Angiv debitorbetalinger**, **Bilag i kladde for betaling** og **Udlign transaktioner**. Denne knap gør det muligt for brugerne at markere individuelle linjer til udligning.
-   **Prioriter udligning (kun AR)** – Angiv denne indstilling til **Ja** for at aktivere knappen **Markér efter prioritet** på siderne **Angiv debitorbetalinger** og **Udlign transaktioner**. Denne knap kan brugere tildele den foruddefinerede udligningsrækkefølge til transaktioner.  Efter udligningen ordren er blevet udlignet med en transaktion, ændres ordren og betalingsfordelingen før bogføring.
-   **Brug prioritet til automatiske udligninger** – angiver denne indstilling til **Ja** at bruge definerede prioritetsrækkefølgen, når posteringer udlignes automatisk. Dette felt vises kun, hvis den **Prioriter udligning** og **automatisk udligning** er indstillet til **Ja**.


