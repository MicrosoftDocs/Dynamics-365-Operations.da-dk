---
title: Kom i gang med tilføjelsesprogrammet til elektronisk fakturering for Brasilien
description: Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med tilføjelsesprogrammet til elektronisk fakturering for Brasilien i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: fb3ec2d60875d7a0747d64b397aafaa0a3d26348
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039863"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a>Kom i gang med tilføjelsesprogrammet til elektronisk fakturering for Brasilien 

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> Tilføjelsesprogrammet til elektronisk fakturering for Brasilien understøtter i øjeblikket ikke alle de funktioner, der er tilgængelige i regnskabsdokumentintegrationen, der er indbygget i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.

Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med tilføjelsesprogrammet til elektronisk fakturering for Brasilien. Det fører dig gennem de konfigurationstrin, der er landeafhængige i Regulatory Configuration Services (RCS) og i Finance and Supply Chain Management. Det fører dig også gennem processen med at sende et NF-e-regnskabsdokument (elektronisk regnskabsdokumentmodel 55) via tjenesten og forklarer, hvordan du gennemgår behandlingsresultaterne og statussen for regnskabsdokumenterne.

## <a name="prerequisites"></a>Forudsætninger

Før du udfører trinene i dette emne, skal du udføre trinnene i [Kom i gang med tilføjelsesprogrammet til elektronisk fakturering](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>RCS-opsætning

Under RCS-opsætningen skal du udføre disse opgaver:

1. Importer e-faktura funktionen til NF-e-regnskabsdokumenter.
2. Gennemgå de filformater, der er nødvendige for at sende NF-e-regnskabsdokumenter til autorisation.
3. Gennemgå de filformater, der er nødvendige for at anmode om annulleringen af en godkendt NF-e.
4. Konfigurer den hændelse, der er nødvendig for at sende NF-e-regnskabsdokumenter til autorisation.
5. Konfigurer den hændelse, der er nødvendig for at anmode om annulleringen af en godkendt NF-e.
6. Tildel e-faktureringsfunktionen til et miljø for tilføjelsesprogrammet til elektronisk fakturering.
7. Publicer e-faktureringsfunktionen.

> [!NOTE]
> "E-faktureringsfunktionen" er det generiske navn på den ressource, der er konfigureret og publiceret til at bruge serveren for tilføjelsesprogrammet til elektronisk fakturering. Konfigurationen af e-faktureringsfunktionen kombinerer bl.a. brugen af konfigurationsformater til elektronisk rapportering (ER) for til at oprette konfigurerbare eksport- og importfiler samt brugen af handlinger og handlingsflow for at muliggøre oprettelsen af regler til at sende anmodninger, importere svar og fortolke indholdet i svar.

## <a name="import-the-e-invoicing-feature"></a>Importere e-faktureringsfunktionen

1. Logge på din RCS-konto
2. I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **e-fakturering**.
3. På siden med **e-faktureringsfunktioner** skal du vælge **Importér** for at importere en e-faktureringsfunktion for et NF-e-regnskabsdokument fra det globale lager.

    ![Knappen Importér](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. Vælg NF-e-regnskabsdokumentsfunktionen, og vælg derefter **Importér**.

    ![Importere NF-e-funktionen](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a>Oprette en ny version af NF-e-regnskabsdokumentfunktionen

- På siden med **e-faktureringsfunktioner** på fanen **Versioner** skal du vælge **Ny**.

![Tilføje en ny version af e-faktureringsfunktionen](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a>Opdatere konfigurationsversionen

1. På siden med **e-faktureringsfunktioner** under **Konfigurationer** skal du vælge **Tilføj** eller **Slet** for at administrere konfigurationsversionerne (filkonfigurationer for ER-format).

    ![Administrere konfigurationer for e-faktureringsfunktion](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - Når du opretter en ny version af NF-e-regnskabsdokumentfunktionen, er alle konfigurationsversioner (ER-filformater) nedarvet fra den nyeste version.
    - Hvis du vil sende NF-e-regnskabsdokumentet til autorisation, kræves følgende konfigurationsversioner:

        - Eksportformat for NFe-indsendelse
        - Import af NFe-svarmeddelelse
        - Import af NFe-fejllog

    - Hvis du vil indsende NF-e-annulleringen, kræves følgende konfigurationsversion:

        - Eksportformat for NFe-annullering

2. Vælg en konfigurationsversion på listen, og vælg derefter **Rediger** eller **Vis** for at åbne siden **Formatdesigner** , hvor du kan redigere eller få vist konfigurationen.

    ![Åbne siden Formatdesigner](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. Du kan bruge siden **Formatdesigner** til at redigere eller få vist filkonfigurationer for ER-format. Du kan finde flere oplysninger i [Oprette konfigurationer for elektroniske dokumenter](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).

    ![Siden Formatdesigner](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a>Administrere funktionsopsætninger for e-fakturering

- På siden med **e-faktureringsfunktioner** på fanen **Konfigurationer** skal du vælge **Tilføj** eller **Slet** for at administrere opsætningerne af e-faktureringsfunktionen (dvs. NF-e-hændelser).

![Administrere funktionsopsætninger for e-fakturering](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

Når du opretter en ny version af NF-e-regnskabsdokumentfunktionen, der er afledt af en anden e-faktureringsfunktion, er alle funktionsopsætninger (NF-e-hændelser) nedarvet fra den seneste version.

Funktionsopsætningen **Send** er nødvendig for at sende NF-e-regnskabsdokumenter til autorisation.

Funktionsopsætningen **Annullering** er nødvendig for at sende NF-e-annulleringen.

#### <a name="configure-the-submit-feature-setup"></a>Konfigurere funktionsopsætningen Send

1. Vælg **Send** i kolonnen **Funktionsopsætning** på fanen **Konfigurationer** på siden med **e-faktureringsfunktioner**.
2. Vælg **Rediger**.

    ![Redigere funktionsopsætningen for e-fakturering](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. På siden **Opsætning af funktionsversion** skal du vælge fanen **Handlinger** for at administrere listen over handlinger.

    ![Fanen Handlinger](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. Gennemgå de handlinger, der er nødvendige for at sende et NF-e til autorisation.

    | Handlings-id | Handlingsnavn                  | Handlingsbeskrivelse                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | 1         | Transformere document           | Opret NF-e-XML-filen til indsendelse.                          |
    | 2         | Underskriv dokument                | Anvend det digitale certifikat på XML-filen.                    |
    | 3         | Kalde brasiliansk SEFAZ-tjeneste | Send den signerede XML-fil til webtjenesterne til autorisation. |
    | 4         | Behandle svar             | Hent svaret fra webtjenesterne.                                     |
    | 5         | Transformere document           | Fortolk indholdet af den fil, der er modtaget som et svar.     |
    | 6         | Transformere document           | Opret XML-filen for at anmode om status for indsendelsen.    |
    | 7         | Kalde brasiliansk SEFAZ-tjeneste | Send den XML-fil, der anmoder om indsendelsesstatussen.          |
    | 8         | Behandle svar             | Hent svaret fra webtjenesterne.                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>Konfigurere URL-adressen til SEFAZ-webtjenester 

1. På siden **Opsætning af funktionsversion** på fanen **Handlinger** på oversigtspanelet **Handlinger** skal du vælge **Kald brasiliansk SEFAZ-tjeneste** (handlings-id **3** ).
2. På oversigtspanelet **Parametre** i feltet **URL-adresseparameter** skal du angive URL-adressen til SEFAZ-webtjenesten til NF-e-indsendelse.
3. På oversigtspanelet **Handlinger** skal du vælge **Kald brasiliansk SEFAZ-tjeneste** (handlings-id **7** ).
4. På oversigtspanelet **Parametre** i feltet **URL-adresseparameter** skal du angive URL-adressen til SEFAZ-webtjenesten til NF-e-indsendelse.

#### <a name="configure-the-cancellation-feature-setup"></a>Konfigurere funktionsopsætningen Annullering

1. Vælg **Annullering** i kolonnen **Funktionsopsætning** på fanen **Konfigurationer** på siden med **e-faktureringsfunktioner**.
2. Vælg **Rediger**.
3. På siden **Opsætning af funktionsversion** skal du vælge fanen **Handlinger** for at administrere listen over handlinger.
4. Gennemgå de handlinger, der er nødvendige for at anmode om annulleringen af en godkendt NF-e.

    | Handlings-id | Handlingsnavn                  | Handlingsbeskrivelse                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | 1         | Transformere document           | Opret XML-filen for NF-annulleringen til indsendelse.            |
    | 2         | Underskriv dokument                | Anvend det digitale certifikat på XML-filen.                   |
    | 3         | Kalde brasiliansk SEFAZ-tjeneste | Send den signerede XML-fil til webtjenesterne til annullering. |
    | 4         | Behandle svar             | Hent svaret fra webtjenesterne.                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>Konfigurere URL-adressen til SEFAZ-webtjenester

1. På siden **Opsætning af funktionsversion** på fanen **Handlinger** på oversigtspanelet **Handlinger** skal du vælge **Kald brasiliansk SEFAZ-tjeneste** (handlings-id **3** ).
2. På oversigtspanelet **Parametre** i feltet **URL-adresseparameter** skal du angive URL-adressen til SEFAZ-webtjenesten til annullering af en godkendt NF-e.

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a>Gøre et e-faktureringsmiljø tilgængeligt og tildele en kladdeversion

1. På siden med **e-faktureringsfunktioner** på fanen **Miljøer** skal du vælge **Aktivér**.
2. Vælg miljøet i feltet **Miljø**.
3. I feltet **Gyldig fra** skal du vælge den dato, hvor miljøet skal være gyldigt.
4. Vælg **Aktivér**.

![Aktivere et e-faktureringsmiljø](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a>Skifte status til Fuldført

1. På siden med **e-faktureringsfunktioner** på fanen **Versioner** skal du vælge den e-faktureringsfunktion, der har statussen **Kladde**.
2. Vælg **Skift status \> Fuldfør**.

### <a name="change-the-status-to-publish"></a>Skifte status til Publicer

1. På siden med **e-faktureringsfunktioner** på fanen **Versioner** skal du vælge den e-faktureringsfunktion, der har statussen **Fuldført**.
2. Vælg **Skift status \> Publicer**.

![Publicere e-faktureringsfunktionen](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Konfigurere integrationen af tilføjelsesprogrammet til elektronisk fakturering i Finance eller Supply Chain Management

Under opsætningen skal du udføre disse opgaver:

1. Aktivér funktionen NF-e-forbund for Brasilien.
2. Importér den specifikke ER-datamodel, datamodeltilknytningen og de formater, der kræves til NF-e-regnskabsdokumenter.
3. Importér ER-konfigurationen, og konfigurer de svartyper, der kræves for at opdatere regnskabsdokumentets status, efter at indsendelsesprocessen er returneret.

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a>Aktivere NF-e Federal-funktionen for Brasilien

1. Gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**.
2. På fanen **Funktioner** skal du markere afkrydsningsfeltet **Aktivér** i rækken for funktionsreferencen **BR00053**.

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a>Importere den ER-datamodeltilknytning, der kræves til NF-e-regnskabsdokumenter

1. Log på Finance.
2. Gå til arbejdsområdet **Elektronisk rapportering** , og vælg feltet **Microsoft** i sektionen **Konfigurationsudbydere**. Kontrollér, at denne konfigurationsudbyder er angivet til **Aktiv**. Du kan finde flere oplysninger om, hvordan du angiver en udbyder til **Aktiv** , i [Oprette konfigurationsudbydere og markere dem som aktive](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Vælg **Lagre**.
4. Vælg **Globalt lager \> Åbn**.
5. Importér konfigurationer for **tilknytning af regnskabsdokumenter**.

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a>Importere ER-konfigurationer og konfigurere svartyper for regnskabsdokumenter

1. Gå til arbejdsområdet **Elektronisk rapportering** , og vælg feltet **Microsoft** i sektionen **Konfigurationsudbydere**.
2. Vælg **Lagre**.
3. Vælg **Globalt lager \> Åbn**.
4. Importér **Import af NFe-fejllog (BR)** , **Format til dataimport af NF-e-svar (BR)** og **Import af NFe-svarmeddelelse (BR)**.
5. Gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**.
6. Vælg **Tilføj** på fanen **Elektronisk dokument**.
6. Angiv **Regnskabsdokumentnotat** i feltet **Tabelnavn**.
7. I feltet **Dokumentkontekst** skal du vælge **Kontekstmodel for debitorfaktura – regnskabsdokumentkontekst**.
8. Vælg **Svartyper**.
9. Vælg **Ny** , og vælg derefter **Svar** i feltet **Svartype**.
10. Vælg **Afventer** i feltet **Indsendelsesstatus**.
11. I feltet **Modeltilknytning** skal du vælge **Format til import af svarmeddelelse – modeltilknytning fra svarmeddelelse**.
12. Vælg **Gem**.
13. Vælg **Ny** , og angiv derefter **ResponseData** i feltet **Svartype**.
14. Vælg **Afventer** i feltet **Indsendelsesstatus**.
15. I **Modeltilknytning** skal du vælge **Format til dataimport af NFe-svar – dataimport af svar**.
16. Vælg **Gem**.

## <a name="electronic-invoice-processing"></a>Behandling af elektronisk faktura

Under behandlingen i Finance skal du udføre disse opgaver:

1. Send et regnskabsdokument ved hjælp af tilføjelsesprogrammet til elektronisk fakturering.
2. Få vist loggene for udførelse af indsendelsen, og gennemgå resultaterne af behandlingen.
3. Send annulleringen af et regnskabsdokument ved hjælp af tilføjelsesprogrammet til elektronisk fakturering.

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a>Sende NF-e-regnskabsdokumenter til SEFAZ-autorisation 

Når du har aktiveret funktionen **Konfigurerbar integration for tilføjelsesprogrammet til elektronisk fakturering** , kan den gamle proces til indsendelse af NF-e-regnskabsdokumenter til autorisation ( **Eksportér/importér NF-e-proces** ) ikke længere bruges. Den erstattes af den nye proces **Send elektroniske dokumenter**.

> [!NOTE]
> Før du fortsætter, skal du sikre dig, at du har et eller flere regnskabsdokumenter (model 55) for debitorer, der er udstedt af debitorens skattekontor. Retningen for disse regnskabsdokumenter skal angives til **Udgående** , og status skal være **Oprettet**. Yderligere oplysninger finder du under [Udstede regnskabsdokument for debitor (Brasilien)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).

1. Gå til **Organisationsadministration \> Periodisk \> Elektroniske dokumenter \> Send elektroniske dokumenter**.
2. Ved den første indsendelse af et dokument skal du altid angive indstillingen **Send dokumenter igen** til **Nej**. Hvis du skal sende et dokument igen via tjenesten, skal du angive denne indstilling til **Ja**.
3. I oversigtspanelet **Poster, der skal indgå** skal du vælge **Filter** for at åbne dialogboksen **Forespørgsel** , hvor du kan oprette en forespørgsel for at vælge de dokumenter, der skal sendes.
4. Vælg **Tilføj** på fanen **Interval**.
5. Vælg **Regnskabsdokumentnotat** i feltet **Tabelnavn**.
6. Vælg **Regnskabsdokumentnotat** i feltet **Afledt tabel**.
6. Vælg **Nummer** i feltet **Felt**.
7. I feltet **Kriterier** skal du angive nummeret på det regnskabsdokument, der skal sendes.
8. Vælg **OK** for at lukke dialogboksen **Forespørgsel**.
8. Vælg **OK** for at sende de valgte dokumenter.

> [!NOTE]
> I løbet af første forsøg på at sende et dokument via tjenesten bliver du bedt om at bekræfte forbindelsen med tilføjelsesprogrammet til elektronisk fakturering. Vælg **Klik her for at oprette forbindelse til tjenesten til indsendelse af elektroniske dokumenter**.

### <a name="view-all-submission-logs"></a>Få vist alle indsendelseslogge

Når du har aktiveret funktionen **Konfigurerbar integration for tilføjelsesprogrammet til elektronisk fakturering** , bliver en ny side tilgængelig, hvor du kan følge op på processen for indsendelse af dokumenter. Du kan bruge denne side til at få vist indsendelseslogge for alle sendte dokumenter.

1. Gå til **Organisationsadministration \> Periodisk \> Elektroniske dokumenter \> Indsendelseslog for elektroniske dokumenter**.
2. I feltet **Dokumenttype** skal du vælge **Regnskabsdokumentnotat** for kun at filtrere regnskabsdokumenter.
3. Vælg **Forespørgsler \> Indsendelsesoplysninger** i handlingsruden for at få vist logoplysningerne for udførelse af indsendelsen.

![Få vist logoplysninger om indsendelse](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> I forbindelse med NF-e-regnskabsdokumenter viser kolonnen **Fejlkode** den returkode, der blev returneret af SEFAZ-webtjenesterne.

### <a name="view-submission-logs-through-the-fiscal-document-page"></a>Få vist indsendelseslogge via regnskabsdokumentsiden

Når du har aktiveret funktionen **Konfigurerbar integration for tilføjelsesprogrammet til elektronisk fakturering** , kan du også få vist indsendelsesloggene via regnskabsdokumentsiden.

1. Gå til **Finans \> Forespørgsler og rapporter \> Regnskabsdokumenter \> Alle regnskabsdokumenter**.
2. Vælg et regnskabsdokument, der tidligere blev sendt via tilføjelsesprogrammet til elektronisk fakturering.
3. Vælg **Log for elektronisk dokument** på fanen **NF-e-forbund**  i handlingsruden.

![Vise indsendelseslogge via regnskabsdokumentsiden](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a>Sende godkendte NF-e-regnskabsdokumenter til SEFAZ-annullering

Når du har aktiveret funktionen **Konfigurerbar integration for tilføjelsesprogrammet til elektronisk fakturering** , kan den gamle proces til annullering af NF-e-regnskabsdokumenter til autorisation ikke længere bruges. Den erstattes af en ny annulleringsproces, der er indlejret på siden **Indsendelseslog for elektroniske dokumenter**.

> [!NOTE]
> Kontrollér, at du har udført annulleringen af regnskabsdokumentet for debitoren for et godkendt NF-e-regnskabsdokument. Yderligere oplysninger finder du under [Annullere regnskabsdokument for debitor (Brasilien)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).

1. Gå til **Organisationsadministration \> Periodisk \> Elektroniske dokumenter \> Indsendelseslog for elektroniske dokumenter**.
2. Vælg regnskabsdokumentet, og vælg derefter **Funktioner \> Send relaterede indsendelser**.
3. Angiv en beskrivelse af den relaterede indsendelse, og vælg derefter **OK**.

### <a name="view-cancellation-submission-logs"></a>Få vist alle indsendelseslogge for annullering

1. Gå til **Organisationsadministration \> Periodisk \> Elektroniske dokumenter \> Indsendelseslog for elektroniske dokumenter**.
2. I feltet **Dokumenttype** skal du vælge **Regnskabsdokumentnotat** for kun at filtrere regnskabsdokumenter.
3. Vælg regnskabsdokumentet, og vælg derefter **Forespørgsler \> Relateret indsendelse** i handlingsruden.

    Relaterede indsendelser er indsendelser, der er relateret til en primær indsendelse, som blev oprettet først. Den indsendelse, der f.eks. godkender et bestemt NF-e, er den primære indsendelse. Den indsendelse, der anmoder om annulleringen af det samme NF-e i SEFAZ, er en relateret indsendelse. Den findes kun, fordi den anmoder om annulleringen af det job, der er udført gennem en anden indsendelse.

    På siden **Relaterede indsendelser** vises alle relaterede indsendelser og deres indsendelsesstatus for et bestemt regnskabsdokument. I følgende illustration repræsenterer den første linje den indsendelse, der anmodede om godkendelse af regnskabsdokumentet. Den anden linje repræsenterer den indsendelse, der annullerede det pågældende regnskabsdokument.

    ![Få vist alle indsendelseslogge for annullering](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. Vælg **Forespørgsler \> Indsendelsesoplysninger** i handlingsruden for at få vist logoplysningerne for udførelse af indsendelsen.

    ![Få vist alle oplysninger om indsendelseslogge for annullering](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger
Aktivering af funktionen BR-00053 (NF-e-forbund) kan kræve, at der sendes begrænsede data, herunder organisationens momsregistrerings-id. Dette vil blive overført til tredjepartsorganer, der er godkendt af skattemyndighederne, med det formål at sende elektroniske fakturaer til denne skattemyndighed i det foruddefinerede format, der kræves til integration med myndighedernes webtjeneste. En administrator kan aktivere og deaktivere funktionen BR-00053 (NF-e-forbund) ved at gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**. Vælg fanen **Funktioner** , vælg den række, der indeholder BR-00053-funktionen, og foretag derefter det relevante valg. De data, der importeres fra disse eksterne systemer til denne Dynamics 365-onlinetjeneste, er underlagt vores [erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=512132). Yderligere oplysninger finder du i sektionerne med Erklæring om beskyttelse af personlige oplysninger i dokumentationen for den landespecifikke funktion.


## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over tilføjelsesprogrammet til elektronisk fakturering](e-invoicing-service-overview.md)
- [Kom i gang med tilføjelsesprogrammet til elektronisk fakturering](e-invoicing-get-started.md)
- [Konfigurere tilføjelsesprogrammet til elektronisk fakturering](e-invoicing-setup.md)
