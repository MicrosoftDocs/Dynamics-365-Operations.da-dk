---
title: Nyheder eller ændringer i Dynamics 365 Supply Chain Management 10.0.21 (oktober 2021)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Supply Chain Management 10.0.21.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 894686446436a390ec2d019672e3a2b8b0e5f5ef
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579730"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10021-october-2021"></a>Nyheder eller ændringer i Dynamics 365 Supply Chain Management 10.0.21 (oktober 2021)

[!include [banner](../includes/banner.md)]

I dette emne vises funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management version 10.0.21. Denne version har et build-nummer på 10.0.960 og er tilgængelig som følger:

- **Forhåndsversion:** august 2021
- **Generel tilgængelighed af version (selv-opdatering):** september 2021
- **Generel tilgængelighed af version (automatisk opdatering):** oktober 2021

## <a name="features-included-in-this-release"></a>Funktioner, der er inkluderet i denne version

Følgende tabel anfører de funktioner, der er inkluderet i denne version. Kolonnen *Funktion* indeholder links til [frigivelsesplanen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), hvor du kan se de officielle frigivelsesdatoer for hver funktion. Kolonnen *Flere oplysninger* indeholder flere oplysninger og/eller links til relateret dokumentation.

De fleste af disse funktioner skal aktiveres ved hjælp af [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), før du kan bruge dem.

