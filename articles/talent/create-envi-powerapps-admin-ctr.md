---
title: "Det er ikke muligt at oprette et miljø i PowerApps Administration"
description: "I dette emne beskrives, hvad du skal gøre, hvis administratoren ikke kan oprette et miljø i Microsoft PowerApps Administration."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.contentlocale: da-dk
ms.lasthandoff: 12/04/2018

---

# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a>Det er ikke muligt at oprette et miljø i PowerApps Administration

[!include [banner](includes/banner.md)]

**Afgang**

- Lejeren/miljøadministratoren kan ikke oprette et miljø i Microsoft PowerApps Administration.
- Der er ikke blevet tildelt en licens, der giver brugerne ret til at udføre miljøoprettelsestrinnet, direkte til den bruger, der udfører dette trin.

**Løsning**

Kontrollér, at lejeradministratoren har tildelt en gyldig licens til PowerApps P2 direkte til den bruger, der skal udføre miljøoprettelsestrinnet. Her er de Microsoft Dynamics-serviceplaner, der indeholder denne rettighed.

| Overordnet produktlagerenhed (SKU)       | PowerApps P2 serviceplan  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | PowerApps for Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | PowerApps for Dynamics 365 |

Bemærk, at forskellige Microsoft Office SKU'er også giver rettigheden sammen med enkeltstående PowerApps Plan 2 SKU'er. Det vigtigste er, at der findes en af disse SKU'er.

1. Gå til [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Opret miljøerne ved at følge vejledningen i [Klargøre Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).
