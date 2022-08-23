---
title: Designe flersprogede rapporter i elektronisk rapportering
description: Denne artikel forklarer, hvordan du kan bruge elektroniske rapporteringsetiketter (ER) til at designe og generere flersprogede rapporter.
author: kfend
ms.date: 05/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
ms.openlocfilehash: 5575ba3154521e3855ce6b97c5b37d3c4868e3e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285479"
---
# <a name="design-multilingual-reports-in-electronic-reporting"></a>Designe flersprogede rapporter i elektronisk rapportering

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Overblik

Som forretningsbruger kan du benytte strukturen for [Elektronisk rapportering (ER)](general-electronic-reporting.md) til at konfigurere formater for udgående dokumenter, der skal genereres i overensstemmelse med de lovgivningsmæssige krav i forskellige lande/områder. Når disse krav kræver, at udgående dokumenter skal genereres på forskellige sprog til forskellige lande/områder, kan du konfigurere et enkelt ER-format, der indeholder sprogafhængige ressourcer. På denne måde kan du genbruge formatet for at generere udgående dokumenter for forskellige lande/områder. Du kan også bruge et enkelt ER-format til at generere et udgående dokument på forskellige sprog for de tilsvarende kunder, leverandører, datterselskaber eller andre parter.

Du kan konfigurere ER-datamodeller og -modeltilknytninger som datakilder for konfigurerede ER-formater for at definere dataflowet, der angiver, hvilke programdata der skal placeres i genererede dokumenter. Som [udbyder](general-electronic-reporting.md#Provider) af ER-konfigurationer kan du [publicere](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs) konfigurerede datamodeller, modeltilknytninger og formater som komponenter i en ER-løsning for at generere specifikke udgående dokumenter. Du kan også give kunder tilladelse til at [uploade](general-electronic-reporting-manage-configuration-lifecycle.md) den publicerede ER-løsning, så den kan bruges og tilpasses. Hvis du forventer, at kunder måske taler andre sprog, kan du konfigurere ER-komponenterne, så de indeholder sprogafhængige ressourcer. På denne måde kan indholdet af en redigerbar ER-komponent vises på en kundes foretrukne sprog på designtidspunktet.

Du kan konfigurere sprogafhængige ressourcer som ER-etiketter. Du kan derefter bruge disse etiketter til at konfigurere ER-komponenter til følgende formål:

- På designtidspunktet:

    - Præsenter indholdet af konfigurerede ER-komponenter på brugerens foretrukne sprog.

- På kørselstidspunktet:

    - Generer sprogafhængigt indhold for udgående dokumenter.
    - Angiv advarsels- og fejlmeddelelser på brugerens foretrukne sprog.
    - Spørg efter obligatoriske felter på brugerens foretrukne sprog.

ER-etiketter kan konfigureres i hver enkelt ER-[konfiguration](general-electronic-reporting.md#Configuration), der indeholder forskellige komponenter. Etiketterne kan vedligeholdes uafhængigt af den konfigurerede logik i ER-datamodeller, ER-modeltilknytninger og ER-formatkomponenter.

Hver ER-etiket identificeres med et id, der er entydigt i omfanget af den ER-konfiguration, som indeholder den pågældende etiket. Alle etiketter kan indeholde etikettekst til alle sprog, der understøttes i den aktuelle forekomst af Microsoft Dynamics 365 Finance. Disse understøttede sprog omfatter sproget i de installerede tilpasninger.

## <a name="entry"></a>Inddatering

Når du designer en ER-datamodel, en ER-modeltilknytning eller et ER-format, vises indstillingen **Oversæt**, når du vælger et felt, der måske indeholder den kontekst, der kan oversættes. Når du vælger denne indstilling, kan du sammenkæde det valgte felt med en ER-etiket i **Tekstoversættelse**<a name="TextTranslationPane">ruden </a>. Du kan vælge en eksisterende ER-etiket, eller du kan tilføje en ny ER-etiket, hvis den ikke er tilgængelig endnu. Når du vælger eller tilføjer en ER-etiket, kan du tilføje relateret tekst for alle sprog, der understøttes i den aktuelle Finance-forekomst.

I følgende illustration vises, hvordan denne oversættelse foretages i en redigerbar datamodel. I dette eksempel oversættes **Beskrivelse**-attributten i feltet **PurchaseOrder** for den redigerbare **Fakturamodel** til sprogene østrigsk tysk (DE-AT) og japanske (JA).

![Levering af oversættelse af en ER-etiket i ER-datamodeldesigneren.](./media/er-multilingual-labels-refer.png)

Kun etikettekst til etiketter, der er placeret i en redigerbar ER-komponent, kan oversættes. Hvis du f.eks. vælger **Oversæt** for etiketattributten til en ER-modeltilknytnings datakilde, og du derefter vælger en ER-etiket, der findes i den overordnede ER-datamodel, kan du se etikettens indhold, men du kan ikke ændre den. I disse tilfælde er feltet **Oversat tekst** ikke tilgængeligt, som det er vist i følgende illustration.

![Gennemgang af leveret oversættelse af en ER-etiket i ER-modeltilknytningsdesigneren.](./media/er-multilingual-labels-refer-mapping.png)

> [!NOTE]
> Du kan ikke bruge designere til at slette en etiket, der er angivet i en redigerbar ER-komponent.

## <a name="scope"></a>Interval

ER-etiketter kan henvises til i flere oversættelsesattributter for ER-komponenter.

### <a name="data-model-component"></a>Datamodelkomponent

Når du konfigurerer en ER-datamodel, kan du tilføje ER-etiketter i den. Attributterne **Etiket** og **Beskrivelse** for modelelementet, alle modelfelterne og alle <a id="LinkModelEnum"></a>modeloptællingsværdier kan sammenkædes med en ER-etiket, der føjes til ER-datamodellen.

![Levering af oversættelse til beskrivelsesattributten i ER-datamodeldesigneren.](./media/er-multilingual-labels-refer.png)

Når en ER-datamodel er konfigureret på denne måde, vises dens indhold for brugere af ER-datamodeldesigneren på hver enkelt brugers foretrukne sprog. Derfor er modelvedligeholdelse forenklet. I følgende illustrationer vises, hvordan denne funktion fungerer for brugere, der har DE-AT og JA indstillet som det foretrukne sprog.

![Layout af ER-datamodeldesigneren for en bruger med angivelse af DE-AT som det foretrukne sprog.](./media/er-multilingual-labels-refer-de.png)

![Layout af ER-datamodeldesigneren for en bruger med angivelse af JA som det foretrukne sprog.](./media/er-multilingual-labels-refer-ja.png)

### <a name="model-mapping-component"></a>Komponent til modeltilknytning

Da ER-modeltilknytningen er baseret på en ER-datamodel, vises etiketterne for de datamodelelementer, der refereres til, på brugerens foretrukne sprog i modeltilknytningsdesigneren. I følgende illustration vises, hvordan betydningen af feltet **PurchaseOrder** er forklaret i den redigerbare modeltilknytning ved hjælp af etiketten for **Beskrivelse**-attributten, der er føjet til den konfigurerede datamodel. Bemærk, at denne etiket vises på brugerens foretrukne sprog (DE-AT i dette eksempel).

![Layout af ER-modeltilknytningsdesigneren for en bruger med angivelse af DE-AT som det foretrukne sprog.](./media/er-multilingual-labels-show-mapping.png)

Når **Etiket**-attributten for datakilden **Brugerinputparameter** er konfigureret som kædet sammen med en ER-etiket, vises det parameterfelt, der svarer til denne datakilde, i brugerdialogboksen ved kørslen for brugerne på deres foretrukne sprog.

### <a name="format-component"></a>Formatkomponent

Når du konfigurerer et ER-format, kan du tilføje ER-etiketter i det. **Etiket**- og **Hjælpetekst**-attributterne for alle konfigurerede datakilder kan sammenkædes med en ER-etiket, der føjes til ER-formatet. **Etiket**- og **Beskrivelse**-attributterne for alle <a id="LinkFormatEnum"></a>formatoptællingsværdier kan også sammenkædes med en ER-etiket, der er tilgængelig fra det redigerbare ER-format.

> [!NOTE]
> Du kan også sammenkæde disse attributter med en ER-etiket på den overordnede ER-datamodel, der genbruger modellens etiketter i hvert ER-format, der er konfigureret til denne ER-datamodel.

Når et ER-format er konfigureret på denne måde, vises dets indhold for brugere af ER-operationsdesigneren på hver enkelt brugers foretrukne sprog. Derfor er det nemmere at vedligeholde og analysere formatet til den konfigurerede logik.

Da et ER-format er baseret på en ER-datamodel, vises de etiketter, som refererer til datamodelelementerne,på brugerens foretrukne sprog i ER-formatdesigneren.

Når **Etiket**-attributten for datakilden **Brugerinputparameter** er kædet sammen med en ER-etiket, vises parameterfeltet i brugerdialogboksen ved kørslen for brugeren som en prompt. I følgende illustrationer vises, hvordan du kan kæde **Etiket**-attributten for datakilden **Brugerinputparameter** til en ER-etiket, så brugerne bliver bedt om at angive parameteren på forskellige brugerforetrukne sprog (vises for amerikansk engelsk (EN-US) og DE-AT) på kørselstidspunktet.

![Levering af oversættelse af attributter for en brugerinputparameter i ER-operationsdesigneren.](./media/er-multilingual-labels-refer-format.png)

![ER-behandling af kreditorbetalinger ved kørsel for EN-US som det brugerforetrukne sprog.](./media/er-multilingual-labels-show-runtime-en.png)

![ER-behandling af kreditorbetalinger ved kørsel for DE-AT som det brugerforetrukne sprog.](./media/er-multilingual-labels-show-runtime-de.png)

### <a name="expressions"></a>Udtryk

Hvis du vil bruge en etiket i et ER-[udtryk](er-formula-language.md), skal du bruge syntaksen **@"GER\_LABEL:X"**, hvor præfikset **@** angiver, at operanden refererer til en etiket, **GER\_LABEL** angiver, at det er en ER-etiket, og **X** er ER-etiket-id'et.

![Konfiguration af et ER-udtryk, der indeholder en reference til en ER-etiket i ER-formeldesigneren.](./media/er-multilingual-labels-expression1.png)

Hvis du vil referere til en systemetiket (program), skal du bruge syntaksen **@"X"**, hvor præfikset **@** angiver, at operanden refererer til en etiket, og **X** er systemetiket-id.

![Konfiguration af et ER-udtryk, der indeholder en reference til en programetiket i ER-formeldesigneren.](./media/er-multilingual-labels-expression2.png)

#### <a name="model-mapping"></a>Modeltilknytning

Et udtryk for en ER-modeltilknytning kan konfigureres ved hjælp af en etiket. Når denne tilknytning kaldes af et ER-format, der køres for at generere et udgående dokument, omfatter konteksten for udførelsen en sprogkode. En konfigureret udtryksetiket vil blive udfyldt med den etikettekst, der er konfigureret for sproget i den pågældende kontekst.

Hvis en refereret etiket ikke har nogen oversættelse til sproget i konteksten af formatudførelsen, der kalder modeltilknytningen, bruges etiketteksten på sproget EN-US i stedet.

#### <a name="format"></a>Formater

Et ER-udtryk for et ER-format kan konfigureres ved hjælp af etiketter. Når dette format køres for at generere et udgående dokument, omfatter konteksten for udførelsen en sprogkode. En konfigureret udtryksetiket vil blive udfyldt med den etikettekst, der er konfigureret for sproget i den pågældende kontekst.

![Levering af oversættelse af en ER-etiket til det redigerbare ER-udtryk i ER-formeldesigneren.](./media/er-multilingual-labels-refer-in-expression.png)

![Eksempel på databinding, der refererer til en ER-etiket i ER-operationsdesigneren.](./media/er-multilingual-labels-refer-in-binding.png)

Du kan konfigurere **FILE**-komponenten i et ER-format for at generere rapporten på brugerens foretrukne sprog.

![Konfigurer FILE-komponenten i ER-operationsdesigneren til at generere rapporten på brugerens foretrukne sprog.](./media/er-multilingual-labels-language-context-user.png)

Hvis du konfigurerer et ER-format på denne måde, oprettes rapporten ved hjælp af den tilsvarende tekst i ER-etiketter. I følgende illustrationer vises eksempler på rapporter på brugersprogene EN-US og DE-AT.

![Forhåndsvisning af den rapport, der er oprettet på EN-US som det brugerforetrukne sprog.](./media/er-multilingual-labels-report-preview-en.png)

![Forhåndsvisning af den rapport, der er oprettet på DE-AT som det brugerforetrukne sprog.](./media/er-multilingual-labels-report-preview-de.png)

Hvis en refereret etiket ikke har nogen oversættelse til sproget i konteksten af formatudførelsen, bruges etiketteksten på sproget EN-US i stedet.

> [!TIP]
> Du kan bruge **MAPPE** og de specifikke typer af **FIL**-komponenter i det ER-format, der kan redigeres, til at angive, hvordan en udgående fil genereres. Hvis du vil navngive en genereret fil, skal du konfigurere [ER-udtrykket](er-formula-language.md) for parameteren **Filnavn** for komponenten. Du kan bruge etiketter i det konfigurerede udtryk. Da parameteren **Filnavn** er sprogagnostisk som standard, vises teksten på alle de etiketter, du refererer til i dette udtryk vises på standardsproget EN-US under kørslen. Men i version 10.0.28 og senere kan du aktivere funktionen **Anvend parameteren "Sprogpræference" på udtrykket "Filnavn"**. I **Filnavn**-udtrykket tages der derefter højde for parameteren **Sprogindstillinger**, når den beregnes.

## <a name="language"></a>Sprog

ER understøtter forskellige måder at angive et sprog til en genereret rapport på. I feltet **Sprogindstillinger** under fanen **Format** kan du vælge følgende værdier:

- **Firmapræference** – Generér en rapport på et firmaspecifikt sprog.

    ![Angiv i ER-operationsdesigneren et firmas foretrukne sprog som sproget i en genereret rapport.](./media/er-multilingual-labels-language-context-company.png)

- **Brugerindstilling** – Generér en rapport på brugerens foretrukne sprog.
- **Udtrykkeligt defineret** – Generér en rapport på et sprog, der er angivet på designtidspunktet.

    ![Angiv i ER-operationsdesigneren et sprog, der er angivet på designtidspunktet, som sproget i en genereret rapport.](./media/er-multilingual-labels-language-context-fixed.png)

- **Defineret på kørselstidspunktet** – Generér en rapport på et sprog, der er angivet på kørselstidspunktet. Hvis du vælger denne værdi, skal du i feltet **Sprog** konfigurere et ER-udtryk, der returnerer sprogkoden for sproget, f.eks. sproget for den tilsvarende kunde.

    ![Angiv i ER-operationsdesigneren et sprog, der er angivet på kørselstidspunktet, som sproget i en genereret rapport.](./media/er-multilingual-labels-language-context-runtime.png)

## <a name="culture-specific-formatting"></a>Kulturspecifik formatering

ER understøtter forskellige metoder til at angive kulturen for en genereret rapport. Derfor kan den korrekte kulturspecifikke formatering bruges til dato, klokkeslæt og numeriske værdier. Når du designer et ER-format, kan du i feltet **Kulturindstillinger** under fanen **Format** vælge en af følgende værdier for alle formatkomponenter af typen **Almindelig\\Fil**, **Excel\\Fil**, **PDF\\Fil** eller **PDF\\Fletning**:

- **Brugerindstilling** – Formatér værdierne i overensstemmelse med brugerens foretrukne kultur. Denne kultur defineres i feltet **Dato, klokkeslæt og nummerformat** under fanen **Indstillinger** på siden **Brugerindstillinger**.

    ![I ER Operations-designeren defineres brugerens foretrukne kultur som en kultur for en genereret rapport.](./media/er-multilingual-labels-culture-context-user-preferred.png)

- **Eksplicit defineret** – Formatér værdierne i overensstemmelse med den kultur, der er angivet på designtidspunktet.

    ![I ER Operations-designeren defineres den kultur, som er angivet på designtidspunktet, som en kultur for en genereret rapport.](./media/er-multilingual-labels-culture-context-fixed.png)

- **Defineret på kørselstidspunkt** – Formatér værdierne i overensstemmelse med den kultur, der er angivet på kørselstidspunktet. Hvis du vælger denne værdi i feltet **Dato, klokkeslæt og nummerformat** under fanen **Tilknytning**, skal du konfigurere et ER-udtryk, der returnerer kulturkoden for kulturen, f.eks. den tilsvarende kundes kultur.

    ![I ER Operations-designeren defineres den kultur, som er defineret på kørselstidspunktet, som en kultur for en genereret rapport.](./media/er-multilingual-labels-culture-context-runtime.png)

> [!NOTE]
> En ER-komponent, som du definerer en bestemt kultur for, kan indeholde underordnede ER-komponenter, der er konfigureret til at udfylde en tekstværdi. Som standard bruges kulturen for den overordnede komponent til at formatere værdierne for disse komponenter. Du kan bruge følgende indbyggede ER-funktioner til at konfigurere bindinger for disse komponenter og anvende en alternativ kultur til værdiformatering:
>
> - [DATEFORMAT](er-functions-datetime-dateformat.md#syntax-2)
> - [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md#syntax-2)
> - [NUMBERFORMAT](er-functions-text-numberformat.md#syntax-2)
>
> I version 10.0.20 og senere bruges landestandarden for formatkomponenter af typen **Almindelig\\Fil** og **Excel\\Fil** til at formatere værdier under [PDF-konvertering](electronic-reporting-destinations.md#OutputConversionToPDF) af et genereret dokument.

## <a name="translation"></a>Oversættelse

Du kan føje de påkrævede ER-etiketter til en redigerbar ER-komponent. Når der tilføjes en ER-etiket, kan den oversættes på to måder: manuelt og automatisk.

### <a name="manual-translation"></a>Manuel oversættelse

Når du tilføjer en ER-etiket i **Tekstoversættelse**-[ruden](#TextTranslationPane), kan du manuelt oversætte den til alle sprog, der understøttes i den aktuelle Finance-forekomst. Du kan vælge det foretrukne sprog i feltet **Sprog** i sektionen **Systemsprog** eller **Brugersprog**, angive den relevante tekst i det tilsvarende **Oversat tekst**-felt og derefter vælge **Oversæt**. Denne proces skal gentages for alle nødvendige sprog og alle de etiketter, du tilføjer.

### <a name="automatic-translation"></a>Automatisk oversættelse

Konfiguration af en ER-komponent sker i kladdeversionen af ER-konfigurationen, som den redigerbare ER-komponent er placeret i.

![ER-konfigurationssiden giver adgang til konfigurationsversionen i kladdestatus.](./media/er-multilingual-labels-configurations.png)

Som beskrevet tidligere i denne artikel kan du føje de påkrævede ER-etiketter til en redigerbar ER-komponent. På denne måde kan du angive teksten i ER-etiketterne på sproget EN-US. Du kan derefter eksportere etiketterne for ER-komponenten ved hjælp af den indbyggede ER-funktion. Vælg kladdeversionen af en ER-konfiguration, der indeholder den redigerbare ER-komponent, og vælg derefter **Exchange \> Eksportér etiketter**.

![ER-konfigurationsside, der tillader eksport af ER-etiketter fra den valgte konfigurationsversion.](./media/er-multilingual-labels-export.png)

Du kan enten eksportere alle etiketter eller etiketter til et enkelt sprog, du angiver i begyndelsen af eksporten. Etiketter eksporteres som en zip-fil, der indeholder XML-filer. Hver XML-fil indeholder etiketter til et enkelt sprog.

![Eksempel på den eksporterede fil, der indeholder ER-etiketter til sproget DE-AT.](./media/er-multilingual-labels-in-xml.png)

Dette format bruges til automatisk oversættelse af etiketter med eksterne oversættelsestjenester, f. eks. [Dynamics 365 Translation service](../lifecycle-services/translation-service-overview.md). Når du modtager de oversatte etiketter, kan du importere dem tilbage til kladdeversionen af en ER-konfiguration, der indeholder de ER-komponenter, der ejer disse etiketter. Vælg kladdeversionen af en ER-konfiguration, der indeholder den redigerbare ER-komponent, og vælg **Exchange \> Indlæs etiketter**.

![ER-konfigurationsside, der tillader import af ER-etiketter til den valgte konfigurationsversion.](./media/er-multilingual-labels-load.png)

Oversatte etiketter importeres til den valgte ER-konfiguration. Oversatte etiketter, der findes i denne ER-konfiguration, erstattes. Hvis der mangler en oversat etiket i ER-konfigurationen, tilføjes den.

## <a name="lifecycle"></a>Livscyklus

Etiketter på en ER-komponent, der kan redigeres, bevares sammen med andet indhold til komponenten i den rette version af en ER-konfiguration.

Der kan henvises til etiketter for en basiskomponent i en afledt version af den ER-komponent, du opretter for at introducere dine ændringer.

> [!TIP]
> Når du designer en ER-løsning, kan du udlede din egen ER-[datamodel](er-overview-components.md#data-model-component)-komponent fra den leverede. I denne afledte datamodel kan du introducere dine egne ER-etiketter og bruge dem i alle ER-formater, der skal bruge datamodellen som datakilde. Derefter kan du aflede din egen ER-[formatkomponent](er-overview-components.md#format-component) fra den komponent, der leveres, ved at vælge den afledte ER-datamodel i stedet for den angivne. I version 10.0.28 og senere kan du aktivere funktionen **Udvidet adgang til navne til den stigende ER-datamodel** for at få adgang til navne til en stigende ER-datamodel i afledte ER-formatkomponenter, selv når du har valgt en ER-datamodel for den afledte ER-komponent, der er forskellig fra den, der blev brugt i ER-basiskomponenten.
>
> Når det samme labelnavn bruges i den afledte komponent og dens stigende komponenter, bruges oversættelsen af den pågældende label som den mest relevante.

ER-versionsstyring kontrollerer etikettildeling til enhver attribut i en ER-komponent. Ændringer i etikettildelingen registreres på listen over ændringer (delta) af en redigerbar ER-komponent, der er oprettet som en afledt version af den leverede ER-komponent. Disse ændringer valideres, når en afledt version baseres igen på en ny basisversion.

## <a name="functions"></a>Funktioner

Den indbyggede ER-funktion [LISTOFFIELDS](er-functions-list-listoffields.md) kan få adgang til ER-etiketter, der er konfigureret for nogle elementer af ER-komponenter.

Som beskrevet tidligere i denne artikel, kan attributterne **Etiket** og **Beskrivelse** for enhver [model](#LinkModelEnum) eller et [format](#LinkFormatEnum) være optællingsværdier, så de er knyttet til en ER-etiket, der er tilgængelig i den relevante ER-komponent. Du kan konfigurere et ER-udtryk, hvor du kalder funktionen **LISTOFFIELDS** ved hjælp af ER-optællingen som et argument. Dette udtryk returnerer en liste, der indeholder en post for hver værdi af en ER-optælling, der er defineret som et argument for denne funktion. Hver post indeholder værdien af en ER-etiket, der er knyttet til en ER-optællingsværdi:

- Værdien af en ER-etiket, der er sammenkædet med **Etiket**-attributter, gemmes i **Etiket**-feltet for den returnerede post.
- Værdien af en ER-etiket, der er sammenkædet med **Beskrivelse**-attributter, gemmes i **Beskrivelse**-feltet for den returnerede post.

## <a name="performance"></a><a name=performance></a>Ydeevne

Når du konfigurerer en ER-formatkomponent til at generere en rapport på dit foretrukne [sprog](#language) eller til at importere et indgående dokument, hvor indholdet fortolkes af dit foretrukne sprog, anbefales det, at du aktiverer funktionen **Cache det foretrukne sprog for den aktuelle bruger til ER-kørsler** i arbejdsområdet til [funktionsstyring](../../fin-ops/get-started/feature-management/feature-management-overview.md). Denne funktion er med til at forbedre ydeevnen, især for ER-formatkomponenter, der indeholder flere referencer til labels i ER-formler og -bindinger og mange [valideringsregler](general-electronic-reporting-formula-designer.md#TestFormula), så der genereres brugermeddelelser på dit foretrukne sprog.

Når du ændrer status for en ER-konfigurationsversion fra **Kladde** til **Fuldført**, gemmes disse labels i programdatabasen, hvis konfigurationsversionen indeholder ER-labels. Lagringsskemaet afhænger af tilstanden for funktionen **Accelerér ER-labels lager**:

- Hvis funktionen ikke er aktiveret, gemmes alle labels i feltet **LABELXML** i tabellen **ERSOLUTIONVERSIONTABLE** som et enkelt XML-kodestykke.
- Hvis funktionen er aktiveret, oprettes der en separat post for hvert sprog i tabellen **ERSOLUTIONVERSIONLABELSTABLE**. I feltet **CONTENTS** i denne tabel gemmes labels pr. sprog som et komprimeret XML-kodestykke.

Det anbefales, at du aktiverer funktionen **Accelerér ER-labels lager** i arbejdsområdet **Funktionsstyring**. Denne funktion er med til at forbedre udnyttelsen af båndbredde på netværket og den overordnede systemydeevne, da ER-labels på et enkelt sprog i de fleste tilfælde bruges, når du arbejder med en enkelt ER-konfiguration.

Hvis du vil anvende det valgte lagerskema til at beholde labels for alle ER-konfigurationer i den aktuelle forekomst af Finans, skal du følge nedenstående trin.

1. Gå til **Organisationsadministration** > **Periodisk** > **Anvend det valgte labellagerskema til alle ER-konfigurationer**.
2. Vælg **OK**.


## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering](general-electronic-reporting.md)
- [Elektroniske rapporteringsfunktioner](er-formula-language.md#Functions)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
