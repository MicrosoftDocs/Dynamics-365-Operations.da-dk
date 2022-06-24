---
title: Konvertere asynkrone kunder til synkrone kunder
description: Denne artikel forklarer, hvordan du konverterer asynkrone kunder til synkrone kunder i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 0ce4906816deab8824b1079a34489e55651c0e03
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884385"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>Konvertere asynkrone kunder til synkrone kunder

[!include [banner](includes/banner.md)]

Denne artikel forklarer, hvordan du konverterer asynkrone kunder til synkrone kunder i Microsoft Dynamics 365 Commerce.

Følg disse trin for at konvertere asynkrone kunder til synkrone kunder.

1. I Commerce Headquarters skal du køre **P-jobbet** for at sende de asynkrone kunder til Commerce Headquarters.
1. Kør jobbet **Synkroniser kunder og forretningspartnere fra asynkron tilstand** for at oprette debitorkonto-id'er. (Dette job blev tidligere kaldt **Synkroniser kunder og forretningspartnere fra asynkron tilstand**.)
1. Kør jobbet **1010** for at synkronisere de nye debitorkonto-id'er med kanalerne.

Hvis en ordre refererer til en asynkron kunde eller adresse, der endnu ikke er synkroniseret med Commerce Headquarters, synkroniseres kunden eller adressen som en del af batchjobbet **Synkroniser ordrer**. Hvis en cash and carry-transaktion refererer til en asynkron kunde eller adresse, synkroniseres kunden eller adressen før bogføringen i slutningen af dagen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Kundestyring i butikker](customer-mgmt-stores.md)

[Oprettelsestilstand for asynkron kunde](async-customer-mode.md)

[Debitorattributter](dev-itpro/customer-attributes.md)

[Offline-dataudelukkelse](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
