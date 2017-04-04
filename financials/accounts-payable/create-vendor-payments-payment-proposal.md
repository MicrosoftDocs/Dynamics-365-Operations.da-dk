---
title: "Oprette kreditorbetalinger ved hjælp af et betalingsforslag"
description: "Dette emne indeholder en oversigt over indstillinger til betalingsforslag og indeholder nogle eksempler på, hvordan betalingsforslag fungerer. Betalingsforslag bruges ofte til at oprette kreditorbetalinger, fordi forespørgsel om betalingsforslag kan bruges til hurtigt at vælge kreditorfakturaer til betaling baseret på forfaldsdatoen og kasserabatten."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14312
ms.assetid: 585d5b0b-1b79-4a03-ab18-528918070377
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: b46037b9509f329e18f0da69d530f6b1f88c8888
ms.lasthandoff: 03/31/2017


---

# <a name="create-vendor-payments-by-using-a-payment-proposal"></a>Oprette kreditorbetalinger ved hjælp af et betalingsforslag

Dette emne indeholder en oversigt over indstillinger til betalingsforslag og indeholder nogle eksempler på, hvordan betalingsforslag fungerer. Betalingsforslag bruges ofte til at oprette kreditorbetalinger, fordi forespørgsel om betalingsforslag kan bruges til hurtigt at vælge kreditorfakturaer til betaling baseret på forfaldsdatoen og kasserabatten. 

Organisationer bruger ofte betalingsforslag til at oprette kreditorbetalinger, fordi forespørgsel om betalingsforslag kan bruges til hurtigt at vælge kreditorfakturaer til betaling, baseret på forfaldsdatoen, kasserabatten og andre kriterier. 

Forespørgslen om betalingsforslag indeholder forskellige faner, der hver især har forskellige indstillinger for at vælge fakturaer til betaling. Den **Parameter** under fanen indeholder indstillinger, som et flertal af organisationen bruger mest. På den **poster medtages** oversigtspanelet du kan angive, hvilke fakturaer eller leverandører for at medtage til betaling ved at definere intervaller for forskellige egenskaber. Hvis du ønsker at betale et bestemt interval af kreditorer, kan du definere et filter for området Kreditor. Denne funktion bruges ofte til at vælge fakturaer for en bestemt af betalingsmåden. For eksempel, hvis du definerer et filter hvor **betalingsmåde** = **se**, kun fakturaer, der har denne betalingsmåde er udvalgt til betaling, forudsat at de også opfylder andre kriterier, der er angivet i forespørgslen. Fanen **Avancerede parametre** indeholder flere indstillinger, hvoraf nogle muligvis ikke er relevante for din organisation. Denne fane indeholder f.eks. indstillinger for betaling af fakturaer for centraliserede betalinger.

## <a name="parameters"></a>Parametre
-   **Vælge fakturaer ved** – fakturaer inden for det datointerval, der er angivet af den **fra dato** og **til dato** felter kan vælges efter forfaldsdato, kasserabatdato eller begge dele. Hvis du bruger kasserabatdatoen, der først søges for fakturaer, der har en dato for kasserabat mellem feltet fra dato og til dato. Systemet afgør derefter, om fakturaen er berettiget til kasserabatten, ved hjælp af sessionsdatoen for at sikre, at kasserabatdatoen ikke er overskredet.
-   **Fra dato** og** Til dato** – Fakturaer, der har en forfaldsdato eller kasserabatdato inden for dette datointerval er udvalgt til betaling.
-   **Betalingsdato** – Hvis der er defineret en dato, oprettes alle betalinger på denne dato. Feltet **Dato for minimumsbetaling** ignoreres.
-   **Dato for minimumsbetaling** – Angiv dato for minimumsbetaling. For eksempel det **fra dato** og **til dato** angive et interval fra 1 September til d. 10, og den mindste betalingsdato er 5 September. I dette tilfælde har alle fakturaer, der har en forfaldsdato fra den 1 til 5 September en betalingsdato for September 5. Alle fakturaer, der har en forfaldsdato fra September 5 til 10 September har dog en betalingsdato, der er lig med forfaldsdatoen for hver faktura.
-   **Beløbsgrænse** – Angiv det maksimale samlede beløb for alle betalinger.
-   **Opret betalinger uden faktura eksempel** – Hvis denne indstilling er angivet til **Ja**, betalinger oprettes straks på den **kreditorbetalinger** side. Den **betalingsforslag** side vil blive sprunget over. Betalinger vil derfor blive oprettet hurtigere. Betalinger kan stadig ændres på siden **Kreditorbetalinger**. Alternativt kan du returnere til siden **Betalingsforslag** ved hjælp af knappen **Rediger fakturaer for valgt betaling**.

