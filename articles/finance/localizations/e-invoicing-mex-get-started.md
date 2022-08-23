---
title: Start her med elektronisk fakturering for Mexico
description: Denne artikel indeholder oplysninger, der hjælper dig med at komme i gang med elektronisk fakturering for Mexico.
author: gionoder
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 46dfa03a3c90eea2d732f355396d148f475429d7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283110"
---
# <a name="get-started-with-electronic-invoicing-for-mexico"></a>Start her med elektronisk fakturering for Mexico

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Elektronisk fakturering for Mexico understøtter i øjeblikket muligvis ikke alle de funktioner, der er tilgængelige i CFDI-dokumentet (Comprobante Fiscal Digital por Internet) og i den relaterede integrering i Microsoft Dynamics 365 Finance eller Dynamics 365 Supply Chain Management.

Denne artikel indeholder oplysninger, der hjælper dig med at komme i gang med elektronisk fakturering for Mexico. Det fører dig gennem de konfigurationstrin, der er landeafhængige i Regulatory Configuration Services (RCS) og i Finance. Det fører også dig gennem de trin, du skal følge i Finance for at sende CFDI-fakturaer via tjenesten, og det forklarer, hvordan du kan gennemse behandlingsresultaterne og statussen for CFDI-fakturaer.

## <a name="prerequisites"></a>Forudsætninger

Før du udfører trinene i denne artikel, skal du udføre trinnene i [Start her med serviceadministration i elektronisk fakturering](e-invoicing-get-started-service-administration.md) og [Start her med elektronisk fakturering](e-invoicing-get-started.md).

## <a name="set-up-the-cadena-xslt"></a>Konfigurere Cadena XSLT

Hvis du vil føje Cadena XSLT-skemaet til globaliseringsfunktionen til CFDI-behandling, skal du gennemføre følgende trin.

