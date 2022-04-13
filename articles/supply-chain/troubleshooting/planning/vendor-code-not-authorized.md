---
title: Kreditorkode er ikke godkendt for et bestemt produkt og en bestemt dato
description: Når du forsøger at autorisere et ordreforslag eller at føje en linje til en indkøbsordre, modtager du en fejlmeddelelse om, at kreditorkoden ikke er godkendt for et produkt og en dato.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 917526dfcefb36ce6e59af6f1f5bebc23ee6e53f
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/26/2022
ms.locfileid: "8489050"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a>Kreditorkode er ikke godkendt for et bestemt produkt og en bestemt dato

Fejlkode: SYP4881415

## <a name="symptoms"></a>Symptomer

Når du forsøger at autorisere et ordreforslag eller at føje en linje til en indkøbsordre, får du vist følgende fejlmeddelelse:

> Kreditorkoden %1 er ikke godkendt for %2 i %3.

## <a name="cause"></a>Årsag

Fejlen opstår, fordi feltet **Godkendt kontrolmetode for kreditorer** er angivet til *Kun advarsel* eller *Ikke tilladt* for det angivne produkt, og kreditoren er i øjeblikket ikke godkendt til at levere det pågældende produkt.

## <a name="resolution"></a>Løsning

Du kan løse dette problem ved enten at deaktivere kreditorkontrollen for det relevante produkt eller godkende kreditoren.

Benyt følgende fremgangsmåde for at deaktivere kreditorkontrollen for et produkt.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Åbn det relevante produkt.
1. I oversigtspanelet **Indkøb** skal du angive feltet **Godkendt kontrolmetode for kreditorer** til en anden værdi end *Kun advarsel* eller *Ikke tilladt*.

Benyt følgende fremgangsmåde for at godkende en kreditor for et produkt.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Åbn den relevante vare.
1. Vælg **Opsætning** i gruppen **Godkendt kreditor** under fanen **Køb** i handlingsruden.
1. Føj en række til gitteret på listesiden **Godkendt kreditor**, og angiv følgende værdier for det:

    - **Kreditor** – Vælg den kreditor, du vil godkende for det aktuelle produkt.
    - **Ikrafttrædelsesdato** – Vælg den første dato, som kreditoren er godkendt for.
    - **Udløbsdato** – Vælg den sidste dato, som kreditoren er godkendt for.

Du kan finde flere oplysninger i [Godkende kreditorer til specifikke produkter](../../procurement/tasks/approve-vendors-specific-products.md).
