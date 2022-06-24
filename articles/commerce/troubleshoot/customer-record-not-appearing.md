---
title: Debitorposter vises ikke i Commerce Headquarters
description: Denne artikel indeholder en vejledning i fejlfinding, der kan hjælpe, når kundeposter ikke omgående vises i Commerce Headquarters.
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
ms.openlocfilehash: 5cdc96c9829be4d34e9346b2c99d300c2349bc41
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876539"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a>Debitorposter vises ikke i Commerce Headquarters

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder en vejledning i fejlfinding, der kan hjælpe, når kundeposter ikke omgående vises i Commerce Headquarters.

## <a name="description"></a>Betegnelse

Når du opretter en ny kundepost ved hjælp af tilmeldingsflowet i e-commerce storefronten, vises den tilsvarende debitorpost ikke med det samme i Commerce Headquarters.

## <a name="resolution"></a>Løsning

### <a name="disable-customer-creation-in-async-mode"></a>Deaktivere kundeoprettelse i async-tilstand

> [!IMPORTANT]
> Hvis du deaktiverer asynkron oprettelse af kunder, kan det påvirke systemets ydeevne, da oprettelsen af hver post vil medføre en anmodning i realtid til Commerce Headquarters. Hvis Commerce Headquarters er nede (f.eks. under servicering af flow), vil nye kundeoprettelsesflow desuden give fejl.

Hvis du vil deaktivere kundeoprettelse i async-tilstand i Commerce Headquarters, skal du følge disse trin.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Konfiguration af onlinebutik \> Funktionalitetsprofiler**.
1. Hvis du ikke allerede bruger en funktionalitetsprofil til din onlinekanal, skal du oprette en.
1. Sørg for, at indstillingen **Opret debitor i async-tilstand** er angivet til **Nej**.
1. Gå til **Retail og Commerce \> Kanaler \> Onlinebutikker**.
1. Vælg den onlinebutik, der skal deaktiveres asynkron oprettelse af kunder for.
1. Under fanen **Generelt** skal du kontrollere, at feltet **Funktionalitetsprofil** er angivet til den funktionalitetsprofil, du bruger til din onlinekanal.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere en B2C-lejer i Commerce](../set-up-b2c-tenant.md)
