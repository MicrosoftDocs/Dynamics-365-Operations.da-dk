---
title: Kan ikke oprette et miljø i Power Apps Administration
description: I dette emne beskrives, hvad du skal gøre, hvis administratoren ikke kan oprette et miljø i Microsoft Power Apps Administration.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 937b372fa95c8076666aed14c2b34b12e8029c4d
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067698"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Kan ikke oprette et miljø i Power Apps Administration


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Udsted**

- Lejeren/miljøadministratoren kan ikke oprette et miljø i Microsoft Power Apps Administration.
- Brugeren har ikke en licens, der giver ret til at oprette miljøer.

**Løsning**

Sørg for, at lejeradministratoren har tildelt en gyldig Power Apps P2-licens til den bruger, der opretter miljøet. Følgende Microsoft Dynamics-serviceplaner indeholder rettigheder til at oprette miljøer:

| Overordnet produktlagerenhed (SKU)       | Serviceplan for Power Apps P2  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps til Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | Power Apps til Dynamics 365 |

Bemærk, at forskellige Microsoft Office-SKU'er også giver rettigheden sammen med enkeltstående Power Apps Plan 2-SKU'er. Det vigtigste er, at der findes en af disse SKU'er.

1. Gå til [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Opret miljøerne ved at følge vejledningen i [Klargøre Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
