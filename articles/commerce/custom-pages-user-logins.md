---
title: Konfigurere brugerdefinerede sider til brugerlogon
description: Dette emne beskriver, hvordan du bygger tilpassede sider i Microsoft Dynamics 365 Commerce, der håndterer tilpasset logon for brugere af Azure Active Directory (Azure AD) Business-to-Consumer-lejere (B2C).
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f4a3c7c3410a903ae7bc0bac27e861a0dbfa19fdd65761628549c403c4e5db16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723257"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>Konfigurere brugerdefinerede sider til brugerlogon

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du bygger tilpassede sider i Microsoft Dynamics 365 Commerce, der håndterer tilpasset logon for brugere af Azure Active Directory (Azure AD) Business-to-Consumer-lejere (B2C).

Hvis du vil bruge brugerdefinerede sider, der er oprettet i Dynamics 365 Commerce, til at håndtere brugerlogon, skal du konfigurere de Azure AD-politikker, der skal refereres til i Commerce-miljøet. Du kan konfigurere Azure AD B2C-politikkerne "Tilmelding og logon", "Profilredigering" og "Nulstilling af adgangskode" ved hjælp af Azure AD B2C-programmet. Der kan derefter refereres til Azure AD B2C-lejeren og politiknavne under den klargørings proces, der udføres for Commerce-miljøet ved hjælp af Microsoft Dynamics Lifecycle Services (LCS).

De brugerdefinerede Commerce-sider kan opbygges ved hjælp af modulet til logon, tilmelding, kontoprofilredigering, nulstilling af adgangskode eller generiske AAD-moduler. De URL-adresser til sider, der udgives for disse brugerdefinerede sider, skal derefter refereres i Azure AD B2C-politikkonfigurationerne i Azure-portalen.

> [!WARNING] 
> Azure AD B2C gør gamle (ældre) brugerflow forældet inden 1. august 2021. Derfor skal du planlægge at overføre dine brugerflow til den nye anbefalede version. Den nye version indeholder funktionsparitet og nye funktioner. Du kan finde flere oplysninger i [Brugerflow i Azure Active Directory B2C](/azure/active-directory-b2c/user-flow-overview).

>Modulbiblioteket til Commerce version 10.0.15 eller derover skal bruges sammen med de anbefalede B2C-brugerflow. De standardbrugerpolitiksider, der tilbydes i Azure AD B2C, kan også bruges og giver mulighed for ekstra ændringer i baggrundsbillede, logo og baggrundsfarve, der er relateret til firmabranding. Selvom de er mere begrænsede i designegenskaber, indeholder standardbrugerpolitiksider Azure AD B2C-politikfunktionaliteten uden at oprette og konfigurere dedikerede brugerdefinerede sider. 

## <a name="set-up-b2c-policies"></a>Konfigurere B2C-politikker

Når du har konfigureret din Azure AD B2C-lejer og har knyttet den til Commerce-miljøet, skal du gå siden **Azure AD B2C** i Azure-portalen og derefter vælge **Brugerstrømme (politikker)** i menuen under **Politikker**.

![Kommandoen Brugerstrømme (politikker) i menuen.](./media/B2C_CustomPage_PoliciesMenu.png)

Du kan nu konfigurere brugerlogonstrømmene "Tilmelding og logon", "Profilredigering" og "Nulstilling af adgangskode".

### <a name="configure-the-sign-up-and-sign-in-policy"></a>Konfigurere politikken "Tilmelding og logon"

For at konfigurere politikken "Tilmelding og logon" skal du udføre følgende trin.

1. Vælg **Nyt brugerflow**, vælg **Tilmelding og logon**, vælg fanen **Anbefalet** og vælg derefter **Opret**.
1. Angiv et navn til politikken (f.eks. **B2C\_1\_TilmeldingLogon**).
1. Vælg de id-udbydere, der skal bruges til politikken, i sektionen **Identitetsudbydere**. Du skal som minimum vælge **E-mailtilmelding**.
1. I kolonnen **Indsaml attribut** skal du markere afkrydsningsfelterne for **E-mailadresse**, **Tildelt navn** og **Efternavn**.
1. I kolonnen **Returkrav** skal du markere afkrydsningsfelterne **E-mailadresser**, **Tildelt navn**, **Identitetsudbyder**, **Efternavn** og **Brugerens objekt-id**.

    ![Valgte attributter og krav.](./media/B2C_SignInSignUp_Attributes.png)

1. Vælg **OK** for at oprette politikken.
1. Dobbeltklik på navnet på den nye politik, og vælg derefter **Egenskaber** i navigationsruden.
1. Vælg **Til** i indstillingen **Aktivér JavaScript-valg af sidelayout (eksempel)**.

    ![Siden Egenskaber for den nye politik.](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> Der bliver refereret til hele politiknavnet i Commerce-miljøet. (**B2C\_1\_**-præfikset bliver medtaget i referencen). Politikker kan ikke omdøbes, når de først er oprettet. Hvis du erstatter en eksisterende politik for Commerce-miljøet, kan du slette den oprindelige politik og oprette en ny politik med samme navn. Hvis miljøet allerede er blevet klargjort, kan du også sende det nye politiknavn via en serviceanmodning.

Du skal vende tilbage til denne politik for at afslutte installationen, når du har opbygget de brugerdefinerede sider. Du skal nu lukke politikken for at vende tilbage til siden **Brugerstrømme (politikker)** i Azure-portalen.

### <a name="configure-the-profile-editing-policy"></a>Konfigurere politikken "Profilredigering"

Du kan konfigurere politikken "Profilredigering" ved at følge disse trin.

1. Vælg **Nyt brugerflow**, vælg **Profilredigering**, vælg fanen **Anbefalet**, og vælg derefter **Opret**.
1. Angiv et navn til politikken (f.eks. **B2C\_1\_RedigerProfil**).
1. Vælg de id-udbydere, der skal bruges til politikken, i sektionen **Identitetsudbydere**. Der skal som minimum være valgt **Log på lokal konto**.
1. I kolonnen **Indsaml attribut** skal du markere afkrydsningsfelterne for **Fornavn** og **Efternavn**.
1. I kolonnen **Returkrav** skal du markere afkrydsningsfelterne **E-mailadresser**, **Tildelt navn**, **Identitetsudbyder**, **Efternavn** og **Brugerens objekt-id**.
1. Vælg **OK** for at oprette politikken.
1. Dobbeltklik på navnet på den nye politik, og vælg derefter **Egenskaber** i navigationsruden.
1. Vælg **Til** i indstillingen **Aktivér JavaScript-valg af sidelayout (eksempel)**.

Du skal vende tilbage til denne politik for at afslutte installationen, når du har opbygget de brugerdefinerede sider. Du skal nu lukke politikken for at vende tilbage til siden **Brugerstrømme (politikker)** i Azure-portalen.

### <a name="configure-the-password-reset-policy"></a>Konfigurere politikken "Nulstilling af adgangskode"

Du kan konfigurere politikken "Nulstilling af adgangskode" ved at følge disse trin.

1. Vælg **Nyt brugerflow**, og vælg derefter indstillingen **Nulstil adgangskode**, og vælg fanen **Anbefalet**, og klik på **Opret**.
1. Angiv et navn til politikken (f.eks. **B2C\_1\_GlemtAdgangskode**).
1. Vælg **Nulstil adgangskode ved hjælp af e-mailadresse** i sektionen **Identitetsudbydere**.
1. I kolonnen **Returkrav** skal du markere afkrydsningsfelterne **E-mailadresser**, **Tildelt navn**, **Efternavn** og **Brugerens objekt-id**.
1. Vælg **OK** for at oprette politikken.
1. Dobbeltklik på navnet på den nye politik, og vælg derefter **Egenskaber** i navigationsruden.
1. Vælg **Til** i indstillingen **Aktivér JavaScript-valg af sidelayout (eksempel)**.

Du skal vende tilbage til denne politik for at afslutte installationen, når du har opbygget de brugerdefinerede sider. Du skal nu lukke politikken for at vende tilbage til siden **Brugerstrømme (politikker)** i Azure-portalen.

## <a name="build-the-custom-pages"></a>Oprette brugerdefinerede sider

Dedikerede Azure AD-moduler inkluderes i Commerce for at bygge brugerdefinerede sider til Azure AD B2C-brugerpolitikker. Sider kan opbygges specifikt til hver brugerpolitiksides layout ved hjælp af de Azure AD-hovedmoduler til B2C, der vises herunder. Du kan også bruge **Generisk AAD**-modul til alle sidelayout og politikker i Azure AD B2C (også for indstillinger af sidelayout i politikker, der ikke er vist nedenfor). 

- Sidespecifikke Azure AD-moduler er bundet til datainddata, der er gengivet af Azure AD B2C. Disse moduler giver dig mere kontrol over placeringen af elementerne på siderne. Der skal dog muligvis oprettes flere sider og moduludvidelser for at tage højde for afvigelser ud over de standardindstillinger, der er beskrevet nedenfor.
- I modulet **Generisk AAD** oprettes elementet "div" til Azure AD B2C, så alle elementer vises i siden med brugerpolitiksidelayout, hvilket giver mere fleksibilitet til sidens B2C-funktioner, men mindre styring af placeringen og typografien (men CSS kan bruges til at matche webstedets udseende).

Du kan oprette en enkelt side med **Generisk AAD**-modul og bruge det til alle dine brugerpolitiksider, eller du kan opbygge specifikke sider ved hjælp af de enkelte Azure AD-moduler til logon, tilmelding, profilredigering, nulstilling af adgangskode og bekræftelse af nulstilling af adgangskode. Du kan også bruge en blanding af begge ved hjælp af de specifikke Azure AD-sider for sidelayoutene, der er angivet nedenfor, og den generiske AAD-modulside til de resterende sidelayout i disse eller andre brugerpolitiksider.

Du kan få mere at vide om Azure AD-moduler, der leveres med modulbiblioteket, ved at læse mere på [Identificere styringssider og -moduler](identity-mgmt-modules.md).

Udfør følgende trin for at opbygge de brugerdefinerede sider med specifikke identitetsmoduler til håndtering af brugerlogon.

1. Naviger til dit websted i Commerce-webstedsgeneratoren.
1. Opbyg følgende fem skabeloner og sider (hvis de ikke allerede findes på dit websted):
    - En **Logon**-skabelon og -side, der bruger logonmodulet.
    - En **Tilmelding**-skabelon og -side, der bruger tilmeldingsmodulet.
    - En skabelon og side til **Nulstilling af adgangskod**, der bruger modulet til nulstilling af adgangskode.
    - En skabelon og side til **Bekræftelse af nulstilling af adgangskod**, der bruger modulet til bekræftelse af nulstilling af adgangskode.
    - En skabelon og side til **Profilredigering**, der bruger modulet til redigering af kontoprofilen.

Når du opbygger siderne, skal du følge disse retningslinjer:

- For hver side eller hvert modul skal du bruge det layout og den typografi, der passer bedst til dine forretningsbehov.
- Udgiv alle sider og URL-adresser, der skal bruges i Azure AD B2C-opsætningen.
- Når siderne og URL-adresserne er publiceret, skal du indsamle de URL-adresser, der skal bruges til konfigurationer af Azure AD B2C-politikken. Der føjes et **?preloadscripts=true**-suffiks til hver URL-adresse, når den bruges.

> [!IMPORTANT]
> Sider, der er opbygget til at blive refereret til i Azure AD B2C, serviceres direkte fra Azure AD B2C-lejerens domæne. Du må ikke genbruge universelle sidehoveder og sidefødder, der har relative links. Da disse sider findes på Azure AD B2C-domænet, når de bruges, bør der kun bruges absolutte URL-adresser til alle links. Det anbefales, at du opretter et bestemt sidehoved og en bestemt sidefod med absolutte URL-adresser til dine Azure AD-relaterede brugerdefinerede sider, hvor eventuelle Commerce-specifikke moduler, der kræver forbindelse til Retail Server, er fjernet. Favoritter, søgepanel, link til logon og indkøbsvognsmoduler skal f.eks. ikke medtages i de sider, der bruges i Azure AD B2C-brugerflow.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>Konfigurere Azure AD B2C-politikker med oplysninger om brugerdefinerede sider 

Gå tilbage til siden **Azure AD B2C** i Azure-portalen, og vælg derefter **Brugerstrømme (politikker)** i menuen under **Politikker**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>Opdatere politikken "Tilmelding og logon" med oplysninger om brugerdefinerede sider

Følg disse trin for at opdatere politikken "Tilmelding og logon" med oplysninger om brugerdefinerede sider.

1. Vælg **Sidelayout** i den **Tilmelding og logon**-politik, du har konfigureret tidligere, i navigationsruden.
1. Vælg layoutet **Side for samlet tilmelding eller logon**.
1. Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.
1. Angiv hele URL-adressen til logon i feltet **Brugerdefineret side-URI**. Medtag suffikset **?preloadscripts=true**. Angiv for eksempel ``www.<my domain>.com/sign-in?preloadscripts=true``.
1. Vælg version **2.1.0** eller senere (kræver modulbibliotek til Commerce version 10.0.15 eller højere) i feltet **Sidelayoutversion**.
1. Vælg **Gem**.
1. Vælg layoutet **Lokal kontotilmelding**.
1. Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.
1. Angiv hele URL-adressen til tilmelding i feltet **URL-adresse til brugerdefineret side**. Medtag suffikset **?preloadscripts=true**. Angiv for eksempel ``www.<my domain>.com/sign-up?preloadscripts=true``.
1. Vælg version **2.1.0** eller senere (kræver modulbibliotek til Commerce version 10.0.15 eller højere) i feltet **Sidelayoutversion**.
1. Benyt følgende fremgangsmåde i sektionen **Brugerattributter**:
    1. Vælg **Nej** i kolonnen **Kræver bekræftelse** for attributterne **Fornavn** og **Efternavn**.
    1. I forbindelse med **Mailadresse**-attributten anbefales det, at standardværdien **Ja** vælges i kolonnen **Kræver bekræftelse**. Denne indstilling sikrer, at brugere, der tilmelder sig med en bestemt mailadresse, kontrollerer, at de ejer mailadressen.
    1. Vælg **Nej** i kolonnen **Valgfri** for attributterne **Mailadresse**, **Fornavn** og **Efternavn**.
1. Vælg **Gem**.

    ![Konfiguration af politikken for tilmeldingssiden til en lokal konto.](./media/B2C_SignInSignUp_Recommended_PageLayoutExample.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>Opdatere politikken "Profilredigering" med oplysninger om brugerdefinerede sider

Følg disse trin for at opdatere politikken "Profilredigering" med oplysninger om brugerdefinerede sider.

1. Vælg **Sidelayout** i den **Profilredigering**-politik, du har konfigureret tidligere, i navigationsruden.
1. Vælg layoutet **Profilredigeringsside** (kan kræve, at du ruller ned over andre layoutindstillinger, afhængigt af skærmen).
1. Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.
1. Angiv hele URL-adressen til profilredigering i feltet **URL-adresse til brugerdefineret side**. Medtag suffikset **?preloadscripts=true**. Angiv for eksempel ``www.<my domain>.com/profile-edit?preloadscripts=true``.
1. Vælg version **2.1.0** eller højere (kræver modulbibliotek til Commerce version 10.0.15 eller højere) som **Sidelayoutversion**.
1. Benyt følgende fremgangsmåde i sektionen **Brugerattributter**:
    1. Vælg **Nej** i kolonnen **Valgfrit** for attributterne **Fornavn** og **Efternavn**.
    1. Vælg **Nej** i kolonnen **Kræver bekræftelse** for attributterne **Fornavn** og **Efternavn**.
1. Vælg **Gem**.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>Opdatere politikken "Nulstilling af adgangskode" med oplysninger om brugerdefinerede sider

Følg disse trin for at opdatere politikken "Nulstilling af adgangskode" med oplysninger om brugerdefinerede sider.

1. Vælg **Sidelayout** i den **Nulstilling af adgangskode**-politik, du har konfigureret tidligere, i navigationsruden.
1. Vælg layoutet **Side for glemt adgangskode**.
1. Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.
1. Angiv hele URL-adressen til verificering af nulstilling af kodeord i feltet **URL-adresse til brugerdefineret side**. Medtag suffikset **?preloadscripts=true**. Angiv for eksempel ``www.<my domain>.com/password-reset-verification?preloadscripts=true``.
1. Vælg version **2.1.0** eller højere (kræver modulbibliotek til Commerce version 10.0.15 eller højere) i feltet **Sidelayoutversion**.
2. Vælg **Gem**.
3. Vælg layoutet **Side for skift adgangskode**.
4. Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.
5. Angiv hele URL-adressen til nulstilling af kodeord i feltet **URL-adresse til brugerdefineret side**. Medtag suffikset **?preloadscripts=true**. Angiv for eksempel ``www.<my domain>.com/password-reset?preloadscripts=true``.
6. Vælg version **2.1.0** eller højere (kræver modulbibliotek til Commerce version 10.0.15 eller højere) i feltet **Sidelayoutversion**.
7. Vælg **Gem**.

## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Tilpasse standardtekststrenge for etiketter og beskrivelser

I modulbiblioteket er logonmoduler udfyldt på forhånd med standardtekststrenge til etiketter og beskrivelser. Du kan tilpasse strengene i egenskabsruden for det modul, du arbejder på. Yderligere strenge på siden (f.eks. linkteksten **Har du glemt adgangskoden?** eller tekst til handlingen **Opret en konto**) kræver brug af Commerce SDK (Software Development Kit) og opdatering af værdierne i filen globale.json for tilmeldingsmodulet.

Standardteksten for linket til den glemte adgangskode er f.eks. **Har du glemt adgangskoden?**. I det følgende vises denne standardtekst på logonsiden.

![Standardtekst for linket til glemt adgangskode på logonsiden.](./media/B2C_SignUp_ModuleFace.png)

Du kan dog redigere teksten til **Har du glemt adgangskoden?** i filen global.json til modulbibliotekets logonmodul, som vist i følgende illustration.

![Linkteksten opdateret i logonmodulets global.json-fil.](./media/B2C_CustomizingStringsForModule.png)

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]