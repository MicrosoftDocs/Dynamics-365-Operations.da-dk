---
title: Tip til Inventory Visibility
description: Denne artikel indeholder et par tip, som du bør overveje, når du konfigurerer og bruger tilføjelsesprogrammet Lagersynlighed.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 9f571d353f99c91776424bc2fa3405f73b2bae0a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885951"
---
# <a name="inventory-visibility-tips"></a>Tip til lagersynlighed

[!include [banner](../includes/banner.md)]

Her er et par tip, som du bør overveje, når du konfigurerer og bruger tilføjelsesprogrammet Lagersynlighed:

- I øjeblikket understøtter tilføjelsesprogrammet Lagersynlighed kun Microsoft Dataverse-miljøer, der er oprettet af Microsoft Dynamics Lifecycle Services (LCS). Hvis dit Dataverse-miljø er oprettet på en anden måde (f.eks. ved hjælp af Power Apps Administration), og hvis det er knyttet til dit Dynamics 365 Supply Chain Management-miljø, skal du først bede produktteamet for Lagersynlighed om at rette tilknytningsfejlen. Du kan kontakte teamet på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). Teamet giver dig besked, når dit miljø er klar til at installere Lagersynlighed.
- Hvis du har mere end ét LCS-miljø, skal du oprette et andet Azure Active Directory-program (Azure AD) til hvert miljø. Hvis du bruger samme program-id og lejer-id til at installere tilføjelsesprogrammet Lagersynlighed i forskellige miljøer, vil der forekomme et tokenproblem for ældre miljøer. Det er kun den sidste forekomst af tilføjelsesprogrammet Lagersynlighed, der er installeret, som er gyldigt.
- Lagersynlighed understøttes i øjeblikket ikke i skybaserede miljøer. Den understøttes kun i miljøer på niveau 2+.
- API'en (Application Programming Interface) understøtter i øjeblikket forespørgsler på op til 100 individuelle varer efter `ProductID`-værdi. Der kan også angives flere `SiteID`- og `LocationID`-værdier i hver forespørgsel. Maksimumgrænsen er defineret som `NumOf(SiteID) * NumOf(LocationID) <= 100`.
- Masse-API'en kan maksimalt returnere 512 poster for hver anmodning.
- Datakilden `fno` er reserveret til Supply Chain Management. Hvis tilføjelsesprogrammet Lagersynlighed er integreret med et Supply Chain Management-miljø, anbefales det, at du ikke sletter konfigurationer, der er relateret til `fno` i [datakilden](inventory-visibility-configuration.md#data-source-configuration).
- Lagersynlighed kan ikke ændre data for datakilden `fno`. Dataflowet er envejs, hvilket betyder, at alle ændringer af antal til datakilden `fno` skal komme fra dit Supply Chain Management-miljø. Du kan derfor ikke bruge API'en til at sende anmodninger om ændring af disponibelt antal eller reservation for datakilden `fno`.
- Hvis du føjer en eller flere nye målinger til Supply Chain Management-miljøet, skal du også føje dem til Lagersynlighed. Alle ændringer af antal for nye målinger skal dog komme fra dit Supply Chain Management-miljø.
- I øjeblikket består [partitionskonfigurationen](inventory-visibility-configuration.md#partition-configuration) af to basisdimensioner (`SiteId` og `LocationId`), der angiver, hvordan dataene fordeles. Operationer under samme partition kan give en højere ydeevne og lavere omkostninger. Løsningen inkluderer som standard denne partitionskonfiguration. Du *behøver derfor ikke definere den selv*. Lad være med at tilpasse standardkonfigurationen af partitioner. Hvis du sletter eller ændrer den, opstår der højst sandsynligt en uventet fejl.
- Basisdimensioner, der er defineret i partitionskonfigurationen, bør ikke defineres i [konfigurationen af produktindekshierarki](inventory-visibility-configuration.md#index-configuration).
- Din [konfiguration af produktindekshierarki](inventory-visibility-configuration.md#index-configuration)skal have mindst ét indekshierarki (f.eks. med basisdimensionen `Empty`) – ellers mislykkes forespørgslerne med fejlen "Der er ikke angivet et indekshierarki".

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
