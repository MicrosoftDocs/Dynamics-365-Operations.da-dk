---
title: Lagerværdirapporter
description: Denne artikel beskriver, hvordan du konfigurerer, genererer og bruger lagerværdirapporter. Disse rapporter indeholder oplysninger om fysiske og økonomiske lagerantal og -beløb.
author: JennySong-SH
ms.date: 11/28/2022
ms.topic: article
ms.search.form: InventValueProcess, InventValueReportSetup, InventValueExecutionHistory, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 6b21f6a7856526863914aac73d50e5c3a70605e8
ms.sourcegitcommit: 5f8f042f3f7c3aee1a7303652ea66e40d34216e3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806400"
---
# <a name="inventory-value-reports"></a>Lagerværdirapporter

[!include [banner](../includes/banner.md)]

Lagerværdirapporter indeholder oplysninger om fysiske og økonomiske lagerantal og -beløb. Du kan få vist rapporterne på mange forskellige måder. Du kan f.eks. få vist totaler eller posteringer eller filtrere efter varer eller et tidsinterval. Du kan få vist vareforbrugsværdier eller IGVF-værdier (igangværende arbejde) og angive andre indstillinger.

Du kan udføre følgende opgaver i rapporter over lagerværdier:

- Afstemme mellem finans og lager.
- Spørge efter lagerbeholdning og værdier for en bestemt periode.
- Oprette rapportkonfigurationer, der er tilpasset et bestemt formål.
- Gemme rapportkonfigurationer, så de kan bruges flere gange.
- Tilføje områder i filtrering af data, når du kører en rapport.

## <a name="types-of-inventory-value-report"></a>Typer af lagerværdirapporter

Der findes to typer lagerværdirapporter: **Lagerværdi** (standardrapporten) og **Lagerværdirapportlager**.

### <a name="standard-inventory-value-report"></a>Standardlagerværdirapport

Standardrapporten **Lagerværdi** er en simpel rapport, som giver dig mulighed for at vælge de oplysninger, der skal medtages, og derefter vise disse oplysninger på skærmen. Resultaterne gemmes ikke. Den giver heller ikke interaktive funktioner til filtrering, detailudledning, gennemsyn eller eksport. Derfor anbefales det, at du i de fleste tilfælde bruger rapporten **Lagerværdirapportlager**.

### <a name="inventory-value-report-storage-report"></a>Rapporten Lagerværdirapportlager

Rapporten **Lagerværdirapportlager** leverer output enten som en interaktiv side i Microsoft Dynamics 365 Supply Chain Management eller som et eksporteret dokument i et af flere formater.

Når du får vist rapporten i din browser, reguleres kolonner og aggregerede saldi dynamisk, afhængigt af det layout, som du har konfigureret. Du kan sortere resultaterne, filtrere dem, gå mere i dybden i dataene og meget mere.

Rapportresultater gemmes i dataenheden **Lagerværdi**. Du kan derfor filtrere og eksportere resultaterne til et format, f.eks. kommaseparerede værdier (CSV) eller Microsoft Excel-format.

**Lagerværdirapportlager** er nyttig, når outputtet indeholder mange linjer. Du har f.eks. 50.000 varer, og 300 butikker er oprettet som lagersteder. Hvis du i dette tilfælde anmoder om lagerafslutningssaldi pr. vare, sted og lagersted, indeholder outputtet mange linjer.

> [!NOTE]
> Rapporten **Lagerværdirapportlager** omfatter ikke subtotaler, der er defineret i rapportlayoutet. Den omfatter heller ikke finanssaldi, selvom de er defineret i rapportlayoutet. Afstemning til finans skal ske ved hjælp af råbalance. Standardrapporten for **Lagerværdi** indeholder dog disse subtotaler og saldi.

## <a name="turn-the-inventory-value-report-storage-feature-on-or-off"></a>Aktivere eller deaktivere funktionen Lagerværdirapportlager

