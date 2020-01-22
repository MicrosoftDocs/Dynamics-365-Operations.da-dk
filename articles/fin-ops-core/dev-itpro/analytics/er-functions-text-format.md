---
title: ER-funktionen FORMAT
description: Dette emne indeholder oplysninger om, hvordan funktionen FORMAT til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: df158e80bd1c11832376678a631a9e0e162534ad
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915711"
---
# <a name="FORMAT">ER-funktionen FORMAT</a>

[!include [banner](../includes/banner.md)]

Funktionen `FORMAT` returnerer den angivne streng som en *Streng*-værdi, efter den er blevet formateret ved at erstatte alle forekomster af **%N** med det *N*'te argument.

## <a name="syntax"></a>Syntaks

```
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a>Argumenter

`string`: *Streng*

En reference til en datakilde af datatypen *Streng*, som skal formateres. Dette argument skal udfyldes.

`argument 1`: *Streng*

Det første argument, der bruges til at erstatte forekomster af **%1**. Dette argument skal udfyldes.

`argument N`: *Streng*

Det *N*'te argument, der bruges til at erstatte forekomster af **%2**, **%3** osv. Disse yderligere argumenter er valgfrie.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Hvis et argument ikke er angivet for en parameter, bliver parameteren returneret som **"%N"** i strengen. For værdier af typen *Reel* er standardstrengkonverteringen begrænset til to decimaler.

## <a name="example"></a>Eksempel

I følgende illustration returnerer datakilden **PaymentModel** en liste over kundeposter ved hjælp af komponenten **Kunde**. Den returnerer værdien for behandlingsdato ved hjælp af feltet **ProcessingDate**.

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

Datakilden **PaymentModel** i det elektroniske rapporteringsformat (ER-format) er designet til at generere en elektronisk fil til de valgte debitorer og er valgt som en datakilde, og den styrer procesforløbet. En undtagelse opstår for at give brugeren besked, hvis en bestemt kunde er spærret for den dato, hvor rapporten behandles. Den formel, der er udviklet til denne type behandlingskontrol, kan bruge følgende ressourcer:

- Etiket SYS70894, som har følgende tekst:

    - **For det amerikanske sprog:** "Nothing to print"
    - **For det danske sprog:** "Intet at udskrive"

- Etiket SYS18389, som har følgende tekst:

    - **For sproget EN-US:** "Kunde %1 er spærret for %2."
    - **For det tyske sprog:** "Debitor '%1' er spærret for %2."

Her er det udtryk, der kan designes.

```
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

Hvis en rapport behandles for debitoren **Litware Retail** den 17. december 2015 i den amerikanske kultur, **EN-US**, og på det amerikanske sprog, **EN-US**, returnerer denne formel følgende tekst, som kan præsenteres for slutbrugeren som en undtagelsesmeddelelse:

*Intet at udskrive. Customer Litware Retail er stoppet for 17/12/2015.*

Hvis den samme rapport behandles den 17. december 2015 for kunden **Litware Retail** med dansk kultur **DA** og sproget **DA**, returnerer formlen følgende tekst, der bruger et andet datoformat:

*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*

>[!NOTE]
> Følgende syntaks er anvendt i ER-formler for etiketter:
>
> - **For etiketter fra ressourcer i Microsoft Dynamics 365 Finance-programmer:** **@X**, hvor **X** er etiket-ID'et i applikationsobjekttræet (AOT)
> - **For etiketter, der er placeret i ER-konfigurationer:** **@GER_LABEL:X"**, hvor **X** er etiket-ID'et i ER-konfigurationen

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)