---
title: Designe flersprogede rapporter i elektronisk rapportering
description: I dette emne forklares det, hvordan du kan bruge elektroniske rapporteringsetiketter (ER) til at designe og generere flersprogede rapporter.
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7934f36877247460ec843201a08d4670456889f9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679696"
---
# <a name="design-multilingual-reports-in-electronic-reporting"></a>Designe flersprogede rapporter i elektronisk rapportering

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Overblik

Som forretningsbruger kan du benytte strukturen for [Elektronisk rapportering (ER)](general-electronic-reporting.md) til at konfigurere formater for udgående dokumenter, der skal genereres i overensstemmelse med de lovgivningsmæssige krav i forskellige lande/områder. Når disse krav kræver, at udgående dokumenter skal genereres på forskellige sprog til forskellige lande/områder, kan du konfigurere et enkelt ER-[format](general-electronic-reporting.md#FormatComponentOutbound), der indeholder sprogafhængige ressourcer. På denne måde kan du genbruge formatet for at generere udgående dokumenter for forskellige lande/områder. Du kan også bruge et enkelt ER-format til at generere et udgående dokument på forskellige sprog for de tilsvarende kunder, leverandører, datterselskaber eller andre parter.

Du kan konfigurere ER-datamodeller og -modeltilknytninger som datakilder for konfigurerede ER-formater for at definere dataflowet, der angiver, hvilke programdata der skal placeres i genererede dokumenter. Som [udbyder](general-electronic-reporting.md#Provider) af ER-konfigurationer kan du [publicere](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs) konfigurerede [datamodeller](general-electronic-reporting.md#data-model-and-model-mapping-components), [modeltilknytninger](general-electronic-reporting.md#data-model-and-model-mapping-components) og [formater](general-electronic-reporting.md#FormatComponentOutbound) som komponenter i en ER-løsning for at generere specifikke udgående dokumenter. Du kan også give kunder tilladelse til at [uploade](general-electronic-reporting-manage-configuration-lifecycle.md) den publicerede ER-løsning, så den kan bruges og tilpasses. Hvis du forventer, at kunder måske taler andre sprog, kan du konfigurere ER-komponenterne, så de indeholder sprogafhængige ressourcer. På denne måde kan indholdet af en redigerbar ER-komponent vises på en kundes foretrukne sprog på designtidspunktet.

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

Når du designer en ER-datamodel, en ER-modeltilknytning eller et ER-format, vises indstillingen **Oversæt**, når du vælger et felt, der måske indeholder den kontekst, der kan oversættes. Når du vælger denne indstilling, kan du sammenkæde det valgte felt med en ER-etiket i **Tekstoversættelse**-<a name="TextTranslationPane">ruden</a>. Du kan vælge en eksisterende ER-etiket, eller du kan tilføje en ny ER-etiket, hvis den ikke er tilgængelig endnu. Når du vælger eller tilføjer en ER-etiket, kan du tilføje relateret tekst for alle sprog, der understøttes i den aktuelle Finance-forekomst.

I følgende illustration vises, hvordan denne oversættelse foretages i en redigerbar datamodel. I dette eksempel oversættes **Beskrivelse**-attributten i feltet **PurchaseOrder** for den redigerbare **Fakturamodel** til sprogene østrigsk tysk (DE-AT) og japanske (JA).

![Levering af oversættelse af en ER-etiket i ER-datamodeldesigneren](./media/er-multilingual-labels-refer.png)

Kun etikettekst til etiketter, der er placeret i en redigerbar ER-komponent, kan oversættes. Hvis du f.eks. vælger **Oversæt** for etiketattributten til en ER-modeltilknytnings datakilde, og du derefter vælger en ER-etiket, der findes i den overordnede ER-datamodel, kan du se etikettens indhold, men du kan ikke ændre den. I disse tilfælde er feltet **Oversat tekst** ikke tilgængeligt, som det er vist i følgende illustration.

![Gennemgang af leveret oversættelse af en ER-etiket i ER-modeltilknytningsdesigneren](./media/er-multilingual-labels-refer-mapping.png)

> [!NOTE]
> Du kan ikke bruge designere til at slette en etiket, der er angivet i en redigerbar ER-komponent.

## <a name="scope"></a>Interval

ER-etiketter kan henvises til i flere oversættelsesattributter for ER-komponenter.

### <a name="data-model-component"></a>Datamodelkomponent

Når du konfigurerer en ER-datamodel, kan du tilføje ER-etiketter i den. Attributterne **Etiket** og **Beskrivelse** for modelelementet, alle modelfelterne og alle <a id="LinkModelEnum"></a>modeloptællingsværdier kan sammenkædes med en ER-etiket, der føjes til ER-datamodellen.

![Levering af oversættelse til beskrivelsesattributten i ER-datamodeldesigneren.](./media/er-multilingual-labels-refer.png)

Når en ER-datamodel er konfigureret på denne måde, vises dens indhold for brugere af ER-datamodeldesigneren på hver enkelt brugers foretrukne sprog. Derfor er modelvedligeholdelse forenklet. I følgende illustrationer vises, hvordan denne funktion fungerer for brugere, der har DE-AT og JA indstillet som det foretrukne sprog.

![Layout af ER-datamodeldesigneren for en bruger med angivelse af DE-AT som det foretrukne sprog](./media/er-multilingual-labels-refer-de.png)

![Layout af ER-datamodeldesigneren for en bruger med angivelse af JA som det foretrukne sprog](./media/er-multilingual-labels-refer-ja.png)

### <a name="model-mapping-component"></a>Komponent til modeltilknytning

Da ER-modeltilknytningen er baseret på en ER-datamodel, vises etiketterne for de datamodelelementer, der refereres til, på brugerens foretrukne sprog i modeltilknytningsdesigneren. I følgende illustration vises, hvordan betydningen af feltet **PurchaseOrder** er forklaret i den redigerbare modeltilknytning ved hjælp af etiketten for **Beskrivelse**-attributten, der er føjet til den konfigurerede datamodel. Bemærk, at denne etiket vises på brugerens foretrukne sprog (DE-AT i dette eksempel).

![Layout af ER-modeltilknytningsdesigneren for en bruger med angivelse af DE-AT som det foretrukne sprog](./media/er-multilingual-labels-show-mapping.png)

Når **Etiket**-attributten for datakilden **Brugerinputparameter** er konfigureret som kædet sammen med en ER-etiket, vises det parameterfelt, der svarer til denne datakilde, i brugerdialogboksen ved kørslen for brugerne på deres foretrukne sprog.

### <a name="format-component"></a>Formatkomponent

Når du konfigurerer et ER-format, kan du tilføje ER-etiketter i det. **Etiket**- og **Hjælpetekst**-attributterne for alle konfigurerede datakilder kan sammenkædes med en ER-etiket, der føjes til ER-formatet. **Etiket**- og **Beskrivelse**-attributterne for alle <a id="LinkFormatEnum"></a>formatoptællingsværdier kan også sammenkædes med en ER-etiket, der er tilgængelig fra det redigerbare ER-format.

> [!NOTE]
> Du kan også sammenkæde disse attributter med en ER-etiket på den overordnede ER-datamodel, der genbruger modellens etiketter i hvert ER-format, der er konfigureret til denne ER-datamodel.

Når et ER-format er konfigureret på denne måde, vises dets indhold for brugere af ER-operationsdesigneren på hver enkelt brugers foretrukne sprog. Derfor er det nemmere at vedligeholde og analysere formatet til den konfigurerede logik.

Da et ER-format er baseret på en ER-datamodel, vises de etiketter, som refererer til datamodelelementerne,på brugerens foretrukne sprog i ER-formatdesigneren.

Når **Etiket**-attributten for datakilden **Brugerinputparameter** er kædet sammen med en ER-etiket, vises parameterfeltet i brugerdialogboksen ved kørslen for brugeren som en prompt. I følgende illustrationer vises, hvordan du kan kæde **Etiket**-attributten for datakilden **Brugerinputparameter** til en ER-etiket, så brugerne bliver bedt om at angive parameteren på forskellige brugerforetrukne sprog (vises for amerikansk engelsk (EN-US) og DE-AT) på kørselstidspunktet.

![Levering af oversættelse af attributter for en brugerinputparameter i ER-operationsdesigneren](./media/er-multilingual-labels-refer-format.png)

![ER-behandling af kreditorbetalinger ved kørsel for EN-US som det brugerforetrukne sprog](./media/er-multilingual-labels-show-runtime-en.png)

![ER-behandling af kreditorbetalinger ved kørsel for DE-AT som det brugerforetrukne sprog](./media/er-multilingual-labels-show-runtime-de.png)

### <a name="expressions"></a>Udtryk

Hvis du vil bruge en etiket i et ER-[udtryk](er-formula-language.md), skal du bruge syntaksen **@"GER\_LABEL:X"**, hvor præfikset **@** angiver, at operanden refererer til en etiket, **GER\_LABEL** angiver, at det er en ER-etiket, og **X** er ER-etiket-id'et.

![Konfiguration af et ER-udtryk, der indeholder en reference til en ER-etiket i ER-formeldesigneren](./media/er-multilingual-labels-expression1.png)

Hvis du vil referere til en systemetiket (program), skal du bruge syntaksen **@"X"**, hvor præfikset **@** angiver, at operanden refererer til en etiket, og **X** er systemetiket-id.

![Konfiguration af et ER-udtryk, der indeholder en reference til en programetiket i ER-formeldesigneren](./media/er-multilingual-labels-expression2.png)

#### <a name="model-mapping"></a>Modeltilknytning

Et udtryk for en ER-modeltilknytning kan konfigureres ved hjælp af en etiket. Når denne tilknytning kaldes af et ER-format, der køres for at generere et udgående dokument, omfatter konteksten for udførelsen en sprogkode. En konfigureret udtryksetiket vil blive udfyldt med den etikettekst, der er konfigureret for sproget i den pågældende kontekst.

Hvis en refereret etiket ikke har nogen oversættelse til sproget i konteksten af formatudførelsen, der kalder modeltilknytningen, bruges etiketteksten på sproget EN-US i stedet.

#### <a name="format"></a>Formater

Et ER-udtryk for et ER-format kan konfigureres ved hjælp af etiketter. Når dette format køres for at generere et udgående dokument, omfatter konteksten for udførelsen en sprogkode. En konfigureret udtryksetiket vil blive udfyldt med den etikettekst, der er konfigureret for sproget i den pågældende kontekst.

![Levering af oversættelse af en ER-etiket til det redigerbare ER-udtryk i ER-formeldesigneren](./media/er-multilingual-labels-refer-in-expression.png)

![Eksempel på databinding, der refererer til en ER-etiket i ER-operationsdesigneren](./media/er-multilingual-labels-refer-in-binding.png)

Du kan konfigurere **FILE**-komponenten i et ER-format for at generere rapporten på brugerens foretrukne sprog.

![Konfigurer FILE-komponenten i ER-operationsdesigneren til at generere rapporten på brugerens foretrukne sprog](./media/er-multilingual-labels-language-context-user.png)

Hvis du konfigurerer et ER-format på denne måde, oprettes rapporten ved hjælp af den tilsvarende tekst i ER-etiketter. I følgende illustrationer vises eksempler på rapporter på brugersprogene EN-US og DE-AT.

![Forhåndsvisning af den rapport, der er oprettet på EN-US som det brugerforetrukne sprog](./media/er-multilingual-labels-report-preview-en.png)

![Forhåndsvisning af den rapport, der er oprettet på DE-AT som det brugerforetrukne sprog](./media/er-multilingual-labels-report-preview-de.png)

Hvis en refereret etiket ikke har nogen oversættelse til sproget i konteksten af formatudførelsen, bruges etiketteksten på sproget EN-US i stedet.

## <a name="language"></a>Sprog

ER understøtter forskellige måder at angive et sprog til en genereret rapport på. I feltet **Sprogindstillinger** under fanen **Format** kan du vælge følgende værdier:

- **Firmapræference** – Generér en rapport på et firmaspecifikt sprog.

    ![Angiv i ER-operationsdesigneren et firmas foretrukne sprog som sproget i en genereret rapport](./media/er-multilingual-labels-language-context-company.png)

- **Brugerindstilling** – Generér en rapport på brugerens foretrukne sprog.
- **Udtrykkeligt defineret** – Generér en rapport på et sprog, der er angivet på designtidspunktet.

    ![Angiv i ER-operationsdesigneren et sprog, der er angivet på designtidspunktet, som sproget i en genereret rapport](./media/er-multilingual-labels-language-context-fixed.png)

- **Defineret på kørselstidspunktet** – Generér en rapport på et sprog, der er angivet på kørselstidspunktet. Hvis du vælger denne værdi, skal du i feltet **Sprog** konfigurere et ER-udtryk, der returnerer sprogkoden for sproget, f.eks. sproget for den tilsvarende kunde.

    ![Angiv i ER-operationsdesigneren et sprog, der er angivet på kørselstidspunktet, som sproget i en genereret rapport](./media/er-multilingual-labels-language-context-runtime.png)

## <a name="translation"></a>Oversættelse

Du kan føje de påkrævede ER-etiketter til en redigerbar ER-komponent. Når der tilføjes en ER-etiket, kan den oversættes på to måder: manuelt og automatisk.

### <a name="manual-translation"></a>Manuel oversættelse

Når du tilføjer en ER-etiket i **Tekstoversættelse**-[ruden](#TextTranslationPane), kan du manuelt oversætte den til alle sprog, der understøttes i den aktuelle Finance-forekomst. Du kan vælge det foretrukne sprog i feltet **Sprog** i sektionen **Systemsprog** eller **Brugersprog**, angive den relevante tekst i det tilsvarende **Oversat tekst**-felt og derefter vælge **Oversæt**. Denne proces skal gentages for alle nødvendige sprog og alle de etiketter, du tilføjer.

### <a name="automatic-translation"></a>Automatisk oversættelse

Konfiguration af en ER-komponent sker i kladdeversionen af ER-konfigurationen, som den redigerbare ER-komponent er placeret i.

![ER-konfigurationssiden giver adgang til konfigurationsversionen i kladdestatus](./media/er-multilingual-labels-configurations.png)

Som beskrevet tidligere i dette emne kan du føje de påkrævede ER-etiketter til en redigerbar ER-komponent. På denne måde kan du angive teksten i ER-etiketterne på sproget EN-US. Du kan derefter eksportere etiketterne for ER-komponenten ved hjælp af den indbyggede ER-funktion. Vælg kladdeversionen af en ER-konfiguration, der indeholder den redigerbare ER-komponent, og vælg derefter **Exchange \> Eksportér etiketter**.

![ER-konfigurationsside, der tillader eksport af ER-etiketter fra den valgte konfigurationsversion](./media/er-multilingual-labels-export.png)

Du kan enten eksportere alle etiketter eller etiketter til et enkelt sprog, du angiver i begyndelsen af eksporten. Etiketter eksporteres som en zip-fil, der indeholder XML-filer. Hver XML-fil indeholder etiketter til et enkelt sprog.

![Eksempel på den eksporterede fil, der indeholder ER-etiketter til sproget DE-AT](./media/er-multilingual-labels-in-xml.png)

Dette format bruges til automatisk oversættelse af etiketter med eksterne oversættelsestjenester, f. eks. [Dynamics 365 Translation service](../lifecycle-services/translation-service-overview.md). Når du modtager de oversatte etiketter, kan du importere dem tilbage til kladdeversionen af en ER-konfiguration, der indeholder de ER-komponenter, der ejer disse etiketter. Vælg kladdeversionen af en ER-konfiguration, der indeholder den redigerbare ER-komponent, og vælg **Exchange \> Indlæs etiketter**.

![ER-konfigurationsside, der tillader import af ER-etiketter til den valgte konfigurationsversion](./media/er-multilingual-labels-load.png)

Oversatte etiketter importeres til den valgte ER-konfiguration. Oversatte etiketter, der findes i denne ER-konfiguration, erstattes. Hvis der mangler en oversat etiket i ER-konfigurationen, tilføjes den.

## <a name="lifecycle"></a>Livscyklus

Etiketter på en ER-komponent, der kan redigeres, bevares sammen med andet indhold til komponenten i den rette version af en ER-konfiguration.

Der kan henvises til etiketter for en basiskomponent i en afledt version af den ER-komponent, du opretter for at introducere dine ændringer.

ER-versionsstyring kontrollerer etikettildeling til enhver attribut i en ER-komponent. Ændringer i etikettildelingen registreres på listen over ændringer (delta) af en redigerbar ER-komponent, der er oprettet som en afledt version af den leverede ER-komponent. Disse ændringer valideres, når en afledt version baseres igen på en ny basisversion.

## <a name="functions"></a>Funktioner

Den indbyggede ER-funktion [LISTOFFIELDS](er-functions-list-listoffields.md) kan få adgang til ER-etiketter, der er konfigureret for nogle elementer af ER-komponenter.

Som beskrevet tidligere i dette emne, kan attributterne **Etiket** og **Beskrivelse** for enhver [model](#LinkModelEnum) eller et [format](#LinkFormatEnum) være optællingsværdier, så de er knyttet til en ER-etiket, der er tilgængelig i den relevante ER-komponent. Du kan konfigurere et ER-udtryk, hvor du kalder funktionen **LISTOFFIELDS** ved hjælp af ER-optællingen som et argument. Dette udtryk returnerer en liste, der indeholder en post for hver værdi af en ER-optælling, der er defineret som et argument for denne funktion. Hver post indeholder værdien af en ER-etiket, der er knyttet til en ER-optællingsværdi:

- Værdien af en ER-etiket, der er sammenkædet med **Etiket**-attributter, gemmes i **Etiket**-feltet for den returnerede post.
- Værdien af en ER-etiket, der er sammenkædet med **Beskrivelse**-attributter, gemmes i **Beskrivelse**-feltet for den returnerede post.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering](general-electronic-reporting.md)
- [Elektroniske rapporteringsfunktioner](er-formula-language.md#functions)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]