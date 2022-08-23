---
title: Vælge sidelayout
description: Denne artikel forklarer, hvordan du kan oprette og vælge sidelayout i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: c01be029a79efe8c3fac6203db51dd1a5a8516e3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282071"
---
# <a name="select-page-layouts"></a>Vælge sidelayout


[!include [banner](includes/banner.md)]

Denne artikel forklarer, hvordan du kan oprette og vælge sidelayout i Microsoft Dynamics 365 Commerce.

## <a name="create-layouts-for-an-existing-page"></a>Oprette layout for en eksisterende side

> [!NOTE]
> Du kan kun oprette layout for en eksisterende side, hvis siden har mindst to moduler under hovedelementet.

Benyt følgende fremgangsmåde for at oprette layout til en eksisterende side.

1. Gå til **Sider**, og find den eksisterende side på listen. Brug søgefunktionen efter behov.
1. Vælg siden, vælg **Rediger** for at tjekke den ud, og vælg derefter sidenavnet for at åbne den. Notér dig modulrækkefølgen.
1. Vælg **Gem som nyt layout**.
1. Angiv et navn til layoutet, og vælg derefter **OK**.
1. Vælg **Konverter til integreret layout**.
1. Rediger rækkefølgen af modulerne efter behov, og notér dig den nye rækkefølge.
1. Vælg **Gem som nyt layout**.
1. Angiv et navn til layoutet, og vælg derefter **OK**.
1. Vælg **Skift layout**, vælg det første layout, du har oprettet, og vælg derefter **OK**. Notér dig modulrækkefølgen. Ret det, så det svarer til den modulrækkefølge, der er gemt sammen med layoutet.
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den. 

## <a name="select-a-different-layout-for-an-existing-page"></a>Vælge et andet layout for en eksisterende side

> [!NOTE]
> Du kan kun vælge et andet layout til en eksisterende side, hvis den skabelon, der blev brugt til at oprette den pågældende side, har mere end ét layout.

Benyt følgende fremgangsmåde for at vælge et andet layout til en eksisterende side.

1. Gå til **Sider**, og find den eksisterende side på listen. Brug søgefunktionen efter behov.
1. Vælg siden, vælg **Rediger** for at tjekke den ud, og vælg derefter sidenavnet for at åbne den.
1. Vælg **Skift layout**.
1. Vælg det nye layout for siden, og vælg derefter **OK**. Sideeditoren opdateres til at vise det nye layout.
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Redigere en eksisterende webstedsside](modify-existing-page.md)

[Tilføje en ny webstedsside](add-new-page.md)

[Administrere SEO-metadata](manage-seo-metadata.md)

[Gemme, få vist og udgive en side](save-preview-publish-page.md)

[Forbedre en produktside](enrich-product-page.md)

[Forbedre en kategorilandingsside](enrich-category-page.md)

[Bekræfte tilgængelighed af sideindhold](verify-accessibility.md)

[Oprette dynamiske e-handelssider baseret på URL-parametre](create-dynamic-pages.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
