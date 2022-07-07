---
title: Nyheder eller ændringer i Dynamics 365 Supply Chain Management 10.0.27. (juli 2022)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management 10.0.27.
author: kamaybac
ms.date: 04/22/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: a50fcbe313901beab610400d8c59dd375f1af93e
ms.sourcegitcommit: d770f0e6a012675a3027641704be804beb99754b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/16/2022
ms.locfileid: "9022615"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10027-july-2022"></a>Nyheder eller ændringer i Dynamics 365 Supply Chain Management 10.0.27. (juli 2022)

[!include [banner](../includes/banner.md)]

Denne artikel viser funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management version 10.0.27. Denne version har et build-nummer på 10.0.1227 og er tilgængelig i følgende plan:

- **Forhåndsvisning af frigivelse:** april 2022
- **Generel tilgængelighed af version (selvopdatering):** juni 2022
- **Generel tilgængelighed af version (automatisk opdatering):** juli 2022

## <a name="features-included-in-this-release"></a>Funktioner, der er inkluderet i denne version

Følgende tabel anfører de funktioner, der er inkluderet i denne version. Vi opdaterer muligvis denne artikel for at medtage funktioner i det build, som er foretaget, efter denne artikel blev udgivet.

| Funktionsområde | Funktion | Flere oplysninger | Aktiveret af   |
|---|---|---|---|
| Lager og logistik | [Lagertildeling for tilføjelsesprogrammet Lagersynlighed](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-allocation-inventory-visibility-add-in) | [Lagerfordeling for lagersynlighed](../inventory/inventory-visibility-allocation.md) | Aktiveret som standard |
| Fremstillingsvirksomhed | Visningen "Min dag" til grænsefladen til produktionsudførelse | [Hvordan arbejdere bruger brugergrænsefladen til produktionsudførelse](../production-control/production-floor-execution-use.md) og [Vis feriesaldi i brugergrænsefladen til produktionsudførelse](../production-control/production-floor-execution-payroll-stats.md) | Funktionsstyring:<br>*Visningen "Min dag" til grænsefladen til produktionsudførelse* |
| Planlægning | [Understøttelse af planlægningsoptimering til underleverandørarbejde](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-subcontracting) | [Administrere underleverandørarbejde i produktionen](../production-control/manage-subcontract-work-production.md) | Aktiveret som standard |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsforbedringer, der er inkluderet i denne version

