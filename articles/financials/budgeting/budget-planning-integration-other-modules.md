---
title: "Integration af budgetplanlægning med andre moduler"
description: "Budgetplaner kan oprettes fra flere forskellige ressourcer. De grundlæggende elementer i den periodiske proces er ens for alle ressourcer."
author: twheeloc
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanGenerate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 64443
ms.assetid: f9a94db5-906c-404a-9ca5-91528d67c490
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: f50e58d63a9db4d6a8b5390174e2c7b87970717d
ms.contentlocale: da-dk
ms.lasthandoff: 01/17/2018

---

# <a name="budget-planning-integration-with-other-modules"></a>Integration af budgetplanlægning med andre moduler

[!include[banner](../includes/banner.md)] Budgetplaner kan oprettes fra flere forskellige ressourcer. De grundlæggende elementer i den periodiske proces er ens for alle ressourcer. 



<a name="periodic-processes-for-generating-budget-plans"></a>Periodiske processer til at generere budgetplaner
----------------------------------------------

Budgetplaner kan oprettes fra følgende ressourcer:

-   Finansposteringer
-   Anlægsaktiver
-   Budgetterede stillinger
-   Projektprognoser
-   Forsyningsprognoser
-   Behovsprognoser
-   Budgetposteringer
-   Andre budgetplaner

De grundlæggende elementer i den periodiske proces er ens for alle processer. Med faner kan du angive kilden for dataene, målattributter (budgetplan) og muligheder for at køre processen i baggrunden som en batchproces. Senere afsnit i denne artikel beskriver de varer, der ikke er synlige i hver proces.

### <a name="actions"></a>Aktioner

For hver oprettelsesproces findes tre handlinger:

-   **Opret en ny budgetplan** opretter en ny plan, der har de attributter, der er valgt i sektionen **Mål**. Disse attributter behøver ikke at være entydige. De to planer kan derfor have samme navn og andre værdier.
-   **Erstat det eksisterende budgetplanscenarie** sletter alle data i målbudgetplanen i det valgte budgetplanscenarie og opretter nye linjer, der bruger de valgte kildedata.
-   **Opdater det eksisterende budgetplansscenarie, og tilføj nye data** opdaterer eksisterende linjer i den målplan, der matcher kildelinjerne, og tilføjer nye linjer til nye data. Matchprocessen er baseret på finansdatoen, budgetklassen og forskellige andre felter. Når du for eksempel genererer budgetplaner fra prognosepositioner, er stillingsnummeret et vigtigt felt. Alle linjer, der har et stillingsnummer, der svarer til kildestillingsnummeret, erstattes med de nye linjer fra kilden.

### <a name="source"></a>Kilde

For alle processer kan du under fanen **Kilde** filtrere data ved hjælp af knappen **Filter**. Som standard føjes specifikke felter til filteret for hver proces. For eksempel er processen **Generér budgetplan fra finanskonto**, kategorierne **Finanskonto** og **Hovedkonto** tilgængelige og vises på oprettelsessiden. Alle de felter, du føjer til filteret, føjes også til siden sammen med de kriterier, du tilføjer.

### <a name="target"></a>Målsætning

Indstillingen **Historisk** under fanen **mål** gør det muligt at bruge datoerne fra kildedatene som ikrafttrædelsesdatoen i budgetplanen. Ikrafttrædelsesdatoen skal typisk være inden for planens budgetcyklus. Når du angiver indstillingen **Historisk** til **Ja**, bruges kildens dato (selv året), så du kan bruge tidligere data som grundlag for sammenligning. Du kan ikke ændre historiske data i budgetplanen, og planen er indstillet til en godkendt arbejdsgangsstatus. Men du kan nulstille statussen, hvis andre scenarier i planen skal ændres.

Feltet **Aggreger total efter** øverst på siden bestemmer også den dato, der bruges. Dette felt laver en total på beløbene og kan også angive ikrafttrædelsesdatoen til den første dag i regnskabsåret eller regnskabsperioden. 

Mange af felterne på fanen **Mål** bliver redigerbare eller skrivebeskyttede, afhængigt af den handling, du vælger. Når du går fra at oprette en ny budgetplan til at opdatere en eksisterende plan, bliver feltet **Navn på budgetplan** utilgængeligt, og de felter, der er relateret til valg af en eksisterende plan, bliver tilgængelige. Både under fanen **Mål** og **Kilde** bliver feltet **Finans** altid utilgængeligt, da værdien bestemmes af den valgte budgetplanlægningsproces. 

