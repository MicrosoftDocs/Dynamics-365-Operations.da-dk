---
title: Fejlfinding af filimport af bankkontoudtog
description: "Det er vigtigt, at bankkontoudtogsfilen fra banken svarer til det layout, som Microsoft Dynamics 365 for Finance and Operations, Enterprise edition understøtter. På grund af strenge standarder for bankkontoudtog fungerer de fleste integrationer korrekt. Men nogle gange kan udtogsfilen ikke importeres eller giver forkerte resultater. Normalt skyldes disse problemer små forskelle i bankkontoudtogsfilen. Denne artikel forklarer, hvordan du løser disse forskelle og løser problemerne."
author: twheeloc
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: b1f772d9c6393df97a3008f60c5c5fc2e802b853
ms.contentlocale: da-dk
ms.lasthandoff: 01/17/2018

---

# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="538af-107">Fejlfinding af filimport af bankkontoudtog</span><span class="sxs-lookup"><span data-stu-id="538af-107">Bank statement file import troubleshooting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="538af-108">Det er vigtigt, at bankkontoudtogsfilen fra banken svarer til det layout, som Microsoft Dynamics 365 for Finance and Operations, Enterprise edition understøtter.</span><span class="sxs-lookup"><span data-stu-id="538af-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 for Finance and Operations, Enterprise edition supports.</span></span> <span data-ttu-id="538af-109">På grund af strenge standarder for bankkontoudtog fungerer de fleste integrationer korrekt.</span><span class="sxs-lookup"><span data-stu-id="538af-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="538af-110">Men nogle gange kan udtogsfilen ikke importeres eller giver forkerte resultater.</span><span class="sxs-lookup"><span data-stu-id="538af-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="538af-111">Normalt skyldes disse problemer små forskelle i bankkontoudtogsfilen.</span><span class="sxs-lookup"><span data-stu-id="538af-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="538af-112">Denne artikel forklarer, hvordan du løser disse forskelle og løser problemerne.</span><span class="sxs-lookup"><span data-stu-id="538af-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="538af-113">Hvad er fejlen?</span><span class="sxs-lookup"><span data-stu-id="538af-113">What is the error?</span></span>
------------------

<span data-ttu-id="538af-114">Når du forsøger at importere en bankkontoudtogsfil, skal du gå til jobhistorikken for Datastyring og se udførelsesoplysningerne for at finde fejlen.</span><span class="sxs-lookup"><span data-stu-id="538af-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="538af-115">Fejlen gør det lettere at udpege kontoudtoget, balancen eller kontoudtogslinjen.</span><span class="sxs-lookup"><span data-stu-id="538af-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="538af-116">Det er dog ikke sandsynligt, at du får tilstrækkelige oplysninger til at identificere det felt eller element, der er årsag til problemet.</span><span class="sxs-lookup"><span data-stu-id="538af-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="538af-117">Hvad er forskellene?</span><span class="sxs-lookup"><span data-stu-id="538af-117">What are the differences?</span></span>
<span data-ttu-id="538af-118">Sammenlign layoutdefinitionen for bankfiler med Finance and Operations-importdefinitionen, og bemærk eventuelle forskelle i felter og elementer.</span><span class="sxs-lookup"><span data-stu-id="538af-118">Compare the bank file layout definition to the Finance and Operations import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="538af-119">Sammenlign bankkontoudtogsfilen med den relaterede Finance and Operations-eksempelfil.</span><span class="sxs-lookup"><span data-stu-id="538af-119">Compare the bank statement file to the related sample Finance and Operations file.</span></span> <span data-ttu-id="538af-120">I ISO20022-filerne bør eventuelle forskelle være lette at se.</span><span class="sxs-lookup"><span data-stu-id="538af-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="transformations"></a><span data-ttu-id="538af-121">Transformationer</span><span class="sxs-lookup"><span data-stu-id="538af-121">Transformations</span></span>
<span data-ttu-id="538af-122">Ændringen foretages typisk i en af tre transformationer.</span><span class="sxs-lookup"><span data-stu-id="538af-122">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="538af-123">Hver transformation er skrevet for en bestemt standard.</span><span class="sxs-lookup"><span data-stu-id="538af-123">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="538af-124">Ressourcenavn</span><span class="sxs-lookup"><span data-stu-id="538af-124">Resource name</span></span>                                         | <span data-ttu-id="538af-125">Filnavn</span><span class="sxs-lookup"><span data-stu-id="538af-125">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="538af-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="538af-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="538af-127">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="538af-127">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="538af-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="538af-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="538af-129">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="538af-129">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="538af-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="538af-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="538af-131">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="538af-131">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="538af-132">Fejlfinding af transformationer</span><span class="sxs-lookup"><span data-stu-id="538af-132">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="538af-133">Justere BAI2- og MT940-filerne</span><span class="sxs-lookup"><span data-stu-id="538af-133">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="538af-134">BAI2- og MT940-filerne er tekstbaserede filer og kræver en justering for at aktivere fejlfinding af Extensible Stylesheet Language Transformations (XSLT).</span><span class="sxs-lookup"><span data-stu-id="538af-134">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="538af-135">Denne justering foretages, når en fil importeres.</span><span class="sxs-lookup"><span data-stu-id="538af-135">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="538af-136">Opret en XML-fil, og kopiér følgende tekst ind i den.</span><span class="sxs-lookup"><span data-stu-id="538af-136">Create an XML file, and copy the following text into it.</span></span>

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  <span data-ttu-id="538af-137">Kopiér indholdet af bankkontoudtogsfilen og indsæt det i XML-filen, så det erstatter **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="538af-137">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="538af-138">Foretage fejlfinding af XSLT-transformationen</span><span class="sxs-lookup"><span data-stu-id="538af-138">Debug the XSLT</span></span>