Før du kan bruge denne funktion, skal den være aktiveret i dit system. Fra og med Supply Chain Management version 10.0.25 er funktionen som standard aktiveret. Fra og med Supply Chain Management version 10.0.29 er denne funktion obligatorisk og kan ikke deaktiveres. Hvis du kører en version, der er ældre end 10.0.29, kan administratorer slå denne funktion til eller fra ved at søge efter funktionen *Lagerværdirapportlager* i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="define-inventory-value-report-configurations"></a><a name="report-configuration"></a>Definere konfigurationer af lagerværdirapport

Du kan bruge siden **Lagerværdirapporter** til at konfigurere det indhold, der medtages i de forskellige typer lagerværdirapporter. Du kan definere ethvert antal rapporttyper. Hver gang du opretter en af typerne af lagerværdirapporten, skal du vælge en rapporttype.

1. Gå til **Omkostningsstyring \> Konfiguration af regnskabspolitik for lager \> Lagerværdirapporter**.
1. Udfør ét af følgende trin:

    - Hvis du vil redigere en eksisterende rapport, skal du vælge den i listeruden og derefter vælge **Rediger** i handlingsruden.
    - Hvis du vil oprette en ny rapport, skal du vælge **Ny** i handlingsruden.

1. Udfyld følgende felter i overskriften til den nye eller valgte rapport:

    - **Id** – Angiv et kort id for rapporten. Denne værdi skal være entydig for alle rapportkonfigurationer af lagerværdier. Den kan ikke redigeres, når du har gemt en ny konfiguration.
    - **Navn** – Angiv et sigende navn til rapporten.

1. Hvis du er ved at oprette en ny rapportkonfiguration, skal du vælge **Gem** i handlingsruden for at gøre de resterende felter tilgængelige.
1. I oversigtspanelet **Generelt** skal du indstille følgende felter:

    - **Datointerval** – Vælg et foruddefineret datointerval. Du kan tilsidesætte dette datointerval, når du kører rapporten.
    - **Interval** – Vælg enten *Bogføringsdato* eller *Transaktionstidspunkt*, afhængigt af den dato og det klokkeslæt, der skal bruges, når der hentes poster til rapporten.
    - **Dimensionssæt** – Vælg det sæt dimensioner, som dataene skal køres for. (Dimensionerne er defineret i finansmodulet). Du kan f.eks. køre data for *Hovedkonto* eller for *Hovedkonto + forretningsenhed*. Det dimensionssæt, du vælger, må ikke have mere end to dimensioner. Du kan finde flere oplysninger under [Økonomiske dimensionssæt](../../finance/general-ledger/financial-dimension-sets.md).

