---
title: Vejledning i opsætning af dobbeltskrivning
description: Denne artikel beskriver de scenarier, der understøttes til installation med to skrivninger.
author: RamaKrishnamoorthy
ms.date: 06/28/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 15dfb609b5e25b4faf2b913cc2310df71c88a74d
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111243"
---
# <a name="guidance-for-dual-write-setup"></a>Vejledning i opsætning af dobbeltskrivning

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



Du kan oprette en forbindelse med dobbeltskrivning mellem et finans- og driftsmiljø og et Dataverse-miljø.

+ Et **finans- og driftsmiljø** leverer den underliggende platform for **programmer til finans og drift** (f.eks Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce og Dynamics 365 Human Resources).
+ Et **Dataverse-miljø** giver den underliggende platform for **modelbaserede apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).


> [!IMPORTANT]
> Modulet Human Resources i Dynamics 365 Finance understøtter dobbeltskrivningsforbindelser, men Dynamics 365 Human Resources-appen gør ikke.

Konfigurationsmekanismen varierer, afhængigt af dit abonnement og miljøet:

+ Ved nye forekomster af programmer til finans og drift begynder opsætningen af dobbeltskrivningsforbindelsen i Microsoft Dynamics Lifecycle Services (LCS). Hvis du har en licens til Microsoft Power Platform, vil du få et nyt Dataverse-miljø, hvis din lejer ikke har en.
+ Ved eksisterende forekomster af programmer til finans og drift begynder opsætningen af dobbeltskrivningsforbindelsen i finans- og driftsmiljøet.

Før du starter dobbeltskrivning på en enhed, kan du køre en indledende synkronisering for at håndtere eksisterende data på begge sider: Programmer til finans og drift og kundeengagementsapps. Du kan springe den første synkronisering over, hvis du ikke har brug for at synkronisere data mellem de to miljøer.

Ved hjælp af en første synkronisering kan du kopiere eksisterende data fra én app til en anden tovejs. Der er flere forskellige opsætningsscenarier, afhængigt af hvilke miljøer du allerede har, og hvilken type data der er i dem.

Følgende konfigurationsscenarier understøttes:

