---
title: Klargøre et Dynamics 365 Commerce-evalueringsmiljø
description: I dette emne beskrives det, hvordan du klargør et Microsoft Dynamics 365 Commerce-evalueringsmiljø.
author: psimolin
manager: annbe
ms.date: 11/05/2020
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
ms.openlocfilehash: b54216a565c264dfcfe821581fee9df7b5e22323
ms.sourcegitcommit: 715508547f9a71a89a138190e8540686556c753d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/05/2020
ms.locfileid: "4411235"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a>Klargøre et Dynamics 365 Commerce-evalueringsmiljø

[!include [banner](includes/banner.md)]

I dette emne beskrives det, hvordan du klargør et Microsoft Dynamics 365 Commerce-evalueringsmiljø.

Før du går i gang, anbefales det, at du hurtigt gennemgår dette emne for at få et indtryk af, hvad processen kræver.

> [!NOTE]
> Miljøer til Commerce-evaluering er ikke generelt tilgængelige og tildeles til partnere og kunder efter anmodning. Du kan få flere oplysninger ved at rette henvendelse til din kontakt hos din Microsoft-partner.

## <a name="overview"></a>Overblik

Hvis du vil kunne klargør et Commerce-evalueringsmiljø, skal du oprette et projekt, der har et bestemt produktnavn og er en bestemt type. Miljøet og Commerce Scale Unit (CSU) har nogle specifikke parametre, du skal bruge, når du forventer at klargøre dit e-Commerce. Instruktionerne i dette emne beskriver alle de påkrævede trin for klargøring og de parametre, du skal bruge.

Nå du har klargjort dit Commerce-evalueringsmiljø, skal du fuldføre nogle få efter-klargørings-trin, for at gøre dit evalueringsmiljø klar til brug. Nogle trin er valgfrie, afhængigt af de aspekter af systemet, du vil evaluere. Du kan altid udføre de valgfrie trin senere.

For yderligere oplysninger om, hvordan du konfigurerer dit Commerce-evalueringsmiljø, efter du har klargjort det, se [Konfigurere et Commerce-evalueringsmiljø](cpe-post-provisioning.md). For yderligere oplysninger om, hvordan du konfigurerer valgfrie funktioner til dit Commerce-evalueringsmiljø, se [Konfigurere valgfrie funktioner til et Commerce-evalueringsmiljø](cpe-optional-features.md).

## <a name="prerequisites"></a>Forudsætninger

Følgende forudsætninger skal være på plads, før du kan klargør dit Commerce-evalueringsmiljø:

- Du er registreret i evalueringsprogrammet og har fået tildelt kapacitet til et evalueringsmiljø.
- Du har adgang til Microsoft Dynamics Lifecycle Services-portalen (LCS).
- Du er en eksisterende Microsoft Dynamics 365-partner eller -kunde og kan oprette et Dynamics 365 Commerce-projekt.
- Du har administratoradgang til dit Microsoft Azure-abonnement, eller du er i kontakt med en abonnementsadministrator, der kan hjælpe dig, hvis det er nødvendigt.
- Du har dit Azure Active Directory-lejer-ID (Azure AD) ved hånden.
- Du har oprettet en Azure AD-sikkerhedsgruppe, der kan bruges som en systemadministratorgruppe til e-Commerce, og du har gruppens ID ved hånden.
- Du har oprettet en Azure AD-sikkerhedsgruppe, der kan bruges som en gruppe for redaktører af vurderinger og anmeldelser, og du har gruppens ID ved hånden. (Denne sikkerhedsgruppe kan være den samme som e-Commerce-systemadministratorgruppen.)

Bemærk, at denne liste ikke er udtømmende. Hvis du oplever nogen problemer, skal du rette henvendelse til din kontakt hos din Microsoft-partner for at få hjælp.

## <a name="provision-your-commerce-evaluation-environment"></a>Klargøre dit Commerce-evalueringsmiljø

