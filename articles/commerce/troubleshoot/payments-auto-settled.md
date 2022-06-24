---
title: Betalinger udlignes automatisk, før ordrer faktureres eller afsendes
description: Denne artikel indeholder en vejledning til fejlfinding, der kan hjælpe, når en betaling udlignes i portalen Adyen umiddelbart efter, at en ordre er afgivet, selvom salgsordren ikke er blevet faktureret eller afsendt.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c01a2fda54e198a43fa84ae83686fc1701958b6b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890263"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>Betalinger udlignes automatisk, før ordrer faktureres eller afsendes

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder en vejledning til fejlfinding, der kan hjælpe, når en betaling udlignes i portalen Adyen umiddelbart efter, at en ordre er afgivet, selvom salgsordren ikke er blevet faktureret eller afsendt.

## <a name="description"></a>Betegnelse

Når en ordre er afgivet, håndteres betalingen med det samme i portalen Adyen, selvom salgsordren ikke er blevet faktureret eller afsendt.

## <a name="resolution"></a>Løsning

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>Konfigurere manuel hentning af e-handelsbetalinger på Adyen-portalen

Følg disse trin for af konfigurere manuel hentning af e-handelsbetalinger på Adyen-portalen.

1. Log på Adyen-portalen.
1. Øverst til højre kan du vælge den handlendes konto for e-handelskanalen.
1. På den øverste navigationslinje skal du vælge **Konto** og derefter **Indstillinger**.
1. Vælg **manuel** i feltet **Hent forsinkelse**.

    ![Indstillingen Hent forsinkelse i Adyen-portalen.](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>Yderligere ressourcer

[Adyen-betalingsregistrering](https://docs.adyen.com/point-of-sale/capturing-payments)

[Dynamics 365 Payment Connector til Adyen](../dev-itpro/adyen-connector.md)

[Konfigurer Adyen-betalingsconnector til Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
