---
title: Klargøring af et Commerce-prøveversionsmiljø
description: I dette emne beskrives det, hvordan du klargør et Microsoft Dynamics 365 Commerce-prøveversionsmiljø.
author: psimolin
manager: annbe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934742"
---
# <a name="provision-a-commerce-preview-environment"></a>Klargøring af et Commerce-prøveversionsmiljø

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

I dette emne beskrives det, hvordan du klargør et Microsoft Dynamics 365 Commerce-prøveversionsmiljø.

Før du går i gang, anbefales det, at du som minimum skimmer hele dette emne igennem for at få en ide om, hvad processen indebærer, og hvad dette emne indeholder.

> [!NOTE]
> Hvis du endnu ikke har fået adgang til Dynamics 365 Commerce-prøveversionen, kan du anmode om adgang fra [Commerce-webstedet](https://aka.ms/Dynamics365CommerceWebsite).

## <a name="overview"></a>Oversigt

Hvis du vil kunne klargør dit Commerce-prøveversionsmiljø, skal du oprette et projekt, der har et bestemt produktnavn og er en bestemt type. Miljøet og Retail Cloud Scale Unit (RCSU) har nogle specifikke parametre, du skal bruge, når du senere klargør dit e-Commerce. Instruktionerne i dette emne beskriver alle de påkrævede trin, du skal fuldføre, og de parametre, du skal bruge.

Nå du har klargjort dit Commerce-prøveversionsmiljø, skal du fuldføre nogle få efter-klargørings-trin, for at gøre dit prøveversionsmiljø klar. Nogle trin er valgfrie, afhængigt af de aspekter af systemet, du vil evaluere. Du kan altid udføre de valgfrie trin senere.

For yderligere oplysninger om, hvordan du konfigurerer dit Commerce-prøveversionsmiljø, efter du har klargjort det, se [Konfigurering af et Commerce-prøveversionsmiljø](cpe-post-provisioning.md). For yderligere oplysninger om, hvordan du konfigurerer valgfrie funktioner til dit Commerce-prøveversionsmiljø, se [Konfiguration af valgfrie funktioner til et Commerce-prøveversionsmiljø](cpe-optional-features.md).

Hvis du har spørgsmål til klargøringstrinnene, eller du oplever problemer, bedes du fortælle det til Microsoft i [Microsoft Dynamics 365 Commerce-prøveversionens-Yammer-gruppen](https://aka.ms/Dynamics365CommercePreviewYammer).

## <a name="prerequisites"></a>Forudsætninger

Følgende forudsætninger skal være på plads, før du kan klargør dit Commerce-prøveversionsmiljø:

- Du har adgang til Microsoft Dynamics Lifecycle Services-portalen (LCS).
- Du er blevet godkendt til Dynamics 365 Commerce-prøveversionsprogrammet.
- Du har de nødvendige rettigheder til at oprette et projekt til **Mulige førsalg** eller **Overflyt, opret løsninger, og lær at bruge**.
- Du er medlem af rollen **Miljøadministrator** eller **Projektejer** i det projekt, hvor du skal klargøre miljøet.
- Du har administratoradgang til dit Microsoft Azure-abonnement eller du er i kontakt med en abonnementsadministrator, der kan fuldføre de to trin, der kræver administratorrettigheder, på dine vegne.
- Du har dit Azure Active Directory-lejer-ID (Azure AD) ved hånden.
- Du har oprettet en Azure AD-sikkerhedsgruppe, der kan bruges som en systemadministratorgruppe til e-Commerce, og du har gruppens ID ved hånden.
- Du har oprettet en Azure AD-sikkerhedsgruppe, der kan bruges som en gruppe for redaktører af vurderinger og anmeldelser, og du har gruppens ID ved hånden. (Denne sikkerhedsgruppe kan være den samme som e-Commerce-systemadministratorgruppen.)

### <a name="find-your-azure-ad-tenant-id"></a>Find dit Azure AD-lejer-ID

Dit Azure AD-lejer-ID er en global entydig identifikator (GUID), der ligner dette eksempel: **72f988bf-86f1-41af-91ab-2d7cd011db47**.

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a>Find dit Azure AD-lejer-ID ved hjælp af Azure-portalen

1. Log på [Azure-portalen](https://portal.azure.com/).
1. Sørg for, at det korrekte bibliotek er valgt.
1. Vælg **Azure Active Directory** i menuen til venstre.
1. Under **Administrer** skal du vælge **Egenskaber**. Dit Azure AD-lejer-ID vises under **Mappe-ID**.

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a>Find dit Azure AD-lejer-ID ved hjælp af OpenID Connect-metadata

Opret en OpenID-URL-adresse ved at erstatte **\{DIT\_DOMÆNE\}** med dit domæne, som eksemeplvis `microsoft.com`. For eksempel `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` bliver til `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.

1. Gå til den OpenID-URL-adresse, der indeholder dit domæne.

    Du kan finde dit Azure AD-lejer-ID i flere egenskabsværdier.

1. Find **godkendelse\_slutpunkt**, og udpak det GUID, der vises umiddelbart efter `login.microsoftonline.com/`.

### <a name="find-your-azure-ad-security-group-id"></a>Find dit Azure AD-sikkerhedsgruppe-ID

ID'et for din Azure AD-sikkerhedsgruppe er et GUID, der ligner dette eksempel: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.

I denne procedure antages det, at du er medlem af den gruppe, du forsøger at finde ID'et for.

1. Åbn [Graf-stifinder](https://developer.microsoft.com/graph/graph-explorer#).
1. Vælg **Log på med Microsoft**, og log på ved hjælp af dine legitimationsoplysninger.
1. Vælg **vis flere eksempler** til venstre.
1. Aktivér **Grupper** i højre rude.
1. Luk den højre rude.
1. Vælg **alle grupper, som jeg tilhører**.
1. Find din gruppe i feltet **Forhåndsvisning af svar**. Sikkerhedsgruppe-ID'et vises under **ID**-egenskaben.

## <a name="provision-your-commerce-preview-environment"></a>Klargøring af dit Commerce-prøveversionsmiljø

Disse procedurer forklarer, hvordan du klargør et Commerce-prøveversionsmiljø. Når du har fuldført dem, vil Commerce-prøveversionsmiljøet være klar til konfiguration. Alle de aktiviteter, der er beskrevet her, finder sted på LCS-portalen.

> [!IMPORTANT]
> Forhåndsadgang er knyttet til den LCS-konto og -organisation, som du angav i prøveversionsansøgning. Du skal bruge den samme konto til at klargøre Commerce-prøveversionmiljøet. Hvis du skal bruge en anden LCS-konto eller -lejer til Commerce-prøveversionmiljøet, skal du oplyse Microsoft herom. Du finder kontaktoplysninger i afsnittet [Support til Commerce-prøveversionmiljøet](#commerce-preview-environment-support) senere i dette emne.

### <a name="grant-access-to-e-commerce-applications"></a>Give adgang til e-handelsprogrammer

> [!IMPORTANT]
> Den person, der logger på, skal være en Azure AD-lejeradministrator, som har Azure AD-lejer-ID'et. Hvis dette trin ikke er fuldført, vil de resterende klargøringstrin mislykkes.

Følg disse trin for at autorisere e-Commerce-programmer til at få adgang til dit Azure-abonnement.

1. Sammensæt en URL-adresse i følgende format:

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. Kopiér og Indsæt URL-adressen i din browser eller teksteditor, og erstat **\{AAD\_LEJER\_-ID\}** med dit Azure AD-lejer-ID. Åbn dernæst URL-adressen.
1. Log på Azure AD i dialogboksen for logon, og bekræft, at du vil give **Dynamics 365 Commerce (prøveversion)** adgang til dit abonnement. Du bliver sendt videre til en side, der indikerer, om handlingen lykkedes.

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a>Bekræft, at prøveversionens funktioner er tilgængelige og aktiverede i LCS

For at bekræfte, at prøveversionens funktioner er tilgængelige og aktiverede i LCS, skal du gøre følgende:

1. Log på [LCS-portalen](https://lcs.dynamics.com) ved at bruge den samme LCS-konto, som du brugte til at anmode om adgang til prøveversionen.
1. Rul helt til højre på LCS-startsiden, og vælg feltet **Styring af prøveversionsfunktion**.

    ![Feltet Styring af prøveversionsfunktion](./media/preview1.png)

1. Rul ned til **Funktioner i private prøveversioner**, bekræft, at følgende funktioner er tilgængelige og aktiverede:

    - Evaluering af e-handel
    - Programmiljøer til Commerce-prøveversion

    ![Funktioner i private prøveversioner](./media/preview2.png)

1. Hvis disse funktioner ikke vises på listen, skal du kontakte Microsoft og angive din arbejdsmailadresse, LCS-konto og lejeroplysninger. Du finder kontaktoplysninger i afsnittet [Support til Commerce-prøveversionmiljøet](#commerce-preview-environment-support).

### <a name="create-a-new-project"></a>Opret et nyt projekt

Hvis du vil oprette et nyt projekt i LCS, skal du følge disse trin.

1. På LCS-startsiden skal du vælge plustegnet (**+**) for at oprette et projekt.
1. Benyt en af følgende fremgangsmåder i højre rude:

    - Hvis du er en partner, skal du vælge **Overflyt, opret løsninger, og lær at bruge**.
    - Hvis du er en kunde, skal du vælge **Mulige førsalg**.

1. Angiv et navn, beskrivelse og branche.
1. I feltet **Produktnavn** skal du vælge **Dynamics 365 Retail**.
1. I feltet **Produktversion** skal du vælge **Dynamics 365 Retail**.
1. I feltet **Metode** skal du vælge **Dynamics Retail-implementeringsmetode**.
1. Valgfrit: Du kan importere roller og brugere fra et eksisterende projekt.
1. Vælg **Opret**. Projektoversigten vises.

### <a name="add-the-azure-connector"></a>Tilføj Azure Connector

Hvis du vil tilføje Azure Connector til dit LCS-projekt, skal du følge disse trin.

1. Udfør ét af følgende trin:

    - Hvis du er en partner, skal du vælge feltet **Projektindstillinger** længst til højre.
    - Hvis du er en kunde, skal du vælge **Projektindstillinger** i den øverste menu.

1. Vælg **Azure-connectorer**.
1. Vælg **Tilføj** for at tilføje Azure Connector'en.
1. Skriv et navn.
1. Angiv dit Azure-abonnements-ID.
1. Aktiver indstillingen **Konfigurer til at bruge Azure Resource Manager (ARM)**.
1. Kontrollér, at værdien **Azure-abonnement AAD-lejerdomæne (eller ID)** er korrekt. Kontakt om nødvendigt din Azure-abonnementsadministrator.
1. Vælg **Næste**.
1. Følg instruktionerne på siden for at give det eller de nødvendige programmer adgang til dit abonnement. Kontakt om nødvendigt din Azure-abonnementsadministrator.

    1. Log på [Azure-portalen](https://portal.azure.com/).
    1. Sørg for, at den korrekte mappe er valgt, og vælg derefter **Abonnementer** i menuen til venstre.
    1. Find det korrekte abonnement på listen, og vælg det. Brug søgefunktionen efter behov.
    1. Vælg **Adgangskontrol (IAM)** i menuen.
    1. Til højre under **Tilføj en rolletildeling** skal du vælge **Tilføj**. Ruden **Tilføj rolletildeling** vises.
    1. I feltet **Rolle** skal du vælge **Bidragsyder**.
    1. I feltet **Tildel adgang** skal du lade standardværdien for **Azure AD-bruger, gruppe eller tjenesteprincipal** være.
    1. Under **Vælg** skal du angive **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.
    1. Vælg **Dynamics-installationstjenester \[wsfed-enabled\]** på listen.
    1. Vælg **Gem**.

1. Vælg **Næste**.
1. Følg instruktionerne på siden for at give det eller de nødvendige programmer adgang til dit abonnement. Kontakt om nødvendigt din Azure-abonnementsadministrator.
1. Vælg **Næste**.
1. I feltet **Azure-region** skal du vælge **Det østlige USA**, **Det østlige USA 2**, **Det vestlige USA** eller **Det vestlige USA 2**.
1. Vælg **Forbind**. Din Azure-connector bør blive vist på listen.

### <a name="import-the-commerce-preview-demo-base-extension"></a>Importer Demobasisudvidelse til Commerce-prøveversion

Følg disse trin for at importere Demobasisudvidelse til Commerce-prøveversion i projektet.

1. Åbn startsiden for dit projekt ved at vælge projektets navn øverst.
1. Udfør ét af følgende trin:

    - Hvis du er en partner, skal du vælge feltet **Aktivbibliotek** længst til højre.
    - Hvis du er en kunde, skal du vælge **Aktivbibliotek** i den øverste menu.

1. Vælg **Installerbar softwarepakke** fra listen til venstre.
1. Vælg **Importér**.
1. Under **Delt aktivbibliotek** skal du vælge **Demobasisudvidelse til Commerce-prøveversion** fra aktivlisten.
1. Vælg **Pluk**. Du kommer tilbage til aktivbiblioteket, og du bør kunne se udvidelsen på listen.

I følgende illustration vises de handlinger, der skal udføres på LCS-siden **Aktivbibliotek**.

![Import af Demobasisudvidelse til Commerce-prøveversion](./media/import.png)

### <a name="deploy-the-environment"></a>Installer miljøet

Følg disse trin for at installere miljøet.

> [!NOTE]
> Du behøver måske ikke at fuldføre trin 6, 7 og/eller 8, fordi sider, der har en enkelt indstilling, springes over. Når du er i visningen **Miljøparametre**, skal du bekræfte, at teksten **Dynamics 365 Commerce (prøveversion) - Demo (10.0.6 med platformsopdatering 30)** vises direkte over feltet **Miljønavn**. Se den illustration, der vises efter trin 8.

1. Vælg **Skybaserede miljøer** øverst i menuen.
1. Vælg **Tilføj** for at tilføje et miljø.
1. I feltet **Programversion** skal du vælge **10.0.6**.
1. I feltet **Platformsversion** skal du vælge **Platformsopdatering 30**.

    ![Valg af program- og platformsversioner](./media/project1.png)

1. Vælg **Næste**.
1. Vælg **Demo** miljøtopologi.

    ![Valg af miljøtopologi 1](./media/project2.png)

1. Vælg **Dynamics 365 Commerce (prøveversion) - Demo** som miljøtopologi. Hvis du har konfigureret en enkelt Azure Connector tidligere, bruges denne til dette miljø. Hvis du har konfigureret flere Azure Connector'er, kan du vælge, hvilken connector der skal bruges: **Det østlige USA**, **Det østlige USA 2**, **Det vestlige USA** eller **Det vestlige USA 2**. (For at opnå den bedste altomfattende præstation anbefaler vi, at du vælger **Det vestlige USA 2**.)

    ![Valg af miljøtopologi 2](./media/project3.png)

1. Angiv et miljønavn på side **Installer miljø**. Lad de avancerede indstillinger være, som de er.

    ![Siden Installer miljø](./media/project4.png)

1. Juster VM-størrelsen efter behov. (Vi anbefaler, at VM-lagerenheden \[SKU\] **D13 V2**.)
1. Gennemgå prissætnings- og licensvilkårene, og markér derefter afkrydsningsfeltet for at angive, at du accepterer dem.
1. Vælg **Næste**.
1. Klik på **Installer** på siden til bekræftelse af installationen, når du har kontrolleret, at oplysningerne er korrekte. Du bliver sendt tilbage til visningen **Skybaserede miljøer**, og dit miljø skulle stå på listen.

    Det miljø, du har anmodet om, vil blive vist i køen og derefter som under installation. Det vil tage nogen tid at fuldføre miljø arbejdsgangene. Kom derfor tilbage efter ca. seks til ni timer.

1. Før du fortsætter, skal du kontrollere, at din statussen for dit miljø er **Installeret**.

### <a name="initialize-rcsu"></a>Initialisere RCSU

Følg disse trin for at påbegynde RCSU.

1. Vælg dit miljø på listen i visningen **Skybaserede miljøer**.
1. Vælg **Alle detaljer** i miljøvisningen til højre. Visningen med miljødetaljer vises.
1. Under **Miljøfunktioner** skal du vælge **Administrer**.
1. På fanen **Retail** skal du vælge **Initialiser**. RCSU-initialiseringsparametrene bliver vist.
1. I feltet **Tegion** skal du vælge **Det østlige USA**, **Det østlige USA 2**, **Det vestlige USA** eller **Det vestlige USA 2**.
1. I feltet **Version** skal du vælge **Angiv en Version** på listen og derefter angive **9.16.19262.5** i det felt, der vises. Sørg for at angive den nøjagtige version, der er angivet her. Ellers skal du opdatere RCSU til den korrekte version senere.
1. Aktivér indstillingen **Anvend udvidelse**.
1. Vælg **Demobasisudvidelse til Commerce-prøveversion** på listen over udvidelser.
1. Vælg **Initialiser**.
1. Klik på **Ja** på siden til bekræftelse af installationen, når du har kontrolleret, at oplysningerne er korrekte. Du returneres til visningen **Retail management**, hvor fanen **Retail** er valgt. Din RCSU er sat i kø til klargøring.
1. Før du fortsætter, skal du kontrollere, at din statussen for dit RCSU er **Vellykket**. Initialiseringen tager ca. to til fem timer.

### <a name="initialize-e-commerce"></a>Initialisere e-handel

Følg disse trin for at påbegynde e-Commerce.

1. Under fanen **e-Commerce (prøveversion)** skal du gennemgå samtykket for prøveversionen og derefter vælge **Opsætning**.
1. Angiv et navn for **e-Commerce-lejernavn** i feltet. Bemærk dog, at navnet vil være synligt i nogle af URL-adresserne, der peger på din e-Commerce-forekomst.
1. I feltet **Retail cloud scale unit-navn** skal du vælge din RCSU fra listen. (Listen bør kun have én indstilling.)

    Feltet **e-Commerce-geografi** angives automatisk, og værdien kan ikke ændres.

1. Vælg **Næste** for at fortsætte.
1. I feltet **Understøttede værtsnavne** skal du angive et vilkårligt gyldigt domæne som f.eks. `www.fabrikam.com`.
1.  I feltet **AAD-sikkerhedsgruppe for systemadministrator** skal du angive de første få bogstaver i navnet på den sikkerhedsgruppe, som du ønsker at bruge. Vælg ikonet for forstørrelsesglasset for at få vist søgeresultaterne. Vælg en sikkerhedsgruppe på listen.
2.  I feltet **AAD-sikkerhedsgruppen for redaktører for vurderinger og anmeldelser** skal du angive de første få bogstaver i navnet på den sikkerhedsgruppe, som du ønsker at bruge. Vælg ikonet for forstørrelsesglasset for at få vist søgeresultaterne. Vælg en sikkerhedsgruppe på listen.
1. Lad indstillingen **Aktivér tjenesten vurderinger og anmeldelser** være aktiveret.
1. Hvis du allerede har fuldført samtykketrinnet for Microsoft Azure Active Directory (Azure AD) som beskrevet i afsnittet "Tildel adgang til e-Commerce-programmer", skal du markere afkrydsningsfeltet for at bekræfte dit samtykke. Hvis du endnu ikke har fuldført dette trin, skal du gøre det, før du fortsætter initialiseringen. Marker hyperlinket i teksten ved siden af afkrydsningsfeltet for at åbne dialogboksen til samtykke og fuldføre trinnet.
1. Vælg **Initialiser**. Du bliver returneret til visningen **Detailstyring**, hvor fanen **e-Commerce (prøveversion)** er valgt. Din initialisering af e-Commerce er påbegyndt.
1. Før du fortsætter, skal du vente, indtil initialiseringsstatus for din e-Commerce er **Initialisering blev gennemført**.
1. Under **Links** nederst til højre skal du notere URL-adresserne for følgende links:

    * **e-Commerce-websted** – linket til roden af dit e-Commerce-websted.
    * **Værktøj til administration af e-Commerce-websted** – linket til administrationsværktøjet for webstedet.

## <a name="commerce-preview-environment-support"></a>Support til Commerce-prøveversionsmiljøet

Hvis der opstår problemer under din fuldførelse af klargøringstrinnene, kan du gå til [Microsoft Dynamics 365 Commerce-prøveversionens Yammer-gruppe](https://aka.ms/Dynamics365CommercePreviewYammer) for at få hjælp.

Hvis du oplever problemer, når du forsøger at få adgang til Yammer-gruppen, kan du kontakte Microsoft via e-mail på <Dynamics365Commerce@microsoft.com>. Denne e-mailadresse overvåges ikke aktivt. Du skal derfor regne med, at svaret vil blive forsinket.

## <a name="next-steps"></a>Næste trin

For at fortsætte processen med klargøring og konfigurering af dit Commerce-prøveversionsmiljø se [Konfigurering af et Commerce-prøveversionsmiljø](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over miljø til prøveversion af Commerce](cpe-overview.md)

[Konfigurering af et Commerce-prøveversionsmiljø](cpe-post-provisioning.md)

[Konfigurer valgfrie funktioner for et Commerce-prøveversionsmiljø](cpe-optional-features.md)

[Ofte stillede spørgsmål om Commerce-prøveversionsmiljø](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-websted](https://aka.ms/Dynamics365CommerceWebsite)

[Hjælp-ressourcer til Dynamics 365 Retail](../retail/index.md)
