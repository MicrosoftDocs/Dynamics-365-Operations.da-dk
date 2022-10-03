---
title: Konfiguration til Finance Insights
description: Denne artikel beskriver de konfigurationstrin, der sætter systemet i gang med at bruge de egenskaber, der er tilgængelige i Finance Insights.
author: ShivamPandey-msft
ms.date: 09/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 05bf5fe5a5ff86bbf52ed58ee6b1e84c15bf2c1e
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573188"
---
# <a name="configuration-for-finance-insights"></a>Konfiguration til Finance Insights

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance Insights kombinerer funktionalitet fra Microsoft Dynamics 365 Finance sammen med Dataverse, Azure og AI Builder for at levere effektive prognoseværktøjer til din organisation. Denne artikel beskriver de konfigurationstrin, der sætter systemet i gang med at bruge de egenskaber, der er tilgængelige i Finance Insights. Hvis du vil gennemføre procedurerne i denne artikel, skal du have adgang som Systemadministrator og Systemtilpasser i [Power Portal-administrationen](https://admin.powerplatform.microsoft.com/), adgang som Systemadministrator i Dynamics 365 Finance og adgang til at oprette miljøer i Microsoft Dynamics Lifecycle Services (LCS).

> [!NOTE]
> Følgende procedurer til opsætning af Finance Insights gælder for Dynamics 365 Finance version 10.0.21 og nyere.

## <a name="deploy-dynamics-365-finance"></a>Udrulle Dynamics 365 Finance

Følg disse trin for at udrulle miljøerne.

1. I LCS skal du oprette eller opdatere et Dynamics 365 Finance-miljø. Miljøet kræver appversion 10.0.21 eller nyere.

    > [!NOTE]
    > Miljøet skal være et miljø med høj tilgængelighed (HA). (Denne type miljø kaldes også et Niveau-2-miljø). Du kan finde flere oplysninger i [Miljøplanlægning](/fin-ops-core/fin-ops/imp-lifecycle/environment-planning).

2. Hvis du konfigurerer Finance Insights i et sandkassemiljø, skal du muligvis kopiere produktionsdata til dette miljø, før forudsigelser kan virke. En forudsigelsesmodel bruger flere års data til at opbygge forudsigelser. Contoso-demodataene indeholder ikke nok historikdata til at træne forudsigelsesmodellen korrekt. 

## <a name="configure-your-azure-ad-tenant"></a>Konfigurér din Azure AD-lejer

Azure Active Directory (Azure AD) skal være konfigureret, så det kan bruges sammen med Dataverse og Microsoft Power Platform-programmerne. Denne konfiguration kræver, at enten rollen **Projektejer** eller rollen **Miljøchef** tildeles brugeren i feltet **Projektsikkerhedsrolle** i LCS.

Kontroller, at følgende opsætning er fuldført:

- Du har adgang til **Systemadministrator** og **Systemtilpasser** i Power Portal Administration.
- Der anvendes en Dynamics 365 Finance eller lignende licens til den bruger, der installerer tilføjelsesprogrammet Finance Insights.
- Følgende Azure AD-apps er registreret i Azure AD.

    |  Applikation                             | App-id                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |

    Kontroller listen **Alle programmer** for at kontrollere , om programmet er registreret i Azure AD. Yderligere oplysninger finder du i [Vise virksomhedsprogrammer](/azure/active-directory/manage-apps/view-applications-portal).
  
    Hvis programmet ikke er registreret i Azure AD, skal du kontakte support.
  
## <a name="configure-dataverse"></a>Konfigurer Dataverse

Benyt følgende fremgangsmåde til at konfigurere Dataverse til Finance Insights.

- Åbn miljøsiden i LCS, og kontrollér, at sektionen **Intregration af Power Platform** allerede er konfigureret.

    - Hvis Dataverse allerede er konfigureret, skal det Dataverse-miljønavn, der er knyttet til Finance-miljøet, være anført.
    - Hvis Dataverse ikke er konfigureret, skal du vælge **Konfiguration**. Det kan tage op til en time at konfigurere Dataverse-miljøet. Når konfiguration er fuldført korrekt, skal det Dataverse-miljønavn, der er tilknyttet Finance-miljøet, være anført.
    - Hvis denne integration er konfigureret med et eksisterende Microsoft Power Platform-miljø, skal du kontakte administratoren for at sikre, at det tilknyttede miljø ikke har den deaktiverede tilstand.

        Du kan finde flere oplysninger under [Aktivere Power Platform-integration](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md). 

        Du kan få adgang til Microsoft Power Platform Administration-webstedet ved at gå til <https://admin.powerplatform.microsoft.com/environments>.

## <a name="configure-the-finance-insights-add-in"></a>Konfigurere tilføjelsesprogrammet Finance Insights

Hvis du tidligere har installeret Finance Insights-tilføjelsesprogrammet, skal du fjerne det, før du fuldfører følgende procedure.

> [!NOTE]
> Hvis du allerede har installeret datasøens tilføjelsesprogram i LCS, vil Finance insights bruge det til at gemme data, der er påkrævet til forudsigelser. Hvis du endnu ikke har installeret datasøens tilføjelsesprogram i LCS, opretter tilføjelsesprogrammet Finance Insights en administreret datasø til dig.

Følg disse trin for at installere tilføjelsesprogrammet Finance Insights.

1. Log på LCS, og vælg derefter detaljerede oplysninger under miljønavnet på højre side af siden, vælg **Alle detaljer**.
2. Vælg **Installér et nyt tilføjelsesprogram** i afsnittet **Tilføjelsesprogrammer for miljø**.
3. Vælg tilføjelsesprogrammet **Finance Insights**.
4. Acceptér vilkår og betingelser, og vælg derefter **Installer**.

Tilføjelsesprogrammet kan være flere minutter om at blive installeret.

## <a name="one-last-thing"></a>En sidste ting...

Når tilføjelsesprogrammet er installeret korrekt, kan det tage op til en time, før du kan aktivere Finance Insights-funktioner i **Økonomistyring**-arbejdsområdet i Dynamics 365 Finance. Hvis du ikke vil vente så længe, kan du køre processen **Kontrol af status for klargøring af indsigt** manuelt. 

1. Gå i Dynamics 365 Finance til **Systemadministration \> Konfiguration \> Procesautomatisering**.
2. Find **Kontrol af status for klargøring af indsigt** under fanen **Baggrundsprocesser**, og vælg **Rediger**.
3. Indstil feltet **Næste udførelse** til 30 minutter før det nuværende tidspunkt.

   Denne ændring skal tvinge processen **Kontrol af status for klargøring af indsigt** til at køre med det samme.

   Når processen **Kontrol af status for klargøring af indsigt** er kørt korrekt, kan du aktivere Finance Insights-funktioner i arbejdsområdet **Funktionsstyring**.

> [!NOTE]
> Hvis processen **Kontrol af status for klargøring af indsigt** ikke kører, skal du gå til **Systemadministration** > **Forespørgsler** > **Batchjob**. I feltet **System til forespørgsler på procesautomatisering** skal du ændre værdien til **Venter** for at starte processen. 
> 
## <a name="feedback-and-support"></a>Feedback og support

Send en mail til [Finance Insights (forhåndsversion)](mailto:fiap@microsoft.com), hvis du er interesseret i at give feedback eller har brug for support.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
