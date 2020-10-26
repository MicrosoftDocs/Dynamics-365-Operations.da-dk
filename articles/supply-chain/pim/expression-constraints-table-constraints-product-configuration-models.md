---
title: Udtryksbegrænsninger og tabelbegrænsninger i produktkonfigurationsmodeller
description: I dette emne beskrives brugen af udtryksbegrænsninger og tabelbegrænsninger. Begrænsninger styrer de attributværdier, som du kan vælge, når du konfigurerer produkter til en salgsordre, et salgstilbud, en indkøbsordre eller en produktionsordre. Du kan bruge udtryksbegrænsninger eller tabelbegrænsninger, afhængigt af hvordan du foretrækker at udforme begrænsninger.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be9d9ae48d21db077928ba7bd5615fea47ea5181
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979822"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a>Udtryksbegrænsninger og tabelbegrænsninger i produktkonfigurationsmodeller

[!include [banner](../includes/banner.md)]

I dette emne beskrives brugen af udtryksbegrænsninger og tabelbegrænsninger. Begrænsninger styrer de attributværdier, som du kan vælge, når du konfigurerer produkter til en salgsordre, et salgstilbud, en indkøbsordre eller en produktionsordre. Du kan bruge udtryksbegrænsninger eller tabelbegrænsninger, afhængigt af hvordan du foretrækker at udforme begrænsninger. 

Begrænsninger bruges til at styre de attributværdier, som du kan vælge, når du konfigurerer produkter til en salgsordre, et salgstilbud, en indkøbsordre eller en produktionsordre. Du kan bruge udtryksbegrænsninger eller tabelbegrænsninger, afhængigt af hvordan du foretrækker at udforme begrænsninger.

## <a name="what-are-expression-constraints"></a>Hvad er udtryksbegrænsninger?
Udtryksbegrænsninger er kendetegnet ved et udtryk, der bruger de aritmetiske og booleske operatorer og funktioner. En udtryksbegrænsning skrives til en bestemt komponent i en produktkonfigurationsmodel. Den kan ikke genbruges af eller deles med en anden komponent. Udtryksbegrænsninger for en komponent kan dog henvise til attributter for komponentens underkomponenter.

## <a name="what-are-table-constraints"></a>Hvad er tabelbegrænsninger?
Tabelbegrænsninger viser kombinationerne af de værdi, der er tilladt for attributter, når du konfigurerer et produkt. Definitioner på tabelbegrænsninger kan anvendes generisk. Når du opretter en tabelbegrænsning for en komponent i en produktkonfigurationsmodel, skal du vælge en definition på en tabelbegrænsning. Hvis du vil oprette kombinationer, der er tilladt, skal du føje attributter af bestemte typer til komponenterne. Hver attributtype har en bestemt værdi.

### <a name="example-of-a-table-constraint"></a>Eksempel på tabelbegrænsning

Dette eksempel viser, hvordan du kan begrænse konfigurationen af en højttaler til bestemte kabinetfinishes og fronter. I den første tabel vises de kabinetfinishes og fronter, der normalt er tilgængelige til konfiguration. Værdierne er defineret for attributtyperne **Kabinetfinish** og **Frontgitter**.

| Attributtype | Værdier                      |
|----------------|-----------------------------|
| Kabinetfinish | Sort, egetræ, rosentræ, hvid |
| Frontgitter    | Sort, metal, hvid         |

I næste tabel vises de kombinationer, der er defineret af tabel begrænsningen **Farve og finish**. Ved hjælp af denne tabelbegrænsning kan du konfigurere en højttaler, der har en finish i egetræ og et sort gitter, en finish i rosentræ og et hvidt gitter og så videre.

| Afslut         | Gitter                       |
|----------------|-----------------------------|
| Egetræ            | Sort                       |
| Rosentræ       | Hvid                       |
| Hvid          | Sort                       |
| Hvid          | Hvid                       |
| Sort          | Sort                       |
| Sort          | Metal                       | 

Du kan oprette systemdefinerede og brugerdefinerede tabelbegrænsninger. Du kan finde flere oplysninger under [Systemdefinerede og brugerdefinerede tabelbegrænsninger](system-defined-user-defined-table-constraints.md).

## <a name="what-syntax-should-be-used-to-write-constraints"></a>Hvilken syntaks skal der bruges til at skrive begrænsninger?
Du skal bruge OML-syntaksen, når du skriver begrænsninger. Systemet bruger Microsoft Solver Foundation-begrænsningsløseren til at løse begrænsningerne.