## <a name="advanced-options"></a>Avancerede indstillinger
-   **Kontroller kreditorsaldo** – Hvis denne indstilling er angivet til **Ja**, kontrollerer systemet, at en kreditor ikke har en debetsaldo, før fakturaen er betalt. Hvis en kreditor har en debetsaldo, oprettes der ingen betaling. Eksempelvis har leverandøren måske kreditnotaer eller betalinger, der er blevet bogført, men endnu ikke er udlignet. I disse tilfælde bør kreditoren ikke betales. I stedet skal kreditnotaer eller betalinger udlignes mod de udestående fakturaer.
-   **Slet negative betalinger** – Denne indstilling fungerer forskelligt, afhængigt af om betalinger er foretaget for enkelte fakturaer eller for summen af fakturaer, der opfylder kriterierne for betaling. Denne adfærd defineres på betalingsmåden .
-   **Betaling for hver faktura** – Hvis indstillingen **Slet negative betalinger** er angivet til **Ja**, og der er en ikke-udlignet fakturaer og betaling for en kreditor, markeres kun fakturaen til betaling. Den eksisterende betaling udlignes i forhold til fakturaen. Hvis indstillingen **Slet negative betalinger** er angivet til **Nej**, og en faktura og betaling ikke er udlignet, vælges både fakturaen og betalingen til betaling. En betaling oprettes for betalingen, og der oprettes en refusion (negativ betaling) til betaling.
-   **Betaling for summen af fakturaer** – Hvis indstillingen **Slet negative betalinger** er angivet til **Ja**, og en ikke-udlignet faktura og betaling findes for en kreditor, vælges både den ikke-udlignede faktura og betalingen til betaling, og beløbene lægges sammen for at frembringe det samlede betalingsbeløb. Den eneste undtagelse opstår, hvis summen resulterer i en refusion. I så fald vælges hverken fakturaen eller betalingen. Hvis den ** Slet negative betalinger ** indstilling er angivet til **ingen**, og en faktura og betaling ikke er udlignet, både fakturaen og betalingen er udvalgt til betaling og beløbene lægges sammen, så det samlede betalingsbeløb.
-   **Udskriv kun rapport** – Angiv denne indstilling til **Ja** for at se resultatet af betalingsforslaget i en rapport, men uden at oprette betalinger.
-   **Medtag kreditorfakturaer fra andre juridiske enheder** – Hvis din organisation har en centraliseret proces til betaling og betalingsforslaget indeholder fakturaer fra andre juridiske enheder, der er inkluderet i søgekriterierne, skal denne indstilling angives til **Ja**.
-   **Foreslå separat kreditorbetaling pr. juridisk enhed** – Hvis denne indstilling er angivet til **Ja**, oprettes der en separat betaling for hver juridisk enhed pr. kreditor. Kreditoren på betalingen er kreditoren fra fakturaen fra hver juridisk enhed. Hvis denne indstilling er angivet til **Nej**, og den samme kreditor har fakturaer i flere juridiske enheder, oprettes en betaling for det samlede beløb af de valgte fakturaer. Kreditoren på betalingen er kreditoren i den aktuelle juridiske enhed. Hvis kreditorkontoen ikke findes i den aktuelle juridiske enhed, bruges kreditorkontoen for den første faktura, der skal betales.
-   **Betalingsvalutaen** – dette felt angiver den valuta, der alle betalinger, der er oprettet i. Hvis der ikke er defineret en valuta, betales hver faktura i fakturaens valuta.
-   **Betalingsugedag** – Angiv den ugedag, hvor betalingen skal foretages. Dette felt bruges kun, hvis betalingsmåden er konfigureret til samlede fakturaer til betaling på en bestemt dag på ugen.
-   **Modkontotype** og **modkonto** – disse felter til at definere en bestemt kontotype angives (f.eks. **Finans** eller **Bank**) og modkonto (f.eks. en bestemt bankkonto). Betalingsmåden for fakturaen, der definerer standardmodkontotype og modkonto, men du kan bruge disse felter til at tilsidesætte standardværdierne.
-   **Ekstra filtre** – på den **poster medtages** oversigtspanel, du kan definere flere områder af kriterier. Hvis du vil betale kun et interval af kreditorer, kan du definere et filter for området Kreditor. Denne funktion bruges ofte til at vælge fakturaer for en bestemt af betalingsmåden. For eksempel, hvis du definerer et filter hvor **betalingsmåde** = **se**, kun fakturaer, der har denne betalingsmåde er udvalgt til betaling, forudsat at de også opfylder andre kriterier, der er angivet i forespørgslen.

## <a name="scenarios"></a>Scenarier
| Kreditor | Faktura | Fakturadato | Fakturabeløb | Forfaldsdato | Kasserabatdato | Kasserabatbeløb |
|--------|---------|--------------|----------------|----------|--------------------|----------------------|
| 3050   | 1001    | 15. juni      | 500,00         | 15. juli  | 29. juni            | 10,00                |
| 3050   | 1002    | 20. juni      | 600,00         | 20. juli  | 4. juli             | 12,00                |
| 3075   | 1003    | 15. juni      | 250,00         | 29. juni  |                    | 0,00                 |
| 3100   | 1004    | 17. juni      | 100,00         | 17. juli  | 1. juli             | 1,00                 |

