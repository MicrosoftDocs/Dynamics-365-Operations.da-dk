---
title: Konfigurere din B2C-lejer i Commerce-webstedsgeneratoren
description: Denne artikel beskriver, hvordan du konfigurerer dine business-to-consumer (B2C)-lejer i Microsoft Dynamics 365 Commerce-webstedsgenerator.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 181edf1570f1a9d071a7fae38ff9d73ff3c068fa
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785261"
---
# <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>Konfigurere din B2C-lejer i Commerce-webstedsgeneratoren

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du konfigurerer dine business-to-consumer (B2C)-lejer i Microsoft Dynamics 365 Commerce-webstedsgenerator.

Når konfigurationen af din Azure AD B2C-lejer er fuldført, skal du konfigurere B2C-lejeren i Commerce-webstedsgeneratoren. Konfigurationstrin omfatter indsamling af oplysninger om B2C-programmet fra Azure-portalen, indtastning af B2C-programoplysninger i webstedsgeneratoren og derefter tilknytning af B2C-programmet til dit webstedsted og din kanal.

### <a name="collect-the-required-application-information"></a>Indsaml de nødvendige programoplysninger

Udfør følgende trin for at indsamle de nødvendige programoplysninger.

1. Gå til **Startside \> Azure AD B2C - Appregistreringer** i Azure-portalen.
1. Vælg dit program, og vælg derefter **Oversigt** i venstre navigationsrude for at få oplysninger om programmet.
1. I referencen **Program-id (klient)** skal du indsamle program-id'et for det B2C-program, der er oprettet i din B2C-lejer. Det vil senere blive angivet som **Klient-GUID** i webstedsgeneratoren.
1. Vælg **Omdirigerings-URI'er**, og få den URL-adresse til svaret, der vises på dit websted (svar-URL-adressen, der blev angivet under opsætningen).
1. Gå til **Startside \> Azure AD B2C – Brugerstrømme**, og få derefter de fulde navne på hver enkelt brugerstrømpolitik.

I følgende billede vises et eksempel på oversigtssiden **Azure AD B2C - Appregistreringer**.

![Azure AD B2C – Oversigtsside for appregistreringer med program-id (klient) fremhævet](./media/ClientGUID_Application_AzurePortal.png)

I følgende billede vises et eksempel på brugerstrømpolitikker på siden **Azure AD B2C – Brugerstrømme (politikker)**.

![Indsaml navnene på de enkelte B2C-politikflow.](./media/B2CImage_22.png)

### <a name="enter-your-azure-ad-b2c-tenant-application-information-into-commerce"></a>Angiv programoplysninger om din Azure AD B2C-lejer i Commerce

Du skal angive oplysninger om Azure AD B2C-lejeren i Commerce-webstedsgenerator, før du knytter B2C-lejeren til dit eller dine websteder.

Udfør følgende trin for at føje Azure AD B2C-lejerens programoplysninger til Commerce.