+ [Et nyt program til finans og drift-forekomst og en ny forekomst af en kundeengagementsapp](#new-new)
+ [Et nyt program til finans og drift-forekomst og en eksisterende forekomst af en kundeengagementsapp](#new-existing)
+ [Et nyt program til finans og drift-forekomst, som har data, og en ny forekomst af kundeengagementsapp](#new-data-new)
+ [Et nyt program til finans og drift-forekomst, som har data, og en eksisterende forekomst af kundeengagementsapp](#new-data-existing)
+ [Et eksisterende program til finans og drift-forekomst og en ny forekomst af en kundeengagementsapp](#existing-new)
+ [Et eksisterende program til finans og drift-forekomst og en eksisterende forekomst af en kundeengagementsapp](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>Et nyt program til finans og drift-forekomst og en ny forekomst af en kundeengagementsapp

Hvis du vil oprette en forbindelse med dobbeltskrivning mellem en ny forekomst af et program til finans og drift, der ikke har data, og en ny forekomst af en kundeengagementsapp, skal du følge trinnene i [Konfiguration af dobbeltskrivning fra Lifecycle Services](lcs-setup.md). Når opsætningen af forbindelsen er fuldført, sker følgende handlinger automatisk:

- Der klargøres et nyt tomt finans og drift-miljø.
- Der klargøres en ny tom forekomst af en kundeengagementapp, hvor den primære CRM-løsning er installeret.
- Der oprettes en forbindelse med to skrivninger for DAT-virksomhedsdata.
- Tabeltilknytninger er aktiveret til direkte synkronisering.

Begge miljøer er derefter klar til dynamisk datasynkronisering.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>Et nyt program til finans og drift-forekomst og en eksisterende forekomst af en kundeengagementsapp

Hvis du vil oprette en forbindelse med dobbeltskrivning mellem en ny forekomst af et program til finans og drift, der ikke har data, og en eksisterende forekomst af en kundeengagementsapp, skal du følge trinnene i [Konfiguration af dobbeltskrivning fra Lifecycle Services](lcs-setup.md). Når opsætningen af forbindelsen er fuldført, sker følgende handlinger automatisk:

- Der klargøres et nyt tomt finans og drift-miljø.
- Der oprettes en forbindelse med to skrivninger for DAT-virksomhedsdata.
- Tabeltilknytninger er aktiveret til direkte synkronisering.

Begge miljøer er derefter klar til dynamisk datasynkronisering.

Udfør følgende trin for at synkronisere Dataverse-data til programmet til finans og drift.

1. Opret et nyt firma i programmet til finans og drift.
2. Føj firmaet til opsætningen af forbindelsen med to skrivninger.
3. [Bootstrap](bootstrap-company-data.md) Dataverse-dataene ved hjælp af en ISO-virksomhedskode (International Organization for Standardization) på tre bogstaver.
4. Kør funktionen **Første synkronisering** for de tabeller, du vil synkronisere data for.

Du kan finde links til et eksempel og en alternativ fremgangsmåde i afsnittet [Eksempel](#example) senere i denne artikel.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>Et nyt program til finans og drift-forekomst, som har data, og en ny forekomst af kundeengagementsapp

Hvis du vil oprette en forbindelse med dobbeltskrivning mellem en ny forekomst af et program til finans og drift, der har data, og en ny forekomst af en kundeengagementsapp, skal du følge trinnene i afsnittet [Et nyt program til finans og drift-forekomst og en ny forekomst af kundeengagementsapp](#new-new) tidligere i denne artikel. Når opsætningen af forbindelsen er fuldført, skal du udføre følgende trin, hvis du vil synkronisere dataene til kundeengagementappen.

1. Åbn programmet til finans og drift fra siden LCS, log på, og gå derefter til **Datastyring \> Dobbeltskrivning**.
2. Kør funktionen **Første synkronisering** for de tabeller, du vil synkronisere data for.

Du kan finde links til et eksempel og en alternativ fremgangsmåde i afsnittet [Eksempel](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>Et nyt program til finans og drift-forekomst, som har data, og en eksisterende forekomst af kundeengagementsapp

Hvis du vil oprette en forbindelse med dobbeltskrivning mellem en ny forekomst af et program til finans og drift, der har data, og en eksisterende forekomst af en kundeengagementsapp, skal du følge trinnene i afsnittet [Et nyt program til finans og drift-forekomst og en eksisterende forekomst af kundeengagementsapp](#new-existing) tidligere i denne artikel. Når opsætningen af forbindelsen er fuldført, skal du udføre følgende trin, hvis du vil synkronisere dataene til kundeengagementappen.

1. Åbn programmet til finans og drift fra siden LCS, log på, og gå derefter til **Datastyring \> Dobbeltskrivning**.
2. Kør funktionen **Første synkronisering** for de tabeller, du vil synkronisere data for.

Udfør følgende trin for at synkronisere Dataverse-data til programmet til finans og drift.

1. Opret et nyt firma i programmet til finans og drift.
2. Føj firmaet til opsætningen af forbindelsen med to skrivninger.
3. [Bootstrap](bootstrap-company-data.md) Dataverse-dataene ved hjælp af en ISO-virksomhedskode på tre bogstaver.
4. Kør funktionen **Første synkronisering** for de tabeller, du vil synkronisere data for.

Du kan finde links til et eksempel og en alternativ fremgangsmåde i afsnittet [Eksempel](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>Et eksisterende program til finans og drift-forekomst og en ny forekomst af en kundeengagementsapp

Opsætningen af en forbindelse med dobbeltskrivning mellem en eksisterende forekomst af et program til finans og drift og en ny forekomst af en kundeengagementsapp forekommer i Finans- og driftsmiljøet.

1. [Konfigurer forbindelsen fra programmet til finans og drift](enable-dual-write.md).
2. Kør funktionen **Første synkronisering** for de tabeller, du vil synkronisere data for.

Du kan finde links til et eksempel og en alternativ fremgangsmåde i afsnittet [Eksempel](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>Et eksisterende program til finans og drift-forekomst og en eksisterende forekomst af en kundeengagementsapp

Opsætningen af en forbindelse med dobbeltskrivning mellem en eksisterende forekomst af program til finans og drifts og en eksisterende forekomst af en kundeengagementsapp forekommer i Finans- og driftsmiljøet.

1. [Konfigurer forbindelsen fra programmet til finans og drift](enable-dual-write.md).
2. Hvis du vil synkronisere eksisterende Dataverse-data med programmet til finans og drift, skal du udføre en [bootstrap](bootstrap-company-data.md) på Dataverse-dataene ved hjælp af en ISO-firmakode på tre bogstaver.
3. Kør funktionen **Første synkronisering** for de tabeller, du vil synkronisere data for.

Du kan finde links til et eksempel og en alternativ fremgangsmåde i afsnittet [Eksempel](#example).

## <a name="example"></a>Eksempel

Du kan finde et eksempel under [Aktivering af Debitorer V3 – tabeltilknytningen Kontakter](enable-entity-map.md#enable-table-map)

Du kan finde en alternativ fremgangsmåde, der er baseret på datamængder i de enkelte enheder, der skal køre den første synkronisering, under [Overvejelser ved første synkronisering](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