## <a name="should-i-use-table-constraints-or-expression-constraints"></a>Skal jeg bruge tabelbegrænsninger eller udtryksbegrænsninger?
Du kan enten bruge udtryksbegrænsninger eller tabelbegrænsninger, afhængigt af hvordan du foretrækker at konfigurere begrænsninger. Du udformer en tabelbegrænsning som en matrix, hvorimod en udtryksbegrænsning er en enkelt sætning. Når du konfigurerer et produkt, betyder det ikke noget, hvilken slags begrænsning der bruges. I følgende eksempel kan du se, hvordan de to metoder adskiller sig fra hinanden.  

Når du konfigurerer et produkt ved hjælp af følgende begrænsnings, er disse kombinationer tilladt:

-   Et produkt i farven sort og i størrelsen 30 eller 50
-   Et produkt i farven rød og i størrelsen 20

### <a name="table-constraint-setup"></a>Konfiguration af tabelbegrænsning

| Farve | Størrelse |
|-------|------|
| Sort | 30   |
| Sort | 50   |
| Rød   | 20   |

### <a name="expression-constraint-setup"></a>Konfiguration af udtryksbegrænsning

(Color == "Sort" & (size == "30" | size == "50")) | (color == "Rød" & size = "20")

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a>Skal jeg bruge operatorer eller infix-anmærkning, når jeg skriver udtryksbegrænsninger?
Du kan skrive en udtryksbegrænsning enten ved hjælp af de tilgængelige præfiksoperatorer eller ved hjælp af infix-anmærkningen. Du kan ikke bruge infix-anmærkningen for operatorerne **Min**, **Max** og **Abs**. Disse operatorer er inkluderet som standardoperatorer i de fleste programmeringssprog.

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a>Hvilke operatorer og hvilken infix-anmærkning kan jeg bruge, når jeg skriver udtryksbegrænsninger?
I følgende tabeller vises de operatorer og den infix-anmærkning, som du kan bruge, når du skriver en udtryksbegrænsning for en komponent i en produktkonfigurationsmodel. I eksemplerne i den første tabel kan du se, hvordan du skriver et udtryk ved hjælp af infix-anmærkningen eller operatorer.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Operatør</th>
<th>Beskrivelse</th>
<th>Syntaks</th>
<th>Eksempler</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Indebærer</td>
<td>Dette er tilfældet, hvis den første betingelse er falsk, den anden betingelse er sand, eller begge dele.</td>
<td>Implies[a, b], infix: a -: b</td>
<td><ul>
<li><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</li>
<li><strong>Infix-anmærkning:</strong> x != 0 -: y &gt;= 0</li>
</ul></td>
</tr>
<tr class="even">
<td>Og</td>
<td>Dette gælder kun, hvis alle betingelser er opfyldt. Hvis antallet af betingelser er 0 (nul), returneres <strong>True</strong>.</td>
<td>And[args], infix: a &amp; b &amp; ... &amp; z</td>
<td><ul>
<li><strong>Operator:</strong> And[x == 2, y &lt;= 2]</li>
<li><strong>Infix-anmærkning:</strong> x == 2 &amp; y &lt;= 2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Eller</td>
<td>Dette er tilfældet, hvis en betingelse er sand. Hvis antallet af betingelser er 0 (nul), returneres <strong>False</strong>.</td>
<td>Or[args], infix: a | b | ... | z</td>
<td><ul>
<li><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</li>
<li><strong>Infix-anmærkning:</strong> x == 2 | y &lt;= 2</li>
</ul></td>
</tr>
<tr class="even">
<td>Plus</td>
<td>Dette opsummerer dens betingelser. Hvis antallet af betingelser er 0 (nul), returneres <strong>0</strong>.</td>
<td>Plus[args], infix: a + b + ... + z</td>
<td><ul>
<li><strong>Operator:</strong> Plus[x, y, 2] == z</li>
<li><strong>Infix-anmærkning:</strong> x + y + 2 == z</li>
</ul></td>
</tr>
<tr class="odd">
<td>Minus</td>
<td>Derved negeres argumentet. Det skal have præcis én betingelse.</td>
<td>Minus[expr], infix: -expr</td>
<td><ul>
<li><strong>Operator:</strong> Minus[x] == y</li>
<li><strong>Infix-anmærkning:</strong> -x == y</li>
</ul></td>
</tr>
<tr class="even">
<td>Abs</td>
<td>Dette tager den absolutte værdi af dets tilstand. Det skal have præcis én betingelse.</td>
<td>Abs[expr]</td>
<td><strong>Operator:</strong> Abs[x]</td>
</tr>
<tr class="odd">
<td>Tider</td>
<td>Herefter tages produktet af dens betingelser. Hvis antallet af betingelser er 0 (nul), returneres <strong>1</strong>.</td>
<td>Times[args], infix: a * b * ... * z</td>
<td><ul>
<li><strong>Operator:</strong> Times[x, y, 2] == z</li>
<li><strong>Infix-anmærkning:</strong> x * y * 2 == z</li>
</ul></td>
</tr>
<tr class="even">
<td>Strøm</td>
<td>Det tager en eksponentiel. Det gælder eksponentiering fra højre mod venstre. (Det er med andre ord en højre-association). Derfor svarer <strong>Power[a, b, c]</strong> til <strong>Power[a, Power[b, c]]</strong>. <strong>Power</strong> kan kun bruges, hvis eksponenten er en positiv konstant.</td>
<td>Power[args], infix: a ^ b ^ ... ^ z</td>
<td><ul>
<li><strong>Operator:</strong> Power[x, 2] == y</li>
<li><strong>Infix-anmærkning:</strong> x ^ 2 == y</li>
</ul></td>
</tr>
<tr class="odd">
<td>Maks.</td>
<td>Dette giver den største tilstand. Hvis antallet af betingelser er 0 (nul), returneres <strong>Infinity</strong>.</td>
<td>Max[args]</td>
<td><strong>Operator:</strong> Max[x, y, 2] == z</td>
</tr>
<tr class="even">
<td>Min.</td>
<td>Dette giver den mindste tilstand. Hvis antallet af betingelser er 0 (nul), returneres <strong>Infinity</strong>.</td>
<td>Min[args]</td>
<td><strong>Operator:</strong> Min[x, y, 2] == z</td>
</tr>
<tr class="odd">
<td>Negeret</td>
<td>Dette giver den logiske inverse af tilstanden. Det skal have præcis én betingelse.</td>
<td>Not[expr], infix: !expr</td>
<td><ul>
<li><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</li>
<li><strong>Infix-anmærkning:</strong> !x!(y == 3)</li>
</ul></td>
</tr>
</tbody>
</table>

