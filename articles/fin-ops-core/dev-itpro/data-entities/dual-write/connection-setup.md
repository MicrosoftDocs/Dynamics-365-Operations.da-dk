---
title: Vejledning i konfiguration af dobbeltskrivning
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
ms.openlocfilehash: 2d77a1458f3f4c79b231e6a6d7cc320b8ee1fad9
ms.sourcegitcommit: ee643d651d57560bccae2f99238faa39881f5c64
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088500"
---
# <a name="guidance-for-how-to-set-up-dual-write"></a>Vejledning i konfiguration af dobbeltskrivning

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Du kan oprette en forbindelse med to skrivninger mellem et Finance and Operations-miljø og et Common Data Service-miljø.

+ Et **Finance and Operations-miljø** leverer den underliggende platform for **Finance and Operations-apps** (f.eks Microsoft Dynamics 365 Finance. Dynamics 365 Supply Chain Management og Dynamics 365 Retail).
+ Et **Common Data Service-miljø** giver den underliggende platform for **kundeengagementapps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).

>[!IMPORTANT]
>Human Resources i Finance and Operations understøtter dobbeltskrivningsforbindelser, men Dynamics 365 Human Resources-appen gør ikke.

Konfigurationsmekanismen varierer, afhængigt af dit abonnement og miljøet.

+ Ved nye forekomster af Finance and Operations-apps begynder opsætningen af en forbindelse med to skrivninger i Microsoft Dynamics Lifecycle Services (LCS). Hvis du har en licens til Power Platform, vil du få et nyt Common Data Service-miljø, hvis din lejer ikke har en.
+ For eksisterende forekomster af Finance and Operations-apps begynder opsætningen af en forbindelse med to skrivninger i Finance and Operations-miljøet.

Før du starter dobbeltskrivning på en enhed, kan du køre en indledende synkronisering for at håndtere eksisterende data på begge sider af Finance and Operations-apps og kundeengagementapps. Du kan springe den første synkronisering over, hvis du ikke har brug for at synkronisere data mellem de to miljøer.

Ved hjælp af en første synkronisering kan du kopiere eksisterende data fra én app til en anden tovejs. Der er flere forskellige opsætningsscenarier, afhængigt af hvilke miljøer du allerede har, og hvilken type data der er i miljøerne.

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
- Enhedstilknytninger er aktiveret til direkte synkronisering.

Begge miljøer er derefter klar til dynamisk datasynkronisering.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>En ny Finance and Operations-app-forekomst og en eksisterende forekomst af en kundeengagementapp

Hvis du vil oprette en forbindelse med dobbeltskrivning mellem en ny forekomst af en Finance and Operations-app, der ikke har data, og en eksisterende forekomst af en kundeengagementapp, skal du følge trinnene i [Konfiguration af dobbeltskrivning fra Lifecycle Services](lcs-setup.md). Når opsætningen af forbindelsen er fuldført, sker følgende handlinger automatisk:

- Der klargøres et nyt tomt Finance and Operations-miljø.
- Der oprettes en forbindelse med to skrivninger for DAT-virksomhedsdata.
- Enhedstilknytninger er aktiveret til direkte synkronisering.

Begge miljøer er derefter klar til dynamisk datasynkronisering.

Udfør følgende trin for at synkronisere Common Data Service-data til Finance and Operations-appen.

1. Opret et nyt regnskab i Finance and Operations-appen.
2. Føj firmaet til opsætningen af forbindelsen med to skrivninger.
3. [Bootstrap](bootstrap-company-data.md) Common Data Service-dataene ved hjælp af en ISO-virksomhedskode (International Organization for Standardization) på tre bogstaver.
4. Kør den **første synkroniseringsfunktion** for de enheder, du vil synkronisere data for.