<span data-ttu-id="538af-139">Få flere oplysninger under <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="538af-139">For more information, see <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="538af-140">Start Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="538af-140">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="538af-141">Opret en konsolansøgning.</span><span class="sxs-lookup"><span data-stu-id="538af-141">Create a console application.</span></span>
3.  <span data-ttu-id="538af-142">Åbn den relevante XSLT-transformation.</span><span class="sxs-lookup"><span data-stu-id="538af-142">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="538af-143">Klik på XLST-transformationen og dens egenskabsside.</span><span class="sxs-lookup"><span data-stu-id="538af-143">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="538af-144">Angiv input til lokationen for bankkontoudtogsfilen.</span><span class="sxs-lookup"><span data-stu-id="538af-144">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="538af-145">Definer en lokation og et filnavn til outputtet.</span><span class="sxs-lookup"><span data-stu-id="538af-145">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="538af-146">Angiv de nødvendige pausepunkter.</span><span class="sxs-lookup"><span data-stu-id="538af-146">Set the required break points.</span></span>
8.  <span data-ttu-id="538af-147">Åbn menuen, og klik på **XML** &gt; **Start fejlfinding af XSLT**.</span><span class="sxs-lookup"><span data-stu-id="538af-147">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="538af-148">Formatér XLST-outputtet</span><span class="sxs-lookup"><span data-stu-id="538af-148">Format the XSLT output</span></span>

<span data-ttu-id="538af-149">Når transformationen er i gang, oprettes der en outputfil, som du kan se i Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="538af-149">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="538af-150">Brug Ctrl+A, Ctrl+K og Ctrl+D til hurtigt at formatere outputfilen.</span><span class="sxs-lookup"><span data-stu-id="538af-150">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="538af-151">Justere transformationen</span><span class="sxs-lookup"><span data-stu-id="538af-151">Adjust the transformation</span></span>

<span data-ttu-id="538af-152">Juster transformationen for at få det relevante felt eller element i bankkontoudtogsfilen.</span><span class="sxs-lookup"><span data-stu-id="538af-152">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="538af-153">Derefter skal du knytte feltet eller elementet til det relevante Finance and Operations-element.</span><span class="sxs-lookup"><span data-stu-id="538af-153">Then map that field or element to the appropriate Finance and Operations element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="538af-154">Indikator for debet/kredit</span><span class="sxs-lookup"><span data-stu-id="538af-154">Debit/credit indicator</span></span>

<span data-ttu-id="538af-155">Nogle gange kan debiteringer importeres som kreditter, og kreditter kan importeres som debet.</span><span class="sxs-lookup"><span data-stu-id="538af-155">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="538af-156">Du kan løse dette problem ved at ændre den relevante XSLT.</span><span class="sxs-lookup"><span data-stu-id="538af-156">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="538af-157">Hvis bankkontoudtog kommer fra flere banker, skal du kontrollere, at de alle bruger samme fremgangsmåde for debet/kredit, eller oprette separate transformationer.</span><span class="sxs-lookup"><span data-stu-id="538af-157">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="538af-158">BAI2XML-til-Reconciliation.xlst GetAmountCreditDebitIndicator-skabelon</span><span class="sxs-lookup"><span data-stu-id="538af-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="538af-159">ISO20022XML-til-Reconcilation.xslt GetCreditDebit-skabelon</span><span class="sxs-lookup"><span data-stu-id="538af-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="538af-160">MT940XML-til-Reconcilation.xslt GetCreditDebitIndicator-skabelon</span><span class="sxs-lookup"><span data-stu-id="538af-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="538af-161">Eksempler på bankkontoudtogsformater og tekniske layout</span><span class="sxs-lookup"><span data-stu-id="538af-161">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="538af-162">Følgende tabel viser eksempler på de tekniske layoutdefinitioner for importfiler til avanceret bankafstemning og tre relaterede eksempelfiler på bankkontoudtog.</span><span class="sxs-lookup"><span data-stu-id="538af-162">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="538af-163">Du kan hente filer eksempelfilerne og tekniske layout her: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="538af-163">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="538af-164">Teknisk layoutdefinition</span><span class="sxs-lookup"><span data-stu-id="538af-164">Technical layout definition</span></span>                             | <span data-ttu-id="538af-165">Eksempelfil med bankkontoudtog</span><span class="sxs-lookup"><span data-stu-id="538af-165">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="538af-166">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="538af-166">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="538af-167">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="538af-167">MT940StatementExample</span></span>                |
| <span data-ttu-id="538af-168">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="538af-168">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="538af-169">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="538af-169">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="538af-170">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="538af-170">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="538af-171">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="538af-171">BAI2StatementExample</span></span>                 |






