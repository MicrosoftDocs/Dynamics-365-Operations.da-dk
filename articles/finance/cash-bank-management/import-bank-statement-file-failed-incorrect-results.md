---
title: Fejlfinding af filimport af bankkontoudtog
description: Det er vigtigt, at kontoudtogsfilen fra banken svarer til det layout, som Microsoft Dynamics 365 Finance understøtter. På grund af strenge standarder for bankkontoudtog fungerer de fleste integrationer korrekt. Men nogle gange kan udtogsfilen ikke importeres eller giver forkerte resultater. Normalt skyldes disse problemer små forskelle i bankkontoudtogsfilen. Denne artikel forklarer, hvordan du løser disse forskelle og løser problemerne.
author: panolte
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac82a269e8f7773c58517ef017576c82c52039cb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253957"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="aeb57-107">Fejlfinding af filimport af bankkontoudtog</span><span class="sxs-lookup"><span data-stu-id="aeb57-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aeb57-108">Det er vigtigt, at kontoudtogsfilen fra banken svarer til det layout, som Microsoft Dynamics 365 Finance understøtter.</span><span class="sxs-lookup"><span data-stu-id="aeb57-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="aeb57-109">På grund af strenge standarder for bankkontoudtog fungerer de fleste integrationer korrekt.</span><span class="sxs-lookup"><span data-stu-id="aeb57-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="aeb57-110">Men nogle gange kan udtogsfilen ikke importeres eller giver forkerte resultater.</span><span class="sxs-lookup"><span data-stu-id="aeb57-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="aeb57-111">Normalt skyldes disse problemer små forskelle i bankkontoudtogsfilen.</span><span class="sxs-lookup"><span data-stu-id="aeb57-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="aeb57-112">Denne artikel forklarer, hvordan du løser disse forskelle og løser problemerne.</span><span class="sxs-lookup"><span data-stu-id="aeb57-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="aeb57-113">Hvad er fejlen?</span><span class="sxs-lookup"><span data-stu-id="aeb57-113">What is the error?</span></span>
------------------

<span data-ttu-id="aeb57-114">Når du forsøger at importere en bankkontoudtogsfil, skal du gå til jobhistorikken for Datastyring og se udførelsesoplysningerne for at finde fejlen.</span><span class="sxs-lookup"><span data-stu-id="aeb57-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="aeb57-115">Fejlen gør det lettere at udpege kontoudtoget, balancen eller kontoudtogslinjen.</span><span class="sxs-lookup"><span data-stu-id="aeb57-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="aeb57-116">Det er dog ikke sandsynligt, at du får tilstrækkelige oplysninger til at identificere det felt eller element, der er årsag til problemet.</span><span class="sxs-lookup"><span data-stu-id="aeb57-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="aeb57-117">Hvad er forskellene?</span><span class="sxs-lookup"><span data-stu-id="aeb57-117">What are the differences?</span></span>
<span data-ttu-id="aeb57-118">Sammenlign layoutdefinitionen for bankfilen med finansimportdefinitionen, og bemærk eventuelle forskelle i felter og elementer.</span><span class="sxs-lookup"><span data-stu-id="aeb57-118">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="aeb57-119">Sammenlign kontoudtogsfilen fra banken med den relaterede finanseksempelfil.</span><span class="sxs-lookup"><span data-stu-id="aeb57-119">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="aeb57-120">I ISO20022-filerne bør eventuelle forskelle være lette at se.</span><span class="sxs-lookup"><span data-stu-id="aeb57-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="aeb57-121">Tidszoneforskelle på importerede bankkontoudtog</span><span class="sxs-lookup"><span data-stu-id="aeb57-121">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="aeb57-122">Dato- og klokkeslætsværdierne i importfilen kan være forskellige fra de dato- og klokkeslætsværdier, der vises i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="aeb57-122">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="aeb57-123">Hvis du vil undgå denne uoverensstemmelse, skal du angive en tidszoneindstilling på siden **Konfigurer datakilder**.</span><span class="sxs-lookup"><span data-stu-id="aeb57-123">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="aeb57-124">Se [Konfigurere importprocessen for avanceret bankafstemning](set-up-advanced-bank-reconciliation-import-process.md) for at få flere oplysninger om angivelse af en indstilling for tidszone.</span><span class="sxs-lookup"><span data-stu-id="aeb57-124">See [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md) for more information about entering a time zone preference.</span></span>

## <a name="transformations"></a><span data-ttu-id="aeb57-125">Transformationer</span><span class="sxs-lookup"><span data-stu-id="aeb57-125">Transformations</span></span>
<span data-ttu-id="aeb57-126">Ændringen foretages typisk i en af tre transformationer.</span><span class="sxs-lookup"><span data-stu-id="aeb57-126">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="aeb57-127">Hver transformation er skrevet for en bestemt standard.</span><span class="sxs-lookup"><span data-stu-id="aeb57-127">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="aeb57-128">Ressourcenavn</span><span class="sxs-lookup"><span data-stu-id="aeb57-128">Resource name</span></span>                                         | <span data-ttu-id="aeb57-129">Filnavn</span><span class="sxs-lookup"><span data-stu-id="aeb57-129">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="aeb57-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="aeb57-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="aeb57-131">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="aeb57-131">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="aeb57-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="aeb57-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="aeb57-133">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="aeb57-133">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="aeb57-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="aeb57-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="aeb57-135">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="aeb57-135">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="aeb57-136">Fejlfinding af transformationer</span><span class="sxs-lookup"><span data-stu-id="aeb57-136">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="aeb57-137">Justere BAI2- og MT940-filerne</span><span class="sxs-lookup"><span data-stu-id="aeb57-137">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="aeb57-138">BAI2- og MT940-filerne er tekstbaserede filer og kræver en justering for at aktivere fejlfinding af Extensible Stylesheet Language Transformations (XSLT).</span><span class="sxs-lookup"><span data-stu-id="aeb57-138">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="aeb57-139">Denne justering foretages, når en fil importeres.</span><span class="sxs-lookup"><span data-stu-id="aeb57-139">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="aeb57-140">Opret en XML-fil, og kopiér følgende tekst ind i den.</span><span class="sxs-lookup"><span data-stu-id="aeb57-140">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="aeb57-141">Kopiér indholdet af bankkontoudtogsfilen og indsæt det i XML-filen, så det erstatter **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="aeb57-141">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="aeb57-142">Foretage fejlfinding af XSLT-transformationen</span><span class="sxs-lookup"><span data-stu-id="aeb57-142">Debug the XSLT</span></span>

