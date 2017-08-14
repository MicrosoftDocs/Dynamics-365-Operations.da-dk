---
title: "Angive primosaldi for løn"
description: "Emnet beskriver trinnene til angivelse af primosaldi for lønkoder, fradrag, frynsegoder og moms. Disse oplysninger er vigtig for partnere, som vil overflytte eller overføre data til en ny lønimplementering fra et andet system."
author: kherr
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: d9e3018eb7b6c20cfd5e23a10d15e230009196de
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---

# <a name="enter-payroll-beginning-balances"></a>Angive primosaldi for løn

[!include[banner](../../includes/banner.md)]

Emnet beskriver trinnene til angivelse af primosaldi for lønkoder, fradrag, frynsegoder og moms. Disse oplysninger er vigtig for partnere, som vil overflytte eller overføre data til en ny lønimplementering fra et andet system. Som indledning til at angive primolønsaldi skal vi kontrollere følgende oplysninger:

> * Medarbejderregistreringer er angivet og er tilgængelige i systemet
> * Følgende data er konfigureret og tildelt til medarbejdere:

> > * Betalingscyklusser og lønperioder
> > * Lønkoder
> > * Moms
> > * Frynsegoder og fradrag

> * Virksomheden skal have valgt en dato, som skal gælde for angivelse af primosaldi for løn.

> * Der er indsamlet oplysninger om alle indtægter, frynsegoder/fradrag, frynsegodebidrag, medarbejderskat, selskabsskat og deres år til dato-beløb fra det gamle system.

Når du skal angive primosaldi, skal du overveje, hvor detaljerede dataene skal være. De fleste virksomheder angive et enkelt, konsolideret år-til-dato-beløb. Hvis der kræves mere detaljerede oplysninger, kan saldi dog angives kvartalsvis. Angivelse af det detaljeringsniveau, der er nødvendigt, bestemmer også, hvor mange manuelle betalingsopgørelser der skal oprettes for hver arbejder. Der er kun brug for én manuel opgørelse for hver medarbejder for et enkelt år-til-dato-beløb. Brug år-til-dato-beløb fra den endelige betalingsopgørelse fra det tidligere system som det beløb, der skal angives i det nye lønsystem, for at bruge dette.

Følgende eksempel viser, hvordan du kan angive medarbejderens primolønsaldi, herunder lønkoder, frynsegoder/fradrag og skat. I et eksempel fra den virkelige verden har du et linjeelement for hver lønkode, hvert frynsegodefradrag, frynsegodebidrag, medarbejderskat og selskabsskat, hvor det angivne beløb er år-til-dato-beløbet. Brug listen over koder og beløb, og følg trinene for at oprette en manuel løn- og betalingsopgørelse. Deaktiver regnskab for at overføre primosaldi i forbindelse med lønbehandling.  Du skal deaktivere regnskab, fordi du ikke vil bogføre primosaldoen for denne betalingsopgørelse til finanskontiene. Det blev foretaget i det oprindelige system og overføres til det nye system, når du definerer startsaldi i Finans.

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a>A. Sådan konfigurerer du lønkoder, der skal bruges på primolønsaldi
Når du angiver primosaldi for løn, skal du kontrollere, at de lønkoder, du vil bruge, er konfigureret, så indstillingen "Tillad redigering af satser på lønopgørelsen" er aktiveret. På denne måde kan du manuelt indtaste beløbet fra det oprindelige system. 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a>B. Oprette lønopgørelse for en medarbejder med en primosaldo
Dette trin opretter manuelt en lønopgørelse for hver arbejder for den sidste lønperiode af oprindelige system, som opretter lønopgørelseslinjerne i nye lønsystem. Angiv én linje pr. lønkode og år til dato-beløb og timer. Der er følgende trin i eksemplet:

1. Åbn siden **Alle lønopgørelser**, og klik på **Ny**.  

Angiv følgende: 

| Felt      | Værdi                 |
|------------|-----------------------|
| Arbejdstråd     | Michael Redmond       |
| Betalingscyklus  | sm                    |
| Lønperiode | 16-06-2017 - 30-06-2017 |

2. Under fanen **Post på lønopgørelse** skal du angive følgende:

Linje 1: Fanen **Post på lønopgørelse**

| Felt            | Værdi       |
|------------------|-------------|
| Lønkode    | Fast løn |
| Mængde         | 1,00        |
| Afgrænsning             | 30.000      |
| Fanen Linjedetaljer |             |
| Manuelt           | (markeret)    |

Linje 2: Fanen **Post på lønopgørelse**

| Felt            | Værdi    |
|------------------|----------|
| Lønkode    | Bonus    |
| Mængde         | 1.0000   |
| Kurs             | 4250.00  |
| Fanen Linjedetaljer |          |
| Manuelt           | (markeret) |

Linje 3: Fanen **Post på lønopgørelse**

| Felt           | Værdi      |
|-----------------|------------|
| Lønkode   | Provision i standardvaluta |
| Mængde        | 1.0000     |
| Kurs            | !,299.00   |
| Kurs            | 1,299.00   |
| Fanen Linjedetalje |            |
| Manuelt          | (markeret)   |

