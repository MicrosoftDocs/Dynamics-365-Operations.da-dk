---
title: Produkt- og kundesøgning i POS
description: Dette emne indeholder en oversigt over de forbedringer, der er foretaget i produkt- og kundesøgefunktionen i Dynamics 365 Commerce.
author: ShalabhjainMSFT
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 043a630408d6b03e528f0afd5443de73ad5f3802c968b9d9bd7a5c51bfe1fb03
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716387"
---
# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Produkt- og kundesøgning i POS

[!include [banner](includes/banner.md)]

Modern Point of Sale (MPOS) og Cloud Point of Sale (CPOS) indeholder brugervenlige søgefunktioner for produkter og debitorer. Eftersom søgelinjen altid vises øverst i MPOS- og CPOS-vinduerne, kan medarbejderne hurtigt søge efter produkter og debitorer.

Medarbejdere kan søge efter produkter i de udvalg og kataloger, der er tilknyttet det aktuelle lager. De kan også søge i udvalg og kataloger, der er tilknyttet ethvert andet lager i virksomheden. Derfor kan kasserere sælge og returnere produkter, der ikke er i butikkens sortiment. På samme måde kan medarbejdere søge efter debitorer, der er tilknyttet den aktuelle butik eller enhver anden butik i virksomheden. Medarbejdere kan desuden søge efter kunder, der er tilknyttet en anden virksomhed i den overordnede organisation.

## <a name="product-search"></a>Produktsøgning

Som standard udføres produktsøgninger i butikkens udvalg. Denne type søgning kaldes en *søgning efter lokalt produkt*. Men medarbejdere kan nemt skifte til ethvert katalog, der er tilknyttet den aktuelle butik, eller de kan søge i en anden butik. Denne type søgning kaldes en *ekstern produktsøgning*. Hvis du vil ændre kataloget, skal du vælge knappen **Kategorier** til venstre på siden. Øverst i ruden, der vises, skal du vælge knappen **Skift katalog** og derefter vælge et af de tilgængelige kataloger for at gennemse det. Systemet søger i det valgte katalog efter produkter.

På siden **Skift katalog** kan medarbejdere nemt vælge alle butikker, eller de kan søge efter produkter på tværs af alle butikker.

![Ændring af kataloget.](./media/Changecatalog.png "Ændring af kataloget")

En lokal produktsøgning søger i følgende produktegenskaber:

- Produktnummer
- Produktnavn
- Betegnelse
- Dimensioner
- Stregkode
- Søg efter navn

### <a name="additional-local-product-search-capabilities"></a>Yderligere egenskaber for lokal produktsøgning

- Til søgninger med flere nøgleord (dvs. til søgninger, der bruger søgeord), kan detailforretninger konfigurere, om søgeresultaterne skal omfatte resultater, der opfylder *ethvert* søgeord, eller kun de resultater, der opfylder *alle* søgeord. Indstillingen for denne funktion findes i POS-funktionalitetsprofilen i en ny gruppe med navnet **Produktsøgning**. Standardindstillingen er **Match et hvilket som helst søgeord**. Denne indstilling er også den anbefalede indstilling. Når indstillingen **Match et hvilket som helst søgeord** bruges, returneres alle produkter, der svarer helt eller delvist til et eller flere søgeord. Resultaterne sorteres automatisk i stigende rækkefølge, så de produkter, der har fleste forekomster af nøgleord (fuld eller delvis), placeres først.

    Indstillingen **Match alle søgeord** returnerer kun produkter, der matcher alle søgeordene (helt eller delvist). Denne indstilling er nyttig, når produktnavnene er lange, og medarbejdere kun vil se begrænsede produkter i søgeresultaterne. Denne type søgning har dog to begrænsninger:

    - Søgningen foretages på de enkelte produktegenskaber. F.eks. returneres kun produkter, der har alle de søgte nøgleord i mindst én produktegenskab.
    - Der søges ikke i dimensioner.

