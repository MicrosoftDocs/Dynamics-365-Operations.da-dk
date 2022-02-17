---
title: Dynamics 365 Finance og Dynamics 365 Supply Chain Management i US Government Community Cloud (GCC)
description: Dette emne indeholder oplysninger om Microsoft Dynamics 365 US Government-produkter, som er tilgængelige for kvalificerede offentlige og private enheder.
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 0c8b88e5d190f6dc9beb9342909d1e489d4af10b
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062280"
---
# <a name="dynamics-365-finance-and-dynamics-365-supply-chain-management-in-us-government-community-cloud-gcc"></a>Dynamics 365 Finance og Dynamics 365 Supply Chain Management i US Government Community Cloud (GCC)

[!include [banner](../includes/banner.md)]



Vælg Microsoft Dynamics 365 produkter fra myndighederne i USA er tilgængelige for kvalificerede offentlige og private enheder. Disse enheder er begrænset til følgende typer:

- Amerikanske føderale, statslige, lokale, valuta- og territorialstyrede enheder
- Private enheder, der bruger Dynamics 365 US Government til at levere løsninger til offentlige myndigheder eller til kvalificerede medlemmer af skymiljøet
- Private enheder, der har kundedata, der er underlagt de lovgivningsmæssige regler, og Dynamics 365 US Government er den rette tjeneste til at opfylde de lovgivningsmæssige krav

Du kan finde flere oplysninger under [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government).

## <a name="onboarding"></a>Onboarding

Hvis du vil fuldføre den første start med et implementeringsprojekt i Microsoft Dynamics Lifecycle Services (LCS), skal du følge instruktionerne i [Onboarde et implementeringsprojekt](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md). Du må dog ikke bruge linket til offentlige LCS, der findes i disse instruktioner. Brug i stedet følgende URL-adresse til at åbne LCS for US Government Community Cloud (GCC): <https://gov.lcs.microsoftdynamics.us>.

Når den første start er fuldført, skal du følge instruktionerne i [Projekt-onboarding](../lifecycle-services/project-onboarding.md). Igen skal du bruge [LCS til GCC](https://gov.lcs.microsoftdynamics.us) i stedet for offentlige LCS.

## <a name="environment-deployment"></a>Miljøinstallation

Når du har fuldført onboarding af projektet, kan du gennemse de ekstra egenskaber i LCS, der er beskrevet i [Lifecycle Services (LCS) for Finans- og driftsapps-kunder](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md). Gå derefter videre til installation af miljøet.

- Hvis du vil implementere Microsoft-administrerede miljøer via LCS, skal du følge instruktionerne i [Lifecycle Services (LCS) for Finans- og driftsapps-kunder](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience).
- Du kan finde oplysninger om miljøer, der er tilknyttet skyen, i [Implementere og få adgang til udviklingsmiljøer](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md). Du skal også fuldføre processen for onboarding af Resource Manager for dine forbindelser, som det er beskrevet i [fuldførelse af Azure Resource Manager-processen til onboarding i de amerikanske myndigheders Lifecycle Services-projekter](arm-onbarding-us-goverment.md).

> [!NOTE]
> I LCS-projekter fra de amerikanske myndigheder understøttes kun Azure Government-specifikke Azure-abonnementer.

## <a name="features-that-arent-available"></a>Funktioner, som ikke er tilgængelige

Nogle funktioner er ikke tilgængelige for implementering i GCC, eller de vil ikke være tilgængelige til brug sammen med Dynamics 365 i GCC. F.eks. er Azure DevOps-tjenester ikke tilgængelige i GCC. Det er dog muligt at bruge lokale Azure DevOps- eller offentlige Azure DevOps-tjenester. Du kan finde detaljerede oplysninger om tilgængelighed af funktioner i [Business Applications-tilgængelighed i de amerikanske myndigheder](https://aka.ms/BAPFunctionalParity).

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>Er Dynamics 365 Finance og Dynamics 365 Supply Chain Management understøttet i GCC-High?

Nr. Dynamics 365 Finance og Dynamics 365 Supply Chain Management understøttes kun i GCC.

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>Kan jeg bruge offentlig Azure DevOps sammen med Finance og Supply Chain Management i GCC?

Ja, du kan bruge offentlige Azure DevOps-tjenester, hvis du ikke har krav til en løsning, der er certificeret af Federal Risk and Authorization Management Program (FEDRAMP). Du kan også bruge Azure DevOps-serveren.

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>Kan jeg implementere et udviklingsmiljø med skyen, Tier-1, på et Azure commercial-abonnement?

Nr. I [LCS til GCC](https://gov.lcs.microsoftdynamics.us) skal du bruge et Azure Government-abonnement til at implementere et miljø med skyen.

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>Hvad kan jeg gøre, hvis jeg skal bruge en pakke fra mappen Delte aktiver, men den ikke kan benyttes i LCS til GCC?

Du kan hente den samme pakke fra mappen Delte aktiver i [offentlige LCS](https://lcs.dynamics.com). Partneren kan også hjælpe dig med at hente pakken.

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>Er værktøjet til kodeopgradering tilgængeligt i GCC?

Nej, værktøjet til kodeopgradering er ikke aktuelt tilgængeligt i GCC. Du kan dog oprette et kundeemneprojekt med [offentlig LCS](https://lcs.dynamics.com) og bruge værktøjet til kodeopgradering. Bemærk, at du ikke kan implementere miljøer på kundeemneprojekter.

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>Kan min partner åbne en supportbillet på mine vegne?

Ja. Hvis din partner bruger en ikke-GCC-identitet, vil supportbilletten dog blive sendt til den offentlige supportkø. Det anbefales, at du bruger rettigheder som kunde-GCC i LCS til at åbne supportbilletter.

## <a name="see-also"></a>Se også

- [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government)
- [Business Applications, der er tilgængelige for amerikanske myndigheder](https://aka.ms/BAPFunctionalParity).
- [Brugervejledning til Lifecycle Services (LCS)](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Oversigt over skyinstallation](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
