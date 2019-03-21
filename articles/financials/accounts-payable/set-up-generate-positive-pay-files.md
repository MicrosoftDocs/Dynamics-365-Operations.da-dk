---
title: Konfigurere og generere filer til positive betalinger
description: I dette emne beskrives, hvordan du opretter positive betalinger og genererer filer til positive betalinger.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: dbc512c6d214dc8cf2527ac23103529111896ec5
ms.sourcegitcommit: 065d9fab832b6bcc88c00dc78ac1ae854c762ec7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/06/2019
ms.locfileid: "778172"
---
# <a name="set-up-and-generate-positive-pay-files"></a><span data-ttu-id="d7513-103">Konfigurere og generere filer til positive betalinger</span><span class="sxs-lookup"><span data-stu-id="d7513-103">Set up and generate positive pay files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7513-104">I dette emne beskrives, hvordan du opretter positive betalinger og genererer filer til positive betalinger.</span><span class="sxs-lookup"><span data-stu-id="d7513-104">This topic explains how to set up positive pay and generate positive pay files.</span></span> 

<span data-ttu-id="d7513-105">Konfigurer en positiv betaling til at generere en elektronisk liste over checks, der er leveret til banken.</span><span class="sxs-lookup"><span data-stu-id="d7513-105">Set up positive pay to generate an electronic list of checks that is provided to the bank.</span></span> <span data-ttu-id="d7513-106">Når checken derefter skal indløses hos banken, sammenligner banken den med listen over checks.</span><span class="sxs-lookup"><span data-stu-id="d7513-106">Then, when a check is presented to the bank, the bank compares it with the list of checks.</span></span> <span data-ttu-id="d7513-107">Hvis checken svarer til en check på listen, indløser banken den.</span><span class="sxs-lookup"><span data-stu-id="d7513-107">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="d7513-108">Hvis checken ikke stemmer overens med en check på listen, beholder banken den til gennemsyn.</span><span class="sxs-lookup"><span data-stu-id="d7513-108">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

