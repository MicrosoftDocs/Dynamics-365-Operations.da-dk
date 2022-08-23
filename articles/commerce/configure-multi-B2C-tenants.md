---
title: Konfigurere flere B2C-lejere i et Commerce-miljø
description: Denne artikel beskriver, hvornår og hvordan du konfigurerer flere Microsoft Azure Active Directory (Azure AD) B2C-lejere (Business-to-Consumer) pr. kanal til brugergodkendelse i et dedikeret Dynamics 365 Commerce-miljø.
author: BrianShook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: 4966a3df20544fd6cdff493b8bd1aa566aecdfe9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276886"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a>Konfigurere flere B2C-lejere i et Commerce-miljø

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvornår og hvordan du konfigurerer flere Microsoft Azure Active Directory (Azure AD) B2C-lejere (Business-to-Consumer) pr. kanal til brugergodkendelse i et dedikeret Dynamics 365 Commerce-miljø.

Dynamics 365 Commerce bruger Azure AD B2C cloud-identitetstjeneste til at understøtte brugerlegitimationsoplysninger og godkendelsesstrømme. Brugerne kan bruge godkendelsesstrømmene til at tilmelde sig, logge på og nulstille deres adgangskode. Azure AD B2C gemmer en brugers følsomme godkendelsesoplysninger, f.eks. brugernavn og adgangskode. Brugerposten er entydig for hver B2C-lejer, og den bruger brugernavnets legitimationsoplysninger (mailadressen) eller sociale identitetsudbyderes legitimationsoplysninger.

I de fleste tilfælde bruges en enkelt Azure AD B2C-lejer i et Commerce-miljø. Commerce-kunder kan derefter oprette og udgive flere websteder i samme Commerce-miljø, og de samme kundelegitimationsoplysninger vil blive anvendt på tværs af disse steder. Hvis webstederne i miljøet imidlertid skal behandles som forskellige brands og vises for brugere som separate firmaer, kan en B2C-lejer konfigureres til den kanal, der bruges til adskillelse af lokation/brand.

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a>Overvejelser ved konfiguration af flere B2C-lejere pr. kanal

Når hver kanal eller et websted behandles som en separat virksomhed, er den bedste mulighed ofte, hvad angår brugergodkendelsesprocesser i Commerce, at bruge separate juridiske enheder. Hvis du imidlertid vil have hver kanal/lokation i samme miljø og juridiske enhed, men gerne vil have adskilt brugergodkendelse for hver enkelt websted, er det vigtigt, at du overvejer følgende punkter, før du fortsætter:

- Brugerne vil have deres egne særskilte legitimationsoplysninger for hver kanal/hvert websted.

    Den samme person kan have to separate konti pr. kanal/lokation, da hver konto vil være en entydig post i en separat B2C-lejer.

- I Microsoft Dynamics-miljøet returneres der separate kundeposter med søgninger med globale poster.

    Hvis en bruger anvender den samme mailadresse på tværs af kanaler/websteder, returnerer globale kundesøgninger resultater for hver kanal/hvert enkelt websted. (Der vises en kanalindikator.)

- Du kan bruge adressekartoteket som hjælp til at gruppere brugere, så de kan spores pr. kanal.
- Antallet af kundeposter pr. kanal kan stige, og denne forøgelse kan påvirke udførelsen af globale kundesøgninger.
- B2C-lejere skal være omhyggeligt knyttet til en kanal for at undgå situationer, hvor kunder tilmelder sig en forkert lejer. Ellers kan der opstå forvirring eller sporingsproblemer.

I følgende illustration vises flere B2C-lejere i et Commerce-miljø.

![Flere B2C-lejere i et Commerce-miljø.](media/MultiB2C_In_Environment.png)

Hvis du beslutter, at din virksomhed kræver særskilte B2C-lejere pr. kanal i det samme Commerce-miljø, skal du fuldføre procedurerne i følgende afsnit for at anmode om denne funktion.

## <a name="configure-b2c-tenants-in-your-environment"></a>Konfigurere B2C-lejere i dit miljø

Hvis du vil konfigurere B2C-lejere i dit miljø, skal du gennemføre de relevante procedurer i dette afsnit.

### <a name="add-an-azure-ad-b2c-tenant"></a>Tilføje en Azure AD B2C-lejer

Følg disse trin for at føje en Azure AD B2C-lejer til dit miljø.

