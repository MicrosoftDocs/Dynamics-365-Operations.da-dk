---
title: Flere B2C-oplysninger
description: Denne artikel indeholder yderligere oplysninger om, hvordan du angiver B2C-lejeren i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/14/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: b60ef15544cd30c44968ee7a588a8a9fb08e8223
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785221"
---
# <a name="additional-b2c-information"></a>Flere B2C-oplysninger

[!include [banner](includes/banner.md)]

Denne artikel indeholder yderligere oplysninger om, hvordan du angiver B2C-lejeren i Microsoft Dynamics 365 Commerce.

### <a name="customer-migration"></a>Kundeoverflytning

Hvis du overvejer at overflytte kundeposter fra en tidligere identitetsudbyderplatform, skal du arbejde med Dynamics 365 Commerce-teamet for at gennemgå dine behov for kundeoverflytning.

Du kan få yderligere Azure AD B2C-dokumentation om kundeoverflytning under [Overflytte brugere til Azure Active Directory B2C](/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Brugerdefinerede politikker

Du kan få yderligere oplysninger om tilpasning af Azure AD B2C-interaktioner og politikstrømme, der ligger ud over, hvad der tilbydes af B2C standardpolitikker, i [Tilpassede politikker i Azure Active Directory B2C](/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Sekundær administrator

Du kan tilføje en valgfri, sekundær administratorkonto under afsnittet **Bruger** i din B2C-lejer. Det kan være en direkte konto eller en generel konto. Hvis du skal dele en konto på tværs af teamressourcer, kan du også oprette en fælles konto. På grund af følsomheden for de data der er lagret i Azure AD B2C, skal en fælles konto overvåges nøje i følge firmaets sikkerhedspraksis.

### <a name="set-up-a-custom-sign-in-domain"></a>Oprette et brugerdefineret domæne til logon

I Azure AD B2C kan du konfigurere et tilpasset domæne for logon til Azure AD B2C-lejeren. Du kan finde instruktioner i [Aktiver brugerdefinerede domæner for Azure Active Directory B2C](/azure/active-directory-b2c/custom-domain). 

Hvis du bruger et brugerdefineret domæne til logon, skal domænet angives i Commerce-webstedsgeneratoren.

Hvis du angive et brugerdefineret domæne til logon i webstedgeneratoren, skal du følge disse trin.

1. Vælg webstedsskifteren øverst til højre i webstedsgeneratoren, og vælg derefter **Administrer websteder**.
1. Vælg **Lejerindstillinger \> Konfiguration af webstedets godkendelse** i venstre navigationsrude.
1. Vælg **Administrer** i sektionen **Godkendelsesprofiler for websted**.
1. I genvejsmenuen til højre skal du vælge knappen **Rediger** (blyantssymbol) ud for den webstedsgodkendelsesprofil, du vil angive et brugerdefineret domæne for.
1. I dialogboksen **Rediger godkendelsesprofil for websted** skal du under **Log på brugerdefineret domæne** angive dit brugerdefinerede logondomæne (f.eks. 'login.fabrikam.com').

> [!WARNING]
> Når du opdaterer til et brugerdefineret domæne for Azure AD B2C-lejeren, påvirker ændringen lejerens udstederoplysninger for det genererede token. Udstederoplysninger inkluderer derefter det brugerdefinerede domæne i stedet for det standarddomæne, der leveres af Azure AD B2C. En anden konfiguration af **Udsteder** i Commerce headquarters (**Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Commerce-delte parametre \> Identitetsudbydere**) ændrer systemets interaktion med webstedsbrugere og kan muligvis oprette en ny kundepost, hvis en bruger godkender hos den nye udsteder. Eventuelle ændringer af brugerdefinerede domæne skal testes grundigt, før der skiftes til det brugerdefinerede domæne i et aktivt Azure AD B2C-miljø.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere en B2C-lejer i Commerce](set-up-b2c-tenant.md)

[Oprette eller sammenkæde med en eksisterende Azure AD B2C-lejer i Azure-portalen](create-link-aad-b2c-tenant.md)

[Opret B2C-programmet](create-b2c-app.md)

[Oprette politikker for brugerstrøm](create-user-flow-policies.md)

[Tilføj sociale identitetsudbydere (valgfrit)](add-social-identity-providers.md)

[Opdater Commerce Headquarters med de nye Azure AD B2C-oplysninger](update-hq-aad-b2c-info.md)

[Konfigurere din B2C-lejer i Commerce-webstedsgeneratoren](config-b2c-tenant-site-builder.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
