---
title: Konventioner i aktivleasing
description: Denne artikel beskriver konventionerne leasede aktiver.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f2f0e21b20a969c0847ce3a6eb167287c1d7ee3e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898263"
---
# <a name="asset-leasing-conventions"></a>Konventioner i aktivleasing

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikel beskriver konventionerne leasede aktiver. Leasingkonventioner bruges til at bestemme startdatoen for leasingkartoteket. Hvis leasingaftalen er angivet til **Ingen**, er startdatoen den samme som startdatoen for leasingaftalen (det vil sige værdien af feltet **Startdato for leasingaftalen**). Hvis leasingaftalen er angivet til **Fuld måned**, er udløbsdatoen den første dag i måneden, hvor startdatoen for leasingaftalen ligger.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
