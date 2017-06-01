---
title: Destinationer for elektronisk rapportering
description: "Du kan konfigurere en destination til hver formatkonfiguration for elektronisk rapportering (ER) og dens outputkomponent (en mappe eller en fil). Brugere, der er tildelt passende adgangsrettigheder, kan også ændre indstillingerne for destinationen på kørselstidspunktet. I denne artikel forklares ER-destinationsstyring, destinationstyperne, der understøttes, og sikkerhedsmæssige overvejelser."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5fb008420f82abd7983ee26854f84330705c0c01
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="electronic-reporting-destinations"></a>Destinationer for elektronisk rapportering

[!include[banner](../includes/banner.md)]


Du kan konfigurere en destination til hver formatkonfiguration for elektronisk rapportering (ER) og dens outputkomponent (en mappe eller en fil). Brugere, der er tildelt passende adgangsrettigheder, kan også ændre indstillingerne for destinationen på kørselstidspunktet. I denne artikel forklares ER-destinationsstyring, destinationstyperne, der understøttes, og sikkerhedsmæssige overvejelser.

Konfigurationer af formater for elektronisk rapportering (ER) består normalt af mindst én output-komponent: en fil. Normalt indeholder konfigurationer flere filoutputkomponenter af forskellige typer (for eksempel XML, TXT eller XLSX), der er grupperet i enten en enkelt mappe eller flere mapper. Med styring af ER-destination kan du forudkonfigurere, hvad sker der, når hver komponent køres. Når en konfiguration køres, åbnes som standard en dialogboks, hvor brugeren kan gemme eller åbne filen. Samme funktionsmåde bruges også, når du importerer en ER-konfiguration og ikke konfigurerer særlige destinationer for den. Når der oprettes en destination for en vigtig outputkomponent, tilsidesætter denne destination standardindstillingen, og mappen eller filen sendes på grundlag af destinationens indstillinger.

## <a name="availability-and-general-prerequisites"></a>Tilgængelighed og generelle forudsætninger
Funktionerne for ER-destinationer findes ikke i Microsoft Dynamics 365 for Operations 7.0-frigivelsen (februar 2016). Derfor skal du installere Microsoft Dynamics 365 for Operations (november 2016 versionen) for at kunne bruge alle de funktioner, der er beskrevet i dette emne. Du kan også vælge at installere en af følgende forudsætninger. Du skal dog være opmærksom på, at disse alternativer giver en mere begrænset ER destinationsoplevelse.