## <a name="security-for-positive-pay-files"></a><span data-ttu-id="d7513-109">Sikkerhed for filer til positive betalinger</span><span class="sxs-lookup"><span data-stu-id="d7513-109">Security for positive pay files</span></span>
<span data-ttu-id="d7513-110">Filer til positiv betaling kan indeholde følsomme oplysninger om beløbsmodtagere og checkbeløb.</span><span class="sxs-lookup"><span data-stu-id="d7513-110">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="d7513-111">Sørg derfor for, at du bruger passende de sikringsforanstaltninger fra det tidspunkt, hvor filerne genereres, indtil de modtages af banken.</span><span class="sxs-lookup"><span data-stu-id="d7513-111">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="d7513-112">Filer til positive betalinger overføres til den lokalitet, der er angivet i webbrowseren.</span><span class="sxs-lookup"><span data-stu-id="d7513-112">Positive pay files are downloaded to the location that is specified by your web browser.</span></span> <span data-ttu-id="d7513-113">Fordi filer til positive betalinger kan indeholde følsomme oplysninger, er det vigtigt, at kun autoriserede brugere har adgang til at generere og få vist disse oplysninger i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d7513-113">Because positive pay files can contain sensitive information, it's important that only authorized users have access to generate and view this information in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="d7513-114">Brug følgende tabel til at afgøre, hvilke rettigheder der kræves.</span><span class="sxs-lookup"><span data-stu-id="d7513-114">Use the following table to help you determine the privileges that are required.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7513-115">Opgave</span><span class="sxs-lookup"><span data-stu-id="d7513-115">Task</span></span></th>
<th><span data-ttu-id="d7513-116">Rettighed</span><span class="sxs-lookup"><span data-stu-id="d7513-116">Privilege</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d7513-117">Generere filer til positive betalinger fra listesiden <strong>Bankkonti</strong> eller siden <strong>Bankkonti</strong>.</span><span class="sxs-lookup"><span data-stu-id="d7513-117">Generate positive pay files from the <strong>Bank accounts</strong> list page or the <strong>Bank accounts</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="d7513-118"><strong>Vedligehold oplysninger om positive bankbetalinger</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="d7513-118"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="d7513-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="d7513-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7513-120">Generere filer til positive betaling for flere juridiske enheder og bankkonti fra siden <strong>Generér en fil til positive betalinger</strong>.</span><span class="sxs-lookup"><span data-stu-id="d7513-120">Generate positive pay files for multiple legal entities and bank accounts from the <strong>Generate a positive pay file</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="d7513-121"><strong>Vedligehold oplysninger om positive bankbetalinger</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="d7513-121"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="d7513-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="d7513-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7513-123">Se filer til positive betalinger på siden <strong>Filoversigt over positive betalinger</strong>.</span><span class="sxs-lookup"><span data-stu-id="d7513-123">View positive pay files on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="d7513-124"><strong>Vis oplysninger om positive bankbetalinger for flere juridiske enheder</strong> (BankPositivePayView)</span><span class="sxs-lookup"><span data-stu-id="d7513-124"><strong>View bank positive pay information for multiple legal entities</strong> (BankPositivePayView)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7513-125">Bekræft en fil til positive betalinger på siden <strong>Filoversigt over positive betalinger</strong>.</span><span class="sxs-lookup"><span data-stu-id="d7513-125">Confirm a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="d7513-126"><strong>Bekræft filen til positive betalinger</strong> (BankPositivePayConfirm)</span><span class="sxs-lookup"><span data-stu-id="d7513-126"><strong>Confirm positive payment file</strong> (BankPositivePayConfirm)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7513-127">Tilbagekalde en fil til positive betalinger på siden <strong>Filoversigt over positive betalinger</strong>.</span><span class="sxs-lookup"><span data-stu-id="d7513-127">Recall a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="d7513-128"><strong>Tilbagekald fil til positive betalinger</strong> (BankPositivePayRecall)</span><span class="sxs-lookup"><span data-stu-id="d7513-128"><strong>Recall positive pay file</strong> (BankPositivePayRecall)</span></span></td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a><span data-ttu-id="d7513-129">Konfigurere et format for positiv betaling</span><span class="sxs-lookup"><span data-stu-id="d7513-129">Set up a positive pay format</span></span>
<span data-ttu-id="d7513-130">Filer til positiv betaling oprettes ved hjælp af dataenheder.</span><span class="sxs-lookup"><span data-stu-id="d7513-130">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="d7513-131">Før du kan generere en fil til positive betalinger, skal du oprette et transformationsinputformat, der skal bruges til at oversætte checkoplysningerne til et format, der kan kommunikere med banken.</span><span class="sxs-lookup"><span data-stu-id="d7513-131">Before you can generate a positive pay file, you must set up a transformation input format that will be used to translate the check information into a format that can communicate with the bank.</span></span> <span data-ttu-id="d7513-132">På siden **Format for positiv betaling** kan du oprette et filformat-id og en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d7513-132">On the **Positive pay format** page, you can create a file format identifier and a description.</span></span> <span data-ttu-id="d7513-133">Transformationsinputformatet skal være af XML-typen.</span><span class="sxs-lookup"><span data-stu-id="d7513-133">The transformation input format must be of the XML type.</span></span> <span data-ttu-id="d7513-134">Det specifikke format afhænger af, hvilken transformationsfil du bruger.</span><span class="sxs-lookup"><span data-stu-id="d7513-134">The specific format depends on the transformation file that you're using.</span></span> <span data-ttu-id="d7513-135">Eksempelvis bruger den leverede XLST-eksempelfil (Extensible Stylesheet Language Transformations) formatet **XML-elementet**.</span><span class="sxs-lookup"><span data-stu-id="d7513-135">For example, the sample Extensible Stylesheet Language Transformations (XSLT) file that is provided uses the **XML-Element** format.</span></span> <span data-ttu-id="d7513-136">Brug handlingen **Overfør fil brugt til transformation** til at angive placeringen af transformationsfilen til det format, som kræves af din bank.</span><span class="sxs-lookup"><span data-stu-id="d7513-136">Use the **Upload file used for transformation** action to specify the location of the transform file for the format that your bank requires.</span></span>

