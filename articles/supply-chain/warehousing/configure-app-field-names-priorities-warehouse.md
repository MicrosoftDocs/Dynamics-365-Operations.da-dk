---
title: Konfigurere felter til mobilappen Warehouse Management
description: Denne artikel beskriver, hvordan du definerer og konfigurerer feltnavne og prioriteter i mobilappen Warehouse Management.
author: Mirzaab
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 00a20faaa05a9d0891ee202951b1ca50d0176c83
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065952"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a>Konfigurere felter til mobilappen Warehouse Management

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du definerer og konfigurerer feltnavne og prioriteter i mobilappen Warehouse Management.

> [!NOTE]
> Denne artikel vedrører funktioner i Warehouse Management. Det gælder ikke for funktioner i Lagerstyring. Mobilappen Warehouse Management er et program, du kan bruge til at udføre opgaver i forbindelse med lagerstedet. Du kan definere og konfigurere de feltnavne, der bruges i appen, samt konfigurere den prioritet, der skal tildeles feltnavnene. Denne artikel beskriver, hvordan du definerer og konfigurerer disse feltnavne og prioriteter i mobilappen Warehouse Management, og hvordan de bruges.

## <a name="configure-warehouse-app-field-names"></a>Konfigurere feltnavne for lagerstedsapp

Når du bruger Lagersted på din mobilenhed, kan du konfigurere, hvordan metadata skal vises på din enhed på siden **Feltnavne for lagerstedsapp**. I et nyt firma skal du vælge **Opret standardopsætning** for at oprette alle de feltnavne, der skal bruges i arbejdsprocesser på mobilenheden til lagerstedet, og derefter tildele dem en foretrukken inputtilstand og inputtype. Når du har oprettet alle feltnavne, kan du vælge følgende indstillinger for input.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Indstilling</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Foretrukket inputtilstand</td>
<td>Denne indstilling angiver, om et scanningsfelt eller et inputfelt til manuel indtastning skal vises for det valgte feltnavn. Det er nyttigt at skelne mellem felterne ud fra, om der bruges stregkoder til feltet. <strong>Bemærk:</strong> For feltnavne, hvor den foretrukne inputtilstand er indstillet til <strong>Scanning</strong>, kan du angive oplysningerne manuelt, hvis stregkoden er ikke kan læses eller er beskadiget.</td>
</tr>
<tr class="even">
<td>Inputtype</td>
<td>Denne indstilling definerer, hvilke inputtype der skal bruges til navnet på det valgte felt. Der er fire valgmuligheder:
<ul>
<li><strong>Valg</strong> - Indeholder en liste over indstillinger at vælge imellem. Feltnavne med denne indstilling kan ikke redigeres.</li>
<li><strong>Dato</strong> - Feltnavne, der er angivet som dato, viser et datoformat i etiketten. Dette hjælper lagermedarbejdere med at se, hvilket format datoen skal indtastes i. Feltnavne med denne indstilling kan ikke redigeres.</li>
<li><strong>Alfa</strong> - Hvis denne indstilling er valgt, bruges tastaturet, når du indtaster oplysninger i programmet manuelt. Tastaturoplevelsen kan ændres, afhængigt af hvilken enhed der bruges.</li>
<li><strong>Numerisk</strong> - Til feltnavne, der kun bruger numerisk input, kan du vælge denne indstilling for at få vist et brugerdefineret numerisk tastatur med inputfelt i stedet for tastaturet på enheden.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a>Konfigurere feltprioritet for lagerstedsapp

På siden **Feltprioritet for lagerstedsapp** kan du placere feltnavnene i forskellige prioriterede grupper. Dette gør det muligt at afgøre, hvilke oplysninger der vises på siden for hovedopgaven, når lagermedarbejderne udfører opgaver ved hjælp af programmet. Hvis du klikker på **Opret standardopsætning**, oprettes et standardsæt af prioriterede grupper. Det er muligt at oprette så mange prioriterede grupper som ønsket, men kun tre prioriterede grupper vil blive vist på opgavesiden. Når systemet sender metadata til programmet, tildeler det hvert felt en relativ prioritet afhængigt af dets prioriterede gruppe, og appen viser de tre første højt prioriterede grupper, der er indeholdt i metadataene på opgavesiden. Resten af overløbsmetadataene vises på en side med sekundære oplysninger. Følgende tabel viser et eksempel på fem prioriterede grupper.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Prioritetsgruppe</th>
<th>Tildelte felter</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> Prioritet 10</td>
<td><ul>
<li>Post</li>
<li>Mængde</li>
<li>Måleenhed</li>
</ul></td>
</tr>
<tr class="even">
<td> Prioritet 20</td>
<td><ul>
<li>Klyngeplacering</li>
<li>Klynge</li>
</ul></td>
</tr>
<tr class="odd">
<td> Prioritet 30</td>
<td><ul>
<li>Varebeskrivelse</li>
</ul></td>
</tr>
<tr class="even">
<td> Prioritet 40</td>
<td><ul>
<li>Variantkonfiguration</li>
<li>Farve</li>
<li>Størrelse</li>
<li>Skabelon</li>
</ul></td>
</tr>
<tr class="odd">
<td> Prioritet 50</td>
<td><ul>
<li>Placering</li>
<li>Nummerplade</li>
</ul></td>
</tr>
</tbody>
</table>

For eksempel når en lagermedarbejder udfører en opgave på en mobilenhed, hvis de metadata, der bliver vist i appen, består af følgende felter:

-   Post
-   Mængde
-   Måleenhed
-   Varebeskrivelse
-   Størrelse og sted

Baseret på den feltprioritet i lagerstedsappen, der er angivet i ovenstående tabel, vises følgende 3 rækker af oplysninger på opgavesiden:

-   Række 1: Vare, Antal, Måleenhed
-   Række 2: Beskrivelse af varen
-   Række 3: Størrelse

De resterende metadata, f.eks. placering, vises ikke på opgavesiden, men vises på en side med oplysninger. Hvis du vil vide mere og se eksempler på brugergrænsefladen, kan du se i blogindlægget [Præsentation af Dynamics 365 Supply Chain Management – Lagersted](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

## <a name="additional-resources"></a>Yderligere ressourcer

[Installere og tilslutte mobilapp til lagerstedsadministration](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
