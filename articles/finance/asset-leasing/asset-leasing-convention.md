---
title: Konventioner i aktivleasing
description: Dette emne beskriver konventionerne leasingaktiver.
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ea89d54f1ce3a1e971d41623bf44f909f7dfdf09
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131275"
---
# <a name="asset-leasing-conventions"></a>Konventioner i aktivleasing

[!include [banner](../includes/banner.md)]

Dette emne beskriver konventionerne leasingaktiver. Leasingkonventioner bruges til at bestemme startdatoen for leasingkartoteket. Hvis leasingaftalen er angivet til **Ingen**, er startdatoen den samme som startdatoen for leasingaftalen (det vil sige værdien af feltet **Startdato for leasingaftalen**). Hvis leasingaftalen er angivet til **Fuld måned**, er udløbsdatoen den første dag i måneden, hvor startdatoen for leasingaftalen ligger.

Datoen for tilskrivningen bestemmer startdatoen for perioden for passiv-amortisering og afskrivningsplaner for aktiver. Renteudgifter og afskrivningsudgifter bogføres på periodens slutdato for de tilsvarende planer. Den første registrering af genkendelse og kladdeposten til justering bogføres på ikrafttrædelsesdatoen.

> [!NOTE]
> Funktionen til leasingkonventioner kan aktiveres via Funktionsstyring. I arbejdsområdet i **Funktionsstyring** skal du finde og vælge den funktion, der hedder **Leasingkonvention for leasingfunktionen**, og derefter vælge **Aktivér nu**.

Leasingkonventioner knyttes til opsætningen af et leasinganlægskartotek.

Benyt følgende fremgangsmåde for at få vist eller angive leasingkonventionen.

1. Gå til **Aktivleasing \> Konfiguration \> Leasingkartotek**.
2. Vælg en af følgende værdier i feltet **Leasingkonvention**.

    | Leasingkonvention | Betegnelse |
    |--------------------|-------------|
    | None               | Amortisations- og afskrivningsplaner for aktiver træder i gang på startdatoen for leasingaftalen, da startdatoen for afskrivningen er lig med startdatoen for leasingaftalen. Slutdatoen er én måned senere. Denne leasingkonvention garanterer ikke, at renten vil blive bogført den sidste dag i hver måned. |
    | Hel måned         | For leasingaftaler, der har en startdato, der finder sted på et vilkårligt tidspunkt i løbet af måneden, starter amortisations- og afskrivningsplanerne for aktiver for at periodisere udgifter den første dag i den pågældende måned. Denne leasingkonvention sikrer, at der påløber renter på den sidste dag i hver måned for hele måneden. |

3. Vælg **Gem**.

Når en leasingaftale oprettes, angives startdatoen for hvert kartotek automatisk på baggrund af den startdato, der er angivet for lejen, og den leasingkonvention, der er angivet i kartoteket.
