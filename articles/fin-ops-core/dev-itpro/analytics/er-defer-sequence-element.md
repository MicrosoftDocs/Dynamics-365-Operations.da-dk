---
title: Udskyde udførelse af sekvenselementer i ER-formater
description: Dette emne forklarer, hvordan du udskyder udførelsen af et sekvenselement i et elektronisk rapporteringsformat (ER).
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-01
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 2af6c95e459246f25574860dc319928380d06cc9fd4fdb68f42203f943b4d386
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718409"
---
# <a name="defer-the-execution-of-sequence-elements-in-er-formats"></a>Udskyde udførelse af sekvenselementer i ER-formater

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Oversigt

Du kan bruge Operationsdesigner i [den elektroniske rapporteringsstruktur (ER)](general-electronic-reporting.md) til at [konfigurere](tasks/er-format-configuration-2016-11.md) [formatkomponenten](general-electronic-reporting.md#FormatComponentOutbound) i en ER-løsning, der bruges til at generere udgående dokumenter i et tekstformat. Den hierarkiske struktur i den konfigurerede formatkomponent består af formatelementer af forskellige typer. Disse formatelementer bruges til at udfylde genererede dokumenter med de nødvendige oplysninger på kørselstidspunktet. Når du kører et ER-format, køres formatelementerne som standard i samme sekvens, som de vises i i formathierarkiet: én ad gangen, fra top mod bund. Men på designtidspunktet kan du ændre udførelsessekvensen for alle sekvenselementer i den konfigurerede formatkomponent.

Hvis du aktiverer indstillingen <a name="DeferredSequenceExecution"></a>**Udskudt udførelse** for et sekvensformatelement i det konfigurerede format, kan du udskyde udførelsen af det pågældende element. I dette tilfælde køres elementet ikke, før alle andre elementer af det overordnede element er blevet kørt.

Hvis du vil vide mere om denne funktion, skal du fuldføre eksemplet i dette emne.

## <a name="limitations"></a>Begrænsninger

Indstillingen **Udskudt udførelse** understøttes kun for sekvenselementer, der er konfigureret til et ER-format, der bruges til at generere **udgående** dokumenter i tekstformat.

Indstillingen **Udskudt udførelse** kan ikke anvendes til sekvenser, der er konfigureret som tilpassede sekvenser, hvor den maksimale længde er begrænset.

## <a name="example-defer-the-execution-of-a-sequence-element-in-an-er-format"></a><a name="Example"></a>Eksempel: Udskyde udførelse af et sekvenselement i et ER-format

I følgende fremgangsmåde forklares det, hvordan en bruger i systemadministratoren eller den funktionelle konsulent i elektronisk rapportering [rolle](../sysadmin/tasks/assign-users-security-roles.md) kan konfigurere et ER-format, der indeholder et sekvenselement, hvor udførelsessekvensen er forskellig fra sekvensen i formathierarkiet.

Disse trin kan udføres i firmaet **USMF** i Microsoft Dynamics 365 Finance.

### <a name="prerequisites"></a>Forudsætninger

For at fuldføre dette eksempel skal du have adgang til **USMF**-firmaet i Finans i en af følgende roller:

- Funktionel konsulent i elektronisk rapportering
- Systemadministrator

Hvis du endnu ikke har fuldført eksemplet i emnet [Udskyde udførelse af XML-elementer i ER-formater](er-defer-xml-element.md#Example), skal du hente følgende [konfigurationer](general-electronic-reporting.md#Configuration) af ER-eksempelløsningen.

| Indholdsbeskrivelse            | Filnavn |
|--------------------------------|-----------|
| ER-datamodelkonfiguration    | [Model til at lære udskudte elementer.version.1.xml](https://download.microsoft.com/download/7/6/0/760933ca-4ac3-4f50-bc0c-c35e596ee066/Modeltolearndeferredelements.version.1.xml) |
| ER-modeltilknytningskonfiguration | [Tilknytning for at lære udskudte elementer.version.1.1.xml](https://download.microsoft.com/download/c/9/c/c9c4b9dd-b700-4385-a087-a84ce9fc1d0f/Mappingtolearndeferredelements.version.1.1.xml) |

Før du går i gang, skal du også hente og gemme følgende konfiguration af ER-eksempelløsningen.

| Indholdsbeskrivelse     |Filnavn |
|-------------------------|----------|
| Konfiguration af ER-format | [Format til at lære udskudte sekvenser.version.1.1.xml](https://download.microsoft.com/download/0/f/5/0f55c341-8285-4d92-a46d-475d9a010927/Formattolearndeferredsequences.version.1.1.xml) |

### <a name="import-the-sample-er-configurations"></a>Importere ER-eksempelkonfigurationerne

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. Vælg **Rapporteringskonfigurationer**.
3. Hvis konfigurationen **Model til at lære udskudte elementer** på siden **Konfigurationer** ikke er tilgængelig i konfigurationstræet, skal du importere ER-datamodelkonfigurationen:

    1. Vælg **Exchange**, og vælg derefter **Indlæs fra XML-fil**.
    2. Vælg **Gennemse**, find og vælg filen **Model til at lære udskudte elementer.1.xml**, og vælg derefter **OK**.

4. Hvis konfigurationen **Tilknytning for at lære udskudte elementer** ikke er tilgængelig i konfigurationstræet, skal du importere ER-modeltilknytningskonfigurationen:

    1. Vælg **Exchange**, og vælg derefter **Indlæs fra XML-fil**.
    2. Vælg **Gennemse**, find og vælg filen **Tilknytning for at lære udskudte elementer.1.1.xml**, og vælg derefter **OK**.

5. Importere ER-formatkonfigurationen:

    1. Vælg **Exchange**, og vælg derefter **Indlæs fra XML-fil**.
    2. Vælg **Gennemse**, find og vælg filen **Format til at lære udskudte sekvenser.1.1.xml**, og vælg derefter **OK**.

6. Udvid **Model til at lære udskudte elementer** i konfigurationstræet.
7. Gennemse listen over importerede ER-konfigurationer i konfigurationstræet.

    ![Importerede ER-konfigurationer på siden Konfigurationer.](./media/ER-DeferredSequence-Configurations.png)

### <a name="activate-a-configurations-provider"></a>Aktivere en konfigurationsudbyder

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** i sektionen **Konfigurationsudbydere** skal du kontrollere, at [konfigurationsudbyderen](general-electronic-reporting.md#Provider) for eksempelfirmaet Litware, Inc. (`http://www.litware.com`) er vist, og at det er markeret som aktivt. Hvis denne konfigurationsudbyder ikke er angivet, eller hvis den ikke er markeret som aktiv, skal du følge trinnene i emnet [Opret en konfigurationsudbyder, og markér den som aktiv](./tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![Eksempelfirmaet Litware, Inc. på siden Lokaliseringskonfigurationer.](./media/ER-DeferredSequence-ElectronicReportingWorkspace.png)

### <a name="review-the-imported-model-mapping"></a>Gennemse tilknytningen af den importerede model

Gennemse indstillingerne for komponenten til ER-modeltilknytning, der er konfigureret til at få adgang til momstransaktioner og vise data, der er adgang til, på anmodning.

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. Vælg **Rapporteringskonfigurationer**.
3. På siden **Konfigurationer** skal du i konfigurationstræet udvide **Model til at lære udskudte elementer**.
4. Vælg konfigurationen **Tilknytning for at lære udskudte elementer**.
5. Vælg **Designer** for at åbne listen over tilknytninger.
6. Vælg **Designer** for at gennemgå tilknytningsdetaljerne.
7. Vælg **Vis detaljer**.
8. Gennemse de datakilder, der er konfigureret til at få adgang til momstransaktioner:

    - Datakilden **Transaktioner** for typen *Tabelpost* er konfigureret til at få adgang til poster i programtabellen **TaxTrans**.
    - Datakilden **Bilag** for typen *Beregnet felt* er konfigureret til at returnere de påkrævede bilagskoder (**INV-10000349** og **INV-10000350**) som en liste over poster.
    - Datakilden **Filtreret** for typen *Beregnet felt* er konfigureret til kun at vælge momstransaktionerne for de påkrævede bilag fra datakilden **Transaktioner**.
    - Feltet **\$TaxAmount** for typen *Beregnet felt* type tilføjes for datakilden **Filtreret** for at vise momsværdien, der har modsat fortegn.
    - Datakilden **Grupperet** for typen *Gruppér efter* er konfigureret til at gruppere filtrerede momstransaktioner for datakilden **Filtreret**.
    - Aggregeringsfeltet **TotalSum** i datakilden **Grupperet** er konfigureret til at opsummere værdier i feltet **\$TaxAmount** i datakilden **Filtreret** for alle filtrerede momstransaktioner for den pågældende datakilde.

        ![Aggregeringsfeltet TotalSum på siden Rediger 'GroupBy'-parametre.](./media/ER-DeferredSequence-GroupByParameters.png)

9. Gennemse, hvordan de konfigurerede datakilder er bundet til datamodellen, og hvordan de viser data, der er adgang til, for at gøre dem tilgængelige i et ER-format:

    - Datakilden **Filtreret** er bundet til feltet **Data.List** i datamodellen.
    - Feltet **\$TaxAmount** i datakilden **Filtreret** er bundet til feltet **Data.List.Value** i datamodellen.
    - Feltet **TotalSum** i datakilden **Grupperet** er bundet til feltet **Data.Summary.Total** i datamodellen.

    ![Siden Modeltilknytningsdesigner.](./media/ER-DeferredSequence-ModelMapping.png)

10. Luk siderne **Modeltilknytningsdesigner** og **Modeltilknytninger**.

### <a name="review-the-imported-format"></a>Gennemse det importerede format

1. På siden **Konfigurationer** skal du vælge konfigurationen **Format til at lære udskudte sekvenser** i konfigurationstræet.
2. Vælg **Designer** for at gennemgå formatdetaljerne.
3. Vælg **Vis detaljer**.
4. Gennemse indstillingerne for de ER-formatkomponenter, der er konfigureret til at generere et udgående dokument i tekstformat, der indeholder oplysninger om momstransaktionerne:

    - Sekvensformatelementet **Rapport\\Linjer** er konfigureret til at udfylde det udgående dokument med en enkelt linje, der genereres fra de indlejrede sekvensformatelementer (**Overskrift**, **Post** og **Oversigt**).

        ![Linjesekvensformatelement og indlejrede elementer på siden Formatdesigner.](./media/ER-DeferredSequence-Format.png)

    - Sekvensformatelementet **Rapport\\Linjer\\Overskrift** er konfigureret til at udfylde det udgående dokument med en enkelt overskriftslinje, der viser den dato og det klokkeslæt, hvor behandlingen igangsættes.
    - Sekvensformatelementet **Rapport \\Linjer\\Post** er konfigureret til at udfylde det udgående dokument med en enkelt linje, der viser detaljerne i de enkelte momstransaktioner. Disse momstransaktioner er adskilt af semikolon.

        ![Formatelement for postsekvens, der bruger et semikolon som afgrænsningstegn.](./media/ER-DeferredSequence-Format1.png)

    - Sekvensformatelementet **Rapport\\Linjer\\Oversigt** er konfigureret til at udfylde det udgående dokument med en enkelt oversigtslinje, der omfatter summen af momsværdierne fra de behandlede momstransaktioner.

4. Gennemse følgende oplysninger under fanen **Tilknytning**:

    - Elementet **Rapport\\Linjer\\Overskrift** behøver ikke at være bundet til en datakilde, for at der kan oprettes en enkelt linje i et udgående dokument.
    - Elementet **Prefix1** opretter **P1**-symboler for at angive, at den linje, der tilføjes, er overskriftslinjen i rapporten.
    - Elementet **ExecutionDateTime** genererer datoen og klokkeslættet (herunder millisekunder), når overskriftslinjen tilføjes.
    - Elementet **Rapport\\Linjer\\Post** er bundet til listen **model.Data.List** for at oprette en enkelt linje for hver post på den bundne liste.
    - Elementet **Prefix2** opretter **P2**-symboler for at angive, at den linje, der tilføjes, er til oplysningerne om momstransaktionen.
    - Elementet **TaxAmount** er bundet til **model.Data.List.Value** (som vises som **\@.Value** i visningen af den relative sti) til at generere momsværdien for den aktuelle momstransaktion.
    - Elementet **RunningTotal** er pladsholder for den løbende total for momsværdierne. I øjeblikket har dette element intet output, fordi der ikke er konfigureret en binding eller en standardværdi for det.
    - Elementet **ExecutionDateTime** genererer datoen og klokkeslættet (herunder millisekunder), når den aktuelle transaktion behandles i denne rapport.
    - Elementet **Rapport\\Linjer\\Oversigt** behøver ikke at være bundet til en datakilde, for at der kan oprettes en enkelt linje i et udgående dokument.
    - Elementet **Prefix3** opretter **P3**-symboler for at angive, at den linje, der tilføjes, indeholder den samlede momsværdi.
    - Elementet **TotalTaxAmount** er bundet til **model.Data.Summary.Total** for at generere summen af momsværdierne for de behandlede momstransaktioner.
    - Elementet **ExecutionDateTime** genererer datoen og klokkeslættet (herunder millisekunder), når oversigtslinjen tilføjes.

    ![Fanen Tilknytning på siden Formatdesigner.](./media/ER-DeferredSequence-Format2.png)

### <a name="run-the-imported-format"></a>Kør det importerede format

1. På siden **Formatdesigner** skal du vælge **Kør**.
2. Hent den fil, som webbrowseren tilbyder, og åbn den til gennemsyn.

    ![Hentet eksempelrapportfil.](./media/ER-DeferredSequence-Run.png)

Bemærk, at oversigtslinje 22 præsenterer summen af momsværdierne for de behandlede transaktioner. Da formatet er konfigureret til at bruge bindingen **model.Data.Summary.Total** til at returnere denne sum, beregnes summen ved at kalde aggregeringen **TotalSum** for datakilden **Grupperet** for typen *GroupBy*, der bruger modeltilknytningen. Hvis du vil beregne denne aggregering, gentages modeltilknytningen over alle de transaktioner, der er valgt i datakilden **Filtreret**. Ved at sammenligne udførselstiderne i linje 21 og 22 kan du fastlægge, at beregningen af summen har taget 10 millisekunder (ms). Ved at sammenligne udførselstiderne i linje 2 og 21 kan du fastlægge, at oprettelse af alle transaktionslinjer har taget 7 ms. Der kræves derfor 17 ms i alt.

### <a name="modify-the-format-so-that-the-summing-is-based-on-generated-output"></a>Rediger formatet, så summeringen er baseret på genereret output

Hvis mængden af transaktioner er meget større end mængden i det aktuelle eksempel, kan opsummeringstiden stige og medføre problemer med ydeevnen. Hvis du ændrer indstillingen af formatet, kan du afhjælpe disse problemer med ydeevnen. Da du har adgang til momsværdier for at medtage dem i den genererede rapport, kan du genbruge disse oplysninger til at summere momsværdier. Du kan finde flere oplysninger i [Konfigurere format for at udføre optælling og sammenlægning](./tasks/er-format-counting-summing-1.md).

1. På siden **Formatdesigner** under fanen **Format** skal du vælge filelementet **Rapport** i formattræet.
2. Angiv indstillingen **Detaljer om indsamlingsoutput** til **Ja**. Du kan nu konfigurere dette format ved at bruge indholdet af en eksisterende rapport som en datakilde, der kan åbnes ved hjælp af de indbyggede ER-funktioner i kategorien [Dataindsamling](er-functions-category-data-collection.md).
3. Vælg sekvenselementet **Rapport\\Linjer** under fanen **Tilknytning**.
4. Konfigurer udtrykket **Nøglenavn for opsamlede data** som `WsColumn`.
5. Konfigurer udtrykket **Nøgleværdi for opsamlede data** som `WsRow`.

    ![Linjesekvenselement på siden Formatdesigner.](./media/ER-DeferredSequence-Format3.png)

6. Vælg det numeriske element **Rapport\\Linjer\\Post\\TaxAmount**.
7. Konfigurer udtrykket **Nøglenavn for opsamlede data** som `SummingAmountKey`.

    ![Det numeriske element TaxAmount på siden Formatdesigner.](./media/ER-DeferredSequence-Format4.png)

    Du kan overveje denne indstilling ved at udfylde et virtuelt regneark, hvor værdien af celle A1 tilføjes sammen med værdien af momsbeløbet fra alle behandlede momstransaktioner.

8. Vælg det numeriske element **Rapport\\Linjer\\Post\\RunningTotal**, og vælg derefter **Rediger formel**.
9. Konfigurer udtrykket `SUMIF(SummingAmountKey, WsColumn, WsRow)` ved hjælp af den indbyggede [SUMIF](er-functions-datacollection-sumif.md) ER-funktion.
10. Vælg **Gem**.

    ![SUMIF-udtryk.](./media/ER-DeferredSequence-FormulaDesigner.png)

11. Luk siden **Formeldesigner**.
12. Vælg **Gem**, og vælg derefter **Kør**.
13. Download og gennemse den fil, som webbrowseren tilbyder.

    ![Hentet fil – Opsummerede momsværdier.](./media/ER-DeferredSequence-Run1.png)

    Linje 21 indeholder den løbende total af momsværdier, der er beregnet for alle behandlede transaktioner ved brug af det genererede output som datakilde. Denne datakilde starter fra starten af rapporten og fortsætter gennem den seneste momstransaktion. Linje 22 indeholder summen af momsværdierne for alle behandlede transaktioner, der er beregnet i modeltilknytningen ved hjælp af datakilden af typen *GroupBy*. Bemærk, at disse værdier er ens. Derfor kan den outputbaserede opsummering bruges i stedet for **GroupBy**. Ved at sammenligne udførselstiderne i linje 2 og 21 kan du fastlægge, at oprettelse af alle transaktionslinjer og opsummering har taget 9 ms. Så vidt angår oprettelse af detaljerede linjer og opsummering af momsværdier, er det ændrede format ca. to gange hurtigere end det oprindelige format.

14. Vælg det numeriske element **Rapport\\Linjer\\Oversigt\\TotalTaxAmount**, og vælg derefter **Rediger formel**.
15. Angiv udtrykket `SUMIF(SummingAmountKey, WsColumn, WsRow)` i stedet for det eksisterende udtryk.
16. Vælg **Gem**, og vælg derefter **Kør**.
17. Download og gennemse den fil, som webbrowseren tilbyder.

    ![Hentet fil med redigeret formel.](./media/ER-DeferredSequence-Run2.png)

    Bemærk, at den løbende total for momsværdier på den sidste linje med transaktionsdetaljer nu svarer til summen på opsummeringslinjen.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Placer værdier fra outputbaseret opsummering i rapporthovedet

Hvis du f.eks. skal vise summen af momsværdier i hovedet i din rapport, kan du ændre formatet.

1. På siden **Formatdesigner** under fanen **Format** skal du vælge sekvenselementet **Rapport\\Linjer\\Oversigt**.
2. Vælg **Flyt op**.
3. Vælg **Gem**, og vælg derefter **Kør**.
4. Download og gennemse den fil, som webbrowseren tilbyder.

    ![Hentet fil til opsummering i rapporthoved.](./media/ER-DeferredSequence-Run3.png)

    Bemærk, at summen af momsværdier på oversigtslinje 2 nu er lig med 0 (nul), fordi denne sum nu beregnes ud fra det genererede output. Når linje 2 genereres, indeholder det genererede output endnu ikke linjer med transaktionsdetaljer. Du kan konfigurere dette format for at udskyde udførelsen af sekvenselementet **Rapport\\Linjer\\Oversigt**, indtil sekvenselementet **Rapport\\Linjer\\Post** er kørt for alle momstransaktionerne.

### <a name="defer-the-execution-of-the-summary-sequence-so-that-the-calculated-total-is-used"></a>Udskyde udførelsen af opsummeringssekvensen, så den beregnede total bruges

1. På siden **Formatdesigner** under fanen **Format** skal du vælge sekvenselementet **Rapport\\Linjer\\Oversigt**.
2. Angiv indstillingen **Udskudt udførelse** til **Ja**.

    ![Indstillingen Udskudt udførelse for sekvenselementet Opsummering på siden Formatdesigner.](./media/ER-DeferredSequence-Format5.png)

3. Vælg **Gem**, og vælg derefter **Kør**.
4. Download og gennemse den fil, som webbrowseren tilbyder.

    ![Hentet fil – udskudt udførelse.](./media/ER-DeferredSequence-Run4.png)

    Sekvenselementet **Rapport\\Linjer\\Oversigt** køres nu kun, efter alle andre elementer, der er indlejret under det overordnede element **Rapport\\Linjer**, er kørt. Derfor køres det, efter at sekvenselementet **Rapport\\Linjer\\Post** er kørt for alle momstransaktioner i datakilden **model.Data.List**. Udførelsestiderne for linje 1, 2 og 3 og for den sidste linje, 22, viser denne oplysning.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Konfigurere format for at udføre optælling og sammenlægning](./tasks/er-format-counting-summing-1.md)
- [Spore kørsel af ER-format for at foretage fejlfinding af problemer med ydeevnen](trace-execution-er-troubleshoot-perf.md)
- [Udskyde udførelse af XML-elementer i ER-formater](er-defer-xml-element.md#Example)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
