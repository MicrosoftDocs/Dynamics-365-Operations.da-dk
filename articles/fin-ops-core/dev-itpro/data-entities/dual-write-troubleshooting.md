---
title: Fejlfindingsvejledning til dataintegration
description: Dette emne indeholder fejlfindingsoplysninger for dataintegration mellem Finance and Operations-apps og Common Data Service.
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
ms.openlocfilehash: 35c0a1e6342008bc2ee6ff25a1663e199c8cb985
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771019"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Fejlfindingsvejledning til dataintegration

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a>Aktivere plug-in-sporingslogge i Common Data Service og se fejldetaljerne for dobbeltskrivnings-plug-in

[!include [banner](../includes/banner.md)]

Hvis du oplever problemer eller fejl under dobbeltskrivningssynkronisering, skal du følge disse trin for at undersøge fejlene i sporingslogfilen.

1. Før du kan kontrollere fejlene, skal du aktivere sporingslogge til plug-ins. Du kan finde instruktioner i afsnittet "Vise sporingslogfiler" [Selvstudium: skrive og registrere en plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).

    Nu kan du inspicere fejlene.

2. Log på Microsoft Dynamics 365 Sales.
3. Vælg knappen **Indstillinger** (tandhjulsymbolet), og vælg derefter **Avancerede indstillinger**.
4. I menuen **Indstillinger** skal du vælge **Tilpasning \> Plug-in-sporingslogfil**.
5. Vælg typenavnet **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** for at få vist fejloplysningerne.

## <a name="inspect-dual-write-synchronization-errors"></a>Undersøg synkroniseringsfejl ved dobbeltskrivning

Udfør følgende trin for at kontrollere fejl under testen.

1. Log på Microsoft Dynamics LifeCycle Services (LCS).
2. Åbn det LCS-projekt, du vil udføre dobbeltskrivningstest for.
3. Vælg **Skybaserede miljøer**.
4. Opret en fjernskrivebordsforbindelse til programmets virtuelle maskine (VM) ved hjælp af en lokal konto, der vises i LCS.
5. Åbn Logbog. 
6. Gå til **Logfiler for programmer og tjenester \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operationel**. Fejlene og detaljerne vises.

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a>Frakoble ét Common Data Service-miljø fra programmet og tilknytte et andet miljø

Hvis du vil opdatere links, skal du følge disse trin.

1. Gå til programmiljøet.
2. Åbn Datastyring.
3. Vælg **Link til CDS for Apps**.
4. Markér alle de tilknytninger, der kører, og vælg derefter **Stop**.
5. Vælg alle tilknytninger, og vælge derefter **Slet**.

    > [!NOTE]
    > Indstillingen **Slet** er ikke tilgængelig, hvis skabelonen **CustomerV3-Account** er valgt. Fjern markeringen af denne skabelon efter behov. **CustomerV3-Account** er en ældre klargjort skabelon, der virker sammen med løsningen Kundeemne til kontant. Fordi den er globalt frigivet, dukker den op under alle skabeloner.

6. Vælg **Ophæv sammenkædning af miljø**.
7. Vælg **Ja** for at bekræfte operationen.
8. Følg trinnene i [installationsvejledningen](https://aka.ms/dualwrite-docs) for at tilknytte det nye miljø.
