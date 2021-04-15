---
title: Fejlfinding af filimport af bankkontoudtog
description: Det er vigtigt, at kontoudtogsfilen fra banken matcher det layout, som Microsoft Dynamics 365 Finance understøtter. På grund af strenge standarder for bankkontoudtog fungerer de fleste integrationer korrekt. Men nogle gange kan udtogsfilen ikke importeres eller giver forkerte resultater. Normalt skyldes disse problemer små forskelle i bankkontoudtogsfilen. Denne artikel forklarer, hvordan du løser disse forskelle og løser problemerne.
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: f0e01881a6b68526479d27014d49a718069cffc9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815878"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="6636a-107">Fejlfinding af filimport af bankkontoudtog</span><span class="sxs-lookup"><span data-stu-id="6636a-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6636a-108">Det er vigtigt, at kontoudtogsfilen fra banken matcher det layout, som Microsoft Dynamics 365 Finance understøtter.</span><span class="sxs-lookup"><span data-stu-id="6636a-108">It's important that the bank statement file from the bank matches the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="6636a-109">På grund af strenge standarder for bankkontoudtog fungerer de fleste integrationer korrekt.</span><span class="sxs-lookup"><span data-stu-id="6636a-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="6636a-110">Men nogle gange kan udtogsfilen ikke importeres eller giver forkerte resultater.</span><span class="sxs-lookup"><span data-stu-id="6636a-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="6636a-111">Normalt skyldes disse problemer små forskelle i bankkontoudtogsfilen.</span><span class="sxs-lookup"><span data-stu-id="6636a-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="6636a-112">Denne artikel forklarer, hvordan du løser disse forskelle og løser problemerne.</span><span class="sxs-lookup"><span data-stu-id="6636a-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="6636a-113">Hvad er fejlen?</span><span class="sxs-lookup"><span data-stu-id="6636a-113">What is the error?</span></span>
------------------

<span data-ttu-id="6636a-114">Når du forsøger at importere en bankkontoudtogsfil, skal du gå til jobhistorikken for Datastyring og se udførelsesoplysningerne for at finde fejlen.</span><span class="sxs-lookup"><span data-stu-id="6636a-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="6636a-115">Fejlen gør det lettere at udpege kontoudtoget, balancen eller kontoudtogslinjen.</span><span class="sxs-lookup"><span data-stu-id="6636a-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="6636a-116">Det er dog ikke sandsynligt, at du får tilstrækkelige oplysninger til at identificere det felt eller element, der er årsag til problemet.</span><span class="sxs-lookup"><span data-stu-id="6636a-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

> [!NOTE]
> <span data-ttu-id="6636a-117">Importerede bankkontoudtog må kun overlappe for et bestemt tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="6636a-117">Imported bank statements can overlap only for single a point in time.</span></span>  <span data-ttu-id="6636a-118">Hvis en opgørelse f.eks. slutter kl. 12:00 den 1. januar 2021, kan startdatoen for den næste opgørelse være 12:00 den 1. januar 2021.</span><span class="sxs-lookup"><span data-stu-id="6636a-118">For example, if a statement ends at 12:00 AM on January 1, 2021, then beginning date for the next statement can be 12:00 AM on Jarnuary 1, 2021 12:00:00 AM.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="6636a-119">Hvad er forskellene?</span><span class="sxs-lookup"><span data-stu-id="6636a-119">What are the differences?</span></span>
<span data-ttu-id="6636a-120">Sammenlign layoutdefinitionen for bankfilen med finansimportdefinitionen, og bemærk eventuelle forskelle i felter og elementer.</span><span class="sxs-lookup"><span data-stu-id="6636a-120">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="6636a-121">Sammenlign kontoudtogsfilen fra banken med den relaterede finanseksempelfil.</span><span class="sxs-lookup"><span data-stu-id="6636a-121">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="6636a-122">I ISO20022-filerne bør eventuelle forskelle være lette at se.</span><span class="sxs-lookup"><span data-stu-id="6636a-122">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="6636a-123">Tidszoneforskelle på importerede bankkontoudtog</span><span class="sxs-lookup"><span data-stu-id="6636a-123">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="6636a-124">Dato- og klokkeslætsværdierne i importfilen kan være forskellige fra de dato- og klokkeslætsværdier, der vises i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6636a-124">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="6636a-125">Hvis du vil undgå denne uoverensstemmelse, skal du angive en tidszoneindstilling på siden **Konfigurer datakilder**.</span><span class="sxs-lookup"><span data-stu-id="6636a-125">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="6636a-126">Se [Konfigurere importprocessen for avanceret bankafstemning](set-up-advanced-bank-reconciliation-import-process.md) for at få flere oplysninger om angivelse af en indstilling for tidszone.</span><span class="sxs-lookup"><span data-stu-id="6636a-126">For more information about entering a time zone preference, see [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md).</span></span>

