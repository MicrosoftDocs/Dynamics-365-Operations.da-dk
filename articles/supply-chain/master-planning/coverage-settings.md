---
title: Disponeringsindstillinger
description: Dette emne indeholder oplysninger om de indstillinger for disponering, som behovsplanlægningen bruger til at beregne varebehov.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538888"
---
# <a name="coverage-settings"></a>Disponeringsindstillinger

[!include [banner](../includes/banner.md)]

Ved behovsplanlægning anvendes disponeringsindstillinger til at beregne varebehov.

Du kan angive disponeringsindstillinger på flere måder:

- Angiv disponeringsindstillinger for en disponeringsgruppe.

    Du kan oprette en disponeringsgruppe, der indeholder alle produkter, der er knyttet til disponeringsgruppen. Du kan oprette en disponeringsgruppe ved at gå til **Varedisponering &gt; Konfiguration &gt; Disponering &gt; Disponeringsgrupper**. Du kan sammenkæde en disponeringsgruppe til et produkt. Hvis sammenkædningen er specifik for et websted, et lagersted eller en produktdimension, skal du bruge feltet **Disponeringsgruppe** på siden **Varedisponering**. Hvis sammenkædningen er generisk, uanset produktdimensionerne, skal du bruge feltet **Disponeringsgruppe** på oversigtspanelet **Plan** på siden **Produktdetaljer**. Hvis du som standard ikke knytter en disponeringsgruppe til et produkt, bruger den overordnede planlægning den standarddisponeringsgruppe, der er angivet på siden **Varedisponeringsparametre**.

- Angiv disponeringsindstillinger for et produkt.

    Du kan oprette disponeringsindstillinger for et bestemt produkt. Gå til **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**. Vælg produktet, og vælg derefter **Varedisponering** i gruppen **Disponering** under fanen **Plan** i handlingsruden for at åbne siden **Varedisponering**. Hvis produktet allerede er knyttet til en dispositionsgruppe, kan du tilsidesætte indstillingerne for dispositionsgruppen ved hjælp af feltet **Tilsidesæt**. Disponeringsindstillinger på siden **Varedisponering** har fortrinsret over indstillingerne på siden **Dækningsgruppe**.

- Angiv disponeringsindstillinger for et produkt ved hjælp af en guide.

    Guiden hjælper dig trin for trin gennem opsætningen af de primære varedisponeringsparametre. På siden **Varedisponering** skal du i handlingsruden klikke på **Guide** for at åbne **Varedisponeringsguide**.

- Angiv disponeringsindstillinger for en dimensionsgruppe.

    Gå til **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**. Vælg linket feltet **Lagringsdimensionsgruppe** i sektionen **Administration** i oversigtspanelet **Generelt** på siden **Frigivne produktdetaljer**. På siden **Lagringsdimensionsgrupper** skal du markere afkrydsningsfeltet **Disponer pr. dimension** for at oprette dispositionsindstillinger for en dimension i lagringsdimensionsgruppen. Feltet **Disponer pr. dimension** skal være markeret for alle produktdimensioner, f.eks. konfiguration, farve, størrelse, typografi.

## <a name="additional-resources"></a>Yderligere ressourcer

[Behovsplaner](master-plans.md)
