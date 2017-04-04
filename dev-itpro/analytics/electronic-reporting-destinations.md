---
title: Destinationer for elektronisk rapportering
description: "Du kan konfigurere en destination til hver formatkonfiguration for elektronisk rapportering (ER) og dens outputkomponent (en mappe eller en fil). Brugere, der er tildelt passende adgangsrettigheder, kan også ændre indstillingerne for destinationen på kørselstidspunktet. I denne artikel forklares ER-destinationsstyring, destinationstyperne, der understøttes, og sikkerhedsmæssige overvejelser."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: d38d05fe445bf0326d408038dff84ccf8c0ff64c
ms.lasthandoff: 03/31/2017


---

# <a name="electronic-reporting-destinations"></a>Destinationer for elektronisk rapportering

Du kan konfigurere en destination til hver formatkonfiguration for elektronisk rapportering (ER) og dens outputkomponent (en mappe eller en fil). Brugere, der er tildelt passende adgangsrettigheder, kan også ændre indstillingerne for destinationen på kørselstidspunktet. I denne artikel forklares ER-destinationsstyring, destinationstyperne, der understøttes, og sikkerhedsmæssige overvejelser.

Konfigurationer af formater for elektronisk rapportering (ER) består normalt af mindst én output-komponent: en fil. Normalt indeholder konfigurationer flere filoutputkomponenter af forskellige typer (for eksempel XML, TXT eller XLSX), der er grupperet i enten en enkelt mappe eller flere mapper. Med styring af ER-destination kan du forudkonfigurere, hvad sker der, når hver komponent køres. Som standard, når du kører en konfiguration, vises en dialogboks, som brugeren kan gemme eller åbne filen. Samme funktionsmåde bruges også, når du importerer en ER-konfiguration og ikke konfigurerer særlige destinationer for den. Når der oprettes en destination for en vigtig outputkomponent, tilsidesætter denne destination standardindstillingen, og mappen eller filen sendes på grundlag af destinationens indstillinger.

## <a name="availability-and-general-prerequisites"></a>Tilgængelighed og generelle forudsætninger
Funktionen ER destinationer er ikke tilgængelig i Microsoft Dynamics 365 for operationer 7.0 (februar 2016) version. Derfor skal du installere Microsoft Dynamics 365 for operationer (November 2016 version) til at bruge alle de funktioner, der er beskrevet i dette emne. Du kan også installere en af følgende forudsætninger. Dog være opmærksom på, at disse alternative giver en mere begrænset erfaring af ER destination.

