---
title: Konfigurere behovsprognoser
description: Denne artikel omhandler de konfigurationsopgaver, du skal udføre, for at forberede behovsprognoser.
author: t-benebo
ms.date: 11/23/2021
ms.topic: article
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10a211e0e20f22dfbfdb4923841808750b6ed71b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900996"
---
# <a name="demand-forecasting-setup"></a>Konfigurere behovsprognoser

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du konfigurerer behovsprognose.  

## <a name="item-allocation-keys"></a>Varefordelingsnøgler

Varefordelingsnøgler opretter varegrupper. En behovsprognose beregnes kun for en vare og dens dimensioner, hvis varen er en del af en varefordelingsnøgle. Denne regel håndhæves for at gruppere et stort antal varer, så der hurtigere kan oprettes behovsprognoser. Prognoser oprettes udelukkede ud fra historiske data.

En vare og dens dimensioner må kun være en del af én varefordelingsnøgle, hvis varefordelingsnøglen anvendes under prognoseoprettelsen.

Hvis du vil oprette varefordelingsnøgler og føje en lagerenhed (SKU) til dem, skal du følge disse trin.

1. Gå til **Varedisponering \> Konfiguration \> Behovsprognose \> Varefordelingsnøgler**.
1. Vælg enten en varefordelingsnøgle i listeruden, eller vælg **Ny** i handlingsruden for at oprette en ny. Udfyld følgende felter i hovedet for den nye eller valgte nøgle:

    - **Varefordelingsnøgle** – Angiv et entydigt navn til nøglen.
    - **Navn** – Angiv et sigende navn til nøglen.

1. Benyt et af disse trin for at føje varer til den valgte varefordelingsnøgle eller fjerne varer:

    - Brug knapperne **Ny** og **Slet** på værktøjslinjen under fanen **Varefordeling** til at tilføje og fjerne varer efter behov. Vælg varenummeret for hver række, og tildel derefter dimensionsværdier i de andre kolonner efter behov. Vælg **Vis dimensioner** på værktøjslinjen for at ændre det sæt dimensionskolonner, der vises i gitteret. (Værdien i kolonnen **Procent** ignoreres, når behovsprognoser genereres).
    - Hvis du vil føje et stort antal varer til nøglen, skal du vælge **Tildel varer** i handlingsruden for at åbne en side, hvor du kan finde og tildele flere varer til den valgte nøgle.

> [!IMPORTANT]
> Pas på kun at medtage relevante varer i hver varefordelingsnøgle. Unødvendige varer kan medføre øgede omkostninger, når du bruger Microsoft Azure Machine Learning.

## <a name="intercompany-planning-groups"></a>Interne planlægningsgrupper

Behovsprognoser kan generere prognoser på tværs af firmaet. I Dynamics 365 Supply Chain Management grupperes firmaer, der er planlagt sammen, i den samme interne planlægningsgruppe. For at angive for hvert firma, hvilke varefordelingsnøgler der skal tages i betragtning til behovsprognose, skal du knytte en varefordelingsnøgle til medlemmet af den interne planlægningsgruppe.

> [!IMPORTANT]
> Planlægningsoptimering understøtter i øjeblikket ikke interne planlægningsgrupper. Hvis du vil udføre intern planlægning, der bruger planlægningsoptimering, skal du konfigurere varedisponeringsbatchjob, der omfatter behovsplaner for alle relevante firmaer.

Benyt følgende fremgangsmåde for at konfigurere dine interne planlægningsgrupper.

1. Gå til **Varedisponering \> Opsætning \> Interne planlægningsgrupper**.
1. Vælg enten en planlægningsgruppe i listeruden, eller vælg **Ny** i handlingsruden for at oprette en ny. Udfyld følgende felter i hovedet for den nye eller valgte gruppe:

    - **Navn** – Angiv et entydigt navn til planlægningsgruppen.
    - **Beskrivelse** – Indtast en kort beskrivelse af planlægningsgruppen.

1. I oversigtspanelet **Medlemmer af interne planlægningsgrupper** kan du bruge knapperne på værktøjslinjen til at tilføje en række for hvert firma (juridisk enhed), der skal være en del af gruppen. På hver række skal du angive følgende felter:

    - **Juridisk enhed** – Vælg navnet på et firma (juridisk enhed), der er medlem af den valgte gruppe.
    - **Planlægningsrækkefølge** – Tildel den rækkefølge, hvori firmaet skal behandles i forhold til andre firmaer. De laveste værdier behandles først. Denne rækkefølge kan være vigtig, når efterspørgslen for ét firma påvirker andre firmaer. I disse tilfælde skal det firma, der leverer behovet, behandles til sidst.
    - **Behovsplan** – Vælg den behovsplan, der skal udløses for det aktuelle firma.
    - **Kopiér automatisk til statisk plan** – Markér dette afkrydsningsfelt for at kopiere planens resultat til den statiske plan.
    - **Kopiér automatisk til dynamisk plan** – Markér dette afkrydsningsfelt for at kopiere planens resultat til den dynamiske plan.

