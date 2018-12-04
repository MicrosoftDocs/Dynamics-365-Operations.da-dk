---
title: "Værdiregulering af udenlandsk valuta for kreditor og debitor"
description: "Variationer i valutakurser medfører, at den teoretiske værdi (bogførte værdi) af åbne posteringer i fremmed valuta varierer over tid. Denne artikel indeholder oplysninger om processen til værdiregulering af udenlandsk valuta, som du skal køre for at opdatere værdien af åbne transaktioner i Kreditor og Debitor."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustExchRateAdjustment, VendExchRateAdjustment
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14211
ms.assetid: defb1ea5-1f3e-4859-87d8-3f9954d3f388
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 259b487b0f11b19af9609d63f12114dcaa61be52
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="foreign-currency-revaluation-for-accounts-payable-and-accounts-receivable"></a>Værdiregulering af udenlandsk valuta for kreditor og debitor

[!include [banner](../includes/banner.md)]

Variationer i valutakurser medfører, at den teoretiske værdi (bogførte værdi) af åbne posteringer i fremmed valuta varierer over tid. Denne artikel indeholder oplysninger om processen til værdiregulering af udenlandsk valuta, som du skal køre for at opdatere værdien af åbne transaktioner i Kreditor og Debitor. 

Den teoretiske værdi, eller bogførte værdi, af åbne posteringer i udenlandsk valuta varierer over tid på grund af udsving i valutakurserne. Hvis du vil opdatere værdien af åbne posteringer i kreditor og debitor, skal du køre processen til værdiregulering af udenlandsk valuta. Værdiregulering af udenlandsk valuta kan køres for både kreditor og debitor. Processen bruger en ny valutakurs til at regulere de åbne, eller ikke-udlignede beløb, på en angivet dato. Forskelle mellem de oprindelige bogførte beløb og de revaluerede beløb vil medføre ikke-realiseret gevinst eller tab for hver åbne postering. Kreditor- og debitorreskontroposterne opdateres derefter for at afspejle det ikke-realiserede gevinst eller tab, og en regnskabspost bogføres til Finans.

## <a name="simulate-a-foreign-currency-revaluation"></a>Simulere en værdiregulering af udenlandsk valuta
Før du foretager værdiregulering af beløb i udenlandsk valuta i åbne posteringer, kan du køre en rapport for værdireguleringen af udenlandsk valuta for den samme dato og metode. Du kan køre simuleringsrapporten på siden **Værdiregulering af udenlandsk valuta** ved at klikke på knappen **Simulering**. Rapporten indeholder et eksempel på ikke-realiserede gevinst- eller tabsbeløb, baseret på de parametre, der er defineret for simuleringen.

## <a name="process-a-foreign-currency-revaluation"></a>Behandl værdiregulering af udenlandsk valuta
Brug siden **Værdiregulering af udenlandsk valuta** under **Periodiske opgaver** til at regulere åbne posteringer. Du kan køre processen i realtid eller planlægge, at den skal køre ved hjælp af en batch. Når du definerer indstillingerne for processen til værdiregulering, skal du kontrollere, om du vil udskrive en rapport over resultaterne. Værdireguleringsrapporten kan ikke genoptrykkes, når processen er fuldført. Hvis du genererer rapporten for værdireguleringen af udenlandsk valuta, viser den forskellige saldi på debitor/kreditorniveau og valutaniveau:

-   Saldi for debitor eller kreditor, der har posteringer for udenlandsk valuta, der er blevet værdireguleret. Følgende saldi vises:
    -   Den samlede oprindelige saldo i den udenlandske valuta.
    -   Det samlede beløb i udenlandsk valuta i regnskabsvaluta pr. den tidligere værdiregulering.
    -   Det samlede beløb i udenlandsk valuta i regnskabsvaluta pr. den aktuelle værdiregulering.
    -   Forskellen mellem tidligere og aktuel kostpris. Forskellen bogføres som en ikke-realisere gevinst eller tab.
-   Samlede ikke-realiserede gevinst eller tab for hver valuta.

Det registreres, hver gang du kører en værdiregulering af udenlandsk valuta. Fra posten på siden **Værdiansættelse af udenlandsk valuta** skal du vælge **Posteringer** for at se en detaljeret oversigt over posteringer, der er oprettet på grund af værdireguleringen. Hver enkelt bilagspostering repræsenterer den åbne postering, der blev værdireguleret. Hvis en åben postering blev værdireguleret mere end én gang, kan du se to poster, der bruger samme bilag. En post er for tilbageførsel af tidligere ikke-realiseret gevinst eller tab, og den anden post er for nye ikke-realiseret gevinster eller tab. Hvis du vil køre processen til værdiregulering, skal du klikke på knappen **Værdiregulering af udenlandsk valuta**. Angiv relevante indstillinger for følgende parametre:

-   **Metode** – Den metode, der blev brugt til den valgte værdiregulering af udenlandsk valuta:
    -   **Standard** – Værdiregulering af udenlandsk valuta bogføres, uanset om resultatet er et overskud eller et underskud.
    -   **Minimum** – Værdiregulering af udenlandsk valuta bogføres kun, hvis resultatet er et underskud.
    -   **Fakturadato** – Værdiregulering af udenlandsk valuta bruger posteringernes oprindelige valutakurs, som værdireguleres til den oprindelige værdi i regnskabsvalutaen. Virkningen af evt. tidligere værdiregulering af udenlandsk valuta annulleres.
-   **Vurderet den** – Den dato, hvor alle posteringer, der har åbne (ikke-udlignede) beløb på den dato, findes. Beløb i udenlandsk valuta værdireguleres ved hjælp af de valutakurser, der er angivet på siden **Valutakurser** for den pågældende dato. Når beløb i udenlandsk valuta værdireguleres på en bestemt dato, bliver denne dato den seneste værdireguleringsdato af udenlandsk valuta for de posteringer, der værdireguleres. Hvis du kører værdiregulering af udenlandsk valuta for en bestemt dato, som ligger tidligere end den seneste værdireguleringsdato af udenlandsk valuta på allerede regulerede posteringer, justerer det periodiske job ikke posteringer, som er åbne på den tidligere dato, men har en nyere seneste værdireguleringsdato af udenlandsk valuta.
-   **Kursdato** – Den dato, der bestemmer, hvilken valutakurs der bruges i værdiregulering af udenlandsk valuta.
-   **Anvend posteringsprofil fra** – Den posteringsprofil, der bruges til at angive standardhovedkontoen for debitor eller kreditor for regnskabsposterne for værdireguleringsposteringerne af udenlandsk valuta:
    -   **Bogføring** – Debitorposteringens posteringsprofil bruges.
    -   **Vælg** – Indtast posteringsprofilen i feltet **Posteringsprofil**.
-   **Posteringsprofil** – Hvis **Vælg** er valgt i feltet **Brug posteringsprofil fra**, bestemmer posteringsprofilen, du angiver i dette felt, posteringsprofilen for værdireguleringsposteringer af udenlandsk valuta.
-   **Økonomiske dimensioner** – De økonomiske dimensioner, der bogføres på regnskabsposter for værdireguleringsposteringerne af udenlandsk valuta:
    -   **Ingen** – Der bogføres ingen økonomiske dimensioner. Hvis du har en økonomisk dimension, der kræves i din kontostruktur, køres værdireguleringsprocessen stadig, og der oprettes regnskabsposter, der ingen økonomiske dimensioner har. Du modtager en advarsel først, så du kan annullere reguleringen.
    -   **Tabel** – Debitor- eller kreditorkontoens økonomiske dimensioner bogføres på værdireguleringsposteringerne af udenlandsk valuta.
    -   **Bogføring** – De økonomiske dimensioner for den postering, der værdireguleres, bogføres på værdireguleringsposteringerne af udenlandsk valuta. De økonomiske dimensioner fra den oprindelige posterings AR/AP-finanskonto bruges til værdiregulering af posteringens AR/AP-hovedkonto som standard, og de økonomiske dimensioner fra den oprindelige posterings finanskonto for udgift/aktiv/omsætning bruges til værdiregulering af posteringens hovedkonto for ikke-realiseret gevinst/tab.