-   Microsoft Dynamics 365 for operationer programversion 7.0.1 (maj 2016)
-   ER destinationsstyring [programhotfix](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Du kan konfigurere destinationer kun for ER-konfigurationer, der er importeret, og for de formater, der er tilgængelige på siden **Konfigurationer for elektronisk rapportering**.

## <a name="overview"></a>Overblik
ER destination management funktionalitet er tilgængelig på **virksomhedsadministration**&gt;**elektronisk indberetning**. Her kan du tilsidesætte standardindstillingen for en konfiguration. Importerede konfigurationer vises først her, når du klikker på **Ny** og derefter i feltet **Reference** vælger en konfiguration at oprette destinationsindstillinger for.

[![Hvis du vælger en konfiguration i feltet Reference](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Når du har oprettet en reference, kan du oprette en fil destination for hver mappe eller en fil. 

[![Oprettelse af en fil-destination](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

**Bemærk:** Du kan oprette én fildestination for hver outputkomponent af samme format som f.eks. en mappe eller en fil, der er markeret i feltet **Filnavn**. Du kan derefter aktivere og deaktivere enkelte destinationer for destinationsfilen i den **indstillinger for printerdestination** dialogboksen. Knappen **Indstillinger** bruges til at styre alle destinationer for en valgt fildestination. I dialogboksen **Indstillinger for destination** kan du styre hver destination separat ved at vælge indstillingen **Aktiveret** for destinationen.

[![Dialogboksen Indstillinger for destination](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Destinationstyper
Forskellige typer destinationer understøttes. Du kan deaktivere eller aktivere alle typer på samme tid. På denne måde kan du enten gøre ingenting eller sende komponenten til alle konfigurerede destinationer. I følgende afsnit beskrives de destinationer, der understøttes.

### <a name="email-destination"></a>Maildestination

Indstil **Aktiveret **til **Ja** for at sende en outputfil via mail. Når denne indstilling er aktiveret, kan du angive e-mail-modtagerne, og rediger emnet og brødteksten i e-mailen. Du kan konfigurere konstant tekster til e-mailens emne og brødtekst, eller du kan bruge ER formler for dynamisk at oprette e-mail-tekster. Du kan konfigurere e-mail-adresser for ER på to måder. Konfigurationen kan udføres på samme måde, som funktionen Udskriv management i Dynamics 365 for operationer udfører den. Du kan også løse en e-mail-adresse ved hjælp af en direkte henvisning til konfigurationen ER gennem en formel.

### <a name="email-address-types"></a>Typer af e-mail-adresse

Når du klikker på **Rediger** for den **til** eller **Cc** felt, den **E-mail til** -dialogboks. Du kan derefter vælge typen e-mail-adresse.

[![E-mail-dialogboksen](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Udskriftsstyring

Hvis du vælger den **udskriftsstyring e-mail** type, kan du angive fast e-mail-adresser i den **til** felt. Hvis du vil bruge e-mail-adresser, der ikke er løst, skal du vælge kildetypen e-mail til en destination for filen. Følgende værdier understøttes: **kunde**, **leverandør**, **kundeemne**, **Kontakt**, **konkurrent**, **arbejder**, **ansøgeren**, **mulig kreditor**, og **ikke tilladt leverandør**. Brug knappen ud for, når du har valgt kildetype en e-mail, de **Email kildekontoen** at åbne den ** formel designer ** form. Du kan bruge denne form til at knytte en formel, der repræsenterer den valgte partskonto til e-mail-destination.

[![Konfigurere udskriftsstyring e-mail-type](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Bemærk, at formler er specifikke for ER-konfigurationen. Angiv en dokumentspecifik reference til en debitor- eller kreditorparttype i feltet **Formel**. I stedet for at skrive kan du finde datakildenoden, der repræsenterer debitor- eller kreditorkontoen, og derefter klikke på **Tilføj** datakilde for at opdatere formlen. Hvis du bruger konfigurationen ISO 20022 SEPA-kreditoverførsel, er den node, der repræsenterer en kreditorkonto, **'$PaymentsForCoveringLetter'. Creditor.Identification.SourceID**. Ellers skal du indtaste en strengværdi som f.eks. **DE-001** for at gemme en formel.

[![Formula designer](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

I den **E-mail til** dialogboksen, klik på genbrug bin ud for den **Email kildekontoen** at slette formlen for kildekontoen e-mail. Du kan også åbne formel designeren for at ændre en formel, der tidligere blev gemt. Hvis du vil tildele e-mail-adresser, skal du klikke på **Rediger** at åbne den **tildele e-mail-adresser** dialogboksen.

[![Tildeling af e-mail-adresser for en e-mail-destination](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Konfigurationsmail

Brug denne e-mail-type, hvis den konfiguration, du bruger, har en node i datakilderne, der repræsenterer en e-mail-adresse. Du kan bruge datakilder og funktioner i den formel designer til at få en korrekt formateret e-mail-adresse.

[![Tildeling af en e-mail-adresse-datakilde for en e-mail-destination](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Bemærk:** En SMTP-server (Simple Mail Transfer Protocol) skal konfigureres og være tilgængelig. Du kan angive din SMTP-server i Dynamics 365 for operationer, ved **systemadministration**&gt;**installation**&gt;**E-mail**&gt;**e-mail-parametre**.

### <a name="archive-destination"></a>Arkivdestination

Du kan bruge denne indstilling til at sende output til en Microsoft SharePoint-mappe eller Microsoft Azure Storage. Indstil **Aktiveret** til **Ja **for at sende output til en destination, der er defineret af den valgte dokumenttype. Kun dokumenttyper, hvor gruppen er indstillet til **Fil**, kan vælges. Du definerer dokumenttyper ved **virksomhedsadministration**&gt;**dokumentstyring**&gt;**de dokumenttyper**. Konfigurationen for ER-destinationer svarer til konfigurationen for dokumentstyringssystemet.

[![Typer af dokumentside](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

Lokaliteten bestemmer, hvor filen gemmes. Efter den **arkiv** destination er aktiveret, resultaterne af kørslen konfiguration kan gemmes i arkivet sagen. Du kan få vist resultaterne på **virksomhedsadministration**&gt;**elektronisk indberetning**&gt;**elektronisk indberetning arkiveret job**. **Bemærk:** kan du vælge en dokumenttype til arkivet i Dynamics 365 for operationer, Job på **virksomhedsadministration**&gt;**arbejdsområder**&gt;**elektronisk indberetning**&gt;**elektronisk indberetning parametre**.

#### <a name="sharepoint"></a>SharePoint

Du kan gemme en fil i en angivet SharePoint-mappe. Du kan definere standard-SharePoint-server på **virksomhedsadministration**&gt;**dokumentstyring**&gt;**management dokumentparametre**under den **SharePoint** tab. Når SharePoint-mappe er konfigureret, kan du markere den som den mappe, hvor ER outputtet skal gemmes for dokumenttypen. 

[![Hvis du vælger en SharePoint-mappe](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azure Storage

Når dokumenttype placeringen er indstillet til **Arkivbibliotek**, kan du gemme en fil på Azure Storage.

### <a name="file-destination"></a>Fildestination

Hvis du indstiller **aktiveret** til **Ja**, en Åbn- eller Gem dialogboks vises, når konfigurationen er afsluttet.

### <a name="screen-destination"></a>Skærmen destination

Hvis du indstiller **aktiveret** til **Ja**, oprettes der et eksempel på output. Du kan få vist nogle filtyper, som XML, TXT eller PDF-fil direkte i et browservindue. For andre filtyper, så Microsoft Excel eller Word, bruges tjenesten Microsoft Office Online.

### <a name="power-bi-destination"></a>Power BI destination

Angiv **aktiveret** til **Ja** at bruge konfigurationen ER for at arrangere overførslen af data fra din forekomst af Dynamics 365 for operationer til Microsoft Power BI-tjenester. De overførte filer er gemt på en Microsoft SharePoint Server-forekomst, der skal være konfigureret til dette formål. Yderligere oplysninger finder du i [giver strøm BI med data fra Dynamics 365 for operationer ved hjælp af en elektronisk rapportering konfiguration](general-electronic-reporting-report-configuration-get-data-powerbi.md). **Tip:** Hvis du vil tilsidesætte standardindstillingen (dvs dialogboksen for en konfiguration), kan du oprette en reference til destinationen og en fildestination for den vigtigste outputkomponent og derefter deaktivere alle destinationer.

## <a name="security-considerations"></a>Sikkerhedsovervejelser
To typer rettigheder og opgaver bruges til ER-destinationer. Én type kontrollerer muligheden for at opretholde de samlede destinationer, der er konfigureret for en juridisk enhed (det vil sige, den styrer adgangen til den **elektronisk indberetning destinationer** side). Den anden type styrer muligheden for at en programbruger på kørselstidspunktet kan tilsidesætte de destinationsindstillinger, der er konfigureret af en ER udvikler eller funktionel konsulent i elektronisk rapportering.

| Rolle (AOT-navn)                     | Navn på rolle                                  | Arbejdsopgave (AOT-navn)                     | Navn på arbejdsopgave                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Udvikler til elektronisk rapportering             | ERFormatDestinationConfigure        | Konfigurer destination for elektronisk rapportformat                |
| ERFunctionalConsultant              | Funktionel konsulent i elektronisk rapportering | ERFormatDestinationConfigure        | Konfigurer destination for elektronisk rapportformat                |
| PaymAccountsPayablePaymentsClerk    | Ansvarlig for kreditorbetalinger            | ERFormatDestinationRuntimeConfigure | Konfigurer destination for elektronisk rapportformat under kørsel |
| PaymAccountsReceivablePaymentsClerk | Ansvarlig for debitorbetalinger         | ERFormatDestinationRuntimeConfigure | Konfigurer destination for elektronisk rapportformat under kørsel |

**Bemærk:** To rettigheder bruges i de foregående opgaver. Disse rettigheder har de samme navne som de tilsvarende opgaver: **ERFormatDestinationConfigure** og **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Jeg har importeret elektroniske konfigurationer, og jeg kan se dem på siden Konfigurationer for elektronisk rapportering. Men Hvorfor kan jeg ikke se dem på siden elektronisk rapportering destinationer?

Sørg for, at du klikker på **ny** og derefter vælge en konfiguration i den **Reference** felt. På siden **Destinationer for elektronisk rapportering** kan du se kun de konfigurationer, som destinationer er konfigureret for.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Er der nogen måde at definere, hvilken konto Azure Storage og Azure Blob storage bruges?

Nr. Standard Azure Blob storage, der er defineret og anvendes til dokumentstyringssystemet bruges.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Hvad er formålet med destinationsfilen i indstillingerne for destination? Hvad gør denne indstilling?

**Fil**destinationen bruges til at styre en dialogboks. Hvis du aktiverer denne destination, eller hvis ingen destination, der er defineret for en konfiguration, kan du se en åben eller dialogboksen Gem, når du har oprettet en outputfil.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Kan du give et eksempel på den formel, der refererer til en kreditorkonto, som jeg kan sende mail til?

Formlen er specifik for ER-konfigurationen. Hvis du bruger konfigurationen ISO 20022 SEPA-kreditoverførsler, kan du f.eks bruge **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** eller **model. Payments.Creditor.Identification.SourceID** til at få en tilknyttet kreditorkonto.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>En af mine formatkonfigurationer indeholder flere filer, der er grupperet i én mappe (for eksempel Mappe1 indeholder, fil1 og fil2 og fil3). Hvordan konfigurerer jeg destinationer, så Mappe1.zip slet ikke oprettes, fil1 sendes via mail, fil2 sendes til SharePoint, og jeg kan åbne fil3 straks, når konfigurationen er udført?

Forudsætningen er, at formatet skal være tilgængelige i konfigurationerne, der ER. Hvis du har formatet, skal du åbne siden **Destination for elektronisk rapportering** og oprette en ny reference til denne konfiguration. Derefter skal du have fire fildestinationer, én for hver outputkomponent. Opret den første fildestination, giv den et navn som f.eks. **Mappe**, og vælg et filnavn, der repræsenterer en mappe i din konfiguration. Klik derefter på **Indstillinger**, og sørg for, at alle destinationer er deaktiveret. Mappen vil ikke blive oprettet for denne fildestination. Som standard fungerer filerne på samme måde på grund af hierarkisk afhængigheder mellem filerne og overordnede mapper. Med andre ord sendes de ikke et vilkårligt sted hen. Hvis du vil tilsidesætte denne standardfunktionsmåde, skal du oprette tre yderligere fildestinationer, én for hver fil. I destinationsindstillingerne for hver skal du aktivere den destination, som filen skal sendes til.

# <a name="see-also"></a>Se også

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)


