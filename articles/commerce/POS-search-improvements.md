---
title: Produkt- og kundesøgning i POS
description: Dette emne indeholder en oversigt over de forbedringer, der er foretaget i produkt- og kundesøgefunktionen i Dynamics 365 Commerce.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 10c843670a280c86790185c8a39cb2943e2838f9
ms.sourcegitcommit: 5472005274f2f94fba82dda90de128f39d8b8390
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759929"
---
# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Produkt- og kundesøgning i POS

[!include [banner](includes/banner.md)]

Modern Point of Sale (MPOS) og Cloud Point of Sale (CPOS) indeholder brugervenlige søgefunktioner for produkter og debitorer. Eftersom søgelinjen altid vises øverst i MPOS- og CPOS-vinduerne, kan medarbejderne hurtigt søge efter produkter og debitorer.

Medarbejdere kan søge efter produkter i de udvalg og kataloger, der er tilknyttet det aktuelle lager. De kan også søge i udvalg og kataloger, der er tilknyttet ethvert andet lager i virksomheden. Derfor kan kasserere sælge og returnere produkter, der ikke er i butikkens sortiment. På samme måde kan medarbejdere søge efter debitorer, der er tilknyttet den aktuelle butik eller enhver anden butik i virksomheden. Medarbejdere kan desuden søge efter kunder, der er tilknyttet en anden virksomhed i den overordnede organisation.

## <a name="product-search"></a>Produktsøgning

Som standard udføres produktsøgninger i butikkens udvalg. Denne type søgning kaldes en *søgning efter lokalt produkt*. Men medarbejdere kan nemt skifte til ethvert katalog, der er tilknyttet den aktuelle butik, eller de kan søge i en anden butik. Denne type søgning kaldes en *ekstern produktsøgning*. Hvis du vil ændre kataloget, skal du vælge knappen **Kategorier** til venstre på siden. Øverst i ruden, der vises, skal du vælge knappen **Skift katalog** og derefter vælge et af de tilgængelige kataloger for at gennemse det. Systemet søger i det valgte katalog efter produkter.

På siden **Skift katalog** kan medarbejdere nemt vælge alle butikker, eller de kan søge efter produkter på tværs af alle butikker.

![Ændring af kataloget](./media/Changecatalog.png "Ændring af kataloget")

En lokal produktsøgning søger i følgende produktegenskaber:

- Produktnummer
- Produktnavn
- Beskrivelse
- Dimensioner
- Stregkode
- Søgenavn

### <a name="enhancements-to-local-product-searches"></a>Forbedringer af lokale produktsøgninger

Oplevelsen af lokale produktsøgninger er nu blevet mere brugervenlig. Der er blevet foretaget følgende forbedringen:

- Rullemenuer for produkt og kunde er føjet til søgelinjen, så medarbejderne kan vælge enten **Produkt** eller **Kunde**, før de søger. Som standard er **Produkt** markeret, som vist i nedenstående illustration.
- Til søgninger med flere nøgleord (dvs. til søgninger, der bruger søgeord), kan detailforretninger konfigurere, om søgeresultaterne skal omfatte resultater, der opfylder *ethvert* søgeord, eller kun de resultater, der opfylder *alle* søgeord. Indstillingen for denne funktion findes i POS-funktionalitetsprofilen i en ny gruppe med navnet **Produktsøgning**. Standardindstillingen er **Match et hvilket som helst søgeord**. Denne indstilling er også den anbefalede indstilling. Når indstillingen **Match et hvilket som helst søgeord** bruges, returneres alle produkter, der svarer helt eller delvist til et eller flere søgeord. Resultaterne sorteres automatisk i stigende rækkefølge, så de produkter, der har fleste forekomster af nøgleord (fuld eller delvis), placeres først.

    Indstillingen **Match alle søgeord** returnerer kun produkter, der matcher alle søgeordene (helt eller delvist). Denne indstilling er nyttig, når produktnavnene er lange, og medarbejdere kun vil se begrænsede produkter i søgeresultaterne. Denne type søgning har dog to begrænsninger:

    - Søgningen foretages på de enkelte produktegenskaber. F.eks. returneres kun produkter, der har alle de søgte nøgleord i mindst én produktegenskab.
    - Der søges ikke i dimensioner.

