---
title: Garantiaftaler
description: I dette emne beskrives garantiaftaler i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7080af2059c9c9bcdd11ca0ee9c5e339cef69302
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021498"
---
# <a name="warranty-agreements"></a>Garantiaftaler

[!include [banner](../../includes/banner.md)]

 


I Styring af aktiver kan du oprette garantibetingelser, der kan knyttes til et aktiv eller en aktivtype. Der oprettes garantibetingelser for en bestemt periode. Der kan oprettes garanti, som giver fuld dækning eller en delvis dækning, og du kan konfigurere betingelser, der er relateret til timer, udgifter og varer.

Det første trin er at oprette eventuelle leverandørgarantiaftaler, som du har for dit udstyr. Derefter kan du knytte garantiaftaler til aktiver eller aktivtyper. Leverandørgarantiaftaler bruges kun til orientering. Hvis der er oprettet en leverandørgaranti på et aktiv, kan du se garantidækningsperioden for aktivet.

## <a name="create-a-warranty-agreement"></a>Oprette en garantiaftale

En garantiaftale kan omfatte flere aftalelinjer, der dækker garantien for arbejdstimer, udgifter og varer.

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Aktiver** \> **Garanti**.
2. Vælg **Ny** for at oprette et produkt.
3. Angiv et garanti-id i feltet **Garanti**. 
4. Angiv en beskrivelse i feltet **Navn**.

    I oversigtspanelet **Detaljer** indeholder feltet **Aktiver** antallet af aktive aktiver, der bruger garantiaftalen.

5. Udfør følgende trin i oversigtspanelet **Garantilinjer** for at tilføje linjer, der skal medtages i en garantiaftale:

    1. Vælg **Tilføj linje** for at føje en ny betingelse til garantien. Der indsættes automatisk et fortløbende linjenummer i feltet **Linje**.
    2. Vælg garantiperiodetypen i feltet **Periode**.
    3. Angiv et tal i feltet **Interval**. Dette felt definerer antallet af perioder, som garantien skal være gældende for.
    4. Angiv dækningsprocenten for garantilinjen i feltet **Procent**. Procenten angiver, hvor meget der dækkes af firmaet.

![Garantiside](media/01-warranty.png)
