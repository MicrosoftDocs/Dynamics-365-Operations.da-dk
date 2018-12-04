---
title: Formeldesigner
description: "I dette emne beskrives, hvordan du bruger formeldesigneren til at analysere og vedligeholde formler i en trævisning."
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a4cfd017fe10bbda6eda0e3a9a045e0832b08753
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="formula-designer"></a>Formeldesigner

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du bruger formeldesigneren til at analysere og vedligeholde formler i en trævisning.

Når du åbner siden **Formeldesigner** fra siden **Frigivne produkter**, viser træet i venstre rude en liste over samprodukter og hierarkiet af stof til det frigivne produkt. Strukturen er afledt af hierarkiet af formler, der er aktive og godkendte for den valgte vare og dens stof, standardordrewebstedet for varen og den faktiske dato.

Klik på **Konfiguration** for at vælge forskellige konfigurationer og angive, hvilke oplysninger der skal vises på linjerne i træet.

Klik på **Filter** for at ændre den oprindelige markering i visningen. Hvis du indstiller visningsprincippet til **Udvalgte/Aktive** eller **Valgte** kan du vælge individuelle formel- eller ruteversioner, der skal bruges i visningen. Du kan vælge ikke-godkendte og ikke-aktive formelversioner for at vise eller vedligeholde i formeldesigneren.  

> [!NOTE]
> Hvis du åbner siden **Formeldesigner** fra listesiden **Styklister**, vises der ikke ruteoplysninger. I øjeblikket gælder valget af en formel- eller ruteversion for alle forekomster af formeldesigneren.  

I følgende afsnit beskrives de funktioner, der findes i styklistedesigneren.

## <a name="analyze-a-formula-structure-by-using-the-formula-designer"></a>Analysere en formelstruktur ved hjælp af formeldesigneren
Formeldesigneren består af to sektioner:

-   Formelstrukturens trævisning.
-   Sektion med oplysninger, der viser oplysninger om de valgte data. Når du markerer en node i trævisningen, opdateres oversigtspaneler i sektionen med oplysninger baseret på denne node:
    -   **Formellinjedetaljer** – Se oplysninger om den formellinje, der er valgt i trævisningen.
    -   **Varedata** – Se oplysninger om hovedvaren eller den vare, der bruges i den valgte node. Du kan klikke på **Rediger frigivet produkt** for at vedligeholde den markerede vare.
    -   **Formel** – Se overskriften til den formel, som er relateret til den valgte node.
    -   **Rute** – Se overskriften i den rute, som er relateret til den valgte node.
    -   **Ruteoperationer** – Se et eksempel på operationer for ruten. Når der vælges en styklistelinje, der er tildelt til en bestemt operation, markeres operationen som **Komponent, der skal bruges ved operationer**.

## <a name="select-a-formula-and-route"></a>Vælg en formel og en rute
Det filter, der anvendes til formlen og ruten vises i overskriften i formeldesigneren. Du kan ændre filteret ved hjælp af dialogboksen **Filter**. I følgende tabel beskrives felterne i denne dialogboks.

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
<td>Hvis den valgte færdigvare er en produktmaster, kan du definere de aktive produktdimensioner for det primære valg. Bemærk, at hvis du åbner formeldesigneren for et produkt, der ikke er en produktmaster, er der ingen produktdimensioner, der kan vælges i dialogboksen <strong>Filter</strong>.</p></td>
</tr>
<tr class="even">
<td>Sted</td>
<td>Vælg et andet sted, som stoftræet skal vises for. Standardstedet er standardlagerstedet for den færdige vare.</td>
</tr>
<tr class="odd">
<td>Visningsprincip</td>
<td><p>Vælg princippet for visning af versioner, der gælder for den aktuelle formel og den aktuelle rute:</p>
<ul>
<li>Når princippet er angivet til <strong>Aktivt</strong> eller <strong>Udvalgte/Aktive</strong>, findes der frem til den gældende formel- eller ruteversion for denne dato.</li>
<li>Når princippet er indstillet til <strong>Udvalgte/Aktive</strong> eller <strong>Valgt</strong>, kan du vælge en formelversion eller ruteversion ved at klikke på <strong>Formel</strong> &gt; <strong>Formelversioner</strong> eller <strong>Rute</strong> &gt; <strong>Ruteversioner</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Versionsdato</td>
<td>Angiv versionsdatoen for formlen og ruten. Versionen identificerer, hvilken formelversion der skal bruges på en bestemt dato ud fra versionsdatoerne i opsætningen af formelversionen.</td>
</tr>
<tr class="odd">
<td>Fra antal</td>
<td>Du kan filtrere versionerne ved at vælge et bestemt antal for &quot;fra&quot;. Hvis du angiver en værdi, kan der vælges forskellige formel- og ruteversioner.</td>
</tr>
<tr class="even">
<td>Vis kun gyldige</td>
<td>Når du markerer afkrydsningsfeltet, vises kun formellinjer, der har gyldige datoer, i træstrukturen. Højreklik eller dobbeltklik på en formellinje for at siden <strong>Rediger formellinje</strong>, så du kan se gyldighedsdatoer for denne formellinje.</td>
</tr>
</tbody>
</table>

