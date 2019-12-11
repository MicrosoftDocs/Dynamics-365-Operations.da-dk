---
title: Tilvælge brug af vurderinger og anmeldelser
description: I dette emne beskrives, hvordan du kan tilvælge at bruge vurderinger og anmeldelser på dit Microsoft Dynamics 365 Commerce-websted.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697974"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Tilvælge brug af vurderinger og anmeldelser

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du kan tilvælge at bruge vurderinger og anmeldelser på dit Microsoft Dynamics 365 Commerce-websted.

## <a name="overview"></a>Oversigt

Vurderings- og anmeldelsesløsningen er en omnikanalløsning, du kan stille til rådighed i Dynamics 365 Commerce ved hjælp af Microsoft Dynamics Lifecycle Services (LCS). LCS er en administrationsportal, som detailhandlere kan bruger til at styre deres miljøer fra klargøring til nedlukning.

Hvis du vil bruge vurderings- og anmeldelsesløsningerne på Commerce-webstedet, skal du først tilvælge det.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Tilvælge brug af vurderinger og anmeldelser

Du kan tilvælge at bruge vurderinger og anmeldelser på dit websted ved at følge disse trin.

1. Følg trinnene i [Implementere et nyt websted for e-handel](deploy-ecommerce-site.md).
1. Mens du stadig er i LCS, skal du gå til **Konfiguration af Retail-installation \> Andre indstillinger**.
1. Vælg **Ja** i indstillingen **Aktivér vurderinger og anmeldelser**.
1. I den **AAD-sikkerhedsgruppen for redaktør af vurderinger og anmeldelser (sikkerhedsgruppens objekt-id)** skal du angive id'et for den Microsoft Azure Active Directory-sikkerhedsgruppe (Azure AD), der omfatter vurderings- og anmeldelsesredaktørerne.

    ![Tilvælge brug af vurderinger og anmeldelser](media/LCS_RnR_Preference.png)

1. Fuldfør processen til e-handelsinitialisering.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over vurderinger og anmeldelser](ratings-reviews-overview.md)

[Administrere vurderinger og anmeldelser](manage-reviews.md)

[Konfigurere vurderinger og anmeldelser](configure-ratings-reviews.md)

[Synkronisere produktvurderinger i Dynamics 365 Retail](sync-product-ratings.md)
