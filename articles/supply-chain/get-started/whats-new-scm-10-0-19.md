---
title: Forhåndsvisning af Dynamics 365 Supply Chain Management 10.0.19 (2021)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Supply Chain Management 10.0.19.
author: kamaybac
ms.date: 04/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-23
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8bb4a7c8085b40ab3eca72675dbe7a3be412d8c1
ms.sourcegitcommit: 2eb7a9ae544f504155657c5c584cbac66c21dba4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2021
ms.locfileid: "5961675"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10019-july-2021"></a>Forhåndsvisning af Dynamics 365 Supply Chain Management 10.0.19 (2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

I dette emne vises funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management-prøveversionen af version 10.0.19. Denne version har et build-nummer på 10.0.837 og er tilgængelig som følger:

- **Forhåndsvisning af frigivelse:** april 2021
- **Generel tilgængelighed af version (selvopdatering):** juni 2021
- **Generel tilgængelighed af version (automatisk opdatering):** juli 2021

## <a name="features-included-in-this-release"></a>Funktioner, der er inkluderet i denne version

Følgende tabel anfører de funktioner, der er inkluderet i denne version. Kolonnen *Funktion* indeholder links til [frigivelsesplanen](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features), hvor du kan se de officielle frigivelsesdatoer for hver funktion. Kolonnen *Flere oplysninger* indeholder links til relateret dokumentation.

De fleste af disse funktioner skal aktiveres ved hjælp af [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), før du kan bruge dem. Nogle af de viste funktioner findes stadig i prøveversionen, mens andre muligvis allerede er generelt tilgængelige.

| Funktionsområde | Funktion | Flere oplysninger |
|---|---|---|
| Lager og logistik | [Eksportoptimering af kontaktpersondataenheden](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | *Ikke ledig* |
| Lager og logistik | [Trinvise forbedringer af funktioner til kørsel af lagersteder med skaleringsenheder](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[Meddelelser om meddelelsesprocessor](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[Lagerregulering for lagersted](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[Arbejdsbelastninger i forbindelse med lagerstedsstyring for sky- og edge-skaleringsenheder](../cloud-edge/cloud-edge-workload-warehousing.md) |
| Lager og logistik | [Opslagsfunktion for felterne Dokumentintroduktion og Dokumentkonklusion på siden Salgstilbud](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | *Ikke ledig* |
| Lager og logistik | [Kørsel af lagersted med kantskalaenheder på din brugerdefinerede hardware](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [Implementering af kantskalaenheder på brugerdefineret hardware ved hjælp af LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Produktion | [Kørsel af produktion med kantskalaenheder på din brugerdefinerede hardware](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [Implementering af kantskalaenheder på brugerdefineret hardware ved hjælp af LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Planlægning | Forespørgselsbaseret autorisation af ordreforslag | [Autoriser ordreforslag](../master-planning/planning-optimization/planned-order-firming.md) |
| Administration af produktoplysninger | [Forbedringer af siden Variantforslag](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [Oprette foruddefinerede produktvarianter](../pim/tasks/create-predefined-product-variants.md) |

## <a name="new-and-updated-documentation-resources"></a>Nye og opdaterede dokumentationsressourcer

Vi har for nylig tilføjet eller væsentligt opdateret følgende Hjælp-emner. De er ikke nødvendigvis relateret til de nye funktioner, der er tilføjet i denne version, som vist i forrige afsnit, men de kan måske hjælpe dig med at få mere ud af eksisterende funktioner.

| Funktionsområde | Nye eller opdaterede emner |
|---|---|
| Styring af tekniske ændringer | [Ofte stillede spørgsmål om styring af tekniske ændringer](../engineering-change-management/change-management-faq.md) |
| Indkøb og forsyning | [Kategorianmodninger fra kreditorer](../procurement/category-requests-from-vendors.md) |
| Administration af produktoplysninger | [Administrere måleenhed](../pim/tasks/manage-unit-measure.md)<br><br>[Beregninger af produktkonfigurationsmodel](../pim/config-model-calculations.md) |
| Produktionsstyring | [Samlet nummerserie for job-id'er](../production-control/unified-job-ids.md) |
| Transportstyring | [LTL-klasser](../transportation/ltl-class.md)<br><br>[NMFC-koder (Global Trade Identification Number-koder)](../transportation/nmfc-codes.md) |
| Lagerstedsstyring | [Fejlfinde batch- og seriereservationshierarkier for lagersteder](../warehousing/troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md) |
| Lagerstedsstyring, oprettelse og behandling af bølger | [Bølgeoprettelse og -behandling](../warehousing/wave-processing.md)<br><br>[Lagerstedsparametre til behandling af bølger](../warehousing/wave-warehouse-parameters.md)<br><br>[Bølgeskabeloner](../warehousing/wave-templates.md)<br><br>[Bølgefordeling](../warehousing/wave-allocation-method.md)<br><br>[Planlægge oprettelse af arbejde under bølgen](../warehousing/configure-wave-schedule-work-creation.md)<br><br>[Containerisering](../warehousing/wave-containerization.md)<br><br>[Beskeder om udførelse af bølge](../warehousing/wave-execution-notifications.md) |

## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformopdateringer til Finance and Operations-apps

Microsoft Dynamics 365 Supply Chain Management 10.0.19 indeholder platformopdateringer. Du kan få mere vide i [Platformopdateringer til version 10.0.19 af Finance and Operations-apps (juli 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md).

### <a name="bug-fixes"></a>Fejlrettelser

Du kan finde flere oplysninger om de fejlrettelser, der er inkluderet i hver af de opdateringer, som er del af 10.0.19, ved at logge på Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=575415).

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
