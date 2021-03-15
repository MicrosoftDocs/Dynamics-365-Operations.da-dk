---
title: Vejledning i opsætning af dobbeltskrivning
description: I dette emne beskrives de scenarier, der understøttes til installation med to skrivninger.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 78a7cdc18476a1c523c83c92ca6f354c3ba806dc
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744847"
---
# <a name="guidance-for-dual-write-setup"></a>Vejledning i opsætning af dobbeltskrivning

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Du kan oprette en forbindelse med to skrivninger mellem et Finance and Operations-miljø og et Dataverse-miljø.

+ Et **Finance and Operations-miljø** leverer den underliggende platform for **Finance and Operations-apps** (f.eks Microsoft Dynamics 365 Finance. Dynamics 365 Supply Chain Management, Dynamics 365 Commerce og Dynamics 365 Human Resources).
+ Et **Dataverse-miljø** giver den underliggende platform for **modelbaserede apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).

> [!IMPORTANT]
> Modulet Human Resources i Dynamics 365 Finance understøtter dobbeltskrivningsforbindelser, men Dynamics 365 Human Resources-appen gør ikke.

Konfigurationsmekanismen varierer, afhængigt af dit abonnement og miljøet:

+ Ved nye forekomster af Finance and Operations-apps begynder opsætningen af en forbindelse med to skrivninger i Microsoft Dynamics Lifecycle Services (LCS). Hvis du har en licens til Microsoft Power Platform, vil du få et nyt Dataverse-miljø, hvis din lejer ikke har en.
+ For eksisterende forekomster af Finance and Operations-apps begynder opsætningen af en forbindelse med to skrivninger i Finance and Operations-miljøet.

Før du starter dobbeltskrivning på en enhed, kan du køre en indledende synkronisering for at håndtere eksisterende data på begge sider: Finance and Operations-apps og kundeengagementapps. Du kan springe den første synkronisering over, hvis du ikke har brug for at synkronisere data mellem de to miljøer.

Ved hjælp af en første synkronisering kan du kopiere eksisterende data fra én app til en anden tovejs. Der er flere forskellige opsætningsscenarier, afhængigt af hvilke miljøer du allerede har, og hvilken type data der er i dem.

Følgende konfigurationsscenarier understøttes:

+ [En ny Finance and Operations-app-forekomst og en ny forekomst af en kundeengagementapp](#new-new)
+ [En ny Finance and Operations-app-forekomst og en eksisterende forekomst af en kundeengagementapp](#new-existing)
+ [En ny Finance and Operations-app-forekomst, som har data, og en ny forekomst af kundeengagementapp](#new-data-new)
+ [En ny Finance and Operations-app-forekomst, som har data, og en eksisterende forekomst af kundeengagementapp](#new-data-existing)
+ [En eksisterende Finance and Operations-app-forekomst og en ny forekomst af en kundeengagementapp](#existing-new)
+ [En eksisterende Finance and Operations-app-forekomst og en eksisterende forekomst af en kundeengagementapp](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>En ny Finance and Operations-app-forekomst og en ny forekomst af en kundeengagementapp

Hvis du vil oprette en forbindelse med dobbeltskrivning mellem en ny forekomst af en Finance and Operations-app, der ikke har data, og en ny forekomst af en kundeengagementapp, skal du følge trinnene i [Konfiguration af dobbeltskrivning fra Lifecycle Services](lcs-setup.md). Når opsætningen af forbindelsen er fuldført, sker følgende handlinger automatisk:

- Der klargøres et nyt tomt Finance and Operations-miljø.
- Der klargøres en ny tom forekomst af en kundeengagementapp, hvor den primære CRM-løsning er installeret.
- Der oprettes en forbindelse med to skrivninger for DAT-virksomhedsdata.
- Tabeltilknytninger er aktiveret til direkte synkronisering.

Begge miljøer er derefter klar til dynamisk datasynkronisering.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>En ny Finance and Operations-app-forekomst og en eksisterende forekomst af en kundeengagementapp

Hvis du vil oprette en forbindelse med dobbeltskrivning mellem en ny forekomst af en Finance and Operations-app, der ikke har data, og en eksisterende forekomst af en kundeengagementapp, skal du følge trinnene i [Konfiguration af dobbeltskrivning fra Lifecycle Services](lcs-setup.md). Når opsætningen af forbindelsen er fuldført, sker følgende handlinger automatisk:

- Der klargøres et nyt tomt Finance and Operations-miljø.
- Der oprettes en forbindelse med to skrivninger for DAT-virksomhedsdata.
- Tabeltilknytninger er aktiveret til direkte synkronisering.

Begge miljøer er derefter klar til dynamisk datasynkronisering.

Udfør følgende trin for at synkronisere Dataverse-data til Finance and Operations-appen.

1. Opret et nyt regnskab i Finance and Operations-appen.
2. Føj firmaet til opsætningen af forbindelsen med to skrivninger.
3. [Bootstrap](bootstrap-company-data.md) Dataverse-dataene ved hjælp af en ISO-virksomhedskode (International Organization for Standardization) på tre bogstaver.
4. Kør funktionen **Første synkronisering** for de tabeller, du vil synkronisere data for.

Du kan finde links til et eksempel og en alternativ fremgangsmåde i afsnittet [Eksempel](#example) senere i dette emne.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>En ny Finance and Operations-app-forekomst, som har data, og en ny forekomst af kundeengagementapp

Hvis du vil oprette en forbindelse med dobbeltskrivning mellem en ny forekomst af en Finance and Operations-app, der har data, og en ny forekomst af en kundeengagementapp, skal du følge trinnene i afsnittet [En ny Finance and Operations-app-forekomst og en ny forekomst af kundeengagementapp](#new-new) tidligere i dette emne. Når opsætningen af forbindelsen er fuldført, skal du udføre følgende trin, hvis du vil synkronisere dataene til kundeengagementappen.

1. Åbn Finance and Operations-appen fra siden LCS, log på, og gå derefter til **Datastyring \> To skrivninger**.
2. Kør funktionen **Første synkronisering** for de tabeller, du vil synkronisere data for.

Du kan finde links til et eksempel og en alternativ fremgangsmåde i afsnittet [Eksempel](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>En ny Finance and Operations-app-forekomst, som har data, og en eksisterende forekomst af kundeengagementapp

Hvis du vil oprette en forbindelse med dobbeltskrivning mellem en ny forekomst af en Finance and Operations-app, der har data, og en eksisterende forekomst af en kundeengagementapp, skal du følge trinnene i afsnittet [En ny Finance and Operations-app-forekomst og en eksisterende forekomst af kundeengagementapp](#new-existing) tidligere i dette emne. Når opsætningen af forbindelsen er fuldført, skal du udføre følgende trin, hvis du vil synkronisere dataene til kundeengagementappen.

1. Åbn Finance and Operations-appen fra siden LCS, log på, og gå derefter til **Datastyring \> To skrivninger**.
2. Kør funktionen **Første synkronisering** for de tabeller, du vil synkronisere data for.

Udfør følgende trin for at synkronisere Dataverse-data til Finance and Operations-appen.

1. Opret et nyt regnskab i Finance and Operations-appen.
2. Føj firmaet til opsætningen af forbindelsen med to skrivninger.
3. [Bootstrap](bootstrap-company-data.md) Dataverse-dataene ved hjælp af en ISO-virksomhedskode på tre bogstaver.
4. Kør funktionen **Første synkronisering** for de tabeller, du vil synkronisere data for.

Du kan finde links til et eksempel og en alternativ fremgangsmåde i afsnittet [Eksempel](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>En eksisterende Finance and Operations-app-forekomst og en ny forekomst af en kundeengagementapp

Opsætningen af en forbindelse med dobbeltskrivning mellem en eksisterende forekomst af en Finance and Operations-app og en ny forekomst af en kundeengagementapp forekommer i Finance and Operations-miljøet.

1. [Konfigurer forbindelsen fra Finance and Operations-appen](enable-dual-write.md).
2. Kør funktionen **Første synkronisering** for de tabeller, du vil synkronisere data for.

Du kan finde links til et eksempel og en alternativ fremgangsmåde i afsnittet [Eksempel](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>En eksisterende Finance and Operations-app-forekomst og en eksisterende forekomst af en kundeengagementapp

Opsætningen af en forbindelse med dobbeltskrivning mellem en eksisterende forekomst af en Finance and Operations-app og en eksisterende forekomst af en kundeengagementapp forekommer i Finance and Operations-miljøet.

1. [Konfigurer forbindelsen fra Finance and Operations-appen](enable-dual-write.md).
2. Hvis du vil synkronisere eksisterende Dataverse-data med Finance and Operations-appen, skal du udføre en [bootstrap](bootstrap-company-data.md) på Dataverse-dataene ved hjælp af en ISO-virksomhedskode på tre bogstaver.
3. Kør funktionen **Første synkronisering** for de tabeller, du vil synkronisere data for.

Du kan finde links til et eksempel og en alternativ fremgangsmåde i afsnittet [Eksempel](#example).

## <a name="example"></a>Eksempel

Du kan finde et eksempel under [Aktivering af Debitorer V3 – tabeltilknytningen Kontakter](enable-entity-map.md#enable-table-map)

Du kan finde en alternativ fremgangsmåde, der er baseret på datamængder i de enkelte enheder, der skal køre den første synkronisering, under [Overvejelser ved første synkronisering](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]