<span data-ttu-id="aeb57-143">Yderligere oplysninger finder du i <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="aeb57-143">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="aeb57-144">Start Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="aeb57-144">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="aeb57-145">Opret en konsolansøgning.</span><span class="sxs-lookup"><span data-stu-id="aeb57-145">Create a console application.</span></span>
3.  <span data-ttu-id="aeb57-146">Åbn den relevante XSLT-transformation.</span><span class="sxs-lookup"><span data-stu-id="aeb57-146">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="aeb57-147">Klik på XLST-transformationen og dens egenskabsside.</span><span class="sxs-lookup"><span data-stu-id="aeb57-147">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="aeb57-148">Angiv input til lokationen for bankkontoudtogsfilen.</span><span class="sxs-lookup"><span data-stu-id="aeb57-148">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="aeb57-149">Definer en lokation og et filnavn til outputtet.</span><span class="sxs-lookup"><span data-stu-id="aeb57-149">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="aeb57-150">Angiv de nødvendige pausepunkter.</span><span class="sxs-lookup"><span data-stu-id="aeb57-150">Set the required break points.</span></span>
8.  <span data-ttu-id="aeb57-151">Åbn menuen, og klik på **XML** &gt; **Start fejlfinding af XSLT**.</span><span class="sxs-lookup"><span data-stu-id="aeb57-151">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="aeb57-152">Formatér XLST-outputtet</span><span class="sxs-lookup"><span data-stu-id="aeb57-152">Format the XSLT output</span></span>

<span data-ttu-id="aeb57-153">Når transformationen er i gang, oprettes der en outputfil, som du kan se i Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="aeb57-153">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="aeb57-154">Brug Ctrl+A, Ctrl+K og Ctrl+D til hurtigt at formatere outputfilen.</span><span class="sxs-lookup"><span data-stu-id="aeb57-154">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="aeb57-155">Justere transformationen</span><span class="sxs-lookup"><span data-stu-id="aeb57-155">Adjust the transformation</span></span>

<span data-ttu-id="aeb57-156">Juster transformationen for at få det relevante felt eller element i bankkontoudtogsfilen.</span><span class="sxs-lookup"><span data-stu-id="aeb57-156">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="aeb57-157">Derefter skal du knytte feltet eller elementet til det relevante Finance-element.</span><span class="sxs-lookup"><span data-stu-id="aeb57-157">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="aeb57-158">Indikator for debet/kredit</span><span class="sxs-lookup"><span data-stu-id="aeb57-158">Debit/credit indicator</span></span>

<span data-ttu-id="aeb57-159">Nogle gange kan debiteringer importeres som kreditter, og kreditter kan importeres som debet.</span><span class="sxs-lookup"><span data-stu-id="aeb57-159">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="aeb57-160">Du kan løse dette problem ved at ændre den relevante XSLT.</span><span class="sxs-lookup"><span data-stu-id="aeb57-160">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="aeb57-161">Hvis bankkontoudtog kommer fra flere banker, skal du kontrollere, at de alle bruger samme fremgangsmåde for debet/kredit, eller oprette separate transformationer.</span><span class="sxs-lookup"><span data-stu-id="aeb57-161">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="aeb57-162">BAI2XML-til-Reconciliation.xlst GetAmountCreditDebitIndicator-skabelon</span><span class="sxs-lookup"><span data-stu-id="aeb57-162">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="aeb57-163">ISO20022XML-til-Reconcilation.xslt GetCreditDebit-skabelon</span><span class="sxs-lookup"><span data-stu-id="aeb57-163">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="aeb57-164">MT940XML-til-Reconcilation.xslt GetCreditDebitIndicator-skabelon</span><span class="sxs-lookup"><span data-stu-id="aeb57-164">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="aeb57-165">Eksempler på bankkontoudtogsformater og tekniske layout</span><span class="sxs-lookup"><span data-stu-id="aeb57-165">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="aeb57-166">Følgende tabel viser eksempler på de tekniske layoutdefinitioner for importfiler til avanceret bankafstemning og tre relaterede eksempelfiler på bankkontoudtog.</span><span class="sxs-lookup"><span data-stu-id="aeb57-166">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="aeb57-167">Du kan hente eksempelfiler og tekniske layout her: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="aeb57-167">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="aeb57-168">Teknisk layoutdefinition</span><span class="sxs-lookup"><span data-stu-id="aeb57-168">Technical layout definition</span></span>                             | <span data-ttu-id="aeb57-169">Eksempelfil med bankkontoudtog</span><span class="sxs-lookup"><span data-stu-id="aeb57-169">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="aeb57-170">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="aeb57-170">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="aeb57-171">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="aeb57-171">MT940StatementExample</span></span>                |
| <span data-ttu-id="aeb57-172">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="aeb57-172">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="aeb57-173">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="aeb57-173">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="aeb57-174">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="aeb57-174">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="aeb57-175">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="aeb57-175">BAI2StatementExample</span></span>                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]