-   Microsoft Dynamics 365 for Operations-programversion 7.0.1 (maj 2016)
-   ER destinationsstyring [programhotfix](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Du kan konfigurere destinationer kun for ER-konfigurationer, der er importeret, og for de formater, der er tilgængelige på siden **Konfigurationer for elektronisk rapportering**.

## <a name="overview"></a>Overblik
Funktionen ER-destinationsstyring er tilgængelig på **Virksomhedsadministration** &gt; **Elektronisk rapportering**. Her kan du tilsidesætte standardindstillingen for en konfiguration. Importerede konfigurationer vises først her, når du klikker på **Ny** og derefter i feltet **Reference** vælger en konfiguration at oprette destinationsindstillinger for.

[![Vælge en konfiguration i feltet Reference](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Når du har oprettet en reference, kan du oprette en fildestination for hver mappe eller for en fil. 

[![Oprettelse af en fildestination](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

**Bemærk:** Du kan oprette én fildestination for hver outputkomponent af samme format som f.eks. en mappe eller en fil, der er markeret i feltet **Filnavn**. Du kan derefter aktivere og deaktivere individuelle destinationer for fildestinationen i dialogboksen **Indstillinger for destination**. Knappen **Indstillinger** bruges til at styre alle destinationer for en valgt fildestination. I dialogboksen **Indstillinger for destination** kan du styre hver destination separat ved at vælge indstillingen **Aktiveret** for destinationen.

[![Dialogboksen Indstillinger for destination](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Destinationstyper
Forskellige typer destinationer understøttes. Du kan deaktivere eller aktivere alle typer på samme tid. På denne måde kan du enten gøre ingenting eller sende komponenten til alle konfigurerede destinationer. I følgende afsnit beskrives de destinationer, der understøttes.

### <a name="email-destination"></a>Maildestination

Indstil **Aktiveret**til **Ja** for at sende en outputfil via mail. Når denne indstilling er aktiveret, kan du angive e-mailmodtagere og redigere e-mailens emne og brødtekst. Du kan konfigurere konstanttekster til e-mailens emne og brødtekst, eller du kan bruge ER formler til dynamisk at oprette e-mailtekster. Du kan konfigurere e-mailadresser for ER på to måder. Konfigurationen kan udføres på samme måde, som funktionen Udskriftsstyring i Dynamics 365 for Operations udfører den. Du kan også oversætte en e-mailadresse ved hjælp af en direkte reference til ER-konfigurationen via en formel.

### <a name="email-address-types"></a>E-mailadressetyper

Når du klikker på **Rediger** for feltet **til** eller **Cc**, åbnes dialogboksen **Mail til**. Du kan derefter vælge type e-mailadresse, du vil bruge.

[![Mail til-dialogboks](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Udskriftsstyring

Hvis du vælger typen **Mail for udskriftsstyring**, kan du angive fast e-mailadresser i feltet **Til**. Hvis du vil bruge mailadresser, der ikke er faste, skal du vælge mailkildetypen for en fildestination. Følgende værdier understøttes: **Kunde**, **Leverandør**, **Kundeemne**, **Kontakt**, **Konkurrent**, **Arbejder**, **Ansøger**, **Mulig kreditor** og **Ikke-godkendt kreditor**. Når du har valgt en kildetype for e-mailen, skal du bruge knappen ud for feltet **Kildekonto for mail** til at åbne formularen **Formeldesigner**. Du kan bruge denne formular til at knytte en formel, der repræsenterer den valgte partskonto, til e-maildestinationen.

[![Konfigurere e-mailtypen udskriftsstyring](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Bemærk, at formler er specifikke for ER-konfigurationen. Angiv en dokumentspecifik reference til en debitor- eller kreditorparttype i feltet **Formel**. I stedet for at skrive kan du finde datakildenoden, der repræsenterer debitor- eller kreditorkontoen, og derefter klikke på **Tilføj** datakilde for at opdatere formlen. Hvis du bruger konfigurationen ISO 20022 SEPA-kreditoverførsel, er den node, der repræsenterer en kreditorkonto, **'$PaymentsForCoveringLetter'. Creditor.Identification.SourceID**. Ellers skal du indtaste en strengværdi som f.eks. **DE-001** for at gemme en formel.

[![Formeldesigner](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

I dialogboksen **Mail til** skal du klikke på papirkurven ud for den **Kildekonto for mail** for at slette formlen for e-mailens kildekonto. Du kan også åbne formeldesigneren for at ændre en formel, der blev gemt tidligere. Hvis du vil tildele e-mailadresser, skal du klikke på **Rediger** for at åbne dialogboksen **Tildel e-mailadresser**.

[![Tildele mailadresser til en maildestination](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Konfigurationsmail

Brug denne e-mailtype, hvis den konfiguration, du bruger, har en node i datakilderne, der repræsenterer en e-mailadresse. Du kan bruge datakilder og funktioner i formeldesigneren til at få en korrekt formateret e-mailadresse.

[![Tildeling af en mailadresses datakilde til en maildestination](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Bemærk:** En SMTP-server (Simple Mail Transfer Protocol) skal konfigureres og være tilgængelig. Du kan angive din SMTP-server i Dynamics 365 for Operations i **Systemadministration** &gt; **Konfiguration** &gt; **Mail** &gt; **E-mail-parametre**.

### <a name="archive-destination"></a>Arkivdestination

Du kan bruge denne indstilling til at sende output til en Microsoft SharePoint-mappe eller Microsoft Azure Storage. Indstil **Aktiveret** til **Ja**for at sende output til en destination, der er defineret af den valgte dokumenttype. Kun dokumenttyper, hvor gruppen er indstillet til **Fil**, kan vælges. Du definerer dokumenttyper i **Virksomhedsadministration** &gt; **Dokumentstyring** &gt; **Dokumenttyper**. Konfigurationen for ER-destinationer svarer til konfigurationen for dokumentstyringssystemet.

[![Siden Dokumenttyper](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

Lokaliteten bestemmer, hvor filen gemmes. Når destinationen **Arkiv** er aktiveret, kan resultaterne af konfigurationskørslen gemmes i jobarkivet. Du kan få vist resultaterne i **Virksomhedsadministration** &gt; **elektronisk rapportering** &gt; **Elektronisk rapportering af arkiverede job**. **Bemærk!** Du kan vælge en dokumenttype til jobarkivet i Dynamics 365 for Operations i **Virksomhedsadministration** &gt; **Arbejdsområder** &gt; **Elektronisk rapportering** &gt; **Parametre til elektronisk rapportering**.

#### <a name="sharepoint"></a>SharePoint

Du kan gemme en fil i en angivet SharePoint-mappe. Du kan definere standard-SharePoint-serveren i **Virksomhedsadministration** &gt; **Dokumentstyring** &gt; **Dokumentstyringsparametre** under fanen **SharePoint**. Når SharePoint-mappen er konfigureret, kan du vælge den som den mappe, hvor ER outputtet vil blive gemt for dokumenttypen. 

[![Valg af en SharePoint-mappe](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azure Storage

Når dokumenttype placeringen er indstillet til **Arkivbibliotek**, kan du gemme en fil på Azure Storage.

### <a name="file-destination"></a>Fildestination

Hvis du indstiller **Aktiveret** til **Ja**, åbnes dialogboksen Åbn eller dialogboksen Gem, når konfigurationen er afsluttet.

### <a name="screen-destination"></a>Skærmdestination

Hvis du indstiller **Aktiveret** til **Ja**, oprettes der et eksempel på outputtet. Du kan få vist nogle filtyper som f.eks. XML, TXT eller PDF direkte i et browservindue. For andre filtyper, f.eks. Microsoft Excel eller Word, bruges tjenesten Microsoft Office Online.

### <a name="power-bi-destination"></a>Power BI-destination

Indstil **Aktiveret** til **Ja** for at bruge din ER-konfiguration til at arrangere overførslen af data fra din forekomst af Microsoft Dynamics 365 for Operations til Power BI-tjenester. De overførte filer gemmes på en forekomst af Microsoft SharePoint Server, der skal konfigureres til dette formål. Du kan finde flere oplysninger under [Brug en konfiguration af elektronisk rapportering til at give Power BI data fra Dynamics 365 for Operations](general-electronic-reporting-report-configuration-get-data-powerbi.md). **Tip:** Hvis du vil tilsidesætte standardindstillingen (dvs dialogboksen for en konfiguration), kan du oprette en reference til destinationen og en fildestination for den vigtigste outputkomponent og derefter deaktivere alle destinationer.

## <a name="security-considerations"></a>Sikkerhedsovervejelser
To typer rettigheder og opgaver bruges til ER-destinationer. Én type styrer muligheden for at opretholde de samlede destinationer, der er konfigureret for en juridisk enhed (dvs. den styrer adgang til siden **Destinationer for elektronisk rapportering**). Den anden type styrer muligheden for at en programbruger på kørselstidspunktet kan tilsidesætte de destinationsindstillinger, der er konfigureret af en ER udvikler eller funktionel konsulent i elektronisk rapportering.

| Rolle (AOT-navn)                     | Navn på rolle                                  | Arbejdsopgave (AOT-navn)                     | Navn på arbejdsopgave                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Udvikler til elektronisk rapportering             | ERFormatDestinationConfigure        | Konfigurer destination for elektronisk rapportformat                |
| ERFunctionalConsultant              | Funktionel konsulent i elektronisk rapportering | ERFormatDestinationConfigure        | Konfigurer destination for elektronisk rapportformat                |
| PaymAccountsPayablePaymentsClerk    | Ansvarlig for kreditorbetalinger            | ERFormatDestinationRuntimeConfigure | Konfigurer destination for elektronisk rapportformat under kørsel |
| PaymAccountsReceivablePaymentsClerk | Ansvarlig for debitorbetalinger         | ERFormatDestinationRuntimeConfigure | Konfigurer destination for elektronisk rapportformat under kørsel |

**Bemærk:** To rettigheder bruges i de foregående opgaver. Disse rettigheder har de samme navne som de tilsvarende opgaver: **ERFormatDestinationConfigure** og **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Jeg har importeret elektroniske konfigurationer, og jeg kan se dem på siden Konfigurationer for elektronisk rapportering. Men hvorfor kan jeg ikke se dem på siden Destinationer for elektronisk rapportering?

Sørg for at klikke på **Ny** og derefter vælge en konfiguration i feltet **Reference**. På siden **Destinationer for elektronisk rapportering** kan du se kun de konfigurationer, som destinationer er konfigureret for.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Er der nogen måde at definere, hvilken Azure Storage-konto og Azure Blob-lager der skal bruges?

Nej. Standard Azure Blob-lageret, der er defineret og anvendes til dokumentstyringssystemet, bruges.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Hvad er formålet med fildestinationen i indstillingerne for destinationen? Hvad gør denne indstilling?

**Fil**destinationen bruges til at styre en dialogboks. Hvis du aktiverer denne destination, eller hvis ingen destination er defineret for en konfiguration, vises en Gem- eller Åbn-dialogboks, når der oprettes en outputfil.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Kan du give et eksempel på den formel, der refererer til en kreditorkonto, som jeg kan sende mail til?

Formlen er specifik for ER-konfigurationen. Hvis du bruger konfigurationen ISO 20022 SEPA-kreditoverførsler, kan du f.eks bruge **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** eller **model. Payments.Creditor.Identification.SourceID** til at få en tilknyttet kreditorkonto.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>En af mine formatkonfigurationer indeholder flere filer, der er grupperet i én mappe (for eksempel Mappe1 indeholder, fil1 og fil2 og fil3). Hvordan konfigurerer jeg destinationer, så Mappe1.zip slet ikke oprettes, fil1 sendes via mail, fil2 sendes til SharePoint, og jeg kan åbne fil3 straks, når konfigurationen er udført?

Forudsætningen er, at formatet skal være tilgængeligt i ER-konfigurationerne. Hvis du har formatet, skal du åbne siden **Destination for elektronisk rapportering** og oprette en ny reference til denne konfiguration. Derefter skal du have fire fildestinationer, én for hver outputkomponent. Opret den første fildestination, giv den et navn som f.eks. **Mappe**, og vælg et filnavn, der repræsenterer en mappe i din konfiguration. Klik derefter på **Indstillinger**, og sørg for, at alle destinationer er deaktiveret. Mappen vil ikke blive oprettet for denne fildestination. Som standard fungerer filerne på samme måde på grund af hierarkisk afhængigheder mellem filerne og overordnede mapper. Med andre ord sendes de ikke et vilkårligt sted hen. Hvis du vil tilsidesætte denne standardfunktionsmåde, skal du oprette tre yderligere fildestinationer, én for hver fil. I destinationsindstillingerne for hver skal du aktivere den destination, som filen skal sendes til.

# <a name="see-also"></a>Se også

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)