1. Log på Commerce-webstedsgeneratoren for dit miljø som systemadministrator. Hvis du vil konfigurere Azure AD B2C-lejere, skal du være systemadministrator for Commerce-miljøet.
1. Vælg **Lejerindstillinger** i venstre navigationsrude for at udvide den.
1. Vælg **B2C-indstillinger**, og vælg derefter **Administrer**.
1. Vælg **Tilføj B2C-program**, og angiv følgende oplysninger:

    - **Programnavn**: Angiv det navn, der skal bruges i programmet i forbindelse med administration af det i Commerce. Vi anbefaler, at du bruger det programnavn, du valgte, da du konfigurerede Azure AD B2C-programmet i Azure-portalen. På denne måde kan du hjælpe med at reducere forvirring, når du håndterer B2C-lejere i Commerce.
    - **Navn på lejer**: Angiv navnet på B2C-lejeren, som det vises i Azure-portalen.
    - **Glem adgangskodepolitik-id**: Angiv politik-id'et (navnet på politikken på Azure-portalen).
    - **Politik-id for tilmelding og logon**: Angiv politik-id'et (navnet på politikken på Azure-portalen).
    - **Klient-GUID**: Angiv det Azure AD B2C-lejer-id, som det vises i Azure-portalen (ikke program-id'et for B2C-lejeren).
    - **Rediger profilpolitik-id**: Angiv politik-id'et (navnet på politikken på Azure-portalen).

1. Vælg **OK**, når du er færdig med at angive disse oplysninger, for at gemme ændringerne. Den nye Azure AD B2C-lejer vises nu på listen under **Administrer B2C-programmer**.

> [!NOTE]
> Du bør lade felter som **Område**, **Ikke-interaktivt politik-id**, **Ikke-interaktivt klient-id**, **Logon på brugerdefineret domæne** og **Politik-id for tilmelding** være tomme, medmindre Dynamics 365 Commerce-teamet beder dig om at angive dem.


### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a>Administrere eller slette en Azure AD B2C-lejer

1. Log på Commerce-webstedsgeneratoren for dit miljø som systemadministrator. Hvis du vil konfigurere Azure AD B2C-lejere, skal du være systemadministrator for Commerce-miljøet.
1. Vælg **Lejerindstillinger** i venstre navigationsrude for at udvide den.
1. Vælg **B2C-indstillinger**, og vælg derefter **Administrer**.
1. Hvis du vil redigere en B2C lejer, skal du vælge blyantsymbolet ud for den. Hvis du vil slette en B2C-lejer, skal du vælge papirkurvssymbolet ud for den.
1. Vælg **Gem**, og vælg derefter **Udgiv** for at aktivere ændringerne.

> [!WARNING]
> Når en B2C-lejer er konfigureret til et live/publiceret websted, har brugerne muligvis tilmeldt sig ved hjælp af konti, der findes i lejeren. Hvis du sletter en konfigureret lejer i menuen **Lejerindstillinger \> B2C-lejer**, fjerner du den pågældende B2C-lejers tilknytning fra steder, der er knyttet til kanaler i lejeren. I dette tilfælde vil brugerne muligvis ikke længere kunne logge på deres konti. Derfor skal du være meget forsigtig, når du sletter en konfigureret lejer.
>
> Når en konfigureret lejer slettes, vil B2C-lejeren og -posterne fortsat være bevaret, men konfigurationen af Commerce-systemlejeren vil blive ændret eller fjernet. Brugere, der forsøger at tilmelde sig eller logge på webstedet, opretter en ny kontopost i standard- eller den netop tilknyttede B2C-lejer, der er konfigureret til kanalen på webstedet.

## <a name="configure-your-channel-with-a-b2c-tenant"></a>Konfigurere din kanal med en B2C-lejer

1. Log på Commerce-webstedsgeneratoren for dit miljø som systemadministrator. Hvis du vil konfigurere Azure AD B2C-lejere, skal du være systemadministrator for Commerce-miljøet.
1. Vælg **Indstillinger for websted** i venstre navigationsrude for at udvide den.
1. Vælg **Kanaler**, og vælg derefter den kanal, der skal konfigureres.
1. Vælg den konfigurerede Azure AD B2C-lejer, der skal bruges til denne kanal, i feltet **Vælg B2C-program** i egenskabsruden til højre.
1. Vælg **Gem og udgiv** på kommandolinjen for at bekræfte den nye eller opdaterede konfiguration.

> [!WARNING]
> Hvis du ændrer det B2C-program, der er tildelt kanalen, fjerner du de aktuelle referencer, der er oprettet for brugere, som allerede er tilmeldt i miljøet. I dette tilfælde vil alle legitimationsoplysninger, der er knyttet til det aktuelt tildelte B2C-program, ikke være tilgængelige for brugerne. Du skal derfor kun ændre en Azure AD B2C-kanalkonfiguration, hvis du konfigurerer kanalen første gang, og ingen brugere har haft mulighed for at tilmelde sig. Ellers skal brugerne måske tilmelde sig igen for at oprette en post i den nye Azure AD B2C-lejer.
## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere dit domænenavn](configure-your-domain-name.md)

[Implementere en ny e-handelslejer](deploy-ecommerce-site.md)

[Oprette et websted for e-handel](create-ecommerce-site.md)

[Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal](associate-site-online-store.md)

[Administrere robots.txt-filer](manage-robots-txt-files.md)

[Masseoverføre omdirigeringer af URL-adresser](upload-bulk-redirects.md)

[Konfigurere en B2C-lejer i Commerce](set-up-B2C-tenant.md)

[Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md)

[Tilføje understøttelse af et netværk, der leverer indhold (CDN)](add-cdn-support.md)

[Aktivere registrering af lokationsbaseret lager](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
