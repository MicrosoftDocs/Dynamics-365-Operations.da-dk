---
title: Nyheder eller ændringer i Dynamics 365 Supply Chain Management 10.0.20 (august 2021)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Supply Chain Management 10.0.20.
author: kamaybac
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1aada0d3ebe80e1efb92815c6d429ed5638dabdbac165aa09be1ca281c51b255
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773507"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10020-august-2021"></a>Nyheder eller ændringer i Dynamics 365 Supply Chain Management 10.0.20 (august 2021)

[!include [banner](../includes/banner.md)]

I dette emne vises funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management version 10.0.20. Denne version har et build-nummer på 10.0.886 og er tilgængelig som følger:

- **Forhåndsversion:** maj 2021
- **Generel tilgængelighed af version (selvopdatering):** juli 2021
- **Generel tilgængelighed af version (automatisk opdatering):** August 2021

## <a name="features-included-in-this-release"></a>Funktioner, der er inkluderet i denne version

Følgende tabel anfører de funktioner, der er inkluderet i denne version. Kolonnen *Funktion* indeholder links til [frigivelsesplanen](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features), hvor du kan se de officielle frigivelsesdatoer for hver funktion. Kolonnen *Flere oplysninger* indeholder flere oplysninger og/eller links til relateret dokumentation.

De fleste af disse funktioner skal aktiveres ved hjælp af [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), før du kan bruge dem.

