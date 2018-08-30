--- 
title: "Konfigurere parametre for Retail, der påvirker detailopgørelser"
description: "Denne procedure viser konfigurationer for detailparametre, der påvirker, hvordan detailopgørelser oprettes og bogføres."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: ff12587d8332801131d5b0cac84e0db38f8f6142
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="configure-retail-parameters-that-affect-retail-statements"></a>Konfigurere parametre for Retail, der påvirker detailopgørelser

[!include [task guide banner](../includes/task-guide-banner.md)]

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


