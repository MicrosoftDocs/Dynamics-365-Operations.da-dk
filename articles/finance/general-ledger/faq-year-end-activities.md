---
title: Ofte spurgte spørgsmål om aktiviteter ved årsafslutningen
description: Denne artikel indeholder en oversigt over de spørgsmål, der kan opstå ved årsafslutningen, og de svar, der kan være en hjælp ved lukning af årets aktiviteter.
author: moaamer
ms.date: 12/01/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2e33c1dcbfa4da74f2e8acc6e29f04fda3abd185
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853034"
---
# <a name="year-end-activities-faq"></a>Ofte spurgte spørgsmål om aktiviteter ved årsafslutningen 

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over de spørgsmål, der kan opstå ved årsafslutningen, og de svar, der kan være en hjælp ved lukning af årets aktiviteter. Oplysningerne i denne artikel fokuserer primært på spørgsmål, der vedrører ultimoaktiviteter ved årsopgørelsen for Finans og Kreditor.

## <a name="general-ledger-year-end-enhancements"></a>Forbedringer af årsopgørelsen for Finans

Microsoft Dynamics 365 Finance version 10.0.20 introducerede en lukning af årsslutpunktet. Denne forbedring er som standard aktiveret i version 10.0.25 og er obligatorisk i version 10.0.29. Hvis organisationen bruger en version, der er ældre end 10.0.25, anbefales det, at du aktiverer denne funktion, før årsafslutningsprocessen startes. Før du kan bruge denne funktion, skal den være aktiveret i dit system. Administratorer kan bruge arbejdsområdet **Funktionsstyring** til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

- **Modul:** Finans
- **Funktionsnavn:** Forbedringer af årsopgørelsen for Finans

Opsætningen af skabeloner til årsafslutningen er flyttet til en ny opsætningsside, **Skabelon til opsætning af årsafslutning**. Den eksisterende årsafslutningsside bliver som siden **værdireguleringer af udenlandsk valuta i Finans**, hvor der vises en liste, hver gang lukningen af årsafslutningen køres eller tilbageføres. På siden vises ikke historiske oplysninger om lukninger ved årsafslutning, der blev udført, før funktionen blev aktiveret. En regnskabschef kan starte årsafslutningen fra den nye side.

Hvis du vil tilbageføre årsafslutningen, skal du vælge det seneste regnskabsår for den relevante juridiske enhed og vælge **Tilbageføre årsafslutning**. Tilbageførslen sletter regnskabsposterne for den forrige årsafslutning og vil ikke køre årsafslutningen igen. Hvis du aktiverer funktionen til **forbedringer af årsslutninger for finansmodulet**, når du har fuldført en årsslutning, og du vil tilbageføre de historiske årsslutresultater, skal du køre den historiske årsslutlukning igen, når du aktiverer finansparameteren **Slet eksisterende årsafslutningsposter ved fornyet lukning af året**.

Du kan køre årsslutningen igen ved at genstarte processen for regnskabsåret og den juridiske enhed. Processen vil fortsætte med at bruge finansparameterindstillingen til at bestemme, om årsafslutningen kun skal fornyes til nye eller ændrede posteringer, eller om processen til fornyelse skal køres for alle transaktioner og helt tilbageføre den forrige lukning.

## <a name="general-ledger-the-general-ledger-year-end-enhancements-feature-is-enabled-why-cant-i-view-my-previous-year-closings-in-the-history-section-of-the-year-end-close-page"></a>Finans: Funktionen til forbedringer af årsopgørelsen under Finans er aktiveret. Hvorfor kan jeg ikke få vist mine forrige års lukninger i afsnittet Historik på siden for årslukning?

Før funktionen **Forbedringer af årsopgørelsen for Finans** aktiveres, registreres den dato og det klokkeslæt, den seneste årsslutningsproces blev kørt. Den sporede ikke historikken, hver gang årsslutslutning blev udført. Detaljerne for hver års afslutningskørsel kan derfor ikke vises. Når funktionen er aktiveret, vedligeholdes de efterfølgende oplysninger om lukkeprocessen for årsslutningen. Bilag fra alle processer ved årsafslutning, også dem, der køres før funktionsaktivering, kan ses på siden **Bilagsposteringer** . 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-cant-be-run-because-one-or-more-ledger-transactions-posted-into-the-fiscal-year-that-you-are-closing-were-settled-to-a-ledger-transaction-in-a-different-fiscal-year-what-does-this-error-mean"></a>Finans: Årsafslutningsprocessen mislykkes pga. følgende fejl: "Årsafslutningslukningen kan ikke køres, fordi en eller flere finansposteringer, der er bogført i det regnskabsår, du lukker, er udlignet med en finanspostering i et andet regnskabsår." Hvad betyder denne fejl?

Da funktionen **Opmærksomhed mellem finansudligning og årsafslutning** er aktiveret er det kun udlignede finanstransaktioner fra det regnskabsår, der afsluttes, som udelukkes fra startsaldoen. Denne adfærd medfører, at debet- og kreditbeløb har saldoafvigelse. Yderligere oplysningerne finde i [Opmærksomhed mellem finansudligning og årsafslutning](awareness-between-ledger-settlement-year-end-close.md).

## <a name="general-ledger-reversal-of-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-for-112022-cant-be-reversed-because-beginning-balance-transaction-have-been-ledger-settled-in-fiscal-year-112023-what-does-this-error-mean"></a>Finans: Tilbageførslen af årsslutning mislykkes pga. følgende fejl: "Årsafslutningen for 1/1/2022 kan ikke tilbageføres, da primosaldotransaktionen er udlignet i regnskabsåret 1/1/2023." Hvad betyder denne fejl?

Da funktionen **Opmærksomhed mellem finansudligning og årsafslutning** er aktiveret, er tilbageførsel af årsafslutningen ikke tilladt, hvis primoposteringerne er udlignet i det nye regnskabsår. Tilbageføre finansudligningen i det nye 2023-regnskabsår, før du tilbagefører årsafslutningen for 1. januar 2022. Alternativt kan året for 1. januar 2022, genlukkes, men kun for nye reguleringsposter. Hvis du kun vil lukke året igen, når der skal foretages reguleringer, skal du deaktivere **Slet eksisterende ultimoposter ved fornyet lukning af året**-finansparameteren.

## <a name="general-ledger-why-isnt-the-ledger-settlement-automation-processing-decembers-ledger-settlement-transactions"></a>Finans: Hvorfor automatiserer finansudligningerne ikke decembers finansudligning?

Funktionen **Automatiser finansudligninger** kører automatiseringen for posteringer, der er dateret fra den første dag i regnskabsåret til den aktuelle dato, hvor forekomsten kører. I forbindelse med regnskabsår, der slutter den 31. december, skal du muligvis justere udførelsesdatoen for forekomsten for at sikre, at den køres i december. Automatisering er f.eks. konfigureret til at køre den første dag i hver måned. Denne automatisering køres 1. december 2022 og skal køres 1. januar 2023. Det anbefales, at du ændrer forekomsten for 1. januar 2023, så den kører i stedet den 31. december 2022. Denne ændring sikrer, at der tages hensyn til automatisk udligning af posteringer, der er dateret 2. december til 31. december.

## <a name="general-ledger-whats-the-difference-between-the-reverse-year-end-close-action-and-the-delete-existing-year-end-entries-when-reclosing-parameter-for-year-end-close"></a>Finans: Hvad er forskellen mellem handlingen Tilbageføre årsafslutning og sletning af eksisterende årsafslutningsposteringer, når parameteren for lukning af årsafslutning gentages?

Der kan være forvirring om forskellen mellem handlingen **Tilbagefør årsafslutning** og parameteren **Slet eksisterende årsafslutningsposteringer** i Finans (**Finans \> Opsætning Finans \> Finansparametre**).

Vælg handlingen **Tilbagefør årsafslutning**, når du kører årsafslutningen for at slette alle ultimosaldo- og startsaldoposter, som om årsafslutningen aldrig var blevet kørt. I disse tilfælde slettes bilagene. Årsafslutningen køres ikke automatisk igen. Hvis du vil køre årsafslutning, skal du vælge handlingen **Kør årsslutning** .

Parameteren **Slet eksisterende ultimoposter ved fornyet lukning af året** i Finans anvendes kun, når du kærer (ikke tilbagefører) årsafslutningen. Hvis den parameter er angivet til **Ja**, slettes alle ultimosaldoposter og startsaldoposter, og årsafslutningen køres igen. Denne funktion bruges, når organisationen ønsker, at alle posteringer, herunder reguleringer siden sidste årsafslutning, skal bogføres i en enkelt regnskabspost for ultimosaldo- og startsaldoposter. Hvis denne parameter er angivet til **Nej**, bevares alle ultimosaldo- og startsaldoposter. De slettes ikke. Der oprettes i stedet en ny ultimosaldo- og startsaldopost for de delta- eller nye posteringer, der er bogført siden sidste årsafslutning af regnskabsåret.