- Detailhandlere kan nu konfigurere produktsøgning til at vise søgeforslag, mens brugerne skriver produktnavne. En ny indstilling for denne funktion findes i POS-funktionalitetsprofilen i en ny gruppe med navnet **Produktsøgning**. Indstillingen hedder **Vis søgeforslag, mens du skriver**. Denne funktion kan hjælpe medarbejderne med hurtigt at finde det produkt, de søger efter, da de ikke behøver at skrive hele navnet manuelt.
- Produktsøgningsalgoritmen søger nu også efter de søgte udtryk i egenskaben **Søgenavn** for produktet.

![Produktforslag](./media/Productsuggestions.png "Produktforslag")

## <a name="customer-search"></a>Kundesøgning

Kundesøgning bruges til at finde kunder til forskellige formål. F.eks. ønsker kasserere eventuelt at få vist en kundes ønskeliste eller købshistorik eller at føje kunden til en transaktion. Søgealgoritmen matcher søgeordene i forhold til de værdier, der findes i følgende kundeegenskaber:

- Navn
- E-mailadresse
- Telefonnummer
- Fordelskundekortnummer
- Adressering
- Kontonummer

Af disse egenskaber giver navnet den største fleksibilitet ved søgninger med flere nøgleord, da algoritmen returnerer alle de kunder, der svarer til et hvilket som helst af de nøgleord, der søges efter. De kunder, der matcher de fleste nøgleord vises øverst i resultaterne. Denne funktionsmåde hjælper kasserere i situationer, hvor de søger ved at skrive det fulde navn, men hvor efternavn og fornavn blev byttet om under den oprindelige indtastning af værdier. Af hensyn til resultaterne bevarer alle andre egenskaber dog rækkefølgen af søgenøgleord. Hvis rækkefølgen af søgenøgleord derfor ikke stemmer overens med den rækkefølge, som dataene er gemt i, vil der ikke blive returneret nogen resultater.

Som standard udføres en kundesøgning på de kundeadressekartoteker, der er knyttet til butikken. Denne type søgning kaldes en *søgning efter lokal kunde*. Men medarbejdere kan også søge efter kunder globalt. De kan med andre ord søge på tværs af virksomhedens butikker og andre juridiske enheder. Denne type søgning kaldes en *ekstern kundesøgning*.

For at søge globalt kan medarbejderne vælge knappen **Filtrer resultater** i bunden af siden og derefter vælge indstillingen **Søg i alle butikker**, som vist i følgende illustration. I dette tilfælde returneres ikke kun kunder. Alle former for parter, der er en del af enhvert adressekartotek i hovedkontoret, returneres også. Disse parter omfatte medarbejdere, leverandører, kontaktpersoner og konkurrenter.

> [!NOTE]
> Der skal angives mindst fire tegn for at en ekstern kundesøgning returnerer resultater.

I en ekstern kundesøgning vises kunde-id ikke for debitorer fra de andre juridiske enheder, da der ikke er oprettet noget kunde-id for disse parter i det aktuelle regnskab. Men hvis en medarbejder åbner siden med oplysninger for kunden, opretter systemet automatisk et kunde-id for parten og knytter også butikkens kundeadressekartoteker til kunden. Kunden vil derfor være synlig i lokale butikssøgninger, der udføres senere.

![Global kundesøgning](./media/Globalcustomersearch.png "Global kundesøgning")

### <a name="enhancements-to-local-customer-search"></a>Forbedringer af søgning efter lokale debitorer

Søgninger, der er baseret på telefonnummeret, er blevet mere enkle. Disse søgninger ignorerer nu specialtegn som f.eks. mellemrum, bindestreger og parenteser, der kan være blevet tilføjet, da debitoren blev oprettet. Derfor behøver kasserere ikke spekulere på telefonnummerets format, når de søger. Hvis en kundes telefonnummer f.eks. blev angivet som **123-456-7890**, kan en kasserer søge efter debitoren ved at skrive **1234567890** eller ved at angive de første par tal af telefonnummeret.

