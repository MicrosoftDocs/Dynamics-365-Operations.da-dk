---
title: Generere FTI-formularer, der kan udskrives
description: Dette emne forklarer, hvordan du bruger strukturen i elektronisk rapportering (ER) til at generere fritekstfakturaformularer (FTI), der kan udskrives, som Microsoft Office-dokumenter.
author: NickSelin
ms.date: 07/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: be5e3ef0f6ecb3d8f911b5be5f8bc9102d201fd299425e847a2df233d9b4edf4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758210"
---
# <a name="generate-printable-fti-forms"></a>Generere FTI-formularer, der kan udskrives

[!include[banner](../includes/banner.md)]

Strukturen i elektronisk rapportering (ER) giver dig mulighed for at generere fritekstfakturaformularer (FTI), der kan udskrives, som Microsoft Office-dokumenter. Dette emne indeholder oplysninger om, hvordan du kan oprette dine egne konfigurationer samt oplysninger om tilgængelige konfigurationsskabeloner.

## <a name="overview"></a>Overblik

Ud over de eksisterende muligheder ved generering af FTI-formularer, der kan udskrives, ved hjælp af Microsoft SQL Server Reporting Services (SSRS), kan du nu bruge ER-strukturen. Du kan administrere FTI-formularer, der kan udskrives, i Microsoft Office Excel og Word. Du kan også ændre layoutet, dataflowet og formateringen for at imødekomme specifikke krav, uden at foretage ændringer i koden.

> [!NOTE]
> Hvis du vil starte med en oversigt over eksisterende ER-konfigurationer til denne prøve på løsningen til FTI-formularer, der kan udskrives, kan du gå direkte til afsnittet **Hent prøve på ER-konfigurationer til at generere FTI formularer, der kan udskrives** senere i dette emne.

## <a name="create-customized-configurations-for-fti-printable-forms"></a>Oprette tilpassede konfigurationer for FTI formularer, der kan udskrives
Som en del af din tilpassede løsning for FTI-formularer, der kan udskrives, skal du oprette et sæt af ER-konfigurationer.

### <a name="configure-the-er-data-model"></a>Konfigurere ER-datamodellen
Programmet skal indeholde den konfiguration af ER-datamodellen, der indeholder en datamodel, som beskriver forretningsdomænet for kundefakturering. Som et krav skal være navnet på datamodellen være **CustomersInvoicing**. Du kan finde oplysninger om, hvordan du designer ER-datamodeller i [Design en domænespecifik datamodel (ER)](tasks/er-design-domain-specific-data-model-2016-11.md).

### <a name="configure-the-er-model-mapping"></a>Konfigurere ER-datamodeltilknytningen
Programmet skal indeholde ER-modeltilknytningen til datamodellen CustomersInvoicing. Modeltilknytningen kan enten være i konfigurationen af ER-datamodellen eller i konfigurationen af ER-modeltilknytningen. Navnet på rodbeskrivelsen af modeltilknytningen skal dog være **FreeTextInvoice**.

Tilknytningen skal indeholde følgende datakilder:

- Datakildetype: **Tabelposter**

    - Denne datakilde skal navngives **CustInvoiceJour**.
    - Det skal referere til programtabellen CustInvoiceJour.
    - Den bruges under kørsel til at overføre fra programmet til ER-modellen for at tilknytte listen over fakturaer, der er valgt til udskrivning.

- Datakildetype: **Objekt**

    - Denne datakilde skal navngives **PrintMgmtPrintSettingDetail**.
    - Den skal referere til programklassen **PrintMgmtPrintSettingDetail**.
    - Den bruges under kørsel til at overføre fra programmet til ER-modeltilknytningsdetaljerne i indstillingerne for udskriftsstyring for det ER-format, der kører.

Du kan finde oplysninger om programintegration med ER-strukturen i klassen **ERPrintMgmtReportFormatSubscriber** (integrationsmodel for ER-programpakke) i kildekoden for programmet.

Du kan finde flere oplysninger om design af ER-modeltilknytninger i [Definer ER-modeltilknytninger, og vælg datakilder til dem](tasks/er-define-model-mapping-select-data-sources-2016-11.md).

### <a name="configure-the-er-format"></a>Konfigurere ER-formatet
I din forekomst af programmet, skal du have den ER-formatkonfiguration, der skal bruges til at generere FTI-formularer. 

> [!NOTE]
> Denne formatkonfiguration skal oprettes for datamodellen CustomersInvoicing, og den skal bruge den modeltilknytning, der har rodbeskrivelsen **FreeTextInvoice**.

