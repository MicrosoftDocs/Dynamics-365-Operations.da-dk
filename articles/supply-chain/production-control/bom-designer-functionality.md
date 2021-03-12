---
title: Funktioner i styklistedesigneren
description: I dette emne beskrives det, hvordan du kan bruge siden Styklistedesigner til at designe og arbejde med træstrukturer til styklister.
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesigner, BOMDesignerSetup, BOMDesignerFilterDialog, BOMDesignerBOMVersion, BOMChangeLine
audience: Application User
ms.reviewer: kamaybac
ms.custom: 20981
ms.assetid: 2b92eec1-d28c-4965-9086-939c77b3c62b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 07d74d9e02049447c69edf56eb6860a2cb6dc5c9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991884"
---
# <a name="bom-designer-functionality"></a>Funktioner i styklistedesigneren

[!include [banner](../includes/banner.md)]

I dette emne beskrives det, hvordan du kan bruge siden Styklistedesigner til at designe og arbejde med træstrukturer til styklister. Du kan klikke på Konfiguration for at vælge forskellige konfigurationer og angive, hvilke oplysninger der skal vises på linjerne i træet.

Når du åbner siden **Styklistedesigner** fra siden **Frigivne produkter**, vises hierarkiet over styklister, der er aktive og godkendte for den valgte vare, standardordrewebstedet for varen og den faktiske dato.  

Klik på **Filter** for at ændre den oprindelige markering i visningen. Ved at angive visningsprincippet til **Udvalgte/Aktive eller Valgte** kan du vælge individuelle styklister eller ruteversioner, der skal bruges i visningen. Du kan vælge ikke-godkendte og ikke-aktive styklisteversioner for at vise eller vedligeholde i styklistedesigneren.  

**Bemærk:** Hvis du åbner styklistedesigneren fra listesiden **Styklister**, vises der ikke ruteoplysninger. I øjeblikket er valget af en stykliste- eller ruteversion en egenskab for stykliste- og ruteversionen og gælder for alle forekomster af styklistedesigneren.  

I følgende afsnit beskrives de funktioner, der findes på de forskellige faner i styklistedesigneren.

## <a name="analyzing-a-bom-structure-by-using-the-bom-designer"></a>Analysere en styklistestruktur ved hjælp af styklistedesigneren
Styklistedesigneren består af to sektioner:

-   Styklistestrukturens trævisning.
-   Sektion med oplysninger, der viser oplysninger om de valgte data. Når du markerer en node i trævisningen, opdateres oversigtspaneler i sektionen med oplysninger baseret på denne node:
    -   **Oplysninger om styklistelinje** – viser oplysninger om styklistelinjen, der er valgt i trævisningen.
    -   **Varedata** – viser oplysninger om hovedvaren eller den vare, der bruges i den valgte node. Du kan klikke på **Rediger frigivet produkt** for at vedligeholde den markerede vare.
    -   **Stykliste** – viser overskriften i den stykliste, som er relateret til den valgte node.
    -   **Rute** – viser overskriften i den rute, som er relateret til den valgte node.
    -   **Ruteoperationer** – viser et eksempel på operationer for ruten. Når der vælges en styklistelinje, der er tildelt til en bestemt operation, markeres operationen som **Komponent, der skal bruges ved operationer**.

## <a name="selecting-a-bom-and-route"></a>Vælge en stykliste og rute
Det filter, der anvendes til styklisten og ruten vises i overskriften i styklistedesigneren. Du kan ændre filteret ved hjælp af dialogboksen **Filter**. I følgende tabel beskrives felterne i denne dialogboks.

<table>
<thead>
<tr class="header">
<th>Felt</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Produktdimensioner</td>
<td>Hvis den valgte færdigvare er en produktmaster, kan du definere de aktive produktdimensioner for det primære valg. <strong>Bemærk:</strong> Hvis du åbner styklistedesigneren for et produkt, der ikke er en produktmaster, er der ingen produktdimensioner, der kan vælges i dialogboksen <strong>Filter</strong>.</td>
</tr>
<tr class="even">
<td>Lokation</td>
<td>Ændr det sted, som styklistetræet vises for. Standardstedet er standardlagerstedet for den færdige vare.</td>
</tr>
<tr class="odd">
<td>Visningsprincip</td>
<td>Vælg princippet for visning af versioner, der gælder for den aktuelle styklistestruktur og den aktuelle rute:
<ul>
<li>Når princippet er angivet til <strong>Aktiv eller Udvalgt/Aktiv</strong>, findes der frem til den gældende stykliste- eller ruteversion for denne dato.</li>
<li>Når princippet er indstillet til <strong>Udvalgt/Aktiv eller Valgt</strong>, kan du vælge en styklisteversion eller ruteversion ved at klikke på <strong>Stykliste</strong> &gt; <strong>Styklisteversioner</strong> eller <strong>Rute</strong> &gt; <strong>Ruteversioner</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Versionsdato</td>
<td>Angiv versionsdatoen for styklisten og ruten. Denne version identificerer, hvilken styklisteversion, der anvendes på en bestemt dato, som fastlagt af versionsdatoerne i opsætningen af styklisteversionen.</td>
</tr>
<tr class="odd">
<td>Antal fra</td>
<td>Du kan filtrere versionerne ved at vælge et bestemt antal. Hvis du angiver en værdi, kan forskellige stykliste- og ruteversioner vælges.</td>
</tr>
<tr class="even">
<td>Vis kun gyldige</td>
<td>Når du markerer afkrydsningsfeltet, vises kun styklistelinjer, der har gyldige datoer, i træstrukturen. Højreklik eller dobbeltklik på en styklistelinje for at siden <strong>Rediger styklistelinje</strong>, så du kan se gyldighedsdatoer for denne styklistelinje.</td>
</tr>
</tbody>
</table>

