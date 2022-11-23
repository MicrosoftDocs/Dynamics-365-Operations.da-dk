---
title: Opret en B2C-ansøgning
description: Denne artikel beskriver, hvordan du opretter en B2C-ansøgning (business-to-consumer) på Microsoft Azure-portalen.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: d8956d51bac7bf2a162a370ae5ef1c7e7cdc1e2f
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785244"
---
# <a name="create-a-b2c-application"></a>Opret en B2C-ansøgning

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du opretter en B2C-ansøgning (business-to-consumer) på Microsoft Azure-portalen.

Når din B2C-lejeren er blevet oprettet, skal du oprette et B2C-program din nye Azure Active Directory (Azure AD)-lejer for at kunne kommunikere med Commerce.

Hvis du vil oprette B2C-programmet, skal du følge disse trin.

1. I Azure-portalen skal du vælge **App-registreringer** og derefter vælge **Ny registrering**.
1. Under **Navn** skal du angive navnet for dette Azure AD B2C-program.
1. Under **Understøttede kontotyper** skal du vælge **Konti i enhver id-udbyder eller organisationsmappe (for godkendelse af brugere med brugerflow)**.
1. For **Omdirigerings-URI** skal du angive dine dedikerede URL-adresser som **Web**-type. Se [Svar-URL-adresser](#reply-urls) nedenfor for at få oplysninger om svar-URL-adresser, og hvordan du formaterer dem. Der skal angives en URL-adresse for omdirigeret URI/svar for at aktivere omdirigering fra Azure AD B2C tilbage til dit websted, når en bruger godkendes. URL-adressen til svaret kan tilføjes under registreringsprocessen, eller den kan tilføjes senere ved at vælge linket **Tilføj et link til en omdirigeret URI** fra menuen **Oversigt** i afsnittet **Oversigt** i B2C-programmet.
1. For **Tilladelser** skal du vælge **Giv administratortilladelser til OpenID og offline_access**.
1. Vælg **Registrer**.
1. Vælg det program, der lige er oprettet, og gå til menuen **Godkendelse**. 
1. Hvis der angives en URL-adresse for svaret, skal du vælge både indstillingen **Adgangstokens** og **Id-tokens** under **Implicit tilladelse og hybridflow** for at aktivere dem til programmet, og vælg derefter **Gem**. Hvis en URL-adresse til svaret ikke er angivet under registreringen, kan den også tilføjes på denne side ved at vælge **Tilføj en platform**, vælge **Web** og derefter angive omdirigerings-URI for programmet. Afsnittet **Implicit tilladelse og hybridflow** vil derefter være tilgængeligt, så der kan vælges både indstillingen **Adgangstokens** og **Id-tokens**.
1. Gå til menuen **Oversigt** på Azure-portalen, og kopiér **Program-id (klient)**. Notér dig dette id til senere opsætningstrin (der senere refereres til som **Klient-GUID**).

Du kan finde yderligere oplysninger om appregistreringer i Azure AD B2C i [Den nye erfaring med appregistreringer for Azure Active Directory B2C](/azure/active-directory-b2c/app-registrations-training-guide)

### <a name="reply-urls"></a>Svar-URL-adresser

Svar-URL-adresser er vigtige, da de giver en liste over returdomænerne, når dit websted kalder Azure AD B2C for at godkende en bruger. Det gør det muligt at returnere den godkendte bruger tilbage til det domæne, hvor de logger på (domænet for dit websted). 

I feltet **Svar-URL-adresse** på skærmen **Azure AD B2C-programmer \> Nyt program** skal du tilføje separate linjer til både dit websteds domæne og (når miljøet er klargjort) til den Commerce-genererede URL-adresse. Disse URL-adresser skal altid bruge et gyldigt URL-adresseformat og må kun være grundlæggende URL-adresser (ingen efterfølgende skråstreger eller stier). Strengen ``/_msdyn365/authresp`` skal derefter føjes til de grundlæggende URL-adresser som i følgende eksempler.

- ``https://www.fabrikam.com/_msdyn365/authresp`` (Domænet skal svare helt til e-handelsdomænet. Hvis du har flere domæner, skal du tilføje denne URL-adresse for hvert domæne.)
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="next-steps"></a>Næste trin

Hvis du vil fortsætte med at konfigurere en B2C-lejer i Commerce, skal du fortsætte til [Opret brugerflowpolitikker](create-user-flow-policies.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere en B2C-lejer i Commerce](set-up-b2c-tenant.md)

[Oprette eller sammenkæde med en eksisterende Azure AD B2C-lejer i Azure-portalen](create-link-aad-b2c-tenant.md)

[Oprette politikker for brugerstrøm](create-user-flow-policies.md)

[Tilføj sociale identitetsudbydere (valgfrit)](add-social-identity-providers.md)

[Opdater Commerce Headquarters med de nye Azure AD B2C-oplysninger](update-hq-aad-b2c-info.md)

[Konfigurere din B2C-lejer i Commerce-webstedsgeneratoren](config-b2c-tenant-site-builder.md)

[Flere B2C-oplysninger](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