Feltet **Budgetklasse** gør det muligt at angive budgetplanlinjerne som enten udgiftsposteringer eller indtægtsposteringer. Normalt er indtægtsposteringer krediteringer til en finanskonto og gemmes derfor som negative beløb. Disse posteringer vises typisk også som negative beløb i budgetplanen. Ved at tilføje budgetklassen som et felt i planlayoutet kan du lade omsætning blive vist som positive beløb.

### <a name="generation-rules"></a>Genereringsregler

Tre felter indeholder yderligere funktioner: **Faktor**, **Minimum** og **Afrundings** **regel**. 

Værdien i feltet **Faktor** ganges med kildebeløbet for at angive beløbet i budgetplanen. Du kan derefter foretage justeringer, når du opretter budgetplanlinjer. Du kan f.eks. angive **1,03** for en stigning på 3 procent. Faktoren skal være et positivt tal. 

Feltet **Minimum** gør det muligt at indstille grænsebeløbet for oprettelse af en budgetplanlinje. Hvis kildebeløbet er mindre end dette antal, er budgetplanlinjen ikke oprettet. En værdi på **0,00** tillader alle beløb, men begrænser ikke linjer til positive beløb. (Ingen værdi begrænser linjer til positive beløb. Negative beløb medtages altid og repræsenterer normalt kreditposter).

Feltet **Afrundingsregel** gør det muligt at angive, hvor præcise de budgetplaner, der oprettes, skal være. Du kan afrunde valutabeløb til nærmeste hele 1,00, 10,00, 100,00 og så fremdeles.

## <a name="notes-for-specific-processes"></a>Bemærkninger til bestemte processer
### <a name="generate-budget-plan-from-general-ledger"></a>Generér budgetplan fra finanskonto

Når du opretter en budgetplan fra finansdata, skal du angive feltet **Aggreger total efter** til **Regnskabsår**, hvis indstillingen **Historisk** er angivet til **Nej**. Perioder og datoer i kilden stemmer muligvis ikke overens med perioderne angivet med datoer i målet. Da processen ikke har en sikker metode til at tilknytte disse værdier, skal du begrænse processen til først på året. 

I målet er feltet **Budgetklasse** indstillet til enten **Udgift** eller **Indtægter**. Denne indstilling bruges til at vælge **Budgettype**-attribut for linjer, der oprettes, når hovedkontoen på en linje ikke er af typen **Indtægter** eller **Udgift**.

### <a name="generate-budget-plan-from-fixed-assets"></a>Generér budgetplan fra anlægsaktiver

Processen **Generér budgetplan fra anlægsaktiver** har ingen valgmulighed for aggregering efter periode eller dag. Der er heller ingen indstilling til angivelse af planen som historisk. Du kan bruge denne periodiske proces til at medtage budgetterede anlægstransaktioner i din budgetplanlægning.

### <a name="generate-budget-plan-from-forecast-positions"></a>Opret budgetplaner fra budgetpositioner

Processen **Opret budgetplaner fra budgetpositioner** tildeler kildeprognosestillingen til budgetplanlinjen. Du kan få vist positionen ved at tilføje prognosestillingen som en række i budgetplanlayoutet eller ved at bruge forespørgslen **Budgetplanlinjer**. Hvis du ikke ønsker, at prognosestillingen skal knyttes til budgetplanlinjer, skal du angive indstillingen **Medtag stilling på budgetplanlinje** til **Nej**.

Linjerne i budgetplanen samles efter finanskonto og position. Dog kan du udelukke positionsnummer, så linjerne kun samles efter finanskonto. På fanen **Mål** skal du angive indstillingen **Medtag stilling på budgetplanlinje** til **Nej**.

I feltet **Budgetplansscenarie for fuldtid** kan du vælge et scenarie for at medtaget antallet af fuldtidsækvivalenter (fuldtidsmedarbejdere) i budgetplanen. Dette felt er begrænset til scenarier med antal, der findes i layoutet for målbudgetplanen. Hvis du vælger et scenarie med fuldtidsækvivalenter, skal du også vælge en hovedkonto med fuldtidsækvivalenter. Denne konto bruges til at oprette budgetplanlinjer med antal. 

Den budgetplanlægningsproces og det budgetplanscenarie, der er valgt i kilden, angiver budgetplanlægningsprocessen og scenariet for målscenariet. Da disse attributter tildeles til prognosestillinger, skal de svare til budgetplanen. Disse attributter kan derfor ikke ændres på målet.

### <a name="generate-budget-plan-from-project-forecasts"></a>Opret budgetplan fra projektprognoser

Processen **Opret budgetplan fra projektprognoser** har ligesom processen **Opret budgetplaner fra budgetpositioner** en mulighed for at medtage projektantal (timer, udgifter og varer) i et scenarie med antal. De to processer har også lignende filtre for kolonnerne i budgetplanlayoutet. 