- Detailhandlere kan konfigurere produktsøgning til at vise søgeforslag, mens brugerne skriver produktnavne. En ny indstilling for denne funktion findes i POS-funktionalitetsprofilen i en ny gruppe med navnet **Produktsøgning**. Indstillingen hedder **Vis søgeforslag, mens du skriver**. Denne funktion kan hjælpe medarbejderne med hurtigt at finde det produkt, de søger efter, da de ikke behøver at skrive hele navnet manuelt.
- Produktsøgningsalgoritmen søger nu også efter de søgte udtryk i egenskaben **Søgenavn** for produktet.

![Produktforslag.](./media/Productsuggestions.png "Produktforslag")

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

Kunde-id vises ikke for debitorer fra de andre juridiske enheder, da der ikke er oprettet noget kunde-id for disse parter i det aktuelle regnskab. Men hvis en medarbejder åbner siden med oplysninger for kunden, opretter systemet automatisk et kunde-id for parten og knytter også butikkens kundeadressekartoteker til kunden. Kunden vil derfor være synlig i lokale butikssøgninger, der udføres senere.

![Global kundesøgning.](./media/Globalcustomersearch.png "Global kundesøgning")

### <a name="additional-local-customer-search-capabilities"></a>Yderligere egenskaber for lokal kundesøgning

Når en bruger søger efter et telefonnr., ignorerer systemet specialtegn (f.eks. mellemrum, bindestreger og parenteser) der kan være blevet tilføjet, da debitoren blev oprettet. Derfor behøver kasserere ikke spekulere på telefonnummerets format, når de søger. Hvis en kundes telefonnummer f.eks. blev angivet som **123-456-7890**, kan en kasserer søge efter debitoren ved at skrive **1234567890** eller ved at angive de første par tal af telefonnummeret.

> [!NOTE]
> En kunde kan have flere telefonnumre og flere mails. Algoritmen til kundesøgning søger også i disse sekundære mails og telefonnumre, men på resultatsiden for kundesøgning vises kun den primære mail og det primære telefonnummer. Dette kan medføre en vis forvirring, fordi de returnerede kunderesultater ikke vil vise den søgte mail eller det søgte telefonnummer. I en fremtidig frigivelse har vi planlagt at forbedre skærmbilledet med kundesøgeresultater for at vise disse oplysninger.

Den traditionelle kundesøgning kan være tidskrævende, da den søger på tværs af flere felter. I stedet kan kasserere søge i en enkelt kundeegenskab, f.eks. navn, mailadresse eller telefonnummer. De egenskaber, som kundesøgningsalgoritmen bruger, kaldes samlet *kundesøgningskriteriet*. Systemadministratoren kan nemt konfigurere et eller flere kriterier som genveje, der skal vises i POS. Da søgningen er begrænset til et enkelt kriterium, vises kun de relevante søgeresultater, og ydeevnen er meget bedre end ydeevnen ved en standardkundesøgning. I følgende illustration vises kundesøgningsgenvejene i POS.

![Genveje til kundesøgning.](./media/SearchShortcutsPOS.png "Genveje til kundesøgning")

For at angive søgekriterier som genveje skal administratoren åbne siden **Commerce-parametre** i Commerce og derefter under fanen **POS-søgekriterier** vælge alle de kriterier, der skal vises som genveje.

![Konfigurere søgegenveje.](./media/ConfigureShortcutsAX.png "Konfigurere søgegenveje")

> [!NOTE]
> Hvis du tilføjer for mange genveje, vil rullemenuen på søgelinjen på POS blive overfyldt, og medarbejderens søgeoplevelse kan blive påvirket. Det anbefales, at du kun tilføje så mange genveje, som du har brug for.