Følgende tabel indeholder de funktionsforbedringer, der er inkluderet i denne version. Hver af disse udvidelser giver en trinvis forbedring af en eksisterende funktion. Da det kun er forbedringer, er de ikke angivet i [udgivelsesplanen](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Men for at sikre, at disse forbedringer ikke er i konflikt med dine eksisterende tilpasninger eller præferencer, er hver af dem som standard deaktiveret (medmindre andet er angivet).

Hvis du vil slå en af disse funktioner til eller fra, skal du gøre det i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funktionsnavn i funktionsstyring | Flere oplysninger |
|---|---|---|
| Varedisponering | Tag højde for lagergennemløbstid, når der oprettes en planlagt overførselsordre | Når der oprettes en planlagt flytteordre, får denne funktion systemet til at tage højde for den lagergennemløbstid, der er angivet i varens standardordreindstillinger ved beregning af modtagelsesdatoen for den planlagte flytteordre til opsætning af leveringsdatokontrol som *Ingen* eller *Salgstype*. Når der er angivet overførselstid, bruges værdien for beregningen af modtagelsesdatoen, og der ses bort fra transportdage. |
| Indkøb og forsyning | Standardoplysninger om mæglerkontraktmoms på kreditorfakturalinjer | Denne funktion introducerer en logik for opsætning af standardværdier for felterne **Moms** og **Varemoms** på kreditorfakturalinjer for mæglerkontrakter. Denne logik anvendes kun, når gebyrtypen på mæglerkontraktlinjen er finans/finans. Varemomsgruppe har standardværdien enten fra indkøbskategorien til mæglervirksomhed (hvis den er konfigureret) eller fra gebyrtypen. Momsgruppen hentes som standard fra kreditorkontoen. |
| Indkøb og forsyning | Begræns antallet af indkøbsordrelinjer pr. batchopgave | Denne funktion giver dig mulighed for at optimere systemets ydeevne, når bekræftelser og produktkvitteringer bogføres. Den føjer en ny indstilling med navnet **Linjer pr. opgave** til fanen **Levering** på siden **Indkøbs- og forsyningsparametre**. Denne nye indstilling giver dig mulighed for at begrænse antallet af indkøbsordrelinjer, som hver batchopgave behandler. Det kan derfor hjælpe dig med at forhindre, at store batchopgaver bliver langsommere i systemet. |
| Administration af produktoplysninger | Udfyld produktattributværdier | Denne funktion tilføjer en periodisk opgave med navnet *Udfyld produktattributværdier*. Denne nye periodiske opgave opretter manglende poster med produktattributværdi for attributter, der er knyttet til produkter via en produktkategori. |
| Produktionsstyring | Yderligere konfiguration af grænsefladen til produktionsudførelse | <p>Denne funktion føjer indstillinger til følgende funktioner på siden **Konfigurer produktionsudførelse**:</p><ul><li>**Automatisk åbning af dialogboksen for start, når søgningen fuldføres** – Når denne indstilling er aktiveret, åbnes dialogboksen **Start job** automatisk, når arbejdere bruger søgelinjen til at finde jobbet.</li><li>**Automatisk åbning af dialogboksen for start, når søgningen fuldføres** – Når denne indstilling er aktiveret, åbnes dialogboksen **Rapporter status** automatisk, når arbejdere bruger søgelinjen til at finde jobbet.</li><li>**Angiv resterende mængde som standard i dialogboksen Rapportér status** – Når denne indstilling er aktiveret, viser dialogboksen **Rapporter status** det restantal, der skal rapporteres for et produktionsjob.</li></ul><p>Yderligere oplysninger finder du i [Konfigurere grænsefladen til kørsel af produktionsudstyr](../production-control/production-floor-execution-configure.md).</p> |
| Produktionsstyring | Grænsefladen til produktionsteam i produktionsudførelse | <p>Når flere arbejdere er tildelt samme produktionsjob, kan de nu udpege én arbejder som pilot. De øvrige arbejdere bliver derefter automatisk assistenter for den pågældende pilot. Det er kun piloten, der skal registrere jobstatus for det resulterende team, hvorimod tidsposter gælder for alle teammedlemmer. Denne funktion understøtter også et scenarie, der kaldes *hjælperessource*. I dette scenario kan en arbejder registrere sig som assistent for en anden arbejder, der derefter bliver pilot for den nyudnævnte gruppe.</p><p>Flere oplysninger under [Sådan bruges grænsefladen til kørsel af produktionsudstyr af arbejdere](../production-control/production-floor-execution-use.md).</p> |
| Produktionsstyring | Rapport over planlægningselementer i grænsefladen til produktionsudførelse | Denne funktion forenkler rapporteringsprocessen for batchordrer ved planlægning af varer i brugergrænsefladen til produktionsudførelse. Når der oprettes en batchordre for et produkt med produktionstypen *Planlægningsvare*, kan færdigmelding kun ske på ko-produkterne og biprodukterne for den pågældende batchordre. Batchordrer til planlægning af varer bruges typisk til at understøtte forskellige processer, hvor et råmaterialeprodukt opdeles i flere specifikke produkter. Når en arbejder færdigmelder en batchordre for en planlægningsvare, vises nu kun ko-produkterne og biprodukterne i dialogboksen med **Rapporter status**. Tidligere har den også vist planlægningselementet, og denne adfærd kunne være forvirrende for arbejdere. |

## <a name="new-and-updated-documentation-resources"></a>Nye og opdaterede dokumentationsressourcer

Vi har for nylig tilføjet eller væsentligt opdateret følgende Hjælp-artikler. Disse artikler er ikke nødvendigvis knyttet til de nye funktioner, der er tilføjet for denne version, som vist i forrige afsnit. De kan dog hjælpe dig med at få mere ud af eksisterende funktioner.

| Funktionsområde | Nye eller opdaterede artikler |
|---|---|
| Omkostningsstyring | [Gennemsnitskostdato med fysisk værdi og afmærkning](../cost-management/weighted-average-date.md) |
| Distribueret hybridtopologi | [Afprøve skalaenheder i en distribueret hybridtopologi](../cloud-edge/cloud-edge-try-out.md) |
| Dobbeltskrivning | [Synkronisere med Supply Chain Management-prissætningsprogrammet efter behov](../../fin-ops-core/dev-itpro/data-entities/dual-write/pricing-engine.md) |
| Warehouse management | [Frigiv til lagersted](../warehousing/release-to-warehouse-process.md) |

## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformsopdateringer til Finans- og driftsapps

Microsoft Dynamics 365 Supply Chain Management 10.0.27 indeholder platformopdateringer. Du kan få mere at vide i [Platformsopdateringer til version 10.0.27 af programmer til finans og drift (juni 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-27.md).

### <a name="bug-fixes"></a>Fejlrettelser

Du kan finde flere oplysninger om de fejlrettelser, der er inkluderet i hver af de opdateringer, som er del af 10.0.27, ved at logge på Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 og brancheskyer: 2022 frigivelsesplan bølge 1

Vil du gerne vide mere om kommende og de senest frigivne funktioner i en af vores forretningsapps eller platforme?

Undersøg [Dynamics 365 og brancheskyer: 2022 frigivelsesplan bølge 1](/dynamics365-release-plan/2022wave1/). Vi har samlet alle oplysninger fra start til slut og top til bund i et enkelt dokument, som du kan bruge til planlægning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og udfasede Supply Chain Management-funktioner

Artiklen [Fjernede eller udfasede funktioner Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver de funktioner, der er planlagt eller skal fjernes eller udfases for Supply Chain Management.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Før en funktion fjernes fra produktet, vil du få besked om udfasning i artiklen [Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder, inden de fjernes.

For ændringer, der kun påvirker kompileringstiden, men som er binære, som er kompatible med sandkasse- og produktionsmiljøer, vil tidsrummet for udfasningen være mindre end 12 måneder. Det er typisk funktionelle opdateringer, der skal foretages i compileren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
