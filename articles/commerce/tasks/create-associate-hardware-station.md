---
title: Oprette og tilknytte en hardwarestation
description: Denne procedure gennemgår oprettelse af en ny hardwarestation.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0c02246a20ef28c0f4f28b73dfe5ff56f38a68b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247038"
---
# <a name="create-and-associate-a-hardware-station"></a>Oprette og tilknytte en hardwarestation

[!include [banner](../includes/banner.md)]

Denne procedure gennemgår oprettelse af en ny hardwarestation. En ny hardwareprofil oprettes og bruges til at tilføje nye hardwarestationer til en foruddefineret butik (kanal). Denne procedure bruger USRT-firmaets demodata.

1. Gå til Oprindelsesdata til handel > Kanaler >.. > .. > .. > Hardwarestations profiler.
2. Klik på Ny.
3. Skriv "TestHWProfile" i feltet Hardwarestation-id.
4. Skriv en værdi i feltet Navn.
5. Angiv et tal i feltet Portnummer.
6. Klik på rullelisten i feltet Hardwareprofil for at åbne opslaget.
7. Find og vælg den ønskede post på listen.
8. Klik op linket i den valgte række på listen.
9. Klik på rullelisten i feltet Pakkens navn for at åbne opslaget.
10. Klik op linket i den valgte række på listen.
    * Dette er den standardpakke, der følger med et nyt miljø. Versionsnummeret kan variere.  
11. Klik på Gem.
12. Luk siden.
13. Gå til Retail og Commerce > Kanaler > Alle butikker.
14. Markér række 17 på listen.
    * Hvis du bruger USRT-demodatafirmaet, er dette Houston-butikken.  
15. Klik op linket i den valgte række på listen.
16. Slå udvidelsen af sektionen Hardwarestationer til/fra.
17. Klik på Tilføj.
18. Markér den valgte række på listen.
19. Klik på rullelisten i feltet Profil-id for at åbne opslaget.
20. Find og vælg den ønskede post på listen.
    * Det skal være den nye hardwarestationsprofil, du oprettede i de forrige trin.  
21. Klik op linket i den valgte række på listen.
22. Indtast en værdi i feltet Værtsnavn.
23. Indtast en værdi i feltet Terminal-id for elektronisk pengeoverførsel.
24. Klik på Gem.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]