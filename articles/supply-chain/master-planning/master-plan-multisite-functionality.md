---
title: Oversigt over varedisponering og funktionen til flere lokationer
description: Den overordnede planlægning tager indretningen af stedet og lagerstedets og lagerets dimensioner i betragtning.
author: roxanadiaconu
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e30bb8dfb790958b30cb3be807847ee737fb5026
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833563"
---
# <a name="master-planning-and-multisite-functionality-overview"></a>Oversigt over varedisponering og funktionen til flere lokationer

[!include [banner](../includes/banner.md)]

Den overordnede planlægning tager indretningen af stedet og lagerstedets og lagerets dimensioner i betragtning. 

Dimensionen for lokation er obligatorisk, og du kan angive, at dimensionen for lagersted skal være obligatorisk.

Når en dimension er obligatorisk, skal der angives en dimensionsværdi på alle lagertransaktioner. Under overordnet planlægning er lokationen og lagerstedet for den første efterspørgsel derfor kendt. Dimensionen for lokation er også ensartet, så lokationsværdien ikke ændres ved udfoldning af efterspørgsel på lavere niveau.

Når lagerstedet ikke er indstillet til obligatorisk, kendes det muligvis ikke fra den første efterspørgsel. Planlægningssystemet skal afgøre, hvilket lagersted der skal bruges ud fra de indstillinger, der er defineret for varen, individuelle lagersteder og detaljerne i ordrelinjen.

Følgende emner beskriver, hvordan planlægningssystemet fungerer, når der defineres forskellige indstillinger for at afgøre, hvilket lagersted der skal bruges.

[Varedisponering for lokalitets- og lagerdisponering, obligatorisk lagersted](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Varedisponering for lokalitetsdisponering, obligatorisk lagersted](master-plan-site-coverage-warehouse-mandatory.md)

[Varedisponering for lokalitets- og lagerdisponering, lagersted ikke obligatorisk](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Varedisponering for lokalitetsdisponering, lagersted ikke obligatorisk](master-plan-site-coverage-warehouse-not-mandatory.md)

[Bestemme styklisteversionen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]