---
title: Ofte spurgte spørgsmål i forbindelse med ultimoaktiviteter
description: Dette emne er kompileret for at hjælpe med ultimoaktiviteter.
author: kweekley
manager: tfehr
ms.date: 01/25/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a9feafcab5969e9ec8fcbb8a6903d7b59505f6ae
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249405"
---
# <a name="year-end-activities-faq"></a>Ofte spurgte spørgsmål i forbindelse med ultimoaktiviteter 

Dette emne er kompileret for at hjælpe med ultimoaktiviteter. Oplysningerne i dette emne fokuserer primært på spørgsmål, der vedrører ultimoaktiviteter ved årsopgørelsen for Finans og Kreditor.

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Finans: Hvordan ved jeg, at vi kører ultimoafslutning og ikke kan fortryde ultimoafslutning?
Vi har set organisationer forsøge at køre ultimoafslutninger, men i stedet fortrød ultimoafslutningen. Hvis ultimoafslutning lukkes meget hurtigt, eller ultimoafslutning ikke giver startsaldi, skal du validere indstillingen **Fortryd forrige lukning** i **Ultimoafslutning** (**Finans > Periodelukning > Ultimoafslutning > Kør regnskabsafslutning**). 

[![Kør ultimoafslutning i forhold til fortryd ultimoafslutning](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

Hvis **Fortryd forrige afslutning** er angivet til **Ja**, tilbageføres den forrige ultimoafslutning. Når du kører en fortrydelse, slettes alle ultimosaldoposter og startsaldoposter, som om ultimoafslutningen aldrig var blevet kørt. Bilagene slettes. Årsafslutningen køres ikke automatisk igen. Du skal starte processen igen, og denne gang skal du ændre **Fortryd forrige lukning** til **Nej**. 

> [!NOTE]
> Ultimosaldoposten oprettes efter eget valg i det år, der afsluttes. Dette sker kun, hvis parameteren Finans **Opret ultimoposteringer ved overførsel** er angivet til **Ja**. Startsaldoposten oprettes altid, da dette er startsaldoen for det næste år.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Finans: Hvad er forskellen mellem Fortryd og Slet Finansparameteren for årsslutning?
Der kan være forvirring over forskellen mellem parameteren **Fortryd forrige lukning**, der findes i dialogboksen til **Årsafslutning**, og posteringerne for parameteren **Slette årsafslutningsposter ved overførsel** i Finans (**Finans > Periodens afslutning > Årsslutslutning > Kør regnskabsafslutning**).  

[![Forskellen mellem Fortryd og Slet Finansparameteren for årsslutning](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Vælg **Fortryd forrige afslutning** i rullemenuen, når du kører årsafslutningen for at slette alle ultimosaldo- og startsaldoposter, som om årsafslutningen aldrig var blevet kørt. Bilagene slettes. Årsafslutningen køres ikke automatisk igen. Hvis du vil køre årsafslutningen, skal du starte denne proces igen, og denne gang skal du ændre **Fortryd forrige afslutning** til **Nej** (**Finans > Opsætning af Finans > Finansparametre**). 

[![Konfiguration af Finansparametre](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

Parameteret **Slette årsafslutningsposter ved overførsel** i Finans bruges kun, når der køres (ikke fortrydes) årsslutslutning årsafslutning (**Fortryd forrige afslutning** er angivet til **Nej**). Hvis den parameter er angivet til **Ja**, slettes alle ultimosaldoposter og startsaldoposter, og årsafslutningen køres igen. Denne proces bruges, når organisationen ønsker, at alle posteringer, herunder reguleringer siden sidste årsafslutning, skal bogføres i en enkelt regnskabspost for ultimosaldo- og startsaldoposter. 

Hvis denne indstilling er angivet til **Nej**, bevares alle ultimosaldo- og startsaldoposter. De slettes ikke. Der oprettes i stedet en ny ultimosaldo- og startsaldopost for de delta- eller nye posteringer, der er bogført siden sidste årsafslutning af regnskabsåret.  

> [!NOTE]
> Ultimosaldoposten oprettes i det år, der afsluttes. Dette sker kun, hvis parameteren Finans **Opret ultimoposteringer ved overførsel** er angivet til **Ja**. Startsaldoposten oprettes altid, da dette er startsaldoen for det næste år. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Finans: Hvad kan ændres for at øge ydeevnen for årsafslutningsbehandling? 
Du kan foretage en række ændringer for at forbedre ydeevnen i forbindelse med årsafslutningen. Det anbefales, at du evaluerer disse foreslåede ændringer for at finde ud af, om ændringen er relevant for organisationen.  

### <a name="dimension-sets"></a>Dimensionsopsætninger
Når du kører årsafslutning, oprettes de enkelte saldi igen, hvilket har direkte indflydelse på ydeevnen. Visse organisationer opretter dimensionsopsætninger unødvendigt, fordi de er brugt på et tidspunkt eller måske skal bruges på et tidspunkt.  Disse unødvendige dimensionsopsætninger opbygges stadig, når årsslutningen lukkes, hvilket øger den tid, der bruges til processen. Brug tid på at evaluere dimensionsopsætninger og slette eventuelle unødvendige dimensionsopsætninger.

De unødvendige dimensionsopsætninger har også indflydelse på batchjobbet **BudgetDimensionFocusInitializeBalance** (**Finans > Kontoplan > Dimensioner > Økonomiske dimensionsopsætninger**).

[![Økonomiske dimensionsopsætninger](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Konfiguration af skabelon til årsafslutning
I skabelonen til årsafslutning kan organisationer vælge det økonomiske dimensionsniveau, der skal vedligeholdes ved overførsel af driftssaldi til overført overskud. Indstillingerne giver en organisation mulighed for at vedligeholde de detaljerede økonomiske dimensioner (**Luk alle**) ved flytning af saldi til overført resultat eller vælger at opsummere beløbene til en enkelt dimensionsværdi (**Luk enkelt**). Dette kan defineres for hver økonomisk dimension. Yderligere oplysninger om disse indstillinger finder du i emnet [Årsafslutning](year-end-close.md).

Det anbefales, at du evaluerer organisationens krav og, hvis det er muligt, lukker så mange dimensioner som muligt ved hjælp af indstillingen **Luk enkelt** for at forbedre ydeevnen. Ved at lukke til en enkelt dimensionsværdi (som også kan være en tom værdi), beregner systemet færre detaljer ved bestemmelse af saldi for poster på konti til overført overskud.

### <a name="10013-update-or-later"></a>10.0.13 opdatering eller senere
Hvis du har opdateret til version 10.0.13 eller senere, siden sidste gang organisationen kørte en årsafslutning, kan årsafslutningen tage længere tid pga. [HashV2-funktionsimplementering](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/verify-hash-function-changes-after-update-to-dynamics-365-finance-2020-release-wave-2). (Betegnelsen *hash* refererer til et felt, der er beregnet ud fra andre strengfelter. API'en til beregning af værdien for Hash GUID-værdien er opdateret for at øge sikkerheden. For hurtigere at kunne afslutte ultimoaktiviteter anbefales det, at saldi for dimensionsopsætninger gendannes, før ultimoafslutningen køres. Hvis du allerede har udført en gendannelse af saldi for dimensionsopsætninger efter at have foretaget opdateringen 10.0.13, er det ikke nødvendigt at køre gendanne processen.
 
## <a name="general-ledger--what-does-the-period-close--year-end-close-do"></a>Finans – Hvad betyder Periodelukning – Årsafslutning?
 
[![Periodelukning, årsafslutning](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets-new-feature"></a>Forbedringer af ydeevne til gendannelse af økonomiske dimensionsopsætninger (ny funktion)
En ny funktion, der er tilføjet i version 10.0.16, forbedrer ydeevnen årsafslutnings- og konsolideringsprocesserne. Funktionen er navngivet, Forbedringer af ydeevne til gendannelse af økonomiske dimensionsopsætninger. Med denne funktion ændres den måde, dimensionsopsætninger opbygges på, så de kun opbygges i en relevant tidsramme. I tidligere versioner blev dimensionssæt genopført for alle datoer. Hvis du f.eks. lukker år 2020, gendanner systemet kun saldi for posteringer i regnskabsåret 2020. Hvis du kører konsolidering for et datointerval fra 1. november 2020 til 30. november 2020, gendanner systemet kun saldi for dette datointerval.

Da denne funktion opfattes som en ændring, der giver beskadigelse, skal du aktivere den ved hjælp af arbejdsområdet **Funktionsstyring**.
 
[![Årsafslutning](./media/faq-2020-yr-end-06.png)](./media/faq-2020-yr-end-06.png)

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2020"></a>Kreditor: Hvilke ændringer er der foretaget for at understøtte 1099-årsafslutningsrapportering for 2020?

Der er tilføjet to nye lovpligtige funktioner for ændringer i 1099-årsafslutning i 2020. Den første funktion, **Anvend ændringer på 1099-NEC og 1099-MISC-formularer til 2020**, blev udgivet midt i året som en obligatorisk funktion. Formålet med dette er at sikre, at der kan spores 1099-transaktionsdata for året 2020 til den nye 1099-NEC-formular. Denne funktion har tilføjet de 1099-felter, der skal bruges for at understøtte de nye 1099-NEC og opdaterede 1099-MISC-felter. Denne opdatering har også opgraderet kreditorpostdataene til 1099-feltoplysningerne. 

Den anden lovpligtige funktion, **1099-erklæringer, der er opdateret til 2020-skattelovgivningen**, indeholder følgende ændringer.

- 1099-OID - IRS har konverteret formularen til fortløbende brug.
   - Rapporteringsårets nummer 3 og 4 skal udfyldes, når de udskrives. Brug udskriftsindstillingerne i **Rapporteringsår**-feltets 3. og 4. cifre fra 4. cifre fra **Udskriftsindstillinger for Moms 1099**. 

- 1099-NEC – En ny formular til 2020. Denne registrerer kompensation for ingen ansatte. 

-   1099-MISC – På grund af oprettelsen af formular 1099-NEC har IRS revideret formular 1099-MISC og omarrangeret feltnumre til rapportering af bestemte indtægter.
Ændringer i rapportering af indtægter og formularens feltnumre vises nedenfor.
   - Betaleren har foretaget direkte salg for $5.000 eller mere (afkrydsningsfelt) i felt 7.
   - Forsikringspræmien indberettes i felt 9.
   - Bruttofortjeneste til jurist rapporteres i felt 10.
   - Sektion 409A udskydelser rapporteres i felt 12.
   - Ikke-kvalificeret udskudt kompensationsindtægt rapporteres i felt 14.
   - Felterne 15, 16 og 17 indberetter tilbageholdt statsskat, stats-id og indtægtsbeløb i staten.

- Ingen ændringer af 1099-DIV eller 1099-INT i 2020.

- Elektronisk indsendelse – Formatet er ændret for at tage højde for den nye NEC-formular, og MISC-feltet ændres som beskrevet ovenfor. Se [IRS-publikation 1220](https://www.irs.gov/pub/irs-pdf/p1220.pdf), hvis du vil have specifikke oplysninger om elektronisk indsendelse.

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Kreditor: 1099 – Hvordan ændrer jeg 1099-feltet og -værdier for en kreditor, der ikke sporer 1099-oplysninger i løbet af hele året?
Brug funktionen Opdater 1099 (**Kreditor > Kreditorer>Alle kreditorer > Vælg en kreditor > fanen Kreditor på båndet > Opdater 1099**) for at gennemgå tidligere betalte fakturaposteringer for at tildele 1099-dataene igen i henhold til indstillingerne under fanen **Moms 1099** på siden **Kreditor**.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Kan jeg køre 1099-opdateringen for alle mine kreditorer på én gang?
Nr. Opdateringsrutinen 1099 udføres i forhold til en enkelt leverandør ad gangen. Hvis organisationen har brug for dette krav, skal du stemme for ideen med titlen [BatchProces for opdatering af kreditors 1099-data](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-vs-update-all-in-the-update-1099-utility"></a>Kreditor: 1099 – "Genberegn eksisterende 1099-beløb" vs. "Opdater alle" i Opdatering 1099-værktøjet.
**Genberegn eksisterende 1099-beløb**-afkrydsningsfeltet nulstiller 1099-beløbet til det samlede betalte beløb, når det bruges sammen med afkrydsningsfeltet **Opdater alle**. 

[![Moms 1099-transaktioner: Før opdateringsrutinen køres](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Afkrydsningsfeltet **Genberegn eksisterende 1099-beløb** træder først i kraft, når der er 1099-delværdier på fakturaen, eller hvis det er ændret i formularen Moms 1099. Antag f.eks., at en faktura har værditilvæksten i $1000,00, men brugeren skriver manuelt et 1099-beløb på $500,00.

[![Moms 1099-transaktioner: Afmærkning af både Opdater alle og Genberegn eksisterende 1099-beløb](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Når denne betaling er betalt, er de $500.00 det 1099-beløb, der er betalt. Hvis du udfører efterberegningsrutinen, vil systemet ændre 1099-beløbet til $1000,00, hvilket er den samlede betaling.

[![Moms 1099-transaktioner: Efter kørsel af 1099-rutinen](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Kreditor: 1099 – Opret 1099-posteringer manuelt
Det kan være nødvendigt for en organisation at oprette 1099-transaktioner manuelt, der ikke har tilknyttet en faktura. Du kan tilføje manuelle 1099-posteringer til **Kreditor > Periodiske opgaver > Moms 1099 > Kreditorudligning for 1099**. Vælg knappen **Manuelle 1099-transaktioner**. 

Manuelt oprettede 1099-posteringer opdateres ikke med processen **Opdater alle** eller processen til **Genberegn eksisterende 1099-beløb** i **Opdateringsværktøj til 1099**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Kreditor: 1099 – Understøtter Dynamics 365 Finance 1096-formularen? 

Dynamics 365 Finance udskriver ikke 1096 Annual Summary and Transmittal of US Information Returns-formlaren.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Kreditor: 1099 – Findes der nye funktioner, der understøtter 1099-rapportering for den offentlige sektor? 
Der er tilføjet en ny funktion til den offentlige sektor, **Opdater 1099-oplysninger efter hovedkonto**, som du kan aktivere i arbejdsområdet til **Funktionsstyring**. Med denne funktion kan du tilknytte 1099-værdierne for en kreditor til hovedkontoen i regnskabsfordelingen og ikke standardkontoen i kreditorposten.

Du kan finde flere oplysninger i [Konfigurere kreditorer til 1099-rapportering](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]