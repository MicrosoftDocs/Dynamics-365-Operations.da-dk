---
title: Konfigurere parametre, som påvirker detailopgørelser
description: Dette emne viser konfigurationer for Commerce-parametre, der påvirker, hvordan opgørelser oprettes og bogføres.
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
ms.openlocfilehash: 7892a216d836ebcc297a5b7eb87bc996dd9b91bf
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140825"
---
# <a name="configure-parameters-that-affect-retail-statements"></a>Konfigurere parametre, som påvirker detailopgørelser

[!include [banner](../includes/banner.md)]

Dette emne viser konfigurationer for Commerce-parametre, der påvirker, hvordan opgørelser oprettes og bogføres. Denne procedure bruger demofirmaet USRT.

1. I navigationsruden skal du gå til **Moduler > Retail og Commerce > Konfiguration af hovedkontor > Parametre > Commerce-parametre**.
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