| Funktionsområde | Funktion | Flere oplysninger |
|---|---|---|
| Lager&nbsp;og&nbsp;logistik | [Forbedringer af ydeevne for salgsordredetaljer](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | Denne funktion gør brugergrænsefladen mere responsiv, når der åbnes salgsordrer, især ordrer, der indeholder mange linjer. |
| Produktion | [Aktivere procesautomatiseringsflow for at oprette kvalitetsordrer](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/invoke-process-automation-flows-create-quality-orders) | [Aktivere procesautomatiseringsflow for at oprette kvalitetsordrer](../production-control/process-automation-quality-orders.md ) |
| Produktion | [Forbedret brugergrænseflade til produktionsudførelse for fremstilling](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-manufacturing) | [Konfigurere grænsefladen til produktionsudførelse](../production-control/production-floor-execution-configure.md) |
| Administration af produktoplysninger | [Administrere ændringer i formler og deres stoffer](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/engineering-change-management-support-process-manufacturing) | [Administrere ændringer i formler og deres stoffer](../engineering-change-management/manage-formula-changes.md) |
| Administration af produktoplysninger | [Kontroller af produktparathed](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/product-readiness-checks) | [Produktparathed](../engineering-change-management/product-readiness.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsforbedringer, der er inkluderet i denne version

Følgende tabel indeholder de funktionsforbedringer, der er inkluderet i denne version. Hver af disse giver en trinvis forbedring af en eksisterende funktion. Da det kun er forbedringer, er de ikke angivet i [udgivelsesplanen](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Men for at sikre, at disse forbedringer ikke er i konflikt med dine eksisterende tilpasninger eller præferencer, er hver af dem som standard deaktiveret (medmindre andet er angivet). Hvis du vil bruge en af disse funktioner, skal du udtrykkeligt aktivere dem i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Funktionsområde | &nbsp;Funktionsnavn&nbsp;i&nbsp;funktionsstyring | Flere oplysninger |
|---|---|---|
| Varedisponering | Parallel godkendelse til justeret behovsprognose | Denne funktion muliggør parallel godkendelse af justeret efterspørgselsprognose fra siden **Justeret efterspørgselsprognose**. Formålet med denne funktion er at øge ydeevnen, når et stort antal budgetter godkendes. Under godkendelse kan brugeren angive **Antal tråde** i dialogboksen til godkendelse. |
| Varedisponering | (Forhåndsversion) Godkendelse og konsolidering, der kan køre i batch, for planlagte bulk- og pakkebatchordrer | Med denne funktion kan du bruge batchjob til at bekræfte og konsolidere planlagte bulk- og pakkeordrer. |
| Produktionsstyring | Kopiér generiske ruter | Denne funktion forbedrer kopieringsrutefunktionen, så brugerne kan kopiere ruter, der ikke er varespecifikke. Det giver systemet mulighed for at opdatere alle relevante oplysninger (f.eks. lokation, rutegruppe, ressourcebehov og forskellige tider), når kopieringsrutefunktionen er blevet brugt til at overskrive en rute, der endnu ikke er tildelt en vare. |
| Produktionsstyring | Opdater relaterede ressourcekrav, når en ruteoperation ændres | Denne funktion giver systemet mulighed for at opdatere de relaterede ressourcekrav, når en bruger ændrer driften af et eksisterende rutetrin. |
| Administration af produktoplysninger | Behandling af styklisterapport på forhånd for at forhindre timeout | Denne funktion medfører, at styklisterapporten behandles på forhånd. Derved undgår du timeoutproblemer, når der er en stor databelastning for rapporten. |
| Indkøb og forsyning | Aktivér nulstilling af indkøbsrelaterede arbejdsgange | Med denne prøveversionsfunktion kan du nulstille følgende arbejdsgange til kladdestatus: Indkøbsordre, Leverandørændring og Indkøbsrekvisitioner. |
| Transportstyring | Aktivér oprettelse af en kreditorfakturakladde, når en fragtregning kasseres | Når denne funktion er aktiveret, oprettes der kun en tilsvarende kreditorfakturakladde med henblik på afstemning, når du bruger indstillingen for betaling af kreditor. Ellers oprettes fakturakladden altid. |
| Lagerstedsstyring | Valider skabeloner, der er valgt til genopfyldningsjob | Denne funktion hjælper med at sikre, at brugere vælger gyldige genopfyldningsskabeloner, når de opretter et genopfyldningsjob. Den forhindrer brugerne i at oprette et genopfyldningsjob uden en skabelon og i at vælge skabeloner af typen *Bølgeefterspørgsel*, som ikke kan oprette genopfyldningsarbejde, og som kan tage lang tid at behandle. |

## <a name="new-and-updated-documentation-resources"></a>Nye og opdaterede dokumentationsressourcer

Vi har for nylig tilføjet eller væsentligt opdateret følgende Hjælp-emner. De er ikke nødvendigvis relateret til de nye funktioner, der er tilføjet i denne version, som vist i forrige afsnit, men de kan måske hjælpe dig med at få mere ud af eksisterende funktioner.

| Funktionsområde | Nye eller opdaterede emner |
|---|---|
| Styring af tekniske ændringer | [Produktlivscyklustilstande og transaktioner](../engineering-change-management/product-lifecycle-state-transactions.md) |
| Lagerstyring | [Tilføjelsesprogram for indsigt i lagerbeholdning](../inventory/inventory-visibility.md)<br><br>[Oversigt over styring af kvalitet og uoverensstemmelse](../inventory/quality-management-processes.md) (plus alle tilknyttede emner om kvalitetsstyring) |
| Indkøb og forsyning | [Vedligeholde kreditorcertificering](../../finance/public-sector/manage-vendor-certification.md) |
| Produktionsstyring | [Designe grænsefladen til produktionsudførelse](../production-control/production-floor-execution-styles.md) |
| Lagerstedsstyring | [Tildele trinikoner og titler til mobilappen Warehouse Management](../warehousing/step-icons-titles.md)<br><br>[Udskudt behandling af manuelle lagerbevægelser](../warehousing/deferred-processing-manual-inventory-movement.md) |

## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformopdateringer til Finance and Operations-apps

Microsoft Dynamics 365 Supply Chain Management 10.0.20 indeholder platformopdateringer. Du kan få mere vide i [Platformopdateringer til version 10.0.20 af Finance and Operations-apps (juli 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20.md).

### <a name="bug-fixes"></a>Fejlrettelser

Du kan finde flere oplysninger om de fejlrettelser, der er inkluderet i hver af de opdateringer, som er del af 10.0.20, ved at logge på Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=586707&dbType=3&qc=d0dad8eee2af234e8c288e2a7df14c579004518673d014be511f900cfed008f8). 

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021-frigivelsesplan bølge 1

Vil du gerne vide mere om kommende og de senest frigivne funktioner i en af vores forretningsapps eller platforme?

Se [Dynamics 365: 2021-frigivelsesplan bølge 1](/dynamics365-release-plan/2021wave1/). Vi har samlet alle oplysninger fra start til slut og top til bund i et enkelt dokument, som du kan bruge til planlægning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og udfasede Supply Chain Management-funktioner

Emnet [Fjernede eller udfasede funktioner Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver de funktioner, der er planlagt eller skal fjernes eller udfases for Supply Chain Management.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Før en funktion fjernes fra produktet, vil du få besked om udfasning i emnet [Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder, inden de fjernes.

For ændringer, der kun påvirker kompileringstiden, men som er binære, som er kompatible med sandkasse- og produktionsmiljøer, vil tidsrummet for udfasningen være mindre end 12 måneder. Det er typisk funktionelle opdateringer, der skal foretages i compileren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
