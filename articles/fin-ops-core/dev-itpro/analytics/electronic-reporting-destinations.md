---
title: Destinationer for elektronisk rapportering (ER)
description: Dette emne indeholder oplysninger om styring af destinationer for elektronisk rapportering, de forskellige typer destinationer, der understøttes, og sikkerhedsovervejelser.
author: nselin
manager: AnnBe
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 725ded9d777a65e5a38a7971c1da8cb74cf0dd47
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097275"
---
# <a name="electronic-reporting-er-destinations"></a>Destinationer for elektronisk rapportering (ER)

[!include [banner](../includes/banner.md)]

Du kan konfigurere en destination til hver formatkonfiguration for elektronisk rapportering (ER) og dens outputkomponent (en mappe eller en fil). Brugere, der har de nødvendige adgangsrettigheder, kan også ændre indstillingerne på kørselstidspunktet. I dette emne forklares ER-destinationsstyring, destinationstyperne, der understøttes, og sikkerhedsmæssige overvejelser.

Konfigurationer af ER-formater består normalt af mindst én output-komponent: en fil. Normalt indeholder konfigurationer flere filoutputkomponenter af forskellige typer (for eksempel XML, TXT, XLSX, DOCX eller PDF), der er grupperet i enten en enkelt mappe eller flere mapper. Med styring af ER-destination kan du forudkonfigurere, hvad sker der, når hver komponent køres. Når en konfiguration køres, åbnes som standard en dialogboks, hvor du kan gemme eller åbne filen. Samme funktionsmåde forekommer også, når du importerer en ER-konfiguration og ikke konfigurerer særlige destinationer for den. Når der oprettes en destination for en vigtig outputkomponent, tilsidesætter denne destination standardindstillingen, og mappen eller filen sendes på grundlag af destinationens indstillinger.

## <a name="availability-and-general-prerequisites"></a>Tilgængelighed og generelle forudsætninger

Funktionaliteten for ER-destinationer findes ikke i Microsoft Dynamics AX 7.0 (februar 2016). Du skal derfor installere Microsoft Dynamics 365 for Operations version 1611 (november 2016) eller nyere for at kunne bruge følgende destinationstyper:

- [E-mail](er-destination-type-email.md)
- [Arkivér](er-destination-type-archive.md)
- [Filer](er-destination-type-file.md)
- [Skærm](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)

Du kan også vælge at installere en af følgende forudsætninger. Du skal dog være opmærksom på, at disse alternativer giver en mere begrænset ER-destinationsoplevelse.