| Funktionsområde | Funktion | Flere oplysninger |
|---|---|---|
| Lager&nbsp;og&nbsp;logistik | [Globalt lagerregnskab-tilføjelsesprogram til Dynamics 365 Supply Chain Management](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [Startside for globalt lagerregnskab](../global-inventory-accounting/global-inventory-accounting-home.md) |
| Lager&nbsp;og&nbsp;logistik | [Bogføre reguleringer af lagerbeholdning ved hjælp af koder, der er tilknyttet modkonti](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [Lageroptællingsårsagskoder](../warehousing/reason-codes-for-counting-journals.md) |
| Lager&nbsp;og&nbsp;logistik | [Eksportpolitik for refererede salgstilbud](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | Vælg, om ændringer af data, der refereres til i tilbud, vil medføre, at disse tilbud (eller linjer) medtages i næste trinvise eksport. Den trinvise eksport køres hurtigere, hvis du ikke medtager tilbud eller linjer.<br><br>Denne funktion tilføjer en indstilling kaldet **Spring salgstilbudsreferencedata over under ændringssporing** til siden **Debitorparametre**. |
| Lager&nbsp;og&nbsp;logistik | Forseglet tilbudsafgivelse <!-- KFM: Add RP link when available --> | [Forseglet bud på tilbudsanmodninger](../procurement/sealed-bidding.md) |
| Lager&nbsp;og&nbsp;logistik | [Scanne stregkoder på lagerstedet ved hjælp af GS1-formatstandarder](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1-stregkoder og QR-koder](../warehousing/gs1-barcodes.md) |
| Lager&nbsp;og&nbsp;logistik | [Foreløbig reservation af tilføjelsesprogrammet Lagersynlighed](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/soft-reservation-inventory-visibility-add-in) | [Reservationer i Lagersynlighed](../inventory/inventory-visibility-reservations.md) |
| Lager&nbsp;og&nbsp;logistik | [Fradrag og fastvægtforbedringer for Rabatstyring](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [Administrere fradrag i fradragspanelet](../rebate-management/deduction-workbench.md )<br><br>[Behandle, gennemse og bogføre rabatter](../rebate-management/process-review-post.md)<br><br>[Rabatstyringshandler](../rebate-management/rebate-management-deals.md) |
| Lager&nbsp;og&nbsp;logistik | [Vejledninger til trin i lagerstedsapp](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Tilpasse trintitler og instruktioner til Warehouse Management-mobilappen](../warehousing/mobile-app-titles-instructions.md) |
| Lager&nbsp;og&nbsp;logistik | [Arbejdspauser og sporingsopdateringer for landingsomkostninger](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [Opdateringssporing for læg på lager](../landed-cost/update-tracking-putaway.md )<br><br>[Behandle varer undervejs](../landed-cost/in-transit-processing.md) |
| Varedisponering | [Negative dage til planlægningsoptimering](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [Forsinkelsestolerance (negative dage)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsforbedringer, der er inkluderet i denne version

Følgende tabel indeholder de funktionsforbedringer, der er inkluderet i denne version. Hver af disse giver en trinvis forbedring af en eksisterende funktion. Da det kun er forbedringer, er de ikke angivet i [udgivelsesplanen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Men for at sikre, at disse forbedringer ikke er i konflikt med dine eksisterende tilpasninger eller præferencer, er hver af dem som standard deaktiveret (medmindre andet er angivet). Hvis du vil bruge en af disse funktioner, skal du udtrykkeligt aktivere dem i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Funktionsområde | &nbsp;Funktionsnavn&nbsp;i&nbsp;funktionsstyring | Flere oplysninger |
|---|---|---|
| Omkostningsstyring | Statusdetaljer om lagerlukning | Denne funktion i forhåndsversionen giver mulighed for en detaljeret visning af status for lagerlukning. |
| Indkøb og forsyning | Undgå overforbrug af generelle budgetreservationer, når der er flere indkøbsrekvisitioner i arbejdsgang | Denne funktion i forhåndsversionen forbedrer fejlkontrollen, når brugere sender og godkender indkøbsrekvisitioner, der overstiger den resterende saldo på en generel budgetreservationslinje. Det hjælper med at forhindre overforbrug af generelle budgetreservationer, når der er flere indkøbsrekvisitioner i arbejdsgangen. |
| Produktionsstyring | Vis fulde serie-, batch- og id-numre i grænsefladen til produktionsudførelse | Denne funktion giver en forbedret ydeevne, når du får vist lister over serie-, batch- og nummerpladenumre i brugergrænsefladen til produktionsudførelse. Visningen ændres fra en kortvisning med et begrænset antal tegn til en listevisning, der giver tilstrækkelig plads til at vise de fulde værdier. Listen giver dig også mulighed for at søge efter bestemte numre. |
| Salg og marketing | Begræns antallet af salgsordrer, der kan vælges til bogføring | Med denne funktion kan du definere det maksimale antal salgsordrer, der kan vælges ved bogføring af bekræftelser, pluklister, følgesedler og fakturaer fra listesiden Salgsordrer. Den aktiveres automatisk. Denne funktion føjer en indstilling, der kaldes **Maks. antal salgsordrer til bogføring**, til siden **Debitorparametre**. Den nye indstilling angives som standard til en værdi på *100*. Funktionen gør det lettere at forbedre ydeevnen for salgsordrelistesiden, når der er valgt et stort antal salgsordrer. Det har ingen indvirkning på antallet af salgsordrer, der kan behandles af en periodisk opgave. |
| Lagerstedsstyring | Afkobl læg på lager-arbejde fra ASN'er | Denne funktion skal bruges til at sende og modtage ASN'er (Advance Shipping Notice), når du kører en arbejdsbyrde for lokationsstyring i en skalaenhed (som en del af en distribueret hybridtopologi). Den tilføjer en ny databasetabel, der er dedikeret til lagring af oplysninger om læg på lager-arbejde. Tidligere blev disse oplysninger gemt i tabeller, som også blev brugt til ASN'er. |
| Lagerstedsstyring | Enheder blandet på slot | Giver systemet mulighed for at indsætte varer på lokationer, der indeholder blandede enheder (som f.eks. både bokse og kasser). Denne funktion giver dig mulighed for på hver enkelt linje i en allokeringsskabelon at vælge, om linjen skal indsætte varer i blandede eller enkeltenhedsplaceringer. |
| Lagerstedsstyring | Brug hurtigere API til containere, der lukker/genåbner på pakkestation | Når denne forhåndsversionsfunktion er aktiveret, oprettes der lagertransaktioner for containere ved hjælp af en ny letvægtsproces, som forbedrer ydeevnen af at lukke eller genåbne containere under manuel behandling af pakkestation. |

## <a name="new-and-updated-documentation-resources"></a>Nye og opdaterede dokumentationsressourcer

Vi har for nylig tilføjet eller væsentligt opdateret følgende Hjælp-emner. De er ikke nødvendigvis relateret til de nye funktioner, der er tilføjet i denne version, som vist i forrige afsnit, men de kan måske hjælpe dig med at få mere ud af eksisterende funktioner.

| Funktionsområde | Nye eller opdaterede emner |
|---|---|
| Varedisponering | [Lagerbudgetter](../master-planning/inventory-forecast.md) |
| Varedisponering | [Parametre, der ikke bruges af planlægningsoptimering](../master-planning/planning-optimization/not-used-parameters.md) |
| Varedisponering | [Genopfyldningsmetoder og ændring af antal](../master-planning/planning-optimization/replenishment-methods-quantity-modification.md) |
| Varedisponering | [Planlægning med ubegrænset kapacitet](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Varedisponering | [Få vist planhistorik og planlægningslogfiler](../master-planning/planning-optimization/plan-history-logs.md) |
| Lagerstedsstyring | [Containerpakningsstrategier](../warehousing/container-packing-strategy-overview.md) |
| Lagerstedsstyring | [Eksempelscenarier for cyklusoptælling](../warehousing/cycle-counting-scenarios.md) |
| Lagerstedsstyring | [Importere indgående ASN'er via V2-dataenheden](../warehousing/import-asn-v2-data-entity.md) |
| Lagerstedsstyring | [Overpluk for salgsordrer og flytteordrer](../warehousing/over-picking-for-sales-and-transfer-orders.md) |
| Lagerstedsstyring | [Planlægge bølgeetiketudskrivning under bølgen](../warehousing/configure-task-based-wave-label-printing.md) |
| Lagerstedsstyring | [Nyheder eller ændringer i Warehouse Management-mobilappen](../warehousing/whats-new-wma.md) |

## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformopdateringer til Finance and Operations-apps

Microsoft Dynamics 365 Supply Chain Management 10.0.21 indeholder platformopdateringer. Du kan få mere vide i [Platformopdateringer til version 10.0.21 af Finance and Operations-apps (oktober 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md).

### <a name="bug-fixes"></a>Fejlrettelser

Du kan finde flere oplysninger om de fejlrettelser, der er inkluderet i hver af de opdateringer, som er del af 10.0.21, ved at logge på Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166&dbType=3&qc=4b9449bf0d947113983bd0697140bf4d8727bfafd5566aa682cb38db343374de).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 og brancheskyer: 2021 frigivelsesplan bølge 2

Vil du gerne vide mere om kommende og de senest frigivne funktioner i en af vores forretningsapps eller platforme?

Undersøg [Dynamics 365 og brancheskyer: 2021 frigivelsesplan bølge 2](/dynamics365-release-plan/2021wave2/). Vi har samlet alle oplysninger fra start til slut og top til bund i et enkelt dokument, som du kan bruge til planlægning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og udfasede Supply Chain Management-funktioner

Emnet [Fjernede eller udfasede funktioner Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver de funktioner, der er planlagt eller skal fjernes eller udfases for Supply Chain Management.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Før en funktion fjernes fra produktet, vil du få besked om udfasning i emnet [Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder, inden de fjernes.

For ændringer, der kun påvirker kompileringstiden, men som er binære, som er kompatible med sandkasse- og produktionsmiljøer, vil tidsrummet for udfasningen være mindre end 12 måneder. Det er typisk funktionelle opdateringer, der skal foretages i compileren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