1. I oversigtspanelet **Kolonner** skal du indstille følgende felter. Disse felter styrer de kolonner, rapporten indeholder, og de typer data, som disse kolonner indeholder.

    - **Lager** – Angiv denne indstilling til *Ja* for at få vist lagerværdierne. Du kan derefter afstemme disse værdier med finanskontosaldi.
    - **IGVF** – Angiv denne indstilling til *Ja* for at få vist IGVF-værdierne. Du kan derefter afstemme disse værdier med IGVF-kontosaldi i finans. Når du angiver denne indstilling til *Ja*, viser rapporten kun de fysiske antal og beløb for lager, der har IGVF-status. Produktionsordrer med IGVF-status er plukket eller færdigmeldt, men de er ikke afsluttet.
    - **Udskudt vareforbrug** – Angiv denne indstilling til *Ja* for at få vist en kolonne, der viser fysiske lagerantal og -beløb for udskudt vareforbrug. Udskudt vareforbrug vises ved hjælp af fysiske antal og beløb, fordi det modregner følgeseddelantal og -beløb.
    - **Vareforbrug** – Angiv denne indstilling til *Ja* for at få vist en kolonne, der viser økonomiske antal og beløb for vareforbrug. Vareforbrug vises ved hjælp af økonomiske antal og beløb, fordi det modregner fakturaantal og -beløb.
    - **Drift** – Angiv denne indstilling til *Ja* for at få vist en kolonne, der viser det økonomiske beløb, der er bogført til driftskontiene for lageret.
    - **Udskriv akkumulerede kontoværdier til sammenligning** – Angiv denne indstilling til *Ja*, hvis du vil have vist en kolonne med saldoen på finanskontoen. På denne måde behøver du ikke kontrollere råbalancen. Denne indstilling fungerer kun sammen med standardrapporten **Lagerværdi**, ikke med rapporten **Lagerværdirapportlager**. Når du har angivet denne indstilling til *Ja*, skal du bruge følgende felter til at angive hver finanskonto, du vil medtage, afhængigt af de indstillinger for **Økonomisk position**, du har aktiveret.

        > [!NOTE]
        > Hvis du vælger en *totalkonto* i et af disse felter, vises både beløbet for hver lagerkonto, der er medtaget i totalkontoen, og totalkontobeløbet.

        - **Lagerkonto** – Angiv den finanskonto, der skal vises lageroplysninger for. (Både indstillingen **Lager** og indstillingen **Udskriv akkumulerede kontoværdier til sammenligning** skal angives til *Ja*).
        - **IGVF-konto** – Angiv den finanskonto, der skal vises IGVF-oplysninger for. (Både indstillingen **IGVF** og indstillingen **Udskriv akkumulerede kontoværdier til sammenligning** skal angives til *Ja*).
        - **Konto for udskudt vareforbrug** – Angiv den finanskonto, der skal vises oplysninger om udskudt vareforbrug for. (Både indstillingen **Udskudt vareforbrug** og indstillingen **Udskriv akkumulerede kontoværdier til sammenligning** skal angives til *Ja*).
        - **Vareforbrugskonto** – Angiv den finanskonto, der skal vises vareforbrugsoplysninger for. (Både indstillingen **Vareforbrug** og indstillingen **Udskriv akkumulerede kontoværdier til sammenligning** skal angives til *Ja*).

    - **Opsummer fysiske og økonomiske værdier** – Angiv denne indstilling til *Ja* for at få vist en kolonne med det samlede lagerantal og lagerbeløb (en oversigt over både fysiske og økonomiske lagerværdier). Hvis denne indstilling er angivet til *Nej*, viser rapporten både fysiske og økonomiske lagerværdier.
    - **Medtag ikke bogført i Finans** Angiv denne indstilling til *Ja* for at få vist en kolonne med de transaktioner, der aldrig er bogført i Finans. Posteringerne for følgende varetyper kan ikke bogføres i finansmodulet:

        - Modtagne og endnu ikke fakturerede varer, når indstillingen **Bogfør fysisk lager** er ryddet for den relevante varemodelgruppe.
        - Modtagne og endnu ikke fakturerede varer, når indstillingen **Bogfør produktkvittering i finans** er ryddet i oversigtspanelet **Produktkvittering** under fanen **Generelt** på siden **Kreditorparametre** (**Kreditor \> Konfiguration \> Kreditorparametre**).

    - **Beregn gennemsnitlig enhedsomkostning** – Angiv denne indstilling til *Ja* for at få vist en kolonne med den gennemsnitlige enhedsomkostning. Den gennemsnitlige enhedsomkostning er det samlede beløb divideret med det samlede antal.
    - **Samlet antal og værdi** – Angiv denne indstilling til *Ja* for at få vist kolonner med det samlede antal fysisk lager (og økonomiske antal) og det samlede beløb for fysisk lager (og økonomiske beløb). Du kan kun angive denne indstilling til *Ja*, hvis indstillingen **Opsummer fysiske og økonomiske værdier** er angivet til *Nej*.
    - **Lagerdimensioner** – I dette gitter skal du markere afkrydsningsfeltet **Vis** for hver dimension, der skal vises i rapporten. Kun dimensioner, hvor indstillingen **Økonomisk lager** er aktiveret, viser værdier i rapporten. Andre dimensioner viser kun tomme kolonner. For de dimensioner, du vælger at vise, kan du markere afkrydsningsfeltet **Total**, hvis du også vil medtage totaler.
    - **Ressource-id** – Angiv indstillingen **Vis** til *Ja* for at få vist en kolonne, der identificerer varen for hver række. Angiv indstillingen **Total** til *Ja*, så totaler også medtages. Afhængigt af den varetype, der er angivet i hver række, viser kolonnen en af følgende typer oplysninger:

        - **Materiale** – Kolonnen viser `ItemID`-feltværdien for den relevante materialepost.
        - **Arbejde** – Kolonnen viser `WorkCenterID`-feltværdien for den relevante arbejdspost.
        - **Indirekte omkostning** – Kolonnen viser `CodeID`-feltværdien for den relevante omkostningspost.

        Hvis indstillingen **Vis** er angivet til *Nej* for både feltet **Ressource-id** og feltet **Ressourcegruppe**, vil du kun få vist en samlet lagerværdi, der er baseret på de lagerdimensioner, du har valgt.

    - **Ressourcegruppe** – Angiv indstillingen **Vis** til *Ja* for at få vist en kolonne, der identificerer ressourcegruppen for hver række. Angiv indstillingen **Total** til *Ja*, så totaler også medtages. Afhængigt af den varetype, der er angivet i hver række, viser kolonnen en af følgende typer oplysninger:

        - **Materiale** – Kolonnen viser `ItemGroup`-feltværdien for den relevante materialepost.
        - **Arbejde** – Kolonnen viser `WorkcenterGroup`-feltværdien for den relevante arbejdspost.
        - **Indirekte omkostning** – Kolonnen viser `CostGroup`-feltværdien for den relevante omkostningspost. (Værdien `CostGroupType` skal være *Indirekte*).

        Hvis indstillingen **Vis** er angivet til *Nej* for både feltet **Ressource-id** og feltet **Ressourcegruppe**, vil du kun få vist en samlet lagerværdi, der er baseret på de lagerdimensioner, du har valgt.

