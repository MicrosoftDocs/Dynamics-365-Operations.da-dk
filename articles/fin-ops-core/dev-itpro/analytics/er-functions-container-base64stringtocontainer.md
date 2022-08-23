---
title: ER-funktionen Base64StringToContainer
description: Denne artikel indeholder oplysninger om, hvordan funktionen Base64StringToContainer til elektronisk rapportering (ER) skal anvendes.
author: kfend
ms.date: 12/14/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 96dfffc3d899f1106c6c931efb08c941f5b3c1a6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291228"
---
# <a name="base64stringtocontainer-er-function"></a>ER-funktionen Base64StringToContainer

[!include [banner](../includes/banner.md)]

Denne `BASE64STRINGTOCONTAINER`-[funktion](er-formula-language.md#Functions) konverterer det angivne input af typen *Streng* til et dataelement af typen *[Container](er-functions-category-container.md)*.

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

![Eksempeldatakilder på designersiden for ER-modeltilknytning.](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Containerfunktioner](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
