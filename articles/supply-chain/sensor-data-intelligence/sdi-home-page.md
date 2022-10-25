---
title: Sensordataintelligens-startside
description: Denne artikel indeholder en oversigt over Sensordataintelligens. Organisationer kan bruge denne funktion til at køre forretningsprocesser i Microsoft Dynamics 365 Supply Chain Management ud fra IoT-signaler (Internet of Things) fra maskiner og udstyr i produktionen.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: ba030364056db8b0524de22aacbc6528ef77813b
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689851"
---
# <a name="sensor-data-intelligence-home-page"></a>Sensordataintelligens-startside

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Sensordataintelligens for Microsoft Dynamics 365 Supply Chain Management giver organisationer denne funktion til at køre forretningsprocesser i Supply Chain Management ud fra IoT-signaler (Internet of Things) fra maskiner og udstyr i produktionen. Det er en opdateret, omdøbt version af *IoT-intelligensfunktionen*, der tidligere var tilgængelig for Supply Chain Management.

Du kan udføre følgende opgaver med Sensordataintelligens:

- Samle oplysninger fra maskiner og udstyr for at opdatere tællerværdier for vedligeholdelse af aktiver i Supply Chain Management og øge den forudsigelige vedligeholdelse.
- Du kan oprette løsningen ved at bruge en simpel startguide i stedet for at installere og konfigurere komponenter manuelt i Microsoft Dynamics Lifecycle Services (LCS).
- Implementer komponenter i dit eget abonnement, så du har større fleksibilitet til at administrere Azure-komponenter.
- Konfigurer, skalaer og udvid løsningen som forretningslogik, der kører på Azure-komponenter. Disse komponenter administreres nu på dit eget abonnement. Du kan derfor tilpasse dem efter behov for at opfylde dine unikke forretningsbehov.

## <a name="business-scenarios"></a>Forretningsscenarier

Ved hjælp af Sensordataintelligens kan der bruges flere funktionstyper, som hver især repræsenteres af et bestemt *scenario* i systemet. Hvert scenario indeholder et specialiseret sæt konfigurationsindstillinger i systemet som beskrevet i nedenstående tabel.

| Scenarie | Beskrivende tekst |
|---|---|
| [Nedetid for aktiv](sdi-scenario-asset-downtime.md) | Du kan præcist spore maskinaktivernes effektivitet ved at bruge data til at spore maskinens nedetid. |
| [Aktivvedligeholdelse](sdi-scenario-asset-maintenance.md) | Minimere vedligeholdelsesomkostningerne og forlænge levetiden for aktiver ved at forbedre vedligeholdelsesplanerne baseret på aflæsninger af vigtige kontrolpunkter for maskinaktiver. |
| [Maskinstatus](sdi-scenario-equipment-downtime.md) | Sikre operationens effektivitet ved at bruge læserne til at give planlægninger besked om maskinfejl og give mulighed for at afhjælpe eventuelle forsinkelser. |
| [Produktkvalitet](sdi-scenario-product-quality.md) | Sikre kvaliteten af produktbatchnumre ved at sammenligne læserne af de faktiske egenskaber for hvert produktbatch, f.eks. fugtighed, temperatur eller brugerdefinerede kvalitetsværdier. Systemet giver brugerne besked, når der opstår afvigelser. |
| [Produktionsforsinkelser](sdi-scenario-production-delays.md) | Brug læserne til at sammenligne faktisk procestid med planlagt procestid, og giv tilsynsførende besked, når produktionsforløbet ikke er til planlagt. Supervisors kan derefter efter behov for at sikre maksimal operationseffektivitet. |

## <a name="architecture"></a>Arkitektur

Følgende arkitekturdiagram indeholder en oversigt over løsningen og dens komponenter.

![Diagram over arkitekturen for dataoplysninger.](media/sdi-architecture.png "Diagram over arkitekturen for dataoplysninger")
