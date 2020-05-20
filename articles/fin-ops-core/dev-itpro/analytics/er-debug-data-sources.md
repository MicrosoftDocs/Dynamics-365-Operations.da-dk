---
title: Fejlfinde datakilder for et udført ER-format for at analysere dataflow og -transformering
description: Dette emne forklarer, hvordan du kan foretage fejlfinding af datakilder i et udført ER-format for at få en bedre forståelse for det konfigurerede dataflow.
author: NickSelin
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 5b51c4beac0ddf1e2b53fe300e10c0f608e5d1e1
ms.sourcegitcommit: 153bb33722c02501bf7bcfd56ac887602d5dfbd3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2020
ms.locfileid: "3318660"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a>Fejlfinde datakilder for et udført ER-format for at analysere dataflow og -transformering

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

Når du [konfigurerer](tasks/er-format-configuration-2016-11.md) en elektronisk rapporteringsløsning (ER) til generering af udgående dokumenter, definerer du de metoder, der bruges til at få data ud af programmet og angive dem i det output, der genereres. Livscyklusunderstøttelsen for ER-løsningen kan gøres mere effektiv, hvis din løsning består af en ER-[datamodel](general-electronic-reporting.md#DataModelComponent) og de tilhørende [tilknytningskomponenter](general-electronic-reporting.md#ModelMappingComponent) samt et ER-[format](general-electronic-reporting.md#FormatComponentOutbound) og de tilhørende tilknytningskomponenter, så modeltilknytningen er programspecifik, mens andre komponenter forbliver programagnostiske. Derfor kan flere ER-komponenter [påvirke](general-electronic-reporting.md#FormatComponentOutbound) processen med at indtaste data i det genererede output.

Nogle gange ser dataene i det genererede output anderledes ud end de samme data i programdatabasen. I disse tilfælde skal du finde ud af, hvilken ER-komponent der er ansvarlig for datatransformationen. Funktionen til fejlfinding af ER-datakilder reducerer i høj grad den tid og de omkostninger, der bruges på denne undersøgelse. Du kan afbryde udførelsen af et ER-format og åbne grænsefladen til fejlfinding af datakilder. Her kan du gennemse de tilgængelige datakilder og vælge en enkelt datakilde til udførelse. Denne manuelle udførelse simulerer udførelsen af datakilden under den reelle kørsel af et ER-format. Resultatet vises på en side, hvor du kan analysere de data, der modtages.

Hvis du vil aktivere funktionen til fejlfinding af datakilder, skal du angive indstillingen **Aktivér datafejlfinding ved formatkørsel** til **Ja** i ER-brugerparametrene. Derefter kan du starte datakildefejlfinding, mens du kører et ER-format for at generere udgående dokumenter. Du kan også bruge indstillingen **Start fejlfinding** til at starte datakildefejlfinding for et ER-format, der er konfigureret i [ER-operationsdesigneren](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).

Dette emne indeholder retningslinjer for start af datakildefejlfinding for udførte ER-formater. Det forklarer, hvordan oplysningerne kan hjælpe dig med at forstå dataflow og datatransformationer. Eksemplerne i dette emne bruger forretningsprocessen for behandling af kreditorbetalinger.

## <a name="limitations"></a>Begrænsninger

Datakildefejlfindingen kan bruges til at få adgang til de datakilder, der bruges i ER-formater, som køres for at generere udgående dokumenter. Den kan ikke bruges til fejlfinding af datakilder for ER-formater, der er udviklet til at fortolke indgående dokumenter.

Følgende indstillinger for ER-formater er i øjeblikket ikke tilgængelige for datakildefejlfinding:

- Formattransformationer
- Valideringsregler for format og tilknytning
- Aktivere udtryk
- Detaljer om dataindsamling i hukommelsen

## <a name="prerequisites"></a>Forudsætninger

- Hvis du vil fuldføre eksemplerne i dette emne, skal du have adgang til en af følgende [roller](../sysadmin/tasks/assign-users-security-roles.md):

    - Udvikler til elektronisk rapportering
    - Funktionel konsulent i elektronisk rapportering
    - Systemadministrator

- Virksomheden skal angives til **DEMF**.

- Følg trinnene i [Bilag 1](#appendix1) i dette emne for at downloade komponenterne for Microsoft ER-løsningen, der er nødvendige for at behandle kreditorbetalinger.
- Følg trinnene i [Bilag 2](#appendix2) i dette emne for at forberede kreditoren til behandling af kreditorbetaling ved hjælp af den ER-løsning, du downloader.

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a>Behandle en kreditorbetaling for at få en betalingsfil

1. Følg trinnene i [Bilag 3](#appendix3) i dette emne for at behandle kreditorbetalinger.

    ![Igangværende behandling af kreditorbetaling](./media/er-data-debugger-process-payment.png)

2. Download og gem zip-filen på den lokale computer.
3. Udpak betalingsfilen **ISO20022 Credit transfer.xml** fra zip-filen.
4. Åbn den udpakkede betalingsfil med XML-filfremviseren.

    IBAN-koden (International Bank Account Number) for kreditorbankkontoen i betalingsfilen indeholder ingen mellemrum. Derfor adskiller den sig fra den værdi, der blev [angivet](#enteredIBANcode) på siden **Bankkonti**.

    ![IBAN-kode uden mellemrum](./media/er-data-debugger-payment-file.png)

    Du kan bruge ER-datakildefejlfindingen til at finde ud af, hvilken komponent i ER-løsningen der bruges til at afkorte mellemrum i IBAN-koden.

## <a name="turn-on-data-source-debugging"></a>Slå datakildefejlfinding til

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
3. Angiv indstillingen **Aktivér datafejlfinding ved formatkørsel** til **Ja**.

    > [!NOTE]
    > Denne parameter er bruger- og virksomhedspecifik.

    ![Dialogboksen Brugerparametre](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a>Behandle en kreditorbetaling til fejlfinding

1. Følg trinnene i [Bilag 3](#appendix3) i dette emne for at behandle kreditorbetalinger.
2. Vælg **Ja** i dialogboksen for at bekræfte, at du vil afbryde behandlingen af kreditorbetalinger, og start i stedet datakildefejlfinding på siden **Foretag fejlfinding af datakilder**.

    ![Bekræftelsesdialogboks](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a>Foretag fejlfinding af datakilder, der bruges i betalingsbehandling

### <a name="debug-the-model-mapping"></a>Foretage fejlfinding af modeltilknytningen

1. På siden **Foretag fejlfinding af datakilder** skal du vælge **Modeltilknytning** i handlingsruden for at starte fejlfinding fra denne ER-komponent.
2. I datakilderuden til venstre skal du vælge **\$notSentTransactions** og derefter vælge **Læs alle poster**.

    Du kan vælge **Læs 1 post**, **Læs 10 poster**, **Læs 100 poster** eller **Læs alle poster** for at tvinge det relevante antal poster til at blive læst fra den valgte datakilde. På denne måde kan du simulere adgang til datakilden fra det kørende ER-format.

3. Vælg **Udvid alle** i dataruden til højre.

    Du kan se, at den valgte datakilde for **Postliste**-typen indeholder en enkelt post.

4. Udvid **\$notSentTransactions**-datakilden, og vælg den indlejrede **vendBankAccountInTransactionCompany()**-metode.
5. Udvid **vendBankAccountInTransactionCompany()**-metoden, og vælg det indlejrede **IBAN**-felt.
6. Vælg **Hent værdi**.

    Du kan vælge **Hent værdi** for at tvinge værdien i et valgt felt for den valgte datakilde til at blive læst. På denne måde kan du simulere adgang til dette felt fra det kørende ER-format.

7. Vælg **Udvid alle**.

    ![Værdien i IBAN-feltet i modeltilknytningen](./media/er-data-debugger-debugging-model-mapping.png)

    Som du kan se, er modeltilknytningen ikke ansvarlig for de afkortede mellemrum, fordi IBAN-koden, som returneres for kreditors bankkonto, indeholder mellemrum. Derfor skal du fortsætte med datakildefejlfinding.

### <a name="debug-the-format-mapping"></a>Fejlfinde formattilknytningen

1. På siden **Foretag fejlfinding af datakilder** skal du vælge **Formattilknytning** i handlingsruden for at fortsætte fejlfindingen fra denne ER-komponent.
2. Vælg **\$PaymentByDebtor**-kilden, og vælg derefter **Læs alle poster**.
3. Udvid **\$PaymentByDebtor**.
4. Udvid **\$PaymentByDebtor.Lines**, og vælg derefter **Læs alle poster**.
5. Udvid **\$PaymentByDebtor.Lines.CreditorAccount**.
6. Udvid **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, og vælg derefter **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.
7. Vælg **Hent værdi**.
8. Vælg **Udvid alle**.

    ![Værdien i IBAN-feltet i formattilknytningen](./media/er-data-debugger-debugging-format-mapping.png)

    Som du kan se, er datakilderne for formattilknytningen ikke ansvarlig for de afkortede mellemrum, fordi IBAN-koden, som de returnerer for kreditors bankkonto, indeholder mellemrum. Derfor skal du fortsætte med datakildefejlfinding.

### <a name="debug-the-format"></a>Fejlfinde formatet

1. På siden **Foretag fejlfinding af datakilder** skal du vælge **Format** i handlingsruden for at fortsætte fejlfindingen fra denne ER-komponent.
2. Udvid formatelementerne for at vælge **ISO20022CTReports** \> **XMLHeader** \> **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf**, og vælg derefter **Læs alle poster**.
3. Udvid formatelementerne for at vælge **ISO20022CTReports** \> **XMLHeader** \> **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, og vælg derefter **Læs alle poster**.
4. Udvid formatelementerne for at vælge **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, og vælg derefter **Hent værdi**.
5. Vælg **Udvid alle**.

    ![Værdien i IBAN-feltet i formatet](./media/er-data-debugger-debugging-format.png)

   Som du kan se, er formattilknytningen ikke ansvarlig for de afkortede mellemrum, fordi IBAN-koden, som returneres for kreditors bankkonto, indeholder mellemrum. Derfor er **BankIBAN**-elementet konfigureret til at bruge en formattransformation, der afkorter mellemrum.

6. Luk datakildefejlfindingen.

### <a name="review-the-format-transformations"></a>Gennemse formattransformationer

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du vælge **Betalingsmodel** \> **ISO20022-kreditoverførsel**.
3. Vælg **Designer**, og udvid derefter elementerne for at vælge **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.

    ![BankIBAN-element på siden Formatdesigner](./media/er-data-debugger-referred-transformation.png)

    Som du kan se, er **BankIBAN**-elementet konfigureret til at bruge **fjern ikke-alfanumerisk** transformation.

4. Vælg fanen **Transformationer**.

    ![Fanen Transformationer for BankIBAN-elementet](./media/er-data-debugger-transformation.png)

    Som du kan se, er **fjern ikke-alfanumerisk** transformation konfigureret til at bruge et udtryk, der afkorter mellemrum fra den tekststreng, der er angivet.

## <a name="start-to-debug-in-the-operation-designer"></a>Starte fejlfinding i Operationsdesigner

Når du konfigurerer en kladdeversion af det ER-format, der kan køres direkte fra Operationsdesigner, kan du få adgang til datakildefejlfindingen ved at vælge **Start fejlfinding** i handlingsruden.

![Knappen Start fejlfinding på siden Formatdesigner](./media/er-data-debugger-run-from-designer.png)

Formattilknytnings- og formatkomponenterne for det ER-format, der redigeres, er tilgængelige for fejlfinding.

## <a name="start-to-debug-in-the-model-mapping-designer"></a>Starte fejlfinding i Modeltilknytningsdesigner

Når du konfigurerer en ER-modeltilknytning, der kan køres fra siden **Modeltilknytning**, kan du få adgang til datakildefejlfindingen ved at vælge **Start fejlfinding** i handlingsruden.

![Knappen Start fejlfinding på siden Modeltilknytning](./media/er-data-debugger-run-from-designer-mapping.png)

Modeltilknytningskomponenten for ER-tilknytningen, der redigeres, er tilgængelig for fejlfinding.

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a>Bilag 1: Få en ER-løsning

### <a name="download-an-er-solution"></a>Download en ER-løsning

Hvis du vil bruge en ER-løsning for at generere en elektronisk betalingsfil for en kreditorbetaling, der behandles, kan du [downloade](download-electronic-reporting-configuration-lcs.md) ER-betalingsformatet **ISO20022-kreditoverførsel**, der er tilgængeligt fra Delt aktivbibliotek i Microsoft Dynamics Lifecycle Services (LCS) eller det globale lager.

![Importere ER-betalingsformatet på siden Konfigurationslager](./media/er-data-debugger-import-from-repo.png)

Ud over det valgte ER-format, skal følgende [konfigurationer](general-electronic-reporting.md#Configuration) automatisk importeres til din Microsoft Dynamics 365 Finance-forekomst som en del af ER-løsningen **ISO20022-kreditoverførsel**:

- **Betalingsmodel** [Konfiguration af ER-datamodel](general-electronic-reporting.md#DataModelComponent)
- **ISO20022-kreditoverførsel** [ER-formatkonfiguration](general-electronic-reporting.md#FormatComponentOutbound)
- **Betalingsmodel-tilknytning 1611** [Konfiguration af ER-modeltilknytning](general-electronic-reporting.md#ModelMappingComponent)
- **Betalingsmodel-tilknytning til destination ISO20022** – konfiguration af ER-modeltilknytning

Du kan finde disse konfigurationer på siden **Konfigurationer** for ER-strukturen (**Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**).

![Konfigurationer, der importeres på siden Konfigurationer](./media/er-data-debugger-configurations.png)

Hvis nogen af de tidligere angivne konfigurationer mangler i konfigurationstræet, skal du manuelt downloade dem fra LCS Delt aktivbibliotek på samme måde, som du downloadede ER-betalingsformatet **ISO20022-kreditoverførsel**.

### <a name="analyze-the-downloaded-er-solution"></a>Analysere den downloadede ER-løsning

#### <a name="review-the-model-mapping"></a>Gennemse modeltilknytningen

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. Vælg **Betalingsmodel** \> **Betalingsmodel-tilknytning 1611**.
3. Vælg **Designer**.
4. Vælg tilknytningsposten **Betalingsmodel-tilknytning ISO20022 CT**.
5. Vælg **Designer**, og gennemse derefter den modeltilknytning, der er åbnet.

    Bemærk, at feltet **Betalinger** i datamodellen er tilknyttet **\$notSentTransactions**-datakilden, der returnerer listen over kreditorbetalingslinjer, som behandles.

    ![Betalingsfeltet på siden Modeltilknytningsdesigner](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a>Gennemse formattilknytningen

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. Vælg **Betalingsmodel** \> **ISO20022-kreditoverførsel**.
3. Vælg **Designer**.
4. På fanen **Tilknytning** skal du gennemse den formattilknytning, der åbnes.

    Bemærk, at elementet **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** i filen **ISO20022CTReports** \> **XMLHeader** er tilknyttet **\$PaymentByDebtor**-datakilden, der er konfigureret til at gruppere poster på datamodellens felt **Betalinger**.

    ![PmtInf-element på siden Formatdesigner](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a>Gennemse formatet

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. Vælg **Betalingsmodel** \> **ISO20022-kreditoverførsel**.
3. Vælg **Designer**, og gennemse derefter det format, der er åbnet.

    Bemærk, at formatelementet under **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** er konfigureret til at angive IBAN-koden for kreditorkontoen i betalingsfilen.

    ![BankIBAN-element på siden Formatdesigner](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a>Bilag 2: Konfigurere kreditor

### <a name="modify-a-vendor-property"></a>Redigere en kreditoregenskab

1. Gå til **Kreditor** \> **Kreditorer** \> **Alle kreditorer**.
2. Vælg kreditor **DE-01002**, og brug derefter handlingsruden på fanen **Kreditor** i gruppen **Konfiguration** til at vælge **Bankkonti**.
3. På oversigtspanelet **Identifikation** i **IBAN**-feltet <a name="enteredIBANcode"></a>skal du skrive **GB33 BUKB 2020 1555 5555 55**.
4. Vælg **Gem**.

![IBAN-feltet på siden Kreditorbankkonti](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a>Oprette en betalingsmåde

1. Gå til **Kreditor** \> **Opsætning af betaling** \> **Betalingsmåder**.
2. Vælg betalingsmåden **SEPA CT**.
3. På oversigtspanelet **Filformater** i sektionen **Filformater** skal du angive indstillingen **Generisk elektronisk eksportformat** til **Ja**.
4. I feltet **Eksportér formatkonfiguration** skal du vælge ER-formatet **ISO20022-overførsel**.
5. Vælg **Gem**.

![Filformatindstillinger på siden Betalingsmåder](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a>Tilføje en kreditorbetaling

1. Gå til **Kreditor** \> **Betalinger** \> **Betalingskladde**.
2. Tilføje en ny betalingskladde.
3. Vælg **Linjer**, og tilføj en ny betalingslinje.
4. Vælg kreditoren **DE-01002** i feltet **Konto**.
5. Angiv en værdi i feltet **Debet**.
6. Vælg **SEPA CT** i feltet **Betalingsmåde**.
7. Vælg **Gem**.

![Kreditorbetaling tilføjet på siden Kreditorbetalinger](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a>Bilag 3: Behandle en kreditorbetaling

1. Gå til **Kreditor** \> **Betalinger** \> **Betalingskladde**.
2. På siden **Kreditorbetalingskladde** skal du vælge den betalingskladde, du oprettede tidligere, og derefter vælge **Linjer**.
3. Vælg betalingslinjen, og vælg derefter **Betalingsstatus** \> **Ingen**.
4. Vælg **Opret betalinger**.
5. Vælg **SEPA CT** i feltet **Betalingsmåde**.
6. Vælg **DEMF OPER** i feltet **Bankkonto**.
7. Vælg **OK** i dialogboksen **Opret betalinger**.
8. Vælg **OK** i dialogboksen **Elektroniske rapporteringsparametre**.
