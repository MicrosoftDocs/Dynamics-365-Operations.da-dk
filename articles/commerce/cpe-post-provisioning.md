---
title: Konfigurere et Dynamics 365 Commerce-evalueringsmiljø
description: Denne artikel beskriver, hvordan du konfigurerer et Microsoft Dynamics 365 Commerce-evalueringsmiljø, efter at det er blevet klargjort.
author: psimolin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 19d88139e35554bce68bc6203141957b96e439a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892324"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a>Konfigurere et Dynamics 365 Commerce-evalueringsmiljø

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du konfigurerer et Microsoft Dynamics 365 Commerce-evalueringsmiljø, efter at det er blevet klargjort.

Fuldfør kun procedurerne i denne artikel, efter dit Commerce-evalueringsmiljø er klargjort. For yderligere oplysninger om, hvordan du klargør dit Commerce-evalueringsmiljø se [Klargøre et Commerce-evalueringsmiljø](provisioning-guide.md).

Når dit Commerce-evalueringsmiljø er blevet klargjort fra ende til anden, skal yderligere konfigurationstrin efter klargøring fuldføres, før du kan begynde at evaluere miljøet. Hvis du vil fuldføre disse trin, skal du bruge Microsoft Dynamics Lifecycle Services (LCS) og Dynamics 365 Commerce.

## <a name="before-you-start"></a>Før du begynder

