---
title: Spore kørslen af ER-formater til fejlfinding af problemer med ydeevnen
description: Dette emne indeholder oplysninger om, hvordan du kan bruge funktionen til performancesporing i elektroniske rapporter (ER) til at foretage fejlfinding af problemer med ydeevnen.
author: NickSelin
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 9a5f943a507483bb4c1bd7fe87c0d65353194a6e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687421"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a>Spore kørslen af ER-formater for at foretage fejlfinding af problemer med ydeevnen

[!include[banner](../includes/banner.md)]

Som en del af processen med at udvikle elektroniske rapporteringskonfigurationer (ER) til generering af elektroniske dokumenter definerer du den metode, der bruges til at få data ud af programmet og angive dem i det output, der genereres. ER-funktionen til sporing af ydeevnen hjælper med at reducere den tid og de omkostninger, der er involveret i indsamling af oplysninger om ER-format, betragteligt, og bruger oplysningerne til fejlfinding af problemer med ydeevnen. Dette selvstudium indeholder en vejledning i, hvordan du kan tage performancesporing for kørte ER-formater, og hvordan du kan bruge oplysningerne fra disse sporinger til at forbedre ydeevnen.

## <a name="prerequisites"></a>Forudsætninger

Før du kan følge eksemplerne i dette selvstudium, skal du have følgende adgang:

- Adgang til en af følgende roller:

    - Udvikler til elektronisk rapportering
    - Funktionel konsulent i elektronisk rapportering
    - Systemadministrator

- Adgang til den forekomst af Regulatory Configuration Service (RCS), der er klargjort til den samme lejer som programmet, for en af følgende roller:

    - Udvikler til elektronisk rapportering
    - Funktionel konsulent i elektronisk rapportering
    - Systemadministrator

Du skal også hente og lokalt gemme følgende filer.

