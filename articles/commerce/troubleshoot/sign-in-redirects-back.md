---
title: Log på link igen til et e-handelswebsted
description: Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når et link, der logges på, omdirigeres tilbage til e-handelswebstedet i stedet for at gå til siden, hvor det logges på.
author: Reza-Assadi
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
ms.openlocfilehash: ee2ac8636dad8d31719971b2cc17c8b923f07959
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801453"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a>Log på link igen til et e-handelswebsted

[!include [banner](../../includes/banner.md)]

Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når et link, der logges på, omdirigeres tilbage til e-handelswebstedet i stedet for at gå til siden, hvor det logges på.

## <a name="description"></a>Betegnelse

Når du har konfigureret en ny Microsoft Azure Active Directory B2C-lejer (Azure AD-B2C) i Commerce-webstedsgenerator, bliver de brugere, der vælger **Log på**-linket, omdirigeret tilbage til den primære e-commerce-landingsside uden at gå til logonsiden.

## <a name="resolution"></a>Løsning

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a>Bekræft, at svar-URL-adressen er konfigureret korrekt i Azure AD B2C-programmet

Bekræft, at svarets URS-adresse er konfigureret korrekt i Azure AD B2C-programmet ved at følge disse trin.

1. Gå til [Azure-portalen](https://portal.azure.com/).
1. Vælg det Azure AD B2C-program, du har oprettet til adgangen til dit websted.
1. Vælg det program, du oprettede i Azure AD B2C-opsætningen.
1. Under **Svar URL-adresse** skal du sørge for, at listen indeholder poster for både URL-adressen for webstedets domæne og den URL-adresse, der genereres af e-handel, som vist i eksemplet i følgende illustration.

    ![Azure AD B2C Svar til URL-adresseindgange](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> Både URL-adressen til webstedet og den url-adresse, der genereres ved e-handel, skal være i et gyldigt URL-format, der ikke inkluderer foranstillede eller efterfølgende skråstreger.

## <a name="additional-resources"></a>Yderligere ressourcer

[Registrer en webstedsansøgning i Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[Konfigurere en B2C-lejer i Commerce](../set-up-b2c-tenant.md)
