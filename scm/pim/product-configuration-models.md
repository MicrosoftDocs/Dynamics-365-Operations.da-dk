---
title: Oversigt over produktkonfigurationsmodeller
description: Denne artikel definerer termer og begreber, der er relevante for produktkonfigurationsmodeller. Med produktkonfigurationsmodeller kan du bygge en generisk produktstruktur, som kan bruges til at konfigurere mange produktvarianter for et enkelt produkt.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 4031
ms.assetid: 70b968e8-e550-4731-823d-d713b8910f7b
ms.search.region: Global
ms.author: yuyus
ms.dyn365.intro: Feb-16
ms.dyn365.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 30580b059a4c240ad540a9c347b0551df0ab5c02
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="product-configuration-models-overview"></a>Oversigt over produktkonfigurationsmodeller

[!include[banner](../includes/banner.md)]


Denne artikel definerer termer og begreber, der er relevante for produktkonfigurationsmodeller. Med produktkonfigurationsmodeller kan du bygge en generisk produktstruktur, som kan bruges til at konfigurere mange produktvarianter for et enkelt produkt.

Produktkonfigurationsmodeller oprettes for at repræsentere en generisk produktstruktur. Når du har oprettet en produktkonfigurationsmodel, kan du konfigurere en distinkt produktvariant med en entydig stykliste (BOM) og en entydig rute. Produktkonfigurationsmodeller bruger både deklarative begrænsninger og afgørende beregninger til at håndtere relationer og begrænsninger mellem forskellige produktvarianter. Du kan konfigurere varer på salgsordrer, salgstilbud, indkøbsordrer og produktionsordrer. Følgende tabel indeholder en beskrivelse af de begrænsningsbaserede termer og begreber.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Komponenter</td>
<td>Komponenter er de vigtigste byggesten i en produktkonfigurationsmodel. Komponenter vises i en træstruktur på siden <strong>Detaljer om begrænsningsbaseret model til produktkonfiguration</strong>. Komponenter kan indeholde følgende elementer:
<ul>
<li>Egenskaber</li>
<li>Begrænsninger</li>
<li>Beregninger</li>
<li>Underkomponenter</li>
<li>Brugerkrav</li>
<li>Styklistelinjer</li>
<li>Ruteoperationer</li>
</ul></td>
</tr>
<tr class="even">
<td>Attributter</td>
<td>Attributter beskriver alle funktioner i produktkonfigurationsmodellen. Du kan bruge attributter til at angive de funktioner, der kan vælges, når et bestemt produkt skal konfigureres. Attributter bruges i begrænsninger og betingelser. Når attributter oprettes og føjes til en produktkonfigurationsmodel, refereres til de relaterede attributtyper. Der kan angives en standardværdi for en attribut. Standardværdien bruges i konfigurationsbrugergrænsefladen (UI), når produktkonfigurationsmodellen konfigureres. Du kan angive, at en attribut er obligatorisk, skrivebeskyttet eller skjult.
<ul>
<li><strong>Tvungen</strong> – Der skal angives en værdi for attributten, når produktet konfigureres.</li>
<li><strong>Skrivebeskyttet</strong> – Attributværdien vises under konfigurationen, men den kan ikke ændres.</li>
<li><strong>Skjult</strong> – Attributværdien medtages i begrænsninger og betingelser, men den vises ikke under konfigurationen.</li>
</ul>
Du kan også angive en betingelse for attributter. Hvis betingelsen er opfyldt, skal der angives en værdi for den obligatoriske attribut. Betingelser er udtryk, der skal opfyldes for attributter, styklistelinjer og ruteoperationer, der skal medtages i en produktkonfigurationsmodel. Alle attributter, der refereres til i en betingelse, bliver tvungne. Det anbefales, at du vælger attributter som tvungne under fanen <strong>Attributter</strong>. Det kan gøre det nemmere at identificere de obligatoriske attributter. Attributværdier er en vigtig del af genbrug af konfigurationer. Systemet bruger attributværdier for at fastslå, om der findes en konfiguration, der svarer til de valg, som en bruger har foretaget under en konfiguration.</td>
</tr>
<tr class="odd">
<td>Attributtyper</td>
<td>Attributtyper angiver det sæt datatyper til attributter, der bruges i en produktkonfigurationsmodel. Der anvendes følgende attributtyper:
<ul>
<li><strong>Heltal</strong> med eller uden et område</li>
<li><strong>Decimal</strong></li>
<li><strong>Tekst</strong> med eller uden en fast liste</li>
<li><strong>Boolesk</strong></li>
</ul>
Hvis attributtypen er <strong>Boolesk</strong>, <strong>Heltal</strong> med et interval eller <strong>Tekst</strong> med en fast liste, er værdisættet tilgængeligt, når en produktkonfigurationsmodel er sat op. <strong>Bemærk!</strong> Produktkonfigurationsproblemløseren genkender kun følgende attributtyper: <strong>Boolesk</strong>, <strong>Tekst</strong> med en fast liste og <strong>Heltal</strong> med et område. Derfor er det udelukkende disse attributtyper, der kan bruges i udtryksbegrænsninger og betingelser.</td>
</tr>
<tr class="even">
<td>Begrænsninger</td>
<td>Begrænsninger beskriver begrænsninger i produktmodelkonfigurationen. Begrænsninger bruges til at sikre, at der kun vælges gyldige værdier, når et produkt konfigureres. Begrænsninger kan enten være udtryksbegrænsninger eller tabelbegrænsninger:
<ul>
<li>Udtryksbegrænsninger kan kun anvendes til den komponent, som de er knyttet til. Udtryksbegrænsninger for en komponent kan dog henvise til attributter for komponentens underkomponenter. Produktkonfigurationsproblemløseren bruges til at løse begrænsningerne, og du bruge problemløsersyntaksen, når du skriver begrænsningerne. Du kan finde flere oplysninger under linket i emnet om udtryksbegrænsninger og tabelbegrænsninger.</li>
<li>Tabelbegrænsninger skal defineres, før de kan anvendes til en komponent i en produktkonfigurationsmodel. Tabelbegrænsninger kan enten være brugerdefinerede eller systemdefinerede. En begrænsning for en brugerdefineret tabel er en matrixtype, der kan bruges til at beskrive sæt af kombinationer af de attributværdier, der er defineret af attributtyper. Hvis der f.eks. produceres højttalere, indeholder matricen for en brugerdefineret tabelbegrænsning muligvis kolonner for højttalerfinish og gitter.</li>
</ul>
<strong>Eksempel</strong> Højttalere fås med fire finishes: sort, egetræ, rosentræ og hvid. Højttalerne kan have et af tre frontgitre: sort, metal eller hvid. Sort finish er tilgængelig for alle gitre, men de andre overfladematerialer er begrænset til bestemte gitre. Følgende tabel viser et eksempel på de oplysninger, der vises under fanen <strong>Tilladte kombinationer</strong> på siden <strong>Rediger tabelbegrænsning</strong>.
<table>
<thead>
<tr class="header">
<th>Kabinetfinish</th>
<th>Frontgitter</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Sort</td>
<td>Sort</td>
</tr>
<tr class="even">
<td>Sort</td>
<td>Metal</td>
</tr>
<tr class="odd">
<td>Sort</td>
<td>Hvid</td>
</tr>
<tr class="even">
<td>Egetræ</td>
<td>Sort</td>
</tr>
<tr class="odd">
<td>Rosentræ</td>
<td>Hvid</td>
</tr>
<tr class="even">
<td>Hvid</td>
<td>Sort</td>
</tr>
<tr class="odd">
<td>Hvid</td>
<td>Hvid</td>
</tr>
</tbody>
</table>
En systemdefineret tabelbegrænsning repræsenterer en tilknytning mellem en attributtype og et felt i en Dynamics 365 for Operations-tabel. En systemdefineret tabelbegrænsning sammenkæder dynamisk attributtypen med feltet. Via linket kan attributten i en produktkonfigurationsmodel afspejle data i feltet i Dynamics 365 for Operations-tabellen.</td>
</tr>
<tr class="odd">
<td>Beregninger</td>
<td>Beregninger udgør et supplement til begrænsninger. Du kan bruge en beregning til at udføre aritmetiske operationer på attributterne for typen <strong>Decimal</strong> og typen <strong>Heltal</strong> eller logiske operationer, der vedrører attributter for typen <strong>Tekst</strong> med en fast liste og typen <strong>Boolesk</strong>. En beregning har en målattribut, der skal indeholde resultatet af beregningsudtrykket. Beregningsudtrykket opbygges ved hjælp af udtrykseditoren.</td>
</tr>
<tr class="even">
<td>Underkomponenter</td>
<td>Underkomponenter afspejler træstrukturen for produktkonfigurationsmodellen. Du kan bruge underkomponenter til at opbygge strukturen for en produktkonfigurationsmodel. Underkomponenter henviser til eksisterende komponenter. Derfor motiverer brugen af underkomponenter til genbrug af komponenter i flere produktkonfigurationsmodeller. På siden <strong>Linjedetaljer i stykliste</strong> for en underkomponent kan du vælge en særskilt værdi for underkomponenten. Du kan også vælge en attribut, som værdien vælges for under opsætning af produktkonfigurationsmodellen. Hvis du vil medtage et produkt som en komponent eller en underkomponent, skal du angive følgende oplysninger på siden <strong>Opret produkt</strong>, når du opretter produktet:
<ul>
<li>Vælg en <strong>Vare</strong> i feltet <strong>Produkttype</strong>.</li>
<li>Vælg <strong>Produktmaster</strong> i feltet <strong>Produktundertype</strong>.</li>
<li>Vælg <strong>Begrænsningsbaseret konfiguration</strong> i feltet <strong>Konfigurationsteknologi</strong>.</li>
</ul>
Du kan få vist, om et frigivet produkt kan bruges som en komponent eller underkomponenter under fanen <strong>Generelt</strong> på siden <strong>Frigivne produktdetaljer</strong>. Hvis <strong>Begrænsningsbaseret konfiguration</strong> er valgt i feltet <strong>Konfigurationsteknologi</strong>, kan produktet bruges som en komponent eller en underkomponent. Du kan skjule underkomponenter, så de ikke vises for brugeren under en konfigurationssession. Attributter, underkomponenter og brugerkrav, der vedrører underkomponenten, skjules også.</td>
</tr>
<tr class="odd">
<td>Brugerkrav</td>
<td>Brugerkrav repræsenterer en abstraktion mellem brugerkrav og bestemte komponenter og attributter. Et brugerkrav kan ikke knyttes til en vare. Forestil dig f.eks., at en kunde ønsker at købe et hjemmebiografsystem. Sælgeren spørger muligvis om størrelsen på det rum, hvor kunden vil have systemet, for at fastslå, hvor mange watt der er påkrævet. I dette eksempel kan rummets størrelse være et brugerkrav, der hjælper med at finde den relevante attributværdi for en bestemt komponent. Du kan skjule brugerkrav, så de ikke vises for brugeren under en konfigurationssession. Attributter, underkomponenter og brugerkrav, der vedrører brugerkrav, skjules også. Du kan skrive en betingelse for at styre, om et brugerkrav kan skjules. Du skal bruge OML-syntaksen (Optimization Modeling Language), når du skriver betingelsen.</td>
</tr>
<tr class="even">
<td>Styklistelinjer</td>
<td>Styklistelinjer repræsenterer separate materialer af komponenterne i produktkonfigurationsmodellen. På siden <strong>Linjedetaljer i stykliste</strong> kan alle elementer vælges. En betingelse kan føjes til styklistelinjen, så de styklistelinjer, der er valgt for en bestemt produktvariant kan variere, baseret på brugerens valg, når produktkonfigurationsmodellen angives. Betingelser er udtryk, der skal opfyldes for attributter, styklistelinjer og ruteoperationer, der skal medtages i en produktkonfigurationsmodel. På siden <strong>Linjedetaljer i stykliste</strong> kan du vælge en bestemt værdi. Du kan også oprette en tilknytning til en attribut, som værdien vælges for under opsætning af produktkonfigurationsmodellen.</td>
</tr>
<tr class="odd">
<td>Ruteoperationer</td>
<td>På siden <strong>Oplysninger om ruteoperation</strong> kan du vælge en bestemt værdi. Du kan også oprette en tilknytning til en attribut, som værdien vælges for under opsætning af produktkonfigurationsmodellen. Betingelser skrives som udtryksbegrænsninger. Betingelser er udtryk, der skal opfyldes for attributter, styklistelinjer og ruteoperationer, der skal medtages i en produktkonfigurationsmodel.</td>
</tr>
</tbody>
</table>