Du kan finde et eksempel og en alternativ fremgangsmåde i [Eksempel](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>En ny Finance and Operations-app-forekomst, som har data, og en ny forekomst af kundeengagementapp

Hvis du vil oprette en forbindelse med dobbeltskrivning mellem en ny forekomst af en Finance and Operations-app, der har data, og en ny forekomst af en kundeengagementapp, skal du følge trinnene i afsnittet [En ny Finance and Operations-app-forekomst og en ny forekomst af kundeengagementapp](#new-new) tidligere i dette emne. Når opsætningen af forbindelsen er fuldført, skal du udføre følgende trin, hvis du vil synkronisere dataene til kundeengagementappen.

1. Åbn Finance and Operations-appen fra siden LCS, log på, og gå derefter til **Datastyring \> To skrivninger**.
2. Kør den **første synkroniseringsfunktion** for de enheder, du vil synkronisere data for.

Du kan finde et eksempel og en alternativ fremgangsmåde i [Eksempel](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>En ny Finance and Operations-app-forekomst, som har data, og en eksisterende forekomst af kundeengagementapp

Hvis du vil oprette en forbindelse med dobbeltskrivning mellem en ny forekomst af en Finance and Operations-app, der har data, og en eksisterende forekomst af en kundeengagementapp, skal du følge trinnene i afsnittet [En ny Finance and Operations-app-forekomst og en eksisterende forekomst af kundeengagementapp](#new-existing) tidligere i dette emne. Når opsætningen af forbindelsen er fuldført, skal du udføre følgende trin, hvis du vil synkronisere dataene til kundeengagementappen.

1. Åbn Finance and Operations-appen fra siden LCS, log på, og gå derefter til **Datastyring \> To skrivninger**.
2. Kør den **første synkroniseringsfunktion** for de enheder, du vil synkronisere data for.

Udfør følgende trin for at synkronisere Common Data Service-data til Finance and Operations-appen.

1. Opret et nyt regnskab i Finance and Operations-appen.
2. Føj firmaet til opsætningen af forbindelsen med to skrivninger.
3. [Bootstrap](bootstrap-company-data.md) Common Data Service-dataene ved hjælp af en ISO-virksomhedskode på tre bogstaver.
4. Kør den **første synkroniseringsfunktion** for de enheder, du vil synkronisere data for.

Du kan finde et eksempel og en alternativ fremgangsmåde i [Eksempel](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>En eksisterende Finance and Operations-app-forekomst og en ny forekomst af en kundeengagementapp

Opsætningen af en forbindelse med dobbeltskrivning mellem en eksisterende forekomst af en Finance and Operations-app og en ny forekomst af en kundeengagementapp forekommer i Finance and Operations-miljøet.

1. [Konfigurer forbindelsen fra Finance and Operations-appen](enable-dual-write.md).
2. Kør den **første synkroniseringsfunktion** for de enheder, du vil synkronisere data for.

Du kan finde et eksempel og en alternativ fremgangsmåde i [Eksempel](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>En eksisterende Finance and Operations-app-forekomst og en eksisterende forekomst af en kundeengagementapp

Opsætningen af en forbindelse med dobbeltskrivning mellem en eksisterende forekomst af en Finance and Operations-app og en eksisterende forekomst af en kundeengagementapp forekommer i Finance and Operations-miljøet.

1. Konfigurer forbindelsen fra Finance and Operations-appen.
2. Hvis du vil synkronisere eksisterende Common Data Service-data med Finance and Operations-appen, skal du udføre en [bootstrap](bootstrap-company-data.md) på Common Data Service-dataene ved hjælp af en ISO-virksomhedskode på tre bogstaver.
3. Kør den **første synkroniseringsfunktion** for de enheder, du vil synkronisere data for.

Du kan finde et eksempel og en alternativ fremgangsmåde i [Eksempel](#example).

## <a name="example"></a>Eksempel

Du kan finde et eksempel under [Aktivering af Debitorer V3 – tilknytning af kontaktenhed](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)

Du kan finde en alternativ fremgangsmåde på basis af datamængder i de enkelte enheder, der skal køre den første synkronisering, under [Overvejelser ved første synkronisering](initial-sync-guidance.md).
