---
title: Konfigurere et produkt, så det kan købes gratis
description: Denne artikel beskriver, hvordan du kan konfigurere et produkt, så det kan købes gratis i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bd7e4f7a7873e471f1aee94f15e7932e8d9eecd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890349"
---
# <a name="configure-a-product-to-be-purchased-for-free"></a>Konfigurere et produkt, så det kan købes gratis

[!include [banner](includes/banner.md)]


Denne artikel beskriver, hvordan du kan konfigurere et produkt, så det kan købes gratis i Microsoft Dynamics 365 Commerce.

## <a name="configure-the-product"></a>Konfigurere produktet

Hvis du vil sælge et produkt i Dynamics 365 Commerce gratis, skal du angive prisen til 0 (nul). Derudover skal du konfigurere produktindstillingen **Nulpris gyldig**.

Hvis du vil konfigurere indstillingen **Nulpris gyldig** i Commerce Headquarters, skal du følge disse trin.

1. Gå til **Retail og Commerce \> Produkter og kategorier \> Frigivne produkter efter kategori**.
1. Gå til det produkt, du vil sælge gratis. 
1. I afsnittet **Commerce** på produktsiden skal du angive indstillingen **Nulpris gyldig** til **Ja**.

I følgende illustration vises et eksempel på et produkt, hvor indstillingen **Nulpris gyldig** er angivet til **Ja**.

![Eksempel på et produkt, hvor indstillingen Nulpris gyldig er angivet til Ja.](./media/Zero-price.png)

## <a name="configure-the-online-stores-functionality-profile"></a>Konfigurere onlinebutikkens funktionalitetsprofil

Før gratis transaktioner kan behandles, skal du konfigurere indstillingen **Tillad udtjekning uden betaling ved kassen** i funktionalitetsprofilen for din onlinebutik, så transaktioner uden betalinger er tilladt. Du kan finde oplysninger om oprettelse af funktionalitetsprofiler under [Oprette en onlinefunktionsprofil](online-functionality-profile.md).

Hvis du vil konfigurere indstillingen **Tillad udtjekning uden betaling ved kassen** i Commerce Headquarters, skal du følge disse trin.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Konfiguration af onlinebutik**.
1. På siden med butikkens funktionalitetsprofil skal du angive indstillingen **Tillad udtjekning uden betaling ved kassen** til **Ja** under **Kasse**.

I følgende illustration vises et eksempel på en onlinebutiksprofil, hvor indstillingen **Tillad udtjekning uden betaling ved kassen** er angivet til **Ja**.

![Eksempel på en onlinebutiksprofil, hvor indstillingen Tillad udtjekning uden betaling ved kassen er angivet til Ja.](./media/Zero-price-profile.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Styring af detailsalgspriser](price-management.md)

[Oprette en onlinefunktionalitetsprofil](online-functionality-profile.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
