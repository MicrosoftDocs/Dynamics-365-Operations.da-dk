---
title: Justere leasingaftaler
description: Emnet forklarer, hvordan du justerer en leasingaftale. Det kan være nødvendigt at foretage en justering, hvis betingelserne for leasingaftalen ændres, leasingaftalen forlænges, eller andre betingelser ændres.
author: moaamer
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7d7151c28d124420638dc4e69a8ab5359ecf443c
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644549"
---
# <a name="adjust-leases"></a>Justere leasingaftaler

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Emnet forklarer, hvordan du justerer en leasingaftale. Det kan være nødvendigt at foretage en justering, hvis betingelserne for leasingaftalen ændres, leasingaftalen forlænges, eller andre betingelser ændres. Aktivleasing er i overensstemmelse med retningslinjerne for, at Accounting Standards Codification Topic 842 (ASC 842) og International Financial Reporting Standard 16 (IFRS 16) omhandler redigering af leasingaftaler. ASC-842-20-15-1 definerer en leasingændring, som enhver ændring af vilkårene og betingelserne i en kontrakt, der medfører en ændring i omfanget af eller overvejelser i forbindelse med en leasingaftale. Punkt 39 i IFRS 16 angiver, at en af modtagerne skal regulere leasingforpligtelsen, så den afspejler ændringer af betalinger af leasingaftalen.

For organisationer, der overholder ASC 842 eller IFRS 16, revurderes en leasingaftale, så den afspejler en ændring i den nuværende værdi af de fremtidige minimums leasingbetalinger (PVFMLP). Hvis PVFMLP øges, vil den oprettede kladdepost være en debitering af kontoen for brugsretsaktivkontoen (ROU) og en kreditering af leasingforpligtelseskontoen for forskellen mellem den nye PVFMLP og den tidligere PVFMLP. Hvis PVFMLP reduceres, vil kladdeposteringen være et debetbeløb af leasingforpligtelseskontoen og en kreditering til ROU-aktivkontoen for forskellen.

Hvis reguleringen reducerer ROU-aktivet til under 0 (nul), krediteres resten med den bogføringskonto for leasingændringer, der er angivet på siden **Leasingsaftalens bogføringskonti**. Systemkontiene for disse transaktioner og andre reguleringsposter, f. eks. klassificeringsændringer, indledende direkte omkostninger, leasingincitamenter, forudbetalinger og faste omkostninger, der opstår i forbindelse med leasingændringer.

Hvis du vil have en specifik vejledning i transaktioner for leasingregulering, anbefales det, at du ser i IFRS 16 og ASC 842.

## <a name="lease-adjustment-wizard"></a>Leasingreguleringsguide

Udfør følgende trin for at oprette en ny leasingaftale. De ændrede data opdaterer leasingplanerne, når du bogfører fra guiden **Leasingjustering**. Du kan gemme dit arbejde og lukke guiden når som helst og derefter vende tilbage senere for at genoptage dit arbejde.

Benyt følgende fremgangsmåde for at åbne guiden **Leasingregulering** fra oversigten over leasingaftalen.

1. Gå til **Aktivleasing \> Leasingaftaler \> Leasingoversigt**. 
2. Vælg den leasingaftale, der skal reguleres, og vælg derefter guiden **Regulering**.
3. Følg vejledningen i guiden for at angive de nødvendige ændringer.

Hvis du vil åbne guiden **Leasingregulering** fra siden **Leasingregulering**, skal du følge disse trin for en regulering, der allerede er i gang.

1.  Gå til **Leasingaftale \> Leasingaftaler \> Leasingreguleringer**.
2.  Vælg en leasingaftale, der har reguleringsstatus **I gang**, og vælg derefter **Reguleringsguiden**.
3.  Angiv de relevante datoer i felterne **Startdato for tilpasning** og **Bogføringsdato**.
4.  Vælg **Næste**.

    Leasingaftalen føjes nu til siden **Leasingreguleringer**, hvor du kan angive de nye oplysninger om den.

    Når leasingaftalen er blevet justeret, gælder felterne for overvejelser om brugerrettigheden for den. Hvis ingen af de indledende direkte omkostninger, leasingincitamenter, forudbetalinger eller faste omkostninger knyttes til den ændrede leasingaftale, skal du lade disse tilhørende felter være tomme. De oprindelige beløb gælder ikke for den opdaterede leasingaftale. 

    En leasinggiver kan f.eks. give $1.000 incitament for at acceptere en forlængelse af en leasingaftale. Hvis du i dette tilfælde justerer leasingaftalen til kontoen for forlængelsen, skal du skrive **1.000** i feltet **Leasingincitamenter efter regulering**.

    Betalingsplanlinjerne viser nu alle betalinger fra måneden og senere måneder i feltet **Startdato for ændring**. Da ændringerne er mulige, kan betalingsplanlinjerne ikke starte, før ændringen starter. Hvis du vil have vist betalingsplanlinjer fra før startdatoen for ændringen, skal du gå til siden **Historik for leasingversion**.

