---
title: Ofte spurgte spørgsmål om aktiviteter ved årsafslutningen
description: Denne artikel indeholder en oversigt over de spørgsmål, der kan opstå ved årsafslutningen, og de svar, der kan være en hjælp ved lukning af årets aktiviteter.
author: moaamer
ms.date: 12/21/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1c5aca6180821dfc9fd1d475d4726c82acdf4d78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865734"
---
# <a name="year-end-activities-faq"></a>Ofte spurgte spørgsmål om aktiviteter ved årsafslutningen 

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over de spørgsmål, der kan opstå ved årsafslutningen, og de svar, der kan være en hjælp ved lukning af årets aktiviteter. Oplysningerne i denne artikel fokuserer primært på spørgsmål, der vedrører ultimoaktiviteter ved årsopgørelsen for Finans og Kreditor.

## <a name="general-ledger-year-end-enhancements"></a>Forbedringer af årsopgørelsen for Finans 
Version 10.0.20 indeholder en forbedring af årsslutpunktet, som er aktiveret som standard og starter med version 10.0.25. Hvis organisationen bruger en version, der er ældre end 10.0.25, anbefales det, at du aktiverer denne funktion, før årsafslutningsprocessen startes. Før du kan bruge denne funktion, skal den være aktiveret i dit system. Administratorer kan bruge arbejdsområdet Funktionsstyring til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

 - Modul: Finans
 - Funktionsnavn: Forbedringer af årsopgørelsen for Finans

Opsætningen af skabeloner til årsafslutningen er flyttet til en ny opsætningsside, **Skabelon til opsætning af årsafslutning**. Den eksisterende årsafslutningsside ændres på samme måde som værdireguleringen af udenlandsk valuta i finansmodulet, hvor der vises en liste, hver gang lukningen af årsafslutningen køres eller tilbageføres. En regnskabschef kan starte årsafslutningen fra den nye side. 

Hvis du vil tilbageføre årsafslutningen, skal du vælge det seneste regnskabsår for den relevante juridiske enhed og vælge knappen **Tilbageføre årsafslutning**. Tilbageførslen sletter regnskabsposterne for den forrige årsafslutning og vil ikke automatisk køre årsafslutningen igen. 

Du kan køre årsslutningen igen ved at genstarte processen for regnskabsåret og den juridiske enhed. Processen vil fortsætte med at bruge parameterindstillingen for Finans til at bestemme, om årsafslutningen kun skal bruges til nye eller ændrede posteringer, eller til at tilbageføre den forrige lukning helt og køre processen for alle posteringer igen.  

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Finans: Hvordan ved jeg, at vi kører ultimoafslutning og ikke kan fortryde ultimoafslutning?
Vi har set organisationer forsøge at køre ultimoafslutninger, men i stedet fortrød ultimoafslutningen. Hvis ultimoafslutning lukkes meget hurtigt, eller ultimoafslutning ikke giver startsaldi, skal du validere indstillingen **Fortryd forrige lukning** i **Ultimoafslutning** (**Finans > Periodelukning > Ultimoafslutning > Kør regnskabsafslutning**). 

