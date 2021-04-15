---
title: Bruge Dynamics 365 Commerce-prissætningsprogrammet med Dynamics 365 Sales
description: Dette emne beskriver, hvordan du bruger Microsoft Dynamics 365 Commerce-prissætningsprogrammet til at oprette salgstilbud i Dynamics 365 Sales.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: cd784bb37eddfc74699d1070eab453a3b527201a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560267"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>Bruge Dynamics 365 Commerce-prissætningsprogrammet med Dynamics 365 Sales

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du bruger Microsoft Dynamics 365 Commerce-prissætningsprogrammet til at oprette salgstilbud i Dynamics 365 Sales.

Dynamics 365 Commerce-prissætningsprogrammet understøtter de fleste B2C-prissætningsscenarier (business-to-consumer), f.eks. prisfastsættelse på butiksniveau, tilknytningsbaseret og loyalitetsbaseret prisfastsættelse, mix og match-rabatter, mængderabatter og tærskelrabatter. Prissætningsprogrammet bruger komplekse regler til at bestemme den bedste pris for et givet tilbud eller en given ordre.

Når du bruger [dobbeltskrivning](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), har du tre muligheder for dine prisfastsættelsesbehov. Du kan bruge den statiske prisfastsættelse, der kommer fra prislisten i Dynamics 365 Sales, prissætningsprogrammet i Dynamics 365 Supply Chain Management eller prissætningsprogrammet i Dynamics 365 Commerce. Blandt disse muligheder er Commerce-prissætningsprogrammet bedst egnet til B2C-scenarier.

## <a name="use-the-commerce-pricing-engine-in-sales"></a>Bruge Commerce-prissætningsprogrammet i Sales

> [!NOTE]
> I øjeblikket kan Commerce-prissætningsprogrammet kun bruges til oprettelse af tilbud i Sales. Salgsordreintegration med Commerce-prissætningsprogrammet er endnu ikke tilgængelig.

Når brugere starter et tilbud i Sales, kopierer dobbeltskrivningsstrukturen tilbudsdetaljerne til Commerce. Eventuelle ændringer i eksisterende tilbudslinjer eller tilbudslinjer, der er tilføjet for nylig i Sales, kopieres til Commerce. Når brugere vil bruge Commerce-prissætningsprogrammet til at prissætte tilbuddet, kan de vælge **Pristilbud** for at opdatere priser for tilbuddet ud fra Commerce-prissætningsprogrammet. Priserne opdateres derefter automatisk i både Sales og Commerce.

## <a name="prerequisites"></a>Forudsætninger

- Før du kan bruge Commerce-prissætningsprogrammet i Sales, skal du følge fremgangsmåderne i [Kundeemne til kontanter i dobbeltskrivning](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).
- Du skal deaktivere evaluering af samhandelsaftale for manuel indtastning ved at følge disse trin:

    1. Gå til **Debitor \> Opsætning \> Debitorparametre** i Commerce-miljøet.
    1. Under fanen **Priser** i oversigtspanelet **Evaluering af samhandelsaftale** skal du fjerne markeringen i afkrydsningsfeltet **Manuel indtastning**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Kundeemner til kontanter og to skrivninger](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]