Når du bruger formeldesigneren til at gennemgå eller redigere formler, der består af et eller flere niveauer af fantomformler, strækker den rute, som typisk er knyttet til topvaren, sig over hele formelhierarkiet. For at forenkle oversigten kan du låse ruten på øverste niveau i visningen ved at klikke på **Vis** &gt; **Lås rute**. For at låse op for ruten skal du klikke på **Vis** &gt; **Lås rute op**.

## <a name="add-and-edit-formulas-and-formula-lines"></a>Tilføje og redigere formler og formellinjer
Brug funktionerne **Styklistelinjer** eller **Formel** til at redigere formellinjerne eller formlen. Når du markerer en node i træet, bestemmer typen af noden, hvilke funktioner der er tilgængelige.

| Funktion                            | Betegnelse                                                                                               | Nodetype og betingelser |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|--------------------------|
| Styklistelinjer &gt; Rediger                 | Åbn en dialogboks, hvor du kan redigere attributterne for formellinjen.                                         | Denne funktion er tilgængelig, når der er valgt en formellinjenode. |
| Styklistelinjer &gt; Slet               | Slet en formellinje fra den valgte formel.                                                          | Denne funktion er tilgængelig, når en formellinjenode er valgt og formlen ikke er låst til redigering. |
| Styklistelinjer &gt; Tilføj før linje      | Åbn en dialogboks, hvor du kan vælge en produktvariant, der skal medtages før den markerede formellinje.     | Denne funktion er tilgængelig, når der er valgt en formellinjenode. |
| Styklistelinjer &gt; Føj til komponentstykliste | Åbn en dialogboks, hvor du kan vælge en produktvariant, der skal medtages ved slutningen af den markerede formel.   | Denne funktion er tilgængelig, når den node, der er valgt, har en valgt formel. Hvis denne funktion ikke er tilgængelig, mangler der eventuelt en formelversion for den valgte varevariant. I så fald kan du klikke på **Formel** &gt; **Opret version** for at oprette den manglende version for den valgte node. |
| Styklistelinjer &gt; Tilføj efter linje       | Åbn en dialogboks, hvor du kan vælge en produktvariant, der skal medtages efter den markerede formellinje.      | Denne funktion er tilgængelig, når der er valgt en formellinjenode. |
| Formel &gt; Opret version         | Opret en ny formelversion eller formel for produktvarianten for den valgte node.                     | Denne funktion er tilgængelig, når formellinjenoden, der er markeret, er knyttet til en vare, der har en produktionstype af **Stykliste** eller **Formel**. |
| Formel &gt; Beregning            | Åbn en dialogboks, hvor du kan køre beregningen af kost- eller salgsprisen for den valgte produktvariant. | Denne funktion er tilgængelig, når den node, der er valgt, er knyttet til en formelversion. |
| Formel &gt; Kontrol                  | Valider og kontrollér den valgte formel.                                                                  | Denne funktion er tilgængelig, når den node, der er valgt, er knyttet til en formelversion. |

## <a name="configuring-the-tree-view"></a>Konfigurere træstrukturen
Klik på **Opsætning** for at tilpasse de oplysninger, der vises i formeldesignerens træstruktur.


| Feltgruppe |                                                                          Betegnelse                                                                          |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     Stykliste     | Brug afkrydsningsfelterne til at vælge de kriterier, der vises i træstrukturen. De valgte kriterier vises nederst under begge faner i formeldesigneren. |
|    Rute    |                                           Brug afkrydsningsfelterne til at vælge de kriterier, der vises for ruterne.                                           |


