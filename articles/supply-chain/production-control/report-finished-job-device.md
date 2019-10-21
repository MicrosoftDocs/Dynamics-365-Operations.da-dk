---
title: Færdigmelde til en id-kontrolleret lokation fra jobkortenheden
description: Dette emne beskriver processen til fuldførelse af færdigvarer på en produktionsordre til et lager, når et id styrer lokationen.
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 35ad27a6b8a52bfd086fbe4fc57b1681ff88fd5b
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/11/2019
ms.locfileid: "1995136"
---
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Færdigmelde til en id-kontrolleret lokation fra jobkortenheden 

Den proces, der kaldes færdigmelding, fuldfører færdigvarerne på en produktionsordre til lageret. Hvis det færdige produkt er aktiveret til de avancerede lagerprocesser, færdigmeldes produktet til en lokation, der kaldes udlagringslokationen for produktionen. Du kan finde oplysninger om, hvordan du konfigurerer udlagringslokationen for produktionen, under [Produktionsudlagringslokation](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

Du skal vælge et eksisterende id-nummer for at udføre denne opgave. Hvis produktionsudlagringslokationen er konfigureret til at blive sporet på basis af id, skal id-nummeret inkluderes, når produktionsudlagringslokationen færdigmeldes. Feltet **Id** vises i prompten **Rapport i gang** på siden **Jobkortenhed**. Feltet er kun synligt i prompten **Rapport i gang**, når der rapporteres for den sidste operation i produktionsordren. Feltet vises kun, hvis varen for produktionsordren er aktiveret til lokationsstyringsprocesserne. 