8.  Vælg **Næste**.

    På den næste side vises nøgleoplysninger om den forventede leasingregulering, f.eks. leasingaftalens regnskabsmæssige værdier før ændringen og den nye forventede leasingaftale efter ændringen. På siden vises også en prøveversion af kladdeposten for den forventede leasingregulering.

9.  Vælg **Send til arbejdsgang** for at sende leasingreguleringen til arbejdsgangssystemet, hvis arbejdsgangen for rettighedsregulering er aktiv, og reguleringen endnu ikke er godkendt. Du kan finde flere oplysninger om, hvordan du bruger arbejdsgangen i leasingreguleringen, i [Bruge arbejdsgange i leasingregulering](use-create-lease-wrkflw.md).

    > [!NOTE]
    > På dette tidspunkt genberegner systemet reguleringsvariablerne for at kontrollere, at der ikke er bogført nogen posteringer mod leasingaftalen, siden reguleringsoversigten og reguleringskladdeposten blev beregnet første gang. Hvis værdierne ændres, opdateres gitteret med justeringsoversigten, og du kan gennemse oplysningerne, før du sender leasingreguleringerne til arbejdsgangssystemet igen.

10. Hvis en arbejdsgang ikke er aktiv, eller hvis leasingreguleringen er godkendt, skal du vælge **Afslut** for at behandle ændringerne og bogføre reguleringskladdeposten.

    > [!NOTE] 
    > På dette tidspunkt genberegner systemet reguleringsvariablerne for at kontrollere, at der ikke er bogført nogen posteringer mod leasingaftalen, siden reguleringsoversigten og reguleringskladdeposten blev beregnet første gang. Hvis der ændres værdier, opdateres gitteret med justeringsoversigten, og du kan gennemse ændringerne, før du vælger **Afslut**. Hvis arbejdsgangen er aktiv, og leasingreguleringen er godkendt, vil eventuelle ændringer i oversigten over reguleringer medføre, at godkendelsesstatus ændres til **Ikke sendt**. I dette tilfælde skal du sende leasingreguleringen til arbejdsgangssystemet igen.

    På siden **Leasingreguleringer** er status nu angivet til **Fuldført**.

    På siden **Leasingreguleringer** kan du stadig få vist oversigtspanelerne **Reguleringsoversigt** og **Prøveversion af reguleringspost**. Oplysningerne om leasingaftalen og datooplysningerne vises i versionshistorikken for den pågældende leasing.

    Der oprettes nu en ny leasingversion og et nyt sæt planer ved hjælp af de ændrede oplysninger. 

13. Hvis du vil have vist de nye planer, skal du gå til leasingaftalen og derefter vælge **Bøger**.
14. Hvis du vil have vist den nygenererede betalingsplan, skal du vælge **Betalingsplan**.
15. Hvis du vil se den nye plan for amortisering af leasingforpligtelser, der genereres ud fra de nye informationer, skal du lukke siden **Betalingsplan** og åbne siden **Amortiseringsplanen for leasingforpligtelse**.
16. Hvis du vil se den nyoprettede afskrivningsplan for anlægsaktiver, skal du åbne siden **Afskrivningsplan for aktiver** på siden **Kartotekoplysninger**.
17. Hvis du vil se reguleringskladdeposten, skal du vælge **Kladder \> Aktivleasingkladde**.

## <a name="cancel-a-lease-adjustment"></a>Annullere en leasingregulering

Hvis du vil slette en igangværende leasingregulering, skal du følge disse trin.

1.  Gå til **Leasingaftale \> Leasingaftaler \> Leasingreguleringer**.
2.  Vælg den igangværende leasingregulering, der skal annulleres.
3.  Vælg **Annuller regulering**. 
4.  Vælg **OK**.

    > [!NOTE] 
    > Hvis du vælger **Annuller** i guiden **Leasingregulering**, annullerer du den seneste ændring, du fuldførte i guiden, men du fjerner ikke en igangværende regulering.

## <a name="use-the-lease-adjustment-workflow"></a>Brug arbejdsgangen til justering af leasing

