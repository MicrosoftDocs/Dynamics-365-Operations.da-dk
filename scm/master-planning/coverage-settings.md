---
title: Disponeringsindstillinger
description: "Ved behovsplanlægning anvendes disponeringsindstillinger til at beregne varebehov."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c1c5654afa6b592e178af052e3e4a7e246a94c9f
ms.lasthandoff: 03/31/2017


---

# <a name="coverage-settings"></a>Disponeringsindstillinger

Ved behovsplanlægning anvendes disponeringsindstillinger til at beregne varebehov. 

Du kan angive disponeringsindstillinger på flere måder:

-   Angiv disponeringsindstillinger for en disponeringsgruppe. Du kan oprette en disponeringsgruppe, der indeholder alle produkter, der er knyttet til disponeringsgruppen. Klik på **Master planning &gt;Setup &gt;dækning &gt;Disponeringsgrupper** til at oprette en disponeringsgruppe. Du kan sammenkæde en disponeringsgruppe til et produkt. Hvis sammenkædningen er specifik for et websted, et lagersted eller en produktdimension, skal du bruge feltet **Disponeringsgruppe** på siden **Varedisponering**. Hvis sammenkædningen er generisk, uanset produktdimensionerne, skal du bruge **Disponeringsgruppe** på oversigtspanelet **Plan** på siden **Produktdetaljer**. Hvis du ikke knytter en disponeringsgruppe til et produkt, bruger den overordnede planlægning som standard den **standarddisponeringsgruppe**, der er angivet på siden **Varedisponeringsparametre**.

-   Angiv disponeringsindstillinger for et produkt. Du kan oprette disponeringsindstillinger for et bestemt produkt. Klik på **administration af produktoplysninger &gt;produkter &gt;frigivne produkter**. Vælg produktet, på den **handlingsruden**under den **Plan** under fanen den **disponeringsgruppe**, skal du klikke på **Varedisponering** at åbne den **Varedisponering** side. Hvis produktet allerede er knyttet til en dispositionsgruppe, kan du tilsidesætte indstillingerne for dispositionsgruppen ved hjælp af feltet **Tilsidesæt**. Disponeringsindstillinger på siden **Varedisponering** har fortrinsret over indstillingerne på siden **Dækningsgruppe**.

<!-- -->

-   Angiv disponeringsindstillinger for et produkt ved hjælp af en guide. Guiden giver dig en trinvis vejledning i at konfigurere de primære dispositionsparametre for varer. På siden **Varedisponering** skal du klikke på **Guide** at åbne **Varedisponeringsguide**.

<!-- -->

-   Angiv disponeringsindstillinger for en dimensionsgruppe. Klik på **administration af produktoplysninger &gt;fælles &gt;frigivne produkter**. På den ** udgivet produktoplysninger ** side på den **generelle** under fanen den **Administration** skal du klikke på den **lagringsdimensionsgruppe** link. Vælg **Lagringsdimensionsgruppe** i feltet **Disponer pr. dimension** for at oprette dispositionsindstillinger for en dimension i lagringsdimensionsgruppen. Alle produktdimensioner, konfiguration, farve, størrelse, typografi, skal have den **Disponer pr. dimension** er markeret.



<a name="see-also"></a>Se også
--------

[Master plans](master-plans.md)


