---
title: Formeldesigner i elektronisk rapportering (ER)
description: Denne artikel indeholder oplysninger om brugen af formeldesigneren i elektronisk rapportering (ER).
author: kfend
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 283c882300ece460c18ffebe572238e7629f8dee
ms.sourcegitcommit: a1d14836b40cfc556f045c6a0d2b4cc71064a6af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/14/2022
ms.locfileid: "9476795"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>Formeldesigner i elektronisk rapportering (ER)

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du bruger formeldesigneren i elektronisk rapportering (ER). Når du designer et format til et bestemt elektronisk dokument i ER, kan du bruge formler til at transformere data, så de opfylder kravene til dokumentets udførelse og formatering. Disse formler ligner formler i Microsoft Excel. Forskellige typer funktioner understøttes i formlerne: tekst, dato og klokkeslæt, matematisk logik, oplysninger samt funktioner til konvertering af datatypen og også andre forretningsdomænespecifikke funktioner.

## <a name="formula-designer-overview"></a>Oversigt over formeldesigner

Elektronisk rapportering (ER) understøtter formeldesigneren. Derfor kan du på designtidspunktet konfigurere udtryk, der kan bruges til følgende opgaver under kørsel:

- Konverter data, der modtages fra en programdatabase, og som skal angives i en ER-datamodel, der er designet til at være datakilde for ER-formater. (F.eks. kan disse transformeringer kan omfatte filtrering, gruppering og datatypekonvertering).
- Formatere de data, der skal sendes til et genereret elektroniske dokument i overensstemmelse med det layout og betingelserne for et bestemt ER-format. (Formatering kan f.eks. udføres i overensstemmelse med det ønskede sprog eller kultur eller kodning).
- Styre processen til oprettelse af elektroniske dokumenter. (F.eks. kan udtrykkene aktivere eller deaktivere outputtet af bestemte elementer i formatet, afhængigt af behandlingen af data. De kan også afbryde processen med oprettelse af dokumentet eller udløse meddelelser til brugere).

Du kan åbne siden **Formeldesigner**, når du udfører en af følgende handlinger:

- Binder datakildeelementer til datamodelkomponenter.
- Binder datakildeelementer til formatkomponenter.
- Vedligeholder beregnede felter som en del af datakilder.
- Definerer synligheds- og redigeringsbetingelser for brugerinputparametre.
- Definerer standardværdier for brugerinputparametre.
- Designer formatets transformeringer.
- Definerer aktivering af betingelserne for formatets komponenter.
- Definerer filnavne til formatets FILE-komponenter.
- Definerer betingelserne for proceskontrolvalideringer.
- Definerer meddelelsestekst for proceskontrolvalideringer.

## <a name="data-binding"></a><a name="Binding"></a>Databinding

ER-formeldesigneren kan bruges til at definere et udtryk, der transformerer data, der er modtaget fra datakilder, så data kan angives i dataforbrugeren på følgende måde på kørselstidspunktet:

- Fra programdatakilder og kørselsparametre til en ER-datamodel
- Fra en ER-datamodel til et ER-format
- Fra programdatakilder og kørselsparametre til et ER-format

I følgende illustration vises et udtryk af denne type design. I dette eksempel afrunder udtrykket værdien af feltet **Intrastat.AmountMST** i Intrastat-tabellen til to decimaler og returnerer den afrundede værdi.

