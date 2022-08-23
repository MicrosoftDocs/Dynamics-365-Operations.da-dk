---
title: Konfigurere servicemiljøer og tilsluttede programmer
description: Denne artikel indeholder oplysninger om, hvordan du konfigurerer dine servicemiljøer og tilsluttede programmer.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 8ede98cfad685992bad3fb643ea46d6adcb08487
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269525"
---
# <a name="configure-service-environments-and-connected-applications"></a>Konfigurere servicemiljøer og tilsluttede programmer

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om, hvordan du konfigurerer dine servicemiljøer og tilsluttede programmer. Der er tre trin i denne proces. Trin 1 er obligatorisk, og trin 2 og 3 er valgfrie.

## <a name="step-1-create-a-service-environment"></a>Trin 1: Opret et servicemiljø

Når du opretter dit servicemiljø, skal du definere listen over brugere, der kan udrulle globaliseringsfunktioner til det. Du kan eventuelt definere listen over eksterne programmer, der kan kommunikere med tjenesten Elektronisk fakturering, i nogle af scenarierne. Konfigurer nummerserier, hvis du vil bruge dem i dine scenarier.

Se [Servicemiljøer](e-invoicing-service-environments.md) for at udføre dette trin.

## <a name="step-2-add-certificates-and-secrets"></a>Trin 2: Tilføj certifikater og hemmeligheder

Tilføj en reference til Microsoft Azure Key Vault og hemmeligheder, så du kan bruge dem i scenarierne. Dette trin er obligatorisk, hvis handlingerne i behandlingspipelines bruger certifikater og hemmeligheder til digital signering eller kommunikation med eksterne webtjenester.

Du kan udføre dette trin i [Kundecertifikater og -hemmeligheder](e-invoicing-customer-certificates-secrets.md).

## <a name="step-3-configure-connected-applications"></a>Trin 3: Konfigurer tilsluttede programmer

Inden du kan oprette kommunikation mellem Dynamics 365 Finance eller Dynamics 365 Supply Chain Management-programmer og elektroniske faktureringer, skal du konfigurere Finance eller Supply Chain Management til at opbygge kaldet til tjenesten Elektronisk fakturering og klargøre forretningsdata i en samlet struktur, der kan konverteres til det nødvendige elektroniske format. Programmerne skal også behandle svar fra tjenesten korrekt. Du kan udføre denne konfiguration direkte i dit Finans- eller Supply Chain Management-miljø, eller du kan fuldføre den i Regulatory Configuration Service (RCS). Hvis du fuldfører konfigurationen i RCS, kan du derefter implementere den i dit Finans- eller Supply Chain Management-miljø. I dette trin registrerer du det tilsluttede program til parameterudrulning.

Se [Tilsluttede programmer](e-invoicing-connected-applications.md) for at udføre dette trin.