- Microsoft Dynamics AX-programversion 7.0.1 (maj 2016)
- [Programhotfix til styring af destination for elektronisk rapportering](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Der findes også en [Udskriv](er-destination-type-print.md)-destinationstype. Hvis du vil bruge den, skal du installere Microsoft Dynamics 365 Finance version 10.0.9 (april 2020).

## <a name="overview"></a>Oversigt

Du kan kun konfigurere destinationer for ER-konfigurationer, der er [importeret](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) til aktuelle Finans-forekomst, og for de formater, der er tilgængelige på siden **Konfigurationer for elektronisk rapportering**. Funktionaliteten for ER-destinationsstyring er tilgængelig på **Organisationsadministration** \> **Elektronisk rapportering** \> **Destination for elektronisk rapportering**.

### <a name="default-behavior"></a>Standardfunktionsmåde

Standardfunktionsmåden for en ER-formatkonfiguration afhænger af den udførelsestype, du angiver, når et ER-format starter.

Hvis du angiver indstillingen **Batchbehandling** til **Nej** i dialogboksen **Intrastat-rapport** på oversigtspanelet **Kør i baggrunden**, køres der øjeblikkeligt et ER-format i interaktiv tilstand. Når denne udførelse er fuldført, er et genereret udgående dokument gjort tilgængeligt for download.

Hvis du angiver **Batchbehandling** til **Ja**, køres et ER-format i [batch](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/batch-processing-overview)-tilstand. Det relevante batchjob oprettes på basis af de parametre, du angiver på fanen **Kør i baggrunden** i dialogboksen **ER-parametre**.

> [!NOTE]
> Jobbeskrivelsen informerer dig om kørslen af en ER-formattilknytning. Den indeholder også navnet på den kørte ER-komponent.

[![Køre et ER-format](./media/ER_Destinations-RunInBatchMode.png)](./media/ER_Destinations-RunInBatchMode.png)

Du kan finde oplysninger om dette job på flere steder:

- Gå til **Generelt** \> **Forespørgsler** \> **Batchjob** \> **Mine batchjob** for at kontrollere status for det planlagte job.
- Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Elektroniske rapportingsjob** for at kontrollere status for det planlagte job og udførelsesresultaterne af det fuldførte job. Når jobudførelsen er fuldført, skal du vælge **Vis filer** på siden **Elektroniske rapportingsjob** for at få et genereret udgående dokument.

    > [!NOTE]
    > Dette dokument gemmes som en vedhæftet fil for den aktuelle jobpost og styres af strukturen [Dokumentstyring](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management). Den [dokumenttype](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types), der bruges til at gemme ER-artefakter af denne type, konfigureres i [ER-parametrene](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

- På siden **Elektroniske rapporteringsjob** skal du vælge **Vis filer** for at få vist listen over de fejl og advarsler, der blev genereret under jobudførelsen.

    [![Gennemse ER-joblisten](./media/ER_Destinations-ReviewERJobs.png)](./media/ER_Destinations-ReviewERJobs.png)

### <a name="user-configured-behavior"></a>Brugerkonfigureret funktionsmåde

På siden **Destination for elektronisk rapportering** kan du tilsidesætte standardfunktionsmåden for en konfiguration. Importerede konfigurationer vises ikke på denne side, før du vælger **Ny** og derefter i feltet **Reference** vælger en konfiguration at oprette destinationsindstillinger for.

[![Vælge en konfiguration i feltet Reference](./media/ER_Destinations-SelectFormat.png)](./media/ER_Destinations-SelectFormat.png)

Når du har oprettet en reference, kan du oprette en fildestination for hver outputkomponent for **Mappe** eller **Fil** i det ER-format, der refereres til.

[![Oprettelse af en fildestination](./media/ER_Destinations-ConfigureElementDestination.png)](./media/ER_Destinations-ConfigureElementDestination.png)

Derefter kan du i dialogboksen **Indstillinger for destination** aktivere og deaktivere individuelle destinationer for fildestinationen. Knappen **Indstillinger** bruges til at styre alle destinationer for en valgt fildestination. I dialogboksen **Indstillinger for destination** kan du styre hver destination separat ved at vælge indstillingen **Aktiveret** for destinationen.

I versioner af Finans **før version 10.0.9** kan du oprette **én fildestination** for hver outputkomponent af samme format som f.eks. en mappe eller en fil, der er markeret i feltet **Filnavn**. Men i **version 10.0.9 og senere** kan du oprette **flere fildestinationer** for hver outputkomponent af samme format.

Du kan f.eks. bruge denne egenskab til at konfigurere fildestinationer for en filkomponent, der bruges til at generere et udgående dokument i Excel-format. En destination ([Arkiv](er-destination-type-archive.md)) kan konfigureres til at gemme den oprindelige Excel-fil i et ER-jobarkiv, og en anden destination ([E-mail](er-destination-type-email.md)) kan konfigureres til samtidigt at [konvertere](#OutputConversionToPDF) Excel-filen til PDF-format og sende PDF-filen med e-mail.

[![Konfigurere flere destinationer for et enkelt formatelement](./media/ER_Destinations-SampleDestinations.png)](./media/ER_Destinations-SampleDestinations.png)

Når du kører et ER-format, køres altid alle de destinationer, der er konfigureret for komponenter i formatet. Derudover er funktionaliteten af ER-destinationer blevet forbedret i Finans **version 10.0.17 og senere**, og den giver dig mulighed for at konfigurere forskellige destinationssæt til et enkelt ER-format. Denne konfiguration markerer hvert sæt som konfigureret til en bestemt brugerhandling. ER-API'en er [udvidet](er-apis-app10-0-17.md), så der kan leveres en handling, som brugeren udfører ved at køre et ER-format. Den handlingskode, der leveres, overføres til ER-destinationer. Du kan køre forskellige destinationer i et ER-format, afhængigt af den leverede handlingskode. Yderligere oplysninger finder du i [Konfigurere handlingsafhængige ER-destinationer](er-action-dependent-destinations.md).

## <a name="destination-types"></a>Destinationstyper

Følgende destinationer understøttes i øjeblikket for ER-formater. Du kan deaktivere eller aktivere alle typer på samme tid. På denne måde kan du enten gøre ingenting eller sende komponenten til alle konfigurerede destinationer.

- [E-mail](er-destination-type-email.md)
- [Arkivér](er-destination-type-archive.md)
- [Filer](er-destination-type-file.md)
- [Skærm](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)
- [Udskrivning](er-destination-type-print.md)

## <a name="applicability"></a>Anvendelighed

Du kan konfigurere destinationer kun for ER-konfigurationer, der er importeret, og for de formater, der er tilgængelige på siden **Konfigurationer for elektronisk rapportering**.

> [!NOTE]
> Konfigurerede destinationer er firmaspecifikke. Hvis du planlægger at bruge et ER-format i forskellige firmaer i den aktuelle forekomst af Finans, skal du konfigurere destinationer for det pågældende ER-format for hvert af disse firmaer.

Når du konfigurerer fildestinationer for et valgt format, skal du konfigurere dem for hele formatet.

[![Konfigurationslink](./media/ER_Destinations-ConfigurationLink.png)](./media/ER_Destinations-ConfigurationLink.png)

Samtidig kan du have flere [versioner](general-electronic-reporting.md#component-versioning) af det format, der er importeret til den aktuelle forekomst af Finans. Du kan få vist dem, hvis du vælger linket **Konfiguration**, der tilbydes, når du vælger feltet **Reference**.

[![Konfigurationsversioner](./media/ER_Destinations-ConfigurationVersions.png)](./media/ER_Destinations-ConfigurationVersions.png)

Som standard anvendes konfigurerede destinationer kun, når du kører en ER-formatversion, der har status som enten **Fuldført** eller **Delt**. Du skal dog sommetider bruge konfigurerede destinationer, når kladdeversionen af et ER-format køres. Det kan f.eks. være, at du redigerer en kladdeversion af dit format, og du vil bruge konfigurerede destinationer til at teste, hvordan det genererede output leveres. Benyt følgende fremgangsmåde til at anvende destinationer for et ER-format, når kladdeversionen køres.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
3. Angiv indstillingen **Anvend destinationer for kladdetilstand** til **Ja**.

[![Indstillingen Anvend destinationer for kladdetilstand](./media/ER_Destinations-UserSetting1.png)](./media/ER_Destinations-UserSetting1.png)

Hvis du vil bruge kladdeversionen af et ER-format, skal du markere ER-formatet i overensstemmelse hermed.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
3. Angiv indstillingen **Indstillingen Kør** til **Ja**.

[![Indstillingen Kør](./media/ER_Destinations-UserSetting2.png)](./media/ER_Destinations-UserSetting2.png)

Når du har fuldført denne konfiguration, bliver indstillingen **Kør kladde** tilgængelig for ER-formater, som du redigerer. Angiv denne indstilling til **Ja** for at begynde at bruge kladdeversionen af formatet, når formatet køres.

[![Indstillingen Kør kladde](./media/ER_Destinations-FormatSetting.png)](./media/ER_Destinations-FormatSetting.png)

## <a name="destination-failure-handling"></a><a name="DestinationFailure"></a>Håndtering af destinationsfejl

Normalt køres et ER-format inden for området for en bestemt forretningsproces. Leveringen af et udgående dokument, der genereres under udførelsen af et ER-format, skal dog nogle gange ses som en del af den pågældende forretningsproces. I dette tilfælde skal udførelsen af forretningsprocessen annulleres, hvis leveringen af et genereret udgående dokument til en konfigureret destination ikke lykkes. Hvis du vil konfigurere den rette ER-destination, skal du vælge indstillingen **Stop behandling ved fejl**.

Du kan f.eks. konfigurere behandling af kreditorbetalinger, så ER-formatet **ISO20022-kreditoverførsel** køres for at generere betalingsfilen og de supplerende dokumenter (f.eks. følgeskrivelse og kontrolrapport). Hvis en betaling kun skal anses for at være behandlet korrekt, hvis følgeskrivelsen er leveret korrekt via mail, skal du markere afkrydsningsfeltet **Stop behandling ved fejl** for komponenten **CoveringLetter** i den rette destinationsfil som vist i følgende illustration. I dette tilfælde ændres status for den betaling, der er valgt til behandling, kun fra **Ingen** til **Sendt**, når det følgebrev, der er oprettet, accepteres til levering af en e-mailudbyder, der er konfigureret i Finans-forekomsten.

[![Konfigurere proceshåndtering for fildestinationsfejl](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)

Hvis du fjerner markeringen af afkrydsningsfeltet **Stop behandling ved fejl** for komponenten **CoveringLetter** på destinationen, anses en betaling for at være behandlet korrekt, også selv om følgebrevet ikke er leveret korrekt via mail. Status for betalingen ændres fra **Ingen** til **Sendt**, selvom følgebrevet ikke kan sendes, f.eks. fordi modtagerens eller afsenderens e-mailadresse mangler eller er forkert.

## <a name="output-conversion-to-pdf"></a><a name="OutputConversionToPDF"></a>Konvertering af output til PDF

Du kan bruge PDF-konverteringsindstillingen til at konvertere output i Microsoft Office-format (Excel eller Word) til PDF-format.

### <a name="make-pdf-conversion-available"></a>Stille PDF-konvertering til rådighed

Hvis du vil stille PDF-konverteringsindstillingen til rådighed i den aktuelle Finans-forekomst, skal du åbne arbejdsområdet **Funktionsstyring** og aktivere funktionen **Konverter udgående dokumenter til elektroniske rapportering fra Microsoft Office-formater til PDF**.

[![Aktivere PDF-konvertering af funktionen udgående dokumenter i Funktionsstyring](./media/ER_Destinations-EnablePdfConversionFeature.png)](./media/ER_Destinations-EnablePdfConversionFeature.png)

### <a name="applicability"></a>Anvendelighed

PDF-konverteringsindstillingen kan kun aktiveres for de filkomponenter, der bruges til at oprette output i Office-format (Excel eller Word) (**Excel-fil**). Når denne indstilling er slået til, konverteres output, der genereres i Office-format, automatisk til PDF-format.

### <a name="limitations"></a>Begrænsninger

> [!NOTE]
> Denne funktion er en prøveversionsfunktion og er underlagt de vilkår for anvendelse, der er beskrevet i [Supplerende vilkår for anvendelse for Microsoft Dynamics 365-prøveversioner](https://go.microsoft.com/fwlink/?linkid=2105274).

PDF-konverteringsindstillingen er kun tilgængelig for skyinstallationer.

Det fremstillede PDF-dokument er begrænset til maksimalt 300 sider.

På nuværende tidspunkt understøttes kun liggende sideretning i det PDF-dokument, der fremstilles af et Excel-output, i Finans **version 10.0.9**. I Finans **version 10.0.10 (maj 2020) og nyere** kan du angive [sideretningen](#SelectPdfPageOrientation) i det PDF-dokument, der oprettes ud fra et Excel-output, mens du konfigurerer en ER-destination.

Det er kun de almindelige systemskrifttyper i Windows-operativsystemet, der bruges til konvertering af et output, der ikke indeholder integrerede skrifttyper.

### <a name="use-the-pdf-conversion-option"></a>Bruge PDF-konverteringsindstillingen

Hvis du vil aktivere PDF-konvertering for en fildestination, skal du markere afkrydsningsfeltet **Konverter til PDF**.

[![Aktivere PDF-konvertering for en fildestination](./media/ER_Destinations-TurnOnPDFConversion.png)](./media/ER_Destinations-TurnOnPDFConversion.png)

### <a name=""></a><a name="SelectPdfPageOrientation">Vælge en sideretning til PDF-konvertering</a>

Hvis du opretter en ER-konfiguration i Excel-format og vil konvertere den til PDF-format, kan du angive sideretningen i PDF-dokumentet. Når du markerer afkrydsningsfeltet **Konverter til PDF** for at aktivere PDF-konvertering for en fildestination, der opretter en outputfil i Excel-format, bliver feltet **Sideretning** tilgængeligt i oversigtspanelet **Indstillinger for PDF-konvertering**. Vælg den foretrukne retning i feltet **Sideretning**.

[![Vælge en sideretning til PDF-konvertering](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)

> [!NOTE]
> Hvis du vil have mulighed for at vælge PDF-sideretningen, skal du installere Finans version 10.0.10 eller nyere.
>
> Den valgte sideretning anvendes på alle de ER-konfigurationer, der genereres i Excel-format og konverteres derefter til PDF-format.
>
> Hvis en ER-konfiguration i Word-format konverteres til PDF-format, hentes sideretningen i PDF-dokumentet fra Word-dokument.

## <a name="security-considerations"></a>Sikkerhedsovervejelser

To typer rettigheder og opgaver bruges til ER-destinationer. Én type styrer en brugers generelle mulighed for at opretholde de destinationer, der er konfigureret for en juridisk enhed (dvs. den styrer adgang til siden **Destinationer for elektronisk rapportering**). Den anden type styrer en programbrugers mulighed for på kørselstidspunktet at tilsidesætte de destinationsindstillinger, der er konfigureret af en ER-udvikler eller en funktionel konsulent i elektronisk rapportering.

| Rolle (AOT-navn)                     | Rollenavn                                  | Arbejdsopgave (AOT-navn)                     | Navn på arbejdsopgave                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Udvikler til elektronisk rapportering             | ERFormatDestinationConfigure        | Konfigurer destination for elektronisk rapportformat                |
| ERFunctionalConsultant              | Funktionel konsulent i elektronisk rapportering | ERFormatDestinationConfigure        | Konfigurer destination for elektronisk rapportformat                |
| PaymAccountsPayablePaymentsClerk    | Ansvarlig for kreditorbetalinger            | ERFormatDestinationRuntimeConfigure | Konfigurer destination for elektronisk rapportformat under kørsel |
| PaymAccountsReceivablePaymentsClerk | Ansvarlig for debitorbetalinger         | ERFormatDestinationRuntimeConfigure | Konfigurer destination for elektronisk rapportformat under kørsel |

> [!NOTE]
> To rettigheder bruges i de foregående opgaver. Disse rettigheder har de samme navne som de tilsvarende opgaver: **ERFormatDestinationConfigure** og **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Jeg har importeret elektroniske konfigurationer, og jeg kan se dem på siden Konfigurationer for elektronisk rapportering. Men hvorfor kan jeg ikke se dem på siden Destinationer for elektronisk rapportering?

Sørg for at vælge **Ny** og derefter vælge en konfiguration i feltet **Reference**. Siden **Destinationer for elektronisk rapportering** viser kun de konfigurationer, som destinationer er konfigureret for.

### <a name="is-there-any-way-to-define-which-microsoft-azure-storage-account-and-azure-blob-storage-are-used"></a>Er der nogen måde at definere, hvilken Microsoft Azure Storage-konto og hvilket Azure Blob-lager der skal bruges?

Nr. Standard Microsoft Azure Blob-lageret, der er defineret og anvendes til dokumentstyringssystemet, bruges.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Hvad er formålet med fildestinationen i indstillingerne for destinationen? Hvad gør denne indstilling?

**Fil**-destinationen bruges til at styre en dialogboks i din webbrowser, når du kører et ER-format i interaktiv tilstand. Hvis du aktiverer denne destination, eller hvis ingen destination er defineret for en konfiguration, vises dialogboksen Åbn eller Gem i din webbrowser, når der oprettes en outputfil.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Kan du give et eksempel på den formel, der refererer til en kreditorkonto, som jeg kan sende mail til?

Formlen er specifik for ER-konfigurationen. Hvis du bruger konfigurationen ISO 20022 SEPA-kreditoverførsler, kan du f.eks bruge **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** eller **model. Payments.Creditor.Identification.SourceID** til at få en tilknyttet kreditorkonto.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-grouped-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>En af mine formatkonfigurationer indeholder flere filer, der er grupperet i én mappe (f.eks. indeholder Mappe1 Fil1, Fil2 og Fil3). Hvordan konfigurerer jeg destinationer, så Mappe1.zip slet ikke oprettes, fil1 sendes via mail, fil2 sendes til SharePoint, og jeg kan åbne fil3 straks, når konfigurationen er udført?

Dit format skal først være tilgængeligt i ER-konfigurationerne. Hvis denne forudsætning er opfyldt, kan du åbne siden **Destination for elektronisk rapportering** og oprette en ny reference til konfigurationen. Derefter skal du have fire fildestinationer, én for hver outputkomponent. Opret den første fildestination, giv den et navn som f.eks. **Mappe**, og vælg et filnavn, der repræsenterer en mappe i din konfiguration. Vælg derefter **Indstillinger**, og sørg for, at alle destinationer er deaktiveret. Mappen vil ikke blive oprettet for denne fildestination. Som standard fungerer filerne på samme måde på grund af hierarkisk afhængigheder mellem filerne og overordnede mapper. Med andre ord sendes de ikke et vilkårligt sted hen. Hvis du vil tilsidesætte denne standardfunktionsmåde, skal du oprette tre yderligere fildestinationer, én for hver fil. I destinationsindstillingerne for hver skal du aktivere den destination, som filen skal sendes til.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Konfigurere handlingsafhængige ER-destinationer](er-action-dependent-destinations.md)