Under fanen **Kilde** bestemmer de tre indstillinger i sektionen **Inkluder udtog**, hvilke budgetplanlinjer der oprettes. Disse indstillinger er de samme som de indstillinger, der er tilgængelige, når du opretter budgetregisterposter direkte fra projektprognoser. Angiv indstillingen **Drift** til **Ja** for at oprette linjer til omkostninger og indtægter. Angiv indstillingen **WIP** til **Ja** for at oprette arbejde i procesposter. Angiv indstillingen **Lønfordeling** til **Ja** for at oprette linjer for modkonti for løn for timeposteringer. 

Feltet **Budgetklasse** er der ikke, fordi budgetklassen (**Udgift** eller **Indtægter**) bestemmes af kilden. 

Du kan bruge projektbudgetter som kilde ved at vælge den prognosemodel, der indeholder projektbudgetbeløb. Husk, at projektbudgetter opretter projektprognoseposter, når de er godkendt.

Hvis du kun vælger omkostninger eller indtægter for budgetplanlinjer, skal du bruge filtret til at vælge **Budgetopdateringer: Beløbsstype = Omkostning**. Hvis du kun vil vælge én type prognose, skal du bruge filtret til at vælge **Budgetopdateringer: Transaktionstype = *xxx***. 

Kun én prognosemodel kan bruges til at oprette et budgetplansscenarie. Hvis du kører processen for en prognosemodel og derefter foretager en opdatering og prøver at angive en anden model, overskrives den første model, hvis det samme projekt og de samme finanskonti gælder. Hvis du vil generere et budgetplanscenarie fra mere end én prognosemodel, skal du generere ind i forskellige budgetplanscenarier og bruge fordelingsindstillinger til at lægge dem sammen i et andet scenarie. 

Processen **Opret budgetplan fra projektprognoser** tildeler også kildeprojektet til budgetplanlinjen.

### <a name="generate-budget-plan-from-supply-forecast"></a>Opret budgetplan fra forsyningsprognose

Kildefilterindstillingerne i processen **Opret budgetplan fra forsyningsprognose** blev modelleret efter indstillingerne i funktionen **Overføre købsbudget til finans**  på grund af ligheden mellem processen og funktionen.

### <a name="generate-budget-plan-from-demand-forecast"></a>Oprette budgetplan fra behovsprognose

For processen **Opret budgetplan fra behovsprognoser** kan du angive indstillingen **Salgsordre** til **Ja** for at generere indtægtslinjer i budgetplanen, angive **fForbrug** til **Ja** for at oprette udgiftslinjer eller angive begge indstillinger til **Ja**.

### <a name="generate-budget-plan-from-budget-register-entries"></a>Opret budgetplan ud fra budgetregisterpostposter

For processen **Opret budgetplan ud fra budgetregisterpostposter** skal kilden angive en undermodel, en budgetkode og et posteringsnummer. Med andre ord kan du kun oprette budgetlinjer for én budgetregisterpost ad gangen. Du kan bruge yderligere poster i samme budgetplan ved at køre processen én gang for hver kildepostering.

### <a name="generate-budget-plan-from-budget-plan"></a>Opret budgetplan fra budgetplan

Når det gælder processen **Opret budgetplan fra budgetplan**, giver et ekstra sæt indstillinger under fanen **Mål** mulighed for at tildele nye økonomiske dimensioner. Hvis en økonomisk dimension er markeret, bruges værdien for alle budgetplanlinjer. Du kan derfor bruge en budgetplan som grundlag for andre budgetplaner, men kan også tildele eksempelvis en anden afdeling eller bærer til de nye budgetplaner.

## <a name="looking-back-from-the-budget-plan"></a>Se tilbage fra budgetplanen
### <a name="budget-plans-by-dimension-set-inquiry"></a>Forespørgsel om budgetplaner efter dimensionssæt

Forespørgslen **Budgetplaner efter dimensionssæt** har flere indstillinger, der gør det muligt at køre en forespørgsel for at identificere kilden til budgetplansdataene. 

Marker en linje, og klik på knappen **Budgetplanlinjer** for at køre forespørgslen **Budgetplanlinjer**. Resultaterne filtreres for dimensionsværdierne på den valgte linje. Du kan derefter anvende yderligere parametre. 

Brug knapperne **Forsyningsprognose** og **Behovsprognose** til at køre disse forespørgsler. I begge tilfælde søger forespørgslen efter prognoselinjer, der kunne have oprettet budgetplanlinjerne. 

Yderligere rapporter, der er tilgængelige, omfatter rapporten **Budgetpositioner efter budgetplan**. Denne rapport er især nyttig, når du vil finde ud af, om en position er blevet allokeret korrekt til budgetplaner.




