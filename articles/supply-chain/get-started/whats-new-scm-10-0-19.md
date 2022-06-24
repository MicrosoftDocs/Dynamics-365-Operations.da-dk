---
title: Nyheder eller ændringer i Dynamics 365 Supply Chain Management version 10.0.19 (juni 2021)
description: Denne artikel beskriver funktioner, der enten er nye eller ændrede i Dynamics 365 Supply Chain Management 10.0.19.
author: kamaybac
ms.date: 04/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-23
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea0f2dae2f558f1ee5c0d2b94a4b926263b7de7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893404"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-version-10019-june-2021"></a>Nyheder eller ændringer i Dynamics 365 Supply Chain Management version 10.0.19 (juni 2021)

[!include [banner](../includes/banner.md)]

Denne artikel viser funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management version 10.0.19. Denne version har et build-nummer på 10.0.837 og er tilgængelig som følger:

- **Forhåndsvisning af frigivelse:** april 2021
- **Generel tilgængelighed af version (selvopdatering):** juni 2021
- **Generel tilgængelighed af version (automatisk opdatering):** juni 2021

## <a name="features-included-in-this-release"></a>Funktioner, der er inkluderet i denne version

Følgende tabel anfører de funktioner, der er inkluderet i denne version. Kolonnen *Funktion* indeholder links til [frigivelsesplanen](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features), hvor du kan se de officielle frigivelsesdatoer for hver funktion. Kolonnen *Flere oplysninger* indeholder flere oplysninger og/eller links til relateret dokumentation.

De fleste af disse funktioner skal aktiveres ved hjælp af [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), før du kan bruge dem.