1. Hvis der ikke tildeles nogen varefordelingsnøgler til medlemmer af den interne planlægningsgruppe, beregnes en behovsprognose for alle varer, der er knyttet til alle varefordelingsnøgler fra alle firmaer. Der findes yderligere filtreringsindstillinger for firmaer og varefordelingsnøgler i dialogboksen **Generér statistisk budgetgrundlag** (**Varedisponering \> Budgettering \> Behovsprognose \> Generér statistisk budgetgrundlag**). Hvis du vil tildele varefordelingsnøgler til et firma i den valgte interne planlægningsgruppe, skal du vælge firmaet og derefter vælge **Varefordelingsnøgler** på værktøjslinjen i oversigtspanelet **Medlemmer af interne planlægningsgrupper**.

> [!IMPORTANT]
> Sørg for kun at medtage relevante varefordelingsnøgler i hver interne planlægningsgruppe. Unødvendige varer kan medføre øgede omkostninger, når du bruger Azure Machine Learning.

## <a name="set-up-demand-forecasting-parameters"></a><a name="parameters"></a>Konfigurere parametre til behovsprognose

Brug siden **Parametre til behovsprognoser** til at konfigurere flere indstillinger, der styrer, hvordan behovsprognose fungerer i systemet.

### <a name="open-the-demand-forecasting-parameters-page"></a>Åbn siden Parametre til behovsprognoser

Hvis du vil konfigurere parametre for behovsprognoser, skal du gå til **Varedisponering \> Konfiguration \> Behovsprognoser \> Parametre til behovsprognoser**. Da behovsprognoser kører på tværs af firmaet, er konfigurationen global. Med andre ord gælder konfigurationen for alle juridiske enheder (firmaer).

### <a name="general-settings"></a>Generelle indstillinger

Brug fanen **Generelt** på siden **Parametre til behovsprognoser** til at definere generelle indstillinger for behovsprognose.

#### <a name="demand-forecast-unit"></a>Behovsprognoseenhed

Behovsprognose genererer prognosen i antal. Måleenheden, antallet skal udtrykkes i, skal derfor angives i feltet **Behovsprognoseenhed**. Dette felt definerer den enhed, der bruges til alle behovsprognoser, uanset hvilken lagerenhed der normalt anvendes til hvert produkt. Hvis du bruger en konsekvent prognoseenhed, er det med til at sikre, at aggregering og procentvis fordeling giver mening. Få flere oplysninger om aggregering og procentvis fordeling under [Foretage manuelle justeringer af prognosegrundlaget](manual-adjustments-baseline-forecast.md).

Når det gælder hver måleenhed, der bruges til lagerenheder, der er inkluderet i behovsprognose, skal du sørge for, at der er en omregningsregel for måleenheden og den generelle måleenhed for prognoser, som du vælger her. Når du opretter en prognose, logføres listen over varer, der ikke har omregning af måleenhed. Derfor er det nemt at rette opsætningen. Du kan finde flere oplysninger om måleenheder, og hvordan du konverterer dem, i [Administrere måleenheder](../pim/tasks/manage-unit-measure.md).

#### <a name="transaction-types"></a>Posteringstyper

Brug felterne i oversigtspanelet **Transaktionstyper** til at vælge de transaktionstyper, der bruges, når det statistiske budgetgrundlag genereres.

Behovsprognoser kan bruges til at lave prognoser om både afhængigt behov og uafhængigt behov. Hvis f.eks. kun **Salgsordre** er indstillet til *Ja*, og alle de varer, der tages i betragtning i forhold til behovsprognose, er varer, der sælges, beregner systemet uafhængigt behov. De kritiske underkomponenter kan imidlertid føjes til varefordelingsnøgler og medtages i behovsprognoser. Hvis indstillingen **Produktionslinje** er angivet til *Ja* i dette tilfælde, beregnes en behovsprognose.

Du kan tilsidesætte transaktionstyper for en eller flere specifikke varefordelingsnøgler ved at bruge fanen **Varefordelingsnøgler**. Denne fane indeholder lignende felter.

#### <a name="choose-how-to-create-the-baseline-forecast"></a>Vælg, hvordan prognosegrundlaget skal oprettes

I feltet **Strategi for generering af prognose** kan du vælge den metode, der skal bruges til at oprette et prognosegrundlag. Der er tre tilgængelige metoder:

- *Kopiér over historisk efterspørgsel* – Opret prognoser ved blot at kopiere historikdata.
- *Azure Machine Learning Service* – Brug en prognosemodel, der bruger Azure Machine Learning Service. Azure Machine Learning Service er den aktuelle løsning til maskinel indlæring for Azure. Det anbefales derfor, at du bruger den, hvis du vil bruge en prognosemodel.
- *Azure Machine Learning* – Brug en prognosemodel, der bruger Azure Machine Learning Studio (klassisk). Azure Machine Learning Studio (klassisk) er udfaset og vil snart blive fjernet fra Azure. Det anbefales derfor, at du vælger *Azure Machine Learning Service*, hvis du konfigurerer behovsprognose for første gang. Hvis du i øjeblikket bruger Azure Machine Learning Studio (klassisk), skal du planlægge at skifte til Azure Machine Learning Service så hurtigt som muligt.

Du kan tilsidesætte prognosegenereringsmetoden for en eller flere specifikke varefordelingsnøgler ved at bruge fanen **Varefordelingsnøgler**. Denne fane indeholder lignende felter.

