---
title: Konfigurere Detailparametre, som påvirker detailopgørelser
description: Dette emne viser konfigurationer for detailparametre, der påvirker, hvordan detailopgørelser oprettes og bogføres.
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b9a0386a4d61395903e82d988244dd131c1febaf
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867265"
---
# <a name="configure-retail-parameters-that-affect-retail-statements"></a>Konfigurere Detailparametre, som påvirker detailopgørelser

[!include[task guide banner](../includes/task-guide-banner.md)]

Dette emne viser konfigurationer for detailparametre, der påvirker, hvordan detailopgørelser oprettes og bogføres. Denne procedure bruger demofirmaet USRT.

1. I navigationsruden skal du gå til **Moduler > Detail og handel > Konfiguration af hovedkontor > Parametre > Detailparametre**.
2. Vælg fanen **Bogføring**.
    - Vælg **Ja**, hvis du specifikt vil bogføre de periodiske rabatbeløb.  
    - Vælg **Standard** for at bruge standardkonti, eller vælg **Periodisk**, hvis du vil angive, hvilken konto der skal bruges til hver periodisk rabat.  
      - Vælg **Oversigt**, hvis lagerlinjer skal samles, når det er muligt.  
      - Vælg **Ja**, hvis fakturaer og betalinger bør udlignes automatisk som en del af processen til bogføring af opgørelser.  
      - Vælg **Ja**, hvis transaktioner med deponering til pengeskab skal samles.  
      - Vælg **Ja**, hvis transaktioner med indsættelse i banken skal samles.  
      - Vælg **Ja** for at aktivere sammenlægning for bogføring af opgørelsen.  
      - Vælg **Ja** for at oprette og behandle ordrer parallelt, når opgørelser bogføres.  
      - Angiv de maksimale ordrer, skal behandles i hver batchjobopgave.  
3. Vælg **Gem**.