1. I oversigtspanelet **Rækker** skal du indstille følgende felter: Med disse felter kan du føje tilsvarende IGVF-relaterede undersektioner til rapporten eller fjerne dem.

    - **Materiale** – Angiv denne indstilling til *Ja* for at få vist oplysninger om materialer. *Materiale* er en standardressourcetype, da materialer skal medtages i alle rapportkonfigurationer for at give pålideligt output.
    - **Arbejde** – Angiv denne indstilling til *Ja* for at få vist arbejdsomkostninger for IGVF.
    - **Indirekte omkostning** – Angiv denne indstilling til *Ja* for at få vist indirekte omkostninger for IGVF.
    - **Direkte outsourcing** – Angiv denne indstilling til *Ja* for at få vist direkte outsourcing for IGVF. Disse oplysninger bruges til underleverandørarbejde.
    - **Detaljeringsniveau** – Vælg en visningsindstilling for rapporten:

        - *Transaktioner* – Få vist alle relevante transaktioner i rapporten. Du kan opleve problemer med ydeevne, når du får vist rapporter, der indeholder et stort antal transaktioner. Hvis du vil bruge denne visningsindstilling, anbefales det derfor, at du bruger rapporten **Lagerværdirapportlager**.
        - *Totaler* – Få vist det samlede resultat.

    - **Medtag primosaldo** – Angiv denne indstilling til *Ja* for at vise primosaldoen. Denne indstilling er kun tilgængelig, når feltet **Detaljeringsniveau** er angivet til *Transaktioner*.

## <a name="generate-an-inventory-value-report-storage-report"></a>Generere en rapport over lagerværdirapportlager

Udfør følgende trin for at generere og gemme en **Lagerværdirapportlager** som rapport.

