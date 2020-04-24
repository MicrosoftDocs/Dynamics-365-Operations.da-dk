---
title: Færdigmelde til en id-kontrolleret lokation fra jobkortenheden
description: I dette emne beskrives processen til fuldførelse af færdigvarer på en produktionsordre til et lager, når et id styrer lokationen.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: f5863202facc83afb91b380ba5666334783ccbcf
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211163"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Færdigmelde til en id-kontrolleret lokation fra jobkortenheden 

Den proces, der kaldes færdigmelding, fuldfører færdigvarerne på en produktionsordre til lageret. Hvis det færdige produkt er aktiveret til de avancerede lagerprocesser, færdigmeldes produktet til en lokation, der kaldes udlagringslokationen for produktionen. Du kan finde oplysninger om, hvordan du konfigurerer udlagringslokationen for produktionen, under [Produktionsudlagringslokation](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

Hvis udlagringslokationen for produktionen er kontrolleret af nummerplader, skal der angives en nummerplade, når færdigmeldingen rapporteres. Feltet **Id** vises i prompten **Rapport i gang** på siden **Jobkortenhed**. Feltet er kun synligt i prompten **Rapportfremgang**, når der rapporteres om den sidste operation i produktionsordren, og varen til produktionsordren er aktiveret for lagerstedets styringsprocesser. 

Der er to muligheder for at angive nummerpladen
- Brugeren vælger et eksisterende nummerpladenummer i feltet nummerplade.
- Nummerpladenummeret genereres automatisk fra en nummerserie og nulstilles til nummerpladefeltet.

Muligheden for automatisk at oprette nummerpladen konfigureres ved at vælge indstillingen **Generer nummerplade** på siden **Konfigurer jobkort for enheder**.