Når du bruger styklistedesigneren til at gennemgå eller redigere styklister, der består af et eller flere niveauer af fantomstyklister, strækker den rute, som typisk er knyttet til topvaren, sig over hele styklistehierarkiet. For at forenkle oversigten kan du låse ruten på øverste niveau i visningen ved at klikke på **Vis** &gt; **Lås rute**. For at låse op for ruten skal du klikke på **Vis** &gt; **Lås rute op**.

## <a name="adding-and-editing-boms-and-bom-lines"></a>Tilføje og redigere styklister og styklistelinjer
Brug funktionerne **Styklistelinjer** eller **Stykliste** til at redigere styklistelinjer eller styklister. Når du markerer en node i træet, bestemmer typen af noden, hvilke funktioner der er tilgængelige.

| Funktion                            | Beskrivelse                                                                                               | Nodetype og betingelser                                                                                                                                                                                                                                                                       |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Styklistelinjer &gt; Rediger                 | Åbn en dialogboks, hvor du kan redigere attributterne for styklistelinjen.                                             | Denne funktion er tilgængelig, når der er valgt en styklistelinjenode.                                                                                                                                                                                                                                   |
| Styklistelinjer &gt; Slet               | Slet en styklistelinje fra den valgte stykliste.                                                                  | Denne funktion er tilgængelig, når en styklistelinjenode er valgt og styklisten ikke er låst til redigering.                                                                                                                                                                                             |
| Styklistelinjer &gt; Tilføj før linje      | Åbn en dialogboks, hvor du kan vælge en produktvariant, der skal medtages før den markerede styklistelinje.         | Denne funktion er tilgængelig, når der er valgt en styklistelinjenode.                                                                                                                                                                                                                                   |
| Styklistelinjer &gt; Føj til komponentstykliste | Åbn en dialogboks, hvor du kan vælge en produktvariant, der skal medtages ved slutningen af den markerede stykliste.       | Denne funktion er tilgængelig, når den node, der er valgt, har en valgt stykliste. Hvis denne funktion ikke er tilgængelig, mangler der eventuelt en styklisteversion for den valgte varevariant. I så fald kan du klikke på **Stykliste** &gt; **Opret version** for at oprette den manglende version for den valgte node. |
| Styklistelinjer &gt; Tilføj efter linje       | Åbn en dialogboks, hvor du kan vælge en produktvariant, der skal medtages efter den markerede styklistelinje.          | Denne funktion er tilgængelig, når der er valgt en styklistelinjenode.                                                                                                                                                                                                                                   |
| Stykliste &gt; Opret version             | Opret en ny styklisteversion eller stykliste for produktvarianten for den valgte node.                             | Denne funktion er tilgængelig, når styklistelinjenoden, der er markeret, er knyttet til en vare, der har en produktionstype af **Stykliste** eller **Formel**.                                                                                                                                                  |
| Stykliste &gt; kalkulation                | Åbn en dialogboks, hvor du kan køre beregningen af kost- eller salgsprisen for den valgte produktvariant. | Denne funktion er tilgængelig, når den node, der er valgt, er knyttet til en styklisteversion.                                                                                                                                                                                                         |
| Stykliste &gt; Kontroller                      | Valider og kontrollér den valgte stykliste.                                                                      | Denne funktion er tilgængelig, når den node, der er valgt, er knyttet til en styklisteversion.                                                                                                                                                                                                         |

## <a name="configuring-the-tree-view"></a>Konfigurere træstrukturen
Klik på **Opsætning** for at tilpasse de oplysninger, der vises i styklistedesignerens træstruktur.

| Feltgruppe | Beskrivelse                                                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stykliste         | Brug afkrydsningsfelterne til at vælge de kriterier, der vises i træstrukturen. Styklistedesigneren viser de valgte kriterier nederst under begge faner. |
| Rute       | Brug afkrydsningsfelterne til at vælge de kriterier, der vises for ruterne.                                                                                    |