D. 1 juli betaler April leverandører. Hun bruger et betalingsforslag til at udføre denne opgave mere effektivt.

### <a name="option-1-by-cash-discount"></a>Mulighed 1: Efter kasserabat

April vælger **Kasserabat** som forslagstype. Hun skriver en dato interval af juni 26 til d. 10. Følgende fakturaer medtages i forslaget:

-   1002, fordi rabatdatoen 4. juli ligger i betalingsdatointervallet.
-   1004, fordi rabatdatoen 1. juli ligger i betalingsdatointervallet.

Følgende fakturaer medtages ikke i forslaget:

-   1001, fordi rabatdatoen 29. juni allerede er udløbet, så denne faktura er ikke længere berettiget til kasserabatten.
-   1003, fordi fakturaen ikke har en rabatdato.

### <a name="option-2-by-due-date"></a>Mulighed 2: Efter forfaldsdato

April vælger **Efter forfaldsdato** som forslagstype. Hun skriver en dato interval af juni 26 til d. 10. Følgende fakturaer medtages i forslaget:

-   1003, fordi forfaldsdatoen 29. juni ligger i betalingsdatointervallet.

Følgende fakturaer medtages ikke i forslaget:

-   1001, fordi forfaldsdatoen 15. juli ligger uden for betalingsdatointervallet.
-   1002, fordi forfaldsdatoen 20. juli ligger uden for betalingsdatointervallet.
-   1004, fordi forfaldsdatoen 17. juli ligger uden for betalingsdatointervallet.

### <a name="option-3-by-due-date-and-cash-discount"></a>Mulighed 3: Efter forfaldsdato og kasserabat

April vælger **Forfaldsdato og kasserabat** som forslagstype. Hun skriver en dato interval af juni 26 til d. 10. Følgende fakturaer medtages i forslaget:

-   1003, fordi forfaldsdatoen 29. juni ligger i betalingsdatointervallet.
-   1002, fordi rabatdatoen 4. juli ligger i betalingsdatointervallet.
-   1004, fordi rabatdatoen 1. juli ligger i betalingsdatointervallet.

Følgende fakturaer medtages ikke i forslaget:

-   1001, da rabatdatoen 29 juni allerede er udløbet, så denne faktura er ikke længere berettiget til en kasserabat, og forfaldsdatoen d. 15 er også uden for datointervallet.

## <a name="country-specific-considerations"></a>Lande-/områdespecifikke overvejelser
### <a name="norway"></a>Norge

#### <a name="dimension-control"></a>Dimensionskontrol

Dimensionskontrolelementet styrer gruppering af linjer, der er genereret af betalingsforslag, og angiver standarddimensioner, der er baseret på økonomiske dimensioner, der anvendes for de anvendte fakturaer. Der er en fane for økonomisk dimension, hvor du kan aktivere dimensionskontrol samt aktivere gruppering for hver dimension i norsk landesammenhæng for hver betalingsmetode. De mulige indstillinger er:

-   Feltet **Dimensionskontrol** er deaktiveret. Betalingsforslaget fungerer som for ethvert andet land.
-   Feltet **Dimensionskontrol** aktiveres uden yderligere definition af dimensioner. Der oprettes et betalingsforslag uden hensyntagen til dimensioner. Den oprettede postering arver ingen dimensioner fra den anvendte post.
-   Feltet **Dimensionskontrol** aktiveres, og yderligere dimensioner aktiveres. Nu kan du definere, hvordan dimensionerne skal kopieres til kladden. For eksempel: • Vælg den **afdelingen** afkrydsningsfelt for at oprette et betalingsforslag pr. afdeling for metoden betalingsmåden • Vælg den **CostCenter** afkrydsningsfelt for at oprette et betalingsforslag pr. bærer for metoden for betaling

**Bemærk:** Hvis du vælger mere end én dimension i den tredje indstilling, oprettes der et betalingsforslag for dimensionskombinationen.

#### <a name="bank-account-selection"></a>Valg af bankkonto

Du kan definere en standardbetalingskonto for debitering pr. metode til betaling uanset landekontekst. Dette angives i betalingslinjer, der er genereret af et forslag. Med funktionen til bankkonto kan du definere flere debiteringsbankkonti, der administreres af dimension og valuta eller en kombination af disse for at bruge forskellige debiteringsbankkonti, afhængig af hver enkelt kombination. Du kan konfigurere disse kombinationer i **betalingsmåder** side ved hjælp af den **bankkonti** knap er tilgængelig for hver betalingsmetode med **bogføringstypen for kontoen** = **Bank**.