> [!NOTE]
> En kunde kan have flere telefonnumre og flere mails. Algoritmen til kundesøgning søger også i disse sekundære mails og telefonnumre, men på resultatsiden for kundesøgning vises kun den primære mail og det primære telefonnummer. Dette kan medføre en vis forvirring, fordi de returnerede kunderesultater ikke vil vise den søgte mail eller det søgte telefonnummer. I en fremtidig frigivelse har vi planlagt at forbedre skærmbilledet med kundesøgeresultater for at vise disse oplysninger.

Den traditionelle kundesøgning kan være tidskrævende, da den søger på tværs af flere felter. I stedet kan kasserere nu søge i en enkelt kundeegenskab, f.eks. navn, mailadresse eller telefonnummer. De egenskaber, som kundesøgningsalgoritmen bruger, kaldes samlet *kundesøgningskriteriet*. Systemadministratoren kan nemt konfigurere et eller flere kriterier som genveje, der skal vises i POS. Da søgningen er begrænset til et enkelt kriterium, vises kun de relevante søgeresultater, og ydeevnen er meget bedre end ydeevnen ved en standardkundesøgning. I følgende illustration vises kundesøgningsgenvejene i POS.

![Genveje til kundesøgning](./media/SearchShortcutsPOS.png "Genveje til kundesøgning")

For at angive søgekriterier som genveje skal administratoren åbne siden **Commerce-parametre** i Commerce og derefter under fanen **POS-søgekriterier** vælge alle de kriterier, der skal vises som genveje.

![Konfigurere søgegenveje](./media/ConfigureShortcutsAX.png "Konfigurere søgegenveje")

> [!NOTE]
> Hvis du tilføjer for mange genveje, vil rullemenuen på søgelinjen på POS blive overfyldt, og medarbejderens søgeoplevelse kan blive påvirket. Det anbefales, at du kun tilføje så mange genveje, som du har brug for.

Feltet **Visningsrækkefølge** bestemmer den rækkefølge, hvori genveje vises i POS. Det kriterie, der vises, er de standardegenskaber, som kundesøgningsalgoritmen bruger til at søge efter kunder. Partnere kan dog tilføje brugerdefinerede egenskaber som søgningsgenveje. For at tilføje brugerdefinerede egenskaber som søgningsgenveje skal systemadministratoren udvide den udvidelige fasttekst, der bruges som kundesøgningskriterie, og derefter markere partnerens brugerdefinerede egenskaber som genveje. Partnere har ansvaret for at skrive kode til at søge efter resultater, når deres brugerdefinerede genveje bruges til søgning.

> [!NOTE]
> En brugerdefineret egenskab, der er føjet til fastteksten, påvirker ikke standardalgoritmen til kundesøgning. Med andre ord søger kundesøgningsalgoritmen ikke i den brugerdefinerede egenskab. Brugere kan kun bruge en brugerdefineret egenskab til søgninger, hvis den brugerdefinerede egenskab tilføjes som en genvej, eller hvis standardalgoritmen til søgning tilsidesættes.

I en kommende udgave af Commerce vil detailhandlere kunne angive standardtilstanden for kundesøgning i POS til **Søg i alle butikker**. Denne konfiguration kan være nyttig i situationer, hvor kunder, der er oprettet uden for POS, skal søges efter med det samme (f.eks. selv før distributionsjobbet køres). En ny indstilling **Standardindstilling for kundesøgning** vil være tilgængelig i POS-funktionalitetsprofilen. Angiv den til **Til** for at indstille standardsøgetilstanden til **Søg i alle butikker**. Alle forsøg på kundesøgninger vil derefter foretage et realtidsopkald til hovedkontoret.

Denne konfiguration er skjult bag et flighting-flag, der kaldes **CUSTOMERSEARCH_ENABLE_DEFAULTSEARCH_FLIGHTING** for at hjælpe med at forhindre uventede problemer med ydeevnen. For at få vist indstillingen **Standardtilstand for kundesøgning** i brugergrænsefladen, skal detailhandleren oprette en supportbillet for dennes brugeraccepttest (UAT) og produktionsmiljøer. Når billetten er modtaget, arbejder den tekniske gruppe sammen med detailhandleren for at sikre, at detailhandleren tester i miljøer, der ikke er et produktionsmiljø, for at vurdere ydeevnen og implementere eventuelle nødvendige optimeringer.

