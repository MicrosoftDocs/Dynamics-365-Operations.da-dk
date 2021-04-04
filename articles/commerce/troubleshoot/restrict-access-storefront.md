---
title: Begrænse adgangen til en butikspromenade under test eller udvikling
description: Dette emne indeholder en forklaring på, hvordan du kan begrænse adgangen til en Microsoft Dynamics 365 Commerce-butikspromenade, mens der udføres intern test eller udvikling.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2cdf131048e0fac940475322294ed99e76c0a53b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585253"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a>Begrænse adgangen til en butikspromenade under test eller udvikling

[!include [banner](../../includes/banner.md)]

Dette emne indeholder en forklaring på, hvordan du kan begrænse adgangen til en Microsoft Dynamics 365 Commerce-butikspromenade, mens der udføres intern test eller udvikling.

## <a name="description"></a>Betegnelse

Under interne test eller aktive udvikling kan du begrænse adgangen til dit websted for at forhindre, at eksterne brugere åbner de publicerede butikspromenadesider.

## <a name="resolution"></a>Løsning

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a>Oprette Azure AD B2C ved hjælp af standardbrugerflow

Du kan finde flere oplysninger om, hvordan du konfigurerer Azure Active Directory B2C (Azure AD B2C) til dit e-handelswebsted, i [Oprette en B2C-lejer i Commerce](../set-up-b2c-tenant.md).

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a>Begrænse brugeradgang til butikspromenadesider og blokere oprettelsen af nye brugere

Hvis du vil begrænse brugeradgang til butikspromenadesider i Commerce Site Builder, skal du følge disse trin.

1. Gå til dit websted.
1. Vælg **Sider**, og vælg derefter den side, der skal begrænses brugeradgang for.
1. Vælg modulet eller fragmentplads, og vælg derefter **Rediger**.
1. Vælg **Kræver logon?** i egenskabsruden, og vælg derefter **Udfør redigering**.
1. Vælg **Publicer**.

Hvis du vil spærre for oprettelse af nye brugere i Azure AD, skal du benytte følgende fremgangsmåde.

1. Gå til [Azure-portalen](https://portal.azure.com/).
1. Vælg det Azure AD B2C-program, du har oprettet til adgangen til dit websted.
1. Vælg **Brugerflows** i navigationsruden til venstre.
1. Vælg **Brugerflows** øverst på siden og vælg **Nyt brugerflow**.
1. Vælg **Forhåndsvisning** på siden **Vælg en brugerflowtype**.
1. Midt på siden skal du vælge **log på v2**. Følg derefter trinnene i [Opsætning af en B2C-lejer i Commerce](../set-up-b2c-tenant.md) for at konfigurere flowet som webstedets standardbrugerflow for Azure AD B2C under test eller udvikling.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere en B2C-lejer i Commerce](../set-up-b2c-tenant.md)

[Konfigurere brugerdefinerede sider til brugerlogon](../custom-pages-user-logins.md)