[![Udtrykket databinding.](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

I følgende illustration vises, hvordan et udtryk af denne type kan bruges. I dette eksempel er resultatet af det designede udtryk angivet i **Transaction.InvoicedAmount**-komponenten af **momsrapporteringsmodellen**.

[![Udtrykket databinding anvendes.](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

På kørselstidspunktet afrunder den designede formel `ROUND (Intrastat.AmountMST, 2)` værdien af feltet **AmountMST** for hver post i Intrastattabellen til to decimaler. Den indsætter derefter den afrundede værdi i komponenten **Transaction.InvoicedAmount** i datamodellen **Momsrapportering**.

## <a name="data-formatting"></a><a name="Transformation"></a>Dataformatering

ER-formeldesigneren kan bruges til at definere et udtryk, der formaterer data, der er modtaget fra datakilder, så data kan sendes som en del af det genererende elektroniske dokument. Du har muligvis formatering, der skal anvendes som en typisk regel, der skal genbruges til et format. I så fald kan du introducere denne formatering én gang i formatkonfigurationen, som en navngivet transformering, der har et formateringsudtryk. Denne navngivne transformation kan sammenkædes med mange formatkomponenter, hvor outputtet skal været formateret i henhold til det formateringsudtryk, du oprettede.

I følgende illustration vises designet af en transformation af denne type. Dette eksempel på **TrimmedString**-transformation afkorter indgående data i af datatypen *Streng* ved at fjerne foranstillede og efterstillede mellemrum. Derefter returneres den afkortede strengværdi.

[![Transformation.](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

I følgende illustration vises, hvordan en transformation af denne type kan bruges. I dette eksempel sender flere komponenter tekst som output til det generere elektroniske dokument på kørselstidspunktet. Alle disse formatkomponenter refererer til transformationen **TrimmedString** efter navn.

[![Transformation, der bruges.](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Når formatkomponenter refererer til **TrimmedString-**-transformation (for eksempel **partyName**-komponenten i den foregående illustration), sendes tekst som output for at generere det elektroniske dokument. Denne tekst indeholder ikke foranstillede eller efterstillede mellemrum.

Hvis du har en formatering, der skal anvendes individuelt, kan den indføres som et individuelt udtryk for binding af en bestemt formatkomponent. I følgende illustration vises et udtryk af denne type. I dette eksempel er **partyType**-formatkomponenten bundet til datakilden via et udtryk, der konverterer indgående data fra feltet **Model.Company.RegistrationType** i datakilden til stor bogstavtekst. Udtrykket sender derefter teksten som output til det elektroniske dokument.

[![Anvende formatering på en enkelt komponent.](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

## <a name="process-flow-control"></a><a name="Validation"></a>Kontrol af procesforløb

ER-formeldesigneren kan bruges til at definere udtryk, der styrer procesforløbet under generering af elektroniske dokumenter. Du kan udføre følgende opgaver:

- Definer betingelser, der bestemmer, hvornår en proces til oprettelse af dokumentet skal stoppes.
- Angiv udtryk, der opretter enten meddelelser til slutbrugeren om stoppede processer eller udløser en kørselslogbesked om, at processen fortsætter med oprettelse af rapporter.
- Angiv filnavne til oprettelse af elektroniske dokumenter, og kontrollér betingelserne for deres oprettelse.

Hver regel i kontrol af procesforløb udformet som en enkelt validering. I følgende illustration vises en validering af denne type. Her er en forklaring af konfigurationen i dette eksempel:

- Valideringen evalueres, når **INSTAT**-noden oprettes under generering af XML-filen.
- Hvis listen over transaktioner er tom, stopper valideringen kørselsprocessen og returnerer **FALSE**.
- Valideringen returnerer en fejlmeddelelse, der indeholder teksten til etiketten for SYS70894 på brugerens foretrukne sprog.

[![Validering.](./media/picture-validation.jpg)](./media/picture-validation.jpg)

ER-formeldesigneren bruges også til at generere et filnavn til et genererende elektronisk dokument og til at styre processen til oprettelse af en fil. I følgende illustration vises designet af en kontrol af procesforløb af denne type. Her er en forklaring af konfigurationen i dette eksempel:

- Listen over poster fra datakilden **model. Intrastat-** er opdelt i batches. Hver batch indeholder op til 1000 poster.
- Output opretter en zip-fil, der indeholder en fil i XML-format for hver batch, der blev oprettet.
- Et udtryk returnerer et filnavn til generering af elektroniske dokumenter ved at sammenkæde filnavnet og filtypenavnet. For den anden batch og alle efterfølgende batches indeholder filnavnet batch-ID som et suffiks.
- Et udtryk aktiverer (returnerer **TRUE**) processen med en filoprettelse for de eneste batches, der indeholder mindst én post.

[![Kontrol af procesforløb.](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

## <a name="document-content-control"></a><a name="Enabled"></a>Kontrol af dokumentindhold

ER-formeldesigneren kan bruges til at konfigurere udtryk, der styrer, hvilke data der indgår i genererede elektroniske dokumenter på kørselstidspunktet. Udtrykkene kan aktivere eller deaktivere outputtet af bestemte elementer i formatet, afhængigt af behandlingen af data og den konfigurerede logik. Disse udtryk kan angives for et enkelt formatelement i feltet **Aktiveret** under fanen **Tilknytning** på siden **Operationsdesigner**. Du kan angive udtrykkene som en logik betingelse, der returnerer en *Boolesk* værdi:

- Hvis betingelsen returnerer **Sand**, køres det aktuelle formatelement.
- Hvis betingelsen returnerer **Falsk**, springes det aktuelle formatelement over.

I følgende illustration vises udtryk af denne type. (Version 11.12.11 af formatkonfigurationen **ISO20022-kreditoverførsel (nr.)**, der leveres af Microsoft, bruges som eksempel.) Formatkomponenten **XMLheader** er konfigureret til at beskrive strukturen i kreditoverførselsmeddelelsen i henhold til ISO20022 XML-meddelelsesstandarderne. Formatkomponenten **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** er konfigureret til at føje **Ustrd**-XML-elementet til den genererede meddelelse, og til at placere remitteringsoplysningerne i et ustruktureret format som tekst i følgende XML-elementer:

- **PaymentNotes**-komponenten bruges til at generere tekst på betalingsnoter.
- **DelimitedSequence**-komponenten genererer kommaseparerede fakturanumre, der bruges til at afstemme den aktuelle kreditoverførsel.

[![Komponenterne PaymentNotes and DelimitedSequence.](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> Komponenterne **PaymentNotes** og **DelimitedSequence** er markeret med et spørgsmålstegn. Et spørgsmålstegn angiver, at brugen af en komponent er betinget. I dette tilfælde er brugen af komponenterne baseret på følgende kriterier:
>
> - Udtrykket `@.PaymentsNotes <> ""` er defineret for komponeneten **PaymentNote** og gør det muligt at udfylde XML-elementet (ved at returnere **SANDT**) **Ustrd** med teksten for betalingsnoter, hvis teksten til den aktuelle kreditoverførsel ikke er tom.
>
>    [![Udtryk for komponenten PaymentNotes.](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)
>
> - Udtrykket `@.PaymentsNotes = ""`, som er defineret for komponenten **DelimitedSequence**, gør det muligt at udfylde XML-elementet (ved at returnere **SANDT**) **Ustrd** med en kommasepareret liste med fakturanumre, der bruges til at afstemme den aktuelle kreditoverførsel, såfremt teksten på betalingsnoter til denne kreditoverførsel er tom.
>
>    [![Udtryk for komponenten DelimitedSequence.](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)
> 
> Baseret på denne indstilling vil den genererede meddelelse for hver debitorbetaling, XML-elementet **Ustrd**, indeholde enten tekst med betalingsnoter eller, når denne tekst er tom, kommasepareret liste med fakturanumre, som bruges til at afstemme denne betaling.

## <a name="assistance-in-formulas-writing"></a>Hjælp til formelskrivning

### <a name="data-sources-navigator"></a>Navigator i datakilder

Du kan redigere en formel, der repræsenterer et element i en struktureret datakilde. Da du konfigurerede ER-parametrene til at vise stien til et element i en struktureret datakilde som den [relative sti](relative-path-data-bindings-er-models-format.md), kan tegnet "ved" (@) [vises](er-formula-language.md#relative-path) i formlen i stedet for den resterende del af den absolutte sti i den hierarkiske træstruktur, der bruges. Denne resterende del af den absolutte sti peges på et overordnet element for det, der kan redigeres. I Finans-version **10.0.30 og senere** kan du i ruden **Datakilder** på **formeldesigner** vælge indstillingen **Gå til @** for at placere markøren for datakildetræet på et element, der er overordnet for det redigerbare. Strukturen af alle skjulte stigende elementer udvides automatisk og udvides igen, når det er nødvendigt. Denne udvidelse kan hjælpe dig med hurtigt at visualisere basiselementet for det redigerbare, overholde det redigerbare element i datakildetræet og bruge hver af dem i den redigerbare formel, hvis det er nødvendigt.

![Brug indstillingen "Gå til @" for at placere markøren fra datakildetræet til et element, der er overordnet for det element, der kan redigeres, på formeldesignersiden.](./media/er_formula-designer-data-sources-navigator.gif)

### <a name="data-sources-picker"></a>Vælger af datakilder

På siden **Formeldesigner** i ruden **Datakilder** til venstre skal du vælge et element i en datakilde, som du vil føre ind i den formel, der kan redigeres. Vælg derefter **Tilføj datakilde**. Bemærk, at det valgte element er føjet til teksten i den redigerbare formel.

> [!TIP]
> Når du bruger indstillingen **Tilføj datakilde** i standardformeleditoren, føjes det valgte element altid til slutningen af formelteksten. Når du gør det samme i [redigeringsprogrammet Avanceret formel](er-advanced-formula-editor.md), indsættes det valgte element i formelteksten på den aktuelle markørposition.

### <a name="built-in-functions-picker"></a>Indbygget funktionsvælger

På siden **Formeldesigner** i ruden **Funktioner** til højre skal du vælge en ER-indbygget funktion, som du vil føre ind i den formel, der kan redigeres. Vælg derefter **Tilføj funktion**. Bemærk, at den valgte funktion er føjet til teksten i den redigerbare formel.

> [!TIP]
> Når du bruger indstillingen **Tilføj funktion** i standardformeleditoren, føjes den valgte funktion altid til slutningen af formelteksten. Når du gør det samme i [redigeringsprogrammet Avanceret formel](er-advanced-formula-editor.md), indsættes den valgte funktion i formelteksten på den aktuelle markørposition.

### <a name="validation-of-configured-formulas"></a><a name="TestFormula"></a>Validering af konfigurerede formler

På siden **Formeldesigner** skal du vælge **Test** for at validere, hvordan den konfigurerede formel fungerer.

[![Valg af test til validering af en formel.](./media/ER-FormulaTest-Start.png)](./media/ER-FormulaTest-Start.png)

Når værdierne for formelargumenter er påkrævede, kan du åbne dialogboksen **Testudtryk** fra siden **Formeldesigner**. I de fleste tilfælde skal disse argumenter defineres manuelt, fordi de konfigurerede bindinger ikke køres på designtidspunktet. Fanen **Testresultat** på siden **Formeldesigner** viser resultatet fra kørslen af den konfigurerede formel.

Følgende eksempel viser, hvordan du kan teste den formel, der er konfigureret for domænet for udenrigshandel, for at sikre, at Intrastat-varekoden kun indeholder cifre.

Når du tester denne formel, kan du bruge dialogboksen **Testudtryk** til at angive værdien af Intrastat-varekoden til test.

[![Angiv Intrastat-varekoden til test.](./media/ER-FormulaTest-Start-EnterArguments.png)](./media/ER-FormulaTest-Start-EnterArguments.png)

Når du har angivet Intrastat-varekoden og valgt **OK**, viser fanen **Testresultater** på siden **Formeldesigner** resultatet af kørslen af den konfigurerede formel. Du kan derefter vurdere, om resultatet er acceptabelt. Hvis resultatet ikke er acceptabelt, kan du opdatere formlen og teste den igen.

[![Testresultat.](./media/ER-FormulaTest-Result.png)](./media/ER-FormulaTest-Result.png)

Nogle formler kan ikke testes på designtidspunktet. For eksempel kan en formel returnere et resultat af en datatype, der ikke kan vises under fanen **Testresultater**. I dette tilfælde får du vist en fejlmeddelelse, der anfører, at formlen ikke kan testes.

[![Fejlmeddelelse.](./media/ER-FormulaTest-Error.png)](./media/ER-FormulaTest-Error.png)

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering](general-electronic-reporting.md)
- [Formelsprog i elektronisk rapportering](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
