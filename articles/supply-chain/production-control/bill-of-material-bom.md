---
title: Styklister og formler
description: Dette emne indeholder oplysninger om styklister og formler, som er en central del af definitionen af produkter og produktvarianter.
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, EcoResProductProcessManufacturingWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19331
ms.assetid: c19b437a-2de2-4728-9477-2bcb0c2b1f5e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 430e2ab0c4438222ceb9102c011940af803acfbc
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="bills-of-materials-and-formulas"></a>Styklister og formler

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om styklister og formler, som er en central del af definitionen af produkter og produktvarianter. Styklister og formler angiver de nødvendige materialer eller ingredienser for et bestemt produkt. Formler angiver også samprodukter og biprodukter, der modtages i forbindelse med den specifikke produktion. 

<a name="bills-of-materials"></a>Styklister
------------------

En stykliste (BOM) definerer de komponenter, der er nødvendige for at producere et produkt. Komponenterne kan være råvarer, halvfærdige produkter eller ingredienser. I nogle tilfælde kan der være henvist til tjenester i en stykliste. Styklister beskriver dog typisk de *materialeressourcer*, der er nødvendige.  

Når det kombineres med en rute eller et produktionsflow, der beskriver handlingerne og ressourcer, der kræves for at opbygge et produkt, danner styklisten grundlag for beregning af de forkalkulerede omkostninger for produktet.  

En stykliste er en enkelt enhed, der er beskrevet af følgende oplysninger:

-   Stykliste-id
-   Navn på styklisten
-   De styklistelinjer, der beskriver komponenterne og ingredienserne
-   De styklisteversioner, der definerer det produkt og den periode, som styklisten kan bruges for

En enkelt stykliste beskriver et enkelt niveau, der identificeres af et entydigt id. Komponenter kan have deres egne styklister, der refereres til af styklisteversioner. Du kan få vist og redigere det komplette hierarki i styklister for et bestemt produkt i styklistedesigneren.

### <a name="formulas-co-products-and-by-products"></a>Formler, samprodukter og biprodukter

En formel er en undertype af styklisten, der typisk bruges til procesproduktion. Ud over komponenter og ingredienser beskriver en formel samprodukter og biprodukter. I den aktuelle version kræver definitionen af samprodukter og biprodukter for formlen formelversionen. En formel er normalt defineret for ét bestemt færdigt produkt (en formel- eller planlægningsvare), der er defineret i formelversionen.

### <a name="boms-in-the-product-lifecycle"></a>Styklister i produktets levetid

I produktets levetid kan mange typer styklister oprettes af forskellige årsager:

-   **Tegning/udkast til styklisten** – denne stykliste giver et udkast til vurdering af nødvendige materialer i en tidlig designfase og hjælper dig med at oprette et overslag over omkostninger og anslåede produktattributter. Denne stykliste bruges normalt ikke i ERP (Enterprise Resource Planning).
-   **Teknikerstykliste** – Denne stykliste anvendes typisk, når du designer produkter, der er baseret på eksisterende produktporteføljer. Teknikerstyklister er struktureret til at forenkle designprocessen og gruppere komplekse produkter i teknikermoduler. Til enkle produkter kan det være muligt at oprette tekniske styklister for den faktiske produktionsproces. For andre produkter skal den tekniske styklisten imidlertid konverteres til en faktisk produktionsstykliste. Tekniske stykliste er typisk repræsenteret af fantomstyklister i styklistehierarkiet. Selvom tekniske styklister kan bruges til planlægning og udførelse af produktionsoperationer, kan denne fremgangsmåde føre til ineffektivitet, især i gentagne operationer hvor mange ordrer oprettes.
-   **Planlægning af styklisten** – Denne stykliste bruges til at udføre planlægning af materialebehov. Behovet for komponenter og ingredienser beregnes ud fra behovet for de færdige produkter. Ligesom efterkalkulation af styklister kan planlægning af styklister repræsentere en bestemt blanding af materialer, der bruges i en periode.
-   **Produktionsstykliste** – Dette er den faktiske stykliste, der bruges til en bestemt produktion. En produktionsstykliste skal medregne faktiske ressourcer, der bruges til at fremstille produktet. Når der oprettes en produktionsordre, en batchordre eller en kanban, er styklistens niveauer, der er repræsenteret af fantomstyklister, skjult på ét niveau og fordelt over operationer for ordren.
-   **Efterkalkulationsstykliste** – Denne stykliste bruges til at beregne den forkalkulerede omkostning for et produkt. Du kan f.eks. bruge en efterkalkulationsstykliste, når standardomkostning bruges eller den forkalkulerede, planlagte omkostning for et givent produkt beregnes. Efterkalkulationsstyklister kan referere til en bestemt blanding af materialer og ressourcer, som forventes at blive brugt. Du kan derfor bruge efterkalkulationsstykliste til at oprette en repræsentativ forkalkuleret omkostning i en periode og undgå afvigelser over tid.

