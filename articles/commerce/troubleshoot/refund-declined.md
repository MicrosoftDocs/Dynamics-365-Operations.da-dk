---
title: Refusion af en returordre afvises
description: Denne artikel indeholder vejledning i fejlfinding, der kan hjælpe, når en refusion på en returordre afvises, fordi det kreditkort, der bruges til fakturering, ikke er det samme som det kort, der blev brugt under den oprindelige betalingsgodkendelse.
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
ms.openlocfilehash: d8d1c40673d4b159a7b7bf00bf6011ba45f47edd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268226"
---
# <a name="refund-on-a-return-order-is-declined"></a>Refusion af en returordre afvises

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder vejledning i fejlfinding, der kan hjælpe, når en refusion på en returordre afvises, fordi det kreditkort, der bruges til fakturering, ikke er det samme som det kort, der blev brugt under den oprindelige betalingsgodkendelse.

## <a name="description"></a>Betegnelse

En refusion afvises, når det kreditkort, der bruges til at fakturere en returordre, afviger fra det kort, der blev brugt under den oprindelige betalingsgodkendelse. Du får vist følgende fejlmeddelelse: "Nogle betalinger har ikke den korrekte status til bogføring. Valider status for alle betalinger inden faktureringen igen."

Oplysningerne om betalingstilladelsen indeholder følgende fejlmeddelelse: "Adyen-gateway SendRequest() mislykkedes med status 'InternalServerError'.22144; Tomt svar, der returneres fra Adyen.(22001);"

![Afviste refusion af en returordre.](media/refund-order-decline.jpg)

## <a name="resolution"></a>Løsning

### <a name="enable-blind-returns-in-adyen"></a>Aktiver skjulte returneringer i Adyen

Hvis du vil aktivere skjulte returneringer, skal du udføre trinnene i [Fejlfinding af Dynamics 365 Payment Connector for Adyen-problemer](adyen-support.md), så du kan kontakte Adyen-supportteamet og anmode om, at skjulte returneringer aktiveres på din Adyen-forhandlerkonto.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dynamics 365-betalingsconnector til Adyen](../dev-itpro/adyen-connector.md)

[Konfigurer Adyen-betalingsconnector til Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
