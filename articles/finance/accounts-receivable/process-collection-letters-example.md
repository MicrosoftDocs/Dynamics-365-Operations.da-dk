---
title: Behandle eksempel på rykkere
description: I dette emne gennemgås et eksempel, der viser processen til oprettelse, udskrivning og bogføring af rykkere.
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 1bb1889e9450685f7b6a5000e2ef81d1a65f1b51
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/06/2022
ms.locfileid: "8721809"
---
# <a name="process-collection-letters-example"></a>Behandle eksempel på rykkere

[!include [banner](../../includes/banner.md)]

I dette emne gennemgås et eksempel, der viser processen til oprettelse, udskrivning og bogføring af rykkere. Eksemplet er baseret på **Ignorer betalinger og kreditnotaer ved beregning af indstillingen for rykkerkode** i Kredit og rykkere. Det bruger data i USMF-demofirmaet og en ny kunde, US-045.

Når du vil starte, skal du gå til **Debitor \> Kunder \> Alle kunder**, vælge **Ny**, og derefter angive de nødvendige oplysninger for at oprette kunde US-045.

Når du er færdig, skal du følge disse trin.

1. Gå til **Kredit og rykkere \> Rykker \> Konfigurer rykkerforløb**, og konfigurer rykkersekvensen, som vist i følgende tabel, som er tildelt debitorens posteringsprofil.

|     Rykkerkode      |     Betegnelse                           |     Valuta      |     Hovedkonto        |     Gebyr i valuta     |     Minimum for over        |     Antal dage      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     Rykker 1         |     Anden besked med gebyr        |     USD           |                           |     0,00                  |     0,00                  |     2                 |
|     Rykker 2         |     Anden besked med gebyr        |     USC           |     403150                |     20.00                 |     10.00                 |     3                 |
|     Incasso                    |     Sidste besked med gebyr         |     USD           |     403150                |     50.00                 |     100.00                |     15                |

I følgende illustration vises de oplysninger, der vises i tabellen, som de vises på siden **Rykkere**. 

