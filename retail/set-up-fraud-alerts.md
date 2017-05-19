---
title: Konfigurere bedragerimeddelelser
description: "Dette emne forklarer, hvordan du opretter regler for at advare kundeservicemedarbejdere om potentielt falske oplysninger ved behandling af ordrer. Du kan definere bestemte koder, der skal bruges for automatisk eller manuelt at sætte mistænkelige ordrer på hold."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: ddcf68b9d9d35d63cb092225d468dd4a6a3d4446
ms.contentlocale: da-dk
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-fraud-alerts"></a>Konfigurere bedragerimeddelelser

[!include[banner](includes/banner.md)]


Dette emne forklarer, hvordan du opretter regler for at advare kundeservicemedarbejdere om potentielt falske oplysninger ved behandling af ordrer. Du kan definere bestemte koder, der skal bruges for automatisk eller manuelt at sætte mistænkelige ordrer på hold. 

Før du konfigurerer og bruger regler til kontrol af bedrageri, skal du aktivere kontrol af bedrageri og definere de grundlæggende værdier for kontrol af bedrageri i parametrene for callcentret. Der findes to typer bedrageriregler:

-   **Statiske regler** bruger en bestemt værdi, f.eks. et telefonnummer, der er blevet blacklistet.
-   **Dynamisk regler** kan oprettes ud fra variabler og betingelser.

Før du kan oprette en dynamisk regel, skal du oprette de variabler og betingelser, der definerer, hvem reglen gælder for, og hvor reglen skal anvendes. Det kan f.eks. være, at du vil oprette en regel, der kræver, at en salgsordre, som debitor 1202 afgiver, og som har en værdi på 1.000,0 eller mere, skal sættes på hold, indtil debitorbetalingen kan kontrolleres. I dette tilfælde er variablerne debitor 1202 og en ordretotal på 1.000,00. Betingelsen angiver, at hvis debitor 1202 afgiver en ordre, og det samlede beløb på ordren er lig med eller mere end 1.000,00, skal salgsordren sættes på hold, indtil debitorbetalingen kan kontrolleres.




