---
title: Nyheder eller ændringer i Dynamics 365 Supply Chain Management 10.0.24 (februar 2022)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management 10.0.24.
author: kamaybac
ms.date: 12/03/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: f8864ac22153908492b5e7c30a03617e6dc9d05a
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/15/2022
ms.locfileid: "9166869"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10024-february-2022"></a>Nyheder eller ændringer i Dynamics 365 Supply Chain Management 10.0.24 (februar 2022)

[!include [banner](../includes/banner.md)]

Denne artikel viser funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management version 10.0.24. Denne version har et build-nummer på 10.0.1084 og er tilgængelig som følger:

- **Foreløbig version:** december 2021
- **Generel tilgængelighed af version (selv-opdatering):** januar 2022
- **Generel tilgængelighed af version (automatisk opdatering):** februar 2022

## <a name="features-included-in-this-release"></a>Funktioner, der er inkluderet i denne version

Følgende tabel anfører de funktioner, der er inkluderet i denne version. Vi opdaterer muligvis denne artikel for at medtage funktioner i det build, som er foretaget, efter denne artikel blev udgivet.

| Funktionsområde | Funktion | Flere oplysninger | Aktiveret af   |
|---|---|---|---|
| Distribueret hybridtopologi | [Forbedret udførelse af lagerstedsarbejdsbyrde på skaleringsenheder](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-warehouse-execution-workloads-scale-units) | [Arbejdsbelastninger i forbindelse med lagerstedsstyring for sky- og edge-skaleringsenheder](../cloud-edge/cloud-edge-workload-warehousing.md) | Aktiveret som standard. |
| Distribueret hybridtopologi | [Starte produktionsordre af arbejdsbelastninger i lagerstyring for sky- og grænseskaleringsenheder](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-manufacturing-execution-workloads-scale-units) | [Produktionsarbejdsbyrder for sky- og kantskaleringsenheder](../cloud-edge/cloud-edge-workload-manufacturing.md) | Funktionsstyring (*Starte produktionsordre af arbejdsbelastninger i lagerstyring for sky- og edge-kaleringsenheder*)  |
| Planlægning | [Understøttelse af planlægningsoptimering for restordremargen og afgangsmargen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-reorder-margin-issue-margin) | [Sikkerhedsmargener](../master-planning/planning-optimization/safety-margins.md) | Aktiveret som standard. |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsforbedringer, der er inkluderet i denne version

Følgende tabel indeholder de funktionsforbedringer, der er inkluderet i denne version. Hver af disse udvidelser giver en trinvis forbedring af en eksisterende funktion. Da det kun er forbedringer, er de ikke angivet i [udgivelsesplanen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Men for at sikre, at disse forbedringer ikke er i konflikt med dine eksisterende tilpasninger eller præferencer, er hver af dem som standard deaktiveret (medmindre andet er angivet).

Hvis du vil slå en af disse funktioner til eller fra, skal du gøre det i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funktionsnavn i funktionsstyring | Flere oplysninger |
|---|---|---|
| Produktionsstyring | Kontrol af materialers tilgængelighed efter behov for produktionsordrer | Denne funktion gør det hurtigere at åbne siden **Produktionsordrer, der skal frigives**, som er tilgængelig fra arbejdsområdet **Administration af produktion**. Uden denne funktion kontrollerer systemet automatisk, om materialerne er tilgængelige for alle produktionsordrer på listen, så snart du åbner siden, hvilket kan tage lang tid, hvis du har et stort antal ordrer. Når denne funktion er aktiveret, leverer systemet i stedet en værktøjslinjeknap, som du kan bruge til kun at starte materialekontrollen for udvalgte ordrer, og hvis det er nødvendigt. |
| Produktionsstyring | Registrer materialeforbrug i grænsefladen for produktionsudførelse (ikke-WMS) | Denne funktion giver arbejdere mulighed for at bruge brugergrænsefladen til produktionsudførelse til at registrere materialeforbrug, batchnumre og serienumre. Denne funktion understøtter kun varer, der ikke er aktiveret til brug af lokationsstyringsprocesser (WMS). Understøttelse af WMS-aktiverede varer er planlagt til en fremtidig frigivelse.<p>Visse producenter, især dem inden for procesindustrien, skal udtrykkeligt kunne registrere den mængde materiale, der forbruges for de enkelte batch- eller produktionsordrer. Arbejdere kan for eksempel bruge en vægt til at veje mængden af materiale, der forbruges, når de arbejder. For at sikre fuld sporbarhed af materialer har disse organisationer også brug for at registrere, hvilke batchnumre der blev forbrugt ved fremstillingen af de enkelte produkter. |
| Produktionsstyring | Færdigmelding af arbejdsbelastninger i lagerstyring for sky- og grænseskaleringsenheder | Med denne funktion kan arbejderne bruge mobilappen Warehouse Management til at færdigmelde en produktions- eller batchordre, når appen køres i forhold til en arbejdsbyrde for lagerstyring i en sky- eller grænseskalaenhed. Du kan finde flere oplysninger i [Færdigmelde og lægge på lager på en skaleringsenhed](../cloud-edge/cloud-edge-workload-manufacturing.md#RAF). |
| Lagerstedsstyring | Nye sider med lastplanlægningspanel | Aktiverer to nye sider i lastplanlægningspanelet: **Indgående lastplanlægningspanel** og **Udgående lastplanlægningspanel**. |

## <a name="new-and-updated-documentation-resources"></a>Nye og opdaterede dokumentationsressourcer

Vi har for nylig tilføjet eller væsentligt opdateret følgende Hjælp-artikler. Disse artikler er ikke nødvendigvis knyttet til de nye funktioner, der er tilføjet for denne version, som vist i forrige afsnit. De kan dog hjælpe dig med at få mere ud af eksisterende funktioner.

| Funktionsområde | Nye eller opdaterede artikler |
|---|---|
| Omkostningsstyring | [Lagerværdirapporter](../cost-management/inventory-value-report-storage.md) |
| Omkostningsstyring | [Eksempler og logik til rapport over lagerværdi](../cost-management/inventory-value-report-examples.md) |
| Varedisponering | [Dato- og klokkeslætsparametre, der bruges af planlægningsoptimering](../master-planning/planning-optimization/date-time-used.md) |
| Varedisponering | [Konfigurere behovsprognoser](../master-planning/demand-forecasting-setup.md) |
| Varedisponering | [Bruge sikkerhedslagerkladde for at opdatere minimumdisponering af varer](../master-planning/safety-stock-journal.md) |
| Produktionsstyring | [Tilpasse grænsefladen til produktionsudførelse](../production-control/production-floor-execution-customize.md) |
| Produktionsstyring | [Designe grænsefladen til produktionsudførelse](../production-control/production-floor-execution-styles.md) |
| Salg og marketing | [Planlægge oprydning af data i salgshistorikken](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| Lagerstedsstyring | [Brugerkonti til mobilenhed](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformsopdateringer til programmer til finans og drift

Microsoft Dynamics 365 Supply Chain Management 10.0.24 indeholder platformopdateringer. Du kan få mere vide i [Platformsopdateringer til version 10.0.24 af programmer til finans og drift (februar 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-24.md).

### <a name="bug-fixes"></a>Fejlrettelser

Du kan finde flere oplysninger om de fejlrettelser, der er inkluderet i hver af de opdateringer, som er del af 10.0.24, ved at logge på Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=641306&dbType=3&qc=5b1d5e49c96b8a5cfb5601889a413e6f3773ba6500f9bc47310dcc5c54fff42f).

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