#### <a name="override-default-forecast-algorithm-parameters-globally"></a>Tilsidesæt standardparametre for prognosealgoritme globalt

Parametre og værdier for standardprognosealgoritmer tildeles på siden **Parametre til behovsprognoser** (**Varedisponering \> Konfiguration \> Behovsprognoser \> Parametre til behovsprognoser**). Du kan dog tilsidesætte dem globalt ved hjælp af oversigtspanelet **Parametre til prognosealgoritme** under fanen **Generelt** på siden **Parametre til behovsprognosee**. (Du kan også tilsidesætte dem for bestemte fordelingsnøgler ved at bruge fanen **Varefordelingsnøgler** på siden **Parametre til behovsprognoser**).

Brug knapperne **Tilføj** og **fjern** på værktøjslinjen til at fastlægge den nødvendige samling parametertilsidesættelser. For hver parameter på listen skal du vælge en værdi i feltet **Navn** og derefter angive en relevant værdi i feltet **Værdi**. Alle de parametre, der ikke vises her, tager deres værdier fra indstillingerne på siden **Parametre til behovsprognoser**. Yderligere oplysninger om, hvordan du bruger standardsættet af parametre og vælger værdier til dem, finder du i afsnittet [Standardparametre og -værdier for behovsprognosemodeller](#model-parameters).

### <a name="set-forecast-dimensions"></a>Angiv prognosedimensioner

En prognosedimension angiver det detaljeniveau, prognosen er defineret for. Firma, lokation og varefordelingsnøgle er påkrævede prognosedimensioner. Du kan også oprette prognoser ud fra lagersted, lagerstatus, debitorgruppe, debitorkonto, land/område, delstat og/eller vareniveau plus alle varedimensionsniveauer. Brug fanen **Prognosedimensioner** på siden **Parametre til behovsprognoser** til at vælge sættet af prognosedimensioner, der skal bruges, når der oprettes behovsprognoser.

Du kan når som helst tilføje prognosedimensioner til listen over dimensioner, der bruges til behovsprognoser. Du kan også fjerne prognosedimensioner fra listen. Manuelle justeringer går dog tabt, hvis du tilføjer eller fjerner en prognosedimension.

### <a name="set-up-overrides-for-specific-item-allocation-keys"></a>Konfigurere tilsidesættelser for bestemte varefordelingsnøgler

Det er ikke alle varer, der fungerer på samme måde, set ud fra en behovsprognose. Du kan derfor oprette fordelingsnøglespecifikke tilsidesættelser for de fleste af de indstillinger, der er defineret under fanen **Generelt**. Undtagelsen er enheden for behovsprognosen. Hvis du vil konfigurere tilsidesættelser for en bestemt varefordelingsnøgle, skal du følge disse trin.

1. På siden **Parametre til behovsprognoser** skal du under fanen **Varefordelingsnøgler** bruge knapperne på værktøjslinjen til at føje varefordelingsnøgler til gitteret i venstre side eller fjerne dem efter behov. Vælg derefter den fordelingsnøgle, du vil konfigurere tilsidesættelser for.
1. I oversigtspanelet **Transaktionstyper** kan du aktivere de transaktionstyper, du vil bruge til at generere det statistiske budgetgrundlag for produkter, der tilhører den valgte fordelingsnøgle. Indstillingerne fungerer på samme måde som under fanen **Generelt**, men de gælder kun for den valgte varefordelingsnøgle. Alle indstillinger her (både *Ja*- og *Nej*-værdier) tilsidesætter alle indstillinger af **Transaktionstyper** under fanen **Generelt**.
1. I oversigtspanelet **Parametre til prognosealgoritme** skal du vælge den strategi for generering af prognose og parameteren for prognosealgoritmer, der tilhører den valgte fordelingsnøgle. Indstillingerne fungerer på samme måde som under fanen **Generelt**, men de gælder kun for den valgte varefordelingsnøgle. Brug knapperne **Tilføj** og **fjern** på værktøjslinjen til at definere den nødvendige samling parametertilsidesættelser. For hver parameter på listen skal du vælge en værdi i feltet **Navn** og derefter angive en relevant værdi i feltet **Værdi**. Yderligere oplysninger om, hvordan du bruger standardsættet af parametre og vælger værdier til dem, finder du i afsnittet [Standardparametre og -værdier for behovsprognosemodeller](#model-parameters).

### <a name="set-up-the-connection-to-the-azure-machine-learning-service"></a>Oprette forbindelse til Azure Machine Learning Service

Brug fanen **Azure Machine Learning Service** til at oprette forbindelse til Azure Machine Learning Service. Denne løsning er en af indstillingerne til oprettelse af prognosegrundlaget. Disse indstillinger under denne fane gælder kun, når feltet **Strategi for generering af prognose** er angivet til *Azure Machine Learning Service*.

Yderligere oplysninger om, hvordan du konfigurerer Azure Machine Learning Service og derefter bruger indstillingerne her til at oprette forbindelse til den, finder du i afsnittet [Konfigurere Azure Machine Learning Service](#setup-amls).

### <a name="set-up-the-connection-to-azure-machine-learning-studio-classic"></a>Oprette forbindelse til Azure Machine Learning Studio (klassisk)

> [!IMPORTANT]
> Azure Machine Learning Studio (klassisk) er udfaset. Derfor kan du ikke længere oprette nye arbejdsområder til det i Azure. Den er blevet erstattet af Azure Machine Learning Service, der giver lignende funktionalitet og meget mere. Hvis du ikke allerede bruger Azure Machine Learning, skal du begynde at bruge Azure Machine Learning Service. Hvis du allerede har et arbejdsområde, der er oprettet til Azure Machine Learning Studio (klassisk), kan du fortsætte med at bruge det, indtil funktionen er helt fjernet fra Azure. Det anbefales dog, at du opdaterer til Azure Machine Learning Service så hurtigt som muligt. Selvom programmet fortsætter med at advare dig om, at Azure Machine Learning Studio (klassisk) er udfaset, påvirkes prognoseresultatet ikke. Yderligere oplysninger om den nye Azure Machine Learning Service og dens konfiguration finder du i afsnittet [Konfigurere Azure Machine Learning Service](#setup-amls).
>
> Du kan frit skifte mellem at bruge nye og gamle løsninger til maskinel indlæring med Supply Chain Management, så længe dit gamle arbejdsområde i Azure Machine Learning Studio (klassisk) forbliver tilgængeligt.

Hvis du allerede har et tilgængeligt arbejdsområde i Azure Machine Learning Studio (klassisk), kan du bruge det til at generere prognoser ved at knytte det til Supply Chain Management. Du kan oprette denne forbindelse ved at bruge fanen **Azure Machine Learning** på siden **Parametre til behovsprognoser**. (Indstillingerne under denne fane gælder kun, når feltet **Strategi for generering af prognose** er indstillet til *Azure Machine Learning*). Angiv følgende oplysninger for arbejdsområdet i Azure Machine Learning Studio (klassisk):

- Webtjeneste-API-nøglen (application programming)
- URL-adresse til webtjenesteslutpunkt
- Kontonavn på Azure-lager
- Nøgle til Azure-lagerkonto

> [!NOTE]
> Navn og nøgle til Azure-lageret er kun påkrævet, hvis du bruger en brugerdefineret lagerkonto. Hvis du installerer den lokale version, skal du have en brugerdefineret lagerkonto i Azure, så Machine Learning kan få adgang til de historiske data.

## <a name="default-parameters-and-values-for-demand-forecasting-models"></a><a name="model-parameters"></a>Standardparametre og -værdier for modeller til behovsprognose

Når du bruger maskinel indlæring til at generere dine prognoseplanlægningsmodeller, kan du styre indstillinger for maskinel indlæring ved at angive værdier for *prognosealgoritmeparametre*. Disse værdier sendes fra Supply Chain Management til Azure Machine Learning. Brug siden **Parametre til prognosealgoritme** til at styre, hvilke typer værdier der skal angives, og hvilke værdier hver enkelt skal have.

Du kan konfigurere standardparametre og -værdier til modeller for behovsprognoser ved at gå til **Varedisponering \> Konfiguration \> Behovsprognoser \> Parametre til prognosealgoritme**. Der er angivet et standardsæt af parametre. Hver parameter har følgende felter:

- **Navn** – Navnet på parameteren, som bruges af Azure. Normalt bør du ikke ændre dette navn, medmindre du har tilpasset eksperimentet i Azure Machine Learning.
- **Beskrivelse** – Et almindeligt navn til parameteren. Dette navn bruges til at identificere parameteren andre steder i systemet (f.eks. på siden **Parametre til behovsprognose**).
- **Værdi** – Standardværdien for parameteren. Den værdi, du skal angive, afhænger af den parameter, du redigerer. 
- **Forklaring** – En kort beskrivelse af parameteren, og hvordan den bruges. Denne beskrivelse indeholder typisk et råd om gyldige værdier i feltet **Værdi**.

Følgende parametre er som standard angivet. (Hvis du skal vende tilbage til standardlisten, skal du vælge **Gendan** i handlingsruden).

- **Konfidensniveau i procent** - Et konfidensinterval består af en række værdier, der fungerer som gode estimater for behovsprognosen. En konfidensinternval på 95 % angiver, at der er 5 % risiko for, at det fremtidige behov falder uden for konfidensintervallet.
- **Gennemtving sæsonudsving** - Angiver, om modellen skal tvinges til at bruge en bestemt type sæsonudsving. Denne parameter gælder kun for ARIMA og ETS. Indstillinger: *AUTO (standard)*, *NONE*, *ADDITIVE*, *MULTIPLICATIVE*.
- **Prognosemodel** – Angiver, hvilken prognosemodel der skal bruges. Indstillinger: *ARIMA*, *ETS*, *STL*, *ETS+ARIMA*, *ETS+STL*, *ALL*. Du får den mest velegnede model, hvis du bruger *ALL*.
- **Maks. budgetteret værdi** - Angiver den maksimale værdi, der skal bruges til forudsigelser. Format: + 1E [n] eller numerisk konstant.
- **Min. budgetteret værdi** - Angiver den mindste værdi, der skal bruges til forudsigelser. Format: -1E[n] eller numerisk konstant.
- **Erstatning af manglende værdi** - Angiver, hvordan huller i historiske data skal udfyldes. Indstillinger: *(numerisk værdi)*, *MEAN*, *PREVIOUS*, *INTERPOLATE LINEAR*, *INTERPOLATE POLYNOMIAL*.
- **Erstatning af manglende værdi** - Angiver, om værdierstatningen kun gælder for datoområdet for hver enkelt granularitetsattribut eller for hele datasættet. Følgende indstillinger er tilgængelige til fastlæggelse af det datointerval, som systemet bruger, når der udfyldes huller i historikdata:

    - *GLOBAL* – Systemet bruger det fulde interval af datoer for alle granularitetsattributter.
    - *HISTORY_DATE_RANGE* – Systemet bruger et bestemt datointerval, der er defineret af felterne **Fra dato** og **Til dato** i sektionen **Historisk i tidshorisont** i dialogboksen **Generér statistisk budgetgrundlag**.
    - *GRANULARITY_ATTRIBUTE* – Systemet bruger datointervallet for den aktuelt behandlede granularitetsattribut.

    > [!NOTE]
    > En granularitetsattribut er en kombination af budgetdimensioner, som budgettet udføres i forhold til. Du kan definere prognosedimensioner på siden **Parametre til behovsprognoser**.

- **Sæsonbetonet tip** - Til sæsonbetonede data skal du angive et tip til prognosemodellen for at øge prognosens nøjagtighed. Format: Heltal, der repræsenterer antallet af puljer, hvor et behovsmønster gentages. Angiv f.eks. *6* for data, der gentages hver sjette måned.
- **Testsætstørrelse i procent** - Procent af historiske data, der skal bruges som testsæt til beregning af prognosenøjagtighed.

Du kan overskrive værdierne af disse parametre ved at gå til **Varedisponering \> Konfiguration \> Efterspørgselsprognose \> Parametre for efterspørgselsprognose**. Du kan tilsidesætte disse parametre på følgende måder på siden **Parametre til behovsprognoser**.

- Brug fanen **Generelt** til at tilsidesætte parametrene globalt.
- Brug fanen **Varefordelingsnøgler** til at tilsidesætte parametrene for hver varefordelingsnøgle. Parametre, der er tilsidesat for en bestemt varefordelingsnøgle, påvirker kun prognosen for varer, der er knyttet til denne varefordelingsnøgle.

> [!NOTE]
> På siden **Parametre for prognosealgoritme** kan du bruge knapperne i handlingsruden til at føje parametre til listen eller fjerne parametre fra listen. Normalt bør du dog ikke bruge denne metode, medmindre du har tilpasset eksperimentet i Azure Machine Learning.

## <a name="set-up-the-azure-machine-learning-service"></a><a name="setup-amls"></a>Oprette forbindelse til Azure Machine Learning Service

Supply Chain Management beregner behovsprognoser ved hjælp af Azure Machine Learning Service, som du skal oprette og køre på dit eget Azure-abonnement. I dette afsnit beskrives, hvordan du kan konfigurere Azure Machine Learning Service i Azure og derefter knytte den til dit Supply Chain Management-miljø.

### <a name="enable-the-azure-machine-learning-service-in-feature-management"></a>Aktivere Azure Machine Learning Service i funktionsstyring

Før du kan bruge Azure Machine Learning Service til behovsprognoser, skal du aktivere en funktion i Supply Chain Management for at muliggøre integrationen. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Varedisponering*
- **Funktionsnavn:** *Azure Machine Learning Service til behovsprognoser*

### <a name="set-up-machine-learning-in-azure"></a><a name="ml-workspace"></a>Konfigurere maskinel indlæring i Azure

Hvis du vil give Azure mulighed for at bruge maskinel indlæring til at behandle dine prognoser, skal du oprette et arbejdsområde til Azure Machine Learning til dette formål. Du har to muligheder:

- Hvis du vil konfigurere arbejdsområdet ved at køre et script fra Microsoft, skal du følge instruktionerne i afsnittet [Mulighed 1: Køre et script for automatisk at konfigurere dit arbejdsområde til maskinel indlæring](#ml-workspace-script) og derefter gå videre til afsnittet [Konfigurere Azure Machine Learning Service-forbindelser i Supply Chain Management](#demand-forecast-parameters).
- Hvis du vil konfigurere arbejdsområdet manuelt, skal du følge instruktionerne i afsnittet [Mulighed 2: Konfigurere dit arbejdsområde til maskinel indlæring manuelt](#ml-workspace-manual) og derefter gå videre til afsnittet [Konfigurere Azure Machine Learning Service-forbindelsesparametre i Supply Chain Management](#demand-forecast-parameters). Denne metode tager mere tid, men den giver dig mere kontrol.

#### <a name="option-1-run-a-script-to-automatically-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-script"></a>Mulighed 1: Køre et script for automatisk at konfigurere dit arbejdsområde til maskinel indlæring

I dette afsnit beskrives, hvordan du kan konfigurere arbejdsområdet til maskinel indlæring ved hjælp af et automatisk script, der leveres af Microsoft. Hvis du foretrækker det, kan du konfigurere alle ressourcer manuelt ved at følge instruktionerne i [Mulighed 2: Konfigurere dit arbejdsområde til maskinel indlæring manuelt](#ml-workspace-manual). Du behøver ikke fuldføre begge metoder.

1. På GitHub skal du åbne [Skabeloner til Dynamics 365 Supply Chain Management-behovsprognose med Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service)-lageret og hente følgende filer:

    - quick_setup.ps1
    - sampleInput.csv
    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. Åbn et PowerShell-vindue, og kør scriptet **quick_setup.ps1**, du hentede i det forrige trin. Følg vejledningen på skærmen. Scriptet konfigurerer det påkrævede arbejdsområde, lager, standarddatalageret og beregne ressourcer. Men du skal stadig oprette de nødvendige pipelines ved at følge de resterende trin i denne procedure. (Pipelines giver dig mulighed for at starte prognosescripts fra Supply Chain Management).
1. I Azure Machine Learning Studio skal du uploade filen **sampleInput.csv**, du hentede i trin 1, til den container, der hedder *demplan-azureml*. (Scriptet quick_setup.ps1 har oprettet denne container). Denne fil skal bruges til at publicere pipelinen og generere en testprognose. Yderligere oplysninger finder du under [Uploade en blok-blob](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob).
1. I Azure Machine Learning Studio skal du vælge **Notebooks** i navigatoren.
1. Find følgende placering i **Filer**-strukturen: **Brugere/\[aktuel bruger\]/src**.
1. Upload de resterende fire filer, du hentede i trin 1, til den placering, du fandt i det foregående trin.
1. Vælg filen **api_trigger.py**, du lige har uploadet, og kør den. Den opretter en pipeline, der kan udløses via API'en.
1. Arbejdsområdet er nu konfigureret. Gå videre til afsnittet [Konfigurere Azure Machine Learning Service-forbindelsesparametre i Supply Chain Management](#demand-forecast-parameters).

#### <a name="option-2-manually-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-manual"></a>Mulighed 2: Konfigurere dit arbejdsområde til maskinel indlæring manuelt

Dette afsnit indeholder en beskrivelse af, hvordan du manuelt kan konfigurere arbejdsområdet til maskinel indlæring. Du skal kun gennemføre procedurerne i dette afsnit, hvis du har valgt ikke at køre det automatiserede opsætningsscript som beskrevet i afsnittet [Mulighed 1: Køre et script for automatisk at konfigurere dit arbejdsområde til maskinel indlæring](#ml-workspace-script).

##### <a name="step-1-create-a-new-workspace"></a><a name="create-workspace"></a>Trin 1: Opret et nyt arbejdsområde

Brug følgende procedure til at oprette et nyt arbejdsområde til maskinel indlæring.

1. Log på din Azure-portal.
1. Åbn tjenesten **Maskinel indlæring**.
1. Vælg **Opret** på værktøjslinjen for at åbne guiden **Opret**.
1. Gennemfør guiden ved at følge instruktionerne på skærmen. Husk på følgende, mens du arbejder:

    - Brug standardindstillinger, medmindre andre punkter på listen anbefaler andre indstillinger.
    - Sørg for at vælge det geografiske område, der svarer til det område, hvor din forekomst af Supply Chain Management er udrullet. Ellers kan nogle af dataene passere gennem områdegrænser. Du kan finde flere oplysninger i afsnittet [Erklæring om beskyttelse af personlige oplysninger](#privacy) senere i denne artikel.
    - Brug dedikerede ressourcer som f.eks. ressourcegrupper, lagerkonti, containerregistre, Azure Key Vaults og netværksressourcer.
    - Angiv et navn til lagerkontoen på siden **Konfigurer Azure Machine Learning Service-forbindelsesparametre** i guiden. Brug en konto, der er dedikeret til behovsprognoser. In- og outputdata til behovsprognoser lagres på denne lagerkonto.

Du kan finde flere oplysninger i [Oprette arbejdsområdet](/azure/machine-learning/quickstart-create-resources#create-the-workspace).

##### <a name="step-2-configure-storage"></a><a name="config-storage"></a>Trin 2: Konfigurer lager

Benyt følgende fremgangsmåde til at konfigurere dit lager.

1. På GitHub skal du åbne [Skabeloner til Dynamics 365 Supply Chain Management-behovsprognose med Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service)-lageret og hente filen **sampleInput.csv**.
1. Åbn den lagerkonto, du oprettede i trin [1: Opret et nyt arbejdsområde](#create-workspace).
1. Følg instruktionerne i [Opret en container](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container) for at oprette en container, der kaldes *demplan-azureml*.
1. Upload filen **sampleInput.csv**, du hentede i trin 1, til den container, du lige har oprettet. Denne fil skal bruges til at publicere pipelinen og generere en testprognose. Yderligere oplysninger finder du under [Uploade en blok-blob](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob).

##### <a name="step-3-configure-a-default-datastore"></a>Trin 3: Konfigurer et standarddatalager

Benyt følgende fremgangsmåde til at konfigurere dit standarddatalager.

1. I Azure Machine Learning Studio skal du vælge **Datalagre** i navigatoren.
1. Opret et nyt datalager af typen *Azure Blob Storage*, der peger på den Blob Storage-container *demplan-azureml*, som du oprettede i [Trin 2: Konfigurer lager](#config-storage). (Hvis det nye datalagers godkendelsestype er *Kontonøgle*, skal du angive en kontonøgle for den oprettede lagerkonto. Du kan finde instruktioner under [Administrere adgangsnøgler til lagerkonto](/azure/storage/common/storage-account-keys-manage?tabs=azure-portal).
1. Gør dit nye datalager til standarddatalager ved at åbne detaljerne og vælge **Angiv som standarddatalager**.

##### <a name="step-4-configure-compute-resources"></a><a name="config-compute-resources"></a>Trin 4: Konfigurer beregningsressourcer

Benyt følgende fremgangsmåde for at konfigurere en beregningsressource i Azure Machine Learning Studio for at køre dine scripts til generering af prognoser.

1. Åbn detaljesiden for det arbejdsområde til maskinel indlæring, du oprettede i [Trin 1: Opret et nyt arbejdsområde](#create-workspace). Find værdien af **URL-adresse til Studio-websted**, og vælg linket for at åbne det.
1. Vælg **Beregn** i navigationsruden.
1. Under fanen **Beregn forekomster** skal du vælge **Ny** for at åbne en guide, der kan hjælpe dig med at oprette en ny beregningsforekomst. Følg vejledningen på skærmen. Beregningsforekomsten bruges til at oprette pipelinen til behovsprognose (den kan slettes, når pipeline er publiceret). Brug standardindstillingerne.
1. Under fanen **Beregn klynger** skal du vælge **Ny** for at åbne en guide, der kan hjælpe dig med at oprette en ny beregningsklynge. Følg vejledningen på skærmen. Beregningsklyngen bruges til at generere behovsprognoser. Dens indstillinger påvirker ydeevnen og det maksimale niveau for parallelisering af kørslen. Angiv følgende felter, men brug standardindstillingerne for alle andre felter:

    - **Navn** – Angiv *e2ecpucluster*.
    - **Virtuel maskinstørrelse** – Juster denne indstilling i overensstemmelse med mængden af data, du forventer at bruge som input til behovsprognose. Nodeantallet må ikke overstige 11, da der kræves én node for at udløse generering af behovsprognoser, og det maksimale antal noder, der derefter kan bruges til generering af en prognose, er 10. (Du skal også angive nodeantallet i filen parameters.py i [Trin 5: Opret pipelines](#create-pipelines)). På hver node vil der være flere arbejderprocesser, der kører prognosescripts parallelt. Det samlede antal arbejderprocesser i jobbet er *Antal kerner, som en node har* × *Nodeantal*. Hvis din beregningsklynge f.eks. har typen *Standard\_D4* (otte kerner) og maksimalt 11 noder, og hvis værdien af `nodes_count` er angivet til *10* i parameters.py-filen, er det effektive parallelitetsniveau 80.

##### <a name="step-5-create-pipelines"></a><a name="create-pipelines"></a>Trin 5: Opret pipelines

Pipelines giver dig mulighed for at starte prognosescripts fra Supply Chain Management. Brug følgende procedure til at oprette de nødvendige pipelines.

1. På GitHub skal du åbne [Skabeloner til Dynamics 365 Supply Chain Management-behovsprognose med Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service)-lageret og hente følgende filer:

    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. I Azure Machine Learning Studio skal du vælge **Notebooks** i navigatoren.
1. Find følgende placering i **Filer**-strukturen: **Brugere/\[aktuel bruger\]/src**.
1. Upload de fire filer, du hentede i trin 1, til den placering, du fandt i det foregående trin.
1. I Azure skal du åbne og gennemse filen **parameters.py**, du lige har uploadet. Sørg for, at værdien af `nodes_count` er mindre end den værdi, du har konfigureret til beregningsklyngen i [Trin 4: Konfigurer beregningsressourcer](#config-compute-resources). Hvis værdien af `nodes_count` er større end eller lig med antallet af noder i beregningsklyngen, kan pipeline-kørslen muligvis starte. Derefter holder den dog op med at svare, mens den venter på de nødvendige ressourcer. Yderligere oplysninger om nodeantal finder du i [Trin 4: Konfigurer beregningsressourcer](#config-compute-resources).
1. Vælg filen **api_trigger.py**, du lige har uploadet, og kør den. Den opretter en pipeline, der kan udløses via API'en.

### <a name="set-up-a-new-active-directory-application"></a><a name="aad-app"></a>Konfigurere et nyt Active Directory-program

Et Active Directory-program skal godkendes med de ressourcer, der er dedikeret til behovsprognoser, ved hjælp af tjenesteprincipal. Derfor skal programmet have det laveste rettighedsniveau, der kræves for at generere prognosen.

1. Log på din Azure-portal.
1. Registrer et nyt program i lejerens Azure Active Directory (Azure AD). Du kan finde flere oplysninger i [Sådan bruges portalen til at oprette en Azure AD-applikation og tjenesteportal, der kan få adgang til ressourcer](/azure/active-directory/develop/howto-create-service-principal-portal).
1. Gennemfør guiden ved at følge instruktionerne på skærmen. Brug standardindstillingerne.
1. Giv dit nye Active Directory-program adgang til følgende ressourcer, du har oprettet i afsnittet [Konfigurere maskinel indlæring i Azure](#ml-workspace). Du kan finde instruktioner under [Tildele Azure-roller ved hjælp af Azure-portalen](/azure/role-based-access-control/role-assignments-portal?tabs=current). Dette trin vil sætte systemet i stand til at importere og eksportere prognosedata og til at udløse pipeline for maskinel indlæring, der køres fra Supply Chain Management.

    - Bidragerrolle til arbejdsområde til maskinel indlæring
    - Bidragerrolle til den dedikerede lagerkonto
    - Bidragerrolle for Storage Blob-data til den dedikerede lagerkonto

1. I sektionen **Certifikater og hemmeligheder** i det program, du har oprettet, skal du oprette en hemmelighed til programmet. Yderligere oplysninger finder du under [Tilføje en klienthemmelighed](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret).
1. Notér dig program-id'et og dets hemmelighed. Du skal bruge detaljerne om dette program senere, når du konfigurerer siden **Parametre til behovsprognoser** i Supply Chain Management.

### <a name="set-up-azure-machine-learning-service-connection-parameters-in-supply-chain-management"></a><a name="demand-forecast-parameters"></a>Konfigurere Azure Machine Learning Service-forbindelsesparametre i Supply Chain Management

Benyt følgende fremgangsmåde til at forbinde dit Supply Chain Management-miljø til den Machine Learning-tjeneste, du lige har konfigureret i Azure.

1. Log på Supply Chain Management.
1. Gå til **Varedisponering \> Konfiguration \> Behovsprognose \> Parametre til behovsprognoser**.
1. Under fanen **Generelt** skal du kontrollere, at feltet **Strategi for generering af prognose** er angivet til *Azure Machine Learning Service*.
1. Under fanen **Varefordelingsnøgler** skal du kontrollere, at feltet **Strategi for generering af prognose** er angivet til *Azure Machine Learning Service* for hver fordelingsnøgle, der skal bruge Azure Machine Learning Service til behovsprognoser.
1. Angiv følgende felter under fanen **Azure Machine Learning Service**:

    - **Lejer-id** – Angiv dit lejer-id for Azure. Supply Chain Management bruger dette id til at blive godkendt i Azure Machine Learning Service. Du kan finde dit lejer-id på siden **Oversigt** for Azure AD på Azure-portalen.
    - **Program-id for tjenesteprincipal** – Angiv program-id'et for det program, du har oprettet i afsnittet [Active Directory-program](#aad-app). Denne værdi bruges til at godkende API-anmodninger til Azure Machine Learning Service.
    - **Hemmelighed for tjenesteprincipal** – Angiv programhemmeligheden for tjenesteprincipalen, du har oprettet i afsnittet [Active Directory-program](#aad-app). Denne værdi bruges til at anskaffe sig adgangstoken til den sikkerhedskonto, du har oprettet til at udføre autoriserede handlinger i Azure Storage og arbejdsområdet på Azure Machine Learning.
    - **Navn på lagerkonto** – Angiv navnet på den Azure-lagerkonto, du angav, da du kørte installationsguiden i dit Azure-arbejdsområde. (Yderligere oplysninger finder du i afsnittet [Konfigurere maskinel indlæring i Azure](#ml-workspace)).
    - **Pipeline-slutpunktadresse** – Angiv URL-adressen til pipeline REST-slutpunktet for din Azure Machine Learning Service. Du oprettede denne pipeline som sidste trin, da du [konfigurerede maskinel indlæring i Azure](#ml-workspace). Hvis du vil hente pipeline-URL-adressen, skal du logge på din Azure-portal og vælge **Pipelines** i navigationen. Vælg det pipelineslutpunkt, der kaldes **TriggerDemandForecastGeneration**, under fanen **Pipeline**. Kopiér derefter det REST-slutpunkt, der vises.

    ![Parametre under fanen Azure Machine Learning Service på siden Parametre til behovsprognoser.](media/azure-ml-service-parameters.png "Parametre under fanen Azure Machine Learning Service på siden Parametre til behovsprognoser")

## <a name="privacy-notice"></a><a name="privacy"></a>Erklæring om beskyttelse af personlige oplysninger

Når du vælger *Azure Machine Learning Service* som strategi for oprettelse af prognoser, sender Supply Chain Management automatisk dine kundedata for historisk efterspørgsel, f.eks. aggregerede mængder, produktnavne og deres produktdimensioner, afsendelses- og modtagelsessteder, kunde-id'er og prognoseparametre, til det geografiske område, hvor arbejdsområdet til maskinel indlæring og dets tilknyttede lagerkonto er placeret, med henblik på at prognosticere den fremtidige efterspørgsel. Azure Machine Learning Service kan være i et andet geografisk område end det geografiske område, hvor Supply Chain Management er udrullet. Nogle brugere kan styre, om denne funktion er aktiveret, ved at vælge strategien for oprettelse af prognoser på siden **Parametre for behovsprognoser**.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over behovsprognoser](introduction-demand-forecasting.md)
- [Generere et statistisk budgetgrundlag](generate-statistical-baseline-forecast.md)
- [Foretage manuelle justeringer af prognosegrundlaget](manual-adjustments-baseline-forecast.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
