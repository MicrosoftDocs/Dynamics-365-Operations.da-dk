---
title: Konfigurere app feltnavne i Logistik app
description: Dette emne beskriver, hvordan du definere og konfigurere lagerstedet app feltnavne og prioriteter i Dynamics 365 for operationer.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: ce8f6d6f7090995bc44db1ba0103a7d6c0416620
ms.lasthandoff: 03/31/2017


---

# <a name="configure-app-field-names-in-warehousing-app"></a>Konfigurere app feltnavne i Logistik app

Dette emne beskriver, hvordan du definere og konfigurere lagerstedet app feltnavne og prioriteter i Dynamics 365 for operationer. 

**Bemærk:** dette emne gælder for funktionerne i Logistik. Det gælder ikke for funktioner i Lagerstyring. Dynamics 365 for operationer - lager er et program, du kan bruge til at udføre opgaver på lagerstedet. Du kan definere og konfigurere de feltnavne, der bruges i programmet, samt konfigurere den prioritet, der skal tildeles feltnavnene. Dette emne forklarer, hvordan du definerer og konfigurerer disse lagersted app feltnavne og prioriteter, og hvordan de bruges i Dynamics 365 for operationer - lager. Yderligere oplysninger om at konfigurere forbindelsen til Dynamics 365 for operationer - oplagring, henvise til selvstudiet [installere og konfigurere Dynamics 365 for operationer - opbevaring](install-configure-warehousing-app.md).

<a name="configure-warehouse-app-field-names"></a>Konfigurere lagerstedet app feltnavne
===================================

Når du bruger Dynamics 365 for operationer - opbevaring på din mobilenhed, kan du konfigurere hvordan metadata skal vises på enheden på den **lagersted app feltnavne** side. Marker i et nyt regnskab i Dynamics 365 for operationer, **Opret standardopsætning** til at oprette alle de feltnavne, der skal bruges på lagerstedet mobilenhed arbejdsprocesser, og derefter tildele en foretrukken tilstand for input og Inputtype til dem. Når du har oprettet alle feltnavne, kan du vælge følgende indstillinger for input.

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
<td>Denne indstilling angiver, om en scanning felt eller en manuel indtastning inputfelt skal vises for det markerede feltnavn. Dette er nyttigt at skelne felterne afhængigt af, hvis der bruges stregkoder til feltet. <strong>Bemærk:</strong> For feltnavnene med foretrukne inputtilstanden er angivet til <strong>Scanning</strong>, kan du angive oplysningerne manuelt, hvis stregkoden er ikke kan læses eller er beskadiget.</td>
</tr>
<tr class="even">
<td>Inputtype</td>
<td>Denne indstilling definerer, hvilke input-typen, der skal bruges til navnet på det valgte felt. Der er fire muligheder:
<ul>
<li><strong>Valg af</strong> - indeholder en liste over indstillinger at vælge imellem. Feltnavne med denne indstilling kan ikke redigeres.</li>
<li><strong>Dato</strong> - feltnavne, der er angivet som dato viser et datoformat med etiketten. Dette hjælper med at lagermedarbejdere, se, i hvilket format du skal indtaste datoen. Feltnavne med denne indstilling kan ikke redigeres.</li>
<li><strong>Alpha</strong> - Hvis markeret, tastaturet enhed der skal bruges ved manuelt at indtaste oplysninger i programmet. Tastatur-oplevelse kan ændres afhængigt af, hvilken enhed der bruges.</li>
<li><strong>Numeriske</strong> - til feltnavne, Brug numeriske kun input, kan du vælge denne indstilling for at få vist et brugerdefineret numerisk tastatur med inputfelt i stedet for tastaturet for enheden.</li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a>Konfigurere lagerstedet app feltet Prioritet
======================================

På den **lagersted app feltet Prioritet** side, kan du placere feltnavnene i forskellige prioriterede grupper. Dette gør det muligt at afgøre, hvilke oplysninger der vises på siden vigtigste opgave når lagermedarbejderne udføre opgaver ved hjælp af programmet. Hvis du klikker på **Opret standardopsætning**, der skal oprettes et standardsæt af prioriterede grupper. Det er muligt at oprette så mange prioriterede grupper efter behov, men kun tre prioriterede grupper vil blive vist på siden opgave. Når Dynamics 365 for operationer sender metadataene til programmet, det tildeler hvert felt en relative prioritet afhængigt af dets prioritet gruppe og programmet viser de første tre højt prioriterede grupper, der er indeholdt i metadata på siden opgave. Resten af standardsidelayoutet metadata vises på en side med sekundære oplysninger. Følgende tabel viser et eksempel på fem prioriterede grupper.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Prioriteret gruppe</th>
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

For eksempel når en lagermedarbejder udfører en opgave på en mobilenhed, hvis de metadata, der vises i programmet består af følgende felter:

-   Post
-   Mængde
-   Måleenhed
-   Varebeskrivelse
-   Størrelse og placering

Baseret på den lagersted app feltet prioritet, der er angivet i ovenstående tabel, vises følgende 3 rækker af oplysninger, der på siden opgaver:

-   Række 1: Vare, antal, enhed
-   Række 2: Beskrivelse
-   Række 3: størrelse

De resterende metadata, placering, vises ikke på siden opgave, men der vises på en side med oplysninger. Hvis du vil vide mere og se eksempler på brugergrænsefladen, henvise til blogindlægget [annoncerer Dynamics 365 for operationer - opbevaring](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

<a name="see-also"></a>Se også
--------

[Installere og konfigurere Microsoft Dynamics 365 for operationer – opbevaring](install-configure-warehousing-app.md)


