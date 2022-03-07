---
title: Konfigurere og generere filer til positive betalinger
description: I dette emne beskrives, hvordan du opretter positive betalinger og genererer filer til positive betalinger.
author: panolte
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 992c73b1ba1f461542873a7df97f1539b99fc015c3e6ef090993e90212993851
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737179"
---
# <a name="set-up-and-generate-positive-pay-files"></a>Konfigurere og generere filer til positive betalinger

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du opretter positive betalinger og genererer filer til positive betalinger. 

Konfigurer en positiv betaling til at generere en elektronisk liste over checks, der er leveret til banken. Når checken derefter skal indløses hos banken, sammenligner banken den med listen over checks. Hvis checken svarer til en check på listen, indløser banken den. Hvis checken ikke stemmer overens med en check på listen, beholder banken den til gennemsyn.

## <a name="security-for-positive-pay-files"></a>Sikkerhed for filer til positive betalinger
Filer til positiv betaling kan indeholde følsomme oplysninger om beløbsmodtagere og checkbeløb. Sørg derfor for, at du bruger passende de sikringsforanstaltninger fra det tidspunkt, hvor filerne genereres, indtil de modtages af banken. Filer til positive betalinger overføres til den lokalitet, der er angivet i webbrowseren. Fordi filer til positive betalinger kan indeholde følsomme oplysninger, er det vigtigt, at kun autoriserede brugere har adgang til at generere og se disse oplysninger i Microsoft Dynamics 365 Finance. Brug følgende tabel til at afgøre, hvilke rettigheder der kræves.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opgave</th>
<th>Rettighed</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Generere filer til positive betalinger fra listesiden <strong>Bankkonti</strong> eller siden <strong>Bankkonti</strong>.</td>
<td><ul>
<li><strong>Vedligehold oplysninger om positive bankbetalinger</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>Generere filer til positive betaling for flere juridiske enheder og bankkonti fra siden <strong>Generér en fil til positive betalinger</strong>.</td>
<td><ul>
<li><strong>Vedligehold oplysninger om positive bankbetalinger</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Se filer til positive betalinger på siden <strong>Filoversigt over positive betalinger</strong>.</td>
<td><strong>Vis oplysninger om positive bankbetalinger for flere juridiske enheder</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>Bekræft en fil til positive betalinger på siden <strong>Filoversigt over positive betalinger</strong>.</td>
<td><strong>Bekræft filen til positive betalinger</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>Tilbagekalde en fil til positive betalinger på siden <strong>Filoversigt over positive betalinger</strong>.</td>
<td><strong>Tilbagekald fil til positive betalinger</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a>Konfigurere et format for positiv betaling
Filer til positiv betaling oprettes ved hjælp af dataenheder. Før du kan generere en fil til positive betalinger, skal du oprette et transformationsinputformat, der skal bruges til at oversætte checkoplysningerne til et format, der kan kommunikere med banken. På siden **Format for positiv betaling** kan du oprette et filformat-id og en beskrivelse. Transformationsinputformatet skal være af XML-typen. Det specifikke format afhænger af, hvilken transformationsfil du bruger. Eksempelvis bruger den leverede XLST-eksempelfil (Extensible Stylesheet Language Transformations) formatet **XML-elementet**. Brug handlingen **Overfør fil brugt til transformation** til at angive placeringen af transformationsfilen til det format, som kræves af din bank.

## <a name="example-xslt-file-for-positive-pay-file"></a>Eksempel: XSLT-filer til positive betalinger

```xml
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
```

> [!NOTE]
> XML-navne i XSLT skal svare til store og små bogstaver af noder i XML-filen. Der skelnes mellem store og små bogstaver i både XSLT- og XML-filerne. 

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a>Tildele formatet for positiv betaling til en bankkonto
For hver bankkonto, du vil generere oplysninger om positiv betaling for, skal du tildele det format for positiv betaling, du angav i forrige afsnit. På siden **Bankkonti** skal du vælge formatet for positive betalinger, der svarer til bankkontoen. Angiv den første dato til generering af filer til positiv betaling i feltet **Startdato for positiv betaling**. Det er vigtigt, at du indtaster en dato i dette felt. Ellers vil den første positive lønfil, du opretter, indeholde alle checks, der nogensinde er oprettet for denne bankkonto.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Tildele en nummerserie for filer til positiv betaling
Hver fil til positiv betaling skal have et entydigt nummer. Brug fanen **Nummerserier** på siden **Likviditets- og bankstyringsparametre** for at oprette en nummerserie for filer til positive betalinger.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Generere en fil til positiv betaling for en enkelt bankkonto
Du kan generere en fil til positiv betaling for en enkelt juridisk enhed og en enkelt bankkonto. Du kan finde oplysninger om, hvordan du genererer en fil til positiv betaling for flere juridiske enheder og bankkonti på samme tid, i det næste afsnit. For at generere en fil til positiv betaling for en enkelt juridisk enhed og en enkelt bankkonto skal du åbne dialogboksen **Generér en fil til positive betalinger** fra siden **Bankkonti**. I feltet **Skæringsdato** skal du angive den sidste checkdato, der skal medtages i filen til positiv betaling. Alle checks, der ikke har været medtaget i en fil til positiv betaling ved udløbet af denne checkdato, medtages i filen.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Generere en fil til positiv betaling for flere bankkonti
For at generere en fil til flere bankkonti skal du bruge fra den periodiske opgave **Generér en fil til positive betalinger**. Vælg et positivt betalingsformat til filen, og angiv, om filen skal genereres til alle juridiske enheder eller en bestemt juridisk enhed. Du kan også generere filen til positiv betaling for alle bankkonti, der bruger det angivne positive betalingsformat, eller for den valgte bankkonto. I feltet **Skæringsdato** skal du angive den sidste checkdato, der skal medtages i filen til positiv betaling. Alle checks, der ikke har været medtaget i en fil til positiv betaling ved udløbet af denne checkdato, medtages i filen.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Få vist resultaterne af generering af fil til positive betalinger
Når filen til positive betalinger er oprettet, kan du se resultatet på siden **Filoversigt over positive betalinger**. Du kan få vist detaljerede oplysninger om de forskellige checks på siden **Fil til positive betalinger**.

## <a name="confirm-a-positive-pay-file"></a>Bekræfte en fil til positiv betaling
Når de checks, der er angivet i en fil til positiv betaling, er betalt, modtager du et bekræftelsesnummer fra din bank. Derefter kan du bekræfte filen til positiv betaling. På siden **Filoversigt over positive betalinger** skal du vælge en fil til positive betalinger, der har statussen **Oprettet** og derefter vælge handlingen **Indtast bekræftelse**. Når du bekræfter en fil til positiv betaling, registreres det bekræftelsesnummer, du modtog fra banken.

## <a name="recall-a-positive-pay-file"></a>Tilbagekald en fil til positive betalinger
Hvis du vil ændre en fil til positiv betaling, kan du tilbagekalde den. På siden **Filoversigt over positive betalinger** skal du vælge en fil til positive betalinger, der har statussen **Oprettet** og derefter vælge handlingen **Tilbagekald**. For hver check i filen til positiv betaling, nulstilles det felt, der angiver, om checken er inkluderet i en fil til positiv betaling. Derefter kan du oprette en ny fil til positiv betaling, der indeholder den check, der blev tilbagekaldt.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
