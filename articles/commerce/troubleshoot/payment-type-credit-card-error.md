---
title: Betalingstypen skal være kreditkortfejl på salgsordresiden
description: Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når der vises en fejlmeddelelse på salgsordresiden, efter at en ordre er synkroniseret.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: eabc64acc74645c7e6c7c4ab5794ed9fdb9dc997
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801669"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>"Betalingstypen skal være kreditkortfejl" på salgsordresiden

[!include [banner](../../includes/banner.md)]

Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når der vises en fejlmeddelelse på salgsordresiden, efter at en ordre er synkroniseret.

## <a name="description"></a>Betegnelse

Når du åbner salgsordresiden, efter at du har synkroniseret en ordre, får du følgende fejlmeddelelse: "Betalingstypen skal være kreditkort, da kreditkortnummeret er angivet".

![Betalingstypen skal være kreditkortfejl](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Løsning

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Angive betalingstypen i Commerce Headquarters

1. Gå til **Debitor \> Betalingsopsætning \> Betalingsbetingelser**.
1. Vælg betalingsbetingelserne i den venstre navigationsrude.
1. Kontroller, at **Kreditkort** er valgt i feltet **Betalingstype**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Bogføre onlinesalg og -betalinger](../tasks/posting-online-sales-payments.md)
