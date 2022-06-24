---
title: Nyheder eller ændringer i Dynamics 365 Supply Chain Management (10.0.22. november 2021)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management 10.0.22.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 53f1670454ef505e61e96b16990d913473b46bf4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849497"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10022-november-2021"></a>Nyheder eller ændringer i Dynamics 365 Supply Chain Management (10.0.22. november 2021)

[!include [banner](../includes/banner.md)]

Denne artikel viser funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management version 10.0.22. Denne version har et build-nummer på 10.0.995 og er tilgængelig som følger:

- **Udgivelse af forhåndsversion:** September 2021
- **Generel tilgængelighed af version (selv-opdatering):** oktober 2021
- **Generel tilgængelighed af version (auto-opdatering):** november 2021

## <a name="features-included-in-this-release"></a>Funktioner, der er inkluderet i denne version

Følgende tabel anfører de funktioner, der er inkluderet i denne version. Kolonnen *Funktion* indeholder links til [frigivelsesplanen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), hvor du kan se de officielle frigivelsesdatoer for hver funktion. Kolonnen *Flere oplysninger* indeholder flere oplysninger og/eller links til relateret dokumentation. Se kolonnen *Aktiveret efter*, hvis du vil have oplysninger om, hvordan du aktiverer funktionen. Du kan finde flere oplysninger om brug af administration af funktioner under [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Vi opdaterer muligvis denne artikel for at medtage funktioner i det build, som er foretaget, efter denne artikel blev udgivet.

| Funktionsområde | Funktion | Flere oplysninger | Aktiveret af   |
|---|---|---|---|
| Planlægning | [Understøttelse af planlægningsoptimering for egenskabsbaseret ressourcefordeling](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capability-based-resource-allocation) | [Planlægning med ressourcevalg baseret på egenskab](../master-planning/planning-optimization/capability-based-scheduling.md) | Funktionsstyring (*Uendelig kapacitetsplanlægning til Planlægningsoptimering*) |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsforbedringer, der er inkluderet i denne version

Følgende tabel indeholder de funktionsforbedringer, der er inkluderet i denne version. Hver af disse udvidelser giver en trinvis forbedring af en eksisterende funktion. Da det kun er forbedringer, er de ikke angivet i [udgivelsesplanen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Men for at sikre, at disse forbedringer ikke er i konflikt med dine eksisterende tilpasninger eller præferencer, er hver af dem som standard deaktiveret (medmindre andet er angivet). Hvis du vil bruge en af disse funktioner, skal du udtrykkeligt aktivere dem i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funktionsnavn i funktionsstyring | Flere oplysninger |
|---|---|---|
| Distribueret hybridtopologi | *(Der kræves ingen funktionsstyring.)* | <p>I denne version udvides udgående planlægningsegenskaber for lokationsstyring for sky- og kantskalaenheder.</p><p>Du kan finde flere oplysninger under [Arbejdsbelastninger i forbindelse med lokationsstyring for sky- og edge-skaleringsenheder](../cloud-edge/cloud-edge-workload-warehousing.md).</p> |
| Styring af tekniske ændringer | Variantgenerering af tekniske produkter | <p>Med denne funktion kan du generere flere varianter for et teknikerprodukt ud fra dets farve-, størrelses-, typografi- eller konfigurationsdimensioner.</p><p>Du kan finde flere oplysninger i [Generere varianter for teknikprodukter](../engineering-change-management/engineering-variants.md).</p> |
| Lager- og lokationsstyring | Integration af lagersynlighed med reservationsmodkonto | <p>Denne funktion kan kun aktiveres, når funktionen til integration med *lagersynlighed* er aktiveret. Det giver funktionalitet til at modpostere reservationer, der er foretaget med lagersynlighed.</p><p>Du kan finde flere oplysninger i [Reservationer i Lagersynlighed](../inventory/inventory-visibility-reservations.md).</p> |

## <a name="new-and-updated-documentation-resources"></a>Nye og opdaterede dokumentationsressourcer

Vi har for nylig tilføjet eller væsentligt opdateret følgende Hjælp-artikler. Disse artikler er ikke nødvendigvis knyttet til de nye funktioner, der er tilføjet for denne version, som vist i forrige afsnit. De kan dog hjælpe dig med at få mere ud af eksisterende funktioner.

| Funktionsområde | Nye eller opdaterede artikler |
|---|---|
| Styring af tekniske ændringer | [Oversigt over ændringsstyring for teknikere](../engineering-change-management/product-engineering-overview.md) viser nu alle relaterede valgfrie funktioner, der findes i funktionsstyring |
| Varedisponering | [Konfigurere behovsprognoser](../master-planning/demand-forecasting-setup.md) |
| Varedisponering | [Oplysninger om nettobehov og udligning med planlægningsoptimering](../master-planning/planning-optimization/net-requirements.md) |
| Lagerstedsstyring | [Udgivelse til lagersted](../warehousing/release-to-warehouse-process.md) giver en detaljeret oversigt over den fulde frigivelse til lagerstedsproces |

## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformsopdateringer til Finans- og driftsapps

Microsoft Dynamics 365 Supply Chain Management 10.0.22 indeholder platformopdateringer. Du kan få mere vide i [Platformsopdateringer til version 10.0.22 af Finans- og driftsapps (november 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22.md).

### <a name="bug-fixes"></a>Fejlrettelser

Du kan finde flere oplysninger om de fejlrettelser, der er inkluderet i hver af de opdateringer, som er del af 10.0.22, ved at logge på Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=615299).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 og brancheskyer: 2021 frigivelsesplan bølge 2

Vil du gerne vide mere om kommende og de senest frigivne funktioner i en af vores forretningsapps eller platforme?

Undersøg [Dynamics 365 og brancheskyer: 2021 frigivelsesplan bølge 2](/dynamics365-release-plan/2021wave2/). Vi har samlet alle oplysninger fra start til slut og top til bund i et enkelt dokument, som du kan bruge til planlægning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og udfasede Supply Chain Management-funktioner

Artiklen [Fjernede eller udfasede funktioner Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver de funktioner, der er planlagt eller skal fjernes eller udfases for Supply Chain Management.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Før en funktion fjernes fra produktet, vil du få besked om udfasning i artiklen [Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder, inden de fjernes.

For ændringer, der kun påvirker kompileringstiden, men som er binære, som er kompatible med sandkasse- og produktionsmiljøer, vil tidsrummet for udfasningen være mindre end 12 måneder. Det er typisk funktionelle opdateringer, der skal foretages i compileren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
