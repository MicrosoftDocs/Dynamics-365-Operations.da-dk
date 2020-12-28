---
title: Vedligehold generelle budgetreservationer
description: Dette emne indeholder trin til at arbejde med generelle budgetreservationer i den offentlige sektor i Microsoft Dynamics 365 Finance.
author: AlexRenney
manager: AnnBe
ms.date: 04/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetReservation_PSN, BudgetReservationYearEndClose_PSN
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: b4ffed93100d28c0a62c49c932520b1436229ffd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407648"
---
# <a name="maintain-general-budget-reservations"></a>Vedligehold generelle budgetreservationer

[!include [banner](../includes/banner.md)]

I dette emne forklares, hvordan du udfører typiske opgaver i forbindelse med generelle budgetreservationer.

## <a name="create-and-encumber-a-general-budget-reservation"></a>Oprette og behæfte en ny generel budgetreservation

Når du har konfigureret systemet til at bruge generelle budgetreservationer, kan du oprette reservationsdokumenter. Generelle budgetreservationer er tilgængelige for de dokumenter, der kræves til den indkøbsmetode, du vælger. Disse indkøbsmetoder omfatter indkøbsordre, indkøbsrekvisition og kreditorfaktura.

Benyt følgende fremgangsmåde, hvis du vil oprette en generel budgetreservation.

1. Gå til **Budgettering \> Generelle budgetreservationer**.
2. Vælg **Ny**.
3. Angiv felterne efter behov i dialogboksen **Budgetreservation**.

    - Reservationstypen bestemmer, hvilken type dokument der skal eftergives denne generelle budgetreservation: en indkøbsrekvisition, en indkøbsordre eller en kreditorfaktura.
    - Hvis du vælger en reference til en indkøbsrekvisition i denne dialogboks, eftergives en upstream indkøbsrekvisition. I dette tilfælde skal den reservationstype, du vælger, være konfigureret med **Indkøbsordre** eller **Kreditorfaktura** som eftergivelsesdokument.

4. Vælg **OK**.
5. I hovedet på siden med detaljer skal du angive felterne efter behov.
6. Vælg **Tilføj linje** i oversigtspanelet **Generelle budgetreservationslinjer**. Angiv oplysningerne for den første linje i reservationen. Gentag dette trin, indtil du har angivet alle linjer.

    - Hvis en indkøbsrekvisition gælder for budgetreservationen, men der ikke blev refereret til den tidligere i dialogboksen **Budgetreservation**, kan du i oversigtspanelet **Linjedetaljer** vælge den indkøbsrekvisitionslinje, som den valgte linje i budgetreservationsreferencer. Varer og tjenester på den valgte rekvisitionslinje, sammen med indkøbskategori, overføres til linjen for den generelle budgetreservation. Dette funktionsmåde gælder for både varer i et indkøbskatalog og varer uden for katalog.
    - Den generelle budgetreservationslinje afspejler ikke nogen underordnede beløb i en refereret indkøbsrekvisition. Disse underordnede beløb omfatter rabatter, gebyrer eller moms.

7. Hvis du bruger projektregnskab, skal du i oversigtspanelet **Linjedetaljer** under fanen **Projekt** angive felterne efter behov.
8. Hvis du bruger projektregnskab, skal du vælge **Bindende omkostninger** i oversigtspanelet **Generelle budgetreservationslinjer**. Siden **Bindende omkostninger** åbnes og viser de bindende omkostninger, der er relateret til den valgte linje.
9. Når du er færdig med at angive hoved- og linjeværdierne, skal du enten sende reservationen til arbejdsgangssystemet eller bogføre den, afhængigt af konfigurationen.

## <a name="view-a-general-budget-reservation"></a>Få vist en generel budgetreservation

Du kan få vist detaljer om en generel budgetreservation, f.eks. oplysninger om kreditoren, de bestilte varer eller tjenesteydelser og budgetoplysninger. Du kan også få adgang til de kildedokumenter, som reservationen henviser til.

1. Gå til **Budgettering \> Generelle budgetreservationer**.
2. Vælg dokumentnummeret på den reservation, du vil have vist. Siden med detaljer vises.
3. Vælg **Regnskab** i handlingsruden, og vælg derefter **Reskontrokladde**, **Få vist fordelinger** eller **Bilag** for at få vist disse poster.
4. For at få vist alle relaterede indkøbsrekvisitioner skal du i oversigtspanelet **Linjedetaljer** vælge indkøbsrekvisitionens referencenummer.
5. Hvis du vil have vist en oversigt over finansregnskabet, skal du vælge **Administrer \> Finansoversigt** i handlingsruden. På listen **Reservationslinje** kan du vælge den linje, du vil se detaljer for.
6. Hvis du vil have vist detaljer om eftergivelsen for budgetreservationen, skal du vælge **Administrer \> Eftergivelsesoplysninger** i handlingsruden. Hvis du vil se det oprindelige dokument, der eftergiver denne generelle budgetreservation (f.eks. en faktura eller en købsordre), skal du vælge **Vis eftergivelsesdokument**.

    Du kan også få adgang til siden **Oplysninger om eftergivelse af generel budgetreservation** på siden **Finansoversigt for generel budgetreservation** ved at vælge **Eftergivelsesoplysninger**.

