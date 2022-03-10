---
title: EU-posteringscertifikater
description: Denne artikel indeholder oplysninger om postcertifikater i den Europæiske Union (EU).
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustEntryCertificateJour_W, CustParameters, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.custom: 11464
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 00b9e80a931c57722a92c3432f9c1006082b1bfbdd844d72c4d5962e106925dc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779787"
---
# <a name="eu-entry-certificates"></a>EU-postcertifikater

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om postcertifikater i den Europæiske Union (EU).

Du kan udføre følgende opgaver for et EU-posteringscertifikat:

-   Oprette og udstede et EU-posteringscertifikat sammen med en følgeseddel eller debitorfaktura for levering af varer eller tjenester til EU-lande/områder.
-   Modtage EU-posteringscertifikatet, der er signeret af en EU-kunde.
-   Overføre det signerede EU-posteringscertifikat, der er modtaget enten fra kunden eller fra en tredjepart, der er ansvarlig for levering af varer til kunden.
-   Tilknytte det overførte EU-posteringscertifikat med en debitorfaktura.
-   Opdatere status for det overførte EU-posteringscertifikat.

## <a name="prerequisites"></a>Forudsætninger
Følgende tabel viser de forudsætninger, der skal være på plads, før du starter.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategori</th>
<th>Forudsætning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Land/område</td>
<td>Den primære adresse for den juridiske skal enhed være i et EU-medlemsland.</td>
</tr>
<tr class="even">
<td>Relaterede opsætningsopgaver</td>
<td><ul>
<li>På siden <strong>Kreditorparametre</strong> skal du vælge indstillingerne <strong>Aktivér administration af indførselscertifikater</strong> og <strong>Aktivér udstedelse af indførselscertifikater</strong>.</li>
<li>På siden <strong>Kunder</strong> på oversigtspanelet <strong>Faktura og levering</strong> skal du vælge indstillingen <strong>Postcertifikat er påkrævet</strong> for at angive, at et EU-indførselscertifikat er obligatorisk for kunden. Vælg indstillingen <strong>Udsted indførselscertifikat</strong> for at udstede et EU-indførselscertifikat for den juridiske enhed for kunden.</li>
<li>På siden <strong>Debitorparametre</strong> skal du vælge en nummerseriekode for referencen <strong>Postcertifikat</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Relaterede transaktioner</td>
<td><ul>
<li>Opret en debitorkonto.</li>
<li>Opret en salgsordre.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="creating-registering-and-uploading-an-eu-entry-certificate"></a>Oprettelse, registrering og overførsel af et EU-indførselscertifikat
Du kan oprette et EU-posteringscertifikat automatisk eller manuelt. Et EU-posteringscertifikat oprettes og udskrives automatisk, når du bogfører en følgeseddel eller en faktura for en kunde ved hjælp af siden **Bogføring af følgeseddel** eller **Bogføring af faktura**. Hvis du manuelt vil oprette eller udskrive et EU-indførselscertifikat til en debitorfaktura igen, skal du bruge siden **Fakturajournal**. Derudover kan du bruge siden **Postcertifikatkladde** til at angive oplysninger om et EU-indførselscertifikat, der er udstedt af en tredjepart.

### <a name="creating-an-eu-entry-certificate-automatically-or-manually"></a>Oprette et EU-indførselscertifikat automatisk eller manuelt

Kan du automatisk oprette et EU-indførselscertifikat ved hjælp af en følgeseddel på siden **Alle salgsordrer** eller ved hjælp af en faktura på siden **Salgsordre**. Hvis du vil oprette et EU-indførselscertifikat manuelt, kan du bruge en faktura på siden **Fakturajournal**. Før du manuelt opretter et EU-indførselscertifikat, skal du dog ændre status for certificering af fakturaen.

### <a name="registering-an-eu-entry-certificate"></a>Registrere et EU-indførselscertifikat

Hvis registrering er påkrævet, kan du bruge siden **Postcertifikatkladde** til at registrere et EU-indførselscertifikat, der er udstedt af en tredjepart.

### <a name="uploading-a-received-eu-entry-certificate"></a>Overføre et modtaget EU-indførselscertifikat

Brug siden **Bilag** til at overføre et modtaget EU-indførselscertifikatet, der er signeret af en EU-kunde. Når certifikatet er overført, kan du knytte det til en faktura som bevis for, at varer er leveret. Denne dokumentation er påkrævet, hvis du skal udstede en faktura, der ikke indeholder moms, og den bruges også under revision.

### <a name="optional-updating-the-certification-status-and-printing-status-of-an-invoice"></a>Valgfrit: Opdatere status for certificering og udskrive status for en faktura

Du kan opdatere status for indførselscertificering og udskriftstatus for en debitorfaktura ved hjælp af siden **Fakturajournal**.

## <a name="technical-information-for-system-administrators"></a>Tekniske oplysninger til systemadministratorer
Hvis du ikke har adgang til de sider, der bruges til at fuldføre denne opgave, skal du kontakte din systemadministrator og angive de oplysninger, der vises i følgende tabel.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategori</th>
<th>Forudsætning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Sikkerhedsroller og programadgangsrettigheder</td>
<td>Når du vil angive og oprette EU-posteringscertifikater for varer eller tjenester, skal du være medlem af en sikkerhedsrolle, der omfatter følgende opgaver:
<ul>
<li><strong>Debitorassistent</strong> (CustInvoiceAccountsReceivableClerk)</li>
<li><strong>Kundeservicerepræsentant</strong> (TradeCustomerServiceRepresentative)</li>
<li><strong>Salgsassistent</strong> (TradeSalesClerk)</li>
<li><strong>Shippingmedarbejder</strong> (InventShippingClerk)</li>
</ul></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]