Eksemplerne i næste tabel viser, hvordan du skriver en infix-anmærkning.


|  Notationen infix   |                                          Betegnelse                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     x + y + z     |                                           Tilføjelse                                            |
|    x \* y \* z    |                                        Multiplikation                                         |
|       x - y       | Binær subtraktion oversættes på samme måde som binær addition, hvor der er et negativt sekund. |
|     x ^ y ^ z     |                          Eksponentiering, der har en højre-association                          |
|        !x         |                                          Boolesk ikke                                          |
|      x -: y       |                                      Boolesk virkning                                      |
|         x         |                                               y                                               |
|     x & y & z     |                                          Boolesk og                                          |
|    x == y == z    |                                           Lig med                                            |
|    x != y != z    |                                           Bestemt                                            |
|  x &lt; y &lt; z  |                                           Mindre end                                           |
|  x &gt; y &gt; z  |                                         Større end                                          |
| x &lt;= y &lt;= z |                                     Mindre end eller lig med                                     |
| x &gt;= y &gt;= z |                                   Større end eller lig med                                    |
|        (x)        |                           Parentes tilsidesætter standardprioritering.                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a>Hvorfor valideres mine udtryksbegrænsninger ikke korrekt?
Du kan ikke bruge et reserveret nøgleord som problemløsernavn til attributter, komponenter og underkomponenter i en produktkonfigurationsmodel.Her er en liste over de reserverede nøgleord, som du kan bruge:

-   Loft
-   Element
-   Lig med
-   Etage
-   Hvis
-   Mindre end
-   Større end
-   Indebærer
-   Log
-   Maks
-   Min.
-   Minus
-   Plus
-   Strøm
-   Tider
-   Slot
-   Model
-   Beslutning
-   Mål


<a name="additional-resources"></a>Yderligere ressourcer
--------

[Oprette en udtryksbegrænsning](tasks/add-expression-constraint-product-configuration-model.md)

[Tilføje en beregning til en produktkonfigurationsmodel](tasks/add-calculation-product-configuration-model.md)



