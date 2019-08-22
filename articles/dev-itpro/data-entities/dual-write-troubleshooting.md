---
title: Fejlfindingsvejledning til dataintegration
description: Dette emne indeholder fejlfindingsoplysninger om dataintegration mellem Microsoft Dynamics 365 for Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797269"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Fejlfindingsvejledning til dataintegration

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a>Aktivere plug-in-sporing i Common Data Service, og se fejldetaljerne for dobbeltskrivnings-plug-in

Hvis du står over for et problem eller en fejl i synkronisering med dobbeltskrivning, kan du undersøge fejlene i sporingsloggen:

1. Før du kan inspicere fejlene, skal du aktivere plug-in-sporing ved hjælp af instruktionerne i [Registrere plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs). Nu kan du inspicere fejlene.
2. Log på Dynamics 365 for Sales.
3. Klik på indstillingsikonet (et tandhjul), og vælg **Avancerede indstillinger**.
4. I menuen **Indstillinger** skal du vælge **Tilpasning > Plug-in-sporingslogfil**.
5. Klik på typenavnet **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** for at få vist fejloplysningerne.

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a>Kontrollere fejl ved dobbeltskrivningssynkronisering i Finance and Operations

Du kan kontrollere fejlene under testen ved at følge disse trin:

+ Log på LifeCycle Services (LCS).
+ Åbn det LCS-projekt, du har valgt til at udføre dobbeltskrivningstest.
+ Gå til Skybaserede miljøer.
+ Fjernskrivebord til Finance and Operations-VM ved hjælp af lokal konto, der vises i LCS.
+ Åbn logbogen. 
+ Naviger til **Logfiler for programmer og tjenester > Microsoft > Dynamics AX-DualWriteSync > Operationel**. Fejlene og detaljerne vises.

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a>Sådan frakobler og tilknytter du et andet Common Data Service-miljø fra Finance and Operations

Du kan opdatere links ved at følge disse trin:

+ Naviger til Finance and Operations-miljøet.
+ Åbn Datastyring.
+ Klik på **Link til CDS for Apps**.
+ Vælg alle de kørende tilknytninger, og klik på **Stop**. 
+ Vælg alle tilknytninger, og klik på **Slet**.

    > [!NOTE]
    > Indstillingen **Slet** vises ikke, hvis skabelonen **CustomerV3-Account** er valgt. Fjern markeringen af den, hvis det er nødvendigt. **CustomerV3-Account** er en ældre klargjort skabelon, der virker sammen med løsningen Kundeemne til kontant. Fordi den er globalt frigivet, dukker den op under alle skabeloner.

+ Klik på **Ophæv sammenkædning af miljø**.
+ Klik på **Ja** for at bekræfte.
+ Følg trinnene i [installationsvejledningen](https://aka.ms/dualwrite-docs) for at tilknytte det nye miljø.

