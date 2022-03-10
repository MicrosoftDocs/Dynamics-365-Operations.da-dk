---
title: Beregninger af produktkonfigurationsmodel
description: Dette emne beskriver, hvordan du opretter beregninger for attributter i en produktkonfigurationsmodel
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 349fed3ca75b94db2f421a1ff3c3553c96c202c37d59857a3d973f3de8f995ad
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755245"
---
# <a name="product-configuration-model-calculations"></a>Beregninger af produktkonfigurationsmodel

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du opretter beregninger for attributter i en produktkonfigurationsmodel.

## <a name="prerequisites"></a>Forudsætninger

Beregninger bruges i en produktkonfigurationsmodel til at beregne konfigurationsværdier for et produkt. Før du kan gå i gang med at konfigurere beregninger, skal den relaterede produktkonfigurationsmodel eksistere. Du kan finde en oversigt over opsætningsprocessen for konfigurationsmodeller og de relaterede opgaver under [Konfigurere en produktkonfigurationsmodel](set-up-maintain-product-configuration-model.md).

## <a name="create-a-calculation"></a>Oprette en beregning

En beregning består af et udtryk og en målattribut. Du kan få flere oplysninger under [Ofte stillede spørgsmål om beregninger for produktkonfigurationsmodeller](calculate-product-configuration-models.md).

Hvis du vil oprette en beregning for en eksisterende produktmodel, skal du følge disse trin.

1. Gå til **Administration af produktoplysninger \> Fælles \> Produktkonfigurationsmodeller**.
1. Åbn en produktkonfigurationsmodel, og vælg derefter **Rediger**.
1. I oversigtspanelet **Beregninger** skal du vælge **Tilføj** for at tilføje en beregning, og indstil derefter følgende felter:

    - **Navn** – Angiv et navn til beregningen.
    - **Beskrivelse** – Indtast en beskrivelse af beregningen.
    - **Målattribut** – Vælg den attribut, du foretager beregningen for.

1. Vælg **Rediger udtryk**.
1. I dialogboksen **Angiv en beregning** skal du føje de påkrævede attributter, operatorer og værdier til udtrykket. Få flere oplysninger om arbejdet med disse elementer under [Udtryksbegrænsninger og tabelbegrænsninger i modeller for produktkonfiguration](expression-constraints-table-constraints-product-configuration-models.md).
1. Når udtrykket er klar, skal du vælge **OK**.

## <a name="calculation-examples"></a>Eksempler på beregninger

Dette afsnit indeholder et par eksempler, der viser, hvordan beregninger fungerer.

### <a name="example-1"></a>Eksempel 1

Målattributten er boolesk, og beregningen bruger følgende betingede udtryk:

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

Udtrykket returnerer værdien *Sand* til målattributten, hvis `decimalAttribute2` er større end eller lig med `decimalAttribute1`. Ellers returneres værdien *Falsk*.

### <a name="example-2"></a>Eksempel 2

I dette eksempel bruges tekstattributten `textFixedList` som målattribut. Denne attribut indeholder følgende faste liste.

| Værdi | Værdi for problemløser |
|---|---|
| A | 1a |
| B | 2b |
| C | 2c |

Følgende skærmbillede viser, hvordan indstillingerne for denne attribut kan se ud i systemet.

![Indstillinger af attributtype, f.eks. 2.](media/model-calculations-example2.png "Indstillinger af attributtype, f.eks. 2")

Attributten bruges i følgende betingede sætning:

`If[integerAttribute < 150, 0, 2]`

Hvis `integerAttribute` er mindre end 150, returnerer denne sætning tekstværdien af den første post på den faste liste, *A*. Ellers returnerer den tekstværdien for den tredje post på den faste liste, *C*.

> [!NOTE]
> Den faste liste svarer til en nulbaseret fasttekst, og dens værdier åbnes med den relevante heltalsværdi. Den første faste listeværdi (*A*) sammenholdes derfor med *0*, den anden værdi (*B*) sammenholdes med *1*, og den tredje værdi (*C*) sammenholdes med *2*.

### <a name="example-3"></a>Eksempel 3

I dette eksempel bruges målattributten `textFixedList` fra det forrige eksempel. Der bruges også en anden tekstattribut, `textAttribute`, der indeholder følgende faste liste.

| Værdi | Værdi for problemløser |
|---|---|
| AA | 1aa |
| BB | 2bb |

Følgende skærmbillede viser, hvordan indstillingerne for denne attribut kan se ud i systemet.

![Indstillinger af attributtype, f.eks. 3.](media/model-calculations-example3.png "Indstillinger af attributtype, f.eks. 3")

Værdien af `textFixedList`-attributten beregnes ved hjælp af følgende betingede sætning:

`If[textAttribute == "1aa", 0, 2]`

Hvis `textAttribute` har en problemløserværdi, der er lig med *1aa*, returnerer dette udtryk tekstværdien af den første post på den faste liste `textFixedList`, *A*. Ellers returnerer den tekstværdien for den tredje post på den faste liste `textFixedList`, *C*.

> [!NOTE]
> - Den betingede sætning skal bruge problemløserværdien for attributten.
> - Det er kun tekstattributter fra fastlisten, der kan bruges i beregninger.

## <a name="see-also"></a>Se også

- [Ofte stillede spørgsmål om beregninger for produktkonfigurationsmodeller](calculate-product-configuration-models.md)
- [Tilføje en udtryksbegrænsing til en produktkonfigurationsmodel](tasks/add-expression-constraint-product-configuration-model.md)
- [Oversigt over produktkonfigurationsmodeller](product-configuration-models.md)
