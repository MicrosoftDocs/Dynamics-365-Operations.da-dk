---
title: Understøttede sammensatte datatyper til elektroniske rapporteringsformler
description: Denne artikel indeholder oplysninger om sammensatte datatyper, der understøttes i formler til elektronisk rapportering (ER).
author: kfend
ms.date: 06/02/2021
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: ea6f8ab1f0cd26fd2414a17be559aa60fc52e7d3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272706"
---
# <a name="supported-composite-data-types-for-electronic-reporting-formulas"></a>Understøttede sammensatte datatyper til elektroniske rapporteringsformler

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om sammensatte datatyper, der understøttes i udtryk til [elektronisk rapportering (ER)](general-electronic-reporting.md). De sammensatte datatyper er [klasse](#class), [container](#container), [post](#record), [postliste](#record-list) og [objekt](#object).

## <a name="class"></a><a name="class"></a>Klasse

*Klasse*-datatypen refererer til en offentlig programklasse. I ER repræsenteres den som en [*post*](#record), der indeholder et separat felt for hver offentlig metode i den klasse, der refereres til. Når metodens kald parameteriseres, skal du også angive de krævede argumenter af de relevante typer i et ER-udtryk, der er konfigureret til at kalde metoden.

I ER-tilknytnings- og formatkomponenter kan du tilføje den **Klasse**-datakilde, der vises som datakilde, og som returnerer en værdi af *klasse*-typen. Denne datakilde viser offentlige metoder i klassen, der kan kaldes under kørslen.

> [!NOTE]
> Kun metoder, der returnerer en værdi, kan kaldes fra ER-udtryk.
>
> Det er kun metoder med et interval på nul til otte argumenter, der kan kaldes fra ER-udtryk.

Standardværdien for en *klasse* er **null**.

I følgende illustration vises, hvordan **systemoplysninger (xInfo)**-datakilden for **klasse**-typen tilføjes for at få forekomsten af **xInfo**-programklassen og kalde dens **productName()**-metode for modtagelse af navnet på det aktuelle program. Navnet på det aktuelle program hentes ved kørsel af den `xInfo.productName`-binding, der blev konfigureret for feltet **Softwarenavn(SoftwareName)** i ER-datamodellen. Denne binding kalder metoden `productName()` for **XInfo**-programklassen, der repræsenteres i den aktuelle modeltilknytning som **Systemoplysninger (xInfo)** datakilde.

[![Konfigurere en klassedatakilde i ER-modeltilknytningsdesigner.](./media/er-formula-supported-data-types-composite-class1.gif)](./media/er-formula-supported-data-types-composite-class1.gif)

I følgende illustration vises, hvordan ER-formatet er konfigureret til at placere det angivne programnavn i genererede dokumenter. Feltet **Softwarenavn(SoftwareName)** for den anvendte datamodel var bundet til den **Streng**-komponent, der er indlejret under **softwareUsed** XML-elementet i ER-formatet. Navnet på det aktuelle program placeres således ved kørsel af **softwareUsed** XML-elementet i et genereret dokument i XML-format.

[![Konfigurere strukturen for et elektronisk udgående dokument i ER-formatdesigneren.](./media/er-formula-supported-data-types-composite-class2.png)](./media/er-formula-supported-data-types-composite-class2.png)

## <a name="container"></a><a name="container"></a>Container

*Container*-datatypen indeholder binært indhold. En *container*-værdi kan bruges til at overføre specifikke oplysninger fra et lager til et genereret dokument. I ER-strukturen anvendes denne datatype ofte til at placere medieindhold som f.eks. et firmalogo i genererede dokumenter.

> [!NOTE]
> Selvom hvert medieelement kan repræsenteres som en *container*-værdi, er det ikke hver *container*-værdi, der repræsenterer et medieelement. Hvis du derfor konfigurerer et ER-format, så der bruges en *container* til at placere et billede i genererede dokumenter, men den *container*, der refereres til, ikke returnerer medieindhold, kan en undtagelse, der ligner følgende eksempel, være "Fejludført kode: Binær (objekt), metode constructFromContainer kaldes med ugyldige parametre".

Standardværdien for en *container* er **null**.

I følgende illustration vises, hvordan feltet **Bitmap(Image)** af *container*-typen er bundet til feltet med datamodellens **Logo** i **container**-typen i modeltilknytningen **Salgsfaktura**. Denne binding gør firmaets logo tilgængeligt for alle ER-formater, der er designet til roddefinitionen af **SalesInvoice**, og som bruger denne modeltilknytning under kørslen.

[![Binding af et felt af typen Container i ER-modeltilknytningsdesigner.](./media/er-formula-supported-data-types-composite-container.png)](./media/er-formula-supported-data-types-composite-container.png)

## <a name="record"></a><a name="record"></a>Optag

En *post* er en samling navngivne felter, som hver især er knyttet til en værdi af enten en [basis](er-formula-supported-data-types-primitive.md)-datatype eller en sammensat datatype. Normalt bruges en *post* til at repræsentere en enkelt post på en postliste. I dette tilfælde repræsenterer hvert element de enkelte felter, metoder og relationer.

Standardværdien for en *post* er **tom**.

> [!NOTE]
> Når du får værdien af et felt i en tom *post*, returneres standardværdien for den relevante datatype.

Der kan hentes en *post* ved hjælp af følgende funktioner:

- [FIRST](er-functions-list-first.md)
- [FIRSTORNULL](er-functions-list-firstornull.md)
- [EMPTYRECORD](er-functions-record-emptyrecord.md)
- [NULLCONTAINER](er-functions-record-nullcontainer.md)

Yderligere oplysninger om transformation af *post*-værdier finder du i [Liste over ER-funktioner i listekategorien](er-functions-category-list.md).

## <a name="record-list"></a><a name="record-list"></a>Liste over poster

En *postliste* er en liste over elementer af *post*-typen. Normalt bruges en *postliste* til at repræsentere listen over poster, der er hentet fra en databasetabel.

Posterne på en *postliste* giver som standard adgang i rækkefølge. Hvis du vil have adgang til en bestemt post, kan du bruge funktionen [INDEX](er-functions-list-index.md) og angive *heltal* som indeks.

Standardværdien for en *postliste* er **tom**. Du kan bruge funktionen [ISEMPTY](er-functions-list-isempty.md) til at evaluere, om en *postliste* er tom.

> [!NOTE]
> Hvis en *postliste* er tom, vil ethvert forsøg på at hente en feltværdi for en *post* forårsage, at der opstår en undtagelse under kørslen. Du kan få mere at vide om, hvordan du kan undgå kørselsundtagelser af denne type, under [Overvejelse i forbindelse med sager med tom liste](er-components-inspections.md#i9).

Der kan startes en *postliste* ved hjælp af følgende funktioner:

- [ALLITEMS](er-functions-list-allitems.md)
- [ALLITEMSQUERY](er-functions-list-allitemsquery.md)
- [EMPTYLIST](er-functions-list-emptylist.md)
- [LIST](er-functions-list-list.md)
- [LISTDISTINCT](er-functions-list-listdistinct.md)

Yderligere oplysninger om transformation af *postliste*-værdier finder du i [Liste over ER-funktioner i listekategorien](er-functions-category-list.md). Du kan få mere at vide om, hvordan du introducerer *postliste*-elementer, ved at udfylde dem med programdata og derefter bruge dataene til at oprette forretningsdokumenter, i [Design af en ny ER-løsning til udskrivning af en brugerdefineret rapport](er-quick-start1-new-solution.md).

## <a name="object"></a><a name="object"></a>Objekt

Et *objekt* refererer til en forekomst af en *klasse*. Normalt startes et *objekt* i kildekoden. Det overføres derefter til en ER-modeltilknytning og viser detaljer om udførelseskonteksten.

Standardværdien for et *objekt* er **null**.

I følgende illustration vises, hvordan datakilden **ReportDataContract** for *objekt*-typen tilføjes for at overføre oplysninger om en genereret faktura fra kildekoden til modeltilknytningen af **Projektfaktura**. Teksten i fakturaforekomsten sendes f.eks. som en del af udførelseskonteksten. Denne tekst tages fra kildekoden under kørslen ved udførelse af den `ReportDataContract.parmInvoiceInstanceText`-binding, der blev konfigureret for feltet **Note** i ER-datamodellen. Denne binding kalder metoden `parmInvoiceInstanceText()` for **PSAProjInvoiceContract**-programklassen, der repræsenteres i den aktuelle modeltilknytning som **ReportDataContract** datakilde.

[![Konfigurere en objektdatakilde i ER-modeltilknytningsdesigner.](./media/er-formula-supported-data-types-composite-object.gif)](./media/er-formula-supported-data-types-composite-object.gif)

Du kan få mere at vide om, hvordan du overfører detaljer i udførelseskonteksten fra kildekode til den kørende ER-løsning, i [Udvikle programartefakter for at kalde den designede rapport](er-quick-start1-new-solution.md#DevelopCustomCode).

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering](general-electronic-reporting.md)
- [Formelsprog i elektronisk rapportering](er-formula-language.md)
- [Understøttede basisdatatyper](er-formula-supported-data-types-primitive.md)