Dette afsnit indeholder en forklaring på, hvordan du bruger arbejdsgangen til justering af leasing. Arbejdsgangen for leasingregulering hjælper dig med at administrere leasingreguleringer på en ensartet måde ved at levere et sæt godkendelsestrin og tildele dem til bestemte brugere, der godkender en leasingregulering, før den bliver endelig. Når leasingreguleringen er godkendt i arbejdsgangen, kan du bruge guiden **Leasingregulering** til at fuldføre leasingreguleringen.

1.  Hvis du vil sende en leasingregulering til godkendelse, skal du gå til **Leasing \> Leasingaftaler \> Leasingreguleringer**.
2.  Vælg den leasing-id for leasingreguleringen, og vælg derefter **Reguleringsguide**.
3.  Vælg **Send til godkendelse** på den sidste side i guiden.
4.  Angiv en kommentar om reguleringen, og vælg derefter **OK**.

    Status for arbejdsgangen ændres til **Afventer godkendelse**, og alle felter i guiden er låst for redigering.

5.  Hvis du vil godkende leasingreguleringen, skal du gå til **Leasing \> Leasingaftaler \> Leasingreguleringer**.
6.  Vælg leasing-id til leasingreguleringen, og gennemse oversigtspanelerne **Reguleringsoversigt** og **Prøveversion af reguleringspost**.
7.  Vælg **Arbejdsgang \> Godkendt**.

    På siden **Leasingreguleringer** er status for arbejdsgangen nu angivet til **Godkendt**. På dette tidspunkt er leasingreguleringen klar til at blive bogført via kladdeposten til regulering.

8.  Hvis du vil fortsætte med at behandle leasingreguleringen og bogføre reguleringsposten, skal du gå til **Leasing \> Leasingaftaler \> Leasingreguleringer**.
9.  Vælg den leasing-id for leasingreguleringen, og vælg derefter **Reguleringsguide**.
10. Vælg **Næste**, indtil du kommer til den sidste side i guiden, og vælg derefter **Afslut**.

Systemet genberegner leasingaftalens opbrugte værdier for at sikre, at de reguleringsvariabler, der er godkendt, er aktuelle. Hvis der sker ændringer, sættes godkendelsesstatussen tilbage til **Kladde**, og du skal sende leasingreguleringen til arbejdsgangssystemet igen.

## <a name="view-lease-versions"></a>Vis leasingversioner

Hvis en leasingaftale er blevet justeret, kan du få vist de forskellige versioner af den. Du kan også se historikplanerne og de tidligere leasingaftaler.

1. Vælg den leasingaftale, der skal kopieres, på siden **Leasingoversigt**, og vælg derefter **Leasingversionshistorik** i handlingsruden.

    Hvis den valgte leasingaftale er blevet justeret, viser siden **Leasingversionshistorik** de forskellige versioner. Den oprindelige leasingaftale er mærket **1**, og efterfølgende versioner har en stigende numerisk rækkefølge.

    I forbindelse med en valgt leasingversion kan du få vist de økonomiske dimensioner, kontraktdetaljer, placeringer og betalingsplanlinjer.

2. Hvis du vil se historikplanerne, skal du åbne den ændrede leasingaftale fra siden **Leasingoversigt**, vælge det ønskede kartotek og derefter vælge **Versionshistorik for kartotek** i handlingsruden.
3. Vælg en version og en plan, der skal vises, på siden **Bogversion**.

## <a name="adjust-a-lease-book"></a>Justere en leasingaftale

Følg disse trin alene for at justere en leasingaftale.

1. Gå til **Aktivleasing** \> **Leasingaftaler** \> **Leasingoversigt**.
2. Vælg og åbn en leasingaftale.
3. På siden **Leasingdetaljer** skal du vælge **Aftaler**.
4. Vælg **Juster aftale** i gruppen **Vedligehold** på Handlingsruden på siden **Detaljer om aftaler**. 
5. Fjern betalingstidsplanslinjer.
6. Angiv ændringsdatoen i feltet **Dato for ændring af leasingaftale**. Overvej derefter at fjerne alle yderligere overvejelser vedrørende aktiv/passiv (første direkte omkostning, rettighedsincitament, forudbetaling af leje, efterstillede omkostninger og værdigaranti), hvis der findes en. 
7. Du kan forhindre unøjagtige beregninger af lejereguleringen ved at tilføje nye betalingsplanlinjer for de nye betalingsdatoer, der svarer til ændringsdatoen. 

> [!NOTE] 
> Det anbefales, at du bruger guiden **Regulering af leasingaftale** til at justere en leasingaftale. Guiden reducerer antallet af manuelle trin, viser en forhåndsversion af saldi efter korrektionen og giver dig mulighed for at ændre beløb, før de bogføres.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
