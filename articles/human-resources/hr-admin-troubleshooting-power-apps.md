---
title: Kan ikke oprette et miljø i Power Apps Administration
description: I denne artikel beskrives det, hvad du skal gøre, hvis administratoren ikke kan oprette et miljø i Microsoft Power Apps Administration.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 68e6dbcbbc9811211570e968047f5faa8a2c8bd0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417783"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Kan ikke oprette et miljø i Power Apps Administration

**Udsted**

- Lejeren/miljøadministratoren kan ikke oprette et miljø i Microsoft Power Apps Administration.
- Der er ikke blevet tildelt en licens, der giver brugerne ret til at udføre miljøoprettelsestrinnet, direkte til den bruger, der udfører dette trin.

**Løsning**

Kontrollér, at lejeradministratoren har tildelt en gyldig licens til Power Apps P2 direkte til den bruger, der skal udføre miljøoprettelsestrinnet. Her er de Microsoft Dynamics-serviceplaner, der indeholder denne rettighed.

| Overordnet produktlagerenhed (SKU)       | Serviceplan for Power Apps P2  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps til Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | Power Apps til Dynamics 365 |

Bemærk, at forskellige Microsoft Office-SKU'er også giver rettigheden sammen med enkeltstående Power Apps Plan 2-SKU'er. Det vigtigste er, at der findes en af disse SKU'er.

1. Gå til [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Opret miljøerne ved at følge vejledningen i [Klargøre Personale](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).


[!INCLUDE[footer-include](../includes/footer-banner.md)]