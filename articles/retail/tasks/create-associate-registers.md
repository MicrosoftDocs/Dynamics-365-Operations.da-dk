--- 
title: " Oprette og tilknytte registre"
description: "Denne fremgangsmåde viser, hvordan du kan oprette en POS-kasse."
author: rubencdelgado
manager: AnnBe
ms.date: 10/05/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 1de4e71fd554ba0486a5d2f65803f0806df37fe4
ms.contentlocale: da-dk
ms.lasthandoff: 02/07/2018

---
# <a name="create-and-associate-registers"></a> Oprette og tilknytte registre

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du kan oprette en POS-kasse. Denne procedure bruger demodatafirmaet USRT.

1. Gå til Detail og handel > Konfiguration af kanal > POS-opsætning > Kasseapparater.
2. Klik på Ny.
3. Indtast et id til den nye kasse i feltet Kassenummer.
    * Kasse-id'et indeholder typisk koder, der kan hjælpe med at knytte kassen til den butik, som den tilhører, og placeringen i butikken.  
4. Skriv et beskrivende navn til kassen i feltet Navn.
5. Indtast eller vælg en værdi i feltet Butiksnummer.
6. Indtast eller vælg en værdi i feltet Hardwareprofil.
    * Hardwareprofiler bruges til at angive detailenheder, der skal knyttes til kassen, f.eks. pengeskuffen og bonprinteren.  
7. Indtast eller vælg en værdi i feltet Visuel profil.
    * Visuelle profiler bruges til at angive de billeder, der bruges i POS-baggrunden og på logonside samt temaer for POS.  
8. Skriv en værdi i feltet Autorisationskode - POS-kasseapparatnummer.
    * Autorisationskode – POS-kasseapparatnummer bruges til at informere betalingsprocessor om, hvilken betalingsterminal der sender anmodninger om godkendelse. Denne værdi kaldes ofte "Terminal-id" eller "TID". TID findes normalt på en mærkat på betalingsenheden.  
9. Klik på Gem.