Feltet **Visningsrækkefølge** bestemmer den rækkefølge, hvori genveje vises i POS. Det kriterie, der vises, er de standardegenskaber, som kundesøgningsalgoritmen bruger til at søge efter kunder. Partnere kan dog tilføje brugerdefinerede egenskaber som søgningsgenveje. For at tilføje brugerdefinerede egenskaber som søgningsgenveje skal systemadministratoren udvide den udvidelige fasttekst, der bruges som kundesøgningskriterie, og derefter markere partnerens brugerdefinerede egenskaber som genveje. Partnere har ansvaret for at skrive kode til at søge efter resultater, når deres brugerdefinerede genveje bruges til søgning.

> [!NOTE]
> En brugerdefineret egenskab, der er føjet til fastteksten, påvirker ikke standardalgoritmen til kundesøgning. Med andre ord søger kundesøgningsalgoritmen ikke i den brugerdefinerede egenskab. Brugere kan kun bruge en brugerdefineret egenskab til søgninger, hvis den brugerdefinerede egenskab tilføjes som en genvej, eller hvis standardalgoritmen til søgning tilsidesættes.

Detailhandlende kan også angive standardtilstanden for kundesøgning i POS til **Søgning i alle butikker**. Denne konfiguration kan være nyttig i situationer, hvor kunder, der er oprettet uden for POS, skal søges efter med det samme (f.eks. selv før distributionsjobbet køres). Dette gøres ved, at forhandleren aktiverer indstillingen **Standardsøgningstilstand for kunder** i POS-funktionsprofilen. Når den er indstillet til **Ja**, vil alle forsøg på kundesøgninger foretage et realtidsopkald til hovedkontoret.

Denne konfiguration er skjult bag et flighting-flag, der kaldes **CUSTOMERSEARCH_ENABLE_DEFAULTSEARCH_FLIGHTING** for at hjælpe med at forhindre uventede problemer med ydeevnen. For at få vist indstillingen **Standardtilstand for kundesøgning** i brugergrænsefladen, skal detailhandleren oprette en supportbillet for dennes brugeraccepttest (UAT) og produktionsmiljøer. Når billetten er modtaget, arbejder den tekniske gruppe sammen med detailhandleren for at sikre, at detailhandleren tester i miljøer, der ikke er et produktionsmiljø, for at vurdere ydeevnen og implementere eventuelle nødvendige optimeringer.

## <a name="cloud-powered-customer-search"></a>Oversigt over skybaseret kundesøgning

Offentlig forhåndsvisning af kundesøgningsfunktionaliteten ved hjælp af Azure Cognitive Search-tjenesten som en del af Commerce 10.0.18-versionen. Ud over forbedringer af ydeevne, har brugerne af tjenesten også stor fordel af udvidede forbedringer og forbedrede relevansegenskaber. Forbedringerne af ydeevnen er særligt synlige, når den globale søgefunktion ("Søg i alle butikker") bruges på POS-funktionen. Det skyldes, at der hentes søgeresultater fra Azure-søgeindekset i stedet for forespørgsler fra dataene i Commerce Headquarters. 

### <a name="enable-the-cloud-powered-search-feature"></a>Aktivere den skybaserede søgefunktion

> [!NOTE]
> Det er påkrævet, at både Commerce Headquarters og Commerce Scale Unit opdateres til version 10.0.18. Det er ikke nødvendigt at opdatere POS.

Hvis du vil aktivere skybaseret søgefunktion i Commerce Headquarters, skal du udføre disse trin.

1. Gå til **Systemadministration \> Arbejdsområder \> Funktionsstyring**.
1. Find og vælg funktionen **(Forhåndsvisning) Skybaseret kundesøgning** og derefter vælge **Aktivér nu**.
1. Gå til **Retail og Commerce > Headquarters-opsætning > Commerce planlægger > Initialiser Commerce-planlægger**, og vælg **OK** for at få vist det nye **1010_CustomerSearch**-job i formularen **Distributionsplan**.
1. Gå til **Retail og Commerce > Retail og Commerce-it > Distributionsplan**.
1. Kør **1010_CustomerSearch**-jobbet. Dette job udgiver datoen til Azure-søgeindekset. Når udgivelse af indekset er fuldført, angives jobbets status til **Anvendt**.
1. Når jobstatus **1010_CustomerSearch** er angivet til **Anvendt**, skal du køre jobbet **1110 - Global konfiguration** for at opdatere POS-kanalerne for den funktion, der netop er aktiveret i **Funktionsstyring**.
1. Efterfølgende skal du køre **1010_CustomerSearch** med jævne mellemrum for at sende kundeopdateringer til søgeindekset.