| Fil                                  | Indhold                               |
|---------------------------------------|---------------------------------------|
| Performance trace model.version.1     | [Eksempler på ER-datamodelkonfiguration](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| Performance trace metadata.version.1  | [Eksempler på ER-metadatakonfiguration](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| Performance trace mapping.version.1.1 | [Eksempler på ER-modeltilknytningskonfiguration](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Performance trace format.version.1.1  | [Eksempler på ER-formatkonfiguration](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a>Konfigurere ER-parametre

Hver ER-performancesporing, der genereres i programmet, gemmes som en vedhæftet fil i kørselslogposten. Dokumentstyringsstrukturen bruges til at administrere disse vedhæftede filer. Du skal konfigurere ER-parametre i forvejen for at angive den DM-dokumenttype, der skal bruges til at tilknytte performancesporing. I arbejdsområdet **Elektronisk rapportering** skal du vælge **Parametre til elektronisk rapportering**. Vælg derefter den DM-dokumenttype, der skal bruges til performancesporing, i feltet **Andre** under fanen **vedhæftede filer** på siden **Parametre til elektronisk rapportering**.

![Siden Parametre til elektronisk rapportering](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

Hvis en DM-dokumenttype skal være tilgængelig i opslagsfeltet **Andet**, skal den være konfigureret på følgende måde på siden **Dokumenttyper** (**Organisationsadministration \> Administration af dokument \> Dokumenttyper**):

- **Klasse:** Vedhæft fil
- **Gruppe:** Fil

![Siden Dokumenttyper](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> Den valgte dokumenttype skal være tilgængelig i alle firmaer i den aktuelle forekomst, da vedhæftede DM-filer er firmaspecifikke.

### <a name="configure-rcs-parameters"></a>Konfigurere RCS-parametre

ER-performancesporing, der genereres, bliver importeret til RCS til analyse ved hjælp af ER-formatdesigneren og ER-tilknytningsdesigneren. Da ER-performancesporinger gemmes som vedhæftede filer i den kørselslogpost, der er relateret til ER-formatet, skal du konfigurere RCS-parametrene på forhånd for at angive den DM-dokumenttype, der skal bruges til at tilknytte performancesporinger. I den forekomst af RCS, der er klargjort for dit firma, skal du vælge **Parametre til elektronisk rapportering** i arbejdsområdet **Elektronisk rapportering**. Vælg derefter den DM-dokumenttype, der skal bruges til performancesporing, i feltet **Andre** under fanen **vedhæftede filer** på siden **Parametre til elektronisk rapportering**.

![Siden Parametre til elektronisk rapportering i RCS](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

Hvis en DM-dokumenttype skal være tilgængelig i opslagsfeltet **Andet**, skal den være konfigureret på følgende måde på siden **Dokumenttyper** (**Organisationsadministration \> Administration af dokument \> Dokumenttyper**):

- **Klasse:** Vedhæft fil
- **Gruppe:** Fil

## <a name="design-an-er-solution"></a>Designe en ER-løsning

Antag, at du er begyndt at designe en ny ER-løsning for at generere en ny rapport, der viser kreditorposteringer. I øjeblikket kan du finde posteringerne for en valgt kreditor på siden **Kreditorposteringer** (gå til **Kreditor \> Kreditorer \> Alle kreditorer**, vælg en kreditor, og vælg derefter i handlingsruden under fanen **Kreditor** i gruppen **Transaktioner** på **Posteringer**). Men du vil have alle kreditorposteringer samtidig i et elektronisk dokument i XML-format. Denne løsning består af flere ER-konfigurationer, der indeholder den nødvendige datamodel, metadata, modeltilknytning og formatkomponenter.

1. Log på den forekomst af RCS, der er klargjort for dit firma.
2. I dette selvstudium skal du oprette og ændre ER-konfigurationerne for eksempelfirmaet **Litware Inc.**. Kontroller derfor, at denne konfigurationsudbyder er føjet til RCS og valgt som aktiv. Du kan finde instruktioner i proceduren [Oprette konfigurationsudbydere og markere dem som aktive](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. I arbejdsområdet **Elektronisk rapportering** skal du vælge feltet **Rapporteringskonfigurationer**.
4. På siden **Konfigurationer** skal du importere de ER-konfigurationer, som du har hentet som en forudsætning i RCS, i følgende rækkefølge: datamodel, metadata, modeltilknytning, format. Benyt følgende fremgangsmåde for hver konfiguration:

    1. Vælg **Exchange \> Indlæs fra XML-fil** i handlingsruden.
    2. Vælg **Gennemse** for at vælge den relevante fil til den krævede ER-konfiguration i XML-format.
    3. Vælg **OK**.

    ![Siden Konfigurationer i RCS](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a>Køre ER-løsningen for at spore kørslen

Antag, at du er færdig med at designe den første version af ER-løsningen. Du vil nu teste den i din forekomst og analysere kørselsydeevnen.

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a>Importere en ER-konfigurationer fra RCS til Finance and Operations

1. Log på din programforekomst.
2. I dette selvstudium skal du importere konfigurationer fra din RCS-forekomst (hvor du udformer dine ER-komponenter) i din forekomst (hvor du tester og til slut bruger dem). Du skal derfor sikre dig, at alle påkrævede artefakter er forberedt. Du kan finde instruktioner i proceduren [Importer konfigurationer af elektronisk rapportering (ER) fra Regulatory Configuration Services (RCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations).
3. Udfør følgende trin for at importere konfigurationerne fra RCS i programmet:

    1. I arbejdsområdet **Elektronisk rapportering** skal du vælge **Lagre** i feltet for **Litware, Inc.**-konfigurationsudbyder.
    2. På siden **Konfigurationslager** skal du vælge lageret for **RCS**-typen og derefter vælge **Åbn**.
    3. I oversigtspanelet **Varianter** skal du vælge konfigurationen **Format for performancesporing**.
    4. I oversigtspanelet **Versioner** skal du vælge version **1.1** af den valgte ER-konfiguration og derefter vælge **Importer**.

    ![Siden Konfigurationslager](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

De tilsvarende versioner af datamodellen og modeltilknytningskonfigurationerne importeres automatisk som forudsætninger for den importerede ER-formatkonfiguration.

### <a name="turn-on-the-er-performance-trace"></a>Aktivere ER-performancesporing

1. Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.
2. På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
3. Udfør følgende trin i sektionen **Kørselssporing** i dialogboksen **Brugerparametre**:

    1. Vælg **Fejlfinding af sporingsformat** i feltet **Udførelsessporingsformat** for at starte indsamling af oplysninger om ER-format. Når denne værdi er valgt, indsamler performancesporing oplysninger om den tid, der bruges på følgende handlinger:

        - Kørsel af hver datakilde i den modeltilknytning, der kaldes for at hente data
        - Behandling af hvert formatelement for at angive data i det output, der genereres

        Du kan bruge feltet **Fejlfinding af sporingsformat** til at angive formatet for den genererede performancesporing, som kørselsoplysningerne gemmes i, for ER-format- og tilknytningselementer. Hvis du vælger **Fejlfinding af sporingsformat** som værdi, kan du analysere indholdet af sporingen i ER Operations-designeren og se de ER-format eller -tilknytningselementer, der er nævnt i sporingen.

    2. Angiv følgende indstillinger til **Ja** for at indsamle specifikke oplysninger om kørslen af ER-modeltilknytningerne og ER-formatkomponenterne:

        - **Indsaml forespørgselsstatistikker** – Når denne indstilling er aktiveret, indsamler performancesporing følgende oplysninger:

            - Det antal databasekald, der er udført af datakilder
            - Antallet af dobbeltkald til databasen
            - Oplysninger om de SQL-sætninger, der blev brugt til at foretage databasekald

        - **Spor adgang for cachelagring** – Når denne indstilling er slået til, indsamler performancesporing oplysninger om ER-modeltilknytningens cacheforbrug.
        - **Spor dataadgang** – Når denne indstilling er aktiveret, indsamler performancesporing oplysninger om antallet af kald til databasen for de afviklede datakilder af postlistetypen.
        - **Fasttekst til sporingsliste** – Når denne indstilling er aktiveret, indsamler performancesporing oplysninger om antallet af poster, der er anmodet om fra datakilder af postlistetypen.

    > [!NOTE]
    > Parametrene i dialogboksen **Brugerparametre** er specifikke for brugeren og det aktuelle firma.

    ![Dialogboksen Brugerparametre](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a>Køre ER-formatet

1. Vælg firmaet **DEMF**.
2. Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.
3. På siden **Konfigurationer** skal du vælge elementet **Format for performancesporing** i konfigurationstræet.
4. Vælg **Kør** i handlingsruden.

Bemærk, at den fil, der genereres, indeholder oplysninger om 265 posteringer for seks kreditorer.

## <a name="review-the-execution-trace"></a>Gennemse kørselssporingen

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a>Eksportere den genererede sporing fra programmet

Performancesporing fjernes fra ER-kildeformatet og kan serialiseres til en ekstern zip-fil.

1. Gå til **Organisationsadministration \> Elektronisk rapportering \> Fejlfindingslogs for konfigurationer**.
2. Vælg **Format for performancesporing** i feltet **Konfigurationsnavn** i den venstre rude på siden **Kørselslogge for elektronisk rapportering** for at finde de poster i loggen, der blev genereret ved kørslen af konfigurationen **Format for performancesporing**.
3. Vælg knappen **Vedhæftede filer** (symbolet med papirklip) i øverste højre hjørne af siden eller tryk på **Ctrl+Skift+A**.

    ![Knappen Vedhæftede filer på siden Kørselslogge for elektronisk rapportering](./media/GER-PerfTrace-GER-DebugLog.png)

4. Vælg **Åbn** i handlingsruden på siden **Vedhæftede filer til kørselslogge for elektronisk rapportering** for at få vist performance-sporing som en zip-fil og gemme den lokalt.

    ![Vedhæftede filer til elektroniske rapporteringslogfiler](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> Den sporing, der genereres, har en reference til ER-kilderapporten via et entydigt rapport-id i **GUID**-format. Formatets versionsnummer tages ikke i betragtning.

Bemærk, at tilknytningen mellem den performancesporing, der er genereret for det kørte ER-format og ER-modeltilknytningen, er baseret på den rodbeskrivelse, der blev brugt, og den fælles datamodel. Formatets versionsnummer og modeltilknytningen tages ikke i betragtning. Indstillingen af **Standard for modeltilknytning**-flaget for modeltilknytningen tages heller ikke i betragtning.

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a>Import af den genererede sporing i RCS

1. I RCS i arbejdsområdet **Elektronisk rapportering** skal du vælge feltet **Rapporteringskonfigurationer**.
2. Udvid elementet **Performancesporingsmodel** i konfigurationstræet på siden **Konfigurationer**, og vælg elementet **Performancesporingsformat**.
3. Vælg **Designer** i handlingsruden.
4. I oversigtspanelet på siden **Formatdesigner** skal du vælge **Performancesporing**.
5. Vælg **Importér performancesporing** i dialogboksen Indstillinger for resultat af **Indstillinger for resultat af performancesporing**.
6. Vælg **Gennemse**, og vælg den zip-fil, du eksporterede tidligere.
7. Vælg **OK**.

    ![Dialogboksen Indstillinger for resultat af performancesporing i RCS](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a>Bruge performancesporing til analyse i RCS – formatkørsel

1. I RCS på siden **Formatdesigner** skal du vælge **Udvid/skjul** for at udvide indholdet af alle formatelementer.

    Bemærk, at der vises yderligere oplysninger for nogle af elementerne i det aktuelle format:

    - Den faktiske tid, der er brugt på at indtaste data i det genererede output ved hjælp af formatelementet
    - Den samme tid angivet som en procentdel af den samlede tid, der blev brugt på at generere hele outputtet

    ![Siden Formatdesigner i RCS](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. Luk siden **Formatdesigner**.

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a>Bruge performancesporing til analyse i RCS – modeltilknytning

1. I RCS på siden **Konfigurationer** skal du vælge elementet **Tilknytning af performancesporing** i konfigurationstræet.
2. Vælg **Designer** i handlingsruden.
3. Vælg **Designer**.
4. I oversigtspanelet på siden **Modeltilknytningsdesigner** skal du vælge **Performancesporing**.
5. Vælg den sporing, du tidligere har importeret.
6. Vælg **OK**.

Bemærk, at nye oplysninger bliver tilgængelige for nogle datakildeelementer i den aktuelle modeltilknytning:

- Den tid, det faktisk blev brugt på at hente data vha. datakilden
- Den samme tid angivet som en procentdel af den samlede tid, der blev brugt på at køre hele modeltilknytningen

Bemærk, at du får besked om, at den aktuelle modeltilknytning duplikerer databaseanmodninger, mens VendTable/\<Relationer/VendTrans.VendTable\_AccountNum-data køres. Denne duplikering sker, fordi listen over kreditorposteringer kaldes to gange for hver af de gentagne kreditorposter:

- Der foretages ét kald for at angive detaljer om hver transaktion i datamodellen baseret på konfigurerede bindinger.
- Der foretages ét kald for at angive det beregnede antal posteringer pr. kreditor i datamodellen.

![Meddelelse om dublerede databaseanmodninger på siden Modeltilknytningsdesigner i RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

Værdien **\[Q:530\]** angiver, at VendTrans-tabellen blev kaldt 530 gange for at returnere en post fra denne tabel til datakilden VendTable/\<Relationer/VendTrans.VendTable\_AccountNum. Værdien **\[530\]** angiver, at datakilden VendTable/\<Relationer/VendTrans.VendTable\_AccountNum blev kaldt 530 gange for at returnere en post fra den pågældende datakilde og angive oplysningerne fra den i datamodellen.

Det anbefales, at du bruger cachelagring til datakilden VendTable/\<Relationer/VendTrans.VendTable\_AccountNum for at reducere antallet af kald, der foretages, for at få oplysninger om 265-transaktioner og hjælpe med at forbedre modeltilknytningens performance.

Det kan også være nyttigt at reducere antallet af kald, der foretages til LedgerTransTypeList-datakilden. Denne datakilde bruges til at knytte hver værdi i **LedgerTransType**-fastteksten til dens etiket. Hvis du bruger denne datakilde, kan du finde en passende etiket og angive den i datamodellen for hver enkelt kreditorpostering. Det aktuelle antal kald til denne datakilde (9.027) er meget højt for 265 transaktioner.

![Modeltilknytningsdesigner i RCS, der viser 9.027 kald til datakilden](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Forbedre modeltilknytningen på baggrund af oplysninger fra kørselssporing

### <a name="modify-the-logic-of-the-model-mapping"></a>Ændre modeltilknytningens logik

1. Udfør følgende trin for at bruge cachelagring til at forhindre, at der foretages identiske kald til databasen:

    1. I RCS på siden **Modeltilknytningsdesigner** skal du i ruden **Datakilder** vælge elementet **VendTable**.
    2. Vælg **Cache**.
    3. Udvid elementet **VendTable**, udvid listen over en-til-mange-relationer til datakilden VendTable (**\<Relationer**-elementet), og vælg **VendTrans. VendTable\_-AccountNum**-elementet.
    4. Vælg **Cache**.

    ![Konfigurere cachelagring til at forhindre dobbelte kald](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. Udfør følgende trin for at bringe LedgerTransTypeList-datakilden ind i området for datakilden VendTable:

    1. Udvid elementet **Funktioner** i ruden **Datakildetyper**, og vælg elementet **Beregnet felt**.
    2. Vælg elementet **VendTable** i ruden **Datakilder**.
    3. Vælg **Tilføj**.
    4. I feltet **Navn** skal du skrive **\$TransType**.
    5. Vælg **Rediger formel**.
    6. Skriv **LedgerTransTypeList** i feltet **Formel**.
    7. Vælg **Gem**.
    8. Luk siden **Formeleditor**.
    9. Klik på **OK**.

3. Udfør følgende trin for at cachelagre feltet **\$TransType**:

    1. Vælg elementet **LedgerTransTypeList**.
    2. Vælg **Cache**.
    3. Vælg elementet **VendTable.\$TransType**.
    4. Vælg **Cache**.

    ![Konfigurere cachelagring for feltet $TransType](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. Udfør følgende trin for at ændre feltet **\$TransTypeRecord**, så det begynder at bruge det cachelagrede felt **\$TransType**:

    1. Udvid elementet **VendTable** i ruden **Datakilder**, udvid **\<Relationer**-elementet, udvid **VendTrans.VendTable\_AccountNum**, og vælg elementet **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.
    2. Vælg **Rediger**.
    3. Vælg **Rediger formel**.
    4. Find følgende udtryk i feltet **Formel**:

        FIRSTORNULL (HVOR (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))

    5. Angiv følgende udtryk i feltet **Formel**:

        FIRSTORNULL (HVOR (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).

    6. Vælg **Gem**.
    7. Luk siden **Formeleditor**.
    8. Vælg **OK**.

5. Vælg **Gem**.
6. Luk siden **Modeltilknytningsdesigner**.
7. Luk siden **Modeltilknytninger**.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>Fuldføre den ændrede version af ER-modeltilknytningen

1. I RCS på siden **Konfigurationer** skal du i oversigtspanelet **Versioner** vælge version **1.2** af konfigurationen af **Tilknytning af performancesporing**.
2. Vælg **Skift status**.
3. Vælg **Fuldfør**.

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a>Importere konfigurationen af den ændrede modeltilknytning fra RCS til programmet

Gentag trinnene i afsnittet [Importere en ER-konfiguration fra RCS til Finance and Operations](#import-configuration) tidligere i dette emne for at importere version 1.2 af **Tilknytning af performancesporing**-konfigurationen.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Køre den ændrede ER-løsning for at spore kørslen

### <a name="run-the-er-format"></a>Køre ER-formatet

Gentag trinnene i afsnittet [Køre ER-formatet](#run-format) tidligere i dette emne for at generere en ny performancesporing.

## <a name="work-with-the-execution-trace"></a>Arbejde med sporingen af udførelsen

### <a name="export-the-generated-trace-from-the-application"></a>Eksportere den genererede sporing fra programmet

Gentag trinnene i afsnittet [Eksportere den genererede sporing fra programmet](#export-trace) tidligere i dette emne, hvis du vil gemme en ny performancesporing lokalt.

### <a name="import-the-generated-trace-into-rcs"></a>Import af den genererede sporing i RCS

Gentag trinnene i afsnittet [Importere de genererede sporinger i RCS](#import-trace) tidligere i dette emne for at importere den nye performancesporing til RCS.

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a>Bruge performancesporing til analyse i RCS – modeltilknytning

Gentag trinnene i afsnittet [Bruge performancesporing til analyse i RCS – modeltilknytning](#use-trace) tidligere i dette emne for at analysere den seneste performancesporing.

Bemærk, at de justeringer, du har foretaget for modeltilknytningen, har elimineret dubletter af forespørgsler til databasen. Antallet af kald til databasetabeller og datakilder for denne modeltilknytning er også blevet reduceret. Derfor er ydeevnen i hele ER-løsningen forbedret.

![Spore oplysninger for VendTable-datakilde i RCS på siden Modeltilknytningsdesigner](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

I sporingsoplysningerne angiver værdien **\[12\]** for datakilden VendTable, at denne datakilde blev kaldt 12 gange. Værdien **\[Q:6\]** angiver, at seks kald blev oversat til databasekald til tabellen VendTable. Værdien **\[C:6\]** angiver, at de poster, der blev hentet fra databasen, blev cachelagret, og seks andre kald blev behandlet ved hjælp af cachen.

Bemærk, at antallet af kald til datakilden LedgerTransTypeList er blevet reduceret fra 9.027 til 240.

![Spore oplysninger for LedgerTransTypeList-datakilde i RCS på siden Modeltilknytningsdesigner](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a>Gennemse udførelsessporingen i programmet

Foruden RCS kan nogle versioner af tilbyde funktioner til ER-strukturdesigner. Disse versioner har indstillingen **Aktivér designtilstand**, der kan slås til. Du kan finde denne indstilling under fanen **Generelt** på siden **Parametre til elektronisk rapportering**, som du kan åbne fra arbejdsområdet **Elektronisk rapportering**.

![Aktivere indstillingen designtilstand på siden med parametre for elektronisk rapportering](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

Hvis du bruger en af disse versioner, kan du analysere detaljerne for genererede performancesporinger direkte i programmet. Du behøver ikke at eksportere dem fra programmet og importere dem til RCS.

## <a name="review-the-execution-trace-by-using-external-tools"></a>Gennemse kørselssporing ved hjælp af eksterne værktøjer

### <a name="configure-user-parameters"></a>Konfigurere brugerparametre

1. Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.
2. På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
3. Vælg **PerfView XML** i feltet **Udførelsessporingsformat** i afsnittet **Kørselssporing** i dialogboksen **Brugerparametre**.

### <a name="run-the-er-format"></a>Køre ER-formatet

Gentag trinnene i afsnittet [Køre ER-formatet](#run-format) tidligere i dette emne for at generere en ny performancesporing.

Bemærk, at webbrowseren kan hente en zip-fil til overførsel. Denne fil indeholder performancesporingen i PerfView-format. Du kan derefter bruge værktøjet PerfView-performanceanalyse til at analysere detaljerne i ER-formatkørslen.

![Oplysninger om performancesporing i PerfView-format](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a>Brug eksterne værktøjer til at gennemse en udførelsessporing, der indeholder databaseforespørgsler

På grund af de forbedringer, der er foretaget i ER-strukturen, indeholder den performancesporing, der er genereret i PerfView-format, nu flere detaljer om udførelse af ER-format. I Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (juli 2019) kan denne sporing også omfatte oplysninger om udførte SQL-forespørgsler i programdatabasen.

### <a name="configure-user-parameters"></a>Konfigurere brugerparametre

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
3. Angiv følgende parametre i sektionen **Kørselssporing** i dialogboksen **Brugerparametre**:

    - I feltet **Udførelsessporingsformat** skal du vælge **PerfView XML**.
    - Angiv indstillingen **Indsaml forespørgselsstatistikker** til **Ja**.
    - Angiv indstillingen **Sporingsforespørgsel** til **Ja**.

    ![Sektionen Sporing af udførelse, dialogboksen Brugerparametre](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a>Køre ER-formatet

Gentag trinnene i afsnittet [Køre ER-formatet](#run-format) tidligere i dette emne for at generere en ny performancesporing.

Bemærk, at webbrowseren kan hente en zip-fil til overførsel. Denne fil indeholder performancesporingen i PerfView-format. Du kan derefter bruge værktøjet PerfView-performanceanalyse til at analysere detaljerne i ER-formatkørslen. Denne sporing indeholder nu oplysninger om SQL-databaseadgang under udførelsen af ER-formatet.

![Sporingsoplysninger om det udførte ER-format i PerfView](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering](general-electronic-reporting.md)
- [Forbedre ydeevnen af ER-løsninger ved at tilføje parameteriserede BEREGNET FELT-datakilder](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]