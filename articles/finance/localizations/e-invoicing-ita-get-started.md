---
title: Kom i gang med tilføjelsesprogrammet til elektronisk fakturering for Italien
description: Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med tilføjelsesprogrammet til elektronisk fakturering for Italien i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 08d41244d3ec785127db8f69e37dd522a463c388
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988534"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-italy"></a>Kom i gang med tilføjelsesprogrammet til elektronisk fakturering for Italien

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> Tilføjelsesprogrammet til elektronisk fakturering for Italien understøtter i øjeblikket muligvis ikke alle de funktioner, der er tilgængelige for elektroniske fakturaer i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management. 

Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med tilføjelsesprogrammet til elektronisk fakturering for Italien. Det fører dig gennem de konfigurationstrin, der er landeafhængige i Regulatory Configuration Services (RCS) og i Finance. Det fører dig også gennem processen til indsendelse af elektroniske fakturaer, der er oprettet i formatet **FatturaPA**, som er specifikt for Italien, og forklarer, hvordan du kan gennemgå resultaterne af behandlingen.

## <a name="prerequisites"></a>Forudsætninger

Før du udfører trinene i dette emne, skal du udføre trinnene i [Kom i gang med tilføjelsesprogrammet til elektronisk fakturering](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>RCS-opsætning

Under RCS-opsætningen skal du udføre disse opgaver:

1. Importér e-faktureringsfunktionen til eksport af elektroniske fakturaer til kunder i formatet **FatturaPA**.
2. Gennemse de formatkonfigurationer, der skal bruges til at oprette, sende og modtage svar om elektroniske fakturaer.
3. Konfigurer de hændelser, der understøtter scenarierne for indsendelse af elektroniske fakturaer.
4. Publicer e-faktureringsfunktionen.

> [!NOTE]
> "E-faktureringsfunktionen" er det generiske navn på den ressource, der er konfigureret og publiceret til at bruge serveren for tilføjelsesprogrammet til elektronisk fakturering. I dette tilfælde er eksporten af elektroniske fakturaer til kunder den e-faktureringsfunktion, du skal konfigurere.

## <a name="import-the-e-invoicing-feature"></a>Importere e-faktureringsfunktionen

1. Log på din RCS-konto.
2. I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **e-fakturering**.
3. På siden med **e-faktureringsfunktioner** skal du vælge **Importér** for at importere e-faktureringsfunktionen fra det globale lager.

    > [!NOTE]
    > Hvis du ikke kan se listen over tilgængelige funktioner, skal du vælge **Synkroniser**. 

4. Vælg funktionen **Eksport af e-fakturaer (IT)**, og vælg derefter **Importér**.

![Importere funktionen Eksport af e-fakturaer (IT)](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

Når du importerer funktionen **Eksport af e-fakturaer (IT)** fra det globale lager, importeres alle de indstillinger, der er beskrevet i de næste afsnit, også.

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a>Oprette en ny version af funktionen Eksport af e-fakturaer (IT)

1. På siden med **e-faktureringsfunktioner** på fanen **Versioner** skal du vælge **Ny**. 

    ![Tilføje en ny version af e-faktureringsfunktionen](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    Derefter skal du konfigurere de elektroniske rapporteringsformater (ER), der er knyttet til e-faktureringsfunktionen.

2. På fanen **Konfigurationer** skal du vælge **Tilføj** for at administrere konfigurationsversionerne.

    ![Administrere konfigurationsversionerne for e-faktureringsfunktion](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    I dette trin tilføjer og konfigurerer du ER-formaterne for de forskellige filer, der bruges til at eksportere italienske e-fakturaer. I forbindelse med italienske FatturaPA-e-fakturaer kan du enten bruge følgende standardkonfigurationer eller de faktiske tilpassede konfigurationer, du bruger til e-fakturering:

    - Salgsfaktura (IT)
    - Projektfaktura (IT)

    Når du opretter en e-faktureringsfunktion, der er afledt af en anden e-faktureringsfunktion, nedarves alle ER-formater fra den oprindelige funktion.

3. Vælg en specifik filkonfiguration for ER-formatet.
4. Vælg **Rediger** eller **Vis** for at åbne siden **Formatdesigner**.

    ![Åbne siden Formatdesigner](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. Du kan bruge siden **Formatdesigner** til at redigere og få vist filkonfigurationer for ER-formatet.

    ![Siden Formatdesigner](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>Administrere funktionsopsætninger for e-fakturering

- På siden med **e-faktureringsfunktioner** på fanen **Konfigurationer** skal du vælge **Tilføj**, **Slet** eller **Rediger** for at administrere funktionsopsætningerne for e-fakturering.

![Administrere funktionsopsætninger for e-fakturering](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

I dette trin konfigurerer du de hændelser, der gælder for elektroniske fakturaer, herunder oprettelse af XML-outputfiler i formatet **FatturaPA** og digital underskrivning (hvis det er nødvendigt).

### <a name="configure-the-sales-invoice-feature-setup"></a>Konfigurere funktionsopsætningen for Salgsfaktura

1. Vælg **Salgsfaktura** i kolonnen **Funktionsopsætning** på fanen **Konfigurationer** på siden med **e-faktureringsfunktioner**.
2. Vælg **Rediger**.
3. På siden **Opsætning af funktionsversion** skal du vælge fanen **Handlinger** for at administrere listen over handlinger. Handlinger definerer en liste over handlinger, der skal køres i rækkefølge for at opnå fuld udførelse af hændelsen.

    ![Fanen Handlinger](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | Handlings-id | Handlingsnavn        | Handlingsbeskrivelse                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | 1         | Transformere document | Opret XML-filen til e-fakturaen i formatet **FatturaPA**. |
    | 2         | Underskriv dokument      | Anvend en digital underskrift på XML-filen.             |

4. Vælg fanen **Anvendelighedsregler** for at få vist og vedligeholde anvendelighedsreglerne. Anvendelighedsregler definerer den kontekst, som handlingen vil blive kørt i.

    ![Fanen Anvendelighedsregler](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. Vælg fanen **Variabler** for at få vist og vedligeholde variablerne.

    ![Fanen Variabler](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. Definer de offentlige variabler, der skal bruges til at køre handlingerne.

### <a name="configure-the-project-invoice-feature-setup"></a>Konfigurere funktionsopsætningen for Projektfaktura 

De trin og indstillinger, der kræves for at konfigurere funktionsopsætningen for **Projektfaktura**, minder meget om trinnene og indstillingerne for funktionsopsætningen for **Salgsfaktura**. Når du arbejder med projektfakturaer, kan du se procedurerne for salgsfakturaer.

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a>Tildele e-faktureringsfunktionen til miljøet

1. På siden med **e-faktureringsfunktioner** på fanen **Miljøer** skal du vælge **Aktivér**.
2. Vælg miljøet i feltet **Miljø**.
3. I feltet **Gyldig fra** skal du vælge den dato, hvor miljøet skal være gyldigt.
4. Vælg **Aktivér**. 

![Aktivere e-faktureringsmiljøet](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a>Publicere e-faktureringsfunktionen

Du kan publicere e-faktureringsfunktionen ved at ændre versions status til **Fuldført** eller **Publiceret**.

### <a name="change-the-version-status-to-completed"></a>Skifte versionsstatus til Fuldført

1. På siden med **e-faktureringsfunktioner** på fanen **Versioner** skal du vælge den e-faktureringsfunktion, der har statussen **Kladde**.
2. Vælg **Skift status \> Fuldfør**. 

### <a name="change-the-version-status-to-published"></a>Skifte versionsstatus til Publiceret 

1. På siden med **e-faktureringsfunktioner** på fanen **Versioner** skal du vælge den e-faktureringsfunktion, der har statussen **Fuldført**.
2. Vælg **Skift status \> Publicer**.

![Ændre status for e-faktureringsfunktionen](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance"></a>Konfigurere integrationen af tilføjelsesprogrammet til elektronisk fakturering i Finance

Under opsætningen af Finance skal du udføre disse opgaver:

1. Importere ER-datamodellen, ER-datamodeltilknytningen og kontekstkonfigurationerne for FatturaPA-e-fakturaer.
2. Konfigurer det certifikat, der kræves for at kunne underskrive italienske e-fakturaer digitalt.

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a>Importere ER-datamodellen, -datamodeltilknytningen og -formaterne

1. I arbejdsområdet **Elektronisk rapportering** skal du kontrollere, at konfigurationsudbyderen **Business Document Service** er angivet til **Aktiv**.
2. Vælg **Lagre**.
3. Vælg **Globalt lager \> Åbn**.
4. Importér **Fakturamodel**, **Fakturamodeltilknytning** og **Debitorfakturakontekstmodel**.

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a>Aktivere funktionen til eksport af elektroniske fakturaer til kunder for Italien

1. Gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**.
2. På fanen **Funktioner** skal du markere afkrydsningsfeltet **Aktiveret** i rækken for funktionsreferencen **IT00036**.

![Aktivere funktionen FatturaPA](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a>Konfigurere elektroniske dokumenter

1. Gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**.
2. Vælg **Tilføj** på fanen **Elektronisk dokument**, og angiv de tabeller, der skal bruges til oprettelse af italienske e-fakturaer:

    - **Tabelnavn:** Debitorfakturajournal
    - **Tabelnavn:** Projektfaktura

3. Definer en relateret dokumentkontekst for hver tabel:

    - Vælg **Debitorfakturakontekst** for **Debitorfakturajournal**.
    - Vælg **Projektfakturakontekst** for **Projektfaktura**.

![Konfigurere svartyper](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a>Behandling af elektronisk faktura

Under behandlingen i Finance skal du udføre disse opgaver:

1. Oprette italienske e-fakturaer ved hjælp af tilføjelsesprogrammet til elektronisk fakturering
2. Få vist logfilerne for udførelse, og gennemse resultaterne af behandlingen

### <a name="generate-electronic-invoices"></a>Oprette elektroniske fakturaer

Når du har aktiveret funktionen **Konfigurerbar integration for tilføjelsesprogrammet til elektronisk fakturering** og aktiverer funktionen **IT00036**, kan den gamle Finance-proces til oprettelse af italienske e-fakturaer ikke længere bruges. Den erstattes af den nye proces **Send elektroniske dokumenter**.

Du kan sende dokumenterne manuelt baseret på dit behov for e-fakturadokumenter.

> [!NOTE]
> Før du fortsætter, skal du kontrollere, at den opsætning, der kræves til italienske e-fakturaer, blev fuldført. Du kan finde flere oplysninger i [Elektroniske fakturaer til kunder](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices). Bemærk, at nogle af de opsætningstrin, der er beskrevet i dette emne, muligvis ikke er tilgængelige pga. aktivering af tilføjelsesprogrammet til elektronisk fakturering.

1. Gå til **Organisationsadministration \> Periodisk \> Elektroniske dokumenter \> Send elektroniske dokumenter**.
2. Ved den første indsendelse af et dokument skal du angive indstillingen **Send dokumenter igen** til **Nej**. Hvis du skal sende et dokument igen via tjenesten, skal du angive denne indstilling til **Ja**.
3. I oversigtspanelet **Poster, der skal indgå** skal du vælge **Filter** for at åbne dialogboksen **Forespørgsel**, hvor du kan oprette en forespørgsel for at vælge de dokumenter, der skal sendes.

![Dialogboksen Send elektroniske dokumenter](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a>Filterforespørgsel

1. I dialogboksen **Forespørgsel** kan du konfigurere filtreringsbetingelserne for både salgsfakturaer og projektfakturaer eller lade betingelserne stå tomme for at medtage alle de fakturaer, der ikke er sendt.

    ![Konfigurere filterkriterier for indsendelse](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. Vælg **OK** for at lukke dialogboksen **Forespørgsel**.
3. Vælg **OK** for at sende de valgte dokumenter.

> [BEMÆRK!] I løbet af første forsøg på at sende et dokument via tjenesten bliver du bedt om at bekræfte forbindelsen med tilføjelsesprogrammet til elektronisk fakturering. Vælg **Klik her for at oprette forbindelse til tjenesten til indsendelse af elektroniske dokumenter**.

#### <a name="view-submission-logs"></a>Få vist indsendelseslogge

Du kan få vist indsendelseslogge for alle sendte dokumenter.

1. Gå til **Organisationsadministration \> Periodisk \> Elektroniske dokumenter \> Indsendelseslog for elektroniske dokumenter**.
2. I feltet **Dokumenttype** skal du vælge **Debitorfakturajournal** eller **Projektfaktura** for at filtrere de nødvendige elektroniske dokumenter.

    ![Vælge en dokumenttype for at få vist indsendelseslogge](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    Den værdi, der vises i kolonnen **Indsendelsesstatus**, repræsenterer status for indsendelsesprocessen. Den angiver, om processen kørte som konfigureret, og om der skal udføres yderligere handlinger.

3. Vælg **Forespørgsler \> Indsendelsesoplysninger** i handlingsruden for at få vist logoplysningerne for udførelse af indsendelsen.

    ![Få vist logoplysninger om indsendelse](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. I oversigtspanelet **Behandling af handlinger** kan du se udførelsesloggen for de handlinger, der er konfigureret i den funktionsversion, som blev konfigureret i RCS. Kolonnen **Status** viser, om handlingen blev kørt korrekt.
5. I oversigtspanelet **Handlingsfiler** kan du se de midlertidige filer, der blev oprettet under udførelse af handlingerne. Du kan vælge **Vis** for at downloade XML-outputfilen i formatet **FatturaPA** og få vis indholdet.

## <a name="related-topics"></a>Relaterede emner

- [Oversigt over tilføjelsesprogrammet til elektronisk fakturering](e-invoicing-service-overview.md)
- [Kom i gang med tilføjelsesprogrammet til elektronisk fakturering](e-invoicing-get-started.md)
- [Konfigurere tilføjelsesprogrammet til elektronisk fakturering](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]