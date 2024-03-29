---
title: Betalingstypen skal være kreditkortfejl på salgsordresiden
description: Denne artikel indeholder en vejledning i fejlfinding, der kan hjælpe, når der vises en fejlmeddelelse på salgsordresiden, efter at en ordre er synkroniseret.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 71c5cbaf574866c74e222f4d67132004327db8fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285626"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>"Betalingstypen skal være kreditkortfejl" på salgsordresiden

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder en vejledning i fejlfinding, der kan hjælpe, når der vises en fejlmeddelelse på salgsordresiden, efter at en ordre er synkroniseret.

## <a name="description"></a>Betegnelse

Når du åbner salgsordresiden, efter at du har synkroniseret en ordre, får du følgende fejlmeddelelse: "Betalingstypen skal være kreditkort, da kreditkortnummeret er angivet".

![Betalingstypen skal være kreditkortfejl.](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Løsning

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Angive betalingstypen i Commerce Headquarters

1. Gå til **Debitor \> Betalingsopsætning \> Betalingsbetingelser**.
1. Vælg betalingsbetingelserne i den venstre navigationsrude.
1. Kontroller, at **Kreditkort** er valgt i feltet **Betalingstype**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Bogføre onlinesalg og -betalinger](../tasks/posting-online-sales-payments.md)