## <a name="example-xslt-file-for-positive-pay-file"></a><span data-ttu-id="d7513-137">Eksempel: XSLT-filer til positive betalinger</span><span class="sxs-lookup"><span data-stu-id="d7513-137">Example: XSLT file for positive pay file</span></span>
    <xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:msxsl="urn:schemas-microsoft-com:xslt" exclude-result-prefixes="msxsl xslthelper" xmlns="urn:iso:std:iso:20022:tech:xsd:pain.001.001.02" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xslthelper="http://schemas.microsoft.com/BizTalk/2003/xslthelper">
      <xsl:output method="xml" omit-xml-declaration="no" version="1.0" encoding="utf-8"/>
      <xsl:template match="/">
        <xsl:value-of select="'
    '" />
        <Document>
          <xsl:value-of select="'
    '" />
          <!--Header Begin-->
          <xsl:value-of select='string("Vendor ID,Vendor Name,Voided,Document Type,Check Date,Check Number,Check Amount,Checkbook ID,Vendor Class ID,Posted Date")'/>
          <xsl:value-of select="'
    '" />
          <!--Header End-->
          <xsl:for-each select="Document/BANKPOSITIVEPAYEXPORTENTITY">
            <!--Cheque Detail begin-->
            <xsl:value-of select='RECIPIENTACCOUNTNUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='BANKNEGINSTRECIPIENTNAME/text()'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Void") or CHEQUESTATUS/text()=normalize-space("Rejected") or CHEQUESTATUS/text()=normalize-space("Cancelled")'>
                <xsl:value-of select='string("Yes")'/>
              </xsl:when>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Payment")'>
                <xsl:value-of select='string("No")'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='string(" ")'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("Payment")'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='CHEQUENUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='AMOUNTCUR/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("BOA-#1812")'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='RECIPIENTTYPE/text()=normalize-space("Vend")'>
                <xsl:value-of select='VENDGROUP/text()'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='CUSTGROUP/text()'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="'
    '" />
          </xsl:for-each>
        </Document>
      </xsl:template>
    </xsl:stylesheet>

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a><span data-ttu-id="d7513-138">Tildele formatet for positiv betaling til en bankkonto</span><span class="sxs-lookup"><span data-stu-id="d7513-138">Assign the positive pay format to a bank account</span></span>
<span data-ttu-id="d7513-139">For hver bankkonto, du vil generere oplysninger om positiv betaling for, skal du tildele det format for positiv betaling, du angav i forrige afsnit.</span><span class="sxs-lookup"><span data-stu-id="d7513-139">For each bank account that you want to generate positive pay information for, you must assign the positive pay format that you specified in the previous section.</span></span> <span data-ttu-id="d7513-140">På siden **Bankkonti** skal du vælge formatet for positive betalinger, der svarer til bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="d7513-140">On the **Bank accounts** page, select the positive pay format that corresponds to the bank account.</span></span> <span data-ttu-id="d7513-141">Angiv den første dato til generering af filer til positiv betaling i feltet **Startdato for positiv betaling**.</span><span class="sxs-lookup"><span data-stu-id="d7513-141">In the **Positive pay start date** field, enter the first date to generate positive pay files.</span></span> <span data-ttu-id="d7513-142">Det er vigtigt, at du indtaster en dato i dette felt.</span><span class="sxs-lookup"><span data-stu-id="d7513-142">It's important that you enter a date in this field.</span></span> <span data-ttu-id="d7513-143">Ellers vil den første positive lønfil, du opretter, indeholde alle checks, der nogensinde er oprettet for denne bankkonto.</span><span class="sxs-lookup"><span data-stu-id="d7513-143">Otherwise, the first positive pay file that you generate will include all checks that have ever been created for this bank account.</span></span>

