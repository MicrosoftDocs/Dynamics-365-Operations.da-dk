---
title: Oprette politikker for brugerstrøm
description: Denne artikel beskriver, hvordan du opretter brugerflowpolitikker på Microsoft Azure-portalen.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 91b9d99dfd8c3d100ca197aa499ca86799bbffc8
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785254"
---
# <a name="create-user-flow-policies"></a>Oprette politikker for brugerstrøm

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du opretter brugerflowpolitikker på Microsoft Azure-portalen.

Brugerstrømme er de politikker, som Azure Active Directory (Azure AD) business-to-consumer (B2C) bruger til at give sikker log ind, registrere, redigere profil og glemme brugeroplevelser med adgangskoder. Dynamics 365 Commerce bruger disse strømme til at udføre politikhandlingerne for at kommunikere med Azure AD B2C-lejeren. Når en bruger kommunikerer med disse politikker, omdirigeres de til Azure AD B2C-lejeren for at udføre handlingerne.

Azure AD B2C omfatter tre grundlæggende brugerstrømtyper:
- Tilmelde og logge på
- Profilredigering
- Adgangskoden er nulstillet

Du kan vælge at bruge de standardbrugerstrømme, der leveres af Azure AD, og som viser en side, der har Azure AD B2C som vært. Du kan også oprette en HTML-side for at styre udseendet af disse brugerstrømoplevelser. 

Hvis du vil tilpasse brugerpolitiksiderne med indbyggede sider i Dynamics 365 Commerce, skal du se [Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md). Du kan finde flere oplysninger under [Tilpasse grænsefladen af brugeroplevelser i Azure Active Directory B2C](/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Oprette en tilmeldings- og logonpolitik for brugerflow

Gør følgende for at konfigurere et brugerflow for en tilmeldings- og logonpolitik.

1. Vælg **Brugerstrømme (politikker)** i navigationsruden til venstre i Azure-portalen.
1. Vælg **Ny brugerstrøm** på siden **Azure AD B2C – Brugerstrømme (politikker)**.
1. Vælg politikken **Tilmelding og logon**, og vælg derefter versionen **Anbefalet**.
1. Angiv et politiknavn under **Navn**. Dette navn vises bagefter med et præfiks, som portalen tildeler (f.eks. "B2C_1_").
1. Under **Identitetsudbydere** skal du vælge **Mailtilmelding** i sektionen **Lokale konti**. Mailgodkendelse bruges i de mest almindelige scenarier for Commerce. Hvis du også bruger godkendelse af social identitetsudbyder, kan disse også vælges på dette tidspunkt.
1. Vælg det relevante valg for dit firma under **Godkendelse af flere oplysninger**. 
1. Vælg indstillinger til at indsamle attributter eller returnere krav efter behov under **Brugerattributter og -krav**. Vælg **Vis mere...** for at få den fulde liste over attributter og kravindstillinger. Commerce kræver følgende standardindstillinger:

    | **Indsaml attribut** | **Returkrav** |
    | ---------------------- | ----------------- |
    | E-mailadresse          | Mailadresser   |
    | Givent navn             | Givent navn        |
    |                        | Identitetsudbyder |
    | Efternavn                | Efternavn           |
    |                        | Brugerens objekt-id  |

1. Vælg **Opret**.

Følgende billede er et eksempel på brugerflowet i Azure AD B2C-tilmelding og -logon.

![Politikindstillinger for tilmelding og login.](./media/B2CImage_11.png)

   
### <a name="create-a-profile-editing-user-flow-policy"></a>Oprette en brugerstrømpolitik til profilredigering

Gør følgende for at oprette en brugerstrømpolitik til profilredigering.

1. Vælg **Brugerstrømme (politikker)** i navigationsruden til venstre i Azure-portalen.
1. Vælg **Ny brugerstrøm** på siden **Azure AD B2C – Brugerstrømme (politikker)**.
1. Vælg **Profilredigering**, og vælg derefter versionen **Anbefalet**.
1. Angiv brugerstrømmen til profilredigeringen under **Navn**. Dette navn vises bagefter med et præfiks, som portalen tildeler (f.eks. "B2C_1_").
1. Under **Identitetsudbydere** skal du vælge **Mailtilmelding** i sektionen **Lokale konti**.
1. Vælg følgende afkrydsningsfelter under **Brugerattributter**:
    
    | **Indsaml attribut** | **Returkrav** |
    | ---------------------- | ----------------- |
    |                        | Mailadresser   |
    | Givent navn             | Givent navn        |
    |                        | Identitetsudbyder |
    | Efternavn                | Efternavn           |
    |                        | Brugerens objekt-id  |
    
1. Vælg **Opret**.

I følgende billede vises et eksempel på brugerstrøm til Azure AD B2C profilredigering.

![Eksempel på brugerflow til Azure AD B2C-profilredigering](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>Opret en brugerstrømpolitik til nulstilling af adgangskode

Gør følgende for at oprette en brugerstrømpolitik til nulstilling af adgangskode.

1. Vælg **Brugerstrømme (politikker)** i navigationsruden til venstre i Azure-portalen.
1. Vælg **Ny brugerstrøm** på siden **Azure AD B2C – Brugerstrømme (politikker)**.
1. Vælg **Nulstilling af adgangskode**, og vælg derefter versionen **Anbefalet**.
1. Angiv et navn til brugerstrømmen til nulstilling af adgangskode under **Navn**.
1. Vælg **Nulstil adgangskode ved hjælp af mailadresse** under **Identitetsudbydere**.
1. Vælg **Opret**.
1. Vælg følgende afkrydsningsfelter under **Programkrav**:
    - **E-mail-adresser**
    - **Givent navn**
    - **Efternavn**
    - **Brugerens objekt-id**
1. Vælg **Opret**.

Følgende billede viser, hvor du kan indstille **Nulstil adgangskode ved hjælp af mailadresse** i en brugerstrøm til nulstilling af adgangskode i Azure AD B2C.

![Indstil "Nulstil adgangskode ved hjælp af mailadresse" i politikken Nulstil adgangskode](./media/B2CImage_13.png)

## <a name="next-steps"></a>Næste trin

Hvis du vil fortsætte med at konfigurere en B2C-lejer i Commerce, skal du fortsætte til [Tilføj sociale identitetsudbydere](add-social-identity-providers.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere en B2C-lejer i Commerce](set-up-b2c-tenant.md)

[Oprette eller sammenkæde med en eksisterende Azure AD B2C-lejer i Azure-portalen](create-link-aad-b2c-tenant.md)

[Opret B2C-programmet](create-b2c-app.md)

[Tilføj sociale identitetsudbydere (valgfrit)](add-social-identity-providers.md)

[Opdater Commerce Headquarters med de nye Azure AD B2C-oplysninger](update-hq-aad-b2c-info.md)

[Konfigurere din B2C-lejer i Commerce-webstedsgeneratoren](config-b2c-tenant-site-builder.md)

[Flere B2C-oplysninger](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
