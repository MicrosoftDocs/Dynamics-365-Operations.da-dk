---
title: Begrænse adgangen til en butikspromenade under test eller udvikling
description: Denne artikel indeholder en forklaring på, hvordan du kan begrænse adgangen til en Microsoft Dynamics 365 Commerce-butikspromenade, mens der udføres intern test eller udvikling.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: e382f01f82b368ad89f7abf122bf806dca4f0340
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292021"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a>Begrænse adgangen til en butikspromenade under test eller udvikling

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder en forklaring på, hvordan du kan begrænse adgangen til en Microsoft Dynamics 365 Commerce-butikspromenade, mens der udføres intern test eller udvikling.

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
