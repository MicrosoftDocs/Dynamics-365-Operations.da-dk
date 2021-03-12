---
title: ER-funktionen Base64StringToContainer
description: Dette emne indeholder oplysninger om, hvordan funktionen Base64StringToContainer til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0e92ae41a3e0f03cb14d4791ab768f096f2a0523
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739065"
---
# <a name="base64stringtocontainer-er-function"></a>ER-funktionen Base64StringToContainer

[!include [banner](../includes/banner.md)]

Denne `BASE64STRINGTOCONTAINER`-[funktion](er-formula-language.md#functions) konverterer det angivne input af typen *Streng* til et dataelement af typen *[Container](er-functions-category-container.md)*.

## <a name="syntax"></a>Syntaks

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a>Argumenter

`input`: *Streng*

Den gyldige sti til en datakilde af typen *Streng*.

## <a name="return-values"></a>Returnerede værdier

*Container*

Den binære værdi, der bliver resultatet, i binært BLOB-format (binært stort objekt).

## <a name="usage-notes"></a>Bemærkninger til brug

Undtagelsen "Parameter er ikke gyldig" vises, hvis inputstrengen ikke indeholder en korrekt Base64-gruppe af binær til tekst-kodningsskemaer.

## <a name="example"></a>Eksempel

Du definerer følgende datakilder i din modeltilknytning:

- Roddatakilden **DocuTypeGroupEnum** for typen *Dynamics 365 for Operations / fasttekst*, der henviser til **DocuTypeGroup**-programfasttekst
- Roddatakilden **Kunde** af typen *Dynamics 365 for Operations / Tabelposter*, som refererer til programtabellen **CustTable**
- Datakilden **\#Medie** af typen *Beregnet felt*, der konfigureres på følgende måde:

    - Den er tilføjet som en underordnet datakilde for datakilden **Kunde**.
    - Den indeholder udtrykket `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.

- Datakilden **\#MediaAsBase64String** af typen *Beregnet felt*, der konfigureres på følgende måde:

    - Den er tilføjet som en underordnet datakilde for datakilden **Kunde.'\#Medie'**.
    - Den indeholder udtrykket `Customer.'#Media'.'getFileContentAsBase64String()'`.

- Datakilden **\#BlobFomBase64** af typen *Beregnet felt*, der konfigureres på følgende måde:

    - Den er tilføjet som en underordnet datakilde for datakilden **Kunde.'\#Medie'**.
    - Den indeholder udtrykket `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.

I dette eksempel koder datakilden **\#MediaAsBase64String** det binære indhold af den aktuelle medietilknytning som tekst, der repræsenterer en Base64-gruppe af binær til tekst-kodningsskemaer. Datakilden **\#BlobFomBase64** afkoder Base64-strengen og returnerer en binær værdi i BLOB-format.

![Eksempeldatakilder på designersiden for ER-modeltilknytning](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Containerfunktioner](er-functions-category-container.md)
