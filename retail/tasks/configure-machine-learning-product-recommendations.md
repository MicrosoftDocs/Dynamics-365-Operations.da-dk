--- 
title: "Konfigurere produktanbefalinger, der er baseret på maskinel indlæring"
description: "Denne procedure opdaterer de data i enheden, der bruges af systemet til maskinel ind læring, som er baseret på produktanbefalingerne, og derefter aktiveres produktanbefalinger på POS-klienter."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: c51c5f82efb50db1e238f4046506920975f33218
ms.contentlocale: da-dk
ms.lasthandoff: 07/28/2017

---
# <a name="configure-machine-learning-powered-product-recommendations"></a>Konfigurere produktanbefalinger, der er baseret på maskinel indlæring

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne procedure opdaterer de data i enheden, der bruges af systemet til maskinel ind læring, som er baseret på produktanbefalingerne, og derefter aktiveres produktanbefalinger på POS-klienter. Denne procedure bruger USRT-firmaets demodata.

1. Gå til Systemadministration > Opsætning > Enhedslager.
2. Find og vælg den posten 'RetailSales' på listen.
3. Klik på Opdater.
4. Klik på OK.
5. Luk siden.
6. Gå til Detail og handel > Konfiguration af hovedkontor > Parametre > Detailparametre.
7. Klik på fanen Maskinel indlæring.
8. Vælg 'Ja' i feltet Aktivér produktanbefalinger.
    * Hvis du modtager meddelelsen "Anbefalingsmodellerne blev ikke hentet", skyldes det, at du har opdateret enhedslageret for nylig, og systemet er måske ikke færdig med at samle de nye data. Vent 2-3 timer, og prøv igen.  
9. Klik på Gem.
10. Luk siden.


