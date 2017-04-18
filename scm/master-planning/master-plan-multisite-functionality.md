---
title: Varedisponering og funktionen til flere lokationer
description: "Den overordnede planlægning tager indretningen af stedet og lagerstedets og lagerets dimensioner i betragtning."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 19eeee753c15cf2670948ce2c615a112813c16ad
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-and-multisite-functionality"></a>Varedisponering og funktionen til flere lokationer

Den overordnede planlægning tager indretningen af stedet og lagerstedets og lagerets dimensioner i betragtning. 

Dimensionen for lokation er obligatorisk, og du kan angive, at dimensionen for lagersted skal være obligatorisk.

Når en dimension er obligatorisk, skal der angives en dimensionsværdi på alle lagertransaktioner. Under overordnet planlægning er lokationen og lagerstedet for den første efterspørgsel derfor kendt. Dimensionen for lokation er også ensartet, så lokationsværdien ikke ændres ved udfoldning af efterspørgsel på lavere niveau.

Når lagerstedet ikke er indstillet til obligatorisk, kendes det muligvis ikke fra den første efterspørgsel. Planlægningssystemet skal afgøre, hvilket lagersted der skal bruges ud fra de indstillinger, der er defineret for varen, individuelle lagersteder og detaljerne i ordrelinjen.

Følgende wiki-artikler beskriver, hvordan planlægningssystemet fungerer, når der defineres forskellige indstillinger for at afgøre, hvilket lagersted der skal bruges.

[Overordnet planlægning – lokations- og lagerdisponering, lagersted er obligatorisk](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Overordnet planlægning – lokalitetsdisponering, lagersted er obligatorisk](master-plan-site-coverage-warehouse-mandatory.md)

[Overordnet planlægning – lokations- og lagerdisponering, lagersted er ikke obligatorisk](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Overordnet planlægning – lokalitetsdisponering, lagersted er ikke obligatorisk](master-plan-site-coverage-warehouse-not-mandatory.md)

[Overordnet planlægning – sådan bestemmes styklisteversionen](master-plan-bom-version-determined.md)