1. Hent skema fra [SAT-webstedet](http://www.sat.gob.mx/sitio_internet/cfd/3/cadenaoriginal_3_3/cadenaoriginal_3_3.xslt).
2. Komprimer skemaet til en zip-fil.
3. Gem xslt-filen på den Azure Storage-konto, der er konfigureret i servicemiljøet for den nye container.

## <a name="rcs-setup"></a>RCS-opsætning

Under RCS-opsætningen skal du udføre disse opgaver:

1. Importér e-faktureringsfunktionen til behandling af CFDI-fakturaer.
2. Gennemse de formatkonfigurationer, der skal bruges til at oprette, sende og modtage svar om CFDI-fakturaer og til at sende og modtage svar om annullering.
3. Konfigurer de hændelser, der understøtter scenarierne for CFDI-fakturaindsendelse.
4. Publicer e-faktureringsfunktionen for CFDI-fakturaer.

> [!NOTE]
> "E-faktureringsfunktionen" er det generiske navn på den ressource, der er konfigureret og publiceret til at bruge serveren for elektronisk fakturering. I dette tilfælde er CFDI-fakturaer (MX) den e-faktureringsfunktion, du skal konfigurere.

## <a name="import-the-e-invoicing-feature"></a>Importere e-faktureringsfunktionen

1. Log på din RCS-konto.
2. I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **e-fakturering**.
3. På siden med **e-faktureringsfunktioner** skal du vælge **Importér** for at importere funktionen **CFDI-fakturaer (MX)** fra det globale lager.

    > [!NOTE]
    > Hvis du ikke kan se funktionen på listen, skal du vælge **Synkroniser** og derefter gentage trin 3.

![Importere funktionen CFDI-fakturaer (MX).](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

Når du importerer funktionen **CFDI-fakturaer (MX)** fra det globale lager, importeres alle funktionsindstillinger, herunder konfigurationer og handlinger, også.

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a>Oprette en ny version af funktionen MX (CFDI fakturaer)

Du kan oprette en ny version, hvis f.eks. URL-adresser skal opdateres. Du kan finde flere oplysninger i [CFDI for e-fakturering](tasks/mx-00010-e-invoicing-cfdi.md).

- På siden med **e-faktureringsfunktioner** på fanen **Versioner** skal du vælge **Ny**.

![Tilføje en ny version af e-faktureringsfunktionen.](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a>Opdatere konfigurationsversionen

1. På siden med **e-faktureringsfunktioner** under **Konfigurationer** skal du vælge **Tilføj** eller **Slet** for at administrere konfigurationsversionerne (filkonfigurationer for ER-format).

    ![Administrere konfigurationer for e-faktureringsfunktion.](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    Når du opretter en ny version, nedarves alle konfigurationer fra den senest publicerede version. Der kræves følgende konfigurationer for at behandle CFDI-fakturaer:

    - CFDI-faktura (BusinessDocumentService)
    - Import af CFDI-svarmeddelelse
    - Import af CFDI-fejllog
    - Anmodning om CFDI-annullering (MX) (BusinessDocumentService)
    - CFDI-faktura (BusinessDocumentService)

2. Vælg en konfigurationsversion på listen, og vælg derefter **Rediger** eller **Vis** for at åbne siden **Formatdesigner**, hvor du kan redigere eller få vist konfigurationen.

    ![Åbne siden Formatdesigner.](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. Du kan bruge siden **Formatdesigner** til at redigere og få vist filkonfigurationer for ER-formatet. Du kan finde flere oplysninger i [Oprette konfigurationer for elektroniske dokumenter](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md).

    ![Siden Formatdesigner.](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>Administrere funktionsopsætninger for e-fakturering

- På siden med **e-faktureringsfunktioner** på fanen **Konfigurationer** skal du vælge **Tilføj**, **Slet** eller **Rediger** for at administrere funktionsopsætningerne for e-fakturering.

![Administrere funktionsopsætninger for e-fakturering.](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

Hvis du vil sende CFDI-fakturaer til autorisation (oprette XML-filen, sende XML-filen og behandle svaret), kræves funktionsopsætningen for **Salgsfaktura**.

Hvis du vil sende en CFDI-fakturaannullering, kræves der funktionsopsætninger for **Annullering** og **Annuller**.

### <a name="configure-the-sales-invoice-feature-setup"></a>Konfigurere funktionsopsætningen for Salgsfaktura

1. Vælg **Salgsfaktura** i kolonnen **Funktionsopsætning** på fanen **Konfigurationer** på siden med **e-faktureringsfunktioner**.
2. Vælg **Rediger** for at konfigurere handlinger, anvendelighedsregler og variabler.

    ![Redigere funktionsopsætningen for e-fakturering.](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. På siden **Opsætning af funktionsversion** skal du vælge fanen **Handlinger** for at administrere listen over handlinger. Handlinger definerer en liste over handlinger, der skal køres i rækkefølge for at opnå fuld udførelse af hændelsen.

    ![Fanen Handlinger.](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | Handlings-id | Handling                   | Handlingsnavn                                  | Handlingsbeskrivelse                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | 1         | Transformér dokument       | Oprette CFDI-e-faktura uden digital underskrift | Opret CFDI-e-fakturaen.                                |
    | 2         | Underskriv dokument            | Underskrive digital                                 | Underskriv e-fakturaen digitalt til indsendelse.                |
    | 3         | Kalde mexicansk PAC-tjeneste | Sende CFDI-e-faktura                        | WCF-klienten (Windows Communication Foundation) sender CFDI-e-fakturaen. |
    | 4         | Behandle svar         | Analysere svar fra webtjeneste                 | Analysér svaret fra webtjenesten, og returner fejlloggen. |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a>Konfigurere URL-adressen til mexicanske PAC-webtjenester 

1. På siden **Opsætning af funktionsversion** på fanen **Handlinger** på oversigtspanelet **Handlinger** skal du vælge **Kald mexicansk PAC-tjeneste**.
2. På oversigtspanelet **Parametre** i feltet **URL-adresse** skal du angive URL-adressen til webtjenesten til CFDI-fakturaindsendelse.

> [!NOTE]
> Brug samme fremgangsmåde for at opdatere URL-adressen til handlingen **Kald mexicansk PAC-tjeneste** for funktionsopsætningerne for **Annuller** og **Anmodning om annullering**.

### <a name="set-up-the-path-for-the-cadena-xlst-schema"></a>Konfigurere stien til Cadena XLST-skemaet

1. På siden **Opsætning af funktionsversion** skal du under fanen **Variabler** vælge variabelnavnet **DigitalSignatureXSLT**.
2. I feltet **Værdier** skal du angive: {"containerUrl":"https://&lt;AccountStorageName&gt;.blob.core.windows.net/&lt;ContainerName&gt;","path":"&lt;RelativePath&gt;"}
   
    hvor: \<RelativePath\> = mappe\\mappe\\filnavn med dobbelte skråstreger, ContainerName skal angive den container, der bruges til tjenesten.
   
    Variablen kan f.eks. være:
    
    {"path":"xxxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx\\dev\\cadena_xslt","containerUrl":https://yyyyyyyyyy.blob.core.windows.net/containername}

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a>Tildele kladdeversionen til et e-faktureringsmiljø

1. På siden med **e-faktureringsfunktioner** på fanen **Miljøer** skal du vælge **Aktivér**.
2. Vælg miljøet i feltet **Miljø**.
3. I feltet **Gyldig fra** skal du vælge den dato, hvor miljøet skal være gyldigt.
3. Vælg **Aktivér**.

![Aktivere et e-faktureringsmiljø.](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a>Skifte versionsstatus til Fuldført

1. På siden med **e-faktureringsfunktioner** på fanen **Versioner** skal du vælge den e-faktureringsfunktion, der har statussen **Kladde**.
2. Vælg **Skift status \> Fuldfør**.

## <a name="change-the-version-status-to-published"></a>Skifte versionsstatus til Publiceret

- På siden med **e-faktureringsfunktioner** på fanen **Versioner** skal du vælge **Skift status \> Publicer**.

## <a name="publish-the-e-invoicing-feature"></a>Publicere e-faktureringsfunktionen

1. På siden med **e-faktureringsfunktioner** skal du vælge fanen **Versioner** for at administrere statussen for funktionen **CFDI-fakturaer (MX)**.
2. Vælg **Skift status** for at ændre funktionens status.

![Ændre status for e-faktureringsfunktionen.](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing--integration-in-finance"></a>Konfigurere integrationen af elektronisk fakturering i Finance

Hvis du vil konfigurere elektronisk fakturering i Finance, skal du fuldføre disse opgaver:

1. Importér ER-datamodellen, ER-datamodeltilknytningen og de formater, der kræves til CFDI-fakturaer.
2. Konfigurer svartyper for opdatering af CFDI-fakturaerne. Disse svartyper bruges til svaret fra den autoriserede certificeringsudbyderserver (PAC).

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a>Importere ER-datamodellen, ER-datamodeltilknytningen og kontekstkonfigurationerne for CFDI-fakturaer

1. Log på Finance.
2. Gå til arbejdsområdet **Elektronisk rapportering**, og vælg feltet **Microsoft** i sektionen **Konfigurationsudbydere**. Kontrollér, at denne konfigurationsudbyder er angivet til **Aktiv**. Du kan finde flere oplysninger om, hvordan du angiver en udbyder til **Aktiv**, i [Oprette konfigurationsudbydere og markere dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Vælg **Lagre**.
4. Vælg **Globalt lager \> Åbn**.
5. Importér **Fakturamodel**, **Fakturamodeltilknytning**, **CFDI-fakturaformat (MX)**, **CFDI-fakturaformat for anmodning om annullering (MX)** og **CFDI fakturaformat for annullering (MX)**.

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a>Aktivere funktionen til behandling af CFDI-fakturaer

1. Gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**.
2. På fanen **Funktioner** skal du markere afkrydsningsfeltet **Aktivér** i rækkerne for funktionsreferencerne **MX-00010** og **MX-00016**.

![Aktivere funktionerne til behandling af CFDI-fakturaer.](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a>Importere ER-konfigurationer og konfigurere svartyper for opdatering af CFDI-fakturaer

#### <a name="import-er-configurations"></a>Importér ER-konfigurationer

1. Gå til arbejdsområdet **Elektronisk rapportering**, og vælg feltet **Microsoft** i sektionen **Konfigurationsudbydere**.
3. Vælg **Lagre**.
4. Vælg **Globalt lager \> Åbn**.
5. Importér **Svarmeddelelsesmodel**, **Import af CFDI-fejllog (MX)** og **Import af CFDI-svarmeddelelse (MX)**.

#### <a name="set-up-the-response-types"></a>Konfigurere svartyper

1. Gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**.
2. Vælg **Tilføj** på fanen **Elektronisk dokument**.
3. Angiv debitorfakturajournalen, og vælg derefter projektfakturaen i feltet **Tabelnavn**.
4. Definer en relateret dokumentkontekst for hver tabel:

    - Angiv en **Debitorfakturakontekst** for **Debitorfakturajournal**.
    - Angiv en **Projektfakturakontekst** for **Projektfaktura**.

4. Vælg **Svartyper** for at konfigurere de svartyper, der kan returneres fra elektronisk fakturering, og som er medtaget i en debitorfakturakladde eller projektfaktura.
5. Vælg **Ny**, og vælg derefter **Svar** i feltet **Svartype**.
6. Vælg **Afventer** i feltet **Indsendelsesstatus**.
7. I feltet **Modeltilknytning** skal du vælge **Format til import af svarmeddelelse – modeltilknytning fra svarmeddelelse**.
8. Vælg **Gem**.
9. Vælg **Ny**, og vælg derefter **ResponseData** i feltet **Svartype**.
10. Vælg **Afventer** i feltet **Indsendelsesstatus**.
11. I **Modeltilknytning** skal du vælge **Format til dataimport af CFDI-svar (detaljer) – dataimport af svar**.
12. Vælg **Gem**.

## <a name="process-electronic-invoices-in-finance"></a>Behandle elektroniske fakturaer i Finance 

Du kan udføre følgende opgaver under behandlingen af CFDI-fakturaer i Finance ved hjælp af elektronisk fakturering:

- Send CFDI-fakturaer.
- Få vist loggene for udførelse af indsendelse.
- Send annulleringen af en CFDI-faktura.

### <a name="submit-cfdi-invoices"></a>Sende CFDI-fakturaer

Når du har aktiveret funktionen **Konfigurerbar integration for elektronisk fakturering**, kan processen **Eksportér/importér elektronisk faktura** (**Debitor \> Fakturaer \> E-fakturaer**) ikke længere bruges til at sende CFDI-fakturaer. Den erstattes af den nye proces **Send elektroniske dokumenter**.

> [!NOTE]
> Før du bruger den nye proces **Send elektroniske dokumenter**, skal du kontrollere, at den opsætning, der kræves til mexicanske e-fakturaer, blev fuldført. Du kan finde flere oplysninger i [CFDI-layoutversion 3.3](./latam-mex-cfdi-3-3.md).

1. Gå til **Organisationsadministration \> Periodisk \> Elektroniske dokumenter \> Send elektroniske dokumenter**.
2. Ved den første indsendelse af et dokument skal du altid angive indstillingen **Send dokumenter igen** til **Nej**. Hvis du skal sende et dokument igen via tjenesten, skal du angive denne indstilling til **Ja**.
3. I oversigtspanelet **Poster, der skal indgå** skal du vælge **Filter** for at åbne dialogboksen **Forespørgsel**, hvor du kan oprette en forespørgsel for at vælge de dokumenter, der skal sendes.

![Sende et CFDI-dokument.](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> Under første forsøg på at sende et dokument via tjenesten bliver du bedt om at bekræfte forbindelsen med elektronisk fakturering. Vælg **Klik her for at oprette forbindelse til tjenesten til indsendelse af elektroniske dokumenter**.

### <a name="view-submission-logs"></a>Få vist indsendelseslogge

Du kan få vist indsendelseslogge for alle sendte dokumenter eller kun for ét sendt dokument.

#### <a name="view-all-submission-logs"></a>Få vist alle indsendelseslogge

Når du har aktiveret funktionen **Konfigurerbar integration for elektronisk fakturering**, bliver en ny side tilgængelig, hvor du kan følge op på processen for indsendelse af dokumenter. Du kan bruge denne side til at få vist indsendelseslogge for alle sendte dokumenter.

1. Gå til **Organisationsadministration \> Periodisk \> Elektroniske dokumenter \> Indsendelseslog for elektroniske dokumenter**.
2. I feltet **Dokumenttype** skal du vælge **Debitorfakturajournal** for at filtrere de nødvendige elektroniske dokumenter.

    ![Vælge en dokumenttype for at få vist indsendelseslogge.](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. Vælg **Forespørgsler \> Indsendelsesoplysninger** i handlingsruden for at få vist logoplysningerne for udførelse af indsendelsen.

    ![Få vist logoplysninger om indsendelse.](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

Oplysningerne i indsendelseslogge er opdelt mellem tre oversigtspaneler:

- **Behandling af handlinger** – I dette oversigtspanel vises udførelsesloggen for de handlinger, der er konfigureret i den funktionsversion, som blev konfigureret i RCS. Kolonnen **Status** viser, om handlingen blev kørt korrekt.
- **Handlingsfiler** – I dette oversigtspanel vises de midlertidige filer, der blev oprettet under udførelse af handlingerne. Du kan vælge **Vis** for at downloade og få vist filen.
- **Handlingslog for behandling** – I dette oversigtspanel vises resultaterne af kommunikationen mellem elektronisk fakturering og destinationswebtjenesten. Den viser også, hvad der blev returneret af behandlingen fra webtjenesten. Kolonnen **Fejlkode** viser den returkode, der blev returneret af autorisationswebtjenesten.

Når den afsendte CFDI-faktura er godkendt, opdateres statussen til **Godkendt**.

#### <a name="view-submission-logs-from-cfdi-invoices"></a>Få vist indsendelseslogge fra CFDI-fakturaer

Når du har aktiveret funktionen **Konfigurerbar integration for elektronisk fakturering**, kan du også få vist indsendelsesloggene fra CFDI-fakturaer.

1. Gå til **Debitor \> Forespørgsler og rapporter \> CFDI (elektroniske fakturaer)**.
2. Vælg en CFDI-faktura, der blev sendt, efter at funktionen **Konfigurerbar integration for elektronisk fakturering** blev aktiveret.
3. Vælg **Log for elektronisk dokument** på fanen **Historik** i handlingsruden.

![Få vist indsendelseslogge fra CFDI-fakturaer.](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> Knappen **Historik** er tilgængelig for CFDI-fakturaer, der blev sendt, før funktionen **Konfigurerbar integration for elektronisk fakturering** blev aktiveret. Knappen **Historik** er ikke tilgængelig for CFDI-fakturaer, der blev sendt, efter at funktionen **Konfigurerbar integration for elektronisk fakturering** blev aktiveret.

### <a name="submit-cancellation-of-cfdi-invoices"></a>Sende annullering af CFDI-fakturaer

Når du har aktiveret funktionen **Konfigurerbar integration for elektronisk fakturering**, kan den gamle proces til annullering af CFDI-fakturaer ikke længere bruges. Den erstattes af en ny annulleringsproces, der er indlejret på siden **Indsendelseslog for elektroniske dokumenter**.

1. Gå til **Debitor \> Forespørgsler og rapporter \> CFDI (elektroniske fakturaer)**.
2. Hvis CFDI-fakturaen har statussen **Godkendt**, skal du vælge **Funktioner \> Annuller CFDI**.
3. Gå til **Organisationsadministration \> Periodisk \> Elektroniske dokumenter \> Indsendelseslog for elektroniske dokumenter**.
4. Vælg CFDI-fakturaen, og vælg derefter **Funktioner \> Send relaterede indsendelser**.
5. Angiv en beskrivelse af den relaterede indsendelse, og vælg derefter **OK**.

#### <a name="view-cancellation-submission-logs"></a>Få vist alle indsendelseslogge for annullering

1. Gå til **Organisationsadministration \> Periodisk \> Elektroniske dokumenter \> Indsendelseslog for elektroniske dokumenter**.
2. I feltet **Dokumenttype** skal du vælge **Debitorfakturajournal** for kun at filtrere efter debitorfakturajournaldokumenter.
3. Vælg CFDI-fakturaen, og vælg derefter **Forespørgsler \> Relateret indsendelse** i handlingsruden.

    På siden **Relaterede indsendelser** vises alle relaterede indsendelser og deres indsendelsesstatus for en bestemt CFDI-faktura. I følgende illustration repræsenterer den første linje den indsendelse, der anmodede om godkendelse af CFDI-fakturaen. Den anden linje repræsenterer den indsendelse, der annullerede den pågældende CFDI-faktura.

    ![Få vist alle indsendelseslogge for annullering.](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. Vælg **Forespørgsler \> Indsendelsesoplysninger** i handlingsruden for at få vist logoplysningerne for udførelse af indsendelsen.

    ![Få vist alle oplysninger om indsendelseslogge for annullering.](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger
Aktivering af funktionen **CFDI mexicansk elektronisk faktura (MX)** kan kræve, at der sendes begrænsede data, herunder organisationens momsregistrerings-id. Dette vil blive overført til tredjepartsorganer, der er godkendt af skattemyndighederne, med det formål at sende elektroniske fakturaer til denne skattemyndighed i det foruddefinerede format, der kræves til integration med myndighedernes webtjeneste. En administrator kan aktivere og deaktivere funktionen **CFDI mexicansk elektronisk faktura (MX)** ved at gå til **Organisationsadministration \> Konfiguration\> Parametre for elektronisk dokument**. Vælg fanen **Funktioner**, og vælg de rækker, der indeholder funktionen **CFDI mexicansk elektronisk faktura (MX)** og derefter foretage de relevante valg. De data, der importeres fra disse eksterne systemer til denne Dynamics 365-onlinetjeneste, er underlagt vores [erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=512132). Yderligere oplysninger finder du i sektionerne med Erklæring om beskyttelse af personlige oplysninger i dokumentationen for den lande- eller områdespecifikke funktion.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk fakturering](e-invoicing-service-overview.md)
- [Start her med elektronisk fakturering](e-invoicing-get-started.md)
- [Konfigurere elektronisk fakturering](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