1. Gå til **Omkostningsstyring \> Forespørgsler og rapporter \> Lagerrapport over lagerværdi**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende felter i dialogboksen **Lagerværdi** i oversigtspanelet **Parametre**:

    - **Navn** – Angiv et entydigt navn til rapporten.
    - **Id** – Vælg den [konfiguration af lagerværdirapporten](#report-configuration), der skal bruges til rapporten. Konfigurationen opretter indstillinger for de kolonner og rækker, der skal medtages i rapporten.
    - **Datointerval** – Brug felterne i dette område til at definere, hvilke poster der medtages i rapporten. Hvis du vil definere datointervallet, kan du enten vælge et foruddefineret interval (i forhold til rapportgenereringsdatoen ) i feltet **Datointervalkode** eller vælge bestemte datoer i felterne **Fra dato** og **Til dato**.

1. I oversigtspanelet **Poster, som skal medtages** skal du konfigurere filtre og begrænsninger for at definere, hvilke data der skal medtages i rapporten. Vælg **Filter** for at åbne en standarddialogboks til forespørgselseditor, hvor du kan definere udvælgelseskriterier, sorteringskriterier og joinforbindelser. Felterne fungerer på samme måde som for andre typer af forespørgsler i Supply Chain Management. Alle disse filtre anvendes på lagertransaktioner, men ikke på finanssaldoen. Husk på denne funktionalitet, når du konfigurerer filtrene. Ellers vil du muligvis se en uoverensstemmelse mellem lageret og finansmodulet.
1. Angiv, hvordan, hvornår og hvor ofte rapporten skal genereres, i oversigtspanelet **Kør i baggrunden**. Felterne fungerer på samme måde som for andre typer af [baggrundsjob](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.

    > [!NOTE]
    > Denne rapport køres altid som en del af et batchjob.

1. Vælg **OK** for at anvende dine indstillinger og dialogboksen.

Når batchjobbet er fuldført, vises rapporten på siden **Lagerrapport over lagerværdi**. Du skal måske opdatere siden for at se rapporten.

> [!IMPORTANT]
> I den valgte rapportkonfiguration til lagerværdi kan du få en forkert primosaldo, hvis du vælger samme dato i både feltet **Fra dato** og feltet **Til dato**, og hvis du også har angivet indstillingen **Medtag primosaldo** til *Ja*.

## <a name="explore-an-inventory-value-report-storage-report"></a>Undersøge en Lagerværdirapportlager-rapport

Når du har genereret en rapport, kan du til enhver tid se og udforske den på følgende måde.

1. Gå til **Omkostningsstyring \> Forespørgsler og rapporter \> Lagerrapport over lagerværdi**.
1. Vælg en rapport på listen. På siden vises detaljer om [konfigurationen af lagerværdirapporten](#report-configuration), der blev brugt til at generere den valgte rapport.
1. Vælg **Vis detaljer** i handlingsruden for at få vist rapportindholdet.
1. Undersøg rapporten ved at følge disse trin:

    - Du kan vælge næsten enhver kolonneoverskrift for at sortere eller filtrere gitteret efter værdier i kolonnen på samme måde som de fleste standardsider i Supply Chain Management.
    - Brug feltet **Filter** til at filtrere rapporten efter en hvilken som helst værdi i en af de tilgængelige kolonner.
    - Brug menuen Vis (oven over **Filter**-feltet) til at gemme og indlæse dine favoritkombinationer af sorterings- og filtreringsindstillinger.

## <a name="export-an-inventory-value-report-storage-report"></a><a name="export-stored-report"></a>Eksportere en Lagerværdirapportlager-rapport

Hver rapport, du opretter, gemmes i dataenheden **Lagerværdi**. Du kan bruge standardfunktionerne til datastyring i Supply Chain Management til at eksportere data fra denne enhed til alle understøttede dataformater, herunder CSV eller Excel-format.

I følgende eksempel vises, hvordan du kan eksportere en **Lagerværdirapportlager**-rapport.

1. Gå til **Systemadministration \> Arbejdsområder \> Datastyring**.
1. Vælg feltet **Eksport** i sektionen **Import/eksport**.
1. På siden **Eksport**, der vises, skal du konfigurere eksportjobbet. Angiv først et gruppenavn til jobbet.
1. Vælg **Tilføj enhed** i sektionen **Valgte enheder**.
1. Angiv følgende felter i den viste dialogboks:

    - **Enhedsnavn** – Vælg *Lagerværdi*.
    - **Målformat for data** – Vælg det format, der skal eksporteres data til.

1. Vælg **Tilføj** for at tilføje den nye række, og vælg derefter **Luk** for at lukke dialogboksen.
1. Normalt skal du eksportere én rapport ad gangen. Hvis du vil eksportere en enkelt rapport, skal du oprette et filter for den række, du lige har føjet til dialogboksen **Forespørgsel**. På denne måde kan du definere, hvilken rapport fra enheden **Lagerværdi** der skal medtages i eksporten. Følg disse trin for at angive følgende filterindstillinger for at eksportere en enkelt rapport:

    1. Under fanen **Område** skal du vælge **Tilføj** for at tilføje en ny række.
    2. Angiv feltet **Tabel** til *Lagerværdi*.
    3. Angiv feltet **Afledt tabel** til *Lagerværdi*.
    4. Angiv feltet **Felt** til det felt, du vil filtrere efter. Du skal normalt bruge feltet **Udførelsesnavn** og/eller feltet **Udførelsestid**.
    5. Angiv feltet **Kriterier** til den værdi, du vil søge efter i det valgte felt. (Hvis du har valgt feltet **Udførelsesnavn** i det foregående trin, vil denne værdi være navnet på rapporten. Hvis du har valgt feltet **Udførelsestid**, vil det være det tidspunkt, hvor rapporten blev oprettet).
    6. Hvis det er nødvendigt, kan du tilføje flere rækker under fanen **Område**, indtil du entydigt har identificeret den rapport, du søger efter.

1. Vælg **OK** for at gemme dine indstillinger og lukke dialogboksen.
1. Vælg **Gem** for at gemme eksportindstillingerne.
1. Åbn fanen **Eksportindstillinger**, og vælg **Eksporter nu** for at generere eksportfilen.
1. Siden **Udførelsesoversigt** åbnes, hvor du kan se status for eksportjobbet og en liste over de enheder, der er eksporteret. Vælg enheden **Lagerværdi** på listen i sektionen **Status for behandling af enhed**, og vælg derefter **Hent fil** for at hente de data, der er eksporteret fra den pågældende enhed.

Du kan finde flere oplysninger om, hvordan du bruger datastyring til at eksportere data i [Oversigt over dataimport og eksportjob](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

## <a name="delete-stored-inventory-value-reports"></a>Slette gemte lagerværdirapporter

Efterhånden som antallet af gemte rapporter over lagerværdier øges, kan de i den sidste ende begynde at optage for megen plads i databasen. Denne situation kan påvirke systemets ydeevne og medføre højere datalagringsomkostninger. Derfor er du sandsynligvis nødt til at rydde op i rapporterne fra tid til anden ved at slette ældre rapporter.

> [!IMPORTANT]
> Før du sletter nogen af de tidligere genererede lagerværdirapporter, anbefales det på det kraftigste, at du først [eksporterer rapporterne](#export-stored-report) og gemmer dem eksternt, da du måske ikke kan generere dem igen senere. Denne begrænsning findes, fordi når du opretter en rapport over lagerværdier, fungerer systemet bagud fra i dag og behandler hver enkelt lagertransaktionspost i omvendt rækkefølge. Hvis du forsøger at søge for langt tilbage, når du opretter en rapport, kan omfanget af posteringer, der skal behandles, i den sidste ende blive så stort, at systemet får timeout, før det kan afslutte generering af rapporten. Hvor langt tilbage i tid, du kan oprette nye rapporter for, afhænger af antallet af lagertransaktioner, du har i systemet for det relevante tidsrum.

### <a name="delete-one-report-at-a-time"></a>Slette én rapport ad gangen

Benyt følgende fremgangsmåde for at slette én gemt rapport ad gangen.

1. [Eksportér den rapport](#export-stored-report), du planlægger at slette, og gem den på en ekstern placering til fremtidig reference.
1. Gå til **Omkostningsstyring \> Forespørgsler og rapporter \> Lagerrapport over lagerværdi**.
1. Vælg den rapport, du vil slette, i listeruden.
1. Vælg **Slet** i handlingsruden.
1. En advarsel minder dig om at sikkerhedskopiere genererede rapporter. Vælg **Ja**, hvis du er klar til at fortsætte med sletningen.

### <a name="delete-several-reports-at-the-same-time"></a>Slette flere rapporter på én gang

Benyt følgende fremgangsmåde for at slette flere gemte rapporter ad gangen.

1. [Eksportér alle de rapporter](#export-stored-report), du planlægger at slette, og gem dem på en ekstern placering til fremtidig reference.
1. Gå til **Omkostningsstyring \> Lagerregnskab \> Oprydning \> Rapporten Lagerværdi – oprydning i data**.
1. I dialogboksen **Rapporten Lagerværdi – oprydning i data** skal du i feltet **Slet lagerværdirapport, der er udført før** vælge den dato, før hvilken alle lagerværdirapporter skal slettes.
1. I oversigtspanelet **Poster, der skal indgå**, kan du konfigurere flere filterbetingelser for at begrænse det sæt rapporter, som skal slettes. Vælg **Filter** for at åbne en standardforespørgselseditor, hvor du kan definere egenskaberne for de rapporter, der skal slettes.
1. Angiv, hvordan, hvornår og hvor ofte rapporterne skal slettes, i oversigtspanelet **Kør i baggrunden**. Felterne fungerer på samme måde som for andre typer af [baggrundsjob](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management. Du vil dog typisk køre dette job manuelt, hver gang der er brug for det.
1. Vælg **OK** for at slette de angivne rapporter.

## <a name="generate-a-standard-inventory-value-report"></a>Generere en standardrapport over lagerværdi

Du kan bruge følgende procedure til at oprette en standardrapport over **Lagerværdi**.

1. Gå til **Omkostningsstyring \> Forespørgsler og rapporter \> Lagerregnskab - statusrapporter \> Lagerværdi**.
1. Angiv følgende felter i dialogboksen **Lagerværdirapport** i oversigtspanelet **Parametre**:

    - **Navn** – Angiv et entydigt navn til rapporten.
    - **Id** – Vælg den [konfiguration af lagerværdirapporten](#report-configuration), der skal bruges til rapporten. Konfigurationen opretter indstillinger for de kolonner og rækker, der skal medtages i din rapport.
    - **Datointerval** – Brug felterne i dette område til at definere, hvilke poster der medtages i rapporten. Hvis du vil definere datointervallet, kan du enten vælge et foruddefineret interval (i forhold til rapportgenereringsdatoen ) i feltet **Datointervalkode** eller vælge bestemte datoer i felterne **Fra dato** og **Til dato**.

1. I oversigtspanelet **Poster, som skal medtages** skal du konfigurere filtre og begrænsninger for at definere, hvilke data der skal medtages i rapporten. Vælg **Filter** for at åbne en standarddialogboks til forespørgselseditor, hvor du kan definere udvælgelseskriterier, sorteringskriterier og joinforbindelser. Felterne fungerer på samme måde som for andre typer af forespørgsler i Supply Chain Management.
1. Angiv, hvordan, hvornår og hvor ofte rapporten skal genereres, i oversigtspanelet **Kør i baggrunden**. Felterne fungerer på samme måde som for andre typer af [baggrundsjob](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Vælg **OK** for at anvende dine indstillinger og dialogboksen. Rapporten vises.

## <a name="reading-inventory-value-reports"></a>Læsning af lagerværdirapporter

Dette afsnit indeholder en vejledning i, hvordan du kan læse og forstå en rapport over lagerværdier.

Supply Chain Management understøtter følgende to vigtige koncepter, der har med lagerstatus at gøre:

- **Økonomisk opdateret** – Dette begreb angiver, at lagertransaktionerne allerede er faktureret. For produktionsordrer angiver det afslutningen af en produktionsordre.
- **Fysisk opdateret** – Dette begreb angiver, at lagertransaktionerne endnu ikke er faktureret, men de er modtaget eller afsendt. I forbindelse med produktionsordrer angiver det, at materiale er plukket, eller at produktionsordren er færdigmeldt.

Når du forstår disse to begreber, vil det være let at forstå følgende kolonner i rapportens output:

- **Lager: økonomisk antal** – Det antal, der er opdateret i økonomisk forstand.
- **Lager: økonomisk beløb** – Beløbsværdien af det lager, der er opdateret i økonomisk forstand.
- **Lager: bogført fysisk antal** – Det antal, der er opdateret i fysisk forstand.
- **Lager: bogført fysisk beløb** – Beløbsværdien af det lager, der er opdateret i fysisk forstand.
- **Lager: ikke bogført fysisk antal** – Det antal, der har lagertransaktioner, men som ikke er bogført i Finans. Du har f.eks. en varemodelgruppe, hvor indstillingerne **Bogfør fysisk lager** og **Bogfør økonomisk lager** er ryddet, og du har en vare, der er knyttet til den pågældende gruppe. Derefter opretter du en indkøbsordre, modtager den og fakturerer den. Hvis du på dette tidspunkt gennemser rapporten over lagerværdien for varen, vil du se, at antallet og værdien på indkøbsordren vises i kolonnerne **Lager: Fysisk antal, der ikke er bogført** og **Lager: Fysisk beløb, der ikke er bogført**.
- **Lager: Fysisk beløb, der ikke er bogført** – Du kan konfigurere rapporterne, så de viser ikke-bogførte beløb. Men hvis du bruger rapporten til lagerafstemning, skal du ikke bruge denne værdi. Ellers bogføres beløbet ikke i Finans.
- **Lager: Antal** – Det samlede antal af alle antalskolonner i rapporten.
- **Lager: Beløb** – Det samlede antal af alle beløbskolonner i rapporten. Når du skal udføre lagerafstemning, skal du ikke bruge denne kolonne, hvis rapporten indeholder kolonnen **Lager: Fysisk beløb, der ikke er bogført**. I dette tilfælde skal du udelade **Lager: Fysisk beløb, der ikke er bogført** fra det samlede beløb.
- **Gennemsnitlig enhedsomkostning** – Det samlede beløb divideret med det samlede antal.

Du vil typisk bruge en rapport over lagerværdi til at få vist lagerværdien og -antallet. Sommetider viser rapporten ikke alle de relevante lagerdimensioner. Hvis du ikke kan se de forventede dimensioner, skal du validere følgende indstillinger:

- Gennemgå varelager og sporingsdimensionsgrupper. Kun dimensioner, hvor indstillingen **Økonomisk lager** er aktiveret, kan vises i rapporten.
- Gå til **Omkostningsstyring \> Konfiguration af regnskabspolitik for lager \> Lagerværdirapporter**, vælg den rapportkonfiguration, du brugte til at oprette rapporten, og sørg for, at de nødvendige lagerdimensioner er valgt i kolonnen **Vis**.

Du kan f.eks. have en vare med varenummer *A0001*. I lagringsdimensionsgruppen er det kun lokationen, der er aktiveret til økonomisk lager. Lokation og lagersted er begge aktiveret til fysisk lager. I sporingsdimensionsgruppen er batchnummeret aktiveret for fysisk lager, men ikke for økonomisk lager. Du kan derefter bruge en rapportkonfiguration, hvor lokation, lagersted og batchnummer alle er valgt. Når du får vist rapporten, kan du kun se en værdi for lokationen. Kolonnerne for lagerstedet og batchnummeret er tomme. Som dette eksempel viser, kan lagerværdirapporter kun vise lagerdimensioner, der er aktiveret til økonomisk lager.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
