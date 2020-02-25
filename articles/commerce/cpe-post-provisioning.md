---
title: Konfigurere et Dynamics 365 Commerce-prøveversionsmiljø
description: I dette emne beskrives det, hvordan du konfigurerer et Microsoft Dynamics 365 Commerce-prøveversionsmiljø, efter at det er blevet klargjort.
author: psimolin
manager: annbe
ms.date: 12/10/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12d3a86698e9250f5d1645de51e0749c8d929f75
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024700"
---
# <a name="configure-a-dynamics-365-commerce-preview-environment"></a>Konfigurere et Dynamics 365 Commerce-prøveversionsmiljø


[!include [banner](includes/banner.md)]

I dette emne beskrives det, hvordan du konfigurerer et Microsoft Dynamics 365 Commerce-prøveversionsmiljø, efter at det er blevet klargjort.

## <a name="overview"></a>Oversigt

Fuldfør kun procedurerne i dette emne, efter dit Commerce-prøveversionsmiljø er klargjort. For yderligere oplysninger om, hvordan du klargør dit Commerce-prøveversionsmiljø se [Klargøring af et Commerce-prøveversionsmiljø](provisioning-guide.md).

Når dit Commerce-prøveversionsmiljø er blevet klargjort fra ende til anden, skal yderligere konfigurationstrin efter klargøring fuldføres, før du kan begynde at evaluere miljøet. Hvis du vil fuldføre disse trin, skal du bruge Microsoft Dynamics Lifecycle Services (LCS) Dynamics 365 Commerce og Dynamics 365 Retail.

## <a name="before-you-start"></a>Før du begynder

1. Log på [LCS-portalen](https://lcs.dynamics.com).
1. Gå til dit projekt.
1. Vælg **Skybaserede miljøer** øverst i menuen.
1. Vælg dit miljø fra listen.
1. Vælg **Alle detaljer** i miljøoplysningerne til højre.
1. Vælg **Log på** for at åbne en menu, og vælg dernæst **Log på miljøet**.
1. Kontrollér, at den juridiske enhed **USRT** er valgt i øverste højre hjørne.

## <a name="configure-the-point-of-sale-in-lcs"></a>Konfigurer POS i LCS

### <a name="associate-a-worker-with-your-identity"></a>Tilknyt en arbejder til din identitet

Hvis du vil knytte en arbejder til din identitet i LCS, skal du følge disse trin.

1. Brug menuen til venstre for at gå til **Moduler \> Retail \> Medarbejdere \> Arbejdere**.
1. Find og vælg følgende post i listen: **000713 - Andrew Collette**.
1. Vælg **Retail** i handlingsruden.
1. Vælg **Tilknyt eksisterende identitet**.
1. Skriv din mailadresse i feltet **E-mail** til højre for **Søg ved hjælp af e-mail**.
1. Vælg **Søg**.
1. Vælg posten med dit navn.
1. Vælg **OK**.
1. Vælg **Gem**.

### <a name="activate-cloud-pos"></a>Aktiverere sky POS

Følg disse trin for at aktivere skybaseret POS i LCS.

1. Vælg **Skybaserede miljøer** øverst i menuen.
1. Vælg dit miljø fra listen.
1. Vælg **Alle detaljer** i miljøoplysningerne til højre.
1. Vælg **Log på** for at åbne en menu, og vælg derefter **Log på skybaseret POS** for at åbne POS.
1. Vælg **Næste**.
1. Log på ved hjælp af din Microsoft Azure Active Directory (Azure AD)-konto.
1. Under **Butiksnavn** skal du vælge **San Francisco**.
1. Vælg **Næste**.
1. Under **Kasseapparat og enhed** skal du vælge **SANFRAN-1**.
1. Vælg **Aktivér**. Du er logget ud og dirigeret til POS-login-siden.
1. Du kan nu logge på den skybaserede POS-oplevelse ved hjælp af operatør-ID **000713** og adgangskoden **123**.

## <a name="set-up-your-site-in-commerce"></a>Konfigurer dit websted i Commerce

Følg disse trin for at begynde at konfigurere dit prøveversionswebsted i Commerce.

1. Log på værktøjet til administration af webstedet ved hjælp af den URL-adresse, som du noterede ned, da du initialiserede e-Commerce i forbindelse med klargøring (jf. [Initialiser e-Commerce](provisioning-guide.md#initialize-e-commerce)).
1. Vælg webstedet **Fabrikam** for at åbne dialogboksen webstedsopsætning.
1. Vælg det domæne, du angav, da du initialiserede e-Commerce.
1. Som standardkanal skal du vælge **Udvidet Fabrikam-onlinebutik**. (Sørg for at vælge den **udvidede** onlinebutik.)
1. Vælg **da-dk** som standardsprog.
1. Lad værdien i feltet **Sti** være, som den er.
1. Vælg **OK**. Listen over sider på webstedet vises.

## <a name="enable-jobs-in-retail"></a>Aktivér job i Retail

Følg disse trin for at aktivere job i Retail.

1. Log på miljøet (hovedkontor).
1. Brug menuen til venstre for at gå til **Retail \> Forespørgsler og rapporter \> Batchjobs**.

    De resterende trin i denne procedure skal fuldføres for hvert af følgende job:

    * Behandling af e-mail-besked om detailordre
    * Produkttilgængelighed
    * P-0001
    * Synkroniser ordrejob

1. Brug Quick Filter til at søge efter jobbet ved hjælp af dets navn.
1. Hvis status for jobbet er **Tilbagehold**, skal du gøre følgende:

    1. Vælg posten.
    1. Klik på **Batchjob** i handlingsruden, og vælg **Skift status**.
    1. Vælg **Afventer**, og vælg derefter **OK**.

### <a name="run-full-data-synchronization-in-retail"></a>Kør fuld datasynkronisering i Retail

Følg disse trin for at køre fuld datasynkronisering i Retail.

1. Brug menuen til venstre for at gå til **Moduler \> Retail \> Konfiguration af hovedkontor \> Retail planlægger \> Kanaldatabase**.
1. På listen til venstre er kanalen **Standard** valgt. Vælg den anden tilgængelige kanal. Denne kanal hedder **scXXXXXXXXX**.
1. Vælg **Fuld datasynkronisering** i handlingsruden.
1. Angiv **9999** som distributionsplanen.
1. Vælg **OK**.
1. Vælg **OK**.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Test kreditkortoplysninger for at udføre testindkøb

Du kan bruge følgende disse testkreditkortoplysninger til at udføre testtransaktioner på webstedet:

- **Kortnummer:** 4111-1111-1111-1111
- **Udløbsdato** 10/20
- **Kontrolcifrene på kreditkortet (CVV):** 737

> [!IMPORTANT]
> Forsøg aldrig under nogen omstændigheder at bruge faktiske kreditkortoplysninger på testwebstedet.

## <a name="next-steps"></a>Næste trin

Når klargørings- og konfigurationstrinnene er fuldførte, er du klar til at evaluere dit prøveversionsmiljø. Brug URL-adressen til administrationsværktøjet for Commerce-webstedet til at gå til oprettelsesoplevelsen. Brug URL-adressen for Commerce-webstedet for at gå til oplevelsen detailkundewebstedet.

Hvis du vil konfigurere valgfrie funktioner til dit Commerce-prøveversionsmiljø, se [Konfiguration af valgfrie funktioner til et Commerce-prøveversionsmiljø](cpe-optional-features.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over Dynamics 365 Commerce-prøveversionsmiljø](cpe-overview.md)

[Klargøre et Dynamics 365 Commerce-prøveversionsmiljø](provisioning-guide.md)

[Konfigurere valgfrie funktioner for et Dynamics 365 Commerce-prøveversionsmiljø](cpe-optional-features.md)

[Ofte stillede spørgsmål om Dynamics 365 Commerce-prøveversionsmiljø](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-websted](https://aka.ms/Dynamics365CommerceWebsite)
