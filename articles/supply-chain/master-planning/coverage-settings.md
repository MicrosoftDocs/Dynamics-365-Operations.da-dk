---
title: Disponeringsindstillinger
description: "Ved behovsplanlægning anvendes disponeringsindstillinger til at beregne varebehov."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fb11a470d98a9742749daaac3244a5bb0d3a689c
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="coverage-settings"></a>Disponeringsindstillinger

[!include[banner](../includes/banner.md)]


Ved behovsplanlægning anvendes disponeringsindstillinger til at beregne varebehov. 

Du kan angive disponeringsindstillinger på flere måder:

-   Angiv disponeringsindstillinger for en disponeringsgruppe. Du kan oprette en disponeringsgruppe, der indeholder alle produkter, der er knyttet til disponeringsgruppen. Klik på **Varedisponering &gt; Konfiguration &gt; Disponering &gt; Disponeringsgrupper** for at oprette en disponeringsgruppe. Du kan sammenkæde en disponeringsgruppe til et produkt. Hvis sammenkædningen er specifik for et websted, et lagersted eller en produktdimension, skal du bruge feltet **Disponeringsgruppe** på siden **Varedisponering**. Hvis sammenkædningen er generisk, uanset produktdimensionerne, skal du bruge **Disponeringsgruppe** på oversigtspanelet **Plan** på siden **Produktdetaljer**. Hvis du ikke knytter en disponeringsgruppe til et produkt, bruger den overordnede planlægning som standard den **standarddisponeringsgruppe**, der er angivet på siden **Varedisponeringsparametre**.

-   Angiv disponeringsindstillinger for et produkt. Du kan oprette disponeringsindstillinger for et bestemt produkt. Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**. Vælg produktet, og klik på **Varedisponering** i gruppen **Disponering** under fanen **Plan** i **handlingsruden** for at åbne siden **Varedisponering**. Hvis produktet allerede er knyttet til en dispositionsgruppe, kan du tilsidesætte indstillingerne for dispositionsgruppen ved hjælp af feltet **Tilsidesæt**. Disponeringsindstillinger på siden **Varedisponering** har fortrinsret over indstillingerne på siden **Dækningsgruppe**.

<!-- -->

-   Angiv disponeringsindstillinger for et produkt ved hjælp af en guide. Guiden giver dig en trinvis vejledning i at konfigurere de primære dispositionsparametre for varer. På siden **Varedisponering** skal du klikke på **Guide** at åbne **Varedisponeringsguide**.

<!-- -->

-   Angiv disponeringsindstillinger for en dimensionsgruppe. Klik på **Administration af produktoplysninger &gt; Almindelige &gt; Frigivne produkter**. Klik på linket **Lagringsdimensionsgruppe** i gruppen **Administration** under fanen **Generelt** på siden **Frigivne produktdetaljer**. Vælg **Lagringsdimensionsgruppe** i feltet **Disponer pr. dimension** for at oprette dispositionsindstillinger for en dimension i lagringsdimensionsgruppen. Alle produktdimensioner, f.eks. konfiguration, farve, størrelse, typografi, skal have feltet **Disponer pr. dimension** markeret.



<a name="see-also"></a>Se også
--------

[Behovsplaner](master-plans.md)