Du kan finde oplysninger om konfiguration af ER-formater i [ER opret en formatkonfiguration (november 2016)](tasks/er-format-configuration-2016-11.md). Du kan finde oplysninger om, hvordan du opretter ER-formater til generering af rapporter i OpenXML-format, i [ER design en konfiguration til generering af rapporter i OPENXML-format (november 2016)](tasks/er-design-reports-openxml-2016-11.md).

## <a name="configure-print-management"></a>Konfigurer udskriftsstyring
Hvis du vil generere FTI-formularer ved hjælp af ER-strukturen, kan du tildele ER-formater på samme måde, som du tildeler SSRS-rapporter. Hvis du vil knytte ER-formatet til alle FTI'er for debitor, skal du gå til **Debitor** \> **Konfiguration** \> **Formularer** \> **Formularopsætning** \> **Generelt** \> **Udskriftsstyring** \> **Fritekstfaktura** \> **Oprindelig**. Hvisl du vil knytte ER-formatet til en bestemt debitor eller faktura, skal du følge disse trin.

1. Gå til **Debitor** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. Vælg den FTI, der skal knyttes til ER-formatet, og åbn siden **Opsætning af udskriftsstyring**.
3. Vælg dokumentniveauet for at angive omfanget af fakturaer til behandling.
4. Vælg ER-formatet for det angivne dokumentniveau.

![Opsætning af udskriftsstyring.](media/FTIbyGER-PMSetting.png)

> [!NOTE]
> Kun ER-formater, der bruger rodbeskrivelsen **FreeTextInvoice** fra datamodellen **CustomersInvoicing** vises i feltet **Opslag af rapportformat** for det valgte format.

## <a name="generate-fti-forms"></a>Generere FTI-formularer
FTI-formularer genereres inden for ER-strukturen på samme måde, som SSRS-rapporter genereres.

Du kan vælge fakturaer for at generere FTI-formularer, efter område eller efter markering. 

![Fakturavalg.](media/FTIbyGER-InvoiceSelection.png)

![Forhåndsvisning af faktura.](media/FTIbyGER-InvoiceExcelPreview.png)

Når du bruger ER-formater til at udskrive FTI-formularer på denne måde, bruges standarddestinationerne for ER-filen. Du kan ikke ændre denne destination. Du kan finde oplysninger om konfiguration af ER-destinationer til ER-formater i [Destinationer for elektronisk rapportering (ER)](electronic-reporting-destinations.md).

Du kan også generere FTI-formularer, når du bogfører en FTI, ved at aktivere **Udskriv faktura** og deaktivere **Brug destinationer for udskriftsstyring**.

> [!NOTE]
> Når du bruger ER-formater til at udskrive FTI-formularer på denne måde, bruges standarddestinationerne for ER-filen. Du kan ændre standarddestinationen under kørslen, hvis destinationen allerede er konfigureret. Hvis du vil ændre destinationen, skal du have følgende sikkerhedsrettighed:
>
> - **Navn:** ERFormatDestinationRuntimeMaintain
> - **Label:** Vedligehold destination for elektronisk rapportformat under kørsel

![Destination for elektronisk rapportering.](media/FTIbyGER-ERFileDestinationSetting.png)

![Destination for elektronisk rapportformat.](media/FTIbyGER-ERFileDestinationUsage.png)

ER-strukturen understøtter i øjeblikket følgende destinationer for oprettede dokumenter:

- **Hentet fil** – Genererede formularer tilbydes som overførsler, du kan gemme ved hjælp af webbrowseren.
- **Skærm** – Microsoft 365 Excel bruges til at få vist oprettede FTI-formularer i Excel-format.
- **SharePoint-mappe** – Genererede formularer gemmes baseret på indstillingerne for strukturen for dokumentstyring.
- **Programarkiv** – Genererede formularer gemmes som vedhæftede filer i kørselslogposter i Microsoft Azure Storage.
- **Mail** – Genererede formularer sendes som vedhæftede filer.

> [!NOTE]
> Du kan ikke sende de FTI-formularer, der genereres, direkte til printeren, da direkte udskrivning, der bruger Dynamics Printer Routing-agenten, ikke understøttes i øjeblikket.

## <a name="download-sample-er-configurations-to-generate-printable-fti-forms"></a>Hent ER-eksempelkonfigurationer for at generere FTI-formularer, der kan udskrives
Du kan hente ER-eksempelkonfigurationer, der kan bruges som skabelon for FTI-løsningen. Konfigurationerne lagres i biblioteket Delte aktiv i Microsoft Dynamics Lifecycle Services (LCS). Konfigurationerne omfatter:

- Konfigurationen **Kundefaktureringsmodel** indeholder den nødvendige datamodel og modeltilknytning.
- Konfigurationen **Kunde FTI-rapport (TYSK)** indeholder eksempelformatet.

> [!NOTE]
> Disse konfigurationer er oprettet som eksempler for at tydeliggøre mulige scenarier. Fremtiden for disse konfigurationer afhænger af resultaterne af denne evaluering og eventuelle tilbagemeldinger, der er modtages.

### <a name="features-that-are-implemented-in-the-sample-er-format"></a>Funktioner, der er implementeret i ER-eksempelformatet
I konfigurationen til ER-eksempelformatet bruges en Excel-fil som en skabelon til at generere FTI-formularer.

![Formatdesigner.](media/FTIbyGER-ERFormat.png)

I øjeblikket understøtter dette ER-eksempelformat følgende funktioner til at generere FTI-formularer:

- FTI-formularer genereres både for oprindelige fakturaer, der er bogført, og oprindelige fakturaer, der endnu ikke er blevet bogført. Rettede fakturaer og kreditnotaer understøttes ikke.
- FTI-formularer genereres på sproget til fakturaen. Formatet for værdier og datoer i de genererede formularer er baseret på indstillingerne for landestandard for brugerens klient.
- Genererede fakturaer viser meddelelser om datautilgængelighed, hvis der ikke er nogen linjer i de fakturaer, der behandles.
- Genererede fakturahoveder er baseret på papirformatet, der er valgt for FTI-formularen på siden **Debitorparametre**. Oplysninger om en virksomhed vises kun i overskriften af den genererede fakturaformular, hvis papirformatet er tomt.
- Genererede fakturaformularer viser virksomhedens og kundens se-numre, når de relevante indstillingen er valgt for FTI formularen på siden **Debitorparametre**.
- De genererede sektioner for fakturalinjer og fakturatotaler viser standardfakturaens monetære detaljer i fakturaens registreringsvaluta.
- Sektionen for genererede fakturatotaler kan vise monetære detaljer i valutaen euro og i fakturaens registreringsvaluta, når indstillingen **Udskriv beløb i valuta, der repræsenterer euroen** er aktiveret på siden **Debitorparametre**.
- De genererede fakturaformularer viser eventuelle fakturabemærkninger fra processen baseret på indstillingerne på siden **Debitorparametre**. Bemærkninger medtages både for hele fakturaen og hver fakturalinje.
- De genererede fakturaformularer indeholder bemærkninger til FTI-kundeformularen og behandlingsfakturasproget, når de er konfigureret på listen AR-formularbemærkninger.
- Afhængigt af indstillingerne for udskriftsstyring, kan de genererede fakturaer indeholde brugerdefineret sidefodstekst, når den er blevet konfigureret for fakturasproget, ER-formatet og FTI-dokumentområdet.
- Afsnittet med totaler for genererede fakturaformularer indeholder alle oplysninger om kasserabat, der er tilgængelige.
- Afsnittet betalingsplan for de genererede fakturaformularer indeholder alle oplysninger om betalingsplanen, der er tilgængelige.
- Afsnittet markup for de generede fakturaformularer indeholder alle gebyrtransaktioner, der er tilgængelige.
- De genererede fakturaformularer indeholder oplysninger om moms, baseret på indstillingen **Momsspecifikation** på siden **Debitorparametre**. Dette afsnit kan vise momsoplysninger enten kun i fakturaens registreringsvaluta, eller i fakturaens registreringsvaluta og firmaets regnskabsvaluta firma på samme tid.
- Genererede fakturaformularer viser oplysninger om direkte debiteringsbesked. De viser f.eks., når betalingsmåden, der har det obligatoriske id for bemyndigelse til direkte debitering, er valgt for fakturaen, når fakturabehandlingen er registreret i valutaen euro, og når id'et for bemyndigelse til direkte debitering er defineret for fakturaen.
- Genererede fakturaer viser alle oplysninger om forudbetaling, der er tilgængelige for bogførte fakturaer.
- Genererede fakturaformularer kan sendes til en fakturakunde som vedhæftet fil i en mail. Den korrekte ER-fildestination skal konfigureres til det ER-format, der bruges.

### <a name="countryregion-specific-features"></a>Funktioner, der er land/område-specifikke 
De følgende land/område-specifikke funktioner findes i ER-eksempelformatet for at vise, hvordan bestemte krav kan håndteres i ER-konfigurationer.

#### <a name="norway"></a>Norge
Termen Virksomhedsregister udskrives i overskriften på den genererede fakturaformular, når fakturaen behandles for en juridisk enhed, der er konfigureret på følgende måde:

- Land/område-konteksten for Norge bruges.
- Parameteren **Udskriv Foretaksregisteret** er aktiv på salgsdokumenter.

#### <a name="spain"></a>Spanien
Termen **Særlig ordning for kontantregnskabsmetode** udskrives i overskriften på den genererede fakturaformular, når fakturaen behandles for en juridisk enhed, der er konfigureret på følgende måde:

- Land/område-konteksten for Spanien bruges.
- Den særlige ordning for kontantregnskabsmetoden er aktiveret på datoen for fakturabehandlingen.

Når oplysningerne om kasserabat, f.eks. kasserabatbeløbet og nettobeløb for fakturalinje, er tilgængelige, præsenteres de i sektionen fakturatotaler i den genererede fakturaformular, når den behandles for en juridisk enhed, der er konfigureret på følgende måde:

- Land/område-konteksten for Spanien bruges.
- **Der anvendes kasserabat på fakturaen** er aktiveret i faktureringsindstillingen (**Økonomiparametre** \> **Afsnittet Moms**).

#### <a name="italy"></a>Italien
Mærket for varerabat medtages på fakturalinjerne for den genererede faktura, når den behandles for en juridisk enhed, der er konfigureret ved hjælp af land/område-konteksten for Italien.

#### <a name="finland"></a>Finland
Ud over den genererede fakturaformular kan giroindbetalingskort genereres på følgende måde:

- For den juridiske enhed, der bruger land/område-konteksten for Finland, og som har mindst én bankkonto, der er markeret som **Girokonto** og **Bankstregkode**. 
- For en faktura, der er markeret som krævet til det tilknyttede **Finske** betalingsbilag.

![Girokort.](media/FTIbyGER-GiroSlip.PNG)

> [!NOTE]
> ER-eksempelformatet er konfigureret til valgfrit at generere giroindbetalingskortet i det separate regneark.

> [!NOTE]
> Du skal først installere den skrifttype, der bruges til at generere stregkoden på den lokale computer, hvor den genererede fakturaformular i Excel-format vises.

### <a name="use-the-sample-er-format-to-configure-email-destinations"></a>Brug ER-eksempelformatet til at konfigurere maildestinationer
Brug følgende elementer af ER-eksempelformatet til at konfigurere maildestinationer:

- Du kan få adgang til mailadressen til en kundekontakt via følgende ER-udtryk: **model.InvoiceBase.Contact.ElectronicMail**.
- Du kan få adgang til emneteksten til mail via følgende ER-udtryk: **Emailing.TxtToUse.Subject**.
- Du kan få adgang til brødteksten til mail via følgende ER-udtryk: **Emailing.TxtToUse.Body**.

![Indstillinger for destination.](media/FTIbyGER-ERFileDestinationSettingEmail.png)

Standardteksten for mailens emne- og brødtekst er defineret i ER-eksempelformatet. Sproget afhænger af formatets etiketter. Denne standardtekst bruges til mails, hvis der ikke er tilføjet en brugerdefineret organisationsmailskabelon, der har det foruddefinerede id **ERFTITMP**.

> [!NOTE]
> Mailskabelon-id'et **ERFTITMP** er defineret i ER-eksempelformatet. Den kan ændres efter behov i et nyt ER-format, der oprettes fra dette eksempelformat.

Hvis den organisationsmailskabelon, der har det foruddefinerede id **ERFTITMP**, er blevet føjet til den juridiske enhed, som du behandler fakturaen for, bruges skabelonen til mailemnet og -brødteksten til at generere mailen. 

![Skabelon til organisationsmail.](media/FTIbyGER-EmailTemplate.png)

![Overfør mailskabelon.](media/FTIbyGER-EmailTemplateBody.png)

ER-udtrykket **Emailing.TxtToUse.Subject** i ER-eksempelformatet er konfigureret til at erstatte alle forekomster af pladsholderen %1 i det behandlede faktura-id.

Udtrykket **Emailing.TxtToUse.Body** i eksempelformatet er konfigureret til de følgende erstatninger for pladsholdere:

- "%1" erstattes med navnet på debitorens kontaktperson.
- "%2" erstattes med firmanavnet.
- "%3" erstattes med kundenavnet.
- "%4" erstattes med navnet på firmaets kontaktperson.
- "%5" erstattes med stillingsbetegnelse for firmaets kontaktperson.
- "%6" erstattes med mailadressen på firmaets kontaktperson.

![Email.](media/FTIbyGER-Email.PNG)

## <a name="additional-resources"></a>Yderligere ressourcer
[Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]