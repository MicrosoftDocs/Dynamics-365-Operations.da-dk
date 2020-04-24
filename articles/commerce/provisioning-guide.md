---
title: Klargøre et Dynamics 365 Commerce-prøveversionsmiljø
description: I dette emne beskrives det, hvordan du klargør et Microsoft Dynamics 365 Commerce-prøveversionsmiljø.
author: psimolin
manager: annbe
ms.date: 04/10/2020
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
ms.openlocfilehash: d54db89372a0f9ef5b267d25e14067e3243a803c
ms.sourcegitcommit: 4254acb3cf8c6299fc2f3818ea6c499f058320d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/09/2020
ms.locfileid: "3254742"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a>Klargøre et Dynamics 365 Commerce-prøveversionsmiljø


[!include [banner](includes/banner.md)]

I dette emne beskrives det, hvordan du klargør et Dynamics 365 Commerce-prøveversionsmiljø.

Før du går i gang, anbefales det, at du hurtigt gennemgår dette emne for at få et indtryk af, hvad processen kræver.

> [!NOTE]
> Hvis du endnu ikke har fået adgang til Dynamics 365 Commerce-prøveversionen, kan du anmode om adgang fra [Dynamics 365 Commerce-webstedet](https://aka.ms/Dynamics365CommerceWebsite).

## <a name="overview"></a>Oversigt

Hvis du vil kunne klargør dit Commerce-prøveversionsmiljø, skal du oprette et projekt, der har et bestemt produktnavn og er en bestemt type. Miljøet og Commerce Scale Unit (CSU) har nogle specifikke parametre, du skal bruge, når du senere klargør dit e-Commerce. Instruktionerne i dette emne beskriver alle de påkrævede trin for klargøring og de parametre, du skal bruge.

Nå du har klargjort dit Commerce-prøveversionsmiljø, skal du fuldføre nogle få efter-klargørings-trin, for at gøre dit prøveversionsmiljø klar. Nogle trin er valgfrie, afhængigt af de aspekter af systemet, du vil evaluere. Du kan altid udføre de valgfrie trin senere.

For yderligere oplysninger om, hvordan du konfigurerer dit Commerce-prøveversionsmiljø, efter du har klargjort det, se [Konfigurering af et Commerce-prøveversionsmiljø](cpe-post-provisioning.md). For yderligere oplysninger om, hvordan du konfigurerer valgfrie funktioner til dit Commerce-prøveversionsmiljø, se [Konfiguration af valgfrie funktioner til et Commerce-prøveversionsmiljø](cpe-optional-features.md).

Hvis du har spørgsmål til klargøringstrinnene, eller du oplever problemer, bedes du fortælle det til Microsoft i [Microsoft Dynamics 365 Commerce-prøveversionens-Yammer-gruppen](https://aka.ms/Dynamics365CommercePreviewYammer).

## <a name="prerequisites"></a>Forudsætninger

Følgende forudsætninger skal være på plads, før du kan klargør dit Commerce-prøveversionsmiljø:

- Du har adgang til Microsoft Dynamics Lifecycle Services-portalen (LCS).
- Du er en eksisterende Microsoft Dynamics 365-partner eller -kunde og kan oprette et Dynamics 365 Commerce-projekt.
- Du er blevet godkendt til Dynamics 365 Commerce-prøveversionsprogrammet.
- Du har de nødvendige rettigheder til at oprette et projekt til **Overflyt, opret løsninger, og lær at bruge**.
- Du er medlem af rollen **Miljøadministrator** eller **Projektejer** i det projekt, hvor du skal klargøre miljøet.
- Du har administratoradgang til dit Microsoft Azure-abonnement eller du er i kontakt med en abonnementsadministrator, der kan fuldføre de to trin, der kræver administratorrettigheder, på dine vegne.
- Du har dit Azure Active Directory-lejer-ID (Azure AD) ved hånden.
- Du har oprettet en Azure AD-sikkerhedsgruppe, der kan bruges som en systemadministratorgruppe til e-Commerce, og du har gruppens ID ved hånden.
- Du har oprettet en Azure AD-sikkerhedsgruppe, der kan bruges som en gruppe for redaktører af vurderinger og anmeldelser, og du har gruppens ID ved hånden. (Denne sikkerhedsgruppe kan være den samme som e-Commerce-systemadministratorgruppen.)

## <a name="provision-your-commerce-preview-environment"></a>Klargøring af dit Commerce-prøveversionsmiljø

Disse procedurer forklarer, hvordan du klargør et Commerce-prøveversionsmiljø. Når du har fuldført dem, vil Commerce-prøveversionsmiljøet være klar til konfiguration. Alle de aktiviteter, der er beskrevet her, finder sted på LCS-portalen.

> [!IMPORTANT]
> Forhåndsadgang er knyttet til den LCS-konto og -organisation, som du angav i Commerce-prøveversionsansøgningen. Du skal bruge den samme konto til at klargøre Commerce-prøveversionmiljøet. Hvis du skal bruge en anden LCS-konto eller -lejer til Commerce-prøveversionsmiljøet, skal du oplyse Microsoft herom. Du finder kontaktoplysninger i afsnittet [Support til Commerce-prøveversionmiljøet](#commerce-preview-environment-support) senere i dette emne.

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
> Du behøver måske ikke at fuldføre trin 6, 7 og/eller 8, fordi sider, der har en enkelt indstilling, springes over. Når du er i visningen **Miljøparametre**, skal du bekræfte, at teksten **Dynamics 365 Commerce - Demo (10.0.* x* med platformsopdatering *xx*)** vises direkte over feltet **Miljønavn**. Se detaljer på den illustration, der vises efter trin 8.

1. Vælg **Skybaserede miljøer** øverst i menuen.
1. Vælg **Tilføj** for at tilføje et miljø.
1. Vælg den seneste version i feltet **Programversion**. Hvis du har et specifikt behov for at vælge en anden programversion end den seneste version, skal du ikke vælge en version før **10.0.8**.
1. I feltet **Platformsversion** skal du bruge den platformsversion, der automatisk vælges for den programversion, du har valgt. 

    ![Valg af program- og platformsversioner](./media/project1.png)

1. Vælg **Næste**.
1. Vælg **Demo** miljøtopologi.

    ![Valg af miljøtopologi 1](./media/project2.png)

1. Vælg **Dynamics 365 Commerce - Demo** som miljøtopologi. Hvis du har konfigureret en enkelt Azure Connector tidligere, bruges denne til dette miljø. Hvis du har konfigureret flere Azure Connector'er, kan du vælge, hvilken connector der skal bruges: **Det østlige USA**, **Det østlige USA 2**, **Det vestlige USA** eller **Det vestlige USA 2**. (For at opnå den bedste altomfattende præstation anbefaler vi, at du vælger **Det vestlige USA 2**.)

    ![Valg af miljøtopologi 2](./media/project3.png)

1. Angiv et miljønavn på side **Installer miljø**. Lad de avancerede indstillinger være, som de er.

    ![Siden Installer miljø](./media/project4.png)

1. Juster VM-størrelsen efter behov. (Vi anbefaler, at VM-lagerenheden \[SKU\] **D13 V2**.)
1. Gennemgå prissætnings- og licensvilkårene, og markér derefter afkrydsningsfeltet for at angive, at du accepterer dem.
1. Vælg **Næste**.
1. Klik på **Installer** på siden til bekræftelse af installationen, når du har kontrolleret, at oplysningerne er korrekte. Du bliver sendt tilbage til visningen **Skybaserede miljøer**, og dit miljø skulle stå på listen.

    Det miljø, du har anmodet om, vil blive vist i køen og derefter som under installation. Det vil tage nogen tid at fuldføre miljø arbejdsgangene. Kom derfor tilbage efter ca. seks til ni timer.

1. Før du fortsætter, skal du kontrollere, at din statussen for dit miljø er **Installeret**.

### <a name="initialize-the-commerce-scale-unit-csu"></a>Initialisere Commerce Scale Unit (CSU)

Følg disse trin for at påbegynde CSU.

1. Vælg dit miljø på listen i visningen **Skybaserede miljøer**.
1. Vælg **Alle detaljer** i miljøvisningen til højre. Visningen med miljødetaljer vises.
1. Under **Miljøfunktioner** skal du vælge **Administrer**.
1. På fanen **Commerce** skal du vælge **Initialiser**. CSU-initialiseringsparametrene bliver vist.
1. I feltet **Tegion** skal du vælge **Det østlige USA**, **Det østlige USA 2**, **Det vestlige USA** eller **Det vestlige USA 2**.
1. I feltet **Version** skal du vælge **Angiv en Version** på listen og derefter angive **9.18.20014.4** i det felt, der vises. Sørg for at angive den nøjagtige version, der er angivet her. Ellers skal du opdatere RCSU til den korrekte version senere.
1. Aktivér indstillingen **Anvend udvidelse**.
1. Vælg **Demobasisudvidelse til Commerce-prøveversion** på listen over udvidelser.
1. Vælg **Initialiser**.
1. Klik på **Ja** på siden til bekræftelse af installationen, når du har kontrolleret, at oplysningerne er korrekte. Visningen **Commerce-administration** vises igen, hvor fanen **Commerce** er valgt. Din CSU er sat i kø til klargøring.
1. Før du fortsætter, skal du kontrollere, at din statussen for dit CSU er **Vellykket**. Initialiseringen tager ca. to til fem timer.

### <a name="initialize-e-commerce"></a>Initialisere e-handel

Følg disse trin for at påbegynde e-Commerce.

1. Under fanen **e-Commerce** skal du gennemgå samtykket for prøveversionen og derefter vælge **Konfiguration**.
1. Angiv et navn for **e-Commerce-lejernavn** i feltet. Bemærk dog, at navnet vil være synligt i nogle af URL-adresserne, der peger på din e-Commerce-forekomst.
1. I feltet **Commerce scale unit-navn** skal du vælge din CSU på listen. (Listen bør kun have én indstilling.)

    Feltet **e-Commerce-geografi** angives automatisk, og værdien kan ikke ændres.

1. Vælg **Næste** for at fortsætte.
1. I feltet **Understøttede værtsnavne** skal du angive et vilkårligt gyldigt domæne som f.eks. `www.fabrikam.com`.
1.  I feltet **AAD-sikkerhedsgruppe for systemadministrator** skal du angive de første få bogstaver i navnet på den sikkerhedsgruppe, som du ønsker at bruge. Vælg ikonet for forstørrelsesglasset for at få vist søgeresultaterne. Vælg den korrekte sikkerhedsgruppe på listen.
2.  I feltet **AAD-sikkerhedsgruppen for redaktører for vurderinger og anmeldelser** skal du angive de første få bogstaver i navnet på den sikkerhedsgruppe, som du ønsker at bruge. Vælg ikonet for forstørrelsesglasset for at få vist søgeresultaterne. Vælg den korrekte sikkerhedsgruppe på listen.
1. Lad indstillingen **Aktivér tjenesten vurderinger og anmeldelser** være aktiveret.
1. Vælg **Initialiser**. Visningen **Commerce-administration** vises igen, hvor fanen **e-Commerce** er valgt. Din initialisering af e-Commerce er påbegyndt.
1. Før du fortsætter, skal du vente, indtil initialiseringsstatus for din e-Commerce er **Initialisering blev gennemført**.
1. Under **Links** nederst til højre skal du notere URL-adresserne for følgende links:

    * **e-Commerce-websted** – linket til roden af dit e-Commerce-websted.
    * **Værktøj til administration af e-Commerce-websted** – linket til administrationsværktøjet for webstedet.

## <a name="commerce-preview-environment-support"></a>Support til Commerce-prøveversionsmiljøet

Hvis der opstår problemer under din fuldførelse af klargøringstrinnene, kan du gå til [Microsoft Dynamics 365 Commerce-prøveversionens Yammer-gruppe](https://aka.ms/Dynamics365CommercePreviewYammer) for at få hjælp.

## <a name="next-steps"></a>Næste trin

For at fortsætte processen med klargøring og konfigurering af dit Commerce-prøveversionsmiljø se [Konfigurering af et Commerce-prøveversionsmiljø](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over Dynamics 365 Commerce-prøveversionsmiljø](cpe-overview.md)

[Konfigurere et Dynamics 365 Commerce-prøveversionsmiljø](cpe-post-provisioning.md)

[Konfigurere valgfrie funktioner for et Dynamics 365 Commerce-prøveversionsmiljø](cpe-optional-features.md)

[Ofte stillede spørgsmål om Dynamics 365 Commerce-prøveversionsmiljø](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-websted](https://aka.ms/Dynamics365CommerceWebsite)

