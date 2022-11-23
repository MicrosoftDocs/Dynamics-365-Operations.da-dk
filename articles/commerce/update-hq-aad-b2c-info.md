---
title: Opdater Commerce Headquarters med de nye Azure AD B2C-oplysninger
description: Denne artikel beskriver, hvordan Microsoft Dynamics 365 Commerce headquarters opdateres med nye Azure Active Directory (Azure AD) B2C-oplysninger (business-to-consumer).
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: c65949ff97182d2692319ac2af00e3ef35a79580
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785264"
---
# <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Opdater Commerce Headquarters med de nye Azure AD B2C-oplysninger

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan Microsoft Dynamics 365 Commerce headquarters opdateres med nye Azure Active Directory (Azure AD) B2C-oplysninger (business-to-consumer).

Når du har udført overstående trin til Azure AD B2C-klargøring, skal Azure AD B2C-programmet registreres i dit Dynamics 365 Commerce-miljø.

Udfør følgende trin for at opdatere Headquarters med de nye Azure AD B2C-oplysninger.

1. Gå til **Delte Commerce-parametre** i Commerce, og vælg **Identitetsudbydere** i menuen til venstre.
1. Gør følgende under **Identitetsudbydere**:
    1. Angiv udstederstrengen til identitetsudbyderen i feltet **Udsteder**. Nedenfor kan du finde din udstederstreng i afsnittet [Anskaffe udstederstreng til hovedkontorets opsætning](#obtain-issuer-string-for-headquarters-setup).
    1. Skriv et navn på din udbyderpost i feltet **Navn**.
    1. Skriv **Azure AD B2C (id_token)** i feltet **Type**.
1. Gør følgende under **Betroede parter** med ovenstående B2C-identitetsudbyderelement valgt:
    1. I feltet **ClientID** skal du angive dit B2C-program-id, som du kan finde i feltet **Program-id** på B2C-ansøgningens egenskabsside.
    1. Skriv **Offentlig** i feltet **Type**.
    1. Skriv **Kunde** i feltet **Brugertype**.
1. Gå til handlingsruden, og vælg **Gem**.
1. Søg efter **Distributionsplan** i feltet Commerce-søgning
1. Vælg job **1110 global konfiguration** i den venstre navigationsmenu på siden **Distributionsplaner**.
1. Vælg **Kør nu** i handlingsruden.

### <a name="obtain-issuer-string-for-headquarters-setup"></a>Anskaffe udstederstreng til hovedkontorets opsætning

Følg disse trin for at få strengen til identitetsudbyderens udsteder.

1. På Azure AD B2C-siden på Azure-portalen skal du navigere til dit brugerflow **Tilmelding og logon**.
1. Vælg **Sidelayout** i navigationsmenuen til venstre, og under **Layoutnavn** skal du vælge **Samlet tilmeldings- eller logonside** og derefter vælge **Kør brugerflow**.
1. Kontrollér, at programmet er indstillet til det ønskede Azure AD B2C-program, der er oprettet ovenfor, og vælg derefter brugerflowlinket under overskriften **Kør brugerflow**, der indeholder ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``. (Vælg ikke **Kør brugerflow**). Der åbnes en ny fane med metadata for politikken for indsamling af udstederstrengen.
1. Kopiér udstederstrengen for identitetsudbyderen på den metadataside, der vises i din browser (værdien for **udsteder**, der starter med "https://" og slutter med "/v2.0/"), der ligner følgende eksempel.
   - ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.
 
**ELLER**: Hvis du vil oprette den samme URL-adresse til metadata manuelt, skal du udføre følgende trin.

1. Opret en URL-metadataadresse i følgende format med din B2C-lejer og -politik: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Eksempel: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Angiv URL-metadataadressen i en browsers adresselinje.
1. Kopier URL-adressen til identitetsudbyderens udsteder (værdien for **"udsteder"**) i metadataene.
    - Eksempel: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="next-steps"></a>Næste trin

Hvis du vil fortsætte med at oprette en B2C-lejer i Commerce, [skal du fortsætte med at konfigurere B2C-lejeren i Commerce site builder](config-b2c-tenant-site-builder.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere en B2C-lejer i Commerce](set-up-b2c-tenant.md)

[Oprette eller sammenkæde med en eksisterende Azure AD B2C-lejer i Azure-portalen](create-link-aad-b2c-tenant.md)

[Opret B2C-programmet](create-b2c-app.md)

[Oprette politikker for brugerstrøm](create-user-flow-policies.md)

[Tilføj sociale identitetsudbydere (valgfrit)](add-social-identity-providers.md)

[Konfigurere din B2C-lejer i Commerce-webstedsgeneratoren](config-b2c-tenant-site-builder.md)

[Flere B2C-oplysninger](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
