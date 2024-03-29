---
title: Serviceniveau og -beskrivelse
description: Denne artikel beskriver serviceniveau og -beskrivelse i Styring af aktiver.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectServiceLevel, EntAssetWorkOrderStandardDescription, EntAssetWorkOrderServiceLevel, EntAssetServiceLevelLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 753ad36b1d01d1ce0594f477cf863ca0e4a1ac75
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879186"
---
# <a name="service-level-and-description"></a>Serviceniveau og -beskrivelse

[!include [banner](../../includes/banner.md)]

 

Når du opretter en arbejdsordre, kan det være en god ide at definere serviceniveauerne for den og føje en generel beskrivelse til den. Du kan oprette serviceniveauer for arbejdsordrer på siden **Serviceniveauer for arbejdsordrer** og beskrivelser på siden **Beskrivelse af arbejdsordre**.

## <a name="create-a-service-level"></a>Oprette et serviceniveau

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Arbejdsordrer** \> **Serviceniveau**.
2. Vælg **Ny**.
3. Angiv serviceniveauet i feltet **Serviceniveau** (f.eks. et nummer).
4. Indtast et navn i feltet **Navn**.

    I oversigtspanelet **Arbejdsordrer** kan du definere forventede start- og slutdatoer og -klokkeslæt. Felterne i dette oversigtspanel definerer den periode, hvor arbejdsordrer skal starte og slutte. De bruges til arbejdsordrer, der er oprettet manuelt, og arbejdsordrer, der oprettes på basis af vedligeholdelsesanmodninger. 

5. Angiv et antal dage i feltet **Startdag** for at definere den periode, hvor arbejdsordren skal starte. Antal dage beregnes på grundlag af oprettelsesdatoen i arbejdsordren. Hvis arbejdsordren f.eks. skal begynde, når den oprettes, skal du angive **0**. Hvis arbejdsordren skal starte inden for en uge efter, at den er oprettet, skal du angive **7**.
6. Hvis du vil angive et starttidspunkt for arbejdsordren, skal du ud over at angive en startdato vælge **Ja** i indstillingen **Angiv starttidspunkt**. Angiv derefter starttidspunktet i feltet **Starttidspunkt**. Hvis du vælger **Nej** i denne indstillingen, bruges det aktuelle tidspunkt på dagen.
7. Angiv et antal dage i feltet **Slutdag** for at definere den periode, hvor arbejdsordren skal slutte. Antal dage beregnes på grundlag af startdatoen i arbejdsordren. Hvis arbejdsordren f.eks. skal slutte inden for en uge fra startdatoen, skal du angive **7**.
8. Hvis du vil angive et sluttidspunkt for arbejdsordren, skal du ud over at angive en slutdato vælge **Ja** i indstillingen **Angiv sluttidspunkt**. Angiv derefter sluttidspunktet i feltet **Sluttidspunkt**. Hvis du vælger **Nej** i denne indstillingen, bruges det aktuelle tidspunkt på dagen.
9. Vælg **Gem**.

![Siden Serviceniveau for arbejdsordrer.](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a>Oprette en beskrivelse

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Arbejdsordrer** \> **Beskrivelser**.
2. Vælg **Ny**.
3. Indtast beskrivelsen i feltet **Beskrivelse**.
4. Vælg **Gem**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]