Disse procedurer forklarer, hvordan du klargør et Commerce-evalueringsmiljø. Når du har fuldført dem, vil Commerce-evalueringsmiljøet være klar til konfiguration. Alle de aktiviteter, der er beskrevet her, finder sted på LCS-portalen.

### <a name="create-a-new-project"></a>Opret et nyt projekt

Hvis du vil oprette et nyt projekt i LCS, skal du følge disse trin.

1. På LCS-startsiden skal du vælge plustegnet (**+**) for at oprette et projekt.
1. Benyt en af følgende fremgangsmåder i højre rude:

    - Hvis du er en partner, skal du vælge **Overflyt, opret løsninger, og lær at bruge**.
    - Hvis du er en kunde, skal du vælge **Mulige førsalg**.

1. Angiv et navn, beskrivelse og branche.
1. I feltet **Produktnavn** skal du vælge **Dynamics 365 Commerce**.
1. I feltet **Produktversion** skal du vælge **Dynamics 365 Commerce**.
1. I feltet **Metode** skal du vælge **Dynamics Retail-implementeringsmetode**.
1. Valgfrit: Du kan importere roller og brugere fra et eksisterende projekt.
1. Vælg **Opret**. Projektoversigten vises.

### <a name="add-the-azure-connector"></a>Tilføj Azure Connector

Hvis du vil føje Azure Connector til dit LCS-projekt, skal du følge trinnene i [Fuldføre processen til onboarding af Azure Resource Manager (ARM)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).

### <a name="deploy-the-environment"></a>Installer miljøet

Følg disse trin for at installere miljøet.

> [!NOTE]
> Du behøver måske ikke at fuldføre trin 6, 7 og/eller 8, fordi sider, der har en enkelt indstilling, springes over. Når du er i visningen **Miljøparametre**, skal du bekræfte, at teksten **Dynamics 365 Commerce - Demo (10.0.* x* med platformsopdatering *xx*)** vises direkte over feltet **Miljønavn**. Se detaljer på den illustration, der vises efter trin 8.

1. Vælg **Skybaserede miljøer** øverst i menuen.
1. Vælg **Tilføj** for at tilføje et miljø.
1. Vælg den seneste version i feltet **Programversion**. Hvis du har et specifikt behov for at vælge en anden programversion end den seneste version, skal du ikke vælge en version før **10.0.14**.
1. I feltet **Platformsversion** skal du bruge den platformsversion, der automatisk vælges for den programversion, du har valgt. 

    ![Valg af program- og platformsversioner](./media/project1.png)

1. Vælg **Næste**.
1. Vælg **Demo** miljøtopologi.

    ![Valg af miljøtopologi 1](./media/project2.png)

1. Angiv et miljønavn på side **Installer miljø**. Lad de avancerede indstillinger være, som de er.

    ![Siden Installer miljø](./media/project4.png)

1. Juster VM-størrelsen efter behov. (Vi anbefaler, at VM-lagerenheden \[SKU\] **D13 V2**.)
1. Gennemgå prissætnings- og licensvilkårene, og markér derefter afkrydsningsfeltet for at angive, at du accepterer dem.
1. Vælg **Næste**.
1. Klik på **Installer** på siden til bekræftelse af installationen, når du har kontrolleret, at oplysningerne er korrekte. Du bliver sendt tilbage til visningen **Skybaserede miljøer**, og dit miljø skulle stå på listen.

    Det miljø, du har anmodet om, vil blive vist i køen og derefter som under installation. Det vil tage nogen tid at fuldføre miljø arbejdsgangene. Kom derfor tilbage efter ca. seks til ni timer.

1. Før du fortsætter, skal du kontrollere, at din statussen for dit miljø er **Installeret**.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Initialisere Commerce Scale Unit (sky)

Følg disse trin for at påbegynde CSU.

