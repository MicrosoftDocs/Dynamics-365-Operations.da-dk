---
title: Konfigurere brugerdefinerede sider til brugerlogon
description: Dette emne beskriver, hvordan du bygger tilpassede sider i Microsoft Dynamics 365 Commerce, der håndterer tilpasset logon for brugere af Azure Active Directory (Azure AD) Business-to-Consumer-lejere (B2C).
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5d9f2febc912b35897b063019146d219cadea1fa
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517226"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>Konfigurere brugerdefinerede sider til brugerlogon


[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du bygger tilpassede sider i Microsoft Dynamics 365 Commerce, der håndterer tilpasset logon for brugere af Azure Active Directory (Azure AD) Business-to-Consumer-lejere (B2C).

## <a name="overview"></a>Oversigt

Hvis du vil bruge brugerdefinerede sider, der er oprettet i Dynamics 365 Commerce, til at håndtere brugerlogon, skal du konfigurere de Azure AD-politikker, der skal refereres til i Commerce-miljøet. Du kan konfigurere Azure AD B2C-politikkerne "Tilmelding og logon", "Profilredigering" og "Nulstilling af adgangskode" ved hjælp af Azure AD B2C-programmet. Der kan derefter refereres til Azure AD B2C-lejeren og politiknavne under den klargørings proces, der udføres for Commerce-miljøet ved hjælp af Microsoft Dynamics Lifecycle Services (LCS).

De brugerdefinerede Commerce-sider kan opbygges ved hjælp af modulet til logon, tilmelding, kontoprofilredigering eller genstart af adgangskode. De URL-adresser til sider, der udgives for disse brugerdefinerede sider, skal derefter refereres i Azure AD B2C-politikkonfigurationerne i Azure-portalen.

## <a name="set-up-b2c-policies"></a>Konfigurere B2C-politikker

Når du har konfigureret din Azure AD B2C-lejer og har knyttet den til Commerce-miljøet, skal du gå siden **Azure AD B2C** i Azure-portalen og derefter vælge **Brugerstrømme (politikker)** i menuen under **Politikker**.

![Kommandoen Brugerstrømme (politikker) i menuen](./media/B2C_CustomPage_PoliciesMenu.png)

Du kan nu konfigurere brugerlogonstrømmene "Tilmelding og logon", "Profilredigering" og "Nulstilling af adgangskode".

### <a name="configure-the-sign-up-and-sign-in-policy"></a>Konfigurere politikken "Tilmelding og logon"

For at konfigurere politikken "Tilmelding og logon" skal du udføre følgende trin.

1. Vælg **Ny brugerstrøm**, og vælg derefter politikken **Tilmelding og logon** under fanen **Anbefalet**.
1. Angiv et navn til politikken (f.eks. **B2C\_1\_TilmeldingLogon**).
1. Vælg de id-udbydere, der skal bruges til politikken, i sektionen **Identitetsudbydere**. Du skal som minimum vælge **E-mailtilmelding**.
1. I kolonnen **Indsaml attribut** skal du markere afkrydsningsfelterne for **E-mailadresse**, **Tildelt navn** og **Efternavn**.
1. I kolonnen **Returkrav** skal du markere afkrydsningsfelterne **E-mailadresser**, **Tildelt navn**, **Identitetsudbyder**, **Efternavn** og **Brugerens objekt-id**.

    ![Valgte attributter og krav](./media/B2C_SignInSignUp_Attributes.png)

1. Vælg **OK** for at oprette politikken.
1. Dobbeltklik på navnet på den nye politik, og vælg derefter **Egenskaber** i navigationsruden.
1. Vælg **Til** i indstillingen **Aktivér JavaScript-valg af sidelayout (eksempel)**.

    ![Siden Egenskaber for den nye politik](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> Der bliver refereret til hele politiknavnet i Commerce-miljøet. (**B2C\_1\_**-præfikset bliver medtaget i referencen). Politikker kan ikke omdøbes, når de først er oprettet. Hvis du erstatter en eksisterende politik for Commerce-miljøet, kan du slette den oprindelige politik og oprette en ny politik med samme navn. Hvis miljøet allerede er blevet klargjort, kan du også sende det nye politiknavn via en serviceanmodning.

Du skal vende tilbage til denne politik for at afslutte installationen, når du har opbygget de brugerdefinerede sider. Du skal nu lukke politikken for at vende tilbage til siden **Brugerstrømme (politikker)** i Azure-portalen.

### <a name="configure-the-profile-editing-policy"></a>Konfigurere politikken "Profilredigering"

Du kan konfigurere politikken "Profilredigering" ved at følge disse trin.

1. Vælg **Ny brugerstrøm**, og vælg derefter politikken **Profilredigering** under fanen **Anbefalet**.
1. Angiv et navn til politikken (f.eks. **B2C\_1\_RedigerProfil**).
1. Vælg de id-udbydere, der skal bruges til politikken, i sektionen **Identitetsudbydere**. Der skal som minimum være valgt **Log på lokal konto**.
1. I kolonnen **Indsaml attribut** skal du markere afkrydsningsfelterne for **E-mailadresse** og **Efternavn**.
1. I kolonnen **Returkrav** skal du markere afkrydsningsfelterne **E-mailadresser**, **Tildelt navn**, **Identitetsudbyder**, **Efternavn** og **Brugerens objekt-id**.
1. Vælg **OK** for at oprette politikken.
1. Dobbeltklik på navnet på den nye politik, og vælg derefter **Egenskaber** i navigationsruden.
1. Vælg **Til** i indstillingen **Aktivér JavaScript-valg af sidelayout (eksempel)**.

Du skal vende tilbage til denne politik for at afslutte installationen, når du har opbygget de brugerdefinerede sider. Du skal nu lukke politikken for at vende tilbage til siden **Brugerstrømme (politikker)** i Azure-portalen.

### <a name="configure-the-password-reset-policy"></a>Konfigurere politikken "Nulstilling af adgangskode"

Du kan konfigurere politikken "Nulstilling af adgangskode" ved at følge disse trin.

1. Vælg **Ny brugerstrøm**, og vælg derefter politikken **Nulstilling af adgangskode v1.1** under fanen **Eksempel**.

    ![Politikken for Nulstilling af adgangskode v.1.1 valgt under fanen Eksempel](./media/B2C_ForgetPassword_Menu.png)

1. Angiv et navn til politikken (f.eks. **B2C\_1\_GlemtAdgangskode**).
1. Vælg **Nulstil adgangskode ved hjælp af e-mailadresse** i sektionen **Identitetsudbydere**.
1. I kolonnen **Returkrav** skal du markere afkrydsningsfelterne **E-mailadresser**, **Tildelt navn**, **Efternavn** og **Brugerens objekt-id**.

    ![Valgte krav](./media/B2C_ForgetPassword_Attributes.png)

1. Vælg **OK** for at oprette politikken.
1. Dobbeltklik på navnet på den nye politik, og vælg derefter **Egenskaber** i navigationsruden.
1. Vælg **Til** i indstillingen **Aktivér JavaScript-valg af sidelayout (eksempel)**.

Du skal vende tilbage til denne politik for at afslutte installationen, når du har opbygget de brugerdefinerede sider. Du skal nu lukke politikken for at vende tilbage til siden **Brugerstrømme (politikker)** i Azure-portalen.

## <a name="build-the-custom-pages"></a>Oprette brugerdefinerede sider

Udfør følgende trin for at opbygge de brugerdefinerede sider til håndtering af brugerlogon.

1. Gå til dit websted i Commerce-oprettelsesværktøjerne.
1. Opbyg følgende fem skabeloner og fem sider:

    - En **Logon**-skabelon og -side, der bruger logonmodulet.
    - En **Logon**-skabelon og -side, der bruger logonmodulet.
    - En skabelon og side til **Nulstilling af adgangskod**, der bruger modulet til nulstilling af adgangskode.
    - En skabelon og side til **Bekræftelse af nulstilling af adgangskod**, der bruger modulet til bekræftelse af nulstilling af adgangskode.
    - En skabelon og side til **Profilredigering**, der bruger modulet til redigering af kontoprofilen

Når du opbygger siderne, skal du følge disse retningslinjer:

- For hver side eller hvert modul skal du bruge det layout og den typografi, der passer bedst til dine forretningsbehov.
- Udgiv alle sider og URL-adresser, der skal bruges i Azure AD B2C-opsætningen.
- Når siderne og URL-adresserne er publiceret, skal du indsamle de URL-adresser, der skal bruges til konfigurationer af Azure AD B2C-politikken. Der føjes et **?preloadscripts=true**-suffiks til hver URL-adresse, når den bruges.

> [!IMPORTANT]
> Du må ikke genbruge universelle sidehoveder og sidefødder, der har relative hyperlinks. Da disse sider findes på Azure AD B2C-domænet, når de bruges, bør der kun bruges absolutte URL-adresser til alle links.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>Konfigurere Azure AD B2C-politikker med oplysninger om brugerdefinerede sider 

Gå tilbage til siden **Azure AD B2C** i Azure-portalen, og vælg derefter **Brugerstrømme (politikker)** i menuen under **Politikker**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>Opdatere politikken "Tilmelding og logon" med oplysninger om brugerdefinerede sider

Følg disse trin for at opdatere politikken "Tilmelding og logon" med oplysninger om brugerdefinerede sider.

1. Vælg **Sidelayout** i den **Tilmelding og logon**-politik, du har konfigureret tidligere, i navigationsruden.
1. Vælg layoutet **Side for samlet tilmelding eller logon**.
1. Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.
1. Angiv hele URL-adressen til logon i feltet **Brugerdefineret side-URI**. Medtag suffikset **?preloadscripts=true**. Angiv for eksempel ``www.<my domain>.com/sign-in?preloadscripts=true``.
1. I feltet **Sidelayoutversion (Eksempel)** skal du vælge **1.2.0**.
1. Vælg layoutet **Lokal kontotilmelding**.
1. Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.
1. Angiv hele URL-adressen til tilmelding i feltet **URL-adresse til brugerdefineret side**. Medtag suffikset **?preloadscripts=true**. Angiv for eksempel ``www.<my domain>.com/sign-up?preloadscripts=true``.
1. I feltet **Sidelayoutversion (Eksempel)** skal du vælge **1.2.0**.
1. Benyt følgende fremgangsmåde i sektionen **Brugerattributter**:

    1. Vælg **Nej** i feltet **Kræver bekræftelse** for attributterne **E-mailadresse**, **Tildelt navn** og **Efternavn**.
    1. Vælg **Nej** i feltet **Valgfrit** for attributterne **Tildelt navn** og **Efternavn**.

    ![Konfiguration af politikken for tilmelding til en lokal konto](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>Opdatere politikken "Profilredigering" med oplysninger om brugerdefinerede sider

Følg disse trin for at opdatere politikken "Profilredigering" med oplysninger om brugerdefinerede sider.

1. Vælg **Sidelayout** i den **Profilredigering**-politik, du har konfigureret tidligere, i navigationsruden.
1. Vælg layoutet til **Profilredigeringsside**.
1. Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.
1. Angiv hele URL-adressen til profilredigering i feltet **URL-adresse til brugerdefineret side**. Medtag suffikset **?preloadscripts=true**. Angiv for eksempel ``www.<my domain>.com/profile-edit?preloadscripts=true``.
1. I feltet **Sidelayoutversion (Eksempel)** skal du vælge **1.2.0**.
1. Benyt følgende fremgangsmåde i sektionen **Brugerattributter**:

    1. Vælg **Nej** i feltet **Kræver bekræftelse** for attributterne **E-mailadresse**, **Tildelt navn**.
    1. Vælg **Nej** i feltet **Valgfrit** for attributterne **Tildelt navn** og **Efternavn**.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>Opdatere politikken "Nulstilling af adgangskode" med oplysninger om brugerdefinerede sider

Følg disse trin for at opdatere politikken "Nulstilling af adgangskode" med oplysninger om brugerdefinerede sider.

1. Vælg **Sidelayout** i den **Nulstilling af adgangskode**-politik, du har konfigureret tidligere, i navigationsruden.
1. Vælg layoutet **Side for ny adgangskode**.
1. Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.
1. Angiv hele URL-adressen til nulstilling af kodeord i feltet **URL-adresse til brugerdefineret side**. Medtag suffikset **?preloadscripts=true**. Angiv for eksempel ``www.<my domain>.com/passwordreset?preloadscripts=true``.
1. I feltet **Sidelayoutversion (Eksempel)** skal du vælge **1.2.0**.
1. Vælg layoutet for **Side til kontogodkendelse**.
1. Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.
1. Angiv hele URL-adressen til verificering af nulstilling af kodeord i feltet **URL-adresse til brugerdefineret side**. Medtag suffikset **?preloadscripts=true**. Angiv for eksempel ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.
1. I feltet **Sidelayoutversion (Eksempel)** skal du vælge **1.2.0**.



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Tilpasse standardtekststrenge for etiketter og beskrivelser

I modulbiblioteket er logonmoduler udfyldt på forhånd med standardtekststrenge til etiketter og beskrivelser. Du kan tilpasse disse strenge i SDK (Software Development Kit) ved at opdatere værdierne i filen global.json for logonmodulet.

Standardteksten for linket til den glemte adgangskode er f.eks. **Har du glemt adgangskoden?**. I det følgende vises denne standardtekst på logonsiden.

![Standardtekst for linket til glemt adgangskode på logonsiden](./media/B2C_SignUp_ModuleFace.png)

Du kan dog redigere teksten til **Har du glemt adgangskoden?** i filen global.json til modulbibliotekets logonmodul, som vist i følgende illustration.

![Linkteksten opdateret i logonmodulets global.json-fil](./media/B2C_CustomizingStringsForModule.png)

Når du har opdateret global.json-filen og publiceret dine ændringer, vises den nye linktekst i logonmodulet i både Commerce og på den direkte logonside.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere dit domænenavn](configure-your-domain-name.md)

[Implementere en ny e-handelslejer](deploy-ecommerce-site.md)

[Oprette et websted for e-handel](create-ecommerce-site.md)

[Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal](associate-site-online-store.md)

[Administrere robots.txt-filer](manage-robots-txt-files.md)

[Masseoverføre omdirigeringer af URL-adresser](upload-bulk-redirects.md)

[Konfigurere en B2C-lejer i Commerce](set-up-B2C-tenant.md)

[Konfigurere flere B2C-lejere i et Commerce-miljø](configure-multi-B2C-tenants.md)

[Tilføje understøttelse af et netværk, der leverer indhold (CDN)](add-cdn-support.md)

[Aktivere registrering af lokationsbaseret lager](enable-store-detection.md)
