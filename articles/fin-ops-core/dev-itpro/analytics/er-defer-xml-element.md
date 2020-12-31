---
title: Udskyde udførelse af XML-elementer i ER-formater
description: Dette emne forklarer, hvordan du udskyder udførelsen af et XLM-element i et elektronisk rapporteringsformat (ER).
author: NickSelin
manager: kfend
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 6dce3768c886403f789063d516e0e696fc829f81
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680704"
---
# <a name="defer-the-execution-of-xml-elements-in-er-formats"></a>Udskyde udførelse af XML-elementer i ER-formater

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Oversigt

Du kan bruge Operationsdesigner i [den elektroniske rapporteringsstruktur (ER)](general-electronic-reporting.md) til at [konfigurere](./tasks/er-format-configuration-2016-11.md) [formatkomponenten](general-electronic-reporting.md#FormatComponentOutbound) i en ER-løsning, der bruges til at generere udgående dokumenter i XLM-format. Den hierarkiske struktur i den konfigurerede formatkomponent består af formatelementer af forskellige typer. Disse formatelementer bruges til at udfylde genererede dokumenter med de nødvendige oplysninger på kørselstidspunktet. Når du kører et ER-format, køres formatelementerne som standard i samme sekvens, som de vises i i formathierarkiet: én ad gangen, fra top mod bund. Men på designtidspunktet kan du ændre udførelsessekvensen for alle XML-elementer i den konfigurerede formatkomponent.

Hvis du aktiverer indstillingen <a name="DeferredXmlElementExecution"></a>**Udskudt udførelse** for et XML-element i det konfigurerede format, kan du udskyde udførelsen af det pågældende element. I dette tilfælde køres elementet ikke, før alle andre elementer af det overordnede element er blevet kørt.

Hvis du vil vide mere om denne funktion, skal du fuldføre eksemplet i dette emne.

## <a name="limitations"></a>Begrænsninger

Indstillingen **Udskudt udførelse** understøttes kun for XML-elementer, der er konfigureret til et ER-format, der bruges til at generere **udgående** dokumenter i XML-format.

Indstillingen **Udskudt udførelse** understøttes kun for XML-elementer, der kun findes i ét andet XML-element. Derfor kan den ikke anvendes til XML-elementer, der er placeret i andre typer formatelementer (f.eks. i et **XML-sekvens**-element).

Indstillingen **Udskudt udførelse** understøttes ikke for XML-elementer, der findes i formatelementet **Almindelig\\Fil**, når indstillingen **Opdel fil** er angivet til **Ja**. Du kan finde flere oplysninger om, hvordan du opdeler XML-filer, i [Opdele genererede XML-filer ud fra filstørrelse og indholdsmængde](er-split-files.md).

## <a name="example-defer-the-execution-of-an-xml-element-in-an-er-format"></a><a name="Example"></a>Eksempel: Udskyde udførelse af et XML-element i et ER-format

I følgende fremgangsmåde forklares det, hvordan en bruger i systemadministratoren eller den funktionelle konsulent i elektronisk rapportering [rolle](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/tasks/assign-users-security-roles) kan konfigurere et ER-format, der indeholder et XML-element, hvor udførelsessekvensen er forskellig fra sekvensen i formathierarkiet.

Disse trin kan udføres i firmaet **USMF** i Microsoft Dynamics 365 Finance.

### <a name="prerequisites"></a>Forudsætninger

For at fuldføre dette eksempel skal du have adgang til **USMF**-firmaet i Finans i en af følgende roller:

- Funktionel konsulent i elektronisk rapportering
- Systemadministrator

Hvis du endnu ikke har fuldført eksemplet i emnet [Udskyde udførelse af sekvenselementer i ER-formater](er-defer-sequence-element.md#Example), skal du hente følgende [konfigurationer](general-electronic-reporting.md#Configuration) af ER-eksempelløsningen.

| Indholdsbeskrivelse            | Filnavn |
|--------------------------------|-----------|
| ER-datamodelkonfiguration    | [Model til at lære udskudte elementer.version.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| ER-modeltilknytningskonfiguration | [Tilknytning for at lære udskudte elementer.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

Før du går i gang, skal du også hente og gemme følgende konfiguration af ER-eksempelløsningen på den lokale computer.

| Indholdsbeskrivelse     | Filnavn |
|-------------------------|-----------|
| Konfiguration af ER-format | [Format til at lære udskudte XML-elementer.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

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
    2. Vælg **Gennemse**, find og vælg filen **Format til at lære udskudte XML-elementer.1.1.xml**, og vælg derefter **OK**.

6. Udvid **Model til at lære udskudte elementer** i konfigurationstræet.
7. Gennemse listen over importerede ER-konfigurationer i konfigurationstræet.

    ![Importerede ER-konfigurationer på siden Konfigurationer](./media/ER-DeferredXml-Configurations.png)

### <a name="activate-a-configuration-provider"></a>Aktivere en konfigurationsudbyder

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** i sektionen **Konfigurationsudbydere** skal du kontrollere, at [konfigurationsudbyderen](general-electronic-reporting.md#Provider) for eksempelfirmaet Litware, Inc. (`http://www.litware.com`) er vist, og at det er markeret som aktivt. Hvis denne konfigurationsudbyder ikke er angivet, eller hvis den ikke er markeret som aktiv, skal du følge trinnene i emnet [Opret en konfigurationsudbyder, og markér den som aktiv](./tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![Eksempelfirmaet Litware, Inc. på siden Lokaliseringskonfigurationer](./media/ER-DeferredXml-ElectronicReportingWorkspace.png)

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

        ![Aggregeringsfeltet TotalSum på siden Rediger 'GroupBy'-parametre](./media/ER-DeferredXml-GroupByParameters.png)

9. Gennemse, hvordan de konfigurerede datakilder er bundet til datamodellen, og hvordan de viser data, der er adgang til, for at gøre dem tilgængelige i et ER-format:

    - Datakilden **Filtreret** er bundet til feltet **Data.List** i datamodellen.
    - Feltet **\$TaxAmount** i datakilden **Filtreret** er bundet til feltet **Data.List.Value** i datamodellen.
    - Feltet **TotalSum** i datakilden **Grupperet** er bundet til feltet **Data.Summary.Total** i datamodellen.

    ![Siden Modeltilknytningsdesigner](./media/ER-DeferredXml-ModelMapping.png)

10. Luk siderne **Modeltilknytningsdesigner** og **Modeltilknytninger**.

### <a name="review-the-imported-format"></a>Gennemse det importerede format

1. På siden **Konfigurationer** skal du vælge konfigurationen **Format til at lære udskudte XML-elementer** i konfigurationstræet.
2. Vælg **Designer** for at gennemgå formatdetaljerne.
3. Vælg **Vis detaljer**.
4. Gennemse indstillingerne for de ER-formatkomponenter, der er konfigureret til at generere et udgående dokument i XML-format, der indeholder oplysninger om momstransaktionerne:

    - XML-elementet **Rapport\\Meddelelse** er konfigureret til at udfylde det udgående dokument med en enkelt node, der indeholder de indlejrede XML-elementer (**Overskrift**, **Post** og **Oversigt**).
    - XML-elementet **Rapport\\Meddelelse\\Overskrift** er konfigureret til at udfylde det udgående dokument med en enkelt overskriftsnode, der viser den dato og det klokkeslæt, hvor behandlingen igangsættes.
    - XML-elementet **Rapport \\Meddelelse\\Post** er konfigureret til at udfylde det udgående dokument med en enkelt postnode, der viser detaljerne i en enkelt momstransaktion.
    - XML-elementet **Rapport\\Meddelelse\\Oversigt** er konfigureret til at udfylde det udgående dokument med en enkelt oversigtsnode, der omfatter summen af momsværdierne fra de behandlede momstransaktioner.

    ![Meddelelses-XML-element og indlejrede XML-elementer på siden Formatdesigner](./media/ER-DeferredXml-Format.png)

5. Gennemse følgende oplysninger under fanen **Tilknytning**:

    - Elementet **Rapport\\Meddelelse\\Overskrift** behøver ikke at være bundet til en kilde, for at der kan oprettes en enkelt node i et udgående dokument.
    - Attributten **ExecutionDateTime** genererer datoen og klokkeslættet (herunder millisekunder), når overskriftsnoden tilføjes.
    - Elementet **Rapport\\Meddelelse\\Post** er bundet til listen **model.Data.List** for at oprette en enkelt postnode for hver post på den bundne liste.
    - Attributten **TaxAmount** er bundet til **model.Data.List.Value** (som vises som **\@.Value** i visningen af den relative sti) til at generere momsværdien for den aktuelle momstransaktion.
    - Attributten **RunningTotal** er pladsholder for den løbende total for momsværdierne. I øjeblikket har denne attribut intet output, fordi der ikke er konfigureret en binding eller en standardværdi for den.
    - Attributten **ExecutionDateTime** genererer datoen og klokkeslættet (herunder millisekunder), når den aktuelle transaktion behandles i denne rapport.
    - Elementet **Rapport\\Meddelelse\\Oversigt** behøver ikke at være bundet til en datakilde, for at der kan oprettes en enkelt node i et udgående dokument.
    - Attributten **TotalTaxAmount** er bundet til **model.Data.Summary.Total** for at generere summen af momsværdierne for de behandlede momstransaktioner.
    - Attributten **ExecutionDateTime** genererer datoen og klokkeslættet (herunder millisekunder), når oversigtsnoden tilføjes.

    ![Fanen Tilknytning på siden Formatdesigner](./media/ER-DeferredXml-Format2.png)

### <a name="run-the-imported-format"></a>Kør det importerede format

1. På siden **Formatdesigner** skal du vælge **Kør**.
2. Hent den fil, som webbrowseren tilbyder, og åbn den til gennemsyn.

    ![Hentet fil](./media/ER-DeferredXml-Run.png)

Bemærk, at oversigtsnoden præsenterer summen af momsværdierne for de behandlede transaktioner. Da formatet er konfigureret til at bruge bindingen **model.Data.Summary.Total** til at returnere denne sum, beregnes summen ved at kalde aggregeringen **TotalSum** for datakilden **Grupperet** for typen *GroupBy* i modeltilknytningen. Hvis du vil beregne denne aggregering, gentages modeltilknytningen over alle transaktioner, der er valgt i datakilden **Filtreret**. Ved at sammenligne udførselstiderne for oversigtsnoden og den sidste postnode kan du fastlægge, at beregningen af summen tog 12 millisekunder (ms). Ved at sammenligne udførselstiderne for den første og sidste postnode kan du fastlægge, at oprettelse af alle postnoder har taget 9 ms. Der kræves derfor 21 ms i alt.

### <a name="modify-the-format-so-that-the-calculation-is-based-on-generated-output"></a>Rediger formatet, så beregningen er baseret på genereret output

Hvis mængden af en transaktion er meget større end mængden i det aktuelle eksempel, kan beregningstiden stige og medføre problemer med ydeevnen. Hvis du ændrer indstillingen af formatet, kan du afhjælpe disse problemer med ydeevnen. Da du har adgang til momsværdier for at medtage dem i den genererede rapport, kan du genbruge disse oplysninger til at beregne momsværdier. Du kan finde flere oplysninger i [Konfigurere format for at udføre optælling og sammenlægning](./tasks/er-format-counting-summing-1.md).

1. På siden **Formatdesigner** under fanen **Format** skal du vælge filelementet **Rapport** i formattræet.
2. Angiv indstillingen **Detaljer om indsamlingsoutput** til **Ja**. Du kan nu konfigurere dette format ved at bruge indholdet af en genereret rapport som en datakilde, der kan åbnes ved hjælp af de indbyggede ER-funktioner i kategorien [Dataindsamling](er-functions-category-data-collection.md).
3. Vælg XML-elementet **Rapport\\Meddelelse\\Post** under mappen **Tilknytning**.
4. Konfigurer udtrykket **Nøglenavn for opsamlede data** som `WsColumn`.
5. Konfigurer udtrykket **Nøgleværdi for opsamlede data** som `WsRow`.

    ![Post-XML-element på siden Formatdesigner](./media/ER-DeferredXml-Format3.png)

6. Vælg attributten **Rapport\\Meddelelse\\Post\\TaxAmount**.
7. Konfigurer udtrykket **Nøglenavn for opsamlede data** som `SummingAmountKey`.

    ![Attributten TaxAmount på siden Formatdesigner](./media/ER-DeferredXml-Format4.png)

    Du kan overveje denne indstilling ved at udfylde et virtuelt regneark, hvor værdien af celle A1 tilføjes sammen med værdien af momsbeløbet fra alle behandlede momstransaktioner.

8. Vælg attributten **Rapport\\Meddelelse\\Post\\RunningTotal**, og vælg derefter **Rediger formel**.
9. Konfigurer udtrykket `SUMIF(SummingAmountKey, WsColumn, WsRow)` ved hjælp af den indbyggede [SUMIF](er-functions-datacollection-sumif.md) ER-funktion, og vælg derefter **Gem**.

    ![SUMIF-udtryk](./media/ER-DeferredXml-FormulaDesigner.png)

10. Luk siden **Formeldesigner**.
11. Vælg **Gem**, og vælg derefter **Kør**.
12. Download og gennemse den fil, som webbrowseren tilbyder.

    ![Hentet fil](./media/ER-DeferredXml-Run1.png)

    Den sidste postnode indeholder den løbende total af momsværdier, der er beregnet for alle behandlede transaktioner ved brug af det genererede output som datakilde. Denne datakilde starter fra starten af rapporten og fortsætter gennem den seneste momstransaktion. Oversigtsnoden indeholder summen af momsværdierne for alle behandlede transaktioner, der er beregnet i modeltilknytningen ved hjælp af datakilden af typen *GroupBy*. Bemærk, at disse værdier er ens. Derfor kan den outputbaserede opsummering bruges i stedet for **GroupBy**. Ved at sammenligne udførselstiderne for den første postnode og oversigtsnoden kan du fastlægge, at oprettelse af alle postnoder og oversigt har taget 11 ms. Så vidt angår oprettelse af postnoder og oversigt over momsværdier, er det ændrede format ca. to gange hurtigere end det oprindelige format.

13. Vælg attributten **Rapport\\Meddelelse\\Oversigt\\TotalTaxAmount**, og vælg derefter **Rediger formel**.
14. Angiv udtrykket `SUMIF(SummingAmountKey, WsColumn, WsRow)` i stedet for det eksisterende udtryk.
15. Vælg **Gem**, og vælg derefter **Kør**.
16. Download og gennemse den fil, som webbrowseren tilbyder.

    ![Hentet fil](./media/ER-DeferredXml-Run2.png)

    Bemærk, at den løbende total for momsværdier i den sidste postnode nu svarer til summen i oversigtsnoden.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Placer værdier fra outputbaseret opsummering i rapporthovedet

Hvis du f.eks. skal vise summen af momsværdier i hovedet i din rapport, kan du ændre formatet.

1. På siden **Formatdesigner** under fanen **Format** skal du vælge XML-elementet **Rapport\\Meddelelse\\Oversigt**.
2. Vælg **Flyt op**.
3. Vælg **Gem**, og vælg derefter **Kør**.
4. Download og gennemse den fil, som webbrowseren tilbyder.

    ![Hentet fil](./media/ER-DeferredXml-Run3.png)

    Bemærk, at summen af momsværdier i oversigtsnoden nu er lig med 0 (nul), fordi denne sum nu beregnes ud fra det genererede output. Når den første postnode genereres, indeholder det genererede output endnu ikke postnoder med transaktionsdetaljer. Du kan konfigurere dette format for at udskyde udførelsen af elementet **Rapport\\Meddelelse\\Oversigt**, indtil elementet **Rapport\\Meddelelse\\Post** er kørt for alle momstransaktionerne.

### <a name="defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used"></a>Udskyde udførelsen af oversigts-XML-elementet, så den beregnede total bruges

1. På siden **Formatdesigner** under fanen **Format** skal du vælge XML-elementet **Rapport\\Meddelelse\\Oversigt**.
2. Angiv indstillingen **Udskudt udførelse** til **Ja**.

    ![Indstillingen Udskudt udførelse for oversigts-XML-elementet på siden Formatdesigner](./media/ER-DeferredXml-Format5.png)

3. Vælg **Gem**, og vælg derefter **Kør**.
4. Download og gennemse den fil, som webbrowseren tilbyder.

    ![Hentet fil](./media/ER-DeferredXml-Run4.png)

    Elementet **Rapport\\Meddelelse\\Oversigt** køres nu kun, efter alle andre elementer, der er indlejret under det overordnede element **Rapport\\Meddelelse**, er kørt. Derfor køres det, efter at elementet **Rapport\\Meddelelse\\Post** er kørt for alle momstransaktioner i datakilden **model.Data.List**. Udførelsestiderne for de første og sidste postnoder og for overskrifts- og oversigtsnoder viser dette.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Konfigurere format for at udføre optælling og sammenlægning](./tasks/er-format-counting-summing-1.md)
- [Spore kørsel af ER-format for at foretage fejlfinding af problemer med ydeevnen](trace-execution-er-troubleshoot-perf.md)
- [Udskyde udførelse af sekvenselementer i ER-formater](er-defer-sequence-element.md#Example)