Hvilke typer af styklisten, der faktisk anvendes i en implementering, afhænger af gennemførelsen og også af de forretningsmæssige scenarier og krav. I enkle implementeringer kan en planlægningsstykliste, produktionsstykliste og efterkalkulationsstykliste modelleres som én stykliste. I miljøer, der har hyppige tekniske ændringer og flere alternative ruter, er et større udvalg af styklistetyper sandsynligvis nødvendigt.

### <a name="approval-of-boms-and-formulas"></a>Godkendelse af styklister og formler

Hver stykliste og formel kan være separat godkendt eller ikke-godkendt. Godkendelse af en stykliste eller formel opstår typisk, når den første relevante styklisteversion er godkendt. Men i nogle forretningsscenarier kan disse godkendelser være forskellige trin i processen, og kan omfatte forskellige procesejere.  

Bemærk, at hvis en stykliste ikke er godkendt, er alle relaterede styklisteversioner heller ikke godkendt.

## <a name="bom-and-formula-versions"></a>Stykliste- og formelversioner
Hvis du vil knytte en bestemt stykliste eller formel til en produktvariant, der kan produceres, skal du oprette en styklisteversion eller formelversion. Gyldigheden af styklisteversioner og formelversioner kan være begrænset af periode, antal, websted, specifikke produktdimensioner og andre kriterier. Formelversioner har flere vigtige attributter, som udbytte, definitioner af samprodukter eller biprodukter og instruktioner til omkostningsfordeling for formlen.

### <a name="approval-of-bom-and-formula-versions"></a>Godkendelse af stykliste- og formelversioner

Før en styklisteversion kan bruges i planlægnings- eller fremstillingsproces, skal den godkendes. Hvis en styklisteversion er godkendt, kan den tilknyttede stykliste også godkendes, afhængigt af brugerens rettigheder for udvælgelse og godkendelse. Bemærk, at en styklisteversion kun kan godkendes, hvis den tilknyttede stykliste selv er godkendt.

### <a name="activation-of-the-default-bom-or-formula-version"></a>Aktivering af standardstykliste eller formelversion

Hvis du vil angive en bestemt stykliste eller formel som standardstyklisteversion eller formelversionen, der skal bruges ved varedisponering eller bruges til at oprette produktionsordrer, skal du aktivere versionen. Når en version er aktiveret, kontrolleres entydigheden af versionen for de givne begrænsninger (for eksempel periode, websted eller antal). Du modtager en fejlmeddelelse, hvis den version, du forsøger at aktivere, er i konflikt med en version, der allerede er aktiv. Du skal derefter enten deaktivere versionen, der er i konflikt, eller redigere versionsbegrænsningerne (som regel perioden) for at forhindre en tvetydig aktivering.

### <a name="product-change-with-case-management"></a>Produktændring med sagsstyring