1. Log på som administrator af Commerce-webstedsgenerator for dit miljø.
1. Vælg **Lejerindstillinger** i venstre navigationsrude for at udvide den.
1. Vælg **Konfiguration af webstedets godkendelse** under **Lejerindstillinger**. 
1. Vælg **Administrer** i hovedvinduet ved siden af **Godkendelsesprofiler for websted**. (Hvis lejeren vises på profillisten til webstedsgodkendelse, er den allerede blevet tilføjet af en administrator. Kontrollér, at punkterne i trin 6 nedenfor svarer til din ønskede B2C-konfiguration. Der kan også oprettes en ny profil ved hjælp af Azure AD B2C-lejere eller programmer for at tage højde for mindre forskelle som f.eks. forskellige brugerpolitik-id'er).
1. Vælg **Tilføj godkendelsesprofil for websted**.
1. Angiv følgende påkrævede punkter i formularen, der vises, ved at bruge værdier fra B2C-lejeren og -programmet. Felter, der ikke er obligatoriske (dvs. uden en stjerne), kan være tomme.

    - **Programnavn**: Navnet på dit B2C-program, f.eks. "Fabrikam B2C".
    - **Navn på lejer**: Navnet på din B2C-lejer (f.eks. brug "fabrikam", hvis domænet vises som "fabrikam.onmicrosoft.com" for B2C-lejeren). 
    - **Glem adgangskodepolitik-id**: Politik-id for brugerstrømmen for glemt adgangskode, f.eks. "B2C_1_PasswordReset".
    - **Politik-id for tilmelding og logon**: Politik-id for tilmelding og logon i brugerflow, f.eks. "B2C_1_signup_signin".
    - **Klient-GUID**: B2C-program-id'et, f.eks. "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".
    - **Rediger profilpolitik-id**: Politik-id'et for brugerstrømmen til profilredigering, f.eks. "B2C_1A_ProfileEdit".

1. Vælg **OK**. Navnet på dit B2C-program vises nu på listen.
1. Vælg **Gem** for at gemme ændringerne.

Det valgfrie felt **Log på brugerdefineret domæne** bør kun bruges, hvis du konfigurerer et brugerdefineret domæne til Azure AD B2C-lejeren. Yderligere oplysninger om brugen af feltet **Log på brugerdefineret domæne** finder du i [Yderligere B2C-oplysninger](additional-b2c-info.md).

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>Knyt B2C-programmet til dit websted og din kanal

> [!WARNING]
> - Hvis dit websted allerede er knyttet til et B2C program, og du skifter til et andet B2C-program, fjernes de aktuelle referencer, der er oprettet for brugere, som allerede er tilmeldt i dette miljø. Hvis de ændres, vil alle legitimationsoplysninger, der er knyttet til det aktuelt tildelte B2C-program, ikke være tilgængelige for brugerne. 
> - Du skal kun opdatere kun B2C-programmet, hvis du konfigurerer kanalens B2C-program for første gang, eller hvis du vil have, at brugere skal tilmelde sig igen med nye legitimationsoplysninger til denne kanal med det nye B2C-program. Vær forsigtig, når du knytter kanaler til B2C-programmer, og navngiv programmer tydeligt. Hvis en kanal ikke er knyttet til et B2C-program i trinnene nedenfor, vil de brugere, der logger på den pågældende kanal til dit websted, blive angivet i B2C-programmet, der vises som **standard** på listen **Lejerindstillinger \> B2C-indstillinger** for B2C-programmer.

Gør følgende for at knytte B2C-programmet til dit websted og din kanal.

1. Naviger til dit websted i Commerce-webstedsgenerator.
1. Vælg **Indstillinger for websted** i venstre navigationsrude for at udvide den.
1. Vælg **Kanaler** nedenunder **Indstillinger for websted**.
1. Vælg kanalen i hovedvinduet under **Kanaler**.
1. I ruden Egenskaber for kanal til højre skal du vælge navnet på dit B2C-program i rullemenuen **Vælg B2C-program**.
1. Vælg **Luk**, og vælg derefter **Gem og udgiv**.

## <a name="next-steps"></a>Næste trin

Hvis du vil fortsætte med at konfigurere en B2C-lejer i Commerce, skal du fortsætte til [Yderligere B2C-oplysninger](additional-b2c-info.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere en B2C-lejer i Commerce](set-up-b2c-tenant.md)

[Oprette eller sammenkæde med en eksisterende Azure AD B2C-lejer i Azure-portalen](create-link-aad-b2c-tenant.md)

[Opret B2C-programmet](create-b2c-app.md)

[Oprette politikker for brugerstrøm](create-user-flow-policies.md)

[Tilføj sociale identitetsudbydere (valgfrit)](add-social-identity-providers.md)

[Opdater Commerce Headquarters med de nye Azure AD B2C-oplysninger](update-hq-aad-b2c-info.md)

[Flere B2C-oplysninger](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
