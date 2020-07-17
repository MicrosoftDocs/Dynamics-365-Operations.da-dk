---
title: Konfigurere en B2C-lejer i Commerce
description: I dette emne beskrives, hvordan du konfigurerer dine Azure Active Directory (Azure AD) B2C-lejere (Business-to-Consumer) til godkendelse af brugerwebsteder i Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BriShoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: b017b0f91960be1504134f6d46878fce956de203
ms.sourcegitcommit: 8a1621327568edf49758b70964e0a3e637527e1b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2020
ms.locfileid: "3497162"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>Konfigurere en B2C-lejer i Commerce

[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du konfigurerer dine Azure Active Directory (Azure AD) B2C-lejere (Business-to-Consumer) til godkendelse af brugerwebsteder i Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Dynamics 365 Commerce bruger Azure AD B2C til at understøtte brugerlegitimationsoplysninger og -godkendelsesstrømme. En bruger kan tilmelde dig, logge på og nulstille deres adgangskode via disse strømme. Azure AD B2C gemmer følsomme brugergodkendelsesoplysninger, f.eks. brugernavn og adgangskode. Brugerposten i B2C-lejeren vil gemme en B2C lokal kontopost eller en B2C social identitetsudbyderpost. Disse B2C-poster vil oprette et link tilbage til kundeposten i Commerce-miljøet.

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a>Oprette eller sammenkæde med en eksisterende AAD B2C-lejer i Azure-portalen

1. Log på [Azure-portalen](https://portal.azure.com/).
1. Vælg **Opret en ressource**i Azure-portalmenuen. Sørg for at bruge det abonnement og den mappe, der er forbundet med dit Commerce-miljø.

    ![Oprette en ressource i Azure-portalen](./media/B2CImage_1.png)

1. Gå til **Identitet \> Azure Active Directory B2C**.
1. Når du er på siden **Opret ny B2C lejer eller Opret et link til en eksisterende lejer**, skal du bruge en af de muligheder nedenfor, der bedst passer til firmaets behov:

    - **Opret en ny Azure AD B2C-lejer**: Brug denne indstilling til at oprette en ny AAD B2C-lejer.
        1. Vælg **Opret en ny Azure AD B2C-lejer**.
        1. Angiv organisationsnavnet under **Organisationsnavn**.
        1. Angiv det oprindelige domænenavn under **Oprindeligt domænenavn**.
        1. Vælg land eller område for **Land eller område**.
        1. Vælg **Opret** for at oprette lejeren.

     ![Opret en ny Azure AD-lejer](./media/B2CImage_2.png)

     - **Sammenkæd en eksisterende Azure AD B2C lejer med mit Azure-abonnement**: Brug denne indstilling, hvis du allerede har en Azure AD B2C lejer, du vil oprette et link til.
        1. Vælg **Sammenkæd en eksisterende Azure AD B2C lejer til mit Azure-abonnement**.
        1. Vælg den relevante B2C-lejer for **Azure AD B2C-lejer**. Hvis meddelelsen "Der ikke blev fundet nogen berettiget B2C-lejer" vises i valgfeltet, har du ikke en eksisterende berettiget B2C-lejer og skal oprette en ny.
        1. Vælg **Opret ny** for **Ressourcegruppe**. Angiv et **Navn** på den ressourcegruppe, der skal indeholde lejeren, Vælg **Ressourcegruppens lokalitet**, og vælg derefter **Opret**.

    ![Sammenkæd en eksisterende Azure AD B2C lejer til mit Azure-abonnement](./media/B2CImage_3.png)

1. Når den nye Azure AD B2C-mappe er oprettet (det kan tage et øjeblik), vises der et link til den nye mappe på dashboardet. Dette link vil føre dig til siden "Velkommen til Azure Active Directory B2C".

    ![Link til ny AAD-mappe](./media/B2CImage_4.png)

> [!NOTE]
> Hvis du har flere abonnementer til din Azure-konto eller har konfigureret B2C-lejeren uden at oprette forbindelse til et aktivt abonnement, kan du bruge banneret **Fejlfinding** til at knytte lejeren til et abonnement. Vælg fejlfindingsmeddelelsen, og følg instruktionerne for at løse abonnementsproblemet.

I følgende billede vises et eksempel på et Azure AD B2C-banner til **Fejlfinding**.

![Advarsel viser, at mappen ikke har noget aktivt abonnement](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a>Opret B2C-programmet

Når B2C-lejeren er blevet oprettet, skal du oprette et B2C-program i lejeren for at kunne kommunikere med Commerce-handlingerne.

Hvis du vil oprette B2C-programmet, skal du følge disse trin.

1. Vælg **Programmer** i Azure-portalen, og vælg derefter **Tilføj**.
1. Angiv på det ønskede AAD B2C-program under **Navn**.
1. Vælg **Ja** for **Inkluder webapp/web-API** under **Webapp/Web-API**.
1. Vælg **Ja** (standardværdien) til **Tillad implicit flow**.
1. Angiv dine dedikerede svar-URL-adresser under **Svar-URL-adresse**. Se [Svar-URL-adresser](#reply-urls) nedenfor for at få oplysninger om svar-URL-adresser, og hvordan du formaterer dem her.
1. Vælg **Nej** (standardværdien) til **Medtag som oprindelig klient**.
1. Vælg **Opret**.

### <a name="reply-urls"></a>Svar-URL-adresser

Svar-URL-adresser er vigtige, da de giver en liste over returdomænerne, når dit websted kalder Azure AD B2C for at godkende en bruger. Det gør det muligt at returnere den godkendte bruger tilbage til det domæne, hvor de logger på (domænet for dit websted). 

I feltet **Svar-URL-adresse** på skærmen **Azure AD B2C-programmer \> Nyt program** skal du tilføje separate linjer til både dit websteds domæne og (når miljøet er klargjort) til den Commerce-genererede URL-adresse. Disse URL-adresser skal altid bruge et gyldigt URL-adresseformat og må kun være grundlæggende URL-adresser (ingen efterfølgende skråstreger eller stier). Strengen ``/_msdyn365/authresp`` skal derefter føjes til de grundlæggende URL-adresser som i følgende eksempler.

- ``https://www.fabrikam.com/_msdyn365/authresp`` (Domænet skal svare helt til e-handelsdomænet. Hvis du har flere domæner, skal du tilføje denne URL-adresse for hvert domæne.)
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a>Oprette politikker for brugerstrøm

Brugerstrømme er de politikker, som Azure AD B2C bruger til at give sikker log ind, registrere, redigere profil og glemme brugeroplevelser med adgangskoder. Dynamics 365 Commerce bruger disse strømme til at udføre politikhandlingerne for at kommunikere med Azure AD B2C-lejeren. Når en bruger kommunikerer med disse politikker, omdirigeres de til Azure AD B2C-lejeren for at udføre handlingerne.

Azure AD B2C omfatter tre grundlæggende brugerstrømtyper:
- Tilmelde og logge på
- Profilredigering
- Adgangskoden er nulstillet

Du kan vælge at bruge de standardbrugerstrømme, der leveres af Azure AD, og som viser en side, der er placeret på Aad B2C. Du kan også oprette en HTML-side for at styre udseendet af disse brugerstrømoplevelser. 

Hvis du vil tilpasse brugerpolitiksiderne for Dynamics 365 Commerce, skal du se [Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md). Du kan finde flere oplysninger under [Tilpasse grænsefladen af brugeroplevelser i Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Oprette en tilmeldings- og login-politik for brugerstrøm

Gør følgende for at konfigurere en tilmeldings- og login-politik.

1. Vælg **Brugerstrømme (politikker)** i navigationsruden til venstre i Azure-portalen.
1. Vælg **Ny brugerstrøm** på siden **Azure AD B2C – Brugerstrømme (politikker)**.
1. Vælg **Tilmelde og logge på** på fanen **Anbefalet**.
1. Angiv et politiknavn under **Navn**. Dette navn vises bagefter med et præfiks, som portalen tildeler (f.eks. "B2C_1_").
1. Marker det relevante afkrydsningsfelt under **Identitetsudbydere**.
1. Vælg det relevante valg for dit firma under **Godkendelse af flere oplysninger**. 
1. Vælg indstillinger til at indsamle attributter eller returnere krav efter behov under **Brugerattributter og -krav**. Commerce kræver følgende standardindstillinger:

    | **Indsaml attribut** | **Returkrav** |
    | ---------------------- | ----------------- |
    | E-mailadresse          | Mailadresser   |
    | Givent navn             | Givent navn        |
    |                        | Identitetsudbyder |
    | Efternavn                | Efternavn           |
    |                        | Brugerens objekt-id  |

1. Vælg **Opret**.

Følgende billede er et eksempel på brugerstrømmen i Azure AD B2C-tilmelding og -login.

![Politikindstillinger for tilmelding og login](./media/B2CImage_11.png)

I følgende billede vises indstillingen **Kør brugerstrøm** i brugerstrømmen Azure AD B2C-tilmelding og -login.

![Kør indstillingen brugerstrøm i politikstrøm](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a>Oprette en brugerstrømpolitik til profilredigering

Gør følgende for at oprette en brugerstrømpolitik til profilredigering.

1. Vælg **Brugerstrømme (politikker)** i navigationsruden til venstre i Azure-portalen.
1. Vælg **Ny brugerstrøm** på siden **Azure AD B2C – Brugerstrømme (politikker)**.
1. Vælg **Profilredigering** på fanen **Anbefalet**.
1. Angiv brugerstrømmen til profilredigeringen under **Navn**. Dette navn vises bagefter med et præfiks, som portalen tildeler (f.eks. "B2C_1_").
1. Vælg **Lokal kontoregistrering** under **Identitetsudbydere**.
1. Vælg følgende afkrydsningsfelter under **Brugerattributter**:
    - **Mailadresser** (kun **Returkrav**)
    - **Givent navn** (**Indsaml attribut** og **Returneringskrav**)
    - **Identitetsudbyder** (kun **Returnkrav**)
    - **Efternavn** (**Indsaml attribut** og **Returneringskrav**)
    - **Brugerens objekt-id** (kun **Returkrav**)
1. Vælg **Opret**.

I følgende billede vises et eksempel på brugerstrøm til Azure AD B2C profilredigering.

![Opret brugerstrømpolitikken til profilredigering](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>Opret en brugerstrømpolitik til nulstilling af adgangskode

Gør følgende for at oprette en brugerstrømpolitik til nulstilling af adgangskode.

1. Vælg **Brugerstrømme (politikker)** i navigationsruden til venstre i Azure-portalen.
1. Vælg **Ny brugerstrøm** på siden **Azure AD B2C – Brugerstrømme (politikker)**.
1. Vælg **Nulstilling af adgangskode** på fanen **Anbefalet**.
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

## <a name="add-social-identity-providers-optional"></a>Tilføj sociale identitetsudbydere (valgfrit)

Sociale identitetsudbydere giver brugerne mulighed for at bruge deres sociale konti til godkendelse. Tilføjelse af godkendelse af sociale identitetsudbydere er valgfri i Dynamics 365 Commerce. 

Hvis godkendelse af sociale identitetsudbydere ikke tilføjes, vil Azure AD B2C-standardprofilerne være hovedprofilerne til din brugerbase. Brugerne vælger deres eget brugernavn (deres foretrukne mailadresse) og angiver en adgangskode. Azure AD B2C vil godkende brugere direkte. 

Hvis godkendelse af sociale identitetsudbydere er tilføjet, og en bruger vælger en af de tilbudte sociale identitetsudbydere, oprettes der stadig en enhed i Azure AD B2C-lejeren. Azure AD B2C godkender derefter brugerens legitimationsoplysninger via den sociale identitetsudbyder.

> [!NOTE]
> Identitetsudbyderens login opretter en post i B2C-lejeren, men i et andet format end lokale konti, da det kalder den eksterne sociale identitetsudbyders reference for godkendelse. Brugeren kan bruge den samme mailadresse på tværs af sociale identitetsudbydere, hvilket betyder, at det brugernavn, der bruges til godkendelse af mailadressen, ikke er entydigt for lejeren. Azure AD B2C vil kun gennemtvinge, at brugere har en entydig mailadresse på lokale B2C-konti.

Før du kan tilføje en social identitetsudbyder til godkendelse, skal du gå til portalen for identitetsudbyderen og konfigurere et identitetsudbyderprogram som angivet i dokumentationen til Azure AD B2C. Der findes en liste over links til dokumentationen nedenfor.

- [Amazon](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD (Enkelt lejer)](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [Microsoft-konto](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>Tilføje og konfigurere en sociale identitetsudbyder

Udfør følgende trin for at tilføje og konfigurere en social identitetsudbyder.  

1. Naviger til **Identitetsudbydere**i Azure-portalen.
1. Vælg **Tilføj**. Skærmbilledet **Tilføj identitetsudbyder** vises.
1. Angiv det navn, der skal vises for brugere på din login-skærm, under **Navn**.
1. Vælg en identitetsudbyder på listen under **Type identitetsudbyder**.
1. Vælg **OK**.
1. Vælg **Konfigurer denne identitetsudbyder** for at få adgang til skærmbilledet **Konfigurer den sociale identitetsudbyder** .
1. Angiv det klient-id, der er hentet fra installationsprogrammet til identitetsudbyderen, under **Klient-id**.
1. Angiv den klienthemmelighed, der er hentet fra installationsprogrammet til identitetsudbyderen, under **Klienthemmelighed**.
1. Knyt brugerstrøm til tilmeldings- og login-politikker:
1. Gå til **Azure AD B2C – Brugerstrømme (politikker) \> {din tilmeldings- og logon-politik} \> Identitetsudbydere**.
1. Hvis du vil knytte brugerstrømmen til login/tilmeldingspolitikken, skal du vælge hver af de identitetsudbydere, du har konfigureret til din konto. Hvis du vil teste disse, skal du vælge **Kør brugerstrøm** for hver identitetsudbyder. Login-siden vises på en ny fane, og der vises et valgfelt til den nye identitetsudbyder.

I følgende billede vises eksempler på skærmbillederne **Tilføj identitetsudbyder** og **Konfigurerer sociale identitetsudbydere** i Azure AD B2C.

![Føje en social identitetsudbyder til dit program](./media/B2CImage_14.png)

I følgende billede vises et eksempel på, hvordan du kan vælge identitetsudbydere på siden Azure AD B2C **Identitetsudbydere**.

![Vælg alle de sociale identitetsudbydere, der skal aktiveres for din politik](./media/B2CImage_16.png)

I følgende billede vises et eksempel på en standardlogin-skærm, hvor der vises en knap til login på en social identitetsudbyder.

![Eksempel på standardlogin-skærm med knap til login til social identitetsudbyder](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Opdater Commerce Headquarters med de nye Azure AD B2C-oplysninger

Når du har udført overstående trin til Azure AD B2C-klargøring, skal Azure AD B2C-programmet registreres i dit Dynamics 365 Commerce-miljø.

Udfør følgende trin for at opdatere Headquarters med de nye Azure AD B2C-oplysninger.

1. Gå til **Delte Commerce-parametre** i Commerce, og vælg **Identitetsudbydere** i menuen til venstre.
1. Gør følgende under **Identitetsudbydere**:
    1. Angiv URL-adressen til udbyderen af identitetsudbydere i feltet **Udbyder**. Du kan finde URL-adressen til udstederen [Få udsteders URL-adresse](#obtain-issuer-url) nedenfor.
    1. Skriv et navn på din udbyderpost i feltet **Navn**.
    1. Skriv **Azure AD B2C (id_token)** i feltet **Type**.
1. Gør følgende under **Betroede parter** med ovenstående B2C-identitetsudbyderelement valgt:
    1. Angiv dit B2C-program-id i feltet **Klient-id**. Du kan finde dette i feltet **Program-id** på siden med egenskaber for B2C-programmet.
    1. Skriv **Offentlig** i feltet **Type**.
    1. Skriv **Kunde** i feltet **Brugertype**.
1. Gå til handlingsruden, og vælg **Gem**.
1. Søg efter **Distributionsplan** i feltet Commerce-søgning
1. Vælg job **1110 global konfiguration** i den venstre navigationsmenu på siden **Distributionsplaner**.
1. Vælg **Kør nu** i handlingsruden.

### <a name="obtain-issuer-url"></a>Hent URL-adresse til udsteder

Følg disse trin for at få URL-adressen til identitetsudbyderens udsteder.

1. Opret en URL-metadataadresse i følgende format med din B2C-lejer og -politik: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Eksempel: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Angiv URL-metadataadressen i en browsers adresselinje.
1. Kopier URL-adressen til identitetsudbyderens udsteder (værdien for **"udsteder"**) i metadataene.
    - Eksempel: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>Konfigurere din B2C-lejer i Commerce-webstedsgeneratoren

Når konfigurationen af din Azure AD B2C-lejer er fuldført, skal du konfigurere B2C-lejeren i Commerce-webstedsgeneratoren. Konfigurationstrin omfatter indsamling af oplysninger om B2C-programmet fra Azure-portalen, indtastning af B2C-programoplysninger i webstedsgeneratoren og derefter tilknytning af B2C-programmet til dit webstedsted og din kanal.

### <a name="collect-the-required-application-information"></a>Indsaml de nødvendige programoplysninger

Udfør følgende trin for at indsamle de nødvendige programoplysninger.

1. Gå til **Start \> Azure AD B2C-programmer** i Azure-portalen.
1. Vælg dit program, og vælg derefter **Egenskaber** i venstre navigationsrude for at få oplysninger om programmet.
1. I boksen **Program-id** skal du indsamle program-id'et for det B2C-program, der er oprettet i din B2C-lejer. Det vil senere blive angivet som **Klient-GUID** i webstedsgeneratoren.
1. Hent svar-URL-adressen under **Svar-URL-adresse**.
1. Gå til **Start \> Azure AD B2C – Brugerstrømme (politikker)**, og indsaml derefter navnene på hver enkelt brugerstrømpolitik.

I følgende billede vises et eksempel på siden **Azure AD B2C-programmer**.

![Naviger til B2C-programmet i din lejer](./media/B2CImage_19.png)

I følgende billede vises et eksempel på siden **Egenskaber** for et program i Azure AD B2C. 

![Kopiér program-id'et fra egenskaberne for B2C-programmet](./media/B2CImage_21.png)

I følgende billede vises et eksempel på brugerstrømpolitikker på siden **Azure AD B2C – Brugerstrømme (politikker)**.

![Indsaml navnene på de enkelte B2C-politikstrømme](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a>Angiv programoplysninger om din AAD B2C-lejer i Commerce

Du skal angive oplysninger om Azure AD B2C-lejeren i Commerce-webstedsgenerator, før du knytter B2C-lejeren til dit eller dine websteder.

Udfør følgende trin for at føje AAD B2C-lejerens programoplysninger til Commerce.

1. Log på som administrator af Commerce-webstedsgenerator for dit miljø.
1. Vælg **Lejerindstillinger** i venstre navigationsrude for at udvide den.
1. Vælg **B2C-indstillinger** under **Lejerindstillinger**. 
1. Vælg **Administrer** i hovedvinduet ved siden af **B2C-programmer**. (Hvis lejeren vises på B2C-programlisten, er den allerede blevet tilføjet af en administrator. Kontrollér, at punkterne i trin 6 nedenfor svarer til dit B2C-program.)
1. Vælg **Tilføj B2C-program**.
1. Angiv følgende påkrævede punkter i formularen, der vises, ved at bruge værdier fra B2C-lejeren og -programmet. Felter, der ikke er obligatoriske (dvs. uden en stjerne), kan være tomme.

    - **Programnavn**: Navnet på dit B2C-program, f.eks. "Fabrikam B2C".
    - **Navn på lejer**: Navnet på din B2C-lejer (f.eks. brug "fabrikam", hvis domænet vises som "fabrikam.onmicrosoft.com" for B2C-lejeren). 
    - **Glem adgangskodepolitik-id**: Politik-id for brugerstrømmen for glemt adgangskode, f.eks. "B2C_1_PasswordReset".
    - **Politik-id for tilmelding og logon**: Politik-id for tilmelding og logon i brugerstrømmen, f.eks. "B2C_1_signup_signin".
    - **Klient-GUID**: B2C-program-id'et, f.eks. "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".
    - **Rediger profilpolitik-id**: Politik-id'et for brugerstrømmen til profilredigering, f.eks. "B2C_1A_ProfileEdit".

1. Vælg **OK**. Navnet på dit B2C-program vises nu på listen.
1. Vælg **Gem** for at gemme ændringerne.

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>Knyt B2C-programmet til dit websted og din kanal

> [!WARNING]
> Hvis dit websted allerede er knyttet til et B2C program, og du skifter til et andet B2C-program, fjernes de aktuelle referencer, der er oprettet for brugere, som allerede er tilmeldt i dette miljø. Hvis de ændres, vil alle legitimationsoplysninger, der er knyttet til det aktuelt tildelte B2C-program, ikke være tilgængelige for brugerne. 
> 
> Du skal kun opdatere kun B2C-programmet, hvis du konfigurerer kanalens B2C-program for første gang, eller hvis du vil have, at brugere skal tilmelde sig med nye legitimationsoplysninger til denne kanal med det nye B2C-program. Vær forsigtig, når du knytter kanaler til B2C-programmer, og navngiv programmer tydeligt. Hvis en kanal ikke er knyttet til et B2C-program i trinnene nedenfor, vil de brugere, der logger på den pågældende kanal til dit websted, blive angivet i B2C-programmet, der vises som **standard** på listen **Lejerindstillinger \> B2C-indstillinger** for B2C-programmer.

Gør følgende for at knytte B2C-programmet til dit websted og din kanal.

1. Naviger til dit websted i Commerce-webstedsgenerator.
1. Vælg **Indstillinger for websted** i venstre navigationsrude for at udvide den.
1. Vælg **Kanaler** nedenunder **Indstillinger for websted**.
1. Vælg kanalen i hovedvinduet under **Kanaler**.
1. I ruden Egenskaber for kanal til højre skal du vælge navnet på dit B2C-program i rullemenuen **Vælg B2C-program**.
1. Vælg **Luk**, og vælg derefter **Gem og udgiv**.

## <a name="additional-b2c-information"></a>Flere B2C-oplysninger

### <a name="customer-migration"></a>Kundeoverflytning

Hvis du overvejer at overflytte kundeposter fra en tidligere identitetsudbyderplatform, skal du arbejde med Dynamics 365 Commerce-teamet for at gennemgå dine behov for kundeoverflytning.

Du kan få yderligere Azure AD B2C-dokumentation om kundeoverflytning under [Overflytte brugere til Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Brugerdefinerede politikker

Du kan få yderligere oplysninger om tilpasning af Azure AD B2C-interaktioner og politikstrømme, der ligger ud over, hvad der tilbydes af B2C standardpolitikker, i [Tilpassede politikker i Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Sekundær administrator

Du kan tilføje en valgfri, sekundær administratorkonto under afsnittet **Bruger** i din B2C-lejer. Det kan være en direkte konto eller en generel konto. Hvis du skal dele en konto på tværs af teamressourcer, kan du også oprette en fælles konto. På grund af følsomheden for de data der er lagret i Azure AD B2C, skal en fælles konto overvåges nøje i følge firmaets sikkerhedspraksis.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere dit domænenavn](configure-your-domain-name.md)

[Implementere et nyt websted for e-handel](deploy-ecommerce-site.md)

[Oprette et websted for e-handel](create-ecommerce-site.md)

[Tilknytte et onlinewebsted til en kanal](associate-site-online-store.md)

[Administrere robots.txt-filer](manage-robots-txt-files.md)

[Masseoverføre omdirigeringer af URL-adresser](upload-bulk-redirects.md)

[Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md)

[Konfigurere flere B2C-lejere i et Commerce-miljø](configure-multi-B2C-tenants.md)

[Tilføje understøttelse af et netværk, der leverer indhold (CDN)](add-cdn-support.md)

[Aktivere registrering af lokationsbaseret lager](enable-store-detection.md)
