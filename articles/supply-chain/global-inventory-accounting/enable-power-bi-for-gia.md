---
title: Aktivere Power BI til Global Inventory Accounting
description: Dette emne indeholder en beskrivelse af, hvordan du aktiverer Microsoft Power BI til Global Inventory Accounting.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f0a8f5948d9e30eb220aa8177a4b9718223a4f9d
ms.sourcegitcommit: 5bfd6511d710deb539b4030eb0e9c48d25513595
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/19/2022
ms.locfileid: "8013828"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a>Aktivere Power BI til Global Inventory Accounting

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Du kan fastgøre felter, dashboards og rapporter fra din [PowerBI.com](https://powerbi.com/)-konto til arbejdsområdet i Microsoft Dynamics 365-programmet.

## <a name="prerequisites"></a>Forudsætninger

Følgende forudsætninger skal være tilstede, før du kan aktivere Power BI-rapportering:

- Du skal være systemadministrator i Dynamics 365-programmet.
- Du skal have en [PowerBI.com](https://powerbi.com/)-konto.
- Du skal have mindst ét dashboard og én rapport i Power BI-kontoen.
- Du skal være administrator for din Azure Active Directory-konto (Azure AD).
- Domænet Azure AD skal være det samme domæne, som du har brugt til din [PowerBI.com](https://powerbi.com/)-konto.

## <a name="setup"></a>Konfiguration

Følg disse trin for at konfigurere Power BI-integrationen.

1. Log på [Microsoft Dynamics LifeCycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).
1. Gå til **Delt aktivbibliotek**, vælg **Power BI-rapportmodel** som aktivtype, og hent pakken **Global Inventory Accounting**. 
1. Log på [PowerBI.com](https://app.powerbi.com/), og overfør Power BI-rapportfilen for **Global Inventory Accounting** ved at følge disse trin:

    1. Vælg **Ny**.
    1. Vælg **Overfør en fil**.
    1. Vælg Power BI-rapportfilen for **Global Inventory Accounting**.

1. Konfigurer Power BI-rapporten for **Global Inventory Accounting** ved at følge disse trin:

    1. Gå til **Mit arbejdsområde**, find datasættet til Global Inventory Accounting, og vælg derefter **Indstillinger** i menuen **Indstillinger**.
    1. Udvid **Parametre** i **Indstillinger for globalt lagerregnskab**, og opdater alle parametre efter behov. Du skal især kontrollere følgende indstillinger:
        1. Overskriv standardværdierne for **Dataverse URL-adressen** og ved hjælp af de værdier, der findes under **Power Platform-miljøoplysninger** i LCS (i sektionen **Power Platform-integration**).
        1. Overskriv standardværdierne for **Miljø-id** ved hjælp af de værdier, der findes under **Miljødetaljer** i LCS (i sektionen **Administrer miljø**).
        1. Vælg linket **Rediger legitimationsoplysninger** ud for **CDS**-etiketten i afsnittet **Legitimationsoplysninger for datakilden**. Log derefter på din Dataverse-konto ved hjælp af **OAuth2**-godkendelsesmetoden.
    1. Kontroller, at de Power BI-rapporter, der findes i **Mit arbejdsområde \> Rapporter \> Globalt lagerregnskab**, nu fungerer korrekt og viser indhold fra systemet.

1. Registrer programmet som beskrevet i [Konfigurere PowerBI.com-integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).
1. Integrer Power BI-rapporten for **Global Inventory Accounting** i Dynamics 365 Supply Chain Management ved at følge disse trin:

    1. Gå til **Systemadministration \> Konfiguration \> PowerBI.com-konfiguration**.
    1. Vælg **Rediger**.
    1. Vælg **Aktivér PowerBI.Com-integration**.
    1. I feltet **Program-id** skal du angive program-id'et.
    1. I feltet **Programnøgle** skal du angive programnøglen.
    1. Vælg **Gem**.

1. Opdater siden, så Power BI-logondialogboksen vises.
1. Vælg **Åbn rapportkatalog** under fanen **Indstillinger**, og vælg derefter den Power BI-rapportfil til **Global Inventory Accounting**, som du overførte tidligere.
1. Opdater siden. Du bør se, at rapporten er blevet tilføjet.
1. Under **Power BI-rapporter** skal du vælge linket **Global Inventory Accounting**.

Du kan finde flere oplysninger i [Konfigurere PowerBI.com-integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).
