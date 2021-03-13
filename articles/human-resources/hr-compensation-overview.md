---
title: Kompensationsplaner
description: Ledere for kompensation og frynsegoder kan bruge kompensationsstyring til at vedligeholde og behandle faste og variable lønstrukturer for organisationens medarbejdere.
author: andreabichsel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a5843b53ae857f1aa65491008c7f0970f20d53f5
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111863"
---
# <a name="compensation-plans"></a>Kompensationsplaner

Ledere for kompensation og frynsegoder kan bruge kompensationsstyring til at vedligeholde og behandle faste og variable lønstrukturer for organisationens medarbejdere.

### <a name="introduction"></a>Introduktion

Kompensationsstyring bruges til at styre fordelingen af grundløn og bonusser. En medarbejders faste grundløn og kvalifikationstillæg styres gennem faste lønstrukturer. Betalingen af incitamentsløn som f.eks. bonusudbetalinger, præstationsbonusser, aktieoptioner og tildelte aktier samt engangsbonusser styres ved hjælp af variable lønstrukturer. 

Medarbejdere kan knyttes til en eller flere strukturer af begge typer. En medarbejder skal opfylde følgende krav for at være berettiget til registrering i en lønstruktur:
-   Medarbejderen skal have en aktiv stillingstildeling.
-   Medarbejderen skal opfylde de kriterier, der er defineret af berettigelsesreglerne for en lønstruktur.

## <a name="compensation-setup"></a>Lønkonfiguration
Følgende tabel viser de komponenter i lønprocessen, der kan være integreret i konfigurationen af virksomhedens lønstrukturer.

