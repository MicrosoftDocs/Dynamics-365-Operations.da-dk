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
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a><span data-ttu-id="36f18-103">Fejlfinde datakilder for et udført ER-format for at analysere dataflow og -transformering</span><span class="sxs-lookup"><span data-stu-id="36f18-103">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="36f18-104">Når du [konfigurerer](tasks/er-format-configuration-2016-11.md) en elektronisk rapporteringsløsning (ER) til generering af udgående dokumenter, definerer du de metoder, der bruges til at få data ud af programmet og angive dem i det output, der genereres.</span><span class="sxs-lookup"><span data-stu-id="36f18-104">When you [configure](tasks/er-format-configuration-2016-11.md) an Electronic reporting (ER) solution to generate outbound documents, you define the methods that are used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="36f18-105">Livscyklusunderstøttelsen for ER-løsningen kan gøres mere effektiv, hvis din løsning består af en ER-[datamodel](general-electronic-reporting.md#DataModelComponent) og de tilhørende [tilknytningskomponenter](general-electronic-reporting.md#ModelMappingComponent) samt et ER-[format](general-electronic-reporting.md#FormatComponentOutbound) og de tilhørende tilknytningskomponenter, så modeltilknytningen er programspecifik, mens andre komponenter forbliver programagnostiske.</span><span class="sxs-lookup"><span data-stu-id="36f18-105">To make the life cycle support of the ER solution more efficient, your solution should consist of an ER [data model](general-electronic-reporting.md#DataModelComponent) and its [mapping](general-electronic-reporting.md#ModelMappingComponent) components, and also an ER [format](general-electronic-reporting.md#FormatComponentOutbound) and its mapping components, so that the model mapping is application-specific, whereas other components remain application-agnostic.</span></span> <span data-ttu-id="36f18-106">Derfor kan flere ER-komponenter [påvirke](general-electronic-reporting.md#FormatComponentOutbound) processen med at indtaste data i det genererede output.</span><span class="sxs-lookup"><span data-stu-id="36f18-106">Therefore, several ER components might [affect](general-electronic-reporting.md#FormatComponentOutbound) the process of entering data in the generated output.</span></span>

<span data-ttu-id="36f18-107">Nogle gange ser dataene i det genererede output anderledes ud end de samme data i programdatabasen.</span><span class="sxs-lookup"><span data-stu-id="36f18-107">Sometimes, the data of the generated output looks different than the same data in the application database.</span></span> <span data-ttu-id="36f18-108">I disse tilfælde skal du finde ud af, hvilken ER-komponent der er ansvarlig for datatransformationen.</span><span class="sxs-lookup"><span data-stu-id="36f18-108">In these cases, you will want to determine which ER component is responsible for the data transformation.</span></span> <span data-ttu-id="36f18-109">Funktionen til fejlfinding af ER-datakilder reducerer i høj grad den tid og de omkostninger, der bruges på denne undersøgelse.</span><span class="sxs-lookup"><span data-stu-id="36f18-109">The ER data source debugger feature significantly reduces the time and cost that are involved in this investigation.</span></span> <span data-ttu-id="36f18-110">Du kan afbryde udførelsen af et ER-format og åbne grænsefladen til fejlfinding af datakilder.</span><span class="sxs-lookup"><span data-stu-id="36f18-110">You can interrupt the execution of an ER format and open the data source debugger interface.</span></span> <span data-ttu-id="36f18-111">Her kan du gennemse de tilgængelige datakilder og vælge en enkelt datakilde til udførelse.</span><span class="sxs-lookup"><span data-stu-id="36f18-111">There, you can browse the available data sources and select an individual data source for execution.</span></span> <span data-ttu-id="36f18-112">Denne manuelle udførelse simulerer udførelsen af datakilden under den reelle kørsel af et ER-format.</span><span class="sxs-lookup"><span data-stu-id="36f18-112">This manual execution simulates the execution of the data source during the real run of an ER format.</span></span> <span data-ttu-id="36f18-113">Resultatet vises på en side, hvor du kan analysere de data, der modtages.</span><span class="sxs-lookup"><span data-stu-id="36f18-113">The result is presented on a page where you can analyze the data that is received.</span></span>

<span data-ttu-id="36f18-114">Hvis du vil aktivere funktionen til fejlfinding af datakilder, skal du angive indstillingen **Aktivér datafejlfinding ved formatkørsel** til **Ja** i ER-brugerparametrene.</span><span class="sxs-lookup"><span data-stu-id="36f18-114">To turn on the data source debugging feature, set the **Enable data debugging at format run** option to **Yes** in the ER user parameters.</span></span> <span data-ttu-id="36f18-115">Derefter kan du starte datakildefejlfinding, mens du kører et ER-format for at generere udgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="36f18-115">You can then start data source debugging while you run an ER format to generate outbound documents.</span></span> <span data-ttu-id="36f18-116">Du kan også bruge indstillingen **Start fejlfinding** til at starte datakildefejlfinding for et ER-format, der er konfigureret i [ER-operationsdesigneren](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span><span class="sxs-lookup"><span data-stu-id="36f18-116">You can also use the **Start debugging** option to initiate data source debugging for an ER format that is configured in the [ER Operation designer](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span></span>

<span data-ttu-id="36f18-117">Dette emne indeholder retningslinjer for start af datakildefejlfinding for udførte ER-formater.</span><span class="sxs-lookup"><span data-stu-id="36f18-117">This topic provides guidelines for initiating data source debugging for executed ER formats.</span></span> <span data-ttu-id="36f18-118">Det forklarer, hvordan oplysningerne kan hjælpe dig med at forstå dataflow og datatransformationer.</span><span class="sxs-lookup"><span data-stu-id="36f18-118">It explains how the information can help you understand the data flow and data transformations.</span></span> <span data-ttu-id="36f18-119">Eksemplerne i dette emne bruger forretningsprocessen for behandling af kreditorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="36f18-119">The examples in this topic use the business process for vendor payments processing.</span></span>

## <a name="limitations"></a><span data-ttu-id="36f18-120">Begrænsninger</span><span class="sxs-lookup"><span data-stu-id="36f18-120">Limitations</span></span>

<span data-ttu-id="36f18-121">Datakildefejlfindingen kan bruges til at få adgang til de datakilder, der bruges i ER-formater, som køres for at generere udgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="36f18-121">The data source debugger can be used to access the data of data sources that are used in ER formats that are run to generate outbound documents.</span></span> <span data-ttu-id="36f18-122">Den kan ikke bruges til fejlfinding af datakilder for ER-formater, der er udviklet til at fortolke indgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="36f18-122">It can't be used to debug data sources of ER formats that are designed to parse inbound documents.</span></span>

<span data-ttu-id="36f18-123">Følgende indstillinger for ER-formater er i øjeblikket ikke tilgængelige for datakildefejlfinding:</span><span class="sxs-lookup"><span data-stu-id="36f18-123">The following settings of ER formats aren't currently accessible for data source debugging:</span></span>

- <span data-ttu-id="36f18-124">Formattransformationer</span><span class="sxs-lookup"><span data-stu-id="36f18-124">Format transformations</span></span>
- <span data-ttu-id="36f18-125">Valideringsregler for format og tilknytning</span><span class="sxs-lookup"><span data-stu-id="36f18-125">Format and mapping validation rules</span></span>
- <span data-ttu-id="36f18-126">Aktivere udtryk</span><span class="sxs-lookup"><span data-stu-id="36f18-126">Enabling expressions</span></span>
- <span data-ttu-id="36f18-127">Detaljer om dataindsamling i hukommelsen</span><span class="sxs-lookup"><span data-stu-id="36f18-127">Details of in-memory data collection</span></span>

## <a name="prerequisites"></a><span data-ttu-id="36f18-128">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="36f18-128">Prerequisites</span></span>

- <span data-ttu-id="36f18-129">Hvis du vil fuldføre eksemplerne i dette emne, skal du have adgang til en af følgende [roller](../sysadmin/tasks/assign-users-security-roles.md):</span><span class="sxs-lookup"><span data-stu-id="36f18-129">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="36f18-130">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="36f18-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="36f18-131">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="36f18-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="36f18-132">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="36f18-132">System administrator</span></span>

- <span data-ttu-id="36f18-133">Virksomheden skal angives til **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="36f18-133">The company must be set to **DEMF**.</span></span>

- <span data-ttu-id="36f18-134">Følg trinnene i [Bilag 1](#appendix1) i dette emne for at downloade komponenterne for Microsoft ER-løsningen, der er nødvendige for at behandle kreditorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="36f18-134">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the Microsoft ER solution that are required to process vendor payments.</span></span>
- <span data-ttu-id="36f18-135">Følg trinnene i [Bilag 2](#appendix2) i dette emne for at forberede kreditoren til behandling af kreditorbetaling ved hjælp af den ER-løsning, du downloader.</span><span class="sxs-lookup"><span data-stu-id="36f18-135">Follow the steps in [Appendix 2](#appendix2) of this topic to prepare Accounts payable for vendor payment processing by using the ER solution that you will download.</span></span>

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a><span data-ttu-id="36f18-136">Behandle en kreditorbetaling for at få en betalingsfil</span><span class="sxs-lookup"><span data-stu-id="36f18-136">Process a vendor payment to get a payment file</span></span>

1. <span data-ttu-id="36f18-137">Følg trinnene i [Bilag 3](#appendix3) i dette emne for at behandle kreditorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="36f18-137">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>

    ![Igangværende behandling af kreditorbetaling](./media/er-data-debugger-process-payment.png)

2. <span data-ttu-id="36f18-139">Download og gem zip-filen på den lokale computer.</span><span class="sxs-lookup"><span data-stu-id="36f18-139">Download and save the zip file to your local computer.</span></span>
3. <span data-ttu-id="36f18-140">Udpak betalingsfilen **ISO20022 Credit transfer.xml** fra zip-filen.</span><span class="sxs-lookup"><span data-stu-id="36f18-140">Extract the **ISO20022 Credit transfer.xml** payment file from the zip file.</span></span>
4. <span data-ttu-id="36f18-141">Åbn den udpakkede betalingsfil med XML-filfremviseren.</span><span class="sxs-lookup"><span data-stu-id="36f18-141">Open the extracted payment file by using the XML file viewer.</span></span>

    <span data-ttu-id="36f18-142">IBAN-koden (International Bank Account Number) for kreditorbankkontoen i betalingsfilen indeholder ingen mellemrum.</span><span class="sxs-lookup"><span data-stu-id="36f18-142">In the payment file, the International Bank Account Number (IBAN) code of the vendor bank account contains no spaces.</span></span> <span data-ttu-id="36f18-143">Derfor adskiller den sig fra den værdi, der blev [angivet](#enteredIBANcode) på siden **Bankkonti**.</span><span class="sxs-lookup"><span data-stu-id="36f18-143">Therefore, it differs from the value that was [entered](#enteredIBANcode) on the **Bank accounts** page.</span></span>

    ![IBAN-kode uden mellemrum](./media/er-data-debugger-payment-file.png)

    <span data-ttu-id="36f18-145">Du kan bruge ER-datakildefejlfindingen til at finde ud af, hvilken komponent i ER-løsningen der bruges til at afkorte mellemrum i IBAN-koden.</span><span class="sxs-lookup"><span data-stu-id="36f18-145">You can use the ER data source debugger to learn which component of the ER solution is used to truncate spaces in the IBAN code.</span></span>

## <a name="turn-on-data-source-debugging"></a><span data-ttu-id="36f18-146">Slå datakildefejlfinding til</span><span class="sxs-lookup"><span data-stu-id="36f18-146">Turn on data source debugging</span></span>

1. <span data-ttu-id="36f18-147">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="36f18-147">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="36f18-148">På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.</span><span class="sxs-lookup"><span data-stu-id="36f18-148">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="36f18-149">Angiv indstillingen **Aktivér datafejlfinding ved formatkørsel** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="36f18-149">Set the **Enable data debugging at format run** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="36f18-150">Denne parameter er bruger- og virksomhedspecifik.</span><span class="sxs-lookup"><span data-stu-id="36f18-150">This parameter is user-specific and company-specific.</span></span>

    ![Dialogboksen Brugerparametre](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a><span data-ttu-id="36f18-152">Behandle en kreditorbetaling til fejlfinding</span><span class="sxs-lookup"><span data-stu-id="36f18-152">Process a vendor payment for debugging</span></span>

1. <span data-ttu-id="36f18-153">Følg trinnene i [Bilag 3](#appendix3) i dette emne for at behandle kreditorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="36f18-153">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>
2. <span data-ttu-id="36f18-154">Vælg **Ja** i dialogboksen for at bekræfte, at du vil afbryde behandlingen af kreditorbetalinger, og start i stedet datakildefejlfinding på siden **Foretag fejlfinding af datakilder**.</span><span class="sxs-lookup"><span data-stu-id="36f18-154">In the message box, select **Yes** to confirm that you want to interrupt vendor payment processing and instead start data source debugging on the **Debug Datasources** page.</span></span>

    ![Bekræftelsesdialogboks](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a><span data-ttu-id="36f18-156">Foretag fejlfinding af datakilder, der bruges i betalingsbehandling</span><span class="sxs-lookup"><span data-stu-id="36f18-156">Debug data sources that are used in payment processing</span></span>

### <a name="debug-the-model-mapping"></a><span data-ttu-id="36f18-157">Foretage fejlfinding af modeltilknytningen</span><span class="sxs-lookup"><span data-stu-id="36f18-157">Debug the model mapping</span></span>

1. <span data-ttu-id="36f18-158">På siden **Foretag fejlfinding af datakilder** skal du vælge **Modeltilknytning** i handlingsruden for at starte fejlfinding fra denne ER-komponent.</span><span class="sxs-lookup"><span data-stu-id="36f18-158">On the **Debug Datasources** page, on the Action Pane, select **Model mapping** to start to debug from this ER component.</span></span>
2. <span data-ttu-id="36f18-159">I datakilderuden til venstre skal du vælge **\$notSentTransactions** og derefter vælge **Læs alle poster**.</span><span class="sxs-lookup"><span data-stu-id="36f18-159">In the data source pane on the left, select the **\$notSentTransactions** data source, and then select **Read all records**.</span></span>

    <span data-ttu-id="36f18-160">Du kan vælge **Læs 1 post**, **Læs 10 poster**, **Læs 100 poster** eller **Læs alle poster** for at tvinge det relevante antal poster til at blive læst fra den valgte datakilde.</span><span class="sxs-lookup"><span data-stu-id="36f18-160">You can select **Read 1 record**, **Read 10 records**, **Read 100 records**, or **Read all records** to force the appropriate number of records to be read from the selected data source.</span></span> <span data-ttu-id="36f18-161">På denne måde kan du simulere adgang til datakilden fra det kørende ER-format.</span><span class="sxs-lookup"><span data-stu-id="36f18-161">In this way, you can simulate access to the data source from the running ER format.</span></span>

3. <span data-ttu-id="36f18-162">Vælg **Udvid alle** i dataruden til højre.</span><span class="sxs-lookup"><span data-stu-id="36f18-162">In the data pane on the right, select **Expand all**.</span></span>

    <span data-ttu-id="36f18-163">Du kan se, at den valgte datakilde for **Postliste**-typen indeholder en enkelt post.</span><span class="sxs-lookup"><span data-stu-id="36f18-163">You can see that the selected data source of the **Record list** type contains a single record.</span></span>

4. <span data-ttu-id="36f18-164">Udvid **\$notSentTransactions**-datakilden, og vælg den indlejrede **vendBankAccountInTransactionCompany()**-metode.</span><span class="sxs-lookup"><span data-stu-id="36f18-164">Expand the **\$notSentTransactions** data source, and select the nested **vendBankAccountInTransactionCompany()** method.</span></span>
5. <span data-ttu-id="36f18-165">Udvid **vendBankAccountInTransactionCompany()**-metoden, og vælg det indlejrede **IBAN**-felt.</span><span class="sxs-lookup"><span data-stu-id="36f18-165">Expand the **vendBankAccountInTransactionCompany()** method, and select the nested **IBAN** field.</span></span>
6. <span data-ttu-id="36f18-166">Vælg **Hent værdi**.</span><span class="sxs-lookup"><span data-stu-id="36f18-166">Select **Get value**.</span></span>

    <span data-ttu-id="36f18-167">Du kan vælge **Hent værdi** for at tvinge værdien i et valgt felt for den valgte datakilde til at blive læst.</span><span class="sxs-lookup"><span data-stu-id="36f18-167">You can select **Get value** to force the value of a selected field of the selected data source to be read.</span></span> <span data-ttu-id="36f18-168">På denne måde kan du simulere adgang til dette felt fra det kørende ER-format.</span><span class="sxs-lookup"><span data-stu-id="36f18-168">In this way, you can simulate access to this field from the running ER format.</span></span>

7. <span data-ttu-id="36f18-169">Vælg **Udvid alle**.</span><span class="sxs-lookup"><span data-stu-id="36f18-169">Select **Expand all**.</span></span>

    ![Værdien i IBAN-feltet i modeltilknytningen](./media/er-data-debugger-debugging-model-mapping.png)

    <span data-ttu-id="36f18-171">Som du kan se, er modeltilknytningen ikke ansvarlig for de afkortede mellemrum, fordi IBAN-koden, som returneres for kreditors bankkonto, indeholder mellemrum.</span><span class="sxs-lookup"><span data-stu-id="36f18-171">As you can see, the model mapping isn't responsible for the truncated spaces, because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="36f18-172">Derfor skal du fortsætte med datakildefejlfinding.</span><span class="sxs-lookup"><span data-stu-id="36f18-172">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format-mapping"></a><span data-ttu-id="36f18-173">Fejlfinde formattilknytningen</span><span class="sxs-lookup"><span data-stu-id="36f18-173">Debug the format mapping</span></span>

1. <span data-ttu-id="36f18-174">På siden **Foretag fejlfinding af datakilder** skal du vælge **Formattilknytning** i handlingsruden for at fortsætte fejlfindingen fra denne ER-komponent.</span><span class="sxs-lookup"><span data-stu-id="36f18-174">On the **Debug Datasources** page, on the Action Pane, select **Format mapping** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="36f18-175">Vælg **\$PaymentByDebtor**-kilden, og vælg derefter **Læs alle poster**.</span><span class="sxs-lookup"><span data-stu-id="36f18-175">Select the **\$PaymentByDebtor** data source, and then select **Read all records**.</span></span>
3. <span data-ttu-id="36f18-176">Udvid **\$PaymentByDebtor**.</span><span class="sxs-lookup"><span data-stu-id="36f18-176">Expand **\$PaymentByDebtor**.</span></span>
4. <span data-ttu-id="36f18-177">Udvid **\$PaymentByDebtor.Lines**, og vælg derefter **Læs alle poster**.</span><span class="sxs-lookup"><span data-stu-id="36f18-177">Expand **\$PaymentByDebtor.Lines**, and then select **Read all records**.</span></span>
5. <span data-ttu-id="36f18-178">Udvid **\$PaymentByDebtor.Lines.CreditorAccount**.</span><span class="sxs-lookup"><span data-stu-id="36f18-178">Expand **\$PaymentByDebtor.Lines.CreditorAccount**.</span></span>
6. <span data-ttu-id="36f18-179">Udvid **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, og vælg derefter **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span><span class="sxs-lookup"><span data-stu-id="36f18-179">Expand **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, and then select **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span></span>
7. <span data-ttu-id="36f18-180">Vælg **Hent værdi**.</span><span class="sxs-lookup"><span data-stu-id="36f18-180">Select **Get value**.</span></span>
8. <span data-ttu-id="36f18-181">Vælg **Udvid alle**.</span><span class="sxs-lookup"><span data-stu-id="36f18-181">Select **Expand all**.</span></span>

    ![Værdien i IBAN-feltet i formattilknytningen](./media/er-data-debugger-debugging-format-mapping.png)

    <span data-ttu-id="36f18-183">Som du kan se, er datakilderne for formattilknytningen ikke ansvarlig for de afkortede mellemrum, fordi IBAN-koden, som de returnerer for kreditors bankkonto, indeholder mellemrum.</span><span class="sxs-lookup"><span data-stu-id="36f18-183">As you can see, the data sources of the format mapping aren't responsible for the truncated spaces, because the IBAN code that they return for the vendor bank account includes spaces.</span></span> <span data-ttu-id="36f18-184">Derfor skal du fortsætte med datakildefejlfinding.</span><span class="sxs-lookup"><span data-stu-id="36f18-184">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format"></a><span data-ttu-id="36f18-185">Fejlfinde formatet</span><span class="sxs-lookup"><span data-stu-id="36f18-185">Debug the format</span></span>

1. <span data-ttu-id="36f18-186">På siden **Foretag fejlfinding af datakilder** skal du vælge **Format** i handlingsruden for at fortsætte fejlfindingen fra denne ER-komponent.</span><span class="sxs-lookup"><span data-stu-id="36f18-186">On the **Debug Datasources** page, on the Action Pane, select **Format** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="36f18-187">Udvid formatelementerne for at vælge **ISO20022CTReports** \> **XMLHeader** \> **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf**, og vælg derefter **Læs alle poster**.</span><span class="sxs-lookup"><span data-stu-id="36f18-187">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf**, and then select **Read all records**.</span></span>
3. <span data-ttu-id="36f18-188">Udvid formatelementerne for at vælge **ISO20022CTReports** \> **XMLHeader** \> **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, og vælg derefter **Læs alle poster**.</span><span class="sxs-lookup"><span data-stu-id="36f18-188">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, and then select **Read all records**.</span></span>
4. <span data-ttu-id="36f18-189">Udvid formatelementerne for at vælge **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, og vælg derefter **Hent værdi**.</span><span class="sxs-lookup"><span data-stu-id="36f18-189">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, and then select **Get value**.</span></span>
5. <span data-ttu-id="36f18-190">Vælg **Udvid alle**.</span><span class="sxs-lookup"><span data-stu-id="36f18-190">Select **Expand all**.</span></span>

    ![Værdien i IBAN-feltet i formatet](./media/er-data-debugger-debugging-format.png)

   <span data-ttu-id="36f18-192">Som du kan se, er formattilknytningen ikke ansvarlig for de afkortede mellemrum, fordi IBAN-koden, som returneres for kreditors bankkonto, indeholder mellemrum.</span><span class="sxs-lookup"><span data-stu-id="36f18-192">As you can see, the format binding isn't responsible for the truncated spaces because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="36f18-193">Derfor er **BankIBAN**-elementet konfigureret til at bruge en formattransformation, der afkorter mellemrum.</span><span class="sxs-lookup"><span data-stu-id="36f18-193">Therefore, the **BankIBAN** element is configured to use a format transformation that truncates spaces.</span></span>

6. <span data-ttu-id="36f18-194">Luk datakildefejlfindingen.</span><span class="sxs-lookup"><span data-stu-id="36f18-194">Close the data source debugger.</span></span>

### <a name="review-the-format-transformations"></a><span data-ttu-id="36f18-195">Gennemse formattransformationer</span><span class="sxs-lookup"><span data-stu-id="36f18-195">Review the format transformations</span></span>

1. <span data-ttu-id="36f18-196">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="36f18-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="36f18-197">På siden **Konfigurationer** skal du vælge **Betalingsmodel** \> **ISO20022-kreditoverførsel**.</span><span class="sxs-lookup"><span data-stu-id="36f18-197">On the **Configurations** page, select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="36f18-198">Vælg **Designer**, og udvid derefter elementerne for at vælge **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span><span class="sxs-lookup"><span data-stu-id="36f18-198">Select **Designer**, and then expand the elements to select **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span></span>

    ![BankIBAN-element på siden Formatdesigner](./media/er-data-debugger-referred-transformation.png)

    <span data-ttu-id="36f18-200">Som du kan se, er **BankIBAN**-elementet konfigureret til at bruge **fjern ikke-alfanumerisk** transformation.</span><span class="sxs-lookup"><span data-stu-id="36f18-200">As you can see, the **BankIBAN** element is configured to use the **remove not alphanumeric** transformation.</span></span>

4. <span data-ttu-id="36f18-201">Vælg fanen **Transformationer**.</span><span class="sxs-lookup"><span data-stu-id="36f18-201">Select the **Transformations** tab.</span></span>

    ![Fanen Transformationer for BankIBAN-elementet](./media/er-data-debugger-transformation.png)

    <span data-ttu-id="36f18-203">Som du kan se, er **fjern ikke-alfanumerisk** transformation konfigureret til at bruge et udtryk, der afkorter mellemrum fra den tekststreng, der er angivet.</span><span class="sxs-lookup"><span data-stu-id="36f18-203">As you can see, the **remove not alphanumeric** transformation is configured to use an expression that truncates spaces from the text string that is provided.</span></span>

## <a name="start-to-debug-in-the-operation-designer"></a><span data-ttu-id="36f18-204">Starte fejlfinding i Operationsdesigner</span><span class="sxs-lookup"><span data-stu-id="36f18-204">Start to debug in the Operation designer</span></span>

<span data-ttu-id="36f18-205">Når du konfigurerer en kladdeversion af det ER-format, der kan køres direkte fra Operationsdesigner, kan du få adgang til datakildefejlfindingen ved at vælge **Start fejlfinding** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="36f18-205">When you configure a draft version of the ER format that can be run directly from the Operation designer, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Knappen Start fejlfinding på siden Formatdesigner](./media/er-data-debugger-run-from-designer.png)

<span data-ttu-id="36f18-207">Formattilknytnings- og formatkomponenterne for det ER-format, der redigeres, er tilgængelige for fejlfinding.</span><span class="sxs-lookup"><span data-stu-id="36f18-207">The format mapping and format components of the ER format that is being edited are available for debugging.</span></span>

## <a name="start-to-debug-in-the-model-mapping-designer"></a><span data-ttu-id="36f18-208">Starte fejlfinding i Modeltilknytningsdesigner</span><span class="sxs-lookup"><span data-stu-id="36f18-208">Start to debug in the Model mapping designer</span></span>

<span data-ttu-id="36f18-209">Når du konfigurerer en ER-modeltilknytning, der kan køres fra siden **Modeltilknytning**, kan du få adgang til datakildefejlfindingen ved at vælge **Start fejlfinding** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="36f18-209">When you configure an ER model mapping that can be run from the **Model mapping** page, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Knappen Start fejlfinding på siden Modeltilknytning](./media/er-data-debugger-run-from-designer-mapping.png)

<span data-ttu-id="36f18-211">Modeltilknytningskomponenten for ER-tilknytningen, der redigeres, er tilgængelig for fejlfinding.</span><span class="sxs-lookup"><span data-stu-id="36f18-211">The model mapping component of the ER mapping that is being edited is available for debugging.</span></span>

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a><span data-ttu-id="36f18-212">Bilag 1: Få en ER-løsning</span><span class="sxs-lookup"><span data-stu-id="36f18-212">Appendix 1: Get an ER solution</span></span>

### <a name="download-an-er-solution"></a><span data-ttu-id="36f18-213">Download en ER-løsning</span><span class="sxs-lookup"><span data-stu-id="36f18-213">Download an ER solution</span></span>

<span data-ttu-id="36f18-214">Hvis du vil bruge en ER-løsning for at generere en elektronisk betalingsfil for en kreditorbetaling, der behandles, kan du [downloade](download-electronic-reporting-configuration-lcs.md) ER-betalingsformatet **ISO20022-kreditoverførsel**, der er tilgængeligt fra Delt aktivbibliotek i Microsoft Dynamics Lifecycle Services (LCS) eller det globale lager.</span><span class="sxs-lookup"><span data-stu-id="36f18-214">If you want to use an ER solution to generate an electronic payment file for a vendor payment that is processed, you can [download](download-electronic-reporting-configuration-lcs.md) the **ISO20022 Credit transfer** ER payment format that is available from the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) or from the Global repository.</span></span>

![Importere ER-betalingsformatet på siden Konfigurationslager](./media/er-data-debugger-import-from-repo.png)

<span data-ttu-id="36f18-216">Ud over det valgte ER-format, skal følgende [konfigurationer](general-electronic-reporting.md#Configuration) automatisk importeres til din Microsoft Dynamics 365 Finance-forekomst som en del af ER-løsningen **ISO20022-kreditoverførsel**:</span><span class="sxs-lookup"><span data-stu-id="36f18-216">In addition to the selected ER format, the following [configurations](general-electronic-reporting.md#Configuration) must be automatically imported into your Microsoft Dynamics 365 Finance instance as part of the **ISO20022 Credit transfer** ER solution:</span></span>

- <span data-ttu-id="36f18-217">**Betalingsmodel** [Konfiguration af ER-datamodel](general-electronic-reporting.md#DataModelComponent)</span><span class="sxs-lookup"><span data-stu-id="36f18-217">**Payment model** [ER data model configuration](general-electronic-reporting.md#DataModelComponent)</span></span>
- <span data-ttu-id="36f18-218">**ISO20022-kreditoverførsel** [ER-formatkonfiguration](general-electronic-reporting.md#FormatComponentOutbound)</span><span class="sxs-lookup"><span data-stu-id="36f18-218">**ISO20022 Credit transfer** [ER format configuration](general-electronic-reporting.md#FormatComponentOutbound)</span></span>
- <span data-ttu-id="36f18-219">**Betalingsmodel-tilknytning 1611** [Konfiguration af ER-modeltilknytning](general-electronic-reporting.md#ModelMappingComponent)</span><span class="sxs-lookup"><span data-stu-id="36f18-219">**Payment model mapping 1611** [ER model mapping configuration](general-electronic-reporting.md#ModelMappingComponent)</span></span>
- <span data-ttu-id="36f18-220">**Betalingsmodel-tilknytning til destination ISO20022** – konfiguration af ER-modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="36f18-220">**Payment model mapping to destination ISO20022** ER model mapping configuration</span></span>

<span data-ttu-id="36f18-221">Du kan finde disse konfigurationer på siden **Konfigurationer** for ER-strukturen (**Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**).</span><span class="sxs-lookup"><span data-stu-id="36f18-221">You can find these configurations on the **Configurations** page of the ER framework (**Organization administration** \> **Electronic reporting** \> **Configurations**).</span></span>

![Konfigurationer, der importeres på siden Konfigurationer](./media/er-data-debugger-configurations.png)

<span data-ttu-id="36f18-223">Hvis nogen af de tidligere angivne konfigurationer mangler i konfigurationstræet, skal du manuelt downloade dem fra LCS Delt aktivbibliotek på samme måde, som du downloadede ER-betalingsformatet **ISO20022-kreditoverførsel**.</span><span class="sxs-lookup"><span data-stu-id="36f18-223">If any of the previously listed configurations are missing in the configuration tree, you must manually download them from the LCS Shared asset library in the same way that you downloaded the **ISO20022 Credit transfer** ER payment format.</span></span>

### <a name="analyze-the-downloaded-er-solution"></a><span data-ttu-id="36f18-224">Analysere den downloadede ER-løsning</span><span class="sxs-lookup"><span data-stu-id="36f18-224">Analyze the downloaded ER solution</span></span>

#### <a name="review-the-model-mapping"></a><span data-ttu-id="36f18-225">Gennemse modeltilknytningen</span><span class="sxs-lookup"><span data-stu-id="36f18-225">Review the model mapping</span></span>

1. <span data-ttu-id="36f18-226">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="36f18-226">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="36f18-227">Vælg **Betalingsmodel** \> **Betalingsmodel-tilknytning 1611**.</span><span class="sxs-lookup"><span data-stu-id="36f18-227">Select **Payment model** \> **Payment model mapping 1611**.</span></span>
3. <span data-ttu-id="36f18-228">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="36f18-228">Select **Designer**.</span></span>
4. <span data-ttu-id="36f18-229">Vælg tilknytningsposten **Betalingsmodel-tilknytning ISO20022 CT**.</span><span class="sxs-lookup"><span data-stu-id="36f18-229">Select the **Payment model mapping ISO20022 CT** mapping record.</span></span>
5. <span data-ttu-id="36f18-230">Vælg **Designer**, og gennemse derefter den modeltilknytning, der er åbnet.</span><span class="sxs-lookup"><span data-stu-id="36f18-230">Select **Designer**, and then review the model mapping that is opened.</span></span>

    <span data-ttu-id="36f18-231">Bemærk, at feltet **Betalinger** i datamodellen er tilknyttet **\$notSentTransactions**-datakilden, der returnerer listen over kreditorbetalingslinjer, som behandles.</span><span class="sxs-lookup"><span data-stu-id="36f18-231">Notice that the **Payments** field of the data model is bound to the **\$notSentTransactions** data source that returns the list of vendor payment lines that are being processed.</span></span>

    ![Betalingsfeltet på siden Modeltilknytningsdesigner](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a><span data-ttu-id="36f18-233">Gennemse formattilknytningen</span><span class="sxs-lookup"><span data-stu-id="36f18-233">Review the format mapping</span></span>

1. <span data-ttu-id="36f18-234">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="36f18-234">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="36f18-235">Vælg **Betalingsmodel** \> **ISO20022-kreditoverførsel**.</span><span class="sxs-lookup"><span data-stu-id="36f18-235">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="36f18-236">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="36f18-236">Select **Designer**.</span></span>
4. <span data-ttu-id="36f18-237">På fanen **Tilknytning** skal du gennemse den formattilknytning, der åbnes.</span><span class="sxs-lookup"><span data-stu-id="36f18-237">On the **Mapping** tab, review the format mapping that is opened.</span></span>

    <span data-ttu-id="36f18-238">Bemærk, at elementet **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** i filen **ISO20022CTReports** \> **XMLHeader** er tilknyttet **\$PaymentByDebtor**-datakilden, der er konfigureret til at gruppere poster på datamodellens felt **Betalinger**.</span><span class="sxs-lookup"><span data-stu-id="36f18-238">Notice that the **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** element of the **ISO20022CTReports** \> **XMLHeader** file is bound to the **\$PaymentByDebtor** data source that is configured to group records of the data model's **Payments** field.</span></span>

    ![PmtInf-element på siden Formatdesigner](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a><span data-ttu-id="36f18-240">Gennemse formatet</span><span class="sxs-lookup"><span data-stu-id="36f18-240">Review the format</span></span>

1. <span data-ttu-id="36f18-241">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="36f18-241">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="36f18-242">Vælg **Betalingsmodel** \> **ISO20022-kreditoverførsel**.</span><span class="sxs-lookup"><span data-stu-id="36f18-242">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="36f18-243">Vælg **Designer**, og gennemse derefter det format, der er åbnet.</span><span class="sxs-lookup"><span data-stu-id="36f18-243">Select **Designer**, and then review the format that is opened.</span></span>

    <span data-ttu-id="36f18-244">Bemærk, at formatelementet under **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** er konfigureret til at angive IBAN-koden for kreditorkontoen i betalingsfilen.</span><span class="sxs-lookup"><span data-stu-id="36f18-244">Notice that the format element under **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** is configured to enter the IBAN code of the vendor account in the payment file.</span></span>

    ![BankIBAN-element på siden Formatdesigner](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a><span data-ttu-id="36f18-246">Bilag 2: Konfigurere kreditor</span><span class="sxs-lookup"><span data-stu-id="36f18-246">Appendix 2: Configure Accounts payable</span></span>

### <a name="modify-a-vendor-property"></a><span data-ttu-id="36f18-247">Redigere en kreditoregenskab</span><span class="sxs-lookup"><span data-stu-id="36f18-247">Modify a vendor property</span></span>

1. <span data-ttu-id="36f18-248">Gå til **Kreditor** \> **Kreditorer** \> **Alle kreditorer**.</span><span class="sxs-lookup"><span data-stu-id="36f18-248">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="36f18-249">Vælg kreditor **DE-01002**, og brug derefter handlingsruden på fanen **Kreditor** i gruppen **Konfiguration** til at vælge **Bankkonti**.</span><span class="sxs-lookup"><span data-stu-id="36f18-249">Select vendor **DE-01002**, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="36f18-250">På oversigtspanelet **Identifikation** i **IBAN**-feltet <a name="enteredIBANcode"></a>skal du skrive **GB33 BUKB 2020 1555 5555 55**.</span><span class="sxs-lookup"><span data-stu-id="36f18-250">On the **Identification** FastTab, in the **IBAN** field, <a name="enteredIBANcode"></a>enter **GB33 BUKB 2020 1555 5555 55**.</span></span>
4. <span data-ttu-id="36f18-251">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="36f18-251">Select **Save**.</span></span>

![IBAN-feltet på siden Kreditorbankkonti](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a><span data-ttu-id="36f18-253">Oprette en betalingsmåde</span><span class="sxs-lookup"><span data-stu-id="36f18-253">Set up a method of payment</span></span>

1. <span data-ttu-id="36f18-254">Gå til **Kreditor** \> **Opsætning af betaling** \> **Betalingsmåder**.</span><span class="sxs-lookup"><span data-stu-id="36f18-254">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="36f18-255">Vælg betalingsmåden **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="36f18-255">Select the **SEPA CT** payment method.</span></span>
3. <span data-ttu-id="36f18-256">På oversigtspanelet **Filformater** i sektionen **Filformater** skal du angive indstillingen **Generisk elektronisk eksportformat** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="36f18-256">On the **File formats** FastTab, in the **File formats** section, set the **Generic electronic Export format** option to **Yes**.</span></span>
4. <span data-ttu-id="36f18-257">I feltet **Eksportér formatkonfiguration** skal du vælge ER-formatet **ISO20022-overførsel**.</span><span class="sxs-lookup"><span data-stu-id="36f18-257">In the **Export format configuration** field, select the **ISO20022 Credit transfer** ER format.</span></span>
5. <span data-ttu-id="36f18-258">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="36f18-258">Select **Save**.</span></span>

![Filformatindstillinger på siden Betalingsmåder](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a><span data-ttu-id="36f18-260">Tilføje en kreditorbetaling</span><span class="sxs-lookup"><span data-stu-id="36f18-260">Add a vendor payment</span></span>

1. <span data-ttu-id="36f18-261">Gå til **Kreditor** \> **Betalinger** \> **Betalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="36f18-261">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="36f18-262">Tilføje en ny betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="36f18-262">Add a new payment journal.</span></span>
3. <span data-ttu-id="36f18-263">Vælg **Linjer**, og tilføj en ny betalingslinje.</span><span class="sxs-lookup"><span data-stu-id="36f18-263">Select **Lines**, and add a new payment line.</span></span>
4. <span data-ttu-id="36f18-264">Vælg kreditoren **DE-01002** i feltet **Konto**.</span><span class="sxs-lookup"><span data-stu-id="36f18-264">In the **Account** field, select vendor **DE-01002**.</span></span>
5. <span data-ttu-id="36f18-265">Angiv en værdi i feltet **Debet**.</span><span class="sxs-lookup"><span data-stu-id="36f18-265">In the **Debit** field, enter a value.</span></span>
6. <span data-ttu-id="36f18-266">Vælg **SEPA CT** i feltet **Betalingsmåde**.</span><span class="sxs-lookup"><span data-stu-id="36f18-266">In the **Method of payment** field, select **SEPA CT**.</span></span>
7. <span data-ttu-id="36f18-267">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="36f18-267">Select **Save**.</span></span>

![Kreditorbetaling tilføjet på siden Kreditorbetalinger](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a><span data-ttu-id="36f18-269">Bilag 3: Behandle en kreditorbetaling</span><span class="sxs-lookup"><span data-stu-id="36f18-269">Appendix 3: Process a vendor payment</span></span>

1. <span data-ttu-id="36f18-270">Gå til **Kreditor** \> **Betalinger** \> **Betalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="36f18-270">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="36f18-271">På siden **Kreditorbetalingskladde** skal du vælge den betalingskladde, du oprettede tidligere, og derefter vælge **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="36f18-271">On the **Vendor payment journal** page, select the payment journal that you previously created, and then select **Lines**.</span></span>
3. <span data-ttu-id="36f18-272">Vælg betalingslinjen, og vælg derefter **Betalingsstatus** \> **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="36f18-272">Select the payment line, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="36f18-273">Vælg **Opret betalinger**.</span><span class="sxs-lookup"><span data-stu-id="36f18-273">Select **Generate payments**.</span></span>
5. <span data-ttu-id="36f18-274">Vælg **SEPA CT** i feltet **Betalingsmåde**.</span><span class="sxs-lookup"><span data-stu-id="36f18-274">In the **Method of payment** field, select **SEPA CT**.</span></span>
6. <span data-ttu-id="36f18-275">Vælg **DEMF OPER** i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="36f18-275">In the **Bank account** field, select **DEMF OPER**.</span></span>
7. <span data-ttu-id="36f18-276">Vælg **OK** i dialogboksen **Opret betalinger**.</span><span class="sxs-lookup"><span data-stu-id="36f18-276">In the **Generate payments** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="36f18-277">Vælg **OK** i dialogboksen **Elektroniske rapporteringsparametre**.</span><span class="sxs-lookup"><span data-stu-id="36f18-277">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