| Funktionsområde | Funktion | Flere oplysninger |
|---|---|---|
| Lager&nbsp;og&nbsp;logistik | [Godkende og gemme bankoplysninger, der er indsendt af kreditorer](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/approve-save-vendor-submitted-bank-details) | [Vedligeholde oplysninger om kreditorbankkonto](../../finance/accounts-payable/maintain-vendor-bank-info.md) |
| Lager og logistik | [Eksportoptimering af kontaktpersondataenheden](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | Når denne funktion er aktiveret, medfører ændringer af data, der refereres til, ikke, at relaterede kontakter medtages i næste trinvise eksport. Når denne funktion er deaktiveret, medfører ændringer af data, der refereres til, at relaterede kontakter medtages i næste trinvise eksport. |
| Lager og logistik | [Trinvise forbedringer af funktioner til kørsel af lagersteder med skaleringsenheder](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[Meddelelser om meddelelsesprocessor](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[Lagerregulering for lagersted](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[Arbejdsbelastninger i forbindelse med lagerstedsstyring for sky- og edge-skaleringsenheder](../cloud-edge/cloud-edge-workload-warehousing.md) |
| Lager og logistik | [Opslagsfunktion for felterne Dokumentintroduktion og Dokumentkonklusion på siden Salgstilbud](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Denne funktion tilføjer opslagsfunktion for felterne **Dokumentintroduktion** og **Dokumentkonklusion** på siden **Salgstilbud**.<br><br>Denne funktion er som standard aktiveret. |
| Lager og logistik | [Kørsel af lagersted med kantskalaenheder på din brugerdefinerede hardware](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [Implementering af kantskalaenheder på brugerdefineret hardware ved hjælp af LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Produktion | [Kørsel af produktion med kantskalaenheder på din brugerdefinerede hardware](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [Implementering af kantskalaenheder på brugerdefineret hardware ved hjælp af LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Planlægning | Forespørgselsbaseret autorisation af ordreforslag | [Autoriser ordreforslag](../master-planning/planning-optimization/planned-order-firming.md) |
| Administration af produktoplysninger | [Forbedringer af siden Variantforslag](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [Oprette foruddefinerede produktvarianter](../pim/tasks/create-predefined-product-variants.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsforbedringer, der er inkluderet i denne version

Følgende tabel indeholder de funktionsforbedringer, der er inkluderet i denne version. Hver af disse giver en trinvis forbedring af en eksisterende funktion. Da det kun er forbedringer, er de ikke angivet i [udgivelsesplanen](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Men for at sikre, at disse forbedringer ikke er i konflikt med dine eksisterende tilpasninger eller præferencer, er hver af dem som standard deaktiveret (medmindre andet er angivet). Hvis du vil bruge en af disse funktioner, skal du udtrykkeligt aktivere dem i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | &nbsp;Funktionsnavn&nbsp;i&nbsp;funktionsstyring | Flere oplysninger |
|---|---|---|
| Salg og marketing | Forbedringer af ydeevnen for oprydning i salgshistorikken | Oprydning i salgshistorikken kan tage lang tid, hvis den køres sjældent i miljøer med en stor mængde salgsopdateringer. For at reducere varigheden og forbedre pålideligheden opdeler denne funktion oprydning i batches, der kører i en begrænset periode. Hvor det er muligt, bruges databasefunktionerne til at minimere låsning og til at undgå at forbinde transaktionstabeller under oprydning. Der er flere oplysninger i [Planlægge oprydning af data i salgshistorikken](../sales-marketing/sales-update-history-cleanup-performance-improvements.md). |
| Salg og marketing | Opdater ønsket modtagelsesdato med bekræftet dato for interne ordrer | Med denne funktion kan du styre, hvad der skal ske med værdier i salgs- og købsdatofelt, når du bruger intern direkte levering. Du kan vælge, om systemet skal opdatere de ønskede datoer eller springe opdateringen over. Hvis du springer opdateringen over, repræsenterer de ønskede datoer det, kunden har anmodet om. Hvis du aktiverer opdatering, repræsenterer de ønskede datoer (ved brug af kontrol af leveringsdato) i første omgang kun det, som kunden har anmodet om. Når kontrollen af leveringsdato er forskellig fra *Ingen*, tilsidesættes det, der oprindeligt blev anmodet om. Du kan angive denne indstilling ved hjælp af den nye indstilling **Opdater anmodet kvitteringsdato med bekræftet dato** i de interne indstillinger for kreditor eller debitor.<br><br>Hvis funktionen er deaktiveret, overskriver systemet den ønskede modtagelsesdato på oprindelige salgsordrer baseret på reglen for kontrol af leveringsdato, men den ønskede afsendelsesdato forbliver, som den er. |
| Lagerstedsstyring | Afrund antal ned til nærmeste salgsenhed ved frigivelse til lagersted | Denne funktion tilføjer en indstilling, der kan begrænse ordreantal ved frigivelse til lagersted. Når indstillingen er aktiveret, rundes ordreantal ned til nærmeste hele salgsenhed, og ordrer, der indeholder antal for mindre end én salgsenhed, afvises til frigivelse. |
| Lagerstedsstyring | Bølgemetoden "Planlæg arbejdsoprettelse" for hele organisationen | Når denne funktion aktiveres, konfigureres bølgemetoden *Planlæg arbejdsoprettelse* til at køre parallelt på tværs af alle juridiske enheder. Flere yderligere indstillinger påvirkes også. Du kan finde de komplette oplysninger i [Planlægge oprettelse af arbejde under bølge](../warehousing/configure-wave-schedule-work-creation.md). |

## <a name="new-and-updated-documentation-resources"></a>Nye og opdaterede dokumentationsressourcer

Vi har for nylig tilføjet eller væsentligt opdateret følgende Hjælp-artikler. De er ikke nødvendigvis relateret til de nye funktioner, der er tilføjet i denne version, som vist i forrige afsnit, men de kan måske hjælpe dig med at få mere ud af eksisterende funktioner.

| Funktionsområde | Nye eller opdaterede artikler |
|---|---|
| Styring af tekniske ændringer | [Ofte stillede spørgsmål om styring af tekniske ændringer](../engineering-change-management/change-management-faq.md) |
| Indkøb og forsyning | [Kategorianmodninger fra kreditorer](../procurement/category-requests-from-vendors.md) |
| Administration af produktoplysninger | [Administrere måleenhed](../pim/tasks/manage-unit-measure.md)<br><br>[Beregninger af produktkonfigurationsmodel](../pim/config-model-calculations.md) |
| Produktionsstyring | [Samlet nummerserie for job-id'er](../production-control/unified-job-ids.md) |
| Transportstyring | [LTL-klasser](../transportation/ltl-class.md)<br><br>[NMFC-koder](../transportation/nmfc-codes.md) |
| Lagerstedsstyring, oprettelse og behandling af bølger | [Bølgeoprettelse og -behandling](../warehousing/wave-processing.md)<br><br>[Lagerstedsparametre til behandling af bølger](../warehousing/wave-warehouse-parameters.md)<br><br>[Bølgeskabeloner](../warehousing/wave-templates.md)<br><br>[Bølgefordeling](../warehousing/wave-allocation-method.md)<br><br>[Planlægge oprettelse af arbejde under bølgen](../warehousing/configure-wave-schedule-work-creation.md)<br><br>[Containerisering](../warehousing/wave-containerization.md)<br><br>[Beskeder om udførelse af bølge](../warehousing/wave-execution-notifications.md) |

## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformsopdateringer til Finans- og driftsapps

Microsoft Dynamics 365 Supply Chain Management 10.0.19 indeholder platformopdateringer. Du kan få mere at vide i [Platformsopdateringer til version 10.0.19 af programmer til finans og drift (juni 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md).

### <a name="bug-fixes"></a>Fejlrettelser

Du kan finde flere oplysninger om de fejlrettelser, der er inkluderet i hver af de opdateringer, som er del af 10.0.19, ved at logge på Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=575415).

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021-frigivelsesplan bølge 1

Vil du gerne vide mere om kommende og de senest frigivne funktioner i en af vores forretningsapps eller platforme?

Se [Dynamics 365: 2021-frigivelsesplan bølge 1](/dynamics365-release-plan/2021wave1/). Vi har samlet alle oplysninger fra start til slut og top til bund i et enkelt dokument, som du kan bruge til planlægning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og udfasede Supply Chain Management-funktioner

Artiklen [Fjernede eller udfasede funktioner Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver de funktioner, der er planlagt eller skal fjernes eller udfases for Supply Chain Management.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Før en funktion fjernes fra produktet, vil du få besked om udfasning i artiklen [Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder, inden de fjernes.

For ændringer, der kun påvirker kompileringstiden, men som er binære, som er kompatible med sandkasse- og produktionsmiljøer, vil tidsrummet for udfasningen være mindre end 12 måneder. Det er typisk funktionelle opdateringer, der skal foretages i compileren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
