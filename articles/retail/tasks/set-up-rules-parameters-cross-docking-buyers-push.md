--- 
title: " Konfigurere regler og parametre for cross-docking og centraliseret indkøb"
description: Denne procedure viser trinnene til oprettelse af opfyldningsregler.
author: josaw1
manager: AnnBe
ms.date: 03/02/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1ff41a18be066b6f32c5172bda38c389e7f34128
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a> Konfigurere regler og parametre for cross-docking og centraliseret indkøb

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne procedure viser trinnene til oprettelse af opfyldningsregler. Opfyldningsregler kan bruges til at styre, hvordan produkter fordeles til butikkerne, når du bruger cross-docking og bestilling efter ordre. Opfyldningsregler kan konfigureres til butikker eller butiksgrupper. Den vægt, der er defineret for hver linje i en regel, bestemmer, hvordan mængderne af produkter vil blive fordelt mellem butikkerne, når der bruges opfyldningsregler som fordelingsmetode i cross-docking eller bestilling efter ordre. Denne procedure bruger demofirmaet USRT.

1. Gå til Opfyldningsregler.
2. Klik på Ny.
3. Skriv en værdi i feltet Opfyldningsregel.
4. Skriv en værdi i feltet Beskrivelse.
5. Klik på Gem.
6. Klik på Tilføj.
7. Markér den valgte række på listen.
    * Du kan vælge Opfyldningshierarki eller Kanal som typen. Værdien kontrollerer, om valget i Navn vil være et hierarki af kanaler eller en bestemt kanal.  I dette eksempel skal lade den være angivet som Opfyldningshierarki.  
8. Vælg en værdi i feltet Navn.
    * Standardvægtværdien udfyldes fra den vægt, der er defineret for lagerstedet.  Denne vægt kan bruges til opfyldningsreglen, eller du kan angive en ny vægt i feltet Vægt.  
9. Angiv et tal i feltet Vægt.
10. Klik på Tilføj.
11. Markér den valgte række på listen.
12. Vælg "Kanal" i feltet Type.
13. Indtast eller vælg en værdi i feltet Navn.
14. Angiv et tal i feltet Vægt.
15. Klik på Gem.