## <a name="modify-a-general-budget-reservation"></a>Ændre en generel budgetreservation

Hvis reservationen er i en arbejdsgang, skal du tilbagekalde arbejdsgangsstatussen til **Kladde** og derefter sende den ændrede reservation til arbejdsgangen igen.

1. Gå til **Budgettering \> Generelle budgetreservationer**.
2. Åbn den ønskede reservation.
3. Vælg **Rediger** i handlingsruden.
4. Foretag evt. nødvendige ændringer. Du kan f.eks. tilføje eller slette linjer.

    Når en reservationslinje allerede er refereret af en indkøbsordre eller en kreditorfaktura, er din mulighed for at ændre eller slette linjer begrænset.

5. Vælg **Bogfør** i handlingsruden.

## <a name="delete-a-general-budget-reservation"></a>Slette en generel budgetreservation

1. Gå til **Budgettering \> Generelle budgetreservationer**.
2. Vælg den reservation, der skal slettes.

    Reservationer kan kun slettes, hvis de har reservations- og arbejdsgangsstatussen **Kladde**. Du kan kun slette reservationer, der aldrig er blevet bogført.

3. Vælg **Slet** i handlingsruden.
4. Vælg **Ja**.

## <a name="cancel-a-general-budget-reservation"></a>Annullere en generel budgetreservation

1. Gå til **Budgettering \> Generelle budgetreservationer**.
2. Vælg den reservation, du vil annullere.

    Reservationer kan kun annulleres, hvis de har reservations- og arbejdsgangsstatussen **Bogført**. Du kan kun annullere reservationer, der ikke har nogen downstream eftergivelsesaktivitet.

3. Vælg **Generel budgetreservation \> Annuller** i handlingsruden.
4. Vælg **Ja**.

    - Der forekommer opdateringer af Finans og budgetkontrol, og posteringen registreres i posteringsloggen.
    - Denne procedure sletter ikke reservationen. Den annullerer reservationen og genererer de regnskabs- og budgetposter, som skal tilbageføre virkningen af det dokument, der oprindeligt blev bogført.
    - Du kan annullere en hel generel budgetreservation, men du kan ikke annullere individuelle linjer.

## <a name="finalize-a-general-budget-reservation"></a>Færdiggøre en generel budgetreservation

1. Gå til **Budgettering \> Generelle budgetreservationer**.
2. Åbn den reservation, der skal færdiggøres.

    Reservationer kan kun færdiggøres, hvis de har reservations- og arbejdsgangsstatussen **Bogført**. Du kan kun færdiggøre reservationer eller reservationslinjer, der har downstream eftergivelsesaktivitet.

3. Udfør ét af følgende trin:

    - Hvis du vil færdiggøre hele budgetreservationen, skal du vælge **Generel budgetreservation \> Færdiggørelse** i handlingsruden.
    - Hvis du kun vil færdiggøre én linje, skal du markere den og derefter vælge **Færdiggør linje** i sektionen **Generelle budgetreservationslinjer**.
    - Hvis du vil færdiggøre flere linjer, skal du markere dem og derefter vælge **Færdiggør linje** i sektionen **Generelle budgetreservationslinjer**.

    Regnskabs- og budgetstyringsposter bogføres. Den resterende saldo fjernes fra dokumentet og returneres til budgettet, medmindre dokumentet er et overførselsdokument, og den tilknyttede finansierings- eller reservationstype er indstillet til **Reducer overført budget**.

## <a name="relieve-a-general-budget-reservation"></a>Eftergive en generel budgetreservation

Der findes tre måder at forbruge eller eftergive en generel budgetreservation på:

- **Indkøbsrekvisition** – Henvis direkte til den generelle budgetreservation på en indkøbsrekvisitionslinje. Hvis du vil bruge denne fremgangsmåde, skal du angive budgetreservationslinjen i oversigtspanelet **Linjedetaljer** under fanen **Detaljer**, når du opretter rekvisitionen. Send derefter rekvisitionen til arbejdsgangssystemet. Reservationen eftergives eller forbruges, når rekvisitionen er godkendt.

    Generelle budgetreservationer, der er eftergivet ved hjælp af en indkøbsrekvisition, kan også tildeles til købsaftaler. De er knyttet til de forskellige købsaftalelinjer. Når en indkøbsrekvisition oprettes, og en linje i den er knyttet til en vare eller en kategori, der er defineret i en købsaftale, er det kun de generelle budgetreservationer, der tidligere er tildelt købsaftalen, som kan eftergives.

