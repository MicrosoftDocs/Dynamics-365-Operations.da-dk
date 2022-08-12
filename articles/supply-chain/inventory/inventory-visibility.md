---
title: Oversigt over tilføjelsesprogram for Inventory Visibility
description: Denne artikel forklarer, hvad lagersynlighed er og beskriver funktionerne.
author: yufeihuang
ms.date: 03/18/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 274f9b368a6074725d1938de5f2172d2810a5985
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066634"
---
# <a name="inventory-visibility-add-in-overview"></a>Oversigt over tilføjelsesprogram for lagersynlighed

[!include [banner](../includes/banner.md)]

Tilføjelsesprogrammet Lagersynlighed (kaldes også *lagersynlighedstjeneste*) er en uafhængig og meget skalerbar mikrotjeneste, der muliggør ændringsposteringer af disponibel lagerbeholdning i realtid og synlighedssporing på tværs af alle dine datakilder og kanaler. Det indeholder en platform, der giver dig mulighed for at administrere den globale lagerbeholdning ved hjælp af funktioner, der omfatter (men ikke er begrænset til) følgende liste:

- Spor den seneste lagerstatus centralt (f.eks. beholdning, bestilt, købt, i transit, returneret og sat i karantæne) på tværs af alle datakilder, lagersteder og lokationer ved at knytte datakilder for Supply Chain Management eller tredjepartslogistik (f.eks. ordrestyringssystemer, tredjeparts systemer til Enterprise Resource Planning \[ERP-systemer\], \[POS\]-systemer og lokationsstyringssystemer) til tjenesten Lagersynlighed.
- Forespørg på tilgængelighed af og mangel på disponible lagerbeholdninger, og få omgående svar ved at kontakte tjenesten Lagersynlighed direkte.
- Undgå oversalg, især når din efterspørgsel kommer fra forskellige kanaler, ved at foretage foreløbige reservationer i realtid i tjenesten Lagersynlighed.
- Administrer bedre lovede ordrer og kundeforventninger ved at angive nøjagtige aktuelle eller næste tilgængelige datoer, så funktionen DTT (omnikanal for disponibel til tilsagn) kan beregne forventede ordreopfyldelsesdatoer.

## <a name="extensibility"></a>Udvidelsesmuligheder