<table>
<thead>
<tr class="header">
<th>Komponent</th>
<th>Flere oplysninger...</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Fast løn-handlinger</td>
<td>Fast løn-handlinger opfylder to formål:
<ul>
<li>Handlinger kan angive den type oplysninger, der skal registreres, når en medarbejders kompensation ændres. For eksempel kan du kræve, at årsagen til en ændring, f.eks en kampagne eller en sænkning, registreres.</li>
<li>Handlinger kan sikre, at der anvendes en beregning, når faste lønstrukturer behandles.  Handlinger af typen Egenkapital sammenligner for eksempel medarbejderlønnen med minimumreferencepunktet for niveauet af medarbejderens og sikrer, at medarbejderen bliver betalt mindst minimum.</li>
</ul></td>
</tr>
<tr class="even">
<td>Niveauer</td>
<td>Niveauer er tilknyttet job og eventuelle stillinger, der er relateret til en jobreference. Du kan oprette separate niveauer for de tre typer lønstrukturer: klasse, omfang eller trin.</td>
</tr>
<tr class="odd">
<td>Rammeudnyttelsesmatrix</td>
<td>En rammeudnyttelsesmatrix hjælper dig med at overføre medarbejdere til deres jobkontrolpunkt. Du kan også bruge rammeudnyttelse til at styre ligelønnen i virksomheden hensyn til den enkelte medarbejders præstation eller virksomhedens overordnede præstation. For eksempel får medarbejdere, der få laverer løn i deres lønramme, en større procentvis stigninger end medarbejdere, der får en højere løn i lønrammen. På denne måde kan du systematisk forskyde forskelle. Rammeudnyttelsen beregnes på følgende måde: (Fast lønsats - Rammeminimum) ÷ (Rammemaksimum - Rammeminimum).</td>
</tr>
<tr class="even">
<td>Opsætninger af referencepunkter</td>
<td>Opsætning af et referencepunkt omfatter et sæt referencepunkter, der repræsenterer intervaller i en matrix. Hver ramme kan tilknyttes en lønsats. Lønklassestrukturer har eksempelvis ofte referencepunkter for minimum, midtpunkt og maksimum.</td>
</tr>
<tr class="odd">
<td>Kompensationsmatrix</td>
<td>En kompensationsmatrix er det sæt referencepunkter og niveauer, du kan bruge til at oprette en lønstruktur.</td>
</tr>
<tr class="even">
<td>Kompensationsstruktur</td>
<td>En lønstruktur er en kompensationsmatrix med rammer, som har lønsatser, der er tilknyttet referencepunkterne for hvert niveau.</td>
</tr>
<tr class="odd">
<td>Berettigelsesregel</td>
<td>Berettigelsesregler bruges til at identificere medarbejdere i bestemte job, jobfunktioner, jobtyper, afdelinger, fagforeninger eller kompensationsområder, der er omfattet af specifikke lønstrukturer. Du skal oprette berettigelsesregler for både variable og faste lønstrukturer for at tilmelde medarbejdere til planen. Når du har angivet berettigelsesreglerne for en lønstruktur, kan du definere niveauer, der skal gælde for de jobs, der er dækket af strukturen.</td>
</tr>
<tr class="even">
<td>Lønfrekvenser</td>
<td>Lønfrekvenser bruges til at definere den periode, godtgørelsen er angivet for.  For eksempel hjælper lønfrekvensen dig med at forstå, om kompensationsbeløbet er angivet som en årslån eller en timeløn. Lønfrekvenser bruges også til at konfigurere omregningsfaktorer til konvertering af kompensationsbeløb fra pr. måned, uge, 14 dage og time til en årlig lønfrekvens.</td>
</tr>
<tr class="odd">
<td>Kompensationsområder</td>
<td>Kompensationsområder bruges til at angive medarbejderkompensation baseret på arbejdsstedets placering.</td>
</tr>
<tr class="even">
<td>Referencepunkt</td>
<td>Referencepunktet definerer, hvad du mener er den ideelle lønsats for alle medarbejdere på et kompensationsniveau. For planstrukturer for trin er referencepunkterne typisk rammens midtpunkt. Tværgående strukturer bruger sjældent kontrolpunkter. Du kan angive kontrolpunktet til en fast lønstruktur i formularen Faste lønstrukturer.</td>
</tr>
<tr class="odd">
<td>Jobfunktioner</td>
<td>Jobfunktioner, der bruges til at klassificere og filtrere kompensationsstrukturer til specifikke job.</td>
</tr>
<tr class="even">
<td>Jobtyper</td>
<td>Jobtyper, der bruges til at klassificere og filtrere kompensationsstrukturer til specifikke job.</td>
</tr>
<tr class="odd">
<td>Variable kompensationstyper</td>
<td>Variabel løn-typer, f.eks. kontantbonusser og aktiebonusser, konfigureres i variable lønstrukturer.</td>
</tr>
<tr class="even">
<td>Kompensationsgitre</td>
<td>Kompensationsgitre indeholder kompensationsstrukturen.  Kompensationsgitre kan bruges af en eller flere kompensationsplaner.</td>
</tr>
<tr class="odd">
<td>Performance-planer</td>
<td>Performance-planer bruges til at knytte performance til en fordelingsmatrix, så du kan bruge planen i en strategi for præstationsløn.</td>
</tr>
<tr class="even">
<td>Performance-rangeringer</td>
<td>Performance-rangeringer bruges i performanceplaner til at bestemme beløbet for en meritbonus eller en performancebonus.</td>
</tr>
</tbody>
</table>

## <a name="process-events"></a>Proceshændelser
En proceshændelse beregner lønoplysninger for en bestemt periode for alle medarbejdere, der er tilmeldt en eller flere strukturer for fast eller variabel løn. Du kan køre en proceshændelse gentagne gange for at teste eller opdatere beregnede lønresultater.

<a name="compensation-events"></a>Kompensationshændelser
-------------------

Hver gang en proceshændelse afvikles, oprettes der en kompensationshændelse.  Kompensationshændelser indeholder resultaterne af kompensationsprocessen for hver medarbejder, der er inkluderet i denne proceshændelse.  Når disse beregninger er korrekte, kan du indlæse kompensationshændelsen for at opdatere lønposterne for de medarbejdere, der er berørt af proceshændelsen.

## <a name="recommendations"></a>Anbefalinger
Når du har kørt en proceshændelse, kan du anbefale justeringer i en medarbejders meritforøgelse eller bonusbeløb baseret på de beregnede retningslinjer for proceshændelsen. For at angive anbefalinger for medarbejdere skal du aktivere anbefalinger, når du opretter lønstrukturer, eller når du konfigurerer proceshændelsen.



