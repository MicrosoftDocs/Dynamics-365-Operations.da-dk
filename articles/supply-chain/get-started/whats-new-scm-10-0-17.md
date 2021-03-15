---
title: Forhåndsversion af Dynamics 365 Supply Chain Management 10.0.17 (april 2021)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Supply Chain Management 10.0.17.
author: kamaybac
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-11-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: bfa6e04f8d7ae192d0acd88fb3f1d7e2ce6cc576
ms.sourcegitcommit: b9c6ad79d05feb858f818b37ce5c344f90cc6eb7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/08/2021
ms.locfileid: "5137922"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10017-april-2021"></a>Forhåndsversion af Dynamics 365 Supply Chain Management 10.0.17 (april 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

I dette emne vises funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management-prøveversionen af version 10.0.17. Denne version har et build-nummer på 10.0.761 og er tilgængelig som følger:

- **Forhåndsversion:** Februar 2021
- **Generel tilgængelighed af version (selvopdatering):** Marts 2021
- **Generel tilgængelighed af version (automatisk opdatering):** April 2021

## <a name="features-included-in-this-release"></a>Funktioner, der er inkluderet i denne version

Følgende funktioner er inkluderet i denne version. Nogle af de viste funktioner findes stadig i prøveversionen, mens andre muligvis allerede er generelt tilgængelige. Følg linkene til [frigivelsesplanen](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) for at få vist de officielle frigivelsesdatoer for hver funktion.

- [Anvende regler for gruppering af arbejdsordrer, mens en vedligeholdelsesplan køres](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/apply-rules-grouping-work-orders-while-running-maintenance-plan)<br> - Du kan finde flere oplysninger i [Oprette arbejdsordrer](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md).

<!-- KFM: Blocked for now. Dana will followup.
- [Approve and save vendor-submitted bank details](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/approve-save-vendor-submitted-bank-details) 
-->

- Aktivstyringsfunktioner i grænsefladen til produktionsudførelse<br> - Der er flere oplysninger under [Sådan bruges grænsefladen til kørsel af produktionsudstyr af arbejdere](../production-control/production-floor-execution-use.md).  <!-- KFM: Not yet published on release plan, but is ready. Should be in the next publish. -->

- [Fakturere kunder for vedligeholdelsesarbejde](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/bill-customers-maintenance-work)<br> - Du kan finde flere oplysninger i [Fakturere for vedligeholdelse af aktiver, der ejes af kunder](../asset-management/integration-to-project-management-and-accounting/customer-billing.md).

- [Understøttelse af disponeringstidshorisont for Planlægningsoptimering](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/coverage-time-fence-support-planning-optimization)<br> - Du kan finde flere oplysninger i [Disponeringstidshorisonter](../master-planning/planning-optimization/coverage-time-fence.md).

- [Aktivér administration af ændringer på eksisterende produkter](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enable-change-management-existing-products)

<!-- KFM: Add this when the feature appears in release plan at next update:
- Enterprise-scale inventory performance improvements and archiving  -->

- [Landingsomkostninger](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/landed-cost)

- [Produktionsudførelse med skaleringsenheder i skyen](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-scale-units-cloud)<br> - Du kan finde flere oplysninger under [Arbejdsbelastninger i forbindelse med produktionsudførelse for sky- og edge-skaleringsenheder](../cloud-edge/cloud-edge-workload-manufacturing.md).

- [Materialehåndtering/automatisk lagersted](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/material-handlingwarehouse-automation) <!-- KFM: Update RP link when the new one goes live -->

- [Emballage vs. lagringsdimensioner](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/packing-vs.-storage-dimensions)<br> - Du kan finde flere oplysninger under [Angive forskellige dimensioner for pakning og lagring](../warehousing/packing-vs-storage-dimensions.md)

- Tilsidesætte standardreservationsprincippet for materialer i produktion<br> - Du kan finde flere oplysninger under [Tilsidesætte standardreservationsprincippet for materialer i produktion](../production-control/override-default-reservation-principle.md). <!-- KFM: Not yet published on release plan, but is ready. Should be in the next publish. -->

- [Planlægge vedligeholdelse baseret på akkumulerede værdier for en aktivtæller](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/plan-maintenance-based-accumulated-asset-counter-values)<br> - Du kan finde flere oplysninger i [Vedligeholdelsesplaner](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md).

- [Understøttelse af indkøbsrekvisition for Planlægningsoptimering](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/purchase-requisition-support-planning-optimization)<br> - Du kan finde flere oplysninger under [Indkøbsrekvisitioner](../master-planning/planning-optimization/purchase-requisitions.md).

- [Gemte visninger af lager og logistik](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-inventory-logistics)<br> - Du kan finde flere oplysninger i [Gemte standardvisninger for Supply Chain Management](saved-views-scm.md).

- [Gemte visninger af ordreforslag](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-planned-orders)<br> - Du kan finde flere oplysninger i [Gemte standardvisninger for Supply Chain Management](saved-views-scm.md).

