---
title: Angive produktantalsgrænser for B2B-e-handelswebsteder
description: Denne artikel beskriver, hvordan du angiver produktantalsgrænser for business-to-business (B2B)-e-handelswebsteder.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: RetailOperations
ms.openlocfilehash: 76a7ad2c3095d1402ff214dbfee26b344b492681
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275671"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a>Angive produktantalsgrænser for B2B-e-handelswebsteder

[!include [banner](../../includes/banner.md)]

Denne artikel beskriver, hvordan du angiver produktantalsgrænser for business-to-business (B2B)-e-handelswebsteder.

De fleste produkter har en måleenhed, der definerer gruppering af dem. Grupperingerne har indflydelse på, hvordan produkterne kan sælges. Nogle produkter kan have en yderligere gruppering for antal. Denne gruppe bestemmer, om produkterne kan sælges som individuelle enheder eller multiplum, og om der er en minimums- eller maksimumordreantalsgrænse, der skal overholdes.

Denne funktion til begrænsning af antal sikrer, at de minimum-, maksimum-, multiplum- og standardmængder, der er konfigureret i Microsoft Dynamics 365 Commerce (i standardordreindstillingerne eller indstillingerne for commerce site builder), anvendes på kundeordrer, der placeres på et e-handelswebsted. Produktantalsgrænser understøttes ikke i øjeblikket for POS og call centers.

Mange detailhandlere giver mulighed for kundeordrer (også kendt som specialordrer) for at opfylde forskellige produkt- og opfyldelseskrav. Her er nogle typiske scenarier:

- En kunde ønsker, at produkter af bestemte varianter skal sælges i multiplum af nogle få.
- En kunde ønsker at afhente varer fra en butik eller et sted, der er forskelligt fra butikken eller det sted, hvor kunden købte varerne. Pakkestandarderne for butikkerne er dog ikke de samme som standarderne for onlinesalgsdistribution.
- En kunde ønsker at købe et limited-edition-produkt med en maksimumantalsgrænse for varer, der kan købes.

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a>Aktivere standardfunktionen for ordreindstillinger i Commerce Headquarters

Inden du kan angive grænser for produktantal, skal funktionen standardordreindstillinger være aktiveret i Commerce Headquarters.

Følg disse trin for at aktivere standardfunktionen for indstilling af ordrer.

1. Gå til **Systemadministration \> Arbejdsområder \> Funktionsstyring**.
1. Find og vælg funktionen **Supportindstillinger for websted- og standardordrer i kundeordre**.
1. Vælg **Aktivér nu** nederst til højre i ruden. 

## <a name="define-quantity-settings"></a>Definere mængdeindstillinger 

Du kan definere mængdeindstillinger på siden **Standardindstillinger for ordre**.

Følg disse trin for at definere mængdeindstillinger. 

1. Gå til Produkt **Retail og Commerce \> Produkter og kategorier \> Frigivne produkter efter kategori**.
1. Vælge et frigivet produkt.
1. På fanen **Administrer lager** i handlingsruden i gruppen **Ordreindstillinger** skal du vælge **Standardordreindstillinger**. 
1. Angiv produktsalgsantallet i sektionen **Salgsmængde** på siden **Standardordreindstillinger** i oversigtspanelet **Salgsordre**:

    - **Flere** – Det antal, som produktet kan købes i multiplum af.
    - **Minimumordreantal** – Det mindste antal produkter, der skal købes.
    - **Maksimumordreantal** – Det maksimale antal produkter, der kan købes.
    - **Standardordreantal** – Det standardantal, der automatisk angives, når produktet vælges.

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a>Aktivator funktionen for B2B-ordreantalsgrænser i Commerce site builder

Følg disse trin for at aktivere funktionen for B2B-ordreantalsgrænser i Commerce site builder.

1. Gå til **Webstedsindstillinger \> Udvidelser**.
1. Vælg **Aktiveret for B2B-kunder** i rullemenuen under **Aktivér antalsgrænser for ordre**. 

> [!NOTE] 
> Opdaterede indstillinger for webstedet træder først i kraft, når app.settings.json-filen er opdateret. Yderligere oplysninger finder du i [SDK- og modulbiblioteksopdateringer](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oprette et B2B-e-handelswebsted](set-up-b2b-site.md)

[Administrere B2B-forretningspartnere ved hjælp af kundehierarkier](partners-customer-hierarchies.md)

[Administrere forretningspartnerbrugere på B2B-e-handelswebsteder](manage-b2b-users.md)

[Konfigurere betalingsmåden for debitorkonti for B2B-e-handelswebsteder](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
