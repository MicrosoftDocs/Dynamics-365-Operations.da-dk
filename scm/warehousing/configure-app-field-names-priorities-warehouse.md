---
title: Konfigurere appfeltnavne i lagerstedsappen
description: I dette emne beskrives, hvordan du definerer og konfigurerer feltnavne og prioriteter i lagerstedsapp i Finance and Operations.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 49db5ad10914897b2157e123c5803ca51e4e66e7
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017

---

# <a name="configure-app-field-names-in-warehousing-app"></a>Konfigurere appfeltnavne i lagerstedsappen

[!include[banner](../includes/banner.md)]


I dette emne beskrives, hvordan du definerer og konfigurerer feltnavne og prioriteter i lagerstedsapp i Finance and Operations. 

**Bemærk!** Denne emne gælder for funktioner i Lagerstedsstyring. Det gælder ikke for funktioner i Lagerstyring. Finance and Operations - Lagersted er et program, du kan bruge til at udføre opgaver i forbindelse med lagerstedet. Du kan definere og konfigurere de feltnavne, der bruges i appen, samt konfigurere den prioritet, der skal tildeles feltnavnene. I dette emne beskrives, hvordan du definerer og konfigurerer disse feltnavne og prioriteter i lagerstedsappen, og hvordan de bruges i Finance and Operations - Lagersted. Du kan finde flere oplysninger om at konfigurere forbindelsen til Finance and Operations - Lagersted i selvstudiet [Installere og konfigurere Finance and Operations - Lagersted](install-configure-warehousing-app.md).

<a name="configure-warehouse-app-field-names"></a>Konfigurere feltnavne for lagerstedsapp
===================================

Når du bruger Finance and Operations - Lagersted på din mobilenhed, kan du konfigurere, hvordan metadata skal vises på din enhed på siden **Feltnavne for lagerstedsapp**. I et nyt regnskab i Finance and Operations skal du vælge **Opret standardopsætning** for at oprette alle de feltnavne, der skal bruges i arbejdsprocesser på mobilenheden til lagerstedet, og derefter tildele dem en foretrukken inputtilstand og inputtype. Når du har oprettet alle feltnavne, kan du vælge følgende indstillinger for input.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Indstilling</th>
<th>Betegnelse</th>
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
<li><strong>Alfa</strong> - Hvis denne indstilling er valg, bruges tastaturet, når du indtaster oplysninger i programmet manuelt. Tastaturoplevelsen kan ændres, afhængigt af hvilken enhed der bruges.</li>
<li><strong>Numerisk</strong> - Til feltnavne, der kun bruger numerisk input, kan du vælge denne indstilling for at få vist et brugerdefineret numerisk tastatur med inputfelt i stedet for tastaturet på enheden.</li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a>Konfigurere feltprioritet for lagerstedsapp
======================================

På siden **Feltprioritet for lagerstedsapp** kan du placere feltnavnene i forskellige prioriterede grupper. Dette gør det muligt at afgøre, hvilke oplysninger der vises på siden for hovedopgaven, når lagermedarbejderne udfører opgaver ved hjælp af programmet. Hvis du klikker på **Opret standardopsætning**, oprettes et standardsæt af prioriterede grupper. Det er muligt at oprette så mange prioriterede grupper som ønsket, men kun tre prioriterede grupper vil blive vist på opgavesiden. Når Finance and Operations sender metadata til programmet, tildeler det hvert felt en relativ prioritet afhængigt af dets prioriterede gruppe, og appen viser de tre første højt prioriterede grupper, der er indeholdt i metadataene på opgavesiden. Resten af overløbsmetadataene vises på en side med sekundære oplysninger. Følgende tabel viser et eksempel på fem prioriterede grupper.

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

De resterende metadata, f.eks. placering, vises ikke på opgavesiden, men vises på en side med oplysninger. Hvis du vil vide mere og se eksempler på brugergrænsefladen, kan du se i blogindlægget [Præsentation af Finance and Operations - Lagersted](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

<a name="see-also"></a>Se også
--------

[Installere og konfigurere Microsoft Dynamics 365 for Finance and Operations – Lagersted](install-configure-warehousing-app.md)