> [!NOTE]
> Ultimosaldoposten oprettes i det år, der afsluttes. Dette sker kun, hvis parameteren Finans **Opret ultimoposteringer ved overførsel** er angivet til **Ja**. Startsaldoposten oprettes altid, da dette er startsaldoen for det næste år.

## <a name="general-ledger-what-is-the-difference-between-close-all-and-close-single-options-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process"></a>Finans: Hvad er forskellen mellem indstillingerne "Luk alle" og "Luk enkelt" i dimensionssektionen Overfør drift i årsafslutningsprocessen?

**Luk alle** bevarer de oprindelige økonomiske dimensionsværdier fra bogførte posteringer og bruger dem til at oprette startsaldi for resultatkontoen. Der oprettes separate startsaldi for resultatkonti for hver enkelt kombination af økonomiske dimensionsværdier. Hvis **Afslut en enkelt** er valgt, opsummeres alle posteringer, der er bogført med den pågældende økonomiske dimension, i en primosaldo for resultatkonti for den dimensionsværdi, der er angivet i det felt, som vises efter **Afslut en enkelt**. 

Alle posteringer for regnskabsåret er f.eks. bogført med kontostrukturen Hovedkonto – Afdeling. For den økonomiske dimension Afdeling i skabelonen er **Afslut en enkelt** valgt, og 100 er angivet som dimensionsværdien. Hvis den samlede indtægt for alle posteringer, der er bogført på afdelingerne 200, 300 og 400 er $100.000, oprettes der en startsaldo for Overført overskud – 100. Hvis du vælger **Afslut en enkelt**, men lader den økonomiske dimensionsværdi være tom, bogføres alle posteringer på overført overskud, og dimensionsværdien vil være tom.

## <a name="general-ledger-when-i-select-close-single-option-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process-will-my-detailed-transactional-information-be-lost"></a>Finans: Når jeg vælger indstillingen "Luk enkelt" i dimensionssektionen Overfør drift i årsslutningsprocessen, går mine detaljerede posteringsoplysninger tabt?

Indstillingerne **Luk alle** og **Luk enkelt** bruges til at angive, hvilke økonomiske dimensioner i posteringer, der bogføres på driftskonti, der skal overføres til hovedkontoen for overført overskud. Den historiske og detaljerede bogføring til driftskontiene har ingen indflydelse og vil være detaljeret. Indstillingen har indflydelse på det detaljeringsniveau, der overføres til kontiene for overført overskud som en startsaldo i det nye år. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-the-reporting-currency-for-the-year-does-not-balance-what-does-this-mean"></a>Finans: Årsafslutningen mislykkes, fordi rapporteringsvalutaen for året ikke balancerer. Hvad betyder dette?

Denne fejl kan du oplever, når du har aktiveret funktionen **Opmærksomhed mellem finansudligning og årsafslutning** (funktionen Opmærksomhed). Når funktionen er aktiveret, medtages finansposteringer, der er udlignet, ikke længere i startsaldoen for det næste regnskabsår, når afslutningen af finansåret afsluttes. Udelukkes af finansposteringer, der er udlignet, kan give udfordringer for kunderne ved årsafslutningen, hvis Finans er defineret som en rapporteringsvaluta.   
Finansudligning udføres kun for regnskabsvalutaen.  Når finansposteringerne er udlignet, sikrer valideringen kun regnskabsvalutaens debetbeløb svarende til regnskabsvalutakreditterne. Beløbene i rapporteringsvalutaen for disse finansposteringer valideres ikke og har muligvis ikke debiteringer = krediteringer.  Derudover beregner og bogføres der ikke automatisk vinding/tab i rapporteringsvalutaen.  På grund af disse begrænsninger skal der findes en postering for vinding/tab i rapporteringsvalutaen ved udførelse af finansudligninger.  Hvis vinding/tab ikke indgår i finansudligning, vil lukningen ved årsafslutning resultere i en meddelelse om saldoafvigelse.  Flere oplysninger i [Forståelsen mellem funktionen til finansudligning og rapporteringsvalutaen har saldoafvigelse](reporting-currency-yec.md).

## <a name="general-ledger-what-can-be-changed-to-help-enhance-the-performance-of-year-end-processing"></a>Finans: Hvad kan ændres for at hjælpe med at øge ydeevnen for årsafslutningsbehandling?

Du kan foretage flere ændringer for at hjælpe med at forbedre ydeevnen i forbindelse med årsafslutningen. Det anbefales, at du evaluerer disse foreslåede ændringer for at vurdere, om de er relevant for organisationen.

