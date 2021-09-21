---
title: Tilvælge brug af vurderinger og anmeldelser
description: I dette emne beskrives, hvordan du kan tilvælge at bruge vurderinger og anmeldelser på dit Microsoft Dynamics 365 Commerce-websted.
author: gvrmohanreddy
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9fe8e9403ccbdc1e26620ae33c6a3866af06b23c
ms.sourcegitcommit: 81bc42551e6c9af6ad38908afb606ee1f8d3c44b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473423"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Tilvælge brug af vurderinger og anmeldelser

[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du kan tilvælge at bruge vurderinger og anmeldelser på dit Microsoft Dynamics 365 Commerce-websted.

Vurderings- og anmeldelsesløsningen er en omnikanalløsning, du kan stille til rådighed i Dynamics 365 Commerce ved hjælp af Microsoft Dynamics Lifecycle Services (LCS). LCS er en administrationsportal, som detailhandlere kan bruger til at styre deres miljøer fra klargøring til nedlukning.

Hvis du vil bruge vurderings- og anmeldelsesløsningen på Commerce-webstedet, skal du tilmelde dig vurderinger og anmeldelser under installationen af dit e-handels-websted på Dynamics 365 Commerce.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Tilvælge brug af vurderinger og anmeldelser

Du kan tilvælge at bruge vurderinger og anmeldelser på dit websted ved at følge disse trin.

1. Følg trinnene i [Implementere et nyt websted for e-handel](deploy-ecommerce-site.md).
1. Mens du stadig er i LCS, skal du gå til **Konfiguration af Retail-installation \> Andre indstillinger**.
1. Vælg **Ja** i indstillingen **Aktivér vurderinger og anmeldelser**.
1. I den **AAD-sikkerhedsgruppen for redaktør af vurderinger og anmeldelser (sikkerhedsgruppens objekt-id)** skal du angive id'et for den Microsoft Azure Active Directory-sikkerhedsgruppe (Azure AD), der omfatter vurderings- og anmeldelsesredaktørerne.

    ![Tilvælge brug af vurderinger og anmeldelser.](media/LCS_RnR_Preference.png)

1. Fuldfør processen til e-handelsinitialisering.

> [!NOTE] 
> Hvis du er eksisterende Dynamics 365 Commerce-kunde, der allerede har implementeret et e-handels-websted uden at have tilmeldt dig vurderinger og anmeldelser og nu vil bruge vurderinger og anmeldelser fra Dynamics 365 Commerce-pakken, skal du sende en serviceanmodning. Oplysninger om, hvordan du sender en serviceanmodning, finder du under [Proces for afsendelse af serviceanmodninger](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over vurderinger og anmeldelser](ratings-reviews-overview.md)

[Administrere vurderinger og anmeldelser](manage-reviews.md)

[Konfigurere vurderinger og anmeldelser](configure-ratings-reviews.md)

[Synkronisere produktvurderinger i Dynamics 365 Commerce](sync-product-ratings.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
