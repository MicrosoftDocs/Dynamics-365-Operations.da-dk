---
title: "Tilbagefør produktionsordrens status"
description: "I dette emne beskrives, hvordan du tilbagefører status for produktionsordrer."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmStatusDecrease
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4761e44b6bbc93ebf4a395948f42c2a73013ecb9
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="reverse-the-production-order-status"></a>Tilbagefør produktionsordrens status

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du tilbagefører status for produktionsordrer. 

Hvis du tilbagefører status for en produktionsordre, gendannes ordren og alle de operationer, der er tilknyttet ruterne, til et tidligere trin i produktionens levetid. En produktionsordrer har f.eks. statussen **Planlagt**, og du kan ændre status tilbage til **Oprettet**. Systemet skal i så fald først ændre status til **Estimeret**, som er den status, der er umiddelbart før **Planlagt**. Derefter kan status ændres til den status, du ønsker, **Oprettet**. **Bemærk!** Hvis ordren har nået statussen **Færdigmelding**, kan du stadig tilbageføre den til en tidligere status. Du skal imidlertid køre forkalkulation og grovplanlægning eller finplanlægning eller begge former for planlægning igen for at opdatere oplysningerne i ordren. Dette trin er påkrævet, da alle reservationer af resterende vareforbrug og forbrug af operationsressourcer også skal nulstilles. I resten af denne artikel forklares det, hvad der sker, når du tilbagefører status for en produktionsordre på følgende måder:

-   Fra **Estimeret** til **Oprettet**
-   Fra **Planlagt** til **Estimeret**
-   Fra **Frigivet** til **Planlagt**
-   Fra **Startet** til **Frigivet**

## <a name="from-estimated-to-created"></a>Fra Estimeret til Oprettet
Når du tilbagefører status for en produktionsordre fra **Estimeret** til **Oprettet**, fjernes det vareforbrug, der blev beregnet for varerne i styklisten. Lagertransaktioner på produktionslinjen slettes, og feltet **Reststatus** på styklistelinjerne i produktionsordren nulstilles til **Afsluttet**. Når indstillingerne **Afledte indkøb** og **Afledt produktion** er valgt, slettes eventuelle underliggende indkøbsordrer eller produktionsordrer. Hvis du har foretaget estimat af omkostninger for produktionsordren, eller hvis du manuelt reserverede varer, så de kunne bruges i produktionen, fjernes disse transaktioner.

## <a name="from-scheduled-to-estimated"></a>Fra Planlagt til Estimeret
Når du fører status for en produktionsordre fra **Planlagt** tilbage til **Estimeret**, fjernes de planlagte start- og slutdatoer. Kapacitetsreservationer, der er foretaget under planlægning, fjernes, og de job, der blev oprettet under finplanlægning, slettes. Alle oplysninger, der er registreret om grovplanlægning og finplanlægning på siden **Detaljer om produktionsordrer**, nulstilles.

## <a name="from-released-to-scheduled"></a>Fra Frigivet til Planlagt
Når du tilbagefører status for en produktionsordre fra **Frigivet** til **Planlagt**, er det eneste, der ændres, værdien i statusfeltet.

## <a name="from-started-to-released"></a>Fra Startet til Frigivet
Når du tilbagefører status for en produktionsordre fra **Startet** til **Frigivet**, tilbageføres alle varer, der er færdigmeldt. Hvis der er plukket materiale, eller hvis der er foretaget indgående eller udgående leveringer til produktion, tilbageføres disse indstillinger. Feltet **Reststatus** på styklistelinjerne i produktionsordren ændres fra **Afsluttet** til **Materialeforbrug**. Hvis der er registreret tid, eller hvis mængder er færdigmeldt for operationerne i produktionsruten, føres disse indstillinger tilbage. Feltet **Reststatus** på ændres fra **Afsluttet** til **Ruteforbrug** på produktionsruten. Indstillingerne for alle varer, der er bogført som igangværende eller igangværende arbejder, tilbageføres. På siden **Detaljer om produktionsordrer** nulstilles felter, der indeholder et antal, som er startet eller færdigmeldt. Datoerne for disse transaktioner nulstilles også.