1. Vælg dit miljø på listen i visningen **Skybaserede miljøer**.
1. Vælg **Alle detaljer** i miljøvisningen til højre. Visningen med miljødetaljer vises.
1. Under **Miljøfunktioner** skal du vælge **Administrer**.
1. På fanen **Commerce** skal du vælge **Initialiser**. CSU-initialiseringsparametrene bliver vist.
1. I feltet **Område** skal du vælge det område, der er det samme eller tæt på det område, du har implementeret miljøet i.
1. Lad feltet **Version** være, som det er.
1. Vælg **Initialiser**.
1. Klik på **Ja** på siden til bekræftelse af installationen, når du har kontrolleret, at oplysningerne er korrekte. Visningen **Commerce-administration** vises igen, hvor fanen **Commerce** er valgt. Din CSU er sat i kø til klargøring.
1. Før du fortsætter, skal du kontrollere, at din statussen for dit CSU er **Vellykket**. Initialiseringen tager ca. to til fem timer.

Hvis du ikke kan finde linket **Administrer** i miljødetaljevisningen, skal du kontakte din Microsoft-kontaktperson for at få hjælp.

### <a name="initialize-e-commerce"></a>Initialisere e-handel

Følg disse trin for at påbegynde e-Commerce.

1. Under fanen **e-Commerce** skal du gennemgå samtykket for evalueringen og derefter vælge **Konfiguration**.
1. Angiv et navn for **e-Commerce-miljønavn** i feltet. Vær opmærksom på, at navnet vil være synligt i nogle af URL-adresserne, der peger på din e-Commerce-forekomst.
1. I feltet **Commerce Scale Unit-navn** skal du vælge din CSU på listen. (Listen bør kun have én indstilling.)

    Feltet **e-Commerce-geografi** indstilles automatisk.

1. Vælg **Næste** for at fortsætte.
1. I feltet **Understøttede værtsnavne** skal du angive et vilkårligt gyldigt domæne som f.eks. `www.fabrikam.com`.
1. I feltet **ADD-sikkerhedsgruppe for systemadministratorer** skal du angive de første par bogstaver i navnet på den sikkerhedsgruppe, du vil bruge, og derefter vælge symbolet for forstørrelsesglas for at få vist søgeresultaterne. Vælg den korrekte sikkerhedsgruppe på listen.
1.  I feltet **ADD-sikkerhedsgruppe for vurderings- og anmeldelsesadministratorer** skal du angive de første par bogstaver i navnet på den sikkerhedsgruppe, du vil bruge, og derefter vælge symbolet for forstørrelsesglas for at få vist søgeresultaterne. Vælg den korrekte sikkerhedsgruppe på listen.
1. Vælg **Ja** i indstillingen **Aktivér vurderinger og anmeldelser**.
1. Vælg **Initialiser**. Visningen **Commerce-administration** vises igen, hvor fanen **e-Commerce** er valgt. Din initialisering af e-Commerce er påbegyndt.
1. Før du fortsætter, skal du vente, indtil initialiseringsstatus for din e-Commerce er **Initialisering blev gennemført**.
1. Under **Links** nederst til højre skal du notere URL-adresserne for følgende links:

    * **e-Commerce-websted** – linket til roden af dit e-Commerce-websted.
    * **Commerce-webstedsgenerator** – linket til administrationsværktøjet for webstedet.

## <a name="next-steps"></a>Næste trin

For at fortsætte processen med klargøring og konfigurering af dit Commerce-evalueringsmiljø se [Konfigurere et Commerce-evalueringsmiljø](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over Dynamics 365 Commerce-evalueringsmiljø](cpe-overview.md)

[Konfigurere et Dynamics 365 Commerce-evalueringsmiljø](cpe-post-provisioning.md)

[Konfigurere BOPIS i et Dynamics 365 Commerce-evalueringsmiljø](cpe-bopis.md)

[Konfigurere valgfrie funktioner til et Dynamics 365 Commerce-evalueringsmiljø](cpe-optional-features.md)

[Ofte stillede spørgsmål om Dynamics 365 Commerce-evalueringsmiljø](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (sky)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-websted](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]