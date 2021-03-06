---
title: Refusion af en returordre afvises
description: Dette emne indeholder vejledning i fejlfinding, der kan hjælpe, når en refusion på en returordre afvises, fordi det kreditkort, der bruges til fakturering, ikke er det samme som det kort, der blev brugt under den oprindelige betalingsgodkendelse.
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
ms.openlocfilehash: 99fd4b816b1a3a1fe3c2d1579be45b43fdc3d385
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020750"
---
# <a name="refund-on-a-return-order-is-declined"></a>Refusion af en returordre afvises

[!include [banner](../../includes/banner.md)]

Dette emne indeholder vejledning i fejlfinding, der kan hjælpe, når en refusion på en returordre afvises, fordi det kreditkort, der bruges til fakturering, ikke er det samme som det kort, der blev brugt under den oprindelige betalingsgodkendelse.

## <a name="description"></a>Betegnelse

En refusion afvises, når det kreditkort, der bruges til at fakturere en returordre, afviger fra det kort, der blev brugt under den oprindelige betalingsgodkendelse. Du får vist følgende fejlmeddelelse: "Nogle betalinger har ikke den korrekte status til bogføring. Valider status for alle betalinger inden faktureringen igen."

Oplysningerne om betalingstilladelsen indeholder følgende fejlmeddelelse: "Adyen-gateway SendRequest() mislykkedes med status 'InternalServerError'.22144; Tomt svar, der returneres fra Adyen.(22001);"

![Afviste refusion af en returordre](media/refund-order-decline.jpg)

## <a name="resolution"></a>Løsning

### <a name="enable-blind-returns-in-adyen"></a>Aktiver skjulte returneringer i Adyen

Hvis du vil aktivere skjulte returneringer, skal du udføre trinnene i [Fejlfinding af Dynamics 365 Payment Connector for Adyen-problemer](adyen-support.md), så du kan kontakte Adyen-supportteamet og anmode om, at skjulte returneringer aktiveres på din Adyen-forhandlerkonto.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dynamics 365-betalingsconnector til Adyen](../dev-itpro/adyen-connector.md)

[Konfigurer Adyen-betalingsconnector til Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
