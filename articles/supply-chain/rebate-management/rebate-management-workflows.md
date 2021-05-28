---
title: Arbejdsprocesser for rabatstyringsaftale
description: Dette emne indeholder en forklaring på, hvordan du kan konfigurere en arbejdsproces for rabatstyringsaftaler for at godkende og aktivere aftaler.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee342de6d069131e230120c5d65aef58da8e632a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020380"
---
# <a name="rebate-management-deal-workflows"></a>Arbejdsprocesser for rabatstyringsaftale

[!include [banner](../includes/banner.md)]

Når rabataftaler skal godkendes, bruger Rabatstyring samme arbejdsprocesplatform som andre Finance and Operations-apps. Der er knyttet to jobprocesser til hver arbejdsproces:

- Et element i arbejdsprocessen aktiverer aftalen, så brugeren eller arbejdsprocessen kan godkende transaktionerne.
- Et element i arbejdsprocessen godkender aftalen.

Før du kan bruge en rabataftale, skal den være aktiv i modulet **Rabatstyring**. Hvis du vil aktivere en aftale, skal du først oprette og konfigurere en *Arbejdsproces for rabatstyringsaftale*.

Når der er aktiveret en arbejdsproces for Rabatstyring, kan brugerne ikke godkende aftaler manuelt. Arbejdsprocessen skal altid bruges.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>Oprette og administrere arbejdsprocesser for rabatstyringsaftale

Du kan arbejde med arbejdsprocesser for rabatstyringsaftaler ved at gå til **Rabatstyring \> Konfiguration \> Arbejdsprocesser for rabatstyring**. Her kan du se, oprette og opdatere arbejdsprocesser efter behov. Der kan kun være én aktiv arbejdsproces ad gangen af denne type. Yderligere oplysninger om arbejdsprocesser, hvordan du arbejder med siden **Arbejdsprocesser for rabatstyring**, og hvordan du opretter arbejdsprocesser, finder du i [oversigten over arbejdsprocessystemet](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) og de relaterede emner.

## <a name="use-a-workflow-to-activate-a-deal"></a>Bruge en arbejdsproces til at aktivere en aftale

Hvis du vil aktivere en aftale via en arbejdsproces, skal du åbne aftalen (f.eks. på siden **Alle rabatstyringsaftaler**). Vælg derefter **Arbejdsproces \> Send** i handlingsruden. Når den nye aftale er behandlet og godkendt via arbejdsprocessen, er den aktiv og klar til brug.

Når en aftale er blevet aktiveret, kan du ikke ændre opsætningen. Hvis du skal ændre en aktiv aftale, skal du deaktivere den og derefter oprette en ny aftale. Hvis den nye aftale skal ligne den gamle aftale, kan du oprette den ved at kopiere den gamle aftale.
