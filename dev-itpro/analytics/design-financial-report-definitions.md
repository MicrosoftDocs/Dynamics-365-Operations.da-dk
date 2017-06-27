---
title: "Rapportdefinitioner i Designer til økonomirapporter"
description: "Denne artikel indeholder oplysninger om rapportdefinitioner. En rapportdefinition er en rapportkomponent (eller dokumentkomponent), der anvender en rækkedefinition, kolonnedefinition og valgfri rapporteringstrædefinition til at oprette en rapport. En rapportdefinition indeholder også indstillinger til tilpasning af en rapport."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Management Reporter, Core
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 86b527b72ef0c9af71e70fe280bcdfe3992a36b1
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="report-definitions-in-financial-report-designer"></a>Rapportdefinitioner i Designer til økonomirapporter

[!include[banner](../includes/banner.md)]


Denne artikel indeholder oplysninger om rapportdefinitioner. En rapportdefinition er en rapportkomponent (eller dokumentkomponent), der anvender en rækkedefinition, kolonnedefinition og valgfri rapporteringstrædefinition til at oprette en rapport. En rapportdefinition indeholder også indstillinger til tilpasning af en rapport. 

En rapportdefinition er en rapportkomponent (eller dokumentkomponent), der anvender en rækkedefinition, kolonnedefinition og valgfri rapporteringstrædefinition til at oprette en rapport. En rapportdefinition indeholder også flere muligheder og indstillinger, som du kan bruge til at tilpasse en rapport. Når du har defineret rækkedefinitioner og kolonnedefinitioner, skal du kombinere dem i en rapportdefinition. På dette tidspunkt definerer du også andre aspekter af definitionerne, som detaljeniveauet og rapportdatoen. Du kan derefter gemme og generere en rapport. Økonomirapportering har følgende detaljeniveauer:

-   Finansiel
-   Finans og Konto
-   Finans, Konto og Transaktion

Afhængigt af hvordan data gemmes i Microsoft Dynamics ERP-systemet, er transaktionsdetaljer muligvis ikke tilgængelige i rapporter.

## <a name="create-a-report-definition"></a>Oprette en rapportdefinition
1.  I Report Designer skal du klikke på **Ny** i menuen **Filer**, og derefter skal du vælge **Rapportdefinition**.
2.  Angiv de relevante oplysninger på fanerne **Rapport**, **Output og fordeling**, **Sidehoveder og sidefødder** og **Indstillinger**.

## <a name="contents-of-a-report-definition"></a>Indholdet af en rapportdefinition
Nedenstående tabel beskriver fanerne i en rapportdefinition, og hvordan oplysningerne bruges.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Fane</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Rapport</td>
<td>Opret en rapport, konfigurer en rapport eller rediger en eksisterende rapport.</td>
</tr>
<tr class="even">
<td>Output og distribution</td>
<td>Rediger rapportens outputtype og destination.</td>
</tr>
<tr class="odd">
<td>Sidehoveder og sidefødder</td>
<td>Definer og formater sidehovederne og sidefødderne til rapporten. Du kan for eksempel tilføje tekst eller billeder til sidehovedet eller sidefoden. Økonomirapportering understøtter .bmp-, .jpg- og .png-billedfiler. Du kan også tilføje autotekstkoder for at indsætte andre oplysninger, f.eks et firmanavn, rapportnavn eller sidetal.</td>
</tr>
<tr class="even">
<td>Indstillinger</td>
<td>Angiv rapportdefinitionsindstillinger, f.eks. følgende indstillinger:
<ul>
<li>Formater og afrund beløb</li>
<li>Formater detaljerapporter</li>
<li>Formater rapporteringstræer</li>
<li>Generér en undtagelsesrapport</li>
<li>Angiv valutaomregning</li>
<li>Oplysninger og filtrer kontodetaljer</li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Se også
--------

[Økonomirapportering](financial-reporting-intro.md)