- **Indkøbsordre** – Henvis til den generelle budgetreservation direkte i indkøbsordrelinjen. Ingen købsaftale er involveret. Hvis du vil bruge denne fremgangsmåde, skal du angive budgetreservationslinjen i oversigtspanelet **Linjedetaljer** under fanen **Generelt**, når du opretter indkøbsordren. Reservationen er eftergivet eller forbrugt, når indkøbsordren er bekræftet.
- **Kreditorfaktura** – Henvis til generelle budgetreservation direkte på en kreditorfaktura. Hvis du vil bruge denne fremgangsmåde, skal du angive budgetreservationslinjen i oversigtspanelet **Linjedetaljer** under fanen **Linjedetaljer**. Reservationen eftergives, når kreditorfakturaen bogføres.

Når du har bogført eller bekræftet et dokument, der henviser til en generel budgetreservation, afspejler budgetreservationssaldoen det eftergivne beløb. Hvis du redigerer, annullerer eller færdiggør det refererende dokument, bliver det eftergivne beløb ikke reduceret eller fjernet. Det er ikke muligt at returnere et eftergivet beløb til saldoen i referencedokumentet.

### <a name="create-a-purchase-requisition-purchase-order-or-vendor-invoice-to-relieve-the-general-budget-reservation"></a>Opret en indkøbsrekvisition, indkøbsordre eller kreditorfaktura for at eftergive den generelle budgetreservation

Følg disse trin for at henvise til en generel budgetreservation på en indkøbsrekvisition, indkøbsordre eller kreditorfaktura.

1. Udfør ét af følgende trin:

    - Gå til **Indkøb og forsyning \> Indkøbsrekvisitioner \> Alle indkøbsrekvisitioner**.
    - Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.
    - Gå til **Kreditor \> Fakturaer \> Ventende kreditorfakturaer**.

2. Vælg **Ny** for at oprette et nyt dokument, eller rediger et eksisterende kladdedokument.
3. Fastlæg referencen, og bogfør dokumentet.

    Hvis du nemmere vil kunne identificere den generelle budgetreservation, du ønsker, skal du vælge **Avancerede valgmuligheder** under referencefeltet.

4. I handlingsruden skal du under fanen **Finans** vælge **Få vist fordelinger**.

    - Finanskontoen på de nye regnskabsfordelinger (overordnede og underordnede) er indstillet til finanskontoen fra regnskabsfordelingen for den generelle budgetreservationslinje.
    - Referencefordelingen på de nye regnskabsfordelinger (overordnede og underordnede) refererer til regnskabsfordelingen for den generelle budgetreservationslinje.

## <a name="carrying-forward-general-budget-reservations"></a>Overføre generelle budgetreservationer

Det gælder for alle generelle budgetreservationer, som ikke er udløbet og stadig har en restsaldo ved regnskabsårets afslutning, at du kan overføre dokumentet til det nye år. Overførselsprocessen opretter nødvendige regnskabs- og budgetteringsposter for at lukke dokumentet for det indeværende år og åbne dokumentet for det nye år.

### <a name="carry-forward-a-general-budget-reservation-to-a-new-fiscal-year"></a>Overføre en generel budgetreservation til et nyt regnskabsår

1. Gå til **Finans \> Luk periode \> Proces for ultimo ved årsafslutning for generel budgetreservation**.
2. Vælg, om du vil overføre det tilknyttede budget for reservationen, i feltet **Indstilling for årsafslutning** i dialogboksen **Proces for ultimo ved årsafslutning for generel budgetreservation**.
3. Vælg regnskabsåret for **Ultimoparametre** og **Primoparametre**.
4. Vælg **Hent dokumenter**.
5. Angiv kriterier for at finde de reservationer, du vil behandle og overføre til det nye år, i forespørgselsdialogboksen.
6. Vælg **OK** for at få vist reservationerne i dialogboksen **Proces for ultimo ved årsafslutning for generel budgetreservation**.
7. Vælg de dokumenter, der skal medtages, på listen, og vælg derefter **Behandl**.
8. Hvis du valgte **Udfør behandling af og overfør budget** i feltet **Indstilling for årsafslutning**, får du vist en meddelelse med alle de budgetposter, der er oprettet, og alle de generelle budgetreservationer, der er blevet behandlet. Dokumenter, der ikke blev behandlet pga. en fejl, vises også.

### <a name="reduce-carry-forward-budget-in-a-new-fiscal-year"></a>Reducere overført budget i et nyt regnskabsår

Hvis du har aktiveret budgetstyring, kan du reducere det overførte budget for alle overførte generelle budgetreservationer, der er afsluttet og har en restsaldo. På denne måde kan du hjælpe med at garantere, at midler fra det forrige år ikke bruges på køb i det nye år.

Hvis der er valgt **Ja** i indstillingen **Reducer overført budget** i den tilknyttede fonds- eller reservationstype, og du færdiggør dokumentet i det nye regnskabsår, bliver den resterende dokumentsaldo og et eventuelt resterende overført budget reduceret til 0 (nul).