## <a name="assign-a-number-sequence-for-positive-pay-files"></a><span data-ttu-id="d7513-144">Tildele en nummerserie for filer til positiv betaling</span><span class="sxs-lookup"><span data-stu-id="d7513-144">Assign a number sequence for positive pay files</span></span>
<span data-ttu-id="d7513-145">Hver fil til positiv betaling skal have et entydigt nummer.</span><span class="sxs-lookup"><span data-stu-id="d7513-145">Each positive pay file must have a unique number.</span></span> <span data-ttu-id="d7513-146">Brug fanen **Nummerserier** på siden **Likviditets- og bankstyringsparametre** for at oprette en nummerserie for filer til positive betalinger.</span><span class="sxs-lookup"><span data-stu-id="d7513-146">Use the **Number sequences** tab on the **Cash and bank management parameters** page to create a number sequence for positive pay files.</span></span>

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a><span data-ttu-id="d7513-147">Generere en fil til positiv betaling for en enkelt bankkonto</span><span class="sxs-lookup"><span data-stu-id="d7513-147">Generate a positive pay file for a single bank account</span></span>
<span data-ttu-id="d7513-148">Du kan generere en fil til positiv betaling for en enkelt juridisk enhed og en enkelt bankkonto.</span><span class="sxs-lookup"><span data-stu-id="d7513-148">You can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="d7513-149">Du kan finde oplysninger om, hvordan du genererer en fil til positiv betaling for flere juridiske enheder og bankkonti på samme tid, i det næste afsnit.</span><span class="sxs-lookup"><span data-stu-id="d7513-149">For information about how to generate positive pay files for multiple legal entities and bank accounts at the same time, see the next section.</span></span> <span data-ttu-id="d7513-150">For at generere en fil til positiv betaling for en enkelt juridisk enhed og en enkelt bankkonto skal du åbne dialogboksen **Generér en fil til positive betalinger** fra siden **Bankkonti**.</span><span class="sxs-lookup"><span data-stu-id="d7513-150">To generate a positive pay file for a single legal entity and a single bank account, open the **Generate a positive pay file** dialog box from the **Bank accounts** page.</span></span> <span data-ttu-id="d7513-151">I feltet **Skæringsdato** skal du angive den sidste checkdato, der skal medtages i filen til positiv betaling.</span><span class="sxs-lookup"><span data-stu-id="d7513-151">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="d7513-152">Alle checks, der ikke har været medtaget i en fil til positiv betaling ved udløbet af denne checkdato, medtages i filen.</span><span class="sxs-lookup"><span data-stu-id="d7513-152">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a><span data-ttu-id="d7513-153">Generere en fil til positiv betaling for flere bankkonti</span><span class="sxs-lookup"><span data-stu-id="d7513-153">Generate a positive pay file for multiple bank accounts</span></span>
<span data-ttu-id="d7513-154">For at generere en fil til flere bankkonti skal du bruge fra den periodiske opgave **Generér en fil til positive betalinger**.</span><span class="sxs-lookup"><span data-stu-id="d7513-154">To generate a positive pay file for multiple bank accounts, use the **Generate a positive pay file** periodic task.</span></span> <span data-ttu-id="d7513-155">Vælg et positivt betalingsformat til filen, og angiv, om filen skal genereres til alle juridiske enheder eller en bestemt juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="d7513-155">Select the positive pay format for the file, and specify whether to generate the file for all legal entities or for a selected legal entity.</span></span> <span data-ttu-id="d7513-156">Du kan også generere filen til positiv betaling for alle bankkonti, der bruger det angivne positive betalingsformat, eller for den valgte bankkonto.</span><span class="sxs-lookup"><span data-stu-id="d7513-156">You can also generate the positive pay file for all bank accounts that use the specified positive pay format or for a selected bank account.</span></span> <span data-ttu-id="d7513-157">I feltet **Skæringsdato** skal du angive den sidste checkdato, der skal medtages i filen til positiv betaling.</span><span class="sxs-lookup"><span data-stu-id="d7513-157">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="d7513-158">Alle checks, der ikke har været medtaget i en fil til positiv betaling ved udløbet af denne checkdato, medtages i filen.</span><span class="sxs-lookup"><span data-stu-id="d7513-158">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="view-the-results-of-positive-pay-file-generation"></a><span data-ttu-id="d7513-159">Få vist resultaterne af generering af fil til positive betalinger</span><span class="sxs-lookup"><span data-stu-id="d7513-159">View the results of positive pay file generation</span></span>
<span data-ttu-id="d7513-160">Når filen til positive betalinger er oprettet, kan du se resultatet på siden **Filoversigt over positive betalinger**.</span><span class="sxs-lookup"><span data-stu-id="d7513-160">After the positive pay file is generated, you can view the results on the **Positive pay file summary** page.</span></span> <span data-ttu-id="d7513-161">Du kan få vist detaljerede oplysninger om de forskellige checks på siden **Fil til positive betalinger**.</span><span class="sxs-lookup"><span data-stu-id="d7513-161">To view the details of the individual checks, use the **Positive pay file** details page.</span></span>