1. Log på [LCS-portalen](https://lcs.dynamics.com).
1. Gå til dit projekt.
1. Vælg **Skybaserede miljøer** øverst i menuen.
1. Vælg dit miljø fra listen.
1. Vælg **Log på miljø** i miljøoplysningerne til højre. Du bliver sendt til Commerce Headquarters.
1. Kontrollér, at den juridiske enhed **USRT** er valgt i øverste højre hjørne.
1. Gå til **Commerce-parametre \> Konfigurationsparametre**, og sørg for, at der er en post for **ProductSearch.UseAzureSearch**, der er angivet til **true**. Hvis denne post mangler, kan du tilføje den, angive værdien til **true** og derefter vælge **Kanaldatabase \> Fuld synkronisering** for den Commerce Scale Unit, der er tilknyttet dit websted for e-handel.
1. Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-planlægger \> Initialiser Commerce-planlægger**. I menuen **Initialiser Commerce-planlægger** skal du sikre, at indstillingen **Slet eksisterende konfiguration** er angivet til **Ja**, og derefter vælge **OK**.
1. Hvis du vil føje kanaler til Commerce Scale Unit, skal du gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-planlægger \>Kanaldatabase** og derefter vælge Commerce Scale Unit i venstre rude. I oversigtspanelet **Detailkanal** skal du tilføje **AW-onlinebutik**, **AW Business-onlinebutik** og **Fabrikams udvidede onlinebutik** som kanaler. Du kan også tilføje detailforretninger, hvis du bruger POS ( f.eks. **Seattle**, **San Francisco** og **San Jose**).

Under klargøring af aktiviteter i Commerce Headquarters skal du kontrollere, at den juridiske enhed **USRT** altid er markeret.

## <a name="configure-the-point-of-sale"></a>Konfigurer POS 

### <a name="associate-a-worker-with-your-identity"></a>Tilknyt en arbejder til din identitet

Hvis du vil knytte en arbejder til din identitet, skal du følge disse trin i Commerce Headquarters.

1. Brug menuen til venstre for at gå til **Moduler \> Retail og Commerce \> Medarbejdere \> Arbejdere**.
1. Find og vælg følgende post i listen: **000713 - Andrew Collette**.
1. Klik på **Commerce** i handlingsruden.
1. Vælg **Tilknyt eksisterende identitet**.
1. Skriv din emailadresse i feltet **Email** til højre for **Søg ved hjælp af email**.
1. Vælg **Søg**.
1. Vælg posten med dit navn.
1. Vælg **OK**.
1. Vælg **Gem**.

### <a name="activate-cloud-pos"></a>Aktiverere sky POS

Følg disse trin for at aktivere skybaseret POS.

1. Vælg **Skybaserede miljøer** øverst i menuen.
1. Vælg dit miljø fra listen.
1. Vælg **Log på skybaseret POS** i miljøoplysningerne til højre.
1. Vælg **Næste** for at åbne dialogboksen **Før du begynder**.
1. Lad feltet **Server-URL-adresse** være, som det er. Vælg **Næste**.
1. Log på ved hjælp af din Microsoft Azure Active Directory (Azure AD)-konto.
1. Under **Butiksnavn** skal du vælge **San Francisco** og derefter vælge **Næste**.
1. Under **Kasseapparat og enhed** skal du vælge **SANFRAN-1**.
1. Vælg **Aktivér**. Du er logget ud og dirigeret til POS-login-siden.
1. Du kan nu logge på den skybaserede POS-oplevelse ved hjælp af operatør-ID **000713** og adgangskoden **123**.

## <a name="set-up-your-site-in-commerce"></a>Konfigurer dit websted i Commerce

Følg disse trin for at begynde at konfigurere dit evalueringswebsted i Commerce.

1. Log på Site Builder ved hjælp af den URL-adresse, som du noterede ned, da du initialiserede e-Commerce i forbindelse med klargøring (jf. [Initialiser e-Commerce](provisioning-guide.md#initialize-e-commerce)).
1. Vælg webstedet **Fabrikam** for at åbne dialogboksen webstedsopsætning.
1. Vælg det domæne, du angav, da du initialiserede e-Commerce.
1. Som standardkanal skal du vælge **Udvidet Fabrikam-onlinebutik**. (Sørg for at vælge den **udvidede** onlinebutik.)
1. Vælg **da-dk** som standardsprog.
1. Lad værdien i feltet **Sti** være, som den er.
1. Vælg **OK**. Listen over sider på webstedet vises.
1. Gentag trin 2-7 for webstedet **AdventureWorks** (som er tilknyttet **AW-onlinebutik**-kanalen) og webstedet **AdventureWorks Business** (som er tilknyttet kanalen **AW Business-onlinebutik**). Hvis feltet **Sti** til Fabrikams websted er tom, skal du tilføje stier for de to AdventureWorks-websteder (f.eks. "aw" og "awbusiness").

## <a name="enable-jobs"></a>Aktivere job

Følg disse trin for at aktivere job i Commerce.

1. Log på miljøet (hovedkontor).
1. Brug menuen til venstre for at gå til **Retail og Commerce \> Forespørgsler og rapporter \> Batchjobs**.

    De resterende trin i denne procedure skal fuldføres for hvert af følgende job:

    * Behandling af email-besked om detailordre
    * Produkttilgængelighed
    * P-0001
    * Synkroniser ordrejob

1. Brug Quick Filter til at søge efter jobbet ved hjælp af dets navn.
1. Hvis status for jobbet er **Udfører**, skal du gøre følgende:

    1. Vælg posten.
    1. Klik på **Batchjob** i handlingsruden, og vælg **Skift status**.
    1. Vælg **Annullering**, og vælg derefter **OK**.

1. Hvis status for jobbet er **Tilbageholdt**, skal du gøre følgende:

    1. Vælg posten.
    1. Klik på **Batchjob** i handlingsruden, og vælg **Skift status**.
    1. Vælg **Afventer**, og vælg derefter **OK**.

Du kan også vælge at angive gentagelsesintervallet til et (1) minut for følgende job:

* Behandling af job med emailbesked om detailordre
* P-0001-job
* Synkroniser ordrejob

### <a name="run-full-data-synchronization"></a>Kør fuld datasynkronisering

Følg disse trin for at køre fuld datasynkronisering i Commerce Headquarters.

1. Brug menuen til venstre for at gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Handelsplanlægger \> Kanaldatabase**.
1. Vælg den kanal, der hedder **scXXXXXXXXX**.
1. Vælg **Fuld datasynkronisering** i handlingsruden.
1. Angiv **9999** som distributionsplanen.
1. Vælg **OK**.
1. Vælg **OK**.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Test kreditkortoplysninger for at udføre testindkøb

Du kan bruge følgende disse testkreditkortoplysninger til at udføre testtransaktioner på webstedet:

- **Kortnummer:** 4111-1111-1111-1111
- **Udløbsdato** 10/30
- **Kontrolcifrene på kreditkortet (CVV):** 737

> [!IMPORTANT]
> Forsøg aldrig under nogen omstændigheder at bruge faktiske kreditkortoplysninger på testwebstedet.

## <a name="next-steps"></a>Næste trin

Når klargørings- og konfigurationstrinnene er fuldførte, kan du begynde at bruge dit evalueringsmiljø. Brug Site Builder-URL-adressen for Commerce-webstedet til at gå til oprettelsesoplevelsen. Brug URL-adressen for Commerce-webstedet for at gå til detailkundewebstedet.

Hvis du vil konfigurere valgfrie funktioner til dit Commerce-evalueringsmiljø, se [Konfigurere valgfrie funktioner til et Commerce-evalueringsmiljø](cpe-optional-features.md).

> [!NOTE]
> Commerce-evalueringsmiljøer har en forudindlæst Azure Active Directory (Azure AD) business-to-consumer-lejer (B2C) til demonstrationsformål. Det er ikke nødvendigt at konfigurere din egen Azure AD B2C-lejer for evalueringsmiljøer. Hvis du konfigurere evalueringsmiljøet for at bruge din egen Azure AD B2C-lejer, skal du tilføje ``https://login.commerce.dynamics.com/_msdyn365/authresp`` som URL-svaradresse i Azure AD B2C-programmet via Azure Portal.

## <a name="troubleshooting"></a>Fejlfinding

### <a name="site-builder-channel-list-is-empty-when-configuring-site"></a>Webstedsgeneratorens kanalliste er tom, når du konfigurerer websted

Hvis webstedsgeneratoren ikke viser nogen onlinebutikskanaler, sikrer hovedkontoret, at kanalerne er føjet til Commerce Scale Unit som beskrevet i afsnittet [Før du begynder](#before-you-start) ovenfor. Du kan også køre **Initialiser Commerce planlægger** med værdien **Slet eksisterende konfiguration** angivet som **Ja**.  Når disse trin er fuldført skal du på siden **Kanaldatabase** (**Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-planlægger \> Kanaldatabase**) køre **9999**-jobbet på Commerce Scale Unit.

### <a name="color-swatches-are-not-rendering-on-the-category-page-but-are-rendering-on-the-product-details-page-pdp-page"></a>Farveprøver gengives ikke på kategorisiden, men gengives på siden med produktdetaljer (PDP)

Benyt følgende fremgangsmåde for at sikre, at farve- og størrelsesprøver er angivet til at være definerbare.

1. Gå i hovedkontoret til **Retail og Commerce \> Konfiguration af kanal \> Kanalkategorier og produktattributter**.
1. Vælg onlinebutikskanalen i venstre rude, og vælg derefter **Angiv attributmetadata**.
1. Angiv indstillingen **Vis attribut på kanal** til **Ja**, angiv indstillingen **Kan redigeres** til **Ja**, og vælg derefter **Gem**. 
1. Vend tilbage til siden med onlinebutikskanalen, og vælg derefter **Publicer kanalopdateringer**.
1. Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-planlægger \> Kanaldatabase** og kør jobbet **9999** på Commerce Scale Unit.

### <a name="business-features-dont-appear-to-be-turned-on-for-the-adventureworks-business-site"></a>Det ser ikke ud til, at forretningsfunktioner er aktiveret for forretningswebstedet AdventureWorks

I hovedkontoret skal du sikre, at onlinebutikskanalen er konfigureret med **Kundetype** angivet til **B2B**. Hvis **Kundetype** er angivet til **B2C**, skal der oprettes en ny kanal, da den eksisterende kanal ikke kan redigeres. 

Demodata, der er leveret i Commerce version 10.0.26, og som tidligere havde en fejl, hvor kanalen **AW Business-onlinebutik** var fejlkonfigureret. Løsningen er at oprette en ny kanal med de samme indstillinger og konfigurationer med undtagelse af **Kundetype**, som skal angives til **B2B**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over Dynamics 365 Commerce-evalueringsmiljø](cpe-overview.md)

[Klargøre et Dynamics 365 Commerce-evalueringsmiljø](provisioning-guide.md)

[Konfigurere valgfrie funktioner til et Dynamics 365 Commerce-evalueringsmiljø](cpe-optional-features.md)

[Konfigurere BOPIS i et Dynamics 365 Commerce-evalueringsmiljø](cpe-bopis.md)

[Ofte stillede spørgsmål om Dynamics 365 Commerce-evalueringsmiljø](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-websted](https://aka.ms/Dynamics365CommerceWebsite)

[Konfigurere en B2C-lejer i Commerce](set-up-B2C-tenant.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
