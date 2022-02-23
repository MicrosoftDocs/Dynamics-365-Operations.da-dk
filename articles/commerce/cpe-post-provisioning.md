---
title: Konfigurere et Dynamics 365 Commerce-evalueringsmiljø
description: I dette emne beskrives det, hvordan du konfigurerer et Microsoft Dynamics 365 Commerce-evalueringsmiljø, efter at det er blevet klargjort.
author: psimolin
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: 6a1ae960f0f530104af7bdea9a8fcb78b01571f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410973"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a>Konfigurere et Dynamics 365 Commerce-evalueringsmiljø

[!include [banner](includes/banner.md)]

I dette emne beskrives det, hvordan du konfigurerer et Microsoft Dynamics 365 Commerce-evalueringsmiljø, efter at det er blevet klargjort.

## <a name="overview"></a>Overblik

Fuldfør kun procedurerne i dette emne, efter dit Commerce-evalueringsmiljø er klargjort. For yderligere oplysninger om, hvordan du klargør dit Commerce-evalueringsmiljø se [Klargøre et Commerce-evalueringsmiljø](provisioning-guide.md).

Når dit Commerce-evalueringsmiljø er blevet klargjort fra ende til anden, skal yderligere konfigurationstrin efter klargøring fuldføres, før du kan begynde at evaluere miljøet. Hvis du vil fuldføre disse trin, skal du bruge Microsoft Dynamics Lifecycle Services (LCS) og Dynamics 365 Commerce.

## <a name="before-you-start"></a>Før du begynder

1. Log på [LCS-portalen](https://lcs.dynamics.com).
1. Gå til dit projekt.
1. Vælg **Skybaserede miljøer** øverst i menuen.
1. Vælg dit miljø fra listen.
1. Vælg **Log på miljø** i miljøoplysningerne til højre. Du bliver sendt til Commerce-hovedkontoret.
1. Kontrollér, at den juridiske enhed **USRT** er valgt i øverste højre hjørne.

Under klargøring af aktiviteter i Commerce-hovedkontoret skal du kontrollere, at den juridiske enhed **USRT** altid er markeret.

## <a name="configure-the-point-of-sale"></a>Konfigurer POS 

### <a name="associate-a-worker-with-your-identity"></a>Tilknyt en arbejder til din identitet

Hvis du vil knytte en arbejder til din identitet, skal du følge disse trin i Commerce-hovedkontor.

1. Brug menuen til venstre for at gå til **Moduler \> Retail og Commerce \> Medarbejdere \> Arbejdere**.
1. Find og vælg følgende post i listen: **000713 - Andrew Collette**.
1. Klik på **Commerce** i handlingsruden.
1. Vælg **Tilknyt eksisterende identitet**.
1. Skriv din mailadresse i feltet **E-mail** til højre for **Søg ved hjælp af e-mail**.
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

## <a name="enable-jobs"></a>Aktivere job

Følg disse trin for at aktivere job i Commerce.

1. Log på miljøet (hovedkontor).
1. Brug menuen til venstre for at gå til **Retail og Commerce \> Forespørgsler og rapporter \> Batchjobs**.

    De resterende trin i denne procedure skal fuldføres for hvert af følgende job:

    * Behandling af e-mail-besked om detailordre
    * Produkttilgængelighed
    * P-0001
    * Synkroniser ordrejob

1. Brug Quick Filter til at søge efter jobbet ved hjælp af dets navn.
1. Hvis status for jobbet er **Udfører**, skal du gøre følgende:

    1. Vælg posten.
    1. Klik på **Batchjob** i handlingsruden, og vælg **Skift status**.
    1. Vælg **Annullering**, og vælg derefter **OK**.

Du kan også vælge at angive gentagelsesintervallet til et (1) minut for følgende job:

* Behandling af job med e-mailbesked om detailordre
* P-0001-job
* Synkroniser ordrejob

### <a name="run-full-data-synchronization"></a>Kør fuld datasynkronisering

Følg disse trin for at køre fuld datasynkronisering i Commerce-hovedkontor.

1. Brug menuen til venstre for at gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Handelsplanlægger \> Kanaldatabase**.
1. Vælg den kanal, der hedder **scXXXXXXXXX**.
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

Når klargørings- og konfigurationstrinnene er fuldførte, kan du begynde at bruge dit evalueringsmiljø. Brug Site Builder-URL-adressen for Commerce-webstedet til at gå til oprettelsesoplevelsen. Brug URL-adressen for Commerce-webstedet for at gå til detailkundewebstedet.

Hvis du vil konfigurere valgfrie funktioner til dit Commerce-evalueringsmiljø, se [Konfigurere valgfrie funktioner til et Commerce-evalueringsmiljø](cpe-optional-features.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over Dynamics 365 Commerce-evalueringsmiljø](cpe-overview.md)

[Klargøre et Dynamics 365 Commerce-evalueringsmiljø](provisioning-guide.md)

[Konfigurere valgfrie funktioner til et Dynamics 365 Commerce-evalueringsmiljø](cpe-optional-features.md)

[Konfigurere BOPIS i et Dynamics 365 Commerce-evalueringsmiljø](cpe-bopis.md)

[Ofte stillede spørgsmål om Dynamics 365 Commerce-evalueringsmiljø](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-websted](https://aka.ms/Dynamics365CommerceWebsite)
