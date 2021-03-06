---
title: " Oprette og tilknytte registre"
description: Denne fremgangsmåde viser, hvordan du kan oprette en POS-kasse.
author: rubencdelgado
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba978a3d895394760687386197dbb3512c62ef98
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798555"
---
# <a name="create-and-associate-registers"></a> Oprette og tilknytte registre

[!include [banner](../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du kan oprette en POS-kasse. Denne procedure bruger demodatafirmaet USRT.

1. Gå til Retail og Commerce> Konfiguration af kanal > POS-opsætning > Kasseapparater.
2. Klik på Ny.
3. Indtast et id til den nye kasse i feltet Kassenummer.
    * Kasse-id'et indeholder typisk koder, der kan hjælpe med at knytte kassen til den butik, som den tilhører, og placeringen i butikken.  
4. Skriv et beskrivende navn til kassen i feltet Navn.
5. Indtast eller vælg en værdi i feltet Butiksnummer.
6. Indtast eller vælg en værdi i feltet Hardwareprofil.
    * Hardwareprofiler bruges til at angive de eksterne enheder, der skal knyttes til kassen, f.eks. pengeskuffen og bonprinteren.  
7. Indtast eller vælg en værdi i feltet Visuel profil.
    * Visuelle profiler bruges til at angive de billeder, der bruges i POS-baggrunden og på logonside samt temaer for POS.  
8. Skriv en værdi i feltet Autorisationskode - POS-kasseapparatnummer.
    * Autorisationskode – POS-kasseapparatnummer bruges til at informere betalingsprocessor om, hvilken betalingsterminal der sender anmodninger om godkendelse. Denne værdi kaldes ofte "Terminal-id" eller "TID". TID findes normalt på en mærkat på betalingsenheden.  
9. Klik på Gem.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]