- [Gemte visninger for produktionsstyring](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-production-control)<br> - Du kan finde flere oplysninger i [Gemte standardvisninger for Supply Chain Management](saved-views-scm.md).

- [Planlægge oprettelse af lagerstedsarbejde](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-warehouse-work-creation)<br> - Du kan finde flere oplysninger i [Planlægge oprettelse af arbejde under bølge](../warehousing/configure-wave-schedule-work-creation.md).

- [Angive økonomiske standarddimensioner for værdireguleringsbilag for lagerstandardomkostninger](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/set-default-financial-dimensions-inventory-standard-cost-revaluation-vouchers)<br> - Du kan finde flere oplysninger i [Administrere opdateringer af standardomkostninger](../cost-management/manage-standard-cost-updates.md).

- [Forsendelse af småpakker (SPS)](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/small-package-shipping-sps)<br> - Du kan finde flere oplysninger i [Forsendelse af småpakker](../warehousing/small-parcel-shipping.md). <!-- KFM: Update RP link when the new one goes live -->

- [Lagerudførelse med skaleringsenheder i skyen](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-scale-units-cloud)<br> - Du kan finde flere oplysninger i [Arbejdsbelastninger i forbindelse med lokationsstyring for sky- og edge-skaleringsenheder](../cloud-edge/cloud-edge-workload-warehousing.md) og [Lagerstedsordrer til sky- og kantskalaenheder](../cloud-edge/cloud-edge-warehouse-order.md).

- [Mobilappen Lokationsstyring](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application)<br> - Du kan finde flere oplysninger i [Installere og tilslutte appen Lokationsstyring](../warehousing/install-configure-warehouse-management-app.md).

De fleste af disse funktioner skal aktiveres ved hjælp af [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), før du kan bruge dem.

## <a name="new-and-updated-documentation-resources"></a>Nye og opdaterede dokumentationsressourcer

Vi har for nylig tilføjet eller væsentligt opdateret følgende Hjælp-emner. De er ikke nødvendigvis relateret til de nye funktioner, der er tilføjet i denne version, som vist i forrige afsnit, men de kan måske hjælpe dig med at få mere ud af eksisterende funktioner.

- [Konfigurere produktfiltre til lagerstedstransaktioner](../warehousing/filters-and-filter-codes.md)

- [Designe grænsefladen til produktionsudførelse](../production-control/production-floor-execution-tabs.md)

- [Intern planlægning](../master-planning/planning-optimization/Intercompany-planning.md)

- [Lagermarkering med planlægningsoptimering](../master-planning/planning-optimization/marking.md)

- [Varedisponering med behovsprognoser](../master-planning/planning-optimization/demand-forecast.md)

- [Delvis cyklusoptælling for lokation](../warehousing/partial-location-cycle-counting.md)

- [Pluklinjegruppering](../warehousing/pick-line-grouping.md)

- [Produktionsplanlægning](../master-planning/planning-optimization/production-planning.md) <!--KFM: Remember to add YouTube link to this topic -->

- [Indkøbsrekvisitioner i varedisponering](../master-planning/planning-optimization/purchase-requisitions.md)

- [Konfigurere arbejdsområdet til aktivstyring på mobilenhed](../asset-management/set-up-asset-management-mobile.md)

- [Fejlfinde i omkostningsstyring](../cost-management/troubleshoot-costmanagement.md)

- [Fejlfinde lagerhandlinger](../inventory/troubleshoot-inventory-operations.md)

- [Lagerstedsallokering](../warehousing/warehouse-slotting.md)

## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformopdateringer til Finance and Operations-apps

Microsoft Dynamics 365 Supply Chain Management 10.0.17 indeholder platformopdateringer. Du kan få mere vide i [Platformopdateringer til version 10.0.17 af Finance and Operations-apps (april 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md).

### <a name="bug-fixes"></a>Fejlrettelser

Du kan finde flere oplysninger om de fejlrettelser, der er inkluderet i hver af de opdateringer, som er del af 10.0.17, ved at logge på Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=551039&dbType=3&qc=91219e7c3fc585acb17b810c915c3cbea499403538520c40e54de43a53aea6a8).

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021-frigivelsesplan bølge 1

Vil du gerne vide mere om kommende og de senest frigivne funktioner i en af vores forretningsapps eller platforme?

Se [Dynamics 365: 2021-frigivelsesplan bølge 1](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/). Vi har samlet alle oplysninger fra start til slut og top til bund i et enkelt dokument, som du kan bruge til planlægning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og udfasede Supply Chain Management-funktioner

Emnet [Fjernede eller udfasede funktioner Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver de funktioner, der er planlagt eller skal fjernes eller udfases for Supply Chain Management.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Før en funktion fjernes fra produktet, vil du få besked om udfasning i emnet [Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder, inden de fjernes.

For ændringer, der kun påvirker kompileringstiden, men som er binære, som er kompatible med sandkasse- og produktionsmiljøer, vil tidsrummet for udfasningen være mindre end 12 måneder. Det er typisk funktionelle opdateringer, der skal foretages i compileren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]