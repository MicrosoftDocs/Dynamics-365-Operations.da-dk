---
title: Debitorposter vises ikke i Commerce Headquarters
description: Denne artikel indeholder en vejledning i fejlfinding, der kan hjælpe, når kundeposter ikke omgående vises i Commerce Headquarters.
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
ms.openlocfilehash: f1ad1f45abbc95cbf6d41b3c8681db781c6c9d23
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268832"
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
