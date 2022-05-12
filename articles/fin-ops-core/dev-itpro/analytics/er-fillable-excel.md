---
title: Designe en konfiguration til at generere dokumenter i Excel-format
description: Dette emne giver beskriver, hvordan du kan designe et ER-format (elektronisk rapportering) til at udfylde en Excel-skabelon og derefter generere udgående Excel-formatdokumenter.
author: NickSelin
ms.date: 03/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec25065f2e3cc3b5dd3c9004d5330447f7b2ac61
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645129"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Designe en konfiguration til generering af dokumenter i Excel-format

[!include[banner](../includes/banner.md)]

Du kan designe en formatkonfiguration af [Elektronisk rapportering (ER)](general-electronic-reporting.md), der har en ER-formatkomponent, som du kan konfigurere til at generere et udgående dokument i et Microsoft Excel-projektmappeformat. Specifikke ER-formatkomponenter skal bruges til dette formål.

Hvis du vil vide mere om denne funktion, skal du følge trinnene i emnet, [Designe en konfiguration til generering af rapporter i OPENXML-format](tasks/er-design-reports-openxml-2016-11.md).

## <a name="add-a-new-er-format"></a>Tilføj et nyt ER-format

Når du tilføjer en ny ER-formatkonfiguration for at generere et udgående dokument i et Excel-projektmappeformat, skal du enten vælge **Excel**-værdien for attributten **Formattype** for formatet eller lade attributten **Formattype** være tom.

- Hvis du vælger **Excel**, kan du konfigurere formatet til kun at oprette et udgående dokument i Excel-format.
- Hvis du lader attributten være tom, kan du konfigurere formatet til at generere et udgående dokument i et hvilket som helst format, der understøttes af ER-strukturen.

Hvis du vil konfigurere ER-formatkomponenten af konfigurationen, skal du vælge **Designer** i handlingsruden og åbne ER-formatkomponenten for redigering i ER-operationsdesigner.

