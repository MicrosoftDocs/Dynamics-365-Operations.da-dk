---
title: Designe en konfiguration til generering af dokumenter i Excel-format
description: Dette emne giver oplysninger om, hvordan du kan designe et ER-format (Electronic reporting) til at udfylde en Excel-skabelon og derefter generere udgående Excel-formatdokumenter.
author: NickSelin
manager: AnnBe
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: d5733e40c67f9c97b04f126f7c3cfea9d4f8f5b5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686532"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Designe en konfiguration til generering af dokumenter i Excel-format

[!include[banner](../includes/banner.md)]

Du kan designe en formatkonfiguration [ER (Electronic reporting)](general-electronic-reporting.md), der har et ER-[formatkomponent](general-electronic-reporting.md#FormatComponentOutbound), som du kan konfigurere til at generere et udgående dokument i et Microsoft Excel-projektmappeformat. Specifikke ER-formatkomponenter skal bruges til dette formål.

Hvis du vil vide mere om denne funktion, skal du følge trinnene i emnet, [Designe en konfiguration til generering af rapporter i OPENXML-format](tasks/er-design-reports-openxml-2016-11.md).

## <a name="add-a-new-er-format"></a>Tilføj et nyt ER-format

Når du tilføjer en ny ER-formatkonfiguration for at generere et udgående dokument i et Excel-projektmappeformat, skal du enten vælge **Excel**-værdien for attributten **Formattype** for formatet eller lade attributten **Formattype** være tom.

- Hvis du vælger **Excel**, kan du konfigurere formatet til kun at oprette et udgående dokument i Excel-format.
- Hvis du lader attributten være tom, kan du konfigurere formatet til at generere et udgående dokument i et hvilket som helst format, der understøttes af ER-strukturen.

Hvis du vil konfigurere ER-formatkomponenten af konfigurationen, skal du vælge **Designer** i handlingsruden og åbne ER-formatkomponenten for redigering i ER-operationsdesigner.

![Siden Konfigurationer](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Excel-filkomponent

### <a name="manual-entry"></a>Manuel indtastning

Du skal føje en **Excel \\Fil**-komponent til det konfigurerede ER-format, hvis du vil generere et udgående dokument i Excel-format.

![Excel-filkomponent](./media/er-excel-format-add-file-component.png)

Hvis du vil angive layoutet for det udgående dokument, skal du vedhæfte en Excel-projektmappe med filtypenavnet .xlsx til **Excel-\\fil**-komponenten som skabelon til udgående dokumenter.

> [!NOTE]
> Når du manuelt tilknytter en skabelon, skal du bruge en [dokumenttype](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types), der er konfigureret til dette formål i [ER-parametrene](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

![Føje en tilknytning til Excel\Fil-komponenten](./media/er-excel-format-add-file-component2.png)

Hvis du vil angive, hvordan den tilknyttede skabelon skal udfyldes, når du kører det konfigurerede ER-format, skal du føje indlejrede komponenter **Ark**, **Område** og **Celle** til komponenten **Excel\\Fil**. Alle indlejrede komponenter skal knyttes til et navngivet element i Excel.

### <a name="template-import"></a>Skabelonimport

Du kan vælge **Importér fra Excel** under fanen **Importer** i handlingsruden for at importere en ny skabelon til et tomt ER-format. I dette eksempel oprettes der automatisk en **Excel\\Fil**-komponent, og den importerede skabelon knyttes til den. Alle nødvendige ER-komponenter oprettes automatisk, baseret på listen over de Excel-navngivne elementer, der registreres.

![Vælge Importér fra Excel](./media/er-excel-format-import-template.png)

> [!NOTE]
> Hvis du vil oprette det valgfrie **Ark**-element i det redigerbare ER-format, skal du angive indstillingen **Opret Excel-arkformatelement** til **Ja**.

## <a name="sheet-component"></a>Arkkomponent

**A**-komponenten angiver et regneark i den tilknyttede Excel-projektmappe, der skal udfyldes. Navnet på regnearket i en Excel-skabelon er defineret i egenskaben **Ark** for denne komponent.

> [!NOTE]
> Denne komponent er valgfri for Excel-projektmapper, der indeholder et enkelt regneark.

Under fanen **Tilknytning** i ER-operationsdesigneren kan du konfigurere egenskaben **Aktiveret** for en **Ark**-komponent for at angive, om komponenten skal placeres i et genereret dokument:

- Hvis et udtryk af egenskaben **Aktiveret** er konfigureret til at returnere **Sand** på kørselstidspunktet, eller, hvis der slet ikke er konfigureret et udtryk, vil det relevante regneark blive taget med i det genererede dokument.
- Hvis et udtryk af egenskaben **Aktiveret** er konfigureret til at returnere **Falsk** på kørselstidspunktet, indeholder det genererede dokument ikke et regneark.

![Eksempel på en arkkomponent](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Områdekomponent

Komponenten **Område** angiver et Excel-område, der skal styres af denne ER-komponent. Navnet på området er defineret i **Excel-området** for denne komponent.

Egenskaben **Replikeringsretning** angiver, om og hvordan området skal gentages i et genereret dokument:

- Hvis egenskaben **Replikeringsretning** er angivet til **Ingen replikering**, gentages det relevante Excel-område ikke i det genererede dokument.
- Hvis egenskaben **Replikeringsretning** er angivet til **Lodret**, gentages det relevante Excel-område i det genererede dokument. Alle replikerede områder placeres under det oprindelige område i en Excel-skabelon. Antallet af gentagelser defineres af antallet af poster i en datakilde for den **Postlistetype**, der er bundet til denne ER-komponent.
- Hvis egenskaben **Replikeringsretning** er angivet til **Vandret**, gentages det relevante Excel-område i det genererede dokument. Alle replikerede områder placeres til højre for det oprindelige område i en Excel-skabelon. Antallet af gentagelser defineres af antallet af poster i en datakilde for den **Postlistetype**, der er bundet til denne ER-komponent.

Hvis du vil vide mere om vandret replikering, skal du følge trinnene i [Brug vandrette, udvidelige områder til dynamisk at tilføje kolonner i Excel-rapporter](tasks/er-horizontal-1.md).

Komponenten **Område** kan have andre indlejrede ER-komponenter, der bruges til at angive værdier i de relevante navngivne Excel-områder.

- Hvis en komponent i gruppen **Tekst** bruges til at angive værdier, indtastes værdien i et Excel-område som en tekstværdi.

    > [!NOTE]
    > Du kan bruge dette mønster til at formatere angivne værdier på basis af den landestandard, der er defineret i programmet.

- Hvis komponenten **Celle** i gruppen **Excel** bruges til at angive værdier, indtastes værdien i et Excel-område som en værdi af den datatype, der er defineret af bindingen for den pågældende **Celle**-komponent (f.eks. **Streng**, **Reelt tal** eller **Heltal**).

    > [!NOTE]
    > Brug dette mønster til at gøre Excel-programmet i stand til at formatere angivne værdier på basis af landestandarden på den lokale computer, der åbner det udgående dokument.

Under fanen **Tilknytning** i ER-operationsdesigneren kan du konfigurere egenskaben **Aktiveret** for en **Område**-komponent for at angive, om komponenten skal placeres i et genereret dokument:

- Hvis et udtryk af egenskaben **Aktiveret** er konfigureret til at returnere **Sand** på kørselstidspunktet, eller, hvis der slet ikke er konfigureret et område, vil det relevante område blive udfyldt i det genererede dokument.
- Hvis et udtryk af egenskaben **Aktiveret** er konfigureret til at returnere **Falsk** på kørselstidspunktet, og hvis dette område ikke repræsenterer rækker eller kolonner i deres helhed, vil det relevante område ikke blive udfyldt i det genererede dokument.
- Hvis et udtryk af egenskaben **Aktiveret** er konfigureret til at returnere **Falsk** på kørselstidspunktet, og hvis dette område repræsenterer rækker eller kolonner i deres helhed, vil det generede dokument indeholde disse rækker og kolonner som skjulte rækker og kolonner.

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

## <a name="edit-an-added-er-format"></a>Redigere et tilføjet ER-format

### <a name="update-a-template"></a>Opdatere en skabelon

Du kan vælge **Opdater fra Excel** under fanen **Importer** i handlingsruden for at importere en opdateret skabelon til et redigerbart ER-format. Under denne proces erstattes en skabelon for den valgte komponent **Excel\\Fil** med en ny skabelon. Indholdet af det redigerbare ER-format synkroniseres med indholdet af den opdaterede ER-skabelon.

- Der oprettes automatisk en ny ER-formatkomponent for alle Excel-navne, hvis ER-formatkomponenten ikke findes i det redigerbare format.
- Alle ER-formatkomponenter slettes fra det redigerbare ER-format, hvis det rette Excel-navn ikke findes.

> [!NOTE]
> Angiv indstillingen **Opret Excel-arkformatelement** til **Ja**, hvis du vil oprette det valgfri **Ark**-element i det redigerbare ER-format.
>
> Hvis det redigerbare ER-format oprindeligt indeholdte **Ark**-elementer, anbefales det, at du angiver indstillingen **Opret Excel-arkformatelement** til **Ja**, når du importerer en opdateret skabelon. Ellers oprettes alle indlejrede elementer i det oprindelige **Ark**-element fra bunden. Derfor går alle bindinger af de genoprettede formatelementer tabt i det opdaterede ER-format.

![Indstillingen Opret Excel-arkformatelement i dialogboksen Opdater fra Excel](./media/er-excel-format-update-template.png)

Hvis du vil vide mere om denne funktion, skal du udføre trinnene i [Redigere elektronisk rapporteringsformat ved at genanvende Excel-skabeloner](modify-electronic-reporting-format-reapply-excel-template.md).

## <a name="validate-an-er-format"></a>Validere et ER-format

Når du validerer et ER-format, der kan redigeres, sker der en konsistenskontrol for at sikre, at Excel-navnet findes i den Excel-skabelon, der aktuelt bruges. Du får besked om eventuelle uoverensstemmelser. Ved visse inkonsistenser tilbydes muligheden for at rette problemer automatisk.

![Validering og fejlmeddelelse](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>Styre beregningen af Excel-formler

Når et udgående dokument i Microsoft Excel-projektmappeformat genereres, kan visse celler i dette dokument indeholde Excel-formler. Når funktionen **Aktivér brug af EPPlus-bibliotek i den elektroniske rapporteringsstruktur** er aktiveret, kan du styre, hvornår formlerne beregnes, ved at ændre værdien i [parameteren](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) **Beregningsindstillinger** i den Excel-skabelon, der bruges:

- Vælg **Automatisk** for at genberegne alle afhængige formler, hver gang et genereret dokument føjes til nye områder, celler osv.
    >[!NOTE]
    > Dette kan forårsage et problem med ydeevnen for Excel-skabeloner, der indeholder flere relaterede formler.
- Vælg **Manuel** for at undgå genberegning af formler, når der genereres et dokument.
    >[!NOTE]
    > Genberegning af formler gennemtvinges manuelt, når et genereret dokument åbnes med henblik på visning i Excel.
    > Brug ikke denne indstilling, hvis du konfigurerer en ER-destination, der forudsætter brug af et genereret dokument uden visning i Excel (PDF-konvertering, afsendelse af mail osv.), da det genererede dokument muligvis ikke indeholder værdier i celler, der indeholder formler.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)

[Designe en konfiguration til generering af rapporter i OPENXML-format](tasks\er-design-reports-openxml-2016-11.md)

[Redigere elektroniske rapporteringsformater ved at genanvende Excel-skabeloner](modify-electronic-reporting-format-reapply-excel-template.md)

[Brug vandrette områder, der kan udvides, til at tilføje kolonner i Excel-rapporter dynamisk](tasks/er-horizontal-1.md)

[Integrere billeder og figurer i de dokumenter, du opretter ved hjælp af ER](electronic-reporting-embed-images-shapes.md)

[Konfigurer Elektronisk rapportering (ER) for at trække data over i Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]