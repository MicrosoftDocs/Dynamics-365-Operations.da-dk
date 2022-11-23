---
title: Konfigurere en B2C-lejer i Commerce
description: Denne artikel beskriver, hvordan du konfigurerer dine Azure Active Directory (Azure AD) B2C-lejere (Business-to-Consumer) til godkendelse af brugerwebsteder i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 3421dd3d67198a99ac236a56cbb4f300cb591a03
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785121"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>Konfigurere en B2C-lejer i Commerce

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du konfigurerer dine Azure Active Directory (Azure AD) B2C-lejere (Business-to-Consumer) til godkendelse af brugerwebsteder i Dynamics 365 Commerce.

Dynamics 365 Commerce bruger Azure AD B2C til at understøtte brugerlegitimationsoplysninger og -godkendelsesstrømme. En bruger kan tilmelde dig, logge på og nulstille deres adgangskode via disse strømme. Azure AD B2C gemmer følsomme brugergodkendelsesoplysninger, f.eks. brugernavn og adgangskode. Brugerposten i B2C-lejeren vil gemme en B2C lokal kontopost eller en B2C social identitetsudbyderpost. Disse B2C-poster vil oprette et link tilbage til kundeposten i Commerce-miljøet.

> [!WARNING] 
> Azure AD B2C gør gamle (ældre) brugerflow forældet inden 1. august 2021. Derfor skal du planlægge at overføre dine brugerflow til den nye anbefalede version. Den nye version indeholder funktionsparitet og nye funktioner. Modulbiblioteket til Commerce version 10.0.15 eller derover skal bruges sammen med de anbefalede B2C-brugerflow. Du kan finde flere oplysninger i [Brugerflow i Azure Active Directory B2C](/azure/active-directory-b2c/user-flow-overview).
 
 > [!NOTE]
 > Commerce-evalueringsmiljøer har en forudindlæst Azure AD B2C-lejer til demonstrationsformål. Det er ikke nødvendigt at indlæse din egen Azure AD B2C-lejer ved hjælp af trinnene nedenfor til evalueringsmiljøer.

> [!TIP]
> Du kan yderligere beskytte dine webstedsbrugere og øge sikkerheden for dine Azure AD B2C-lejere med Azure AD-identitetsbeskyttelse og betinget adgang. Hvis du vil have vist de egenskaber, der er tilgængelige for Azure AD B2C Premium P1- og Premium P2-lejere, kan du se [Identitetsbeskyttelse og betinget adgang for Azure AD B2C](/azure/active-directory-b2c/conditional-access-identity-protection-overview).

## <a name="dynamics-environment-prerequisites"></a>Forudsætninger for Dynamics-miljø

Før du går i gang, skal du sikre dig, at dit Dynamics 365 Commerce-miljø og din e-handelskanal er konfigureret korrekt under følgende forudsætninger.

- Angiv værdien for POS-handlinger **AllowAnonymousAccess** til "1" i Commerce headquarters:
    1. Gå til **POS-handlinger**.
    1. Højreklik i handlingsgitteret, og klik på **Personaliser**.
    1. Vælg **Tilføj et felt**.
    1. Vælg kolonnen **AllowAnonymousAccess** på listen over tilgængelige kolonner for at tilføje den.
    1. Vælg **Opdater**.
    1. For handlingen **612** "Customer add" skal du ændre **AllowAnonymousAccess** til "1."
    1. Kør jobbet **1090 (kasseapparater)**.
- Angiv den manuelle nummerserie for debitorkontoattributten **Manuel** til **Nej** i Commerce headquarters:
    1. Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Debitorparametre**.
    1. Vælge **nummerserier**.
    1. Dobbeltklik på værdien for **nummerseriekoden** i rækken med **debitorkontoen**.
    1. Angiv **Manuel** til **Nej** i oversigtspanelet **Generelt for nummerserien**.

Når du har implementeret Dynamics 365 Commerce-miljøet, anbefales det også [at initialisere basisdata](enable-configure-retail-functionality.md) i miljøet.

## <a name="next-steps"></a>Næste trin

Hvis du vil fortsætte med at oprette en B2C-lejer i Commerce, skal du fortsætte til [Opret eller link til en eksisterende Azure AD B2C-lejer på Azure-portalen](create-link-aad-b2c-tenant.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oprette eller sammenkæde med en eksisterende Azure AD B2C-lejer i Azure-portalen](create-link-aad-b2c-tenant.md)

[Opret B2C-programmet](create-b2c-app.md)

[Oprette politikker for brugerstrøm](create-user-flow-policies.md)

[Tilføj sociale identitetsudbydere (valgfrit)](add-social-identity-providers.md)

[Opdater Commerce Headquarters med de nye Azure AD B2C-oplysninger](update-hq-aad-b2c-info.md)

[Konfigurere din B2C-lejer i Commerce-webstedsgeneratoren](config-b2c-tenant-site-builder.md)

[Flere B2C-oplysninger](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