[![Kør ultimoafslutning i forhold til fortryd ultimoafslutning.](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

Hvis **Fortryd forrige afslutning** er angivet til **Ja**, tilbageføres den forrige ultimoafslutning. Når du kører en fortrydelse, slettes alle ultimosaldoposter og startsaldoposter, som om ultimoafslutningen aldrig var blevet kørt. Bilagene slettes. Årsafslutningen køres ikke automatisk igen. Du skal starte processen igen, og denne gang skal du ændre **Fortryd forrige lukning** til **Nej**. 

> [!NOTE]
> Ultimosaldoposten oprettes efter eget valg i det år, der afsluttes. Dette sker kun, hvis parameteren Finans **Opret ultimoposteringer ved overførsel** er angivet til **Ja**. Startsaldoposten oprettes altid, da dette er startsaldoen for det næste år.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Finans: Hvad er forskellen mellem Fortryd og Slet Finansparameteren for årsslutning?
Der kan være forvirring over forskellen mellem parameteren **Fortryd forrige lukning**, der findes i dialogboksen til **Årsafslutning**, og posteringerne for parameteren **Slette årsafslutningstransaktioner ved overførsel** i Finans (**Finans > Periodens afslutning > Årsslutslutning > Kør regnskabsafslutning**).  

[![Forskellen mellem Fortryd og Slet Finansparameteren for årsslutning.](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Vælg **Fortryd forrige afslutning** i rullemenuen, når du kører årsafslutningen for at slette alle ultimosaldo- og startsaldoposter, som om årsafslutningen aldrig var blevet kørt. Bilagene slettes. Årsafslutningen køres ikke automatisk igen. Hvis du vil køre årsafslutningen, skal du starte denne proces igen, og denne gang skal du ændre **Fortryd forrige afslutning** til **Nej** (**Finans > Opsætning af Finans > Finansparametre**). 

[![Konfiguration af Finansparametre.](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

Parameteret **Slette årsafslutningstransaktioner ved overførsel** i Finans bruges kun, når der køres (ikke fortrydes) årsslutslutning årsafslutning (**Fortryd forrige afslutning** er angivet til **Nej**). Hvis den parameter er angivet til **Ja**, slettes alle ultimosaldoposter og startsaldoposter, og årsafslutningen køres igen. Denne proces bruges, når organisationen ønsker, at alle posteringer, herunder reguleringer siden sidste årsafslutning, skal bogføres i en enkelt regnskabspost for ultimosaldo- og startsaldoposter. 

Hvis denne indstilling er angivet til **Nej**, bevares alle ultimosaldo- og startsaldoposter. De slettes ikke. Der oprettes i stedet en ny ultimosaldo- og startsaldopost for de delta- eller nye posteringer, der er bogført siden sidste årsafslutning af regnskabsåret.  

> [!NOTE]
> Ultimosaldoposten oprettes i det år, der afsluttes. Dette sker kun, hvis parameteren Finans **Opret ultimoposteringer ved overførsel** er angivet til **Ja**. Startsaldoposten oprettes altid, da dette er startsaldoen for det næste år. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Finans: Hvad kan ændres for at øge ydeevnen for årsafslutningsbehandling? 
Du kan foretage en række ændringer for at forbedre ydeevnen i forbindelse med årsafslutningen. Det anbefales, at du evaluerer disse foreslåede ændringer for at finde ud af, om ændringen er relevant for organisationen.  

### <a name="dimension-sets"></a>Dimensionsopsætninger
Når du kører årsafslutning, oprettes de enkelte saldi igen, hvilket har direkte indflydelse på ydeevnen. Visse organisationer opretter dimensionsopsætninger unødvendigt, fordi de er brugt på et tidspunkt eller måske skal bruges på et tidspunkt.  Disse unødvendige dimensionsopsætninger opbygges stadig, når årsslutningen lukkes, hvilket øger den tid, der bruges til processen. Brug tid på at evaluere dimensionsopsætninger og slette eventuelle unødvendige dimensionsopsætninger.

De unødvendige dimensionsopsætninger har også indflydelse på batchjobbet **BudgetDimensionFocusInitializeBalance** (**Finans > Kontoplan > Dimensioner > Økonomiske dimensionsopsætninger**).

[![Økonomiske dimensionsopsætninger.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Konfiguration af skabelon til årsafslutning
I skabelonen til årsafslutning kan organisationer vælge det økonomiske dimensionsniveau, der skal vedligeholdes ved overførsel af driftssaldi til overført overskud. Indstillingerne giver en organisation mulighed for at vedligeholde de detaljerede økonomiske dimensioner (**Luk alle**) ved flytning af saldi til overført resultat eller vælger at opsummere beløbene til en enkelt dimensionsværdi (**Luk enkelt**). Dette kan defineres for hver økonomisk dimension. Yderligere oplysninger om disse indstillinger finder du i artiklen [Årsafslutning](year-end-close.md).

Det anbefales, at du evaluerer organisationens krav og, hvis det er muligt, lukker så mange dimensioner som muligt ved hjælp af indstillingen **Luk enkelt** for at forbedre ydeevnen. Ved at lukke til en enkelt dimensionsværdi (som også kan være en tom værdi), beregner systemet færre detaljer ved bestemmelse af saldi for poster på konti til overført overskud.

## <a name="degenerate-dimensions"></a>Degenerere dimensioner

En degenereret dimension giver ikke mulighed for at genbruge den i sig selv og sammen med andre dimensioner. Der findes to forskellige typer degenererede dimensioner. Den første type er en dimension, der er individuelt degenereret. Normalt vises denne type degenererede dimensioner kun på en enkelt postering eller i mindre sæt af posteringer. Den anden type er en dimension, der bliver degenereret i kombination med en eller flere yderligere dimensioner, der udnytter samme potentiale baseret på de mulige kombinationsmuligheder, der kan genereres. En degenereret dimension kan have stor indflydelse på processens ydeevne i årsafslutningen. Hvis du vil minimere problemer med ydeevnen, skal du definere alle degenererede dimensioner som **Luk enkelt** i opsætningen af årsafslutning som beskrevet i det foregående afsnit.

## <a name="general-ledger-what-does-the-period-close-year-end-close-do"></a>Finans: Hvad betyder periodelukning – Årsafslutning?
 
[![Periodelukning, årsafslutning.](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets"></a>Ydeevneforbedringer til genopbygning af økonomiske dimensionssæt
En ny funktion, der blev tilføjet i version 10.0.16, forbedrer ydeevnen årsafslutnings- og konsolideringsprocesserne. Funktionen er navngivet, Forbedringer af ydeevne til gendannelse af økonomiske dimensionsopsætninger. Med denne funktion ændres den måde, dimensionsopsætninger opbygges på, så de kun opbygges i en relevant tidsramme. I tidligere versioner blev dimensionssæt genopført for alle datoer. Hvis du f.eks. lukker år 2020, gendanner systemet kun saldi for posteringer i regnskabsåret 2020. Hvis du kører konsolidering for et datointerval fra 1. november 2020 til 30. november 2020, gendanner systemet kun saldi for dette datointerval.

Før du kan bruge denne funktion, skal den være aktiveret i dit system. Administratorer kan bruge arbejdsområdet Funktionsstyring til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:
 
- Modul: Finans
- Funktionsnavn: Forbedringer af ydeevne til gendannelse af økonomiske dimensionsopsætninger

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2021"></a>Kreditor: Hvilke ændringer er der foretaget for at understøtte 1099-årsafslutningsrapportering for 2021?

I 2021 er formularerne DIV, NEC og MISC ændret en smule, og der er tilføjet nogle ekstra felter.

#### <a name="div-new-box2e-2f"></a>DIV: nyt felt 2e, 2f
 
- Felt 2e. Viser den del af beløbet i felt 1a, der med sektion 897 kan henføres til disposition af amerikanske real property interests (USRPI).  
- Felt 2f. Viser den del af beløbet i felt 2a, der med sektion 897 kan henføres til disposition af USRPI. Bemærk, at felt 2e og 2f kun gælder for fremmede personer og enheder, hvis indtægter vedligeholder deres karakter, når de gennemgås eller fordeles til deres direkte eller indirekte udenlandske ejere eller beneficianter. Den behandles generelt som effektivt forbundet med en branche eller en virksomhed i USA. Se instruktionerne til selvangivelsen. 
 
#### <a name="nec-new-box-2"></a>NEC: nyt felt 2 
 
Hvis felt 2 er markeret, skal du rapportere forbrugsprodukter for i alt $5.000 eller mere, der er solgt til dig til videresalg, på basis af køb-salg, indbetalingsprovision eller andet. Du skal generelt rapportere indtægter fra dit salg af disse produkter i Plan C (formular 1040). 
 
Samtidig ændres formularstørrelsen for NEC. Under udskrivningen er der tre formularer pr. side. 
 
#### <a name="misc-new-box-11"></a>MISC: nyt felt 11 
 
Felt 11 viser det beløb, der er betalt for købet af varer til videresalg fra alle personer, der er involveret i den pågældende handel eller forretning. Se instruktionerne til momsangivelse for rapportering af denne indtægt. 
 
#### <a name="electronic-filing"></a>Elektronisk indsendelse 
Du kan finde oplysninger om elektronisk indsendelse under [Publikation for krav til elektronisk indsendelse](https://www.irs.gov/pub/irs-pdf/p1220.pdf).

Opdater formatspecifikationer og layout for poster til 2021 e-rapport 
- Sec. 2 Udsteder "A"-post. 
- Beløbskoder – Øget feltposition 28-45, længde til 18. 
 
#### <a name="sec-2-issuer-a-record-for-reporting-payments-on-form-1099-div"></a>Sek. 2 Udsteder "A"-post til rapportering af betalinger i form 1099-DIV: 
- Beløbstype – Tilføjet sektion 897 Ordinært udbytte og tilføjet beløbskode H. 
- Beløbstype – Tilføjet sektion 897 Kapitelvinding og tilføjet beløbskode J. 
 
#### <a name="sec-3-payee-b-record"></a>Sec. 3 Remittent "B"-post 
- Generelle oplysninger om poster – Opdateret tredje punkt fra 16 til 18 angående felter med betalingsbeløb. 
- Felttitel, betaling H – Opdateret feltposition 247-258, felttitel, længde og generel feltbeskrivelse. 
- Felttitel, betaling J – Opdateret feltposition 259-270, felttitel, længde og generel feltbeskrivelse. 
- Opdateret tomt felt til feltposition 271-286. 
- Opdateret indikator for udlandet til feltposition 287. 
- Opdateret linjefelt for første betalingsnavn til feltposition 288-327. 
- Opdateret linjefelt for andet betalingsnavn til feltposition 328-367. 
- Layoutpositioner for post, Formular 1099-MISC – Slettet feltposition 548 og felttitel FATCA Indikator for indsendelse af krav. 
- Layoutpositioner for poster, formular 1099-NEC – Opdateret 545-546 til blank, opdateret 547-felt til direkte salgsindikator, længde og beskrivelse og opdaterede bemærkninger til 548-722-feltet til tom. 
 
#### <a name="sec-4-end-of-issuer-c-record"></a>Sec. 4 Slut for udsteder "C"-post 
- Felttitel, betaling H – Opdateret feltposition 304-321, felttitel, længde og generel feltbeskrivelse. 
- Felttitel, betaling J – Opdateret feltposition 322-339, felttitel, længde og generel feltbeskrivelse. 
- Felttitel 340-499 – Opdateret længde til 160. 
 
#### <a name="sec-5-state-totals-k-record"></a>Sec. 5 State Totaler "K"-post 
- Felttitel, betaling H – Opdateret feltposition 304-321, felttitel, længde og generel feltbeskrivelse. 
- Felttitel, betaling J – Opdateret feltposition 322-339, felttitel, længde og generel feltbeskrivelse. 
- Felttitel 340-499 – Opdateret længde til 160.  

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Kreditor: 1099 – Hvordan ændrer jeg 1099-feltet og -værdier for en kreditor, der ikke sporer 1099-oplysninger i løbet af hele året?
Brug funktionen Opdater 1099 (**Kreditor > Kreditorer>Alle kreditorer > Vælg en kreditor > fanen Kreditor på båndet > Opdater 1099**) for at gennemgå tidligere betalte fakturaposteringer for at tildele 1099-dataene igen i henhold til indstillingerne under fanen **Moms 1099** på siden **Kreditor**.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Kan jeg køre 1099-opdateringen for alle mine kreditorer på én gang?
Nr. Opdateringsrutinen 1099 udføres i forhold til en enkelt leverandør ad gangen. Hvis organisationen har brug for dette krav, skal du stemme for ideen med titlen [BatchProces for opdatering af kreditors 1099-data](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Kreditor: 1099 – Genberegn eksisterende 1099-beløb vs. Opdater alle i Opdatering 1099-værktøjet
**Genberegn eksisterende 1099-beløb**-afkrydsningsfeltet nulstiller 1099-beløbet til det samlede betalte beløb, når det bruges sammen med afkrydsningsfeltet **Opdater alle**. 

[![Moms 1099-transaktioner: Før opdateringsrutinen køres.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Afkrydsningsfeltet **Genberegn eksisterende 1099-beløb** træder først i kraft, når der er 1099-delværdier på fakturaen, eller hvis det er ændret i formularen Moms 1099. Antag f.eks., at en faktura har værditilvæksten i $1000,00, men brugeren skriver manuelt et 1099-beløb på $500,00.

[![Moms 1099-transaktioner: Afmærkning af både Opdater alle og Genberegn eksisterende 1099-beløb.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Når denne betaling er betalt, er de DKK 500,00 det 1099-beløb, der er betalt. Hvis du udfører efterberegningsrutinen, vil systemet ændre 1099-beløbet til DKK 1000,00, hvilket er den samlede betaling.

[![Moms 1099-transaktioner: Efter kørsel af 1099-rutinen.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Kreditor: 1099 – Opret 1099-posteringer manuelt
Det kan være nødvendigt for en organisation at oprette 1099-transaktioner manuelt, der ikke har tilknyttet en faktura. Du kan tilføje manuelle 1099-posteringer til **Kreditor > Periodiske opgaver > Moms 1099 > Kreditorudligning for 1099**. Vælg knappen **Manuelle 1099-transaktioner**. 

Manuelt oprettede 1099-transaktioner opdateres ikke med processen **Opdater alle** eller processen til **Genberegn eksisterende 1099-beløb** i **Opdateringsværktøj til 1099**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Kreditor: 1099 – Understøtter Dynamics 365 Finance 1096-formularen? 

Dynamics 365 Finance udskriver ikke 1096 Annual Summary and Transmittal of US Information Returns-formularen.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Kreditor: 1099 – Findes der nye funktioner, der understøtter 1099-rapportering for den offentlige sektor? 
Der er tilføjet en ny funktion til den offentlige sektor, **Opdater 1099-oplysninger efter hovedkonto**, som du kan aktivere i arbejdsområdet til **Funktionsstyring**. Med denne funktion kan du tilknytte 1099-værdierne for en kreditor til hovedkontoen i regnskabsfordelingen og ikke standardkontoen i kreditorposten.

Du kan finde flere oplysninger i [Konfigurere kreditorer til 1099-rapportering](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
