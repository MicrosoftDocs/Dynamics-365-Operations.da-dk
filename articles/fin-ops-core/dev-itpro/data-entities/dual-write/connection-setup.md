---
title: Understøttede scenarier til installation med to skrivninger
description: I dette emne beskrives de scenarier, der understøttes til installation med to skrivninger.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d7ff514768ee8e4797b591da89e190a855385885
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172848"
---
# <a name="supported-scenarios-for-dual-write-setup"></a>Understøttede scenarier til installation med to skrivninger

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Du kan oprette en forbindelse med to skrivninger mellem et Finance and Operations-miljø og et Common Data Service-miljø.

+ Et **Finance and Operations-miljø** leverer den underliggende platform for **Finance and Operations-apps** (f.eks Microsoft Dynamics 365 Finance. Dynamics 365 Supply Chain Management, Dynamics 365 Retail og Dynamics 365 Human Resources).
+ Et **Common Data Service-miljø** giver den underliggende platform for **modelstyrede apps i Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).

Konfigurationsmekanismen varierer, afhængigt af dit abonnement og miljøet.

+ Ved nye forekomster af Finance and Operations-apps begynder opsætningen af en forbindelse med to skrivninger i Microsoft Dynamics Lifecycle Services (LCS). Hvis du har en licens til Microsoft Power Platform, vil du få et nyt Common Data Service-miljø, hvis din lejer ikke har en.
+ For eksisterende forekomster af Finance and Operations-apps begynder opsætningen af en forbindelse med to skrivninger i Finance and Operations-miljøet.

Følgende konfigurationsscenarier understøttes:

+ [En ny Finance and Operations-app-forekomst og en ny modeldrevet app-forekomst](#new-new)
+ [En ny Finance and Operations-app-forekomst og en eksisterende modeldrevet app-forekomst](#new-existing)
+ [En ny Finance and Operations-app-forekomst, som har demodata og en ny modeldrevet app-forekomst](#new-demo-new)
+ [En ny Finance and Operations-app-forekomst, som har demodata og en eksisterende modeldrevet app-forekomst](#new-demo-existing)
+ [En eksisterende Finance and Operations-app-forekomst og en ny modeldrevet app-forekomst](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a>En ny Finance and Operations-app-forekomst og en ny modeldrevet app-forekomst

Hvis du vil oprette en forbindelse med to skrivninger mellem en ny forekomst af en Finance and Operations-app, der ikke har data, og en ny forekomst af en modeldrevet app i Dynamics 365, skal du følge trinnene i [Opsætning af en forbindelse med to skrivninger fra Lifecycle Services](lcs-setup.md). Når opsætningen af forbindelsen er fuldført, sker følgende handlinger automatisk:

- Der klargøres et nyt tomt Finance and Operations-miljø.
- Der klargøres en ny tom forekomst af en modeldrevet app, hvor CRM standardløsningen installeres.
- Der oprettes en forbindelse med to skrivninger for DAT-virksomhedsdata.
- Enhedstilknytninger er aktiveret til direkte synkronisering.

Begge miljøer er derefter klar til dynamisk datasynkronisering.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a>En ny Finance and Operations-app-forekomst og en eksisterende modeldrevet app-forekomst

Hvis du vil oprette en forbindelse med to skrivninger mellem en ny forekomst af en Finance and Operations-app, der ikke har data, og en eksisterende forekomst af en modeldrevet app i Dynamics 365, skal du følge trinnene i [Opsætning af en forbindelse med to skrivninger fra Lifecycle Services](lcs-setup.md). Når opsætningen af forbindelsen er fuldført, sker følgende handlinger automatisk:

- Der klargøres et nyt tomt Finance and Operations-miljø.
- Der oprettes en forbindelse med to skrivninger for DAT-virksomhedsdata.
- Enhedstilknytninger er aktiveret til direkte synkronisering.

Begge miljøer er derefter klar til dynamisk datasynkronisering.

Udfør følgende trin for at synkronisere Common Data Service-data til Finance and Operations-appen.

1. Opret et nyt regnskab i Finance and Operations-appen.
2. Føj firmaet til opsætningen af forbindelsen med to skrivninger.
3. [Bootstrap](bootstrap-company-data.md) Common Data Service-dataene ved hjælp af en ISO-virksomhedskode (International Organization for Standardization) på tre bogstaver.

Da to skrivninger er i direkte synkroniseringstilstand, starter dataene fra Common Data Service automatisk med at strømme til Finance and Operations-appen.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a>En ny Finance and Operations-app-forekomst, som har demodata og en ny modeldrevet app-forekomst

Hvis du vil oprette en forbindelse med to skrivninger mellem en ny forekomst af en Finance and Operations-app, der har demonstrationsdata og en ny forekomst af en modeldrevet app i Dynamics 365, skal du følge trinnene i afsnittet [En ny Finance and Operations-app-forekomst og en ny modeldrevet app-forekomst](#new-new) tidligere i dette emne. Når opsætningen af forbindelsen er fuldført, skal du udføre følgende trin, hvis du vil synkronisere demodataene til den modelbaserede app.

1. Åbn Finance and Operations-appen fra siden LCS, log på, og gå derefter til **Datastyring \> To skrivninger**.
2. Kør den **første synkroniseringsfunktion** for de enheder, du vil synkronisere data for.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a>En ny Finance and Operations-app-forekomst, som har demodata og en eksisterende modeldrevet app-forekomst

Hvis du vil oprette en forbindelse med to skrivninger mellem en ny forekomst af en Finance and Operations-app, der har demonstrationsdata og en eksisterende forekomst af en modeldrevet app i Dynamics 365, skal du følge trinnene i afsnittet [En ny Finance and Operations-app-forekomst og en eksisterende modeldrevet app-forekomst](#new-existing) tidligere i dette emne. Når opsætningen af forbindelsen er fuldført, skal du udføre følgende trin, hvis du vil synkronisere demodataene til den modelbaserede app.

1. Åbn Finance and Operations-appen fra siden LCS, log på, og gå derefter til **Datastyring \> To skrivninger**.
2. Kør den **første synkroniseringsfunktion** for de enheder, du vil synkronisere data for.

Udfør følgende trin for at synkronisere Common Data Service-data til Finance and Operations-appen.

1. Opret et nyt regnskab i Finance and Operations-appen.
2. Føj firmaet til opsætningen af forbindelsen med to skrivninger.
3. [Bootstrap](bootstrap-company-data.md) Common Data Service-dataene ved hjælp af en ISO-virksomhedskode på tre bogstaver.

Da to skrivninger er i direkte synkroniseringstilstand, starter dataene fra Common Data Service automatisk med at strømme til Finance and Operations-appen.

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a>En eksisterende Finance and Operations-app-forekomst og en ny modeldrevet app-forekomst

Opsætningen af en forbindelse med tom skrivninger mellem en eksisterende forekomst af en Finance and Operations-app og en ny eller eksisterende forekomst af en modelbaseret app i Dynamics 365 forekommer i økonomi- og handlingsmiljøet.

1. Konfigurer forbindelsen fra Finance and Operations-appen.
2. Hvis du vil synkronisere eksisterende Common Data Service-data med Finance and Operations-appen, skal du udføre en [bootstrap](bootstrap-company-data.md) på Common Data Service-dataene ved hjælp af en ISO-virksomhedskode på tre bogstaver.

Da to skrivninger er i direkte synkroniseringstilstand, starter dataene fra Common Data Service automatisk med at strømme til Finance and Operations-appen.
