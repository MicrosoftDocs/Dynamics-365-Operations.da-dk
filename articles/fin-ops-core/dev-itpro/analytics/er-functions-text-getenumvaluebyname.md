---
title: ER-funktionen GETENUMVALUEBYNAME
description: Dette emne indeholder oplysninger om, hvordan funktionen GETENUMVALUEBYNAME til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ded0c62b4556b21e731cd9b98db2863ec6ec442
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916838"
---
# <a name="GETENUMVALUEBYNAME">ER-funktionen GETENUMVALUEBYNAME</a>

[!include [banner](../includes/banner.md)]

Funktionen `GETENUMVALUEBYNAME` søger efter en bestemt *Fasttekst*-værdi i den angivne fasttekstdatakilde ved hjælp af det fasttekstnavn, der er angivet som en *Streng*-værdi. Hvis *Fasttekst*-værdien findes, returnerer funktionen den. Ellers returnerer funktionen **nul** i fasttekstværdi.

## <a name="syntax"></a>Syntaks

```
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>Argumenter

`enumeration data source path`: *Fasttekst*

Den gyldige sti til en datakilde for en af følgende fastteksttyper:

- Modelfasttekst til elektronisk rapportering (ER)
- ER-formatfasttekst
- Microsoft Dynamics 365 Finance-fasttekst

`enumeration value text`: *Streng*

En strengværdi, der repræsenterer navnet på en enkelt fasttekstværdi.

## <a name="return-values"></a>Returnerede værdier

*Enum* kan være nul

Den returnerede fasttekstværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Der udløses ingen undtagelse, hvis der ikke findes en *Enum*-værdi ved hjælp af navnet på den fasttekstværdi, der er angivet som en *Streng*-værdi.

## <a name="example"></a>Eksempel

I følgende illustration introduceres fastteksten **ReportDirection** i en datamodel. Bemærk, at der er defineret etiketter for fasttekstværdierne.

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Følgende illustration viser disse detaljer:

- Datakilden **$Retning** er konfigureret i en ER-rapport. Denne datakilde konfigureres på basis af modelfastteksten **RapportRetning**.
- Udtrykket `$IsArrivals` er designet til at bruge den modelfasttekstbaserede datakilde **$Retning** som parameter for denne funktion.
- Værdien af denne sammenligning er **SAND**.

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)