Produktændringssagen til godkendelse og aktivering af nye eller ændrede styklister og styklisteversioner er en nem måde at få vist en oversigt over styklisteversionens begrænsninger på. Du kan også godkende og aktivere alle styklister og formler, der er relateret til en bestemt ændring for én aktiveringsdato.

### <a name="alternative-bom-versions"></a>Alternativ styklisteversioner

Nogle gange bør den aktive styklisteversion eller formelversion ikke bruges i prognoser, salg eller et overordnet produkt. I så fald kan du vælge en bestemt godkendt stykliste som en del af behovet (budgetlinje, salgslinje eller styklistelinje), hvis der findes en styklisteversion eller formelversion for den alternative stykliste eller formel.  

Når der oprettes ordreforslag, produktionsordrer eller kanbans, kan planlæggeren eller den tilsynsførende for produktion bruge enhver godkendt styklisteversion, der er gældende på den planlagte produktionsdato, for at planlægge for eller fremstille et bestemt produkt. Den styklisteversion, der bruges, behøver ikke at være aktiveret som standardstyklisteversionen.

## <a name="bom-and-formula-lines"></a>Stykliste- og formellinjer
Der oprettes en styklistelinje for hvert materiale, service eller stof. Linjen definerer det planlagte forbrug af den angivne produktvariant og definerer også de forskellige attributter, der er relateret til det planlagte forbrug.  

Styklistelinjer kan have følgende linjetyper: **Vare**, **Fantom**, **Sporet forsyning**, **Leverandør**.

### <a name="item"></a>Vare

Vælg **varens** linjetype for materialer eller tjenester, der forbruges direkte, og som ikke kræver yderligere nedbrydning eller sporet forsyning.

### <a name="phantom"></a>Fantom

Vælg linjetypen **Fantom**, når du vil udfolde alle de lavere styklistevareniveauer, der er indeholdt på styklistelinjen. I behovsplanlægningen, i beregning af planlagte omkostninger eller under forkalkulation for en produktionsordre, der bruger styklistelinjer af typen **Fantom** er den overordnede styklistelinje, som henviser til en produktvariant, der har en fantomstykliste, erstattet af de komponentvarer, der er anført som styklistelinjer i den pågældende stykliste, som fastsat af den relevante aktive styklisteversion for produktvarianten. Hvis produktvarianten har en relevant aktiv rute, flettes operationer af denne rute med den overordnede rute.  

Bemærk, at fantomstyklister typisk bruges til at forenkle den tekniske proces. Omfattende brug af fantomstyklister på mange niveauer har indflydelse på ydeevnen, især i meget gentagne produktionsscenarier. For at forbedre ydeevnen skal du undgå dybe hierarkier af fantomstyklister. I stedet skal du bruge produktionsstyklister, der allerede er udfoldet, og ruter.

### <a name="pegged-supply"></a>Sporet forsyning

Vælg linjetypen **Sporet forsyning**, når du vil oprette en underproduktion, en hændelseskanban for en styklistelinje eller en direkte købsordre for en produktvariant, som styklistelinje henviser til. Den underproduktion, hændelseskanban eller indkøbsordre, der oprettes, når du forkalkulerer produktionsordren. De påkrævede vareantal reserveres automatisk til den forbrugende produktionsordre.

### <a name="vendor"></a>Kreditor

Vælg linjetypen **Leverandør**, hvis der i produktionsprocessen gøres brug af en underleverandør, og du ønsker, at en underproduktion eller en indkøbsordre skal oprettes automatisk for underleverandøren.  

**Note til underleverandøroperationer i en stykliste:** Tjeneste eller Arbejde, der udføres af underleverandøren, skal være oprettet som en servicevare, der er registreret på lageret. Du skal knytte servicevaren til den overordnede vare som en styklistelinje. Ruten skal indeholde en operation, der er tildelt underleverandørens operationsressource.