Lagersynlighedstjenesten er stærkt udvidelig, da datainput og -output ikke er begrænset til Microsoft-programmer. Eksterne systemer kan få adgang til tjenesten via RESTful Application Programming Interface (API'er). Udover at bruge de indbyggede tilknytninger, som er tilgængelige for datakilden og dimensionerne i Supply Chain Management, kan du integrere Lagersynlighed med flere tredjepartssystemer ved at konfigurere yderligere datakilder, målinger af lagerstatus (kaldet *fysiske målinger* i lagersynlighedstjenesten) og lagerdimensioner via konfigurationsappen. På denne måde kan du fleksibelt forespørge på og ændre dine datakilder og foruddefinerede lagerdimensioner.

Da lagersynlighedstjenesten er baseret på Microsoft Dataverse, kan dataene derudover bruges til at opbygge og integrere med Power Apps. Du kan også anvende Power BI til at oprette tilpassede dashboards, der opfylder dine forretningsbehov.

## <a name="scalability"></a>Skalerbarhed

Lagersynlighedstjenesten kan skaleres op eller ned, afhængigt af datavolumen. Erfaringen med skalerbarhed er oftest problemfri og udføres af Microsoft-platformteamet baseret på automatisk registrering og vurdering af volumen af dine transaktionsdata.

## <a name="feature-highlights"></a>Fremhævning af funktioner

### <a name="get-a-global-view-of-real-time-inventory"></a>Få en global visning af lageret i realtid

Med Lagersynlighed kan du sikre dig adgang til de mest opdaterede lagerantal til enhver tid på tværs af alle kanaler, lokaliteter og lagersteder. Det er den største fordel at bruge den til at understøtte dit daglige driftsmæssige firma, når du skal have lagerposter. Fysisk disponibel lagerbeholdning, solgte antal og købte antal er alle tilgængelige som standard. Du kan også konfigurere andre fysiske lagermålinger (f.eks. returnerede, sat i karantæne og bogførte data) efter behov for at få disse oplysninger i realtid. Med lagersynlighed kan du behandle millioner af lagerændringsposter effektivt. Disse data kan aggregeres og afspejles i de seneste lagerantal i tjenesten med det samme, hvert sekund eller minut, afhængigt af det interval, data bogføres i. Du kan finde flere oplysninger i [Offentlige API'er til lagersynlighed](inventory-visibility-api.md).

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>Foreløbig reservation for at undgå oversalg på tværs af alle ordrekanaler

Med en *foreløbig reservation* kan du tildele eller markere bestemte antal for at opfylde en ordre eller efterspørgsel. En foreløbig reservation påvirker ikke det fysiske lager, men den fratrækker det *disponible antal for reservation* af lager og angiver et opdateret antal til fremtidig ordreopfyldelse. Denne funktion vil være nyttig, hvis salgsanmodninger eller ordrer kommer ind i din virksomhed fra en eller flere kanaler eller datakilder, der ligger uden for ERP-systemet (Enterprise Resource Planning).

Hvis du ikke bruger foreløbige reservationer i lagersynlighedstjenesten, skal du vente, indtil ordren synkroniseres til og behandles af ERP-systemet, så du får en fysisk opdatering af lagerantal. Denne proces har typisk stor ventetid. Foreløbige reservationer træder dog i kraft, hver gang der genereres en salgsanmodning eller -ordre i salgskanalerne. De hjælper derfor med at forhindre oversalgssituationer ved at sikre, at dine omnikanalordrer ikke påvirker hinanden, når de senere kommer til ERP-systemet. Foreløbige reservationer sikrer også, at du kan opfylde alle de ordrer, du har lovet. De hjælper dig derfor med at imødekomme kundernes forventninger og bevare kundeloyalitet. Du kan finde flere oplysninger i [Reservationer i Lagersynlighed](inventory-visibility-reservations.md).

### <a name="immediate-response-of-atp-dates-confirmation"></a>Strakssvar på bekræftelse af DTT-datoer

Det er vigtigt, at du får overblik over den nærmeste fremtidige forventede lagerbeholdning (herunder udbud, efterspørgsel og forventede lagerbeholdninger), da det hjælper dit firma med at nå følgende mål:

- Minimere lagerniveauer for at reducere lagerstyringsomkostninger.
- Forenkle intern behandling af ordrer, så sælgere kan beregne forsendelses- og leveringsdatoer baseret på tilgængeligheden af de bestilte produkter.
- Sikre gennemsigtighed af, hvornår kunder kan forvente, at en vare, der ikke er på lager, bliver tilgængelig, ved at angive den næste tilgængelige dato.

DTT-funktionen er let at optage i den daglige ordreopfyldelsesproces. Ligesom andre tilbud om lagersynlighed er DTT-funktionen vigtigst af alt *global og i realtid*. Du kan derfor konfigurere flere DTT-beregningsformler for at have forespørgsler om fuld lagertilgængelighed, der dækker alle din virksomheds kanaler og datakilder. Du kan finde flere oplysninger i [Ændringsplaner for disponibelt antal og disponibel til tilsagn i lagersynlighed](inventory-visibility-available-to-promise.md).

### <a name="compatibility-with-warehouse-management-processes-wms-items"></a>Kompatibilitet med varer i lokationsstyringsprocesser (WMS)

Microsoft sigter efter at levere standardintegration med lokationsstyringsprocesser (WMS), så WMS-kunder også kan få glæde af tjenesten Lagersynlighed. Fra og med frigivelsesbølge 1 i 2022 (offentlig forhåndsversion i marts) understøtter lagertjenesten WMS-vareforespørgsler og ATP. Funktionen til foreløbig reservation og fordeling understøttes til WMS-kunder i næste bølge. Du kan finde flere oplysninger i [Understøttelse af lagersynlighed for WMS-varer](inventory-visibility-whs-support.md).

## <a name="licensing"></a>Licensering

Lagersynlighedstjenesten er tilgængelig i følgende versioner:

- **Tilføjelsesprogrammet Lagersynlighed til Microsoft Dynamics 365 Supply Chain Management** – For firmaer med en gyldig licens til Supply Chain Management er Lagersynlighed tilgængelig uden ekstra licensomkostninger. Du kan begynde at prøve det af i dag. Oplysninger om installation finder du under [Installere og konfigurere lagersynlighed](inventory-visibility-setup.md).
- **Lagersynlighedstjeneste som en komponent i IOM** – Denne version er til enten Intelligent Order Management-kunder eller -firmaer (IOM), der ikke bruger Supply Chain Management som deres ERP-system. Licensen er inkluderet i IOM-bundtet. Yderligere oplysninger finder du i [Oversigt over Intelligent Order Management](/dynamics365/intelligent-order-management/overview).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
