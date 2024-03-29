---
title: " Konfigurere regler og parametre for cross-docking og centraliseret indkøb"
description: Denne procedure viser trinnene til oprettelse af opfyldningsregler.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 776defca4a9d2a860901efe9e8890fd11ec8ce7302c53dc1507cc77ff501aded
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753046"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a> Konfigurere regler og parametre for cross-docking og centraliseret indkøb

[!include [banner](../includes/banner.md)]

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]