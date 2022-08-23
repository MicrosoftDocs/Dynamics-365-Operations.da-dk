---
title: Konvertere asynkrone kunder til synkrone kunder
description: Denne artikel forklarer, hvordan du konverterer asynkrone kunder til synkrone kunder i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: b442bfc0685706359771e4d9e2729565d3652a60
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278186"
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