> [!NOTE]
> I forbindelse med det første indeksudgiven kan det tage **1010_CustomerSearch** et par timer at fuldføre et job, da det vil sende alle kundeposterne til Azure-søgeindekset. Efterfølgende opdateringer bør tage et par minutter. Inden for den tidsperiode, hvor den skybaserede søgefunktion er aktiveret, men indeksudgivelse endnu ikke er fuldført, vil kundesøgningen fra POS som standard blive baseret på den eksisterende SQL-baseret søgning. Det sikrer, at der ikke er nogen arbejdsgange, der kan bruges i butiksoperationer.

### <a name="functional-differences-from-the-existing-search"></a>Funktionelle forskelle fra den eksisterende søgning

Nedenstående liste viser, hvordan funktionaliteten til kundesøgning i skyen er forskellig fra den eksisterende søgefunktionalitet. 

- Kunder, der oprettes og redigeres i Commerce headquarters, sendes til Azure-søgeindekset, når **1010_CustomerSearch**-jobbet køres. Det tager minimum 15-20 minutter at opdatere indekset med disse opdateringer. POS-brugere vil kunne søge efter nye kunder (eller søge ud fra opdaterede oplysninger) om 15 til 20 minutter, efter at opdateringerne forekommer i Commerce Headquarters. Hvis forretningsprocessen kræver, at kunder, der oprettes i Commerce Headquarters, straks kan søges i POS, er dette muligvis ikke den rigtige service til dig.
- Nye kunder, der oprettes i POS, sendes til Azure-søgeindekset fra Commerce Scale Unit og kan med det samme søges i alle butikker. Men hvis funktionen til oprettelse af Async-kunder er aktiveret, vil nye kundeposter ikke blive udgivet til Azure-søgeindekset fra Commerce Scale Unit og kan ikke søges i POS, før kundeoplysningerne synkroniseres med Commerce Headquarters og debitor-iD'er genereres for Async-kunder. Jobbet **1010_CustomerSearch** vil derefter kunne sende Async-kundeposterne til Azure-søgeindekset. I gennemsnit vil der være ca. 30 minutter, før der kan søges i nyoprettede Async-kunder på POS. Dette estimat antager, at job i **1010_CustomerSearch**, **P-job** og **Synkroniser kunder og forretningspartnere fra job i Async-tilstand** er planlagt til at køre hvert 15. minut.
- I skybaseret søgning søges der også efter sekundære mails og telefonnumre til kunder, men søgeresultaterne for kunder viser i øjeblikket kun kundernes primære telefonnummer og primære mailadresse. Det kan umiddelbart se ud, som om irrelevante søgeresultater er returneret, men hvis du kontrollerer en kundes sekundære mail og telefonnummer i søgeresultaterne, kan det hjælpe med at kontrollere, om det søgte nøgleord resulterede i kundematch. For at undgå en sådan forvirring er der planer om at forbedre siden med søgeresultater for at gøre det let for brugerne at forstå, hvorfor et søgeresultat blev returneret.
- Kravet om at søge med mindst fire tegn i en global søgning ("Søg i alle butikker") er ikke relevant for denne tjeneste.

> [!NOTE]
> Kundesøgningsfunktionaliteten ved hjælp af azure Azure Azure-søgetjenesten er tilgængelig i begrænsede områder som forhåndsvisning. Debitorsøgningsfunktionaliteten er *ikke* tilgængelig i følgende områder:
> - Brasilien
> - Indien
> - Canada
> - Storbritannien

[!INCLUDE[footer-include](../includes/footer-banner.md)]