## <a name="transformations"></a><span data-ttu-id="6636a-127">Transformationer</span><span class="sxs-lookup"><span data-stu-id="6636a-127">Transformations</span></span>
<span data-ttu-id="6636a-128">Ændringen foretages typisk i en af tre transformationer.</span><span class="sxs-lookup"><span data-stu-id="6636a-128">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="6636a-129">Hver transformation er skrevet for en bestemt standard.</span><span class="sxs-lookup"><span data-stu-id="6636a-129">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="6636a-130">Ressourcenavn</span><span class="sxs-lookup"><span data-stu-id="6636a-130">Resource name</span></span>                                         | <span data-ttu-id="6636a-131">Filnavn</span><span class="sxs-lookup"><span data-stu-id="6636a-131">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="6636a-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="6636a-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="6636a-133">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="6636a-133">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="6636a-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="6636a-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="6636a-135">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="6636a-135">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="6636a-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="6636a-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="6636a-137">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="6636a-137">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="6636a-138">Fejlfinding af transformationer</span><span class="sxs-lookup"><span data-stu-id="6636a-138">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="6636a-139">Justere BAI2- og MT940-filerne</span><span class="sxs-lookup"><span data-stu-id="6636a-139">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="6636a-140">BAI2- og MT940-filerne er tekstbaserede filer og kræver en justering for at aktivere fejlfinding af Extensible Stylesheet Language Transformations (XSLT).</span><span class="sxs-lookup"><span data-stu-id="6636a-140">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="6636a-141">Denne justering foretages, når en fil importeres.</span><span class="sxs-lookup"><span data-stu-id="6636a-141">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="6636a-142">Opret en XML-fil, og kopiér følgende tekst ind i den.</span><span class="sxs-lookup"><span data-stu-id="6636a-142">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="6636a-143">Kopiér indholdet af bankkontoudtogsfilen og indsæt det i XML-filen, så det erstatter **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="6636a-143">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="6636a-144">Foretage fejlfinding af XSLT-transformationen</span><span class="sxs-lookup"><span data-stu-id="6636a-144">Debug the XSLT</span></span>

<span data-ttu-id="6636a-145">Yderligere oplysninger finder du i <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="6636a-145">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="6636a-146">Start Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6636a-146">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="6636a-147">Opret en konsolansøgning.</span><span class="sxs-lookup"><span data-stu-id="6636a-147">Create a console application.</span></span>
3.  <span data-ttu-id="6636a-148">Åbn den relevante XSLT-transformation.</span><span class="sxs-lookup"><span data-stu-id="6636a-148">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="6636a-149">Klik på XLST-transformationen og dens egenskabsside.</span><span class="sxs-lookup"><span data-stu-id="6636a-149">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="6636a-150">Angiv input til lokationen for bankkontoudtogsfilen.</span><span class="sxs-lookup"><span data-stu-id="6636a-150">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="6636a-151">Definer en lokation og et filnavn til outputtet.</span><span class="sxs-lookup"><span data-stu-id="6636a-151">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="6636a-152">Angiv de nødvendige pausepunkter.</span><span class="sxs-lookup"><span data-stu-id="6636a-152">Set the required break points.</span></span>
8.  <span data-ttu-id="6636a-153">Åbn menuen, og klik på **XML** &gt; **Start fejlfinding af XSLT**.</span><span class="sxs-lookup"><span data-stu-id="6636a-153">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="6636a-154">Formatér XLST-outputtet</span><span class="sxs-lookup"><span data-stu-id="6636a-154">Format the XSLT output</span></span>

<span data-ttu-id="6636a-155">Når transformationen er i gang, oprettes der en outputfil, som du kan se i Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6636a-155">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="6636a-156">Brug Ctrl+A, Ctrl+K og Ctrl+D til hurtigt at formatere outputfilen.</span><span class="sxs-lookup"><span data-stu-id="6636a-156">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="6636a-157">Justere transformationen</span><span class="sxs-lookup"><span data-stu-id="6636a-157">Adjust the transformation</span></span>

<span data-ttu-id="6636a-158">Juster transformationen for at få det relevante felt eller element i bankkontoudtogsfilen.</span><span class="sxs-lookup"><span data-stu-id="6636a-158">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="6636a-159">Derefter skal du knytte feltet eller elementet til det relevante Finance-element.</span><span class="sxs-lookup"><span data-stu-id="6636a-159">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="6636a-160">Indikator for debet/kredit</span><span class="sxs-lookup"><span data-stu-id="6636a-160">Debit/credit indicator</span></span>

<span data-ttu-id="6636a-161">Nogle gange kan debiteringer importeres som kreditter, og kreditter kan importeres som debet.</span><span class="sxs-lookup"><span data-stu-id="6636a-161">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="6636a-162">Du kan løse dette problem ved at ændre den relevante XSLT.</span><span class="sxs-lookup"><span data-stu-id="6636a-162">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="6636a-163">Hvis bankkontoudtog kommer fra flere banker, skal du kontrollere, at de alle bruger samme fremgangsmåde for debet/kredit, eller oprette separate transformationer.</span><span class="sxs-lookup"><span data-stu-id="6636a-163">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="6636a-164">BAI2XML-til-Reconciliation.xlst GetAmountCreditDebitIndicator-skabelon</span><span class="sxs-lookup"><span data-stu-id="6636a-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="6636a-165">ISO20022XML-til-Reconcilation.xslt GetCreditDebit-skabelon</span><span class="sxs-lookup"><span data-stu-id="6636a-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="6636a-166">MT940XML-til-Reconcilation.xslt GetCreditDebitIndicator-skabelon</span><span class="sxs-lookup"><span data-stu-id="6636a-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="6636a-167">Eksempler på bankkontoudtogsformater og tekniske layout</span><span class="sxs-lookup"><span data-stu-id="6636a-167">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="6636a-168">Følgende tabel viser eksempler på de tekniske layoutdefinitioner for importfiler til avanceret bankafstemning og tre relaterede eksempelfiler på bankkontoudtog.</span><span class="sxs-lookup"><span data-stu-id="6636a-168">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="6636a-169">Du kan hente eksempelfiler og tekniske layout her: [Importere fileksempler](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span><span class="sxs-lookup"><span data-stu-id="6636a-169">You can download the example files and technical layouts here: [Import file examples](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span></span>  

| <span data-ttu-id="6636a-170">Teknisk layoutdefinition</span><span class="sxs-lookup"><span data-stu-id="6636a-170">Technical layout definition</span></span>                             | <span data-ttu-id="6636a-171">Eksempelfil med bankkontoudtog</span><span class="sxs-lookup"><span data-stu-id="6636a-171">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="6636a-172">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="6636a-172">DynamicsAXMT940Layout</span></span>                                   | [<span data-ttu-id="6636a-173">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="6636a-173">MT940StatementExample</span></span>](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| <span data-ttu-id="6636a-174">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="6636a-174">DynamicsAXISO20022Layout</span></span>                                | [<span data-ttu-id="6636a-175">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="6636a-175">ISO20022StatementExample</span></span>](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| <span data-ttu-id="6636a-176">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="6636a-176">DynamicsAXBAI2Layout</span></span>                                    | [<span data-ttu-id="6636a-177">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="6636a-177">BAI2StatementExample</span></span>](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
