---
title: Angiv kombinationer af konto og dimension (segmenteret postkontrolelement)
description: I denne artikel beskrives det, hvordan du indtaster kontoen og dimensionskombinationer eller finanskonti. Indtastningshandlingen kaldes ofte segmenteret postkontrolelement.
author: aprilolson
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fca993294327e6742a11203255a187f8456e2921
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715268"
---
# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a>Angiv kombinationer af konto og dimension (segmenteret postkontrolelement)

[!include [banner](../includes/banner.md)]

I denne artikel beskrives det, hvordan du indtaster kontoen og dimensionskombinationer eller finanskonti. Indtastningshandlingen kaldes ofte segmenteret postkontrolelement.

Brugere angiver kombinationer af konto og dimension på forskellige sider, f.eks. sider til finanskladder, budgettering og bogføringsdefinitioner. Gyldige kombinationer af konto og dimension afhænger af de kontostrukturer, der er tildelt finans og de avancerede regler, der er tildelt kontostrukturerne. Når brugerne indtaster en kombination, kan de enten manuelt indtaste værdierne eller drage fordel af omfattende opslagsmuligheder. Når du angiver feltet, kan du begynde at skrive, og derefter søger det efter værdien og beskrivelsen. For eksempel hvis du skriver 180 søger det efter enhver værdi, der begynder med denne talkombination. Eller du kan skrive kontanter, hvorefter det søger efter enhver værdi, som har en beskrivelse, der begynder med kontanter. Du kan også bruge jokertegn, f.eks. \*kontant eller \*180 til at søge, hvis værdien eller beskrivelsen indeholder søgekriterierne. 

I følgende tabel beskriver de tastaturgenveje, der kan bruges, når opslaget er lukket.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tastaturgenvej</th>
<th>Handling</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Alt+pil ned</td>
<td>Åbn opslaget. Hvis du trykker på Alt + pil ned igen, flyttes fokus til segmenter i pop op-vinduet.</td>
</tr>
<tr class="even">
<td><ul>
<li>Enter og Skift + Enter</li>
<li>Afgrænser til kontoplan</li>
<li>Højre pil og venstre pil</li>
</ul></td>
<td>Flyt til næste eller forrige segment.</td>
</tr>
<tr class="odd">
<td>Fane</td>
<td>Flyt til næste felt i gitteret.</td>
</tr>
</tbody>
</table>

I følgende tabel beskriver de tastaturgenveje, der kan bruges, når opslaget er åbent.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tastaturgenvej</th>
<th>Handling</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Esc</td>
<td>Luk opslaget.</td>
</tr>
<tr class="even">
<td><ul>
<li>Pil op og pil ned</li>
<li>Page Up og Page Down</li>
<li>Home og End</li>
</ul></td>
<td>Flyt til forrige eller næste værdi på listerne, til den forrige eller næste gruppe af værdier eller til det første eller sidste element i opslaget.</td>
</tr>
<tr class="odd">
<td><ul>
<li>Afgrænser til kontoplan</li>
<li>Højre pil og venstre pil</li>
</ul></td>
<td>Flyt til næste eller forrige segment.</td>
</tr>
<tr class="even">
<td>Fane</td>
<td>Flyt til næste felt i gitteret.</td>
</tr>
<tr class="odd">
<td>Alt+W</td>
<td>Skift mellem <strong>Vis alle</strong> og <strong>Vis gyldige</strong>.</td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