## <a name="confirm-a-positive-pay-file"></a><span data-ttu-id="d7513-162">Bekræfte en fil til positiv betaling</span><span class="sxs-lookup"><span data-stu-id="d7513-162">Confirm a positive pay file</span></span>
<span data-ttu-id="d7513-163">Når de checks, der er angivet i en fil til positiv betaling, er betalt, modtager du et bekræftelsesnummer fra din bank.</span><span class="sxs-lookup"><span data-stu-id="d7513-163">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="d7513-164">Derefter kan du bekræfte filen til positiv betaling.</span><span class="sxs-lookup"><span data-stu-id="d7513-164">You can then confirm the positive pay file.</span></span> <span data-ttu-id="d7513-165">På siden **Filoversigt over positive betalinger** skal du vælge en fil til positive betalinger, der har statussen **Oprettet** og derefter vælge handlingen **Indtast bekræftelse**.</span><span class="sxs-lookup"><span data-stu-id="d7513-165">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Enter confirmation** action.</span></span> <span data-ttu-id="d7513-166">Når du bekræfter en fil til positiv betaling, registreres det bekræftelsesnummer, du modtog fra banken.</span><span class="sxs-lookup"><span data-stu-id="d7513-166">When you confirm a positive pay file, the confirmation number that you received from the bank is recorded.</span></span>

## <a name="recall-a-positive-pay-file"></a><span data-ttu-id="d7513-167">Tilbagekald en fil til positive betalinger</span><span class="sxs-lookup"><span data-stu-id="d7513-167">Recall a positive pay file</span></span>
<span data-ttu-id="d7513-168">Hvis du vil ændre en fil til positiv betaling, kan du tilbagekalde den.</span><span class="sxs-lookup"><span data-stu-id="d7513-168">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="d7513-169">På siden **Filoversigt over positive betalinger** skal du vælge en fil til positive betalinger, der har statussen **Oprettet** og derefter vælge handlingen **Tilbagekald**.</span><span class="sxs-lookup"><span data-stu-id="d7513-169">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Recall** action.</span></span> <span data-ttu-id="d7513-170">For hver check i filen til positiv betaling, nulstilles det felt, der angiver, om checken er inkluderet i en fil til positiv betaling.</span><span class="sxs-lookup"><span data-stu-id="d7513-170">For each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span> <span data-ttu-id="d7513-171">Derefter kan du oprette en ny fil til positiv betaling, der indeholder den check, der blev tilbagekaldt.</span><span class="sxs-lookup"><span data-stu-id="d7513-171">You can then create a new positive pay file that includes the check that was recalled.</span></span>



