---
title: Tilpasse konfigurationer af elektroniske rapporter for at generere et elektronisk dokument
description: Dette emne forklarer, hvordan du tilpasser konfigurationer af et elektronisk rapporteringsformat (ER) fra Microsoft, der bruges til at oprette et brugerdefineret elektronisk dokument.
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "220314"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3c867af3b4d93e5a124d14e88eae60ff45987aebc639bd78806ff7a12009447
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769990"
---
# <a name="customize-electronic-reporting-configurations-to-generate-an-electronic-document"></a>Tilpasse konfigurationer af elektroniske rapporter for at generere et elektronisk dokument

[!include[banner](../includes/banner.md)]

Du kan bruge den [elektroniske rapporteringsstruktur (ER)](general-electronic-reporting.md) til at uploade de [ER-konfigurationer](general-electronic-reporting.md#Configuration), som Microsoft leverer til din Microsoft Dynamics 365 Finance-forekomst. På denne måde kan de konfigurationer, der leveres af Microsoft, fungere som den ER-løsning, der bruges til at generere elektroniske debitorfakturaer (e-fakturaer). Du kan bruge denne ER-løsning til at konfigurere din brugerdefinerede ER-løsning til at få adgang til dine brugerdefinerede databasefelter og generere e-fakturaer, der er kompatible med dine specifikke behov, uden at skulle redigere kildekoden.

## <a name="overview"></a>Overblik

I eksemplet i dette emne skal du angive en momsidentifikationskode som en ny brugerdefineret attribut for hver debitor, du fakturerer. Du skal derfor tilpasse strukturen for den faktura, der aktuelt bruges, ved at tilføje en ny vare, der skal udfyldes med momskoden i alle e-fakturaer, der genereres.

Procedurerne i dette emne forklarer, hvordan en bruger med rollen Systemadministrator, Udvikler af elektronisk rapportering eller Funktionel konsulent i elektronisk rapportering kan udføre disse opgaver i din forekomst af Finance:

- [Konfigurer det minimale sæt af ER-parametre, der kræves for at begynde at bruge ER-strukturen](#ConfigureER).
- [Importér de første versioner af ER-standardkonfigurationer, der leveres til generering af e-fakturaer](#ImportERConfigurations1).
- [Konfigurer debitorparametre for at begynde at bruge ER-standardkonfigurationerne](#ConfigureAR1).
- [Konfigurer de juridiske enhedsparametre for at fakturere kunder](#ConfigureLE).
- [Forbered en kundepost til elektronisk fakturering](#ConfigureCustomer1).
- [Tilføj, bogfør og send en debitorfaktura ved hjælp af ER-standardkonfigurationerne](#ProcessInvoice1).
- [Tilføj et brugerdefineret databasefelt for at administrere en momsidentifikationskode for kunder](#AddCustomField).
- [Opdater ER-metadataene for at aktivere databaseændringer for ER-modeltilknytningsdesigneren](#RefreshERMetadata).
- [Design brugerdefinerede ER-konfigurationer til generering af e-fakturaer, der indeholder den nye momskode](#DesignCustomERConfigurations).
- [Konfigurer debitorparametre for at anvende de brugerdefinerede ER-konfigurationer](#ConfigureAR2).
- [Opdater en kundepost til elektronisk fakturering](#ConfigureCustomer2).
- [Tilføj, bogfør og send en debitorfaktura ved hjælp af brugerdefinerede ER-konfigurationer](#ProcessInvoice2).
- [Importér de nye versioner af ER-standardkonfigurationer, der leveres til generering af e-fakturaer](#ImportERConfigurations2).
- [Anvend ændringerne på de nye versioner af ER-standardkonfigurationerne i dine brugerdefinerede ER-konfigurationer](#RebaseCustomERConfigurations).
- [Tilføj, bogfør og send en debitorfaktura ved hjælp af nye versioner af brugerdefinerede ER-konfigurationer](#ProcessInvoice3).

Alle disse procedurer kan udføres i **DEMF**-virksomheden.

## <a name="configure-the-er-framework"></a><a name="ConfigureER"></a>Konfigurere ER-strukturen

Som bruger af den elektroniske rapporteringskonsulent eller den elektroniske rapportudvikler skal du konfigurere det minimale sæt af ER-parametre. Du kan derefter begynde at bruge ER-strukturen til at designe brugerdefinerede versioner af standardkonfigurationerne i den ER-løsning, der bruges til generering af e-fakturaer.

### <a name="configure-er-parameters"></a>Konfigurere ER-parametre

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Parametre til elektronisk rapportering** i sektionen **Relaterede links**.
3. På siden **Parametre til elektronisk rapportering** under fanen **Generelt** skal du vælge **Ja** i indstillingen **Aktiver designtilstand** .
4. Vælg **Fil** i feltet **Konfigurationer** under fanen **Vedhæftede filer**.
5. I felterne **Jobarkiv**, **Midlertidig**, **Grundlag** og **Andre** skal du vælge typen **Fil**.

Du kan finde flere oplysninger om ER-parametre under [Konfigurere ER-strukturen](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a>Aktivere en udbyder af ER-konfigurationer

Alle ER-konfigurationer, der tilføjes, er markeret som ejet af en udbyder af ER-konfigurationer. Den udbyder af ER-konfigurationer, der aktiveres i arbejdsområdet **Elektronisk rapportering**, bruges til dette formål. Du skal derfor aktivere en udbyder af ER-konfigurationer i arbejdsområdet **Elektronisk rapportering**, før du begynder at tilføje eller redigere ER-konfigurationer.

> [!NOTE]
> Det er kun ejeren af en ER-konfiguration, der kan redigere den. Før du kan redigere en ER-konfiguration, skal den relevante udbyder af ER-konfiguration aktiveres i arbejdsområdet **Elektronisk rapportering**.

#### <a name="review-the-list-of-er-configuration-providers"></a>Gennemse listen over udbydere af ER-konfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Konfigurationsudbydere** i sektionen **Relaterede links**.
3. På siden **Tabel over konfigurationsudbydere** har hver udbyderpost et entydigt navn og en entydig URL-adresse. Gennemse indholdet af denne side. Hvis der allerede findes en post for **Litware, Inc.** (`https://www.litware.com`), skal du springe den næste procedure over, [Tilføje en ny udbyder af ER-konfigurationer](#AddProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Tilføje en ny udbyder af ER-konfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Konfigurationsudbydere** i sektionen **Relaterede links**.
3. På siden **Konfigurationsudbydere** skal du vælge **Ny**.
4. I feltet **Navn** skal du angive **Litware, Inc.**
5. I feltet **Internetadresse** skal du angive `https://www.litware.com`.
6. Vælg **Gem**.

#### <a name="activate-an-er-configuration-provider"></a>Aktivere en udbyder af ER-konfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. Gå til siden **Lokaliseringskonkfigurationer**, og vælg feltet **Litware, Inc.** i sektionen **Konfigurationsudbydere**, og vælg derefter **Angiv som aktive**.

Få flere oplysninger om udbydere af ER-konfigurationer under [Oprette konfigurationsudbydere og markere dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-initial-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations1"></a>Importere de første versioner af ER-standardkonfigurationer

Hvis du vil føje standard-ER-konfigurationerne til din aktuelle forekomst af Finance, skal du importere dem fra det [ER-lager](general-electronic-reporting.md#Repository), der er konfigureret for den pågældende forekomst.

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du i sektionen **Konfigurationsudbydere** vælge feltet **Microsoft** og derefter vælge **Lagre** for at få vist listen over lagre for Microsoft-udbyderen.
3. På siden **Konfigurationslagre** skal du vælge lageret for **Global**-typen og derefter vælge **Åbn**. Hvis du bliver bedt om at angive godkendelse for at oprette forbindelse til Regulatory Configuration Service, skal du følge godkendelsesvejledningen.
4. På siden **Konfigurationslager** skal du i konfigurationstræet i venstre rude vælge formatkonfigurationen **Peppol Salgsfaktura**.
5. I oversigtspanelet **Versioner** skal du vælge version **11.2.2**.
6. Vælg **Importér** for at downloade den valgte version fra det globale lager.

![Siden Konfigurationslager.](./media/er-quick-start3-import-solution1.png)

> [!TIP]
> Hvis du har problemer med at få adgang til det [globale lager](er-download-configurations-global-repo.md), kan du [hente konfigurationer](download-electronic-reporting-configuration-lcs.md) fra Microsoft Dynamics Lifecycle Services (LCS) i stedet.

### <a name="review-the-imported-er-configurations"></a>Gennemse de importerede ER-konfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Rapporteringskonfigurationer** i sektionen **Konfigurationer**.
3. På siden **Konfigurationer** skal du udvide oversigtspanelet **Konfigurationskomponenter**.
4. I konfigurationstræet i venstre rude skal du udvide **Fakturamodel** og derefter udvide **UBL-salgsfaktura**.

Bemærk, at der ud over det valgte **Peppol Salgsfaktura**-format, blev importeret andre påkrævede ER-konfigurationer. Da nye versioner af ER- konfigurationer løbende publiceres til det globale lager og LCS og for at holde de tilsvarende løsninger kompatible med de nye krav, blev de seneste versioner af konfigurationen af den påkrævede [datamodel](general-electronic-reporting.md#data-model-and-model-mapping-components) og den tilhørende [modeltilknytning](general-electronic-reporting.md#data-model-and-model-mapping-components) importeret.

![Siden Konfigurationer.](./media/er-quick-start3-imported-solution1a.png)

Hvis du vil simulere den tilstand, som ER-konfigurationer i den aktuelle Finance-forekomst ville være, hvis du har importeret version **11.2.2** af **Peppol Salgsfaktura** tidligere (f.eks. 7. august 2019), skal du følge disse trin.

- I handlingsruden skal du vælge **Slet** for at slette alle de ER-konfigurationer, der er udgivet efter 7. august 2019. De eneste konfigurationer af **Fakturamodel**, **Fakturamodeltilknytning** (oprindeligt navngivet **Kundefakturamodeltilknytning**), **UBL-salgsfaktura** og **Peppol Salgsfaktura** skal efterlades.
- I oversigtspanelet **Versioner** skal du vælge **Slet** for at slette alle versioner af ER-konfigurationer, der er udgivet efter 7. august, 2019.

Kontrollér derefter, at følgende ER-konfigurationer er tilgængelige i konfigurationstræet:

- **Fakturamodel** som ER-datamodelkonfiguration (oprindeligt navngivet **Debitorfakturamodel**):

    - Version 11 indeholder version 10 af [datamodellen](general-electronic-reporting.md#data-model-and-model-mapping-components) som ER-komponent, der repræsenterer datastrukturen for domænet til fakturering. Denne ER-konfiguration er importeret som en forgænger til det ER-format for **Peppol Salgsfaktura**, der blev valgt til import.
    - Version 50 indeholder version 31 af ER-komponenten til datamodellen. Denne ER-konfiguration er importeret som en forgænger til versionen fra 7. august 2019 af ER-modeltilknytningskonfigurationen **Fakturamodeltilknytning**.

    ![Fakturamodel som ER-datamodelkonfiguration på siden Konfigurationer.](./media/er-quick-start3-imported-solution1b1.png)

    > [!TIP]
    > Hvis du ikke kan se version 50 af denne datamodel, skal du åbne det globale lager og importere version 50.19 af ER-konfigurationen **Fakturamodeltilknytning**.

- **Fakturamodeltilknytning** som ER-modeltilknytningskonfiguration (oprindeligt navngivet **Kundefakturamodeltilknytning**):

    - Version 50.19 er blevet importeret som den seneste implementering af version 50 af **Fakturamodel** som ER-datamodelkonfigurationen. Den indeholder to [modeltilknytning](general-electronic-reporting.md#data-model-and-model-mapping-components)-ER-komponenter, der beskriver, hvordan datamodellen udfyldes med applikationsdata under kørslen.

    ![Fakturamodeltilknytning som ER-modeltilknytningskonfiguration på siden Konfigurationer.](./media/er-quick-start3-imported-solution1b2.png)

    > [!TIP]
    > Hvis du ikke kan se version 50.19 af denne modeltilknytning, skal du åbne det globale lager og importere version 50.19 af ER-konfigurationen **Fakturamodeltilknytning**.

- **UBL-salgsfaktura** som ER-formatkonfiguration:

    - Version 11.2 indeholder [format](general-electronic-reporting.md#FormatComponentOutbound) og formattilknytning som ER-komponenter. Formatkomponenten angiver rapportlayoutet. Komponenten til formattilknytning indeholder modeldatakilden og angiver, hvordan denne datakilde bruges til at udfylde rapportlayoutet på kørselstidspunktet. Dette Er-format blev konfigureret til at generere e-fakturaer i UBL-format (Universal Business Language). Det er importeret som overordnet til det ER-format for **Peppol Salgsfaktura**, der blev valgt til import.

- **Peppol Salgsfaktura** som ER-formatkonfiguration:

    - Version 11.2.2 indeholder de ER-komponenter til format og formattilknytning, der er konfigureret til generering af e-fakturaer i PEPPOL-format (Pan-European Public Procurement OnLine).

    ![Peppol Salgsfaktura som ER-formatkonfiguration på siden Konfigurationer.](./media/er-quick-start3-imported-solution1b3.png)

## <a name="configure-the-accounts-receivable-parameters"></a><a name="ConfigureAR1"></a>Konfigurere debitorparametre

1. Gå til **Debitor** \> **Konfiguration** \> **Debitorparametre**.
2. Vælg **Peppol Salgsfaktura** i feltet **Salgs- og fritekstfaktura** under fanen **Elektroniske dokumenter** i oversigtspanelet **Elektronisk rapportering**.
3. Vælg **Gem**.

![Fanen Elektroniske dokumenter på siden Debitorparametre.](./media/er-quick-start3-configure-ar1.png)

## <a name="configure-the-legal-entity-parameters"></a><a name="ConfigureLE"></a>Konfigurere parametrene for den juridiske enhed

1. Gå til **Organisationsadministration** \> **Organisationer** \> **Juridiske enheder**.
2. Angiv **1234** i feltet **Registreringsnummer** i oversigtspanelet **Bankkontooplysninger** for det valgte **DEMF**-firma.
3. Vælg **Gem**.
4. Luk siden **Juridiske enheder**.

## <a name="prepare-a-customer-record"></a><a name="ConfigureCustomer1"></a>Forberede en kundepost

1. Gå til **Debitor** \> **Kunder** \> **Alle kunder**.
2. Vælg debitorkontolinket **DE-014** på siden **Alle kunder**.

### <a name="add-a-customer-contact"></a>Tilføje en kundekontakt

1. Gå til **Debitor** \> **Kunder** \> **Alle kunder**.
2. Vælg **Kontakter** i gruppen **Konti** under fanen **Debitor** i handlingsruden.
3. Vælg **Tilføj kontakter**.
4. Åbn opslaget i feltet **Fornavn** på siden **Kontakter**, vælg **Adam Carter**, og vælg derefter **Vælg** for at lukke opslaget.
5. Vælg **Gem**.
6. Luk siden **Kontakter**.

### <a name="define-a-primary-contact"></a>Definere en primær kontakt

1. Gå til **Debitor** \> **Kunder** \> **Alle kunder**.
2. Gå til oversigtspanelet **Salgsdemografi**, og vælg **Adam Carter** i feltet **Primær kontakt**.

### <a name="set-the-e-invoicing-option"></a>Angive indstillingen for e-fakturering

1. Gå til **Debitor** \> **Kunder** \> **Alle kunder**.
2. I oversigtspanelet **faktura og levering** skal du angive indstillingen **eFaktura** til **Ja**.
3. Vælg **Gem**.
4. Luk siden **Alle kunder**.

## <a name="process-a-customer-invoice-by-using-the-standard-er-configurations"></a><a name="ProcessInvoice1"></a>Behandle en debitorfaktura ved hjælp af ER-standardkonfigurationerne

Du kan nu bruge ER-standardkonfigurationerne, som du importerede, til elektronisk afsendelse af en fritekstfaktura til en kunde.

### <a name="add-a-new-invoice"></a>Tilføje en ny faktura

1. Gå til **Debitor** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. Vælg **Ny** på siden **Fritekstfaktura**.
3. I oversigtspanelet **Fritekstfakturahoved** skal du i feltet **Debitorkonto** vælge **DE-014**.
4. I oversigtspanelet **Fakturalinjer** tilføjes der automatisk en fakturalinje. Angiv følgende felter på denne linje:

    - Indtast **Notesbog** i feltet **Beskrivelse**.
    - Vælg **401100** i feltet **Hovedkonto**.
    - Indtast **1000** i feltet **Enhedspris**.

5. Vælg **Gem**.

![Siden Fritekstfaktura.](./media/er-quick-start3-add-invoice.png)

Du kan finde flere oplysninger i [Oprette en fritekstfaktura](../../../finance/accounts-receivable/create-free-text-invoice-new.md).

### <a name="post-a-new-invoice"></a>Bogføre en ny faktura

1. Gå til **Debitor** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. Vælg **Bogfør** i handlingsruden på siden **Fritekstfaktura**.
3. Vælg **OK** i dialogboksen **Bogfør fritekstfaktura**.

![Siden Detaljer om fritekstfaktura.](./media/er-quick-start3-post-invoice.png)

### <a name="send-a-posted-invoice"></a>Sende en bogført faktura

1. Gå til **Debitor** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. Vælg **Send** \> **Original** i **Dokument**-gruppen i handlingsruden på siden **Fritekstfaktura**.

    ![Visning af originalfakturaen.](./media/er-quick-start3-send-invoice.png)

3. Luk siden **Fritekstfaktura**.

### <a name="analyze-a-generated-e-invoice"></a>Analysere en genereret e-faktura

1. Gå til **Virksomhedsadministration** \> **Elektronisk rapportering** \> **Elektroniske rapporteringsjob**.
2. På siden **Elektroniske rapporteringsjob** skal du vælge den første post, der indeholder opgavebeskrivelsen **Send eFaktura-XML**.
3. Vælg **Vis filer** for at få adgang til listen over genererede filer.

    ![Siden Elektroniske rapporteringsjob.](./media/er-quick-start3-jobs-list.png)

4. Vælg **Åbn** for at downloade den XML-fil, der er oprettet for e-fakturaen.
5. Analysér XML-filen med e-fakturaen. Bemærk, at debitormomsskemaet i øjeblikket er repræsenteret af XML-attributterne **schemeID** og **schemeAgencyID**. Bemærk også, at **cbc:CustomizationID**-XML-elementet i øjeblikket indeholder følgende tekst: `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0`.

    ![Visning af den genererede XML-fil med e-faktura.](./media/er-quick-start3-e-invoice1.png)

## <a name="add-a-custom-database-field"></a><a name="AddCustomField"></a>Tilføje et brugerdefineret databasefelt

Du kan bruge funktionen [Brugerdefineret felt](../../fin-ops/get-started/user-defined-fields.md) til at foretage følgende tilpasning i den aktuelle Finance-forekomst:

- Tilpas databasestrukturen ved at tilføje et nyt brugerdefineret databasefelt, der gemmer en momsidentifikationskode for hver debitor.
- Tilpas siden **Debitor** ved at tilføje et nyt dataindtastningsfelt, der kan bruges til at angive en momskodeværdi i det nye brugerdefinerede databasefelt.

Udfør følgende trin for at foretage tilpasningen.

1. Gå til **Debitor** \> **Kunder** \> **Alle kunder**.
2. Vælg debitorkontolinket **DE-014** på siden **Alle kunder**.
3. I oversigtspanelet **Generelt** skal du højreklikke i et tomt område under **Sprog**-feltet og derefter vælge **Tilpas: UpperGroup**.

    Indholdet af oversigtspanelet **Generelt** er fremhævet, og menuen **Tilpas** vises.

4. Vælg **Tilføj et felt** i menuen **Tilpas**.
5. Vælg **Opret nyt felt** i dialogboksen **Tilføj kolonner**.
6. Vælg **Debitorer** i feltet **Tabelnavn** i dialogboksen **Opret nyt felt**.
7. I feltet **Navnepræfiks** skal du angive **FederalTaxID**.

    > [!NOTE]
    > Hele feltnavnet er automatisk defineret som **FederalTaxID\_Brugerdefineret**.

8. Angiv **Federal Tax ID** i feltet **Etiket**.
9. Vælg **Tekst** i feltet **Type**.
10. Angiv **20** i feltet **Længde**.
11. Vælg **Gem**.
12. Vælg **Ja** i den meddelelsesboks, der vises, for at bekræfte, at du vil oprette en ny **FederalTaxID**-feltpost for tabellen **Debitorer**.
13. Vælg **Indsæt** for at <a name="insert_custom_field"></a>tilføje feltet **FederalTaxID\_Brugerdefineret** på den aktuelle side.

    ![Siden Alle debitorer.](./media/er-quick-start3-create-new-field.gif)

14. Luk siden **Alle kunder**.

## <a name="refresh-the-er-metadata"></a><a name="RefreshERMetadata"></a>Opdatere ER-metadata

Du skal opdatere ER-metadataene for at gøre det brugerdefinerede felt, du har tilføjet, [synligt](electronic-reporting-er-configure-parameters.md#frequently-asked-questions) i ER-modeltilknytningsdesigneren.

1. Gå til **Virksomhedsadministration** \> **Elektronisk rapportering** \> **Genopbyg tabelreferencer**.
2. Vælg **OK** i dialogboksen **Opdater datamodel**.

## <a name="design-the-custom-er-configurations"></a><a name="DesignCustomERConfigurations"></a>Designe de brugerdefinerede ER-konfigurationer

Du kan bruge ER-konfigurationerne fra Microsoft til at designe dine brugerdefinerede ER-konfigurationer, så de genererer e-fakturaer, der indeholder den nye momskode.

### <a name="customize-the-data-model-configuration"></a>Tilpasse konfigurationen af datamodellen

Som bruger i rollen Funktionel konsulent i elektronisk rapportering kan du designe din brugerdefinerede ER-datamodel.

#### <a name="add-a-custom-data-model-configuration"></a>Tilføje en brugerdefineret datamodelkonfiguration

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude vælge **Debitorfakturamodel**.
3. Vælg **Opret konfiguration** i handlingsruden.
4. Vælg **Afledt fra navn: debitorfakturamodel, Microsoft** på rullelisten i dialogboksen for feltet **Ny** for at angive, at din nye brugerdefinerede ER-datamodelkonfiguration skal baseres på konfigurationen af ER-datamodellen.
5. Angiv **Fakturamodel (Litware)** i feltet **Navn**.
6. Vælg **Opret konfiguration** for at tilføje den nye ER-konfiguration.

Du kan nu bruge ER-datamodeldesigneren til at redigere version 50.1 af **Fakturamodel (Litware)**-ER-konfigurationen i **Kladde-**[status](general-electronic-reporting.md#component-versioning).

![Version 50.1 af den redigerbare ER-konfiguration på siden Konfigurationer.](./media/er-quick-start3-added-custom-model.png)

#### <a name="configure-a-custom-data-model"></a>Konfigurer en brugerdefineret datamodel

Du skal redigere din brugerdefinerede datamodel ved at tilføje et nyt felt, hvis du vil angive værdien for en momsidentifikationskode. Denne kode er en del af kundedataene for hvert ER-format, der skal bruge denne datamodel som datakilde.

1. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude vælge **Fakturamodel (Litware)**.
2. I oversigtspanelet **Versioner** skal du vælge version **50.1** for den valgte ER-datamodelkonfiguration i status **Kladde**.
3. Vælg **Designer** for den valgte konfigurationsversion i handlingsruden.
4. På siden **Datamodeldesigner** i datamodeltræet skal du vælge **Kundeoplysninger (kunde)**.
5. Vælg **Ny**.
6. Acceptér standardværdien **Underordnet for en aktiv node** i feltet **Ny node** på rullelisten i dialogboksen.
7. I feltet **Navn** skal du angive **FederalTaxID\_Litware**.
8. Acceptér standardværdien **Streng** i feltet **Varetype**.
9. Vælg **Tilføj**, og vælg derefter **Gem**.

    ![Siden Datamodeldesigner.](./media/er-quick-start3-add-data-model-field.png)

    > [!NOTE]
    > Felterne **Etiket** og **Beskrivelse** beskriver formålet med det nye felt. Du kan udfylde disse felter på flere sprog. Du kan finde flere oplysninger under [Designe flersprogede rapporter i elektronisk rapportering](er-design-multilingual-reports.md).

10. Luk siden **Datamodeldesigner**.

#### <a name="complete-a-custom-data-model-configuration"></a>Fuldføre en brugerdefineret datamodelkonfiguration

Du skal [fuldføre](general-electronic-reporting.md#component-versioning) dit arbejde med version 50.1 af din brugerdefinerede ER-datamodelkonfiguration for at gøre den tilgængelig, så der kan tilføjes andre brugerdefinerede ER-konfigurationer.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Fakturamodel** og derefter vælge **Fakturamodel (Litware)**.
3. I oversigtspanelet **Versioner** skal du vælge **Skift status** \> **Fuldfør** og derefter vælge **OK**.

Statussen for version 50.1 ændres fra **Kladde** til **Fuldført**, og versionen bliver skrivebeskyttet. Der er tilføjet en ny redigerbar version, 50.2, som har status af **Kladde**. Du kan bruge denne version til at foretage yderligere ændringer af din brugerdefinerede ER-datamodelkonfiguration.

![Version 50.1 fuldført på siden Konfigurationer.](./media/er-quick-start3-completed-custom-model1.png)

### <a name="customize-the-model-mapping-configuration"></a>Tilpasse konfigurationen af modeltilknytning

Som bruger i rollen udvikler af elektronisk rapportering kan du designe din brugerdefinerede ER-modeltilknytning.

#### <a name="add-a-custom-model-mapping-configuration"></a>Tilføje en brugerdefineret modeltilknytningskonfiguration

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Debitorfakturamodel** og derefter vælge **Kundefakturamodeltilknytning**.
3. Vælg **Opret konfiguration** i handlingsruden.
4. Vælg **Afledt fra navn: Kundefakturamodeltilknytning, Microsoft** på rullelisten i dialogboksen for feltet **Ny** for at angive, at din nye brugerdefinerede ER-modeltilknytningskonfiguration skal baseres på ER-modeltilknytningskonfigurationen.
5. Angiv **Fakturamodeltilknytning (Litware)** i feltet **Navn**.
6. Vælg **Fakturamodel (Litware)** i feltet **Målmodel**.

    > [!IMPORTANT]
    > Dette trin er meget vigtigt. Hvis du udelader den, kan du ikke bruge din brugerdefinerede datamodel i den konfigurerede modeltilknytning.

7. Vælg **Opret konfiguration** for at tilføje den nye ER-konfiguration.

![Tilføjelse af en brugerdefineret modeltilknytningskonfiguration på siden Konfigurationer.](./media/er-quick-start3-adding-custom-mapping.png)

#### <a name="configure-a-custom-model-mapping"></a>Konfigurere en brugerdefineret modeltilknytning

Du skal redigere din brugerdefinerede modeltilknytning og angive, hvordan feltet **FederalTaxID\_Litware** i den brugerdefinerede datamodel skal udfyldes med programdata ved kørslen.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Debitorfakturamodel** \> **Kundefakturamodeltilknytning** og vælge **Fakturamodeltilknytning (Litware)**.
3. Vælg **Designer** i handlingsruden.
4. Vælg **Debitorfaktura** i handlingsruden på siden **Tilknytning af model til datakilde**.

    ![Siden Tilknytning af model til datakilde.](./media/er-quick-start3-select-customer-mapping.png)

5. Vælg **Designer**.
6. På siden **Modeltilknytningsdesigner** i ruden **Datakilder** skal du udvide den **CustInvoiceJour**-datakilde, der repræsenterer **CustInvoiceJour**-programtabellen.
7. Under **CustInvoiceJour** skal du udvide **Relationer** for at gennemgå listen over relationer af typen mange til én (N:1) for tabellen **CustInvoiceJour**.
8. Under **CustInvoiceJour** \> **Relationer** skal du udvide **Debitorer (CustTable)** for at få adgang til felterne og relationerne i tabellen **Debitorer (CustTable)**.
9. Vælg det **FederalTaxID\_Brugerdefineret**-datakildefelt, som du har implementeret [tidligere](#insert_custom_field).
10. Udvid **Kundeoplysninger (kunde)** i ruden **Datamodel**, og vælg **FederalTaxID\_Litware**-datamodelfeltet.
11. Vælg **Bind**.

    ![Siden Modeltilknytningsdesigner.](./media/er-quick-start3-customize-model-mapping.gif)

12. Vælg **Gem**.
13. Luk siden **Modeltilknytningsdesigner**.
14. Luk siden **Tilknytning af model til datakilde**.

#### <a name="complete-a-custom-model-mapping-configuration"></a>Fuldføre en brugerdefineret modeltilknytningskonfiguration

Du skal [fuldføre](general-electronic-reporting.md#component-versioning) dit arbejde med version 50.19.1 af din brugerdefinerede ER-modeltilknytningskonfiguration for at gøre den tilgængelig for brug.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Debitorfakturamodel** \> **Kundefakturamodeltilknytning** og vælge **Fakturamodeltilknytning (Litware)**.
3. I oversigtspanelet **Versioner** skal du vælge **Skift status** \> **Fuldfør** og derefter vælge **OK**.

Statussen for version 50.19.1 ændres fra **Kladde** til **Fuldført**, og versionen bliver skrivebeskyttet. Der er tilføjet en ny redigerbar version, 50.19.2, som har status af **Kladde**. Du kan bruge denne version til at foretage yderligere ændringer af din brugerdefinerede ER-modeltilknytningskonfiguration.

![Version 50.19.1 fuldført på siden Konfigurationer.](./media/er-quick-start3-completed-custom-mapping1.png)

> [!NOTE]
> Den understøttede konfigurations [livscyklus](general-electronic-reporting-manage-configuration-lifecycle.md) dækker ikke livscyklussen for databaseændringer. Hvis du eksporterer version 50.19.1 af **Fakturamodeltilknytning (Litware)**-konfigurationen fra den aktuelle Finance-forekomst og forsøger at importere den i en anden forekomst, der ikke indeholder feltet **FederalTaxID\_Brugerdefineret** i tabellen **CustTable**, opstår der en undtagelse. Undtagelsen vil angive, at den importerede ER-konfiguration ikke er kompatibel med metadataene i målforekomsten af Finance.

### <a name="customize-the-format-configuration"></a>Tilpasse formatkonfigurationen

Som bruger i rollen Funktionel konsulent i elektronisk rapportering kan du designe dit brugerdefinerede ER-format.

#### <a name="add-a-custom-format-configuration"></a>Tilføje en brugerdefineret formatkonfiguration

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Debitorfakturamodel** \> **UBL-salgsfaktura** og vælge **Peppol Salgsfaktura**.
3. Vælg **Opret konfiguration** i handlingsruden.
4. Vælg **Afledt fra navn: Peppol Salgsfaktura, Microsoft** på rullelisten i dialogboksen for feltet **Ny** for at angive, at din nye brugerdefinerede ER-formatkonfiguration skal baseres på konfigurationen af ER-formatet.
5. Angiv **Peppol Salgsfaktura (Litware)** i feltet **Navn**.
6. I feltet **Datamodel** skal du vælge **Fakturamodel (Litware)** for at bruge din brugerdefinerede datamodel og modeltilknytningskomponenter.

    > [!NOTE]
    > Dette trin er meget vigtigt. Hvis du udelader den, kan du ikke bruge din brugerdefinerede datamodel i det konfigurerede format.

7. Vælg definitionen **InvoiceCustomer** i feltet **Roddefinition**.
8. Vælg **Opret konfiguration** for at tilføje den nye ER-konfiguration.

![Tilføjelse af en brugerdefineret formatkonfiguration på siden Konfigurationer.](./media/er-quick-start3-adding-custom-format.png)

Du kan nu bruge ER-operationsdesigner til at redigere version 11.2.2.1 af **Peppol Salgsfaktura (Litware)**-ER-konfigurationen i **Kladde-**[status](general-electronic-reporting.md#component-versioning).

![Version 11.2.2.1 af den redigerbare ER-konfiguration på siden Konfigurationer.](./media/er-quick-start3-added-custom-format.png)

#### <a name="configure-a-custom-format"></a>Konfigurere et brugerdefineret format

Du skal redigere det brugerdefinerede format ved at tilføje et nyt formatelement, der skal udfylde værdien af en faktureret kundes momsidentifikationskode.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Debitorfakturamodel** \> **UBL-salgsfaktura** \> **Peppol Salgsfaktura** og vælge **Peppol Salgsfaktura (Litware)**.
3. Vælg **Designer** i handlingsruden.
4. I formattræet skal du udvide **XMLHeader** \> **Faktura** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** og vælge **cbc:ID**.
5. Vælg **Tilføj**, og vælg derefter **XML** \> **Attribut**.
6. I dialogboksen **Komponentegenskab** skal du i feltet **Navn** angive **FederalTaxID**.
7. Vælg **OK** for at tilføje et nyt formatelement for at oprette en ny **FederalTaxID**-XML-attribut i en genereret XML-fil.
8. I formattræet skal du under **XMLHeader** \> **Faktura** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** \> **cbc:ID** vælge **FederalTaxID**.
9. Vælg **Flyt op**.

![Nyt formatelement på siden Formatdesigner.](./media/er-quick-start3-customized-format.png)

#### <a name="configure-a-custom-format-mapping"></a>Konfigurere en brugerdefineret formattilknytning

1. På siden **Formatdesigner** under fanen **Tilknytning** skal du udvide datakilden **Faktura** for **Model**-typen.
2. Udvid **Kundeoplysninger (kunde)** under **Faktura**, og vælg **FederalTaxID\_Litware**.
3. Vælg **Bind**.

    ![Siden Formatdesigner.](./media/er-quick-start3-customized-format-mapping.png)

4. Vælg **Faktura** som datakilde for typen **Model**, og vælg derefter **Rediger**.
5. I feltet **Version** skal du vælge version **1** af din brugerdefinerede datamodel og derefter vælge **OK**.
6. Vælg **Gem**.
7. Luk siden **Formatdesigner**.

#### <a name="complete-a-custom-format-configuration"></a>Fuldføre en brugerdefineret formatkonfiguration

Du skal [fuldføre](general-electronic-reporting.md#component-versioning) dit arbejde med version 11.2.2.1 af din brugerdefinerede ER-formatkonfiguration for at gøre den tilgængelig for brug.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Debitorfakturamodel** \> **UBL-salgsfaktura** \> **Peppol Salgsfaktura** og vælge **Peppol Salgsfaktura (Litware)**.
3. I oversigtspanelet **Versioner** skal du vælge **Skift status** \> **Fuldfør** og derefter vælge **OK**.

Statussen for version 11.2.2.1 ændres fra **Kladde** til **Fuldført**, og versionen bliver skrivebeskyttet. Der er tilføjet en ny redigerbar version, 11.2.2.2, som har status af **Kladde**. Du kan bruge denne version til at foretage yderligere ændringer i din brugerdefinerede ER-formatkonfiguration.

![Version 11.2.2.1 fuldført på siden Konfigurationer.](./media/er-quick-start3-completed-custom-format1.png)

## <a name="configure-the-accounts-receivable-parameters-to-start-to-use-custom-er-configurations"></a><a name="ConfigureAR2"></a>Konfigurere debitorparametre for at anvende de brugerdefinerede ER-konfigurationer

1. Gå til **Debitor** \> **Konfiguration** \> **Debitorparametre**.
2. Vælg **Peppol Salgsfaktura (Litware)** i feltet **Salgs- og fritekstfaktura** under fanen **Elektroniske dokumenter** i oversigtspanelet **Elektronisk rapportering**.
3. Vælg **Gem**.

![Fanen Elektroniske dokumenter i oversigtspanelet Elektronisk rapportering på siden Debitorparametre.](./media/er-quick-start3-configure-ar2.png)

## <a name="update-a-customer-record-by-adding-a-federal-tax-identification-code"></a><a name="ConfigureCustomer2"></a>Opdatere en kundepost ved at tilføje en momsidentifikationskode

1. Gå til **Debitor** \> **Kunder** \> **Alle kunder**.
2. Vælg debitorkontolinket **DE-014** på siden **Alle kunder**.
3. Angiv **LITWARE-6789** i feltet **Federal Tax ID** i oversigtspanelet **Generelt**.
4. Vælg **Gem**.

    ![Side med DE-014-kundeoplysninger.](./media/er-quick-start3-added-tax-id-value.png)

5. Luk siden **Alle kunder**.

## <a name="process-a-customer-invoice-by-using-custom-er-configurations"></a><a name="ProcessInvoice2"></a>Behandle en debitorfaktura ved hjælp af brugerdefinerede ER-konfigurationerne

### <a name="select-and-send-a-posted-invoice"></a>Vælge og sende en bogført faktura

1. Gå til **Debitor** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. På siden **Fritekstfaktura** skal du vælge den faktura, som du tidligere har tilføjet og bogført.
3. Vælg **Send** \> **Original** i **Dokument**-gruppen i handlingsruden.
4. Luk siden **Fritekstfaktura**.

### <a name="analyze-a-generated-e-invoice"></a>Analysere en genereret e-faktura

1. Gå til **Virksomhedsadministration** \> **Elektronisk rapportering** \> **Elektroniske rapporteringsjob**.
2. På siden **Elektroniske rapporteringsjob** skal du vælge den sidste post, der indeholder opgavebeskrivelsen **Send eFaktura-XML**.
3. Vælg **Vis filer** for at få adgang til listen over genererede filer.
4. Vælg **Åbn** for at downloade den XML-fil, der er oprettet for e-fakturaen.
5. Analysér XML-filen med e-fakturaen. Bemærk, at i overensstemmelse med tilpasningen inkluderer kundemomsskemaet den brugerdefinerede **FederalTaxID**-XML-attribut ud over **schemeID**- og **schemeAgencyID**-XML-attributterne. Værdien af denne nye XML-attribut er angivet af det **LITWARE-6789**-moms-id, der blev angivet for en faktureret kunde.

    ![Visning af den genererede XML-fil med e-faktura og dine tilpasninger.](./media/er-quick-start3-e-invoice2.png)

## <a name="import-the-latest-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations2"></a>Importere de sidste versioner af ER-standardkonfigurationer

Hvis du vil bevare sættet med ER-standardkonfigurationer i din Finance-forekomst [opdateret](general-electronic-reporting-manage-configuration-lifecycle.md), skal du importere nye versioner af dem, når de bliver tilgængelige i det ER-[lager](general-electronic-reporting.md#Repository), der blev konfigureret for den pågældende forekomst.

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du i sektionen **Konfigurationsudbydere** vælge feltet **Microsoft** og derefter vælge **Lagre** for at få vist listen over lagre for Microsoft-udbyderen.
3. På siden **Konfigurationslagre** skal du vælge lageret for **Global**-typen og derefter vælge **Åbn**. Hvis du bliver bedt om at angive godkendelse for at oprette forbindelse til Regulatory Configuration Service, skal du følge godkendelsesvejledningen.
4. På siden **Konfigurationslager** skal du i konfigurationstræet i venstre rude vælge formatkonfigurationen **Peppol Salgsfaktura**.
5. I oversigtspanelet **Versioner** skal du vælge version **32.6.7** af den valgte ER-formatkonfiguration, der er udgivet for at understøtte kunders elektroniske fakturaer i PEPPOL BIS 3-format. Du kan finde flere oplysninger i [KB4490320](https://support.microsoft.com/help/4490320/an-update-for-european-union-to-support-export-of-customers-electronic).
6. Vælg **Importér** for at hente den valgte version fra Global-lageret til den aktuelle Finans-forekomst.

![Version 32.6.7, der er valgt på siden Konfigurationslager.](./media/er-quick-start3-import-solution2.png)

Oplysninger om, hvordan denne proces kan automatiseres, finder du under [Importere opdaterede versioner af ER-konfigurationer](er-download-updated-versions-global-repo.md).

### <a name="review-the-imported-er-configurations"></a>Gennemse de importerede ER-konfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Rapporteringskonfigurationer** i sektionen **Konfigurationer**.
3. Udvid oversigtspanelet **Konfigurationskomponenter**.
4. Udvid **Fakturamodel** i konfigurationstræet i ruden til venstre. Bemærk, at navnet **Debitorfakturamodel** er ændret til **Fakturamodel** i en af de importerede konfigurationer af ER-datamodellen.
5. Udvid **Fakturamodeltilknytning** i konfigurationstræet i ruden til venstre. Bemærk, at navnet **Kundefakturamodeltilknytning** er ændret til **Fakturamodeltilknytning** i en af de importerede konfigurationer af ER-modeltilknytning.
6. Udvid **UBL-salgsfaktura** \> **Peppol Salgsfaktura**.

Bemærk, at der ud over det valgte **Peppol Salgsfaktura**-format, blev de seneste versioner af andre påkrævede ER-konfigurationer også importeret. Da nye versioner af ER- konfigurationer løbende publiceres til det globale lager og LCS og for at holde de tilsvarende ER-løsninger kompatible med de nye krav, blev de seneste versioner af konfigurationen af den påkrævede datamodel og den tilhørende modeltilknytning importeret.

Kontrollér, at følgende ER-konfigurationer er tilgængelige i konfigurationstræet:

- **Fakturamodel** Konfiguration af ER-datamodel:

    - Version 206 (eller nyere) indeholder version 24 (eller nyere) af datamodellen som ER-komponent, der repræsenterer datastrukturen for domænet til fakturering. Denne ER-konfiguration er importeret som en forgænger til den senest tilgængelige ER-modeltilknytningskonfiguration af **Fakturamodeltilknytning**.

    ![Version 206 på siden Konfigurationer.](./media/er-quick-start3-imported-solution2b1.png)

- **Fakturamodeltilknytning** Konfiguration af ER-modeltilknytning:

    - Version 206.132 (eller nyere) er blevet importeret som den seneste implementering af version 206 af **Fakturamodel** som ER-datamodelkonfigurationen. Den indeholder flere modeltilknytning-ER-komponenter, der beskriver, hvordan datamodellen udfyldes med applikationsdata under kørslen.

    ![Version 206.132 på siden Konfigurationer.](./media/er-quick-start3-imported-solution2b2.png)

- **UBL-salgsfaktura** som ER-formatkonfiguration:

    - Version 32.6 indeholder format og formattilknytning som ER-komponenter. Formatkomponenten angiver rapportlayoutet. Komponenten til formattilknytning indeholder modeldatakilden og angiver, hvordan denne datakilde bruges til at udfylde rapportlayoutet på kørselstidspunktet. Dette Er-format blev konfigureret til at generere e-fakturaer i UBL-format. Det er importeret som overordnet til det ER-format for **Peppol Salgsfaktura**, der blev valgt til import.

- **Peppol Salgsfaktura** som ER-formatkonfiguration:

    - Version 32.6.7 indeholder de ER-komponenter til format og formattilknytning, der er konfigureret til generering af e-fakturaer i PEPPOL-format.

    ![Version 32.6.7 på siden Konfigurationer.](./media/er-quick-start3-imported-solution2b3.png)

## <a name="adopt-the-changes-to-the-new-standard-er-configurations-in-your-custom-er-configurations"></a><a name="RebaseCustomERConfigurations"></a>Anvende ændringerne på de nye ER-standardkonfigurationer i dine brugerdefinerede ER-konfigurationer

### <a name="adopt-your-custom-er-data-model"></a>Avende din brugerdefinerede ER-datamodel

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Fakturamodel** og derefter vælge **Fakturamodel (Litware)**.
3. I oversigtspanelet **Versioner** skal du for kladdeversion **50.2** af den valgte datamodelkonfiguration vælge **Rebasér**.
4. Bekræft valget af version **206** af ER-basisdatamodelkonfiguration i feltet **Målversion**, og vælg derefter **OK**.

    Kladdeversionen af din brugerdefinerede ER-datamodelkonfiguration nummereres om fra **50.2** til **206.2** for at angive, at den nu indeholder din tilpasning, der er blevet flettet med ændringerne i den seneste version (206) af ER-basisdatamodelkonfigurationen.

    > [!NOTE]
    > Rebaseringshandling kan fortrydes. Hvis du vil annullere denne rebasering, skal du vælge version **50.1** af modellen **Fakturamodel (Litware)** i oversigtspanelet **Versioner** og derefter vælge **Hent denne version**. Version 206.2 vil derefter blive nummereret tilbage til **50.2**, og indholdet af kladdeversion 50.2 vil svare til indholdet af version 50.1.

5. I oversigtspanelet **Versioner** skal du vælge **Skift status** \> **Fuldfør** og derefter vælge **OK**.

Statussen for version 206.2 ændres fra **Kladde** til **Fuldført**, og versionen bliver skrivebeskyttet. Der er tilføjet en ny redigerbar version, 206.3, som har status af **Kladde**. Du kan bruge denne version til at foretage yderligere ændringer af din brugerdefinerede ER-datamodelkonfiguration.

![Version 206.2 fuldført på siden Konfigurationer.](./media/er-quick-start3-completed-custom-model2.png)

### <a name="adopt-your-custom-er-model-mapping"></a>Avende din brugerdefinerede ER-modeltilknytning

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Fakturamodel** \> **Fakturamodeltilknytning** og vælge **Fakturamodeltilknytning (Litware)**.
3. I oversigtspanelet **Versioner** skal du for kladdeversion **50.19.2** af den valgte modeltilknytningskonfiguration vælge **Rebasér**.
4. Bekræft valget af version **206.132** af ER-basismodeltilknytningen i feltet **Målversion**, og vælg derefter **OK**.

    Kladdeversionen af din brugerdefinerede ER-modelmodeltilknytningskonfiguration nummereres om fra **50.19.2** til **206.132.2** for at angive, at den nu indeholder din tilpasning, der er blevet flettet med ændringerne i den seneste version (206.132) af ER-basismodelmodeltilknytningens konfiguration.

    Bemærk, at der er fundet nogle rebaseringskonflikter. Du skal nu løse disse konflikter manuelt.

    ![Meddelelsen om rebaseringskonflikt på siden Konfigurationer.](./media/er-quick-start3-rebase-conflicts-model-mapping1.png)

5. Vælg **Designer** i handlingsruden, og vælg derefter **Debitorfaktura** på listen over tilknytninger.
6. For hver rebaseringskonflikt skal du vælge **Bevar egen værdi**, da du skal beholde versionsnummeret for den brugerdefinerede datamodel for hver komponent, der er nævnt.

    ![Rebaseringskonflikter på siden for modeltilknytningsdesigneren.](./media/er-quick-start3-rebase-conflicts-model-mapping2.png)

7. Vælg **Gem**, og luk derefter siden **Modeltilknytningsdesigner**.
8. Vælg **Projektfaktura** på listen over tilknytninger.
9. For hver rebaseringskonflikt skal du vælge **Bevar egen værdi**, da du skal beholde versionsnummeret for den brugerdefinerede datamodel for hver komponent, der er nævnt.
10. Vælg **Gem**, og luk derefter siden **Modeltilknytninger**.

    > [!NOTE]
    > Rebaseringshandling kan fortrydes. Hvis du vil annullere denne rebasering, skal du vælge version **50.19.1** af modeltilknytningen **Fakturamodeltilknytning (Litware)** i oversigtspanelet **Versioner** og derefter vælge **Hent denne version**. Version 206.132.2 vil derefter blive nummereret tilbage til **50.19.2**, og indholdet af kladdeversion 50.19.2 vil svare til indholdet af version 50.19.1.

11. I oversigtspanelet **Versioner** skal du vælge **Skift status** \> **Fuldfør** og derefter vælge **OK**.

Statussen for version 206.132.2 ændres fra **Kladde** til **Fuldført**, og versionen bliver skrivebeskyttet. Der er tilføjet en ny redigerbar version, 206.132.3, som har status af **Kladde**. Du kan bruge denne version til at foretage yderligere ændringer af din brugerdefinerede ER-modeltilknytningskonfiguration.

![Version 206.132.2 fuldført på siden Konfigurationer.](./media/er-quick-start3-completed-custom-mapping2.png)

### <a name="adopt-your-custom-er-format"></a>Anvende dit brugerdefinerede ER-format

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Fakturamodel** \> **UBL-salgsfaktura** \> **Peppol Salgsfaktura** og vælge **Peppol Salgsfaktura (Litware)**.
3. I oversigtspanelet **Versioner** skal du for kladdeversion **11.2.2.2** af den valgte formatkonfiguration vælge **Rebasér**.
4. Bekræft valget af version **32.6.7** af ER-basisformatkonfiguration i feltet **Målversion**, og vælg derefter **OK**.

    Kladdeversionen af din brugerdefinerede ER-formatkonfiguration nummereres om fra **11.2.2.2** til **32.6.7.2** for at angive, at den nu indeholder din tilpasning, der er blevet flettet med ændringerne i den seneste version (32.6.7) af ER-basisformatkonfigurationen.

    Bemærk, at der er fundet nogle rebaseringskonflikter. Du skal nu løse disse konflikter manuelt.

5. Vælg **Designer** i handlingsruden.
6. For hver rebaseringskonflikt skal du vælge **Bevar egen værdi**, da du skal beholde versionsnummeret for den brugerdefinerede datamodel for hver komponent, der er nævnt.
7. Vælg **Gem**.
8. Vælg **Faktura** som datakilde for typen **Model** under fanen **Tilknytning** , og vælg derefter **Rediger**.
9. I feltet **Version** skal du vælge version **2** af din brugerdefinerede datamodel og derefter vælge **OK**.
10. Vælg **Gem**.

    > [!NOTE]
    > Rebaseringshandling kan fortrydes. Hvis du vil annullere denne rebasering, skal du vælge version **11.2.2.1** af formatet **Peppol Salgsfaktura (Litware)** i oversigtspanelet **Versioner** og derefter vælge **Hent denne version**. Version 32.6.7.2 vil derefter blive nummereret tilbage til **11.2.2.2**, og indholdet af kladdeversion 11.2.2.2 vil svare til indholdet af version 11.2.2.1.

11. Luk siden **Formatdesigner**.
12. I oversigtspanelet **Versioner** skal du vælge **Skift status** \> **Fuldfør** og derefter vælge **OK**.

Statussen for version 32.6.7.2 ændres fra **Kladde** til **Fuldført**, og versionen bliver skrivebeskyttet. Der er tilføjet en ny redigerbar version, 32.6.7.3, som har status af **Kladde**. Du kan bruge denne version til at foretage yderligere ændringer i din brugerdefinerede ER-formatkonfiguration.

![Version 32.6.7.2 fuldført på siden Konfigurationer.](./media/er-quick-start3-completed-custom-format2.png)

## <a name="process-a-customer-invoice-by-using-new-versions-of-the-custom-er-configurations"></a><a name="ProcessInvoice3"></a>Behandle en debitorfaktura ved hjælp af nye versioner af brugerdefinerede ER-konfigurationer

### <a name="select-and-send-a-posted-invoice"></a>Vælge og sende en bogført faktura

1. Gå til **Debitor** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. På siden **Fritekstfaktura** skal du vælge den faktura, som du tidligere har tilføjet og bogført.
3. Vælg **Send** \> **Original** i **Dokument**-gruppen i handlingsruden.

    > [!NOTE] 
    > Da du nu har to versioner af **Peppol Salgsfaktura (Litware)** som ER-formatkonfiguration, og ingen af versionerne har en værdi for [ikrafttrædelsesdato](general-electronic-reporting.md#component-date-effectivity), bruges den seneste version til at oprette en e-faktura.

4. Luk siden **Fritekstfaktura**.

### <a name="analyze-a-generated-e-invoice"></a>Analysere en genereret e-faktura

1. Gå til **Virksomhedsadministration** \> **Elektronisk rapportering** \> **Elektroniske rapporteringsjob**.
2. På siden **Elektroniske rapporteringsjob** skal du vælge den nyeste post, der indeholder opgavebeskrivelsen **Send eFaktura-XML**.
3. Vælg **Vis filer** for at få adgang til listen over genererede filer.
4. Vælg **Åbn** for at downloade den XML-fil, der er oprettet for e-fakturaen.
5. Analysér XML-filen med e-fakturaen. Bemærk, at i overensstemmelse med tilpasningen inkluderer kundemomsskemaet stadig den brugerdefinerede **FederalTaxID**-XML-attribut ud over **schemeID**- og **schemeAgencyID**-XML-attributterne. Desuden, fordi ændringerne i den nye version af basisformatet **UBL-salgsfaktura** blev flettet sammen med din tilpasning, er teksten i **cbc:CustomizationID**-XML-elementet ændret fra `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0` til `urn:cen.eu:en16931:2017#compliant#urn:fdc:peppol.eu:2017:poacc:billing:3.0`.

    ![Visning af den genererede XML-fil med e-faktura med tilpasninger.](./media/er-quick-start3-e-invoice3.png)

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering](general-electronic-reporting.md)
- [Hente ER-konfigurationer fra Lifecycle Services](download-electronic-reporting-configuration-lcs.md)
- [Hente ER/konfigurationer fra det globale lager til Konfigurationstjenesten](er-download-configurations-global-repo.md)
- [Opret en fritekstfaktura](../../../finance/accounts-receivable/create-free-text-invoice-new.md)
- [Oprette og arbejde med brugerdefinerede felter](../../fin-ops/get-started/user-defined-fields.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]