### <a name="optimize-year-end-close-service"></a>Optimer tjenesten årsafslutning

Tjenesten **Optimer årsafslutning**-tjenesten gør det muligt for Microsoft Dynamics 365 Finance-kunder at sætte fart i deres årsafslutninger ved at flytte den tunge årsafslutningsbehandling til en mikroservice. Den tid, der gemmes via en effektiv lukning ved årsslutning, gør det muligt for de enkelte Finance-team at reagere i god tid på nødvendige justeringer og dermed afslutte generering af regnskabsrapporter. Når året afsluttes på en mikroservice, frigøres værdifulde ressourcer. Ved behandlingen minimeres belastningen på SQL Server, og kunderne får mulighed for at sætte fart i årsafslutningsbehandlingen.

Tjenesten **Optimer årsafslutning** er tilgængelig i version 10.0.31, så flere kunder kan bruge den nye service til 2022-årsafslutningen. Tjenesten er desuden tilbageporteret til versionerne 10.0.30 og 10.0.29. Du kan finde yderligere oplysninger i [Optimer årsafslutning](optimize-year-end-close.md).

### <a name="dimension-sets"></a>Dimensionsopsætninger

Når du kører årsslutslutning, oprettes de enkelte saldi for dimensionssættet igen. Denne funktionsmåde har direkte indflydelse på ydeevnen. Visse organisationer opretter dimensionsopsætninger unødvendigt, fordi de er brugt på et tidspunkt eller måske skal bruges på et tidspunkt. Da disse unødvendige dimensionsopsætninger opbygges, når årsslutningen lukkes, øges den tid, der bruges til processen. Brug tid på at evaluere dimensionsopsætninger og slette eventuelle unødvendige handlinger.

De unødvendige dimensionsopsætninger har også indflydelse på batchjobbet **BudgetDimensionFocusInitializeBalance** (**Finans \> Kontoplan \> Dimensioner \> Økonomiske dimensionsopsætninger**).

[![Økonomiske dimensionsopsætninger.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Konfiguration af skabelon til årsafslutning

I skabelonen til årsafslutning kan organisationer vælge det økonomiske dimensionsniveau, der skal vedligeholdes ved overførsel af driftssaldi til overført overskud. Indstillingerne giver en organisation mulighed for at vedligeholde de detaljerede økonomiske dimensioner (**Luk alle**) ved flytning af saldi til overført resultat eller vælger at opsummere beløbene til en enkelt dimensionsværdi (**Luk enkelt**). Dette kan defineres for hver økonomisk dimension. Yderligere oplysninger om disse indstillinger finder du i artiklen [Årsafslutning](year-end-close.md).

Det anbefales, at du evaluerer organisationens krav og, hvis det er muligt, lukker så mange dimensioner som muligt ved hjælp af indstillingen **Luk enkelt** for at forbedre ydeevnen. Ved at lukke til en enkelt dimensionsværdi (som også kan være en tom værdi), beregner systemet færre detaljer ved bestemmelse af saldi for poster på konti til overført overskud.

### <a name="degenerate-dimensions"></a>Degenerere dimensioner

En degenereret dimension giver ikke mulighed for at genbruge den i sig selv og sammen med andre dimensioner. Der findes to forskellige typer degenererede dimensioner. Den første type er en dimension, der er individuelt degenereret. Normalt vises denne type degenererede dimensioner kun på en enkelt postering eller i mindre sæt af posteringer. Den anden type er en dimension, der bliver degenereret i kombination med en eller flere yderligere dimensioner, der udnytter samme potentiale baseret på de mulige kombinationsmuligheder, der kan genereres. En degenereret dimension kan have stor indflydelse på processens ydeevne i årsafslutningen. Hvis du vil minimere problemer med ydeevnen, skal du definere alle degenererede dimensioner som **Luk enkelt** i opsætningen af årsafslutning som beskrevet i det foregående afsnit.

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2022"></a>Kreditor: Hvilke ændringer er der foretaget for at understøtte 1099-årsafslutningsrapportering for 2022?

#### <a name="update-to-all-1099-forms"></a>Opdater til alle 1099-formularer

Følgende ændringer er foretaget i alle 1099-formularer for 2022-skatteåret:

- I 2021 blev året fastlagt på 1099-formularer. Fra og med 2022 udfyldes året af rapporten.

#### <a name="1099-misc"></a>1099-MISC

Følgende opdateringer er foretaget på formularen 1099-MISC for 2022-skatteåret:

- Felt 13: Angiver nu indsendelseskravet til lovgivningen om efterrettelighed vedrørende beskatning af konti i udlandet (FATCA – Foreign Account Tax Compliance Act).
- Felt 14: Bruges nu til at rapportere de overskydende gylden faldskærm-betalinger.
- Boks 15: Bruges nu til at rapportere betalingen under ikke-kvalificerede, udskudte kompensationsplaner (NQDC).
- Boks 16: Bruges nu til at rapportere tilbageholdt moms på statsniveau.
- Felt 17: Bruges nu til at rapportere betalerens statsnummer.
- Boks 18: Bruges nu til at rapportere indkomsten på statsniveau.

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Kreditor: 1099 – Hvordan ændrer jeg 1099-feltet og -værdier for en kreditor, der ikke sporer 1099-oplysninger i løbet af hele året?

Brug funktionen **Opdater 1099** til at gennemgå tidligere betalte fakturaposteringer og tildele 1099-dataene på en korrekt måde i henhold til indstillingerne under fanen **Moms 1099** på siden **Leverandør**. Hvis du vil bruge funktionen **Opdater 1099**, skal du gå til **Kreditorer \> Leverandører \> Alle leverandører**, vælge en leverandør og derefter i ruden Handling på fanen **Leverandør** vælge **Opdater 1099**.

## <a name="can-i-run-the-update-1099-functionality-for-all-my-vendors-at-once"></a>Kan jeg køre 1099-opdateringen for alle mine kreditorer på én gang?

Du kan bruge **Opdater 1099-oplysningerne for flere kreditorer** til at opdatere 1099-feltet i en kreditorpost og til at opdatere posteringer med oplysningerne fra 1099-feltet. Du kan åbne denne side ved at gå til **Kreditor \> Periodisk opgave \> Moms 1099**. For at få adgang til siden skal du være tildelt feltet **Opdater 1099 og posteringer for flere kreditorers**-sikkerhedsrettigheder.

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Kreditor: 1099 – Genberegn eksisterende 1099-beløb vs. Opdater alle i Opdatering 1099-værktøjet

**Genberegn eksisterende 1099-beløb**-afkrydsningsfeltet nulstiller 1099-beløbet til det samlede betalte beløb, når det bruges sammen med afkrydsningsfeltet **Opdater alle**.

[![Moms 1099-transaktioner: Før opdateringsrutinen køres.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Afkrydsningsfeltet **Genberegn eksisterende 1099-beløb** træder først i kraft, når der er 1099-delværdier på fakturaen, eller hvis det er ændret i formularen Moms 1099. Antag f.eks., at en faktura har værditilvæksten i $1.000,00, men brugeren skriver manuelt et 1099-beløb på $500,00 på fakturaen.

[![Moms 1099-transaktioner: Afmærkning af både Opdater alle og Genberegn eksisterende 1099-beløb.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Når denne faktura er betalt, er de $500,00 det 1099-beløb, der er betalt. Hvis du udfører efterberegningsrutinen, vil systemet ændre 1099-beløbet til $1.000,00, hvilket er den samlede betaling.

[![Moms 1099-transaktioner: Efter kørsel af 1099-rutinen.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Kreditor: 1099 – Opret 1099-posteringer manuelt

Det kan være nødvendigt for en organisation at oprette 1099-transaktioner manuelt, der ikke har tilknyttet en faktura. Du kan tilføje manuelle 1099-posteringer til **Kreditor \> Periodiske opgaver \> Moms 1099 \> Kreditorudligning for 1099**. Vælg knappen **Manuelle 1099-transaktioner**.

Manuelt oprettede 1099-transaktioner opdateres ikke med processen **Opdater alle** eller processen til **Genberegn eksisterende 1099-beløb** i **Opdateringsværktøj til 1099**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Kreditor: 1099 – Understøtter Dynamics 365 Finance 1096-formularen?

Dynamics 365 Finance udskriver ikke 1096 Annual Summary and Transmittal of US Information Returns-formularen.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Kreditor: 1099 – Findes der nye funktioner, der understøtter 1099-rapportering for den offentlige sektor?

Der er tilføjet en ny funktion til den offentlige sektor, **Opdater 1099-oplysninger efter hovedkonto**, som du kan aktivere i arbejdsområdet til **Funktionsstyring**. Med denne funktion kan du tilknytte 1099-værdierne for en kreditor til hovedkontoen i regnskabsfordelingen og ikke standardkontoen i kreditorposten.

Du kan finde flere oplysninger i [Konfigurere kreditorer til 1099-rapportering](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
