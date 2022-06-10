---
title: Konfigurere og generere positive betalingsfiler ved hjælp af elektronisk rapportering
description: I dette emne beskrives, hvordan du konfigurerer positive betalinger med elektronisk rapportering.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: bc2f17d62b429b599d5ac5f2a521819275d36b64
ms.sourcegitcommit: 2b4ee1fe05792332904396b5f495d74f2a217250
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2022
ms.locfileid: "8770241"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Konfigurere positive betalingsfiler ved hjælp af elektronisk rapportering

I dette emne beskrives, hvordan du opretter positive betalinger og genererer filer til positive betalinger med Elektronisk rapportering.

> [!NOTE] 
> Før du bruger funktionen **Generér positiv bankbetalingsfil**, skal du opdatere enhedslisten først.
> Gå til oversigtspanelet **Datastyring > Importér/eksportér > Rammeparametre** 
> **Enhedsindstillinger**, og vælg **Opdater liste over enheder**.


Konfigurer en positiv betaling til at generere en elektronisk liste over checks, der er leveret til banken. Når en check derefter skal indløses i banken, sammenligner banken den med listen over checks. Hvis checken svarer til en check på listen, indløser banken den. Hvis checken ikke stemmer overens med en check på listen, beholder banken den til gennemsyn.

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

## <a name="set-up-the-electronic-reporting-configuration"></a>Konfigurere elektronisk rapportering

1. Gå til **Arbejdsområder \> Elektronisk rapportering**.
2. På feltet for **Microsoft**-konfigurationsudbyderen skal du vælg **Lagre**.
3. Vælg **Global**, og vælg derefter **Åbn**.
4. Hvis der skal oprettes en forbindelse til lageret, skal du vælge det blå link i dialogboksen.
5. Søg efter og vælg **Positiv betalingsmodel \> Format for positiv betaling** på konfigurationslisten.
6. I oversigtspanelet **Versioner** skal du vælge den seneste version og derefter vælge **Importér**.

## <a name="set-up-a-positive-pay-format"></a>Konfigurere et format for positiv betaling

1. Gå til **Kontant- og bankstyring \> Konfiguration \> Positive betalingsformater**.
2. Vælg **Ny**.
3. Angiv felterne **Betalingsformat** og **Beskrivelse**.
4. Markér afkrydsningsfeltet **Generisk elektronisk eksportformat**.
5. Angiv feltet **Konfiguration af eksportformat** til **Format for positiv betaling**.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Tildele et format for positiv betaling til en bankkonto
For hver bankkonto, du vil generere oplysninger om positiv betaling for, skal du tildele det format for positiv betaling, du angav i forrige afsnit. På siden Bankkonti skal du vælge formatet for positive betalinger, der svarer til bankkontoen. Angiv den første dato til generering af filer til positiv betaling i feltet **Startdato for positiv betaling**. 

>[!Important]
> Angiv en dato i feltet **Startdato for positiv betaling**. Hvis det er tomt, vil den første fil til positive betalinger, der oprettes, indeholde alle checks, der er oprettet for denne bankkonto.

1. Gå til **Kontant- og bankstyring \> Bankkonti \> Bankkonti**.
2. Åbn bankkontoen.
3. Angiv feltet **Positivt betalingsformat** til det format, der blev oprettet tidligere, i oversigtspanelet **Generelt**.
4. Angiv feltet **Startdato for positiv betaling** til dags dato.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Tildele en nummerserie for filer til positiv betaling
Hver fil til positiv betaling skal have et entydigt nummer. Brug fanen **Nummerserier** på siden **Likviditets- og bankstyringsparametre** til at oprette en nummerserie for filer til positive betalinger.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Generere en fil til positiv betaling for en enkelt bankkonto
Du kan generere en fil til positiv betaling for en enkelt juridisk enhed og en enkelt bankkonto. Du kan finde oplysninger om, hvordan du genererer en fil til positiv betaling for flere juridiske enheder og bankkonti på samme tid, i det næste afsnit. For at generere en fil til positiv betaling for en enkelt juridisk enhed og en enkelt bankkonto skal du åbne dialogboksen **Generér en fil til positive betalinger** fra siden **Bankkonti**. I feltet **Skæringsdato** skal du angive den sidste checkdato, der skal medtages i filen til positiv betaling. Alle checks, der ikke har været medtaget i en fil til positiv betaling ved udløbet af denne checkdato, medtages i filen.

1. Gå til **Kontant- og bankstyring \> Bankkonti \> Bankkonti**.
2. Åbn en bankkonto, der er konfigureret positiv betaling for.
3. Vælg **Administrer betalinger \> Positiv betaling \> Positiv betalingsfil**.
4. Angiv feltet **Skæringsdato**. Checks, der blev genereret før denne dato, inkluderes.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Generere en fil til positiv betaling for flere bankkonti
For at generere en fil til flere bankkonti skal du bruge fra den periodiske opgave **Fil til positive betalinger**. Vælg et positivt betalingsformat til filen, og angiv, om filen skal genereres til alle juridiske enheder eller en bestemt juridisk enhed. Du kan også generere filen til positiv betaling for alle bankkonti, der bruger det angivne positive betalingsformat, eller for den valgte bankkonto. I feltet **Skæringsdato** skal du angive den sidste checkdato, der skal medtages i filen til positiv betaling. Alle checks, der ikke har været medtaget i en fil til positiv betaling ved udløbet af denne checkdato, medtages i filen.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Få vist resultaterne af generering af fil til positive betalinger
Når filen til positive betalinger er oprettet, kan du se resultatet på siden **Filoversigt over positive betalinger**. Du kan få vist detaljerede oplysninger om de forskellige checks på siden **Fildetaljer om positiv betaling**.

## <a name="confirm-a-positive-pay-file"></a>Bekræfte en fil til positiv betaling
Når de checks, der er angivet i en fil til positiv betaling, er betalt, modtager du et bekræftelsesnummer fra din bank. Derefter kan du bekræfte filen til positiv betaling. På siden **Filoversigt over positive betalinger** skal du vælge en fil til positive betalinger, der har statussen **Oprettet** og derefter vælge handlingen **Indtast bekræftelse**. Når du bekræfter en fil til positiv betaling, registreres det bekræftelsesnummer, du modtog fra banken.

## <a name="recall-a-positive-pay-file"></a>Tilbagekald en fil til positive betalinger
Hvis du vil ændre en fil til positiv betaling, kan du tilbagekalde den. På siden **Filoversigt over positive betalinger** skal du vælge en fil til positive betalinger, der har statussen **Oprettet** og derefter vælge handlingen **Tilbagekald**. For hver check i filen til positiv betaling, nulstilles det felt, der angiver, om checken er inkluderet i en fil til positiv betaling. Derefter kan du oprette en ny fil til positiv betaling, der indeholder den check, der blev tilbagekaldt.


Den XML-fil, der oprettes, bliver downloadet.
