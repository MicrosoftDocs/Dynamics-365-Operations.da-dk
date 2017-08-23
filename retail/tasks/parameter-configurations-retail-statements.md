--- 
title: "Parameterkonfigurationer for detailopgørelser"
description: "Denne procedure viser konfigurationer for detailparametre, der påvirker, hvordan detailopgørelser oprettes og bogføres."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: ba3b528f8739e4e84ffdbeea5d0af5817f2d9c10
ms.contentlocale: da-dk
ms.lasthandoff: 07/28/2017

---
# <a name="parameter-configurations-for-retail-statements"></a>Parameterkonfigurationer for detailopgørelser

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne procedure viser konfigurationer for detailparametre, der påvirker, hvordan detailopgørelser oprettes og bogføres. Denne procedure bruger demofirmaet USRT.

1. Gå til Detail og handel > Konfiguration af hovedkontor > Parametre > Detailparametre.
2. Klik på fanen Bogføring.
    * Vælg "Ja", hvis du specifikt vil bogføre de periodiske rabatbeløb.  
    * Vælg "Standard" for at bruge standardkonti, eller Vælg "Periodisk", hvis du vil angive, hvilken konto der skal bruges til hver periodisk rabat.  
    * Vælg "Oversigt", hvis lagerlinjer skal samles, når det er muligt.  
    * Vælg "Ja", hvis fakturaer og betalinger bør udlignes automatisk som en del af processen til bogføring af opgørelser.  
    * Vælg "Ja", hvis transaktioner med deponering til pengeskab skal samles.  
    * Vælg "Ja", hvis transaktioner med indsættelse i banken skal samles.  
    * Vælg "Ja" for at aktivere sammenlægning for bogføring af opgørelsen.  
    * Vælg "Ja" for at oprette og behandle ordrer parallelt, når opgørelser bogføres.  
    * Angiv de maksimale ordrer, skal behandles i hver batchjobopgave.  
3. Klik på Gem.


