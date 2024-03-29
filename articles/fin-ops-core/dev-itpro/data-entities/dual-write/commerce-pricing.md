---
title: Bruge Dynamics 365 Commerce-prissætningsprogrammet med Dynamics 365 Sales
description: Denne artikel beskriver, hvordan du bruger Microsoft Dynamics 365 Commerce-prissætningsprogrammet til at oprette salgstilbud i Dynamics 365 Sales.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 11a164ec15c8b7a69172a153b961011a8b324712
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881388"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>Bruge Dynamics 365 Commerce-prissætningsprogrammet med Dynamics 365 Sales

[!include [banner](../../includes/banner.md)]

Denne artikel beskriver, hvordan du bruger Microsoft Dynamics 365 Commerce-prissætningsprogrammet til at oprette salgstilbud i Dynamics 365 Sales.

Dynamics 365 Commerce-prissætningsprogrammet understøtter de fleste B2C-prissætningsscenarier (business-to-consumer), f.eks. prisfastsættelse på butiksniveau, tilknytningsbaseret og loyalitetsbaseret prisfastsættelse, mix og match-rabatter, mængderabatter og tærskelrabatter. Prissætningsprogrammet bruger komplekse regler til at bestemme den bedste pris for et givet tilbud eller en given ordre.

Når du bruger [dobbeltskrivning](./dual-write-overview.md), har du tre muligheder for dine prisfastsættelsesbehov. Du kan bruge den statiske prisfastsættelse, der kommer fra prislisten i Dynamics 365 Sales, prissætningsprogrammet i Dynamics 365 Supply Chain Management eller prissætningsprogrammet i Dynamics 365 Commerce. Blandt disse muligheder er Commerce-prissætningsprogrammet bedst egnet til B2C-scenarier.

## <a name="use-the-commerce-pricing-engine-in-sales"></a>Bruge Commerce-prissætningsprogrammet i Sales

> [!NOTE]
> I øjeblikket kan Commerce-prissætningsprogrammet kun bruges til oprettelse af tilbud i Sales. Salgsordreintegration med Commerce-prissætningsprogrammet er endnu ikke tilgængelig.

Når brugere starter et tilbud i Sales, kopierer dobbeltskrivningsstrukturen tilbudsdetaljerne til Commerce. Eventuelle ændringer i eksisterende tilbudslinjer eller tilbudslinjer, der er tilføjet for nylig i Sales, kopieres til Commerce. Når brugere vil bruge Commerce-prissætningsprogrammet til at prissætte tilbuddet, kan de vælge **Pristilbud** for at opdatere priser for tilbuddet ud fra Commerce-prissætningsprogrammet. Priserne opdateres derefter automatisk i både Sales og Commerce.

## <a name="prerequisites"></a>Forudsætninger

- Før du kan bruge Commerce-prissætningsprogrammet i Sales, skal du følge fremgangsmåderne i [Kundeemne til kontanter i dobbeltskrivning](./dual-write-prospect-to-cash.md).
- Du skal deaktivere evaluering af samhandelsaftale for manuel indtastning ved at følge disse trin:

    1. Gå til **Debitor \> Opsætning \> Debitorparametre** i Commerce-miljøet.
    1. Under fanen **Priser** i oversigtspanelet **Evaluering af samhandelsaftale** skal du fjerne markeringen i afkrydsningsfeltet **Manuel indtastning**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Kundeemner til kontanter og to skrivninger](./dual-write-prospect-to-cash.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]