[![Konfigurere et rykkerforløb.](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)

 Du skal nu angive de to parametre, der skal bruges til dette eksempel.

2. Gå til **Kredit og rykkere \> Opsætning \> Debitorparametre**, og følg disse trin.

    1. På fanen **Rykkere** skal du indstille **Ignorer betalinger og kreditnotaer ved beregning af indstillingen for rykkerkode** til **Ja**.
    2. Kontroller, at feltet **Opret rykker** pr. felt er angivet til **Debitor**.

    [![Angive debitorparametre for kreditrykkere.](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)

3. Gå til **Debitor \> Fakturaer \> Alle fritekstfakturaer**, vælg **Ny**, og følg derefter disse trin:

    1. Vælg **US-045** i feltet **Debitorkonto**.
    2. I feltet **Fakturadato** angives **1/15/2021**.
    3. I feltet **Forfaldsdato** angives **1/16/2021**.
    4. På oversigtspanelet **Fakturalinjer** i feltet **Hovedkonto** skal du skrive **401100**.
    5. Indtast **500.00** i feltet **Enhedspris**.
    6. Vælg **Bogfør**.

    Du skal nu indtaste to kreditnotaer for kunden.

4. Vælg **Ny**, og følg derefter følgende fremgangsmåde:

    1. Vælg **US-045** i feltet **Debitorkonto**.
    2. I feltet **Fakturadato** angives **1/15/2021**.
    3. I feltet **Forfaldsdato** angives **1/16/2021**.
    4. På oversigtspanelet **Fakturalinjer** i feltet **Hovedkonto** skal du skrive **401100**.
    5. I feltet **Enhedspris** skal du indtaste **-100.00**.
    6. Vælg **Bogfør**.

5. Gentag trin 4, men skriv **-200,00** i feltet **Enhedspris**.
6. Gå til **Debitor \> Debitorer \> Alle debitorer**, og vælg debitor **US-045**. Vælg derefter i handlingsruden **Transaktioner \> Transaktioner** for at gennemse de debitorposteringer, du har bogført tidligere.

    [![Gennemgå de bogførte debitorposteringer.](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)

    Du skal nu oprette rykkere til debitor US-045.

7. Gå til **Kredit og rykkere \> Rykker \> Opret rykkere**, og følg disse trin.

    1. Angiv indstillingerne for **faktura** og **Kreditnota** til **Ja**.

        Som standard skal feltet **Rykker** angives til **Rykker pr. debitor**.

    2. I feltet **Fakturadato** angives **1/19/2021**.
    3. I oversigtsfeltet **Poster, der skal indgå** skal du vælge **Filter** og derefter i feltet **Kundekonto** skal du tilføje **US-045**.
    4. Vælg **OK**.
    5. Vælg **OK** for at oprette rykkere.

8. Gå til **Kredit og rykkere \> Rykker \> Gennemse og behandle rykkere**, og følg disse trin.

    1. Bemærk, at rykkerkoden både på hoved- og posteringslinjerne er **Rykker 1**, da denne rykker er den første rykker i sekvensen. (Hvis du vil have vist posteringslinjerne, kan du være nødt til at vælge oversigtspanelet **Posteringer**.)

   [![Kontrollere, at den samme rykkerkode vises i sidehovedet og på linjerne.](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)

    2. Vælg **Bogfør** i handlingsruden.
    3. I feltet **Bogføringsdato** angives **1/19/2021**.

    Du skal nu oprette rykkere igen til debitor US-045.

9. Gå til **Kredit og rykkere \> Rykker \> Opret rykkere**, og følg disse trin.

    1. Angiv indstillingerne for **faktura** og **Kreditnota** til **Ja**.

        Som standard skal feltet **Rykker** angives til **Rykker pr. debitor**.

    2. I feltet **Fakturadato** angives **1/23/2021**.
    3. I oversigtsfeltet **Poster, der skal indgå** skal du vælge **Filter** og derefter i feltet **Kundekonto** skal du tilføje **US-045**.
    4. Vælg **OK**.
    5. Vælg **OK** for at oprette rykkere.

10. Gå til **Kredit og rykkere \> Rykker \> Gennemse og behandle rykkere**, og følg disse trin.

    1. Bemærk, at rykkerkoden i hovedet er **Rykker 1**. Koden på posteringslinjerne er **Rykker 2**.

   [![Kontrollere, at forskellige rykkerkoder vises i sidehovedet og på linjerne.](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)

  Koden er anderledes, fordi **Ignorer betalinger og kreditnotaer ved beregning af indstillingen for rykkerkode** er angivet til **Ja**.

  2. Bogfør ikke rykkeren.

11. Gå til **Kredit og rykkere \> Opsætning \> Parametre for debitorer**, og på fanen **Rykkere** skal du angive indstillingen **Ignorer betalinger og kreditnotaer ved beregning af indstillingen for rykkerkode** til **Nej**.

    [![Angive Ignorer betalinger og kreditnotaer ved beregning af indstillingen for rykkerkode til Nej.](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)

    Du skal nu oprette rykkere igen til debitor US-045.

12. Gå til **Kredit og rykkere \> Rykker \> Opret rykkere**, og følg disse trin.

    1. Angiv indstillingerne for **faktura** og **Kreditnota** til **Ja**.

        Som standard skal feltet **Rykker** angives til **Rykker pr. debitor**.

    2. I feltet **Fakturadato** angives **1/23/2021**.
    3. I oversigtsfeltet **Poster, der skal indgå** skal du vælge **Filter** og derefter i feltet **Kundekonto** skal du tilføje **US-045**.
    4. Vælg **OK**.
    5. Vælg **OK** for at oprette rykkere.

13. Gå til **Kredit og rykkere \> Rykker \> Gennemse og behandle rykkere**, og bemærk at rykkerkoden på både hovedet og i transaktionslinjerne er **Rykker 2**.

    [![Vise igen, at den samme rykkerkode vises i sidehovedet og på linjerne](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)

    Den samme kode vises begge steder, fordi **Ignorer betalinger og kreditnotaer ved beregning af indstillingen for rykkerkode** nu er angivet til **Nej**.