![Siden Konfigurationer.](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Excel-filkomponent

### <a name="manual-entry"></a>Manuel indtastning

Du skal føje en **Excel \\Fil**-komponent til det konfigurerede ER-format, hvis du vil generere et udgående dokument i Excel-format.

![Excel-filkomponent.](./media/er-excel-format-add-file-component.png)

Hvis du vil angive layoutet for det udgående dokument, skal du vedhæfte en Excel-projektmappe med filtypenavnet .xlsx til **Excel-\\fil**-komponenten som skabelon til udgående dokumenter.

> [!NOTE]
> Når du manuelt tilknytter en skabelon, skal du bruge en [dokumenttype](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types), der er konfigureret til dette formål i [ER-parametrene](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

![Føje en tilknytning til Excel\Fil-komponenten.](./media/er-excel-format-add-file-component2.png)

Hvis du vil angive, hvordan den tilknyttede skabelon skal udfyldes, når du kører det konfigurerede ER-format, skal du føje indlejrede komponenter **Ark**, **Område** og **Celle** til komponenten **Excel\\Fil**. Alle indlejrede komponenter skal knyttes til et navngivet element i Excel.

### <a name="template-import"></a>Skabelonimport

Du kan vælge **Importér fra Excel** under fanen **Importer** i handlingsruden for at importere en ny skabelon til et tomt ER-format. I dette eksempel oprettes der automatisk en **Excel\\Fil**-komponent, og den importerede skabelon knyttes til den. Alle nødvendige ER-komponenter oprettes automatisk, baseret på listen over de Excel-navngivne elementer, der registreres.

![Vælge Importér fra Excel.](./media/er-excel-format-import-template.png)

> [!NOTE]
> Hvis du vil oprette det valgfrie **Ark**-element i det redigerbare ER-format, skal du angive indstillingen **Opret Excel-arkformatelement** til **Ja**.

## <a name="sheet-component"></a>Arkkomponent

**A**-komponenten angiver et regneark i den tilknyttede Excel-projektmappe, der skal udfyldes. Navnet på regnearket i en Excel-skabelon er defineret i egenskaben **Ark** for denne komponent.

> [!NOTE]
> Denne komponent er valgfri for Excel-projektmapper, der indeholder et enkelt regneark.

Under fanen **Tilknytning** i ER-operationsdesigneren kan du konfigurere egenskaben **Aktiveret** for en **Ark**-komponent for at angive, om komponenten skal placeres i et genereret dokument:

- Hvis et udtryk af egenskaben **Aktiveret** er konfigureret til at returnere **Sand** på kørselstidspunktet, eller, hvis der slet ikke er konfigureret et udtryk, vil det relevante regneark blive taget med i det genererede dokument.
- Hvis et udtryk af egenskaben **Aktiveret** er konfigureret til at returnere **Falsk** på kørselstidspunktet, indeholder det genererede dokument ikke et regneark.

![Eksempel på en arkkomponent.](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Områdekomponent

### <a name="nested-components"></a>Indlejrede komponenter

#### <a name="data-typing"></a>Dataindtastning

Komponenten **Område** kan have andre indlejrede ER-komponenter, der bruges til at angive værdier i de relevante områder.

- Hvis en komponent i gruppen **Tekst** bruges til at angive værdier, indtastes værdien i et Excel-område som en tekstværdi.

    > [!NOTE]
    > Du kan bruge dette mønster til at formatere angivne værdier på basis af den landestandard, der er defineret i programmet.

- Hvis komponenten **Celle** i gruppen **Excel** bruges til at angive værdier, indtastes værdien i et Excel-område som en værdi af den datatype, der er defineret af bindingen for den pågældende **Celle**-komponent. Datatypen kan f.eks. være **Streng**, **Reelt tal** eller **Heltal**.

    > [!NOTE]
    > Brug dette mønster til at gøre Excel-programmet i stand til at formatere angivne værdier på basis af landestandarden på den lokale computer, der åbner det udgående dokument.

#### <a name="row-handling"></a>Rækkehåndtering

Komponenten **Område** kan konfigureres som lodret replikeret, så der genereres flere rækker i et Excel-regneark. Rækkerne kan genereres af den overordnede **Område**-komponent eller af de indlejrede **Område**-komponenter.

I version 10.0.26 og senere kan du tvinge et genereret regneark til at beholde de genererede rækker på samme side. I ER-formatdesigneren skal du indstille indstillingen **Hold rækker sammen** til **Ja** for den overordnede **Område**-komponent i det redigerbare ER-format. ER forsøger derefter at beholde alt det indhold, der genereres af det pågældende område, på samme side. Hvis højden på indholdet overstiger den resterende plads på den aktuelle side, tilføjes et sideskift, og indholdet vil starte øverst på den næste nye side.

> [!NOTE]
> Det anbefales, at du kun konfigurerer indstillingen **Hold rækker sammen** for områder, der dækker hele bredden på et genereret dokument.
>
> Indstillingen **Hold rækker sammen** gælder kun for komponenter i **Excel \> Filer**, der er konfigureret til at bruge en Excel-projektmappeskabelon.
>
> Indstillingen **Hold rækker sammen** fungerer kun, når funktionen **Aktivér brug af EPPlus-bibliotek i Elektronisk rapporteringsstruktur** er aktiveret.
>
> Denne funktion kan bruges til **Område**-komponenter, der findes under **Side**-komponenten. Men der er ingen garanti for, at [sidefodstotaler](er-paginate-excel-reports.md#add-data-sources-to-calculate-page-footer-totals) beregnes korrekt ved hjælp af datakilder til [indsamling af data](er-data-collection-data-sources.md).

Du kan få mere at vide om, hvordan du bruger denne indstilling, ved at følge eksemplet i [Designe et ER-format for at holde rækker sammen på samme Excel-side](er-keep-excel-rows-together.md).

### <a name="replication"></a>Replikering

Egenskaben **Replikeringsretning** angiver, om og hvordan et område skal gentages i et genereret dokument:

- **Ingen replikering** – Det relevante Excel-område vil ikke blive gentaget i det genererede dokument.
- **Lodret** – Det relevante Excel-område vil blive gentaget lodret i det genererede dokument. Hvert replikerede område placeres under det oprindelige område i en Excel-skabelon. Antallet af gentagelser defineres af antallet af poster i en datakilde for den **Postlistetype**, der er bundet til denne ER-komponent.
- **Vandret** – Det relevante Excel-område vil blive gentaget vandret i det genererede dokument. Hvert replikerede område placeres til højre for det oprindelige område i en Excel-skabelon. Antallet af gentagelser defineres af antallet af poster i en datakilde for den **Postlistetype**, der er bundet til denne ER-komponent.

    Hvis du vil vide mere om vandret replikering, skal du følge trinnene i [Brug vandrette, udvidelige områder til dynamisk at tilføje kolonner i Excel-rapporter](tasks/er-horizontal-1.md).

### <a name="enabling"></a>Aktivering

Under fanen **Tilknytning** i ER-operationsdesigneren kan du konfigurere egenskaben **Aktiveret** for en **Område**-komponent for at angive, om komponenten skal placeres i et genereret dokument:

- Hvis et udtryk af egenskaben **Aktiveret** er konfigureret til at returnere **Sand** på kørselstidspunktet, eller, hvis der slet ikke er konfigureret et område, vil det relevante område blive udfyldt i det genererede dokument.
- Hvis et udtryk af egenskaben **Aktiveret** er konfigureret til at returnere **Falsk** på kørselstidspunktet, og hvis dette område ikke repræsenterer rækker eller kolonner i deres helhed, vil det relevante område ikke blive udfyldt i det genererede dokument.
- Hvis et udtryk af egenskaben **Aktiveret** er konfigureret til at returnere **Falsk** på kørselstidspunktet, og hvis dette område repræsenterer rækker eller kolonner i deres helhed, vil det generede dokument indeholde disse rækker og kolonner som skjulte rækker og kolonner.

### <a name="resizing"></a>Tilpasning af størrelse

Du kan konfigurere Excel-skabelonen til at bruge celler til at vise tekstdata. For at sikre, at hele teksten i en celle er synlig i et genereret dokument, kan du konfigurere den pågældende celle, så teksten automatisk ombrydes i den. Du kan også konfigurere den række, der indeholder den pågældende celle, til automatisk at justere dens højde, hvis den tekst, der ombrydes, ikke er helt synlig. Der er flere oplysninger i afsnittet "Ombryde tekst i en celle" i [Rette data, der afskæres i celler](https://support.microsoft.com/office/fix-data-that-is-cut-off-in-cells-e996e213-6514-49d8-b82a-2721cef6144e).

> [!NOTE]
> På grund af en kendt [Excel-begrænsning](https://support.microsoft.com/topic/you-cannot-use-the-autofit-feature-for-rows-or-columns-that-contain-merged-cells-in-excel-34b54dd7-9bfc-6c8f-5ee3-2715d7db4353), selvom du konfigurerer celler til at ombryde tekst, og du konfigurerer de rækker, der indeholder disse celler, til automatisk at justere deres højde, så de passer til den tekst, der ombrydes, kan du muligvis ikke bruge Excel-funktionerne **Autotilpas** og **Ombryd tekst** til flettede celler og rækker, der indeholder dem. 

Fra og med Dynamics 365 Finance-version 10.0.23 kan du, når du arbejder i et genereret dokument, tvinge ER til i et genereret dokument at beregne højden på hver række, der blev konfigureret, så den automatisk passer til indholdet af indlejrede celler, når den pågældende række indeholder mindst én flettet celle, der er konfigureret til at ombryde teksten i den. Den beregnede højde bruges derefter til at ændre størrelsen på rækken for at sikre, at alle celler i rækken er synlige i det genererede dokument.

> [!NOTE]
> Vær opmærksom på, at denne funktionalitet muligvis ikke fungerer som forventet, når en brugerdefineret skrifttype bruges til at formatere en flettet celle. Da Excel ikke integrerer brugerdefinerede skrifttyper, indeholder programmet ikke oplysninger om brugerdefineret skriftstørrelse. Størrelsen på den flettede celle kan derfor forkalkuleret forkert.

Benyt følgende fremgangsmåde, hvis du vil begynde at bruge denne funktion, når du kører ER-formater, der er konfigureret til at bruge Excel-skabeloner, til at generere udgående dokumenter.

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Parametre til elektronisk rapportering** i sektionen **Relaterede links**.
3. På siden **Parametre til elektronisk rapportering** under fanen **Kørsel** skal du vælge **Ja** i indstillingen **Tilpas rækkehøjde automatisk**.

Når du vil ændre denne regel for et enkelt ER-format, skal du opdatere kladdeversionen af det pågældende format ved at følge disse trin.

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge **Rapporteringskonfigurationer** i sektionen **Konfigurationer**.
3. På siden **Konfigurationer** i konfigurationstræet i venstre rude skal du vælge en ER-konfiguration, der er beregnet til at bruge en Excel-skabelon til at generere udgående dokumenter.
4. I oversigtspanelet **Versioner** skal du vælge den konfigurationsversion, der har statussen **Kladde**.
5. Vælg **Designer** i handlingsruden.
6. Vælg den Excel-komponent, der er knyttet til en Excel-skabelon, i formattræet i venstre rude på siden **Formatdesigner**.
7. Vælg en værdi i feltet **Juster rækkehøjde** under fanen **Format** for at angive, om ER skal tvinges under kørslen til at ændre højden på rækker i et udgående dokument, der genereres af det redigerede ER-format:

    - **Standard** – Brug den generelle indstilling, der er konfigureret i feltet **Tilpas rækkehøjde automatisk** på siden **Parametre for elektronisk rapportering**.
    - **Ja** – Tilsidesæt den generelle indstilling, og ret rækkehøjden ved kørsel.
    - **Nej** – Tilsidesæt den generelle indstilling, og ret ikke rækkehøjden ved kørsel.

## <a name="cell-component"></a>Cellekomponent

Komponenten **Celle** bruges til at udfylde navngivne Excel-celler, -figurer og -billeder. Hvis du vil angive, at et navngivet Excel-objekt skal være udfyldt af **Celle** ER-komponent, skal du angive navnet på det pågældende objekt i egenskaben **Excel-område** for komponenten **Celle**.

Under fanen **Tilknytning** i ER-operationsdesigneren kan du konfigurere egenskaben **Aktiveret** for en **Celle**-komponent for at angive, om objektet skal udfyldes i et genereret dokument:

- Hvis et udtryk af egenskaben **Aktiveret** er konfigureret til at returnere **Sand** på kørselstidspunktet, eller, hvis der slet ikke er konfigureret et objekt, vil det relevante område blive udfyldt i det genererede dokument. Bindingen for denne **Celle**-komponent angiver en værdi, der placeres i det relevante objekt.
- Hvis et udtryk af egenskaben **Aktiveret** er konfigureret til at returnere **Falsk** på kørselstidspunktet, udfyldes det relevante objekt ikke i det genererede dokument.

Når en **Celle**-komponent er konfigureret til at angive en værdi i en celle, kan den bindes til en datakilde, der returnerer værdien af en primitiv datatype (f.eks. **Streng**, **Reelt tal** eller **Heltal**). I dette tilfælde indtastes værdien i cellen som en værdi af samme datatype.

Når en **Celle**-komponent er konfigureret til at angive en værdi i Excel-figur, kan den bindes til en datakilde, der returnerer en værdi af en primitiv datatype (f.eks. **Streng**, **Reelt tal** eller **Heltal**). I dette tilfælde indtastes værdien i Excel-figuren som tekst med dem pågældende figur. Når det gælder værdier af datatyper, der ikke er **strenge**, udføres konverteringen til tekst automatisk.

> [!NOTE]
> Du kan konfigurere en **Celle**-komponent, så den kun udfyldes på en figur i de tilfælde, hvor egenskaben figurtekst understøttes.

Når en **Celle**-komponent er konfigureret til at angive en værdi i et Excel-billede, kan den bindes til en datakilde, der returnerer en værdi af en datatype **Container**, der repræsenterer et billede i binært format. I dette tilfælde angives værdien i Excel-billedet som et billede.

> [!NOTE]
> Alle Excel-billeder og -figurer betragtes som forankret af dets øverste venstre hjørne til en bestemt Excel-celle eller et specifikt celleområde. Hvis du vil replikere et Excel-billede eller -figur, skal du konfigurere den celle eller det område, det eller den er forankret til, som en replikeret celle eller et celleområde.

Du kan få mere at vide om, hvordan du integrerer billeder og figurer, under [Integrere billeder og figurer i et dokumenter, du genererer ved hjælp af ER](electronic-reporting-embed-images-shapes.md).

## <a name="page-break-component"></a>Komponenten Sideskift

Komponenten **Sideskift** tvinger Excel til at starte en ny side. Denne komponent er ikke påkrævet, når du vil bruge Excels standardsideinddeling, men du bør bruge den, når du vil have, at Excel skal følge dit ER-format til opbygning af sideinddeling.

## <a name="page-component"></a><a name="page-component"></a>Sidekomponent

### <a name="overview"></a>Overblik

Du kan bruge komponenten **Side**, når Excel skal følge dit ER-format og strukturere sideinddeling i et genereret udgående dokument. Når et ER-format kører komponenter under **Side**-komponenten, tilføjes de påkrævede sideskift automatisk. Under denne proces tages der hensyn til størrelsen på det genererede indhold, sideopsætningen af Excel-skabelonen og den papirstørrelse, der er valgt i Excel-skabelonen.

Hvis du skal opdele et genereret dokument i forskellige sektioner, hvor hver af dem har forskellige sideinddelinger, kan du konfigurere flere **Side**-komponenter i hver [Ark](er-fillable-excel.md#sheet-component)-komponent.

### <a name="structure"></a><a name="page-component-structure"></a>Opbygning

Hvis den første komponent under **Side**-komponenten er en [Område](er-fillable-excel.md#range-component)-komponent, hvor egenskaben **Replikeringsretning** er angivet til **Ingen replikering**, betragtes dette område som sidehovedet til sideinddeling, der er baseret på indstillingerne for den aktuelle **Side**-komponent. Det Excel-område, der er tilknyttet denne formatkomponent, gentages øverst på alle sider, der genereres ved hjælp af indstillingerne for den aktuelle **Side**-komponent.

> [!NOTE]
> Hvis de [Rækker, der skal gentages i øverste](https://support.microsoft.com/office/repeat-specific-rows-or-columns-on-every-printed-page-0d6dac43-7ee7-4f34-8b08-ffcc8b022409) område, konfigureres i Excel-skabelonen, skal adressen for dette Excel-område være lig med adressen på det Excel-område, der er tilknyttet den tidligere beskrevne **Område**-komponent.

Hvis den sidste komponent under **Side**-komponenten er en **Område**-komponent, hvor egenskaben **Replikeringsretning** er angivet til **Ingen replikering**, betragtes dette område som sidefoden til sideinddeling, der er baseret på indstillingerne for den aktuelle **Side**-komponent. Det Excel-område, der er tilknyttet denne formatkomponent, gentages nederst på alle sider, der genereres ved hjælp af indstillingerne for den aktuelle **Side**-komponent.

> [!NOTE]
> For at få korrekt sideinddeling bør de Excel-områder, der er tilknyttet **Område**-komponenterne, ikke få ændret størrelse under kørslen. Vi fraråder, at du formaterer celler i dette område ved at bruge **Ombryd tekst i en celle** og **Tilpas automatisk rækkehøjde** som [indstillinger](https://support.microsoft.com/office/wrap-text-in-a-cell-2a18cff5-ccc1-4bce-95e4-f0d4f3ff4e84) i Excel.

Du kan tilføje flere andre **Område**-komponenter mellem de valgfrie **Område**-komponenter for at angive, hvordan et genereret dokument er udfyldt.

Hvis sættet af indlejrede **Område**-komponenter under **Side**-komponenten ikke overholder den tidligere beskrevne struktur, opstår der en [valideringsfejl](er-components-inspections.md#i17) på designtidspunktet i ER-formatdesigneren. Fejlmeddelelsen fortæller dig, at problemet kan forårsage problemer under kørslen.

> [!NOTE]
> Hvis du vil generere korrekt output, skal du ikke angive en binding for nogen **Område**-komponent under **Side**-komponenten, hvis egenskaben **Replikeringsretning** for den pågældende **Område**-komponent er angivet til **Ingen replikering**, og området er konfigureret til at generere sidehoveder eller sidefødder.

Hvis du vil bruge sideinddelingsrelateret summering og optælling til at beregne løbende totaler og totaler pr. side, anbefales det, at du konfigurerer de påkrævede datakilder for [indsamling af data](er-data-collection-data-sources.md). Du kan få mere at vide om, hvordan du bruger **Side**-komponenten til at sideopdele et genereret Excel-dokument, ved at gennemføre procedurerne i [Designe et ER-format for at sideopdele et genereret dokument i Excel-format](er-paginate-excel-reports.md).

### <a name="limitations"></a><a name="page-component-limitations"></a>Begrænsninger

Når du bruger **Side**-komponenten til Excel-sideinddeling, kender du ikke det endelige antal sider i et genereret dokument, før sideinddelingen er fuldført. Du kan derfor ikke beregne det samlede antal sider ved hjælp af ER-formler og udskrive det korrekte antal sider i et genereret dokument på en side før den sidste side.

> [!TIP]
> Du kan opnå dette resultat i Excel-sidehoved eller -sidefod ved hjælp af den særlige Excel-[formatering](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) af sidehoveder og sidefødder.

Konfigurerede **Side**-komponenter tages ikke i betragtning, når du opdaterer en Excel-skabelon i det format, der kan redigeres, i Dynamics 365 Finance-version 10.0.22. Denne funktionalitet tages i betragtning i yderligere versioner af Finance.

Hvis du konfigurerer Excel-skabelonen til at bruge [betinget formatering](/office/dev/add-ins/excel/excel-add-ins-conditional-formatting), vil det muligvis ikke fungere som forventet i nogle tilfælde.

### <a name="applicability"></a>Anvendelighed

**Side**-komponenten virker kun til [Excel-filens](er-fillable-excel.md#excel-file-component) formatkomponent, når den pågældende komponent er konfigureret til at bruge en skabelon i Excel. Hvis du [erstatter](tasks/er-design-configuration-word-2016-11.md) Excel-skabelonen med en Word-skabelon og derefter kører det redigerbare ER-format, ignoreres **Side**-komponenten.

**Side**-komponenten fungerer kun, når funktionen **Aktivér brug af EPPlus-bibliotek i Elektronisk rapporteringsstruktur** er aktiveret. En undtagelse opstår under kørslen, hvis ER prøver at behandle **Side**-komponenten, mens denne funktion er deaktiveret.

> [!NOTE]
> En undtagelse opstår under kørslen, hvis et ER-format behandler **Side**-komponenten til en Excel-skabelon, der indeholder mindst én formel, der henviser til en celle, som ikke er gyldig. Du kan hjælpe med at forhindre kørselsfejl ved at rette Excel-skabelonen som beskrevet i [Sådan retter du fejlen #REF!](https://support.microsoft.com/office/how-to-correct-a-ref-error-822c8e46-e610-4d02-bf29-ec4b8c5ff4be).

## <a name="footer-component"></a>Sidefodskomponent

Komponenten **Sidefod** bruges til at udfylde sidefødder nederst i et genereret regneark i en Excel-projektmappe.

> [!NOTE]
> Du kan tilføje denne komponent for hver **ark**-komponent for at angive forskellige sidefodsfødder til forskellige regneark i en genereret Excel-projektmappe.

Når du konfigurerer en individuel **sidefod**-komponent, kan du bruge egenskaben for udseende for **sidehoved/sidefod** til at angive de sider, som komponenten bruges til. Følgende værdier er tilgængelige:

- **Alle** – Kør den konfigurerede **sidefod**-komponent for enhver side i det overordnede Excel-regneark.
- **Først** – Kør den konfigurerede **sidefod**-komponent kun for den første side i det overordnede Excel-regneark.
- **Lige** – Kør den konfigurerede **sidefod**-komponent kun for hver lige side i det overordnede Excel-regneark.
- **Ulige** – Kør den konfigurerede **sidefod**-komponent kun for ulige side i det overordnede Excel-regneark.

I forbindelse med en komponent i et enkelt **ark** kan du tilføje flere komponenter i **sidefoden**, som hver især har en anden værdi for egenskaben for udseende for **sidehoved/sidefod**. På denne måde kan du generere forskellige sidefødder til forskellige typer sider i et Excel-regneark.

> [!NOTE]
> Sørg for, at hver **sidefod**-komponent, du tilføjer til et enkelt **ark**-komponent, har en anden værdi for egenskaben for udseende for **sidehoved/sidefod**. Ellers opstår en [valideringsfejl](er-components-inspections.md#i16). Den fejlmeddelelse, du modtager, giver dig besked om uoverensstemmelsen.

Under den tilføjede **sidefod**-komponent skal du tilføje de nødvendige indlejrede komponenter i **Tekst\\Streng**, **Tekst\\Dato og tid** eller en anden type. Konfigurer bindingerne for disse komponenter for at angive, hvordan sidefoden skal udfyldes.

Du kan også bruge særlige [formatteringskoder](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) til at formatere indholdet af en genereret sidefod korrekt. Du kan få mere at vide om, hvordan du bruger denne indfaldsvinkel ved at følge trinnene i [Eksempel 1](#example-1) senere i dette emne.

> [!NOTE]
> Når du konfigurerer ER-formater, skal du huske at bruge Excel [grænsen](https://support.microsoft.com/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3) og det maksimale antal tegn i et enkelt sidehoved eller en enkelt sidefod.

## <a name="header-component"></a>Sidehovedkomponent

Komponenten **Sidehoved** bruges til at udfylde sidehoveder øverst i et genereret regneark i en Excel-projektmappe. Det bruges på samme måde som **sidefod**-komponenten.

## <a name="edit-an-added-er-format"></a>Redigere et tilføjet ER-format

### <a name="update-a-template"></a>Opdatere en skabelon

Du kan vælge **Opdater fra Excel** under fanen **Importer** i handlingsruden for at importere en opdateret skabelon til et redigerbart ER-format. Under denne proces erstattes en skabelon for den valgte komponent **Excel\\Fil** med en ny skabelon. Indholdet af det redigerbare ER-format synkroniseres med indholdet af den opdaterede ER-skabelon.

- Der oprettes automatisk en ny ER-formatkomponent for alle Excel-navne, hvis ER-formatkomponenten ikke findes i det redigerbare format.
- Alle ER-formatkomponenter slettes fra det redigerbare ER-format, hvis det rette Excel-navn ikke findes.

> [!NOTE]
> Angiv indstillingen **Opret Excel-arkformatelement** til **Ja**, hvis du vil oprette det valgfri **Ark**-element i det redigerbare ER-format.
>
> Hvis det redigerbare ER-format oprindeligt indeholdte **Ark**-elementer, anbefales det, at du angiver indstillingen **Opret Excel-arkformatelement** til **Ja**, når du importerer en opdateret skabelon. Ellers oprettes alle indlejrede elementer i det oprindelige **Ark**-element fra bunden. Derfor går alle bindinger af de genoprettede formatelementer tabt i det opdaterede ER-format.

![Indstillingen Opret Excel-arkformatelement i dialogboksen Opdater fra Excel.](./media/er-excel-format-update-template.png)

Hvis du vil vide mere om denne funktion, skal du udføre trinnene i [Redigere elektronisk rapporteringsformat ved at genanvende Excel-skabeloner](modify-electronic-reporting-format-reapply-excel-template.md).

## <a name="validate-an-er-format"></a>Validere et ER-format

Når du validerer et ER-format, der kan redigeres, sker der en konsistenskontrol for at sikre, at Excel-navnet findes i den Excel-skabelon, der aktuelt bruges. Du får besked om eventuelle uoverensstemmelser. Ved visse inkonsistenser tilbydes muligheden for at rette problemer automatisk.

![Validering og fejlmeddelelse.](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>Styre beregningen af Excel-formler

Når et udgående dokument i Microsoft Excel-projektmappeformat genereres, kan visse celler i dette dokument indeholde Excel-formler. Når funktionen **Aktivér brug af EPPlus-bibliotek i den elektroniske rapporteringsstruktur** er aktiveret, kan du styre, hvornår formlerne beregnes, ved at ændre værdien i [parameteren](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) **Beregningsindstillinger** i den Excel-skabelon, der bruges:

- Vælg **Automatisk** for at genberegne alle afhængige formler, hver gang et genereret dokument føjes til nye områder, celler osv.

    > [!NOTE]
    > Dette kan forårsage et problem med ydeevnen for Excel-skabeloner, der indeholder flere relaterede formler.

- Vælg **Manuel** for at undgå genberegning af formler, når der genereres et dokument.

    > [!NOTE]
    > Genberegning af formler gennemtvinges manuelt, når et genereret dokument åbnes med henblik på visning i Excel.
    > Brug ikke denne indstilling, hvis du konfigurerer en ER-destination, der forudsætter brug af et genereret dokument uden visning i Excel (PDF-konvertering, afsendelse af mail osv.), da det genererede dokument muligvis ikke indeholder værdier i celler, der indeholder formler.

## <a name="example-1-format-footer-content"></a><a name="example-1"></a>Eksempel 1: Formater sidefodsindhold

1. Brug de angivne ER-konfigurationer til at [generere](er-generate-printable-fti-forms.md) et FTI-dokument (fritekstfaktura, der kan udskrives).
2. Gennemse sidefoden i det genererede dokument. Bemærk, at den indeholder oplysninger om det aktuelle sidenummer og det samlede antal sider i dokumentet.

    ![Gennemse sidefoden i et genereret dokument i Excel-format.](./media/er-fillable-excel-footer-1.gif)

3. I ER-formatdesigneren skal du [åbne](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format)-eksempelformatet ER til gennemsyn

    Sidefoden i arbejdsarket **Faktura** genereres på basis af indstillingerne for de to **streg**-komponenter, der findes under komponenten **Sidefod**:

    - Den første **streng**-komponent udfylder følgende særlige formateringskoder for at tvinge Excel til at anvende bestemt formatering:

        - **&C** – Juster sidefodsteksten i den midterste del.
        - **&"Segoe UI,Regular"&8** - Vis sidefodsteksten i "Segoe UI Regular"-skrifttypen på en størrelse på 8 point.

    - Den anden **streng**-komponent udfylder den tekst, der indeholder det aktuelle sidenummer, og det samlede antal sider i det aktuelle dokument.

    ![Gennemse ER-formatkomponenten på siden Formatdesigner for sidefod.](./media/er-fillable-excel-footer-2.png)

4. Tilpas eksempel-ER-formatet for at redigere den aktuelle sidefod:

    1. [Opret](er-quick-start2-customize-report.md#DeriveProvidedFormat) en udledt **fritekst-faktura (Excel) brugerdefineret** ER-format, der er baseret på eksempel-ER-formatet.
    2. Tilføj det første nye sæt **streng**-komponenter til **sidefod**-komponenten i arbejdsarket **Faktura**:

        1. Tilføj en **Streng**-komponent, der justerer firmanavnet til venstre og viser det med skrifttypen 8 "Segoe UI Regular" (**"&L&"Segoe UI,Regular"&8"**).
        2. Tilføj en **streng**-komponent, der udfylder firmanavnet (**model.InvoiceBase.CompanyInfo.Name**).

    3. Tilføj et andet nyt sæt **streng**-komponenter til **sidefod**-komponenten i arbejdsarket **Faktura**:

        1. Tilføj en **Streng**-komponent, der justerer behandlingen af data til højre og viser det med skrifttypen 8 "Segoe UI Regular" (**"&R&"Segoe UI,Regular"&8"**).
        2. Tilføj en **Streng**-komponent, der udfylder behandlingsdatoen i et brugerdefineret format (**"&nbsp;"&DATEFORMAT (SESSIONTODAY(), "yyy-MM-dd")**).

        ![Gennemse ER-formatkomponenten på siden Formatdesigner for sidefod.](./media/er-fillable-excel-footer-3.png)

    4. [Fuldfør](er-quick-start2-customize-report.md#CompleteDerivedFormat) kladdeversionen af det afledte **Fritekstfaktura (Excel) brugerdefineret** ER-format.

5. [Konfigurer](er-generate-printable-fti-forms.md#configure-print-management) udskriftsstyring til at bruge det afledte **Fritekstfaktura (Excel) brugerdefineret** ER-format i stedet for prøve ER-format.
6. Generer et FTI-dokument, der kan udskrives, og gennemse sidefoden i det oprettede dokument.

    ![Gennemse sidefoden i et genereret dokument i Excel-format.](./media/er-fillable-excel-footer-4.gif)

## <a name="example-2-fixing-the-merged-cells-epplus-issue"></a><a name="example-2"></a>Eksempel 2: Rettelse af EPPlus-problemet de sammenflettede celler

Du kan køre et ER-format for at generere et udgående dokument i et Excel-projektmappeformat. Når funktionen **Aktivér brug af EPPlus-bibliotek i elektronisk rapporteringsstruktur** er aktiveret i arbejdsområdet **Funktionsstyring**, bruges [EPPlus-biblioteket](https://www.nuget.org/packages/epplus/4.5.2.1) til at oprette Excel-output. Men på grund af den kendte [Excel-funktionalitet](https://answers.microsoft.com/msoffice/forum/all/deleting-a-range-of-cells-that-includes-merged/8601462c-4e2c-48e0-bd23-848eecb872a9) og begrænsningen for EPPlus-biblioteket kan du komme ud for følgende undtagelse: "Kan ikke slette/overskrive flettede celler. Et interval flettes delvist sammen med et andet flettet område." Du kan finde ud af, hvilken type Excel-skabeloner der kan forårsage denne undtagelse, og hvordan du kan løse problemet, ved at fuldføre følgende eksempel.

1. I Excel-skrivebordsprogrammet skal du oprette en ny Excel-projektmappe.
2. Tilføj navnet **ReportTitle** for celle **A2** i regnearket **Sheet1**.
3. Flet celle **A1** og **A2**.

    ![Gennemse resultaterne af fletning af celle A1 og A2 i den designede Excel-projektmappe i Excel-skrivebordsprogrammet.](./media/er-fillable-excel-example2-1.png)

3. På siden **Konfigurationer** skal du [tilføjet et nyt ER-format](er-fillable-excel.md#add-a-new-er-format) for at generere et udgående dokument i et Excel-projektmappeformat.
4. På siden **Formatdesigner** skal du [importere](er-fillable-excel.md#template-import) den designede Excel-projektmappe til det tilføjede ER-format som en ny skabelon til udgående dokumenter.
5. På siden **Tilknytning** skal du konfigurere bindingen for **ReportTitle**-komponenten af [Celle](er-fillable-excel.md#cell-component)-typen.
6. Kør det konfigurerede ER-format. Bemærk, at følgende undtagelse vises: "Kan ikke slette/overskrive sammenflettede celler. Et interval flettes delvist sammen med et andet flettet område."

    ![Gennemse resultaterne af at køre det konfigurerede ER-format på formatdesignersiden.](./media/er-fillable-excel-example2-2.png)

Du kan rette fejlen på en af følgende måder:

- **Nemmere, men anbefales ikke**: I arbejdsområdet **Funktionsstyring** skal du deaktivere funktionen **Aktivér brug af EPPlus-bibliotek i Elektronisk rapporteringsstruktur**. Selvom denne metode er nemmere, kan du komme ud for andre problemer, hvis du bruger den, da nogle ER-funktioner kun understøttes, når funktionen **Aktivér brug af EPPlus-bibliotek i Elektronisk rapporteringsstruktur** er aktiveret.
- **Anbefalet:** Følg disse trin:

    1. I Excel-desktopprogrammet kan du redigere Excel-projektmappen på en af følgende måder:

        - I regnearket **Sheet1** skal du fjerne fletning af celle **A1** og **A2**.
        - Ret referencen for navnet **ReportTitle** fra **=Sheet1!$A$2** til **=Sheet1!$A$1**.

        ![Gennemse resultaterne af ændret reference i den designede Excel-projektmappe i Excel-skrivebordsprogrammet.](./media/er-fillable-excel-example2-3.png)

    2. På siden **Formatdesigner** skal du [importere](er-fillable-excel.md#template-import) den ændrede Excel-projektmappe til det ER-format, der kan redigeres, for at opdatere den eksisterende skabelon.
    3. Kør det ændrede ER format.

        ![Gennemse det genererede dokument i Excel-skrivebordsprogrammet.](./media/er-fillable-excel-example2-4.png)

## <a name="limitations"></a>Begrænsninger

### <a name="known-epplus-library-limitations"></a>Kendte begrænsninger for EPPlus-bibliotek

#### <a name="external-data-sources"></a>Eksterne datakilder

Hvis en af skabelonerne indeholder en pivottabel, der er baseret på en PowerPivot-model, der henviser til en [ekstern datakilde](https://support.microsoft.com/office/create-a-pivottable-with-an-external-data-source-db50d01d-2e1c-43bd-bfb5-b76a818a927b), og funktionen **Aktivér brug af EPPlus-bibliotek i elektronisk rapporteringsstruktur** er aktiveret, modtager du følgende fejlmeddelelse, når du kører et ER-format, der bruger denne skabelon til at generere et udgående dokument i Excel-format: "Cachekilden er ikke et regneark". Du kan løse dette problem på følgende måder:

- **Anbefales:** Ret designet af den Excel-løsning, du bruger:

    1. Isoler den del, der indeholder pivottabeller, i en separat Excel-projektmappe (projektmappe A). 
    2. Brug ER til at generere en anden Excel-projektmappe (projektmappe B) fra Finans, der indeholder de nødvendige oplysninger. 
    3. Referer til projektmappe B i projektmappe A, så snart projektmappe B er genereret.

- Deaktiver funktionen **Aktivér brug af EPPlus-bibliotek i Elektronisk rapporteringsstruktur** for at bruge en anden indstilling end EPPlus. 

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)

[Designe en konfiguration til generering af rapporter i OPENXML-format](tasks\er-design-reports-openxml-2016-11.md)

[Redigere elektroniske rapporteringsformater ved at genanvende Excel-skabeloner](modify-electronic-reporting-format-reapply-excel-template.md)

[Brug vandrette områder, der kan udvides, til at tilføje kolonner i Excel-rapporter dynamisk](tasks/er-horizontal-1.md)

[Integrere billeder og figurer i de dokumenter, du opretter ved hjælp af ER](electronic-reporting-embed-images-shapes.md)

[Konfigurer Elektronisk rapportering (ER) for at trække data over i Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
