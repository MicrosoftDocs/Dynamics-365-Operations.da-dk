---
title: Rapportdefinitioner i Designer til økonomirapporter
description: Denne artikel indeholder oplysninger om rapportdefinitioner.
author: aprilolson
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.form: FinancialReports
ms.openlocfilehash: 2ffef335c694af56486ccd7738818c4edda49b9e
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802526"
---
# <a name="report-definitions-in-financial-report-designer"></a>Rapportdefinitioner i Designer til økonomirapporter

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om rapportdefinitioner. En rapportdefinition er en rapportkomponent (eller dokumentkomponent), der anvender en rækkedefinition, kolonnedefinition og valgfri rapporteringstrædefinition til at oprette en rapport. En rapportdefinition indeholder også indstillinger til tilpasning af en rapport. 

En rapportdefinition er en rapportkomponent (eller dokumentkomponent), der anvender en rækkedefinition, kolonnedefinition og valgfri rapporteringstrædefinition til at oprette en rapport. En rapportdefinition indeholder også yderligere indstillinger, som du kan anvende til tilpasning af en rapport. Når du har defineret rækkedefinitioner og kolonnedefinitioner, skal du kombinere dem i en rapportdefinition. På dette tidspunkt definerer du også andre aspekter af definitionerne, som detaljeniveauet og rapportdatoen. Du kan derefter gemme og generere en rapport. Økonomirapportering har følgende detaljeniveauer:

- Finansiel
- Finans og Konto
- Finans, Konto og Transaktion

Afhængigt af hvordan dataene er lagret i Microsoft Dynamics ERP-systemet, er transaktionsdetaljerne dog muligvis ikke tilgængelige i rapporter.

## <a name="create-a-report-definition"></a>Oprette en rapportdefinition
1. I Report Designer skal du klikke på **Ny** i menuen **Filer** og derefter vælge **Rapportdefinition**.
2. Angiv de relevante oplysninger under fanerne **Rapport**, **Output og distribution**, **Sidehoveder og sidefødder** og **Indstillinger**.

## <a name="contents-of-a-report-definition"></a>Indholdet af en rapportdefinition
Nedenstående tabel beskriver fanerne i en rapportdefinition, og hvordan oplysningerne bruges.

<table>
<thead>
<tr>
<th>Fane</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr>
<td>Rapport</td>
<td>Opret en rapport, konfigurer en rapport eller rediger en eksisterende rapport.</td>
</tr>
<tr>
<td>Output og distribution</td>
<td>Rediger rapportens outputtype og destination.</td>
</tr>
<tr>
<td>Sidehoveder og sidefødder</td>
<td>Definer og formater sidehovederne og sidefødderne til rapporten. Du kan for eksempel tilføje tekst eller billeder til sidehovedet eller sidefoden. Økonomirapportering understøtter .bmp-, .jpg- og .png-billedfiler. Du kan også tilføje autotekstkoder for at indsætte andre oplysninger, f.eks et firmanavn, rapportnavn eller sidetal.</td>
</tr>
<tr>
<td>Indstillinger</td>
<td>Angiv rapportdefinitionsindstillinger, f.eks. følgende indstillinger:
<ul>
<li>Formater og afrund beløb</li>
<li>Formater detaljerapporter</li>
<li>Formater rapporteringstræer</li>
<li>Generér en undtagelsesrapport</li>
<li>Angiv valutaomregning</li>
<li>Oplysninger og filtrer kontodetaljer</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Yderligere ressourcer

[Økonomirapportering](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
