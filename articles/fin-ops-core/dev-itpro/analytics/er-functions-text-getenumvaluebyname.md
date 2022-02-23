---
title: ER-funktionen GETENUMVALUEBYNAME
description: Dette emne indeholder oplysninger om, hvordan funktionen GETENUMVALUEBYNAME til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29d7ec6498090ea47259303237c5a64a26e4926b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685925"
---
# <a name="getenumvaluebyname-er-function"></a>ER-funktionen GETENUMVALUEBYNAME

[!include [banner](../includes/banner.md)]

Funktionen `GETENUMVALUEBYNAME` søger efter en bestemt *Fasttekst*-værdi i den angivne fasttekstdatakilde ved hjælp af det fasttekstnavn, der er angivet som en *Streng*-værdi. Hvis *Fasttekst*-værdien findes, returnerer funktionen den. Ellers returnerer funktionen **nul** i fasttekstværdi.

## <a name="syntax"></a>Syntaks

```vb
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

## <a name="example-1"></a>Eksempel 1

I følgende illustration introduceres fastteksten **ReportDirection** i en datamodel. Bemærk, at der er defineret etiketter for fasttekstværdierne.

![Tilgængelige værdier for en datamodelfasttekst](./media/ER-data-model-enumeration-values.PNG)

Følgende illustration viser disse detaljer:

- Datakilden **$Retning** er konfigureret i en ER-rapport. Denne datakilde konfigureres på basis af modelfastteksten **RapportRetning**.
- Udtrykket `$IsArrivals` er designet til at bruge den modelfasttekstbaserede datakilde **$Retning** som parameter for denne funktion.
- Værdien af denne sammenligning er **SAND**.

![Eksempel på en datamodelfasttekst](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a>Eksempel 2

Funktionerne `GETENUMVALUEBYNAME` og [`LISTOFFIELDS`](er-functions-list-listoffields.md) giver dig mulighed for at hente værdier og etiketter på understøttet fasttekst som tekstværdier. (Den understøttede fasttekst er programfasttekst, datamodelfasttekst og formatfasttekst).

I følgende illustration introduceres datakilden **TransType** i en modeltilknytning. Denne datakilde refererer til programfastteksten **LedgerTransType**.

![Datakilde for en modeltilknytning, der refererer til en programfasttekst](./media/er-functions-text-getenumvaluebyname-example2-1.png)

Følgende illustration viser datakilden **TransTypeList**, der er konfigureret i en modeltilknytning. Denne datakilde konfigureres på basis af programfastteksten **TransType**. Funktionen `LISTOFFIELDS` bruges til at returnere alle fasttekstværdier som en liste over poster, der indeholder felter. På denne måde vises detaljerne for alle fasttekstværdier.

> [!NOTE]
> Feltet **EnumValue** er konfigureret for datakilden **TransTypeList** ved hjælp af udtrykket `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)`. Dette felt returnerer en fasttekstværdi for hver post på denne liste.

![Datakilde for en modeltilknytning, der returnerer alle fasttekstværdier for en valgt fasttekst som en liste over poster](./media/er-functions-text-getenumvaluebyname-example2-2.png)

Følgende illustration viser datakilden **VendTrans**, der er konfigureret i en modeltilknytning. Denne datakilde returnerer kreditorposteringer fra programtabellen **VendTrans**. Finanstypen for hver postering defineres af værdien i feltet **TransType**.

> [!NOTE]
> Feltet **TransTypeTitle** er konfigureret for datakilden **VendTrans** ved hjælp af udtrykket `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label`. I dette felt returneres etiketten for en fasttekstværdi for den aktuelle postering som tekst, hvis denne fasttekstværdi er tilgængelig. Ellers returneres en tom strengværdi.
>
> Feltet **TransTypeTitle** er knyttet til feltet **LedgerType** i en datamodel, der gør det muligt at bruge disse oplysninger i hvert ER-format, der bruger datamodellen som en datakilde.

![Datakilde for en modeltilknytning, der returnerer kreditorposteringer](./media/er-functions-text-getenumvaluebyname-example2-3.png)

I følgende illustration vises, hvordan du kan bruge [datakildefejlfindingen](er-debug-data-sources.md) til at teste den konfigurerede modeltilknytning.

![Bruge datakildefejlfindingen til at teste den konfigurerede modeltilknytning](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

Feltet **LedgerType** i en datamodel viser etiketter af posteringstyperne som forventet.

Hvis du planlægger at bruge denne fremgangsmåde til en stor mængde transaktionsdata, skal du overveje kørselsydeevnen. Du kan finde flere oplysninger i [Spore kørslen af ER-formater til fejlfinding af problemer med ydeevnen](trace-execution-er-troubleshoot-perf.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)

[Spore kørslen af ER-formater til fejlfinding af problemer med ydeevnen](trace-execution-er-troubleshoot-perf.md)

[ER-funktionen LISTOFFIELDS](er-functions-list-listoffields.md)

[ER-funktionen FIRSTORNULL](er-functions-list-firstornull.md)

[ER-funktionen WHERE](er-functions-list-where.md)
