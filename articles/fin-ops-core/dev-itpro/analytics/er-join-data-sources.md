---
title: Bruge JOIN-datakilder i ER-modeltilknytninger for at hente data fra flere programtabeller
description: I dette emne beskrives, hvordan du kan bruge datakilder af JOIN-typen i elektronisk rapportering (ER).
author: NickSelin
manager: AnnBe
ms.date: 10/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: 224acc19ee5dda430cd9471aa50e9d870a4f8c60
ms.sourcegitcommit: 564aa8eec89defdbe2abaf38d0ebc4cca3e28109
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2019
ms.locfileid: "2667948"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a>Bruge JOIN-datakilder til at hente data fra flere programtabeller i ER-modeltilknytninger (elektronisk rapportering)

[!include[banner](../includes/banner.md)]

Under konfiguration af ER-modeltilknytninger eller -formater kan du [tilføje](#review) nødvendige datakilder af **Join-typen**. På designtidspunktet konfigureres en **Join**-datakilde som et sæt af flere datakilder, der hver især returnerer en liste over poster. For hver datakilde med undtagelse af den første skal du definere de nødvendige betingelser for at sammenføje poster af aktuelle og tidligere datakilder. På kørselstidspunktet vil en konfigureret datakilde af typen **Join** [returnere](#executeERformat) en enkelt join-forbundet liste over poster, der indeholder felter fra posterne i indlejrede datakilder.

Følgende join-typer understøttes i øjeblikket:

- Ydre (venstre) join:
    - Forbind alle poster fra den første (længst til venstre) datakilde og derefter eventuelle matcher i overensstemmelse med konfigurerede betingelsesposter for den anden (længst til højre) datakilde.
- Indre (højre) join:
    - Forbind kun poster fra den første (længst til venstre) datakilde og kun poster for den anden (længst til højre) datakilde, der matcher hinanden i overensstemmelse med konfigurerede betingelser.

Når alle datakilder er af typen **Tabelposter** i den konfigurerede **Join**-datakilde, kan kørslen af Join-datakilden [udføres på databaseniveau](#analyze) ved hjælp af en enkelt SQL-sætning. Dette reducerer antallet af databasekald, hvilket forbedrer modeltilknytningens ydeevne. Ellers foretages der en kørsel af **Join**-datakilden i hukommelsen.

> [!NOTE]
> Brug af funktionen **VALUEIN** i ER-udtryk, der angiver betingelser for sammenkædning af poster i datakilder af typen Join, er ikke understøttet endnu. Besøg siden [Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md) for at få flere oplysninger om denne funktion.

Hvis du vil vide mere om denne funktion, skal du fuldføre eksemplet i dette emne.

## <a name="example-use-join-data-sources-in-er-model-mappings"></a>Eksempel: Bruge JOIN-datakilder i ER-modeltilknytninger

I følgende fremgangsmåde forklares det, hvordan systemadministratoren eller den elektroniske rapporteringsudvikler kan konfigurere en ER-modeltilknytning af elektronisk rapportering til at hente data fra flere programtabeller på én gang ved at bruge datakilder af typen **Join** til at forbedre ydeevnen af dataadgang. Disse trin kan udføres for ethvert regnskab i Dynamics 365 Finance eller Regulatory Configuration Service (RCS).

### <a name="prerequisites"></a>Forudsætninger

Hvis du vil udføre eksemplerne i dette emne, skal du have adgang til en af følgende, afhængigt af hvilken tjeneste der bruges til at udføre disse trin:

**Adgang til Finance for en af følgende roller:**

- Udvikler til elektronisk rapportering
- Funktionel konsulent i elektronisk rapportering
- Systemadministrator

**Adgang til RCS for en af følgende roller:**

- Udvikler til elektronisk rapportering
- Funktionel konsulent i elektronisk rapportering
- Systemadministrator

Du skal også først fuldføre trinnene i proceduren: [Opret en konfigurationsudbyder, og markér den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

På skal også på forhånd downloade fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=000000) og gemme følgende ER-eksempelkonfigurationsfiler lokalt:

| **Indholdsbeskrivelse**  | **Filnavn**   |
|--------------------------|-----------------|
| Eksempelkonfigurationsfil til **ER-datamodel**, der bruges som datakilde til eksemplerne.| [Model til at lære JOIN-datakilder.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Eksempelkonfigurationsfil til **ER-modeltilknytning**, der implementerer ER-datamodellen for eksemplerne. | [Tilknytning til at lære JOIN-datakilder.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Eksempelkonfigurationsfil til **ER-format**. I denne fil beskrives de data, der skal udfylde ER-formatkomponenten til eksemplerne. | [Format til at lære JOIN-datakilder.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="activate-a-configurations-provider"></a>Aktivere en konfigurationsudbyder

1. Få adgang til enten Finance eller RCS i den første session i din webbrowser.
2. Gå til **Virksomhedsadministration \> Arbejdsområder \> Elektronisk rapportering**.
3. Gå til sektionen **Konfigurationsudbydere** på siden **Lokaliseringskonfigurationer**, og sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware, Inc. (http://www.litware.com) er vist og er markeret som **Aktiv**. Hvis du ikke ser denne konfigurationsudbyder, skal du følge trinnene i proceduren [Opret en konfigurationsudbyder, og markér den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![Arbejdsområde til elektronisk rapportering](./media/GER-JoinDS-ActiveProvider.PNG)

### <a name="import-sample-er-configuration-files"></a>Importere ER-eksempelkonfigurationsfiler

1. Vælg **Rapporteringskonfigurationer**.
2. Importér konfigurationsfilen for ER-datamodellen.
    1. Vælg **Udveksling**.
    2. Vælg **Indlæs fra XML-fil**.
    3. Vælg **Gennemse** for at finde filen **Model til at lære JOIN-datakilder.version.1.1.xml**.
    4. Vælg **OK**.
3. Importér konfigurationsfilen for ER-modeltilknytningen.
    1. Vælg **Udveksling**.
    2. Vælg **Indlæs fra XML-fil**.
    3. Vælg **Gennemse** for at finde filen **Tilknytning til at lære JOIN-datakilder.version.1.1.xml**.
    4. Vælg **OK**.
4.  Importér ER-formatkonfigurationsfilen.
    1. Vælg **Udveksling**.
    2. Vælg **Indlæs fra XML-fil**.
    3. Vælg **Gennemse** for at finde filen **Format til at lære JOIN-datakilder.version.1.1.xml**.
    4. Vælg **OK**.
5.  I konfigurationstræet skal du udvide elementet **Model til at lære JOIN-datakilder** og andre modelelementer (når de er tilgængelige).
6.  Se listen over ER-konfigurationer i træet samt versionsoplysninger under fanen **Versioner** – de bruges som datakilden til eksempelrapporten.

    ![Siden med konfigurationer for elektronisk rapportering](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a>Aktivere indstillinger for udførelsessporing
1.  Vælg **KONFIGURATIONER**.
2.  Vælg **Brugerparametre**.
3.  Angiv parametre for udførelsessporing som vist på skærmbilledet nedenfor.

    ![Siden med brugerparametre til elektronisk rapportering](./media/GER-JoinDS-Parameters.PNG)

    Når disse parametre er aktiveret, vil udførelsessporing blive genereret for hver kørsel af den importerede ER-formatfil. Hvis du bruger detaljer om genereret udførelsessporing, kan du analysere udførelsen af ER-format og ER-modeltilknytningskomponenter. Besøg siden [Spore kørsel af ER-format for at foretage fejlfinding af problemer med ydeevnen](trace-execution-er-troubleshoot-perf.md) for at få flere oplysninger om funktionen til ER-udførelsessporing.

### <a name="review-er-model-mapping-part-1"></a>Gennemgå ER-modeltilknytning (del 1)

Gennemgå indstillingerne for komponenten til ER-modeltilknytning. Komponenten er konfigureret til at få adgang til oplysninger om versioner af ER-konfigurationer, detaljer om konfigurationer og konfigurationsudbydere uden brug af datakilder af typen **Join**.

1.  Vælg konfigurationen **Tilknytning til at lære JOIN-datakilder**.
2.  Vælg **Designer** for at åbne listen over tilknytninger.
3.  Vælg **Designer** for at gennemgå tilknytningsdetaljerne. 
4.  Vælg **Vis detaljer**.
5.  Udvid datamodelelementerne **Set1** og **Set1.Details** i konfigurationstræet:

    1. Bindingen **Details: Record list = Versions** angiver, at **Set1.Details** er bundet til **Versions**-datakilden, der returnerer poster i tabellen **ERSolutionVersionTable**. Hver post i denne tabel repræsenterer en enkelt version af en ER-konfiguration. Indholdet af denne tabel vises på oversigtspanelet **Versioner** på siden **Konfigurationer**.
    2. Bindingen **ConfigurationVersion: String = @.PublicVersionNumber** betyder, at værdien af den offentlige version af hver ER-konfigurationsversion hentes fra feltet **PublicVersionNumber** i tabellen **ERSolutionVersionTable** og placeres i elementet **ConfigurationVersion**.
    3. Bindingen **ConfigurationTitle: String = @.'>Relations'.Solution.Name** angiver, at navnet på en ER-konfiguration hentes fra feltet **Name** i tabellen **ERSolutionTable** via mange til én-relationen (**'>Relations'**) mellem tabellerne **ERSolutionVersionTable** og **ERSolutionTable**. Navne på ER-konfigurationer af den aktuelle programforekomst vises i konfigurationstræet på siden **Konfigurationer**.
    4. Bindingen **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** angiver, at navnet på konfigurationsudbyderen, der ejer den aktuelle konfiguration, hentes fra feltet **Name** i tabellen **ERVendorTable** via mange til én-relationen mellem tabellerne **ERSolutionTable** og **ERVendorTable**. Navne på ER-konfigurationsudbydere vises i konfigurationstræet på siden **Konfigurationer** i sidehovedet for hver konfiguration. Hele listen over ER-konfigurationsudbydere findes på tabel siden **Organisationsadministration \> Elektronisk rapportering \> Konfigurationsudbyder**.

    ![Side for ER-modeltilknytningsdesigner](./media/GER-JoinDS-Set1Review.PNG)

6.  Udvid datamodelelementet **Set1.Summary** i konfigurationstræet:

    1. Bindingen **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** angiver, at elementet **Set1.Summary.VersionsNumber** er bundet til aggregeringsfeltet **VersionsNumber** i datakilden **VersionsSummary** af typen **GroupBy**, der blev konfigureret til at returnere antallet af poster i tabellen **ERSolutionVersionTable** via datakilden **Versions**.

    ![Siden med GROUPBY-parametre for datakilde](./media/GER-JoinDS-Set1GroupByReview.PNG)

7.  Luk siden.

### <a name="review"></a> Gennemgå ER-modeltilknytning (del 2)

Gennemgå indstillingerne for komponenten til ER-modeltilknytning. Komponenten er konfigureret til at få adgang til oplysninger om versioner af ER-konfigurationer, detaljer om konfigurationer og konfigurationsudbydere med brug af en datakilde af typen **Join**.

1.  Udvid datamodelelementerne **Set2** og **Set2.Details** i konfigurationstræet: Bemærk, at bindingen **Details: Record list = Details** detaljer angiver, at elementet **Set2.Details** er bundet til datakilden **Details**, der er konfigureret som datakilden for **Join**-typen.

    ![Side for ER-modeltilknytningsdesigner](./media/GER-JoinDS-Set2Review.PNG)

    **Join**-datakilden kan tilføjes ved at vælge datakilden **Functions\Join**:

    ![Side for ER-modeltilknytningsdesigner](./media/GER-JoinDS-AddJoinDS.PNG)

2.  Vælg datakilden **Details**.
3.  Vælg **Rediger** i ruden **Datakilder**.
4.  Vælg **Rediger join.**
5.  Vælg **Vis detaljer**.

    ![Side med JOIN-parametre for datakilde](./media/GER-JoinDS-JoinDSEditor.PNG)

    Denne side bruges til at designe den påkrævede datakilde for **Join-typen**. På kørselstidspunktet opretter denne datakilde en enkelt join-forbundet liste med poster fra datakilderne i gitteret **Forenet liste**. Sammenkædningen af poster vil starte fra den **ConfigurationProviders**-datakilde, der findes i gitteret som første (kolonnen **Type** er tom for den). Alle poster for alle andre datakilder vil derfor blive forenet med poster for den overordnede datakilde baseret på rækkefølgen i dette gitter. Alle join-datakilder skal være konfigureret som en datakilde, der er indlejret under en destinationsdatakilde (datakilden **1Versions** er indlejret under én **1Configurations**, datakilden **1Configurations** er indlejret under én **ConfigurationProviders**). Hver enkelt konfigureret datakilde skal indeholde betingelserne for join-forbindelsen. I datakilden for denne bestemte **Join** defineres følgende join-forbindelser:

    - Hver post i datakilden **ConfigurationProviders** (der henvises til tabellen **ERVendorTable**) er kun knyttet til poster af én **1Configurations** (henvises til i tabellen **ERSolutionTable**), der har samme værdi i felterne **SolutionVendor** og **RecId**. Den **Indre join**-type bruges til denne join-forbindelse samt følgende betingelser for matchende poster: 

    FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)

    - Hver post i datakilden **1Configurations** (der henvises til tabellen **ERSolutionTable**) er kun knyttet til poster af én **1Versions** (der henvises til tabellen **ERSolutionVersionTable**), der har samme værdi i felterne **Solution** og **RecId**. Den **Indre join**-type bruges til denne join-forbindelse samt følgende betingelser for matchende poster:

    FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)

    - Indstillingen**Udfør** er konfigureret som **Forespørgsel**, hvilket vil sige, at denne join-datakilde udføres ved kørsel på databaseniveau som et direkte SQL-kald.

    Bemærk, at ved sammenkædning af poster i datakilder, der repræsenterer programtabeller, kan du angive join-betingelser ved hjælp af et par andre felter end dem, der beskriver eksisterende AOT-relationer mellem disse tabeller. Denne type join kan også konfigureres til at køre på databaseniveau.

6.  Luk siden.
7.  Vælg **Annuller**.
8.  Udvid datamodelelementet **Set2.Summary** i konfigurationstræet:

    - Bindingen **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** angiver, at elementet **Set2.Summary.VersionsNumber** er bundet til aggregeringsfeltet **VersionsNumber** i datakilden **DetailsSummary** af typen **GroupBy**, der blev konfigureret til at returnere antallet af join-poster i datakilden **Details** af typen **Join**.
    - Bemærk, at lokationsindstillingen **Udførelse** er konfigureret som **Forespørgsel**, hvilket vil sige, at denne **GroupBy**-datakilde udføres på kørselstidspunktet som et direkte SQL-kald på databaseniveau. Dette er muligt, fordi basisdatakilden **Details** for typen **Join** er konfigureret som udført på databaseniveau.

    ![Siden med GROUPBY-parametre for datakilde](./media/GER-JoinDS-Set2GroupByReview.PNG)

9.  Luk siden.
10. Vælg **Annuller**.

### <a name="executeERformat"></a> Udføre ER-format

1.  Få adgang til Finance eller RCS i den anden session af din webbrowser med samme legitimationsoplysninger og firma som i den første session.
2.  Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.
3.  Udvid konfigurationen **Model til at lære JOIN-datakilder**.
4.  Vælg konfigurationen **Format til at lære JOIN-datakilder**.
5.  Vælg **Designer**.
6.  Vælg **Vis detaljer**.
7.  Vælg **Tilknytning**.
8.  Vælg **Udvid/skjul**.

    Bemærk, at dette format er beregnet til at udfylde en genereret tekstfil med en ny linje for hver version af en ER-konfiguration (**Version**-sekvens). Hver genereret linje indeholder navnet på en konfigurationsudbyder, der ejer den aktuelle konfiguration, konfigurationsnavnet og konfigurationsversionen adskilt af semikolon. Den sidste linje i den genererede fil vil indeholde antallet af registrerede versioner af ER-konfigurationer (**Resume**-sekvens).

    ![Side med ER-formatdesigner](./media/GER-JoinDS-FormatReview.PNG)

    Datakilderne **Data** og **Resume** bruges til at udfylde oplysninger om konfigurationsversionen til den genererede fil:

    - Oplysninger fra datamodellen **Set1** bruges, når du vælger **Nej** for datakilden **Vælger** under kørsel på siden med brugerdialogboks, når der køres ER-format.
    - Oplysninger fra datamodellen **Set2** bruges, når du vælger **Ja** for datakilden **Vælger** under kørsel på siden med brugerdialogboks.

    ![Side med ER-formatdesigner](./media/GER-JoinDS-FormatMappingReview.PNG)

9.  Vælg **Kør**.
10. Vælg **Nej** i feltet **Brug JOIN-datakilde** på dialogbokssiden.
11. Vælg **OK**.
12. Gennemgå den genererede fil.

    ![Siden med ER-brugerdialogboks](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a>Analysere udførelsessporing i ER-format

1.  Vælg **Designer** i den første Finance- eller RCS-session.
2.  Vælg **Performancesporing**.
3.  I gitteret **Performancesporing** skal du vælge den øverste post med den seneste udførelsessporing af et ER-format, der brugte den aktuelle modeltilknytningskomponent.
4.  Vælg **OK**.

    Bemærk, at udførelsesstatistik oplyser om dublerede kald til programtabeller:

    - **ERSolutionTable** er blevet kaldt så mange gange, som du har konfigurationsversionsposter i tabellen **ERSolutionVersionTable**, mens antallet af sådanne opkald kan reduceres i tider for at forbedre ydeevnen.
    - **ERVendorTable** er blevet kaldt to gange for hver konfigurationsversionspost, der er registreret i tabellen **ERSolutionVersionTable**, men antallet af sådanne opkald kan også reduceres.

    ![Side for ER-modeltilknytningsdesigner](./media/GER-JoinDS-Set1Run2.PNG)

5.  Luk siden.

### <a name="execute-er-format"></a>Udføre ER-format

1.  Skift til fanen i webbrowseren med den anden session af Finance eller RCS.
2.  Vælg **Kør**.
3.  Vælg **Ja** i feltet **Brug JOIN-datakilde** på dialogbokssiden.
4.  Vælg **OK**.
5.  Gennemgå den genererede fil.

    ![Siden med ER-brugerdialogboks](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze"></a> Analysere udførelsessporing i ER-format

1.  Vælg **Designer** i den første Finance- eller RCS-session.
2.  Vælg **Performancesporing**.
3.  I gitteret **Performancesporing** skal du vælge den øverste post, der repræsenterer den seneste udførelsessporing af et ER-format, der brugte den aktuelle modeltilknytningskomponent.
4.  Vælg **OK**.

    Bemærk, at kørselsstatistik oplyser dig om følgende:

    - Programdatabasen er kaldt én gang for at hente poster fra tabellerne **ERVendorTable**, **ERSolutionTable** og **ERSolutionVersionTable** for at få adgang til obligatoriske felter.

    ![Side for ER-modeltilknytningsdesigner](./media/GER-JoinDS-Set2Run2.PNG)

    - Programdatabasen er blevet kaldt én gang for at beregne antallet af konfigurationsversioner ved hjælp af join-forbindelser, der er konfigureret i datakilden **Detaljer**.

    ![Side for ER-modeltilknytningsdesigner](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="additional-resources"></a>Yderligere ressourcer

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Spore kørsel af ER-format for at foretage fejlfinding af problemer med ydeevnen](trace-execution-er-troubleshoot-perf.md)