> [!NOTE]
> Det er vigtigt, at indstille skyderen **Manuel** til **Ja** under fanen **Linjedetaljer** for hver lønopgørelseslinje, når der skal angives primolønsaldi for hver arbejder.

3. I ruden **Handling** skal du klikke på **Frigiv lønopgørelse** USA-FED-ER-FICA.

4. Klik i ruden **Handling** på **Betalingsopgørelse** for at åbne siden **Generér betalingsopgørelser**, og angiv følgende:

| Felt              | Værdi     |
|--------------------|-----------|
| Betalingsdato       | 6/30/2017 |
| Betalingskørselstype   | Manuelt    |
| Deaktiver regnskab |   Ja     |

> [!NOTE] 
> Dette er kun tilgængeligt, når betalingskørselstypen er manuel, og når brugeren vil deaktivere regnskab for lønkørslen.

Klik på **OK**, og luk **Infolog**.

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a>Hvorfor skal skyderen Deaktiver regnskab være indstillet til Ja, når der genereres betalingsopgørelser?
Indstilling af skyderen til **Ja** forhindrer, at linjer i betalingsopgørelsen fordeles til Finans. Finansbeløb blev opdateret tidligere, da kontosaldi fra det oprindelige system blev angivet. Når du angiver primosaldi for løn, kan du generere rapporter, der indeholder oplysninger fra tidligere år, samt til at identificere grænser med tanke på frynsegoder og til skattemæssige formål.   

### <a name="c-create-pay-statements-for-employees"></a>C. Oprette betalingsopgørelser for medarbejdere
Når du har oprettet betalingsopgørelser, der har primosaldi, skal du kontrollere, at opgørelserne præcist afspejler lønoplysninger. Du skal også manuelt opdatere oplysningerne om frynsegoder og skat, så de svarer til værdierne i det oprindelige lønsystem. Når du har kontrolleret, at beløbene fra oprindelige lønsystem svarer til beløbene på de aktuelle betalingsopgørelser, skal du færdiggøre betalingsopgørelserne.

1. Åbn siden **Alle betalingsopgørelser**.

2. Fremhæve den sidst genererede betalingsopgørelse for Michael Redmond

3. Klik på **Rediger** for at åbne siden **Betalingsopgørelse**.

4. Åbn fanen **Frynsegodefradrag**, og angiv følgende:

| Felt                           | Værdi            |
|---------------------------------|------------------|
| Frynsegode                         | Fradragsbeløb |
| 401K | Deltag              | 3000.00          |
| Tandlægeforsikring | SubSp                  | 495,00           |
| Beløb til sikring af afhængige | Deltag | 2500.00          |
| Vision | SupSp                  | 500,00           |

5. Angiv følgende under fanen **Frynsegodebidrag**:

| Felt              | Værdi               |
|--------------------|---------------------|
| Frynsegode            | Bidragsbeløb |
| 401K | Deltag | 3000,00             |
| Tandlægeforsikring | SubSp     | 495,00              |
| Vision | SubSp     | 500,00              |

6. Angiv følgende under fanen **Skattefradrag**:

| Felt           | Værdi            |
|-----------------|------------------|
| Momskode        | Fradragsbeløb |
| USA-FED-ER-FICA | 1600.00          |
| USA-FED-ER-MEDI | 825.75           |

7. Angiv følgende under fanen **Skattebidrag**:

8. Klik på **Beregn**.
> [!IMPORTANT] 
> Kontroller, at de samlede beløb på betalingsopgørelsen svarer til år til dato i det oprindelige system for arbejderen. Du kan eventuelt vente med afslutningen i næste trin for at foretage en overordnet validering af alle samlede betalingsopgørelser. Efter valideringen skal du gennemse alle betalingsopgørelser og færdiggøre dem.

Den samme proces kan evt. udføres kvartalsvis for alle tidligere kvartaler i året. Dette er kun nødvendigt, hvis kunden har brug at se dataene pr. kvartal uden at skulle gå tilbage til det oprindelige system.

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a>Hvis du laver en fejl under angivelse af primosaldi for en medarbejder
Det er muligt at tilbageføre posteringer og angive dem igen. Hvis du vil tilbageføre posteringen, skal du blot udføre følgende trin på siden **Alle betalingsopgørelser**.

1. Klik på **Tilbagefør**.

2. Klik på **Ja**, når meddelelsen "Når du tilbagefører denne betalingsopgørelse, oprettes en tilbageførselsbetalingsopgørelse til modregning af betalingsopgørelsen. Ingen af betalingsopgørelserne kan redigeres. Vil du tilbageføre denne betalingsopgørelse?" vises. 

Når du tilbagefører betalingsopgørelsen, kan du generere en ny betalingsopgørelse for arbejderen ud fra den lønopgørelse, du har oprettet tidligere. Sørg for at rette forkerte linjer på lønopgørelsen, før du genererer den nye betalingsopgørelse, og derefter genererer nye betalingsopgørelser med de korrekte beløb. 

