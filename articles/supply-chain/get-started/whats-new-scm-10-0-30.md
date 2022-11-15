---
title: Nyheder eller ændringer i Dynamics 365 Supply Chain Management (10.0.30. november 2022)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management 10.0.30.
author: kamaybac
ms.date: 11/07/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-09-08
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 20674ebd9d49b077371998f53d2b22c74f888fc6
ms.sourcegitcommit: 613be2f35e600ae1a1fa7ea2ae30e78984ca398a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748458"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10030-november-2022"></a>Nyheder eller ændringer i Dynamics 365 Supply Chain Management (10.0.30. november 2022)

[!include [banner](../includes/banner.md)]

Denne artikel viser funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management version 10.0.30. Denne version har et build-nummer på 10.0.1362 og er tilgængelig i følgende plan:

- **Udgivelse af forhåndsversion:** September 2022
- **Generel tilgængelighed af version (selv-opdatering):** oktober 2022
- **Generel tilgængelighed af version (auto-opdatering):** november 2022

## <a name="features-included-in-this-release"></a>Funktioner, der er inkluderet i denne version

Følgende tabel anfører de funktioner, der er inkluderet i denne version. Vi opdaterer muligvis denne artikel for at medtage funktioner i det build, som er foretaget, efter denne artikel blev udgivet.

| Funktionsområde | Funktion | Flere oplysninger | Aktiveret af   |
|---|---|---|---|
| Lager og logistik | [Spore foreløbigt reserverede antal i tildelinger](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/track-soft-reserved-quantities-within-allocations) | [Lagerfordeling for lagersynlighed](../inventory/inventory-visibility-allocation.md) |  Aktiveret af [servicekonfiguration](../inventory/inventory-visibility-configuration.md) |
| Fremstillingsvirksomhed | [Overvåge udstyr med Sensordataintelligens](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/monitor-equipment-sensor-data-intelligence) | [Sensordataintelligens-startside](../sensor-data-intelligence/sdi-home-page.md) | Funktionsstyring:<br>*(Forhåndsversion) Sensordataintelligens* |
| Warehouse management | [Omveje i flere niveauer til Warehouse Management-mobilappen](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/multi-level-detours-warehouse-management-mobile-app) | [Konfigurere omveje til trin i menupunkter på mobilenheder](../warehousing/warehouse-app-detours.md) | Funktionsstyring:<br>*Omveje i flere niveauer til Warehouse Management-mobilappen* |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsforbedringer, der er inkluderet i denne version

Følgende tabel indeholder de funktionsforbedringer, der er inkluderet i denne version. Hver af disse udvidelser giver en trinvis forbedring af en eksisterende funktion. Da det kun er forbedringer, er de ikke angivet i [udgivelsesplanen](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Men for at sikre, at disse forbedringer ikke er i konflikt med dine eksisterende tilpasninger eller præferencer, er hver af dem som standard deaktiveret (medmindre andet er angivet).

Hvis du vil slå en af disse funktioner til eller fra, skal du gøre det i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funktionsnavn i funktionsstyring | Flere oplysninger |
|---|---|---|
| Produktionsstyring | Disponible produktionsordreoplysninger til udgivelsesside | Tilføjer en kolonne for den disponible lagerbeholdning for linjeelementet i linjesektionen på siden **produktionsordrer til udgivelsessiden**. |
| Transportstyring | Tildel forsendelser til relaterede rutesegmenter | Denne funktion gør det muligt for systemet at dele forsendelsesfragtomkostninger mere nøjagtigt, herunder belastninger med flere forsendelser, der er leveret til forskellige segmentdestinationer på en enkelt rute. Den tildeler hver forsendelse til det mest velegnede rutesegment på baggrund af destinationsadresserne for forsendelsen og segmentet. Funktionen beregner derefter de enkelte forsendelsers fragtomkostninger som en del af belastningens samlede fragtomkostninger baseret på forsendelsens relative vægt, volumen, antal og rejselængde. Denne funktion gælder kun for forsendelser, der administreres ved hjælp af modulet Transportstyring (TMS). |

## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformsopdateringer til Finans- og driftsapps

Microsoft Dynamics 365 Supply Chain Management 10.0.30 indeholder platformopdateringer. Du kan få mere vide i [Platformsopdateringer til version 10.0.30 af Finans- og driftsapps (november 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md).

### <a name="bug-fixes"></a>Fejlrettelser

Du kan finde flere oplysninger om de fejlrettelser, der er inkluderet i hver af de opdateringer, som er del af version 10.0.30, ved at logge på Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 og brancheskyer: 2022 frigivelsesplan bølge 1

Vil du gerne vide mere om kommende og de senest frigivne funktioner i en af vores forretningsapps eller platforme?

Undersøg [Dynamics 365 og brancheskyer: 2022 frigivelsesplan bølge 2](/dynamics365-release-plan/2022wave2/). Vi har samlet alle oplysninger fra start til slut og top til bund i et enkelt dokument, som du kan bruge til planlægning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og udfasede Supply Chain Management-funktioner

Artiklen [Fjernede eller udfasede funktioner Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver de funktioner, der er planlagt eller skal fjernes eller udfases for Supply Chain Management.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Før en funktion fjernes fra produktet, vil du få besked om udfasning i artiklen [Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder, inden de fjernes.

For ændringer, der kun påvirker kompileringstiden, men som er binære, som er kompatible med sandkasse- og produktionsmiljøer, vil tidsrummet for udfasningen være mindre end 12 måneder. Det er typisk funktionelle opdateringer, der skal foretages i compileren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
