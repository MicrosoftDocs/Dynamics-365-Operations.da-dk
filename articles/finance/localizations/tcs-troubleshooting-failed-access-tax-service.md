---
title: Der kunne ikke opnås adgang til momsservice
description: Denne artikel beskriver, hvordan du foretager fejlfinding af manglende adgang til momsberegningstjenesten.
author: hangwan
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 02/16/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 65d819b97be3d1238bc0ecfc201b4e24edac8616
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861216"
---
# <a name="failed-to-access-tax-service"></a>Der kunne ikke opnås adgang til momsservice

[!include [banner](../includes/banner.md)]


Denne artikel forklarer, hvordan du kan rette fejlen "Der kunne ikke opnås adgang til momsservice" i momsberegningstjenesten.

## <a name="symptoms"></a>Symptomer

I Microsoft Dynamics 365 Finance skal du gå til **Moms** \> **Konfiguration** \> **Momskonfiguration** \> **Parametre for momstjeneste**. Under fanen **Generelt** skal du aktivere indstillingen **Aktivér momsberegning**. Hvis du derefter forsøger at vælge en værdi i feltet **Navn på funktionsopsætning**, opstår der en fejl. Fejlmeddelelsen er "Der kunne ikke opnås adgang til momsservice".

## <a name="cause"></a>Årsag

Denne fejl opstår, fordi Finans ikke kan få adgang til tjenesten Momsberegning.

## <a name="resolution"></a>Løsning 

1. Log på Microsoft Dynamics LifeCycle Services (LCS).
2. På siden **Miljø** under fanen **Miljøtilføjelsesprogrammer** skal du finde elementet **Momsberegning** og vurdere dens status. Status bør være **Installerer** eller **Installeret**. Hvis tilføjelsesprogrammet Momsberegningstjeneste ikke er installeret, vises fejlen.

## <a name="mitigation"></a>Afhjælpning

1. I LCS skal du vælge **Installer et nyt tilføjelsesprogram** på siden **Finans** i afsnittet **Integration af Power Platform**.
2. Rul til den nederste del af siden, og vælg tilføjelsesprogrammet **Momsberegning** for at installere det.
3. Vend tilbage til dit økonomimiljø, og prøv at få adgang til tjenesten Momsberegning.

> [!NOTE]
> Før du installerer tjenesten Momsberegning, skal du gennemgå [forudsætningerne for momsberegningstjenesten](global-get-started-with-tax-calculation-service.md#prerequisites).
> 
> Hvis du ikke kan installere tilføjelsesprogrammet, fordi afsnittet **Integration af Power Platform** ikke er tilgængeligt, kan du finde flere oplysninger i [Oversigt over tilføjelsesprogrammer](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Hvis der stadig opstår fejl, efter du har installeret tilføjelsesprogrammet, skal du kontakte systemadministratoren.
