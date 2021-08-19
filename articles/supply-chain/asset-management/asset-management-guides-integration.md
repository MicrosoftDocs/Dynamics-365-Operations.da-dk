---
title: Integrere Dynamics 365 Supply Chain Management (Styring af aktiver) med Dynamics 365 Guides
description: I dette emne forklares, hvordan du kan integrere modulet Styring af aktiver i Microsoft Dynamics 365 Supply Chain Management med Dynamics 365 Guides for at udnytte Mixed Reality-hjælpelinjer i din service fra dag til dag og dine vedligeholdelsesarbejdsgange.
author: kamaybac
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 94d98aa011d0db3991c14596f5d6bdecc0fb6c831915ae124f623fa57277fcfe
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721529"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a>Integrere Dynamics 365 Supply Chain Management (Styring af aktiver) med Dynamics 365 Guides

Du kan integrere modulet **Styring af aktiver** i Microsoft Dynamics 365 Supply Chain Management med Dynamics 365 Guides for at udnytte Mixed Reality-guider i din service fra dag til og dine vedligeholdelsesarbejdsgange. Hvis der er knyttet en hjælpelinje til en arbejdsordre i Styring af aktiver, kan en arbejder, der åbner en arbejdsordres vedligeholdelsestjekliste i Supply Chain Management 365 (Dynamics 365)-mobilappen, se, at en hjælpelinje er tilgængelig. Arbejderen kan derefter finde og åbne hjælpelinjen i Dynamics 365 Guides HoloLens-appen.

## <a name="prerequisites"></a>Forudsætninger

Før du kan føje hjælpelinjer til arbejdsordrer i Styring af aktiver, skal du fuldføre disse forudsætninger:

- [Konfigurere Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) version 10.0.9 eller nyere.
- [Slå dobbeltskrivning til for Supply Chain Management-apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).
- [Slå flight til](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for **MRGuidesFeature**-funktionen. (I forbindelse med produktionsmiljøer skal du først sende en supportanmodning for at få din lejer føjet til flighting-gruppen).
- [Slå følgende konfigurationsnøgler til](/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) på siden **Licenskonfiguration**:

    - Styring af aktiver \> Styring af aktiver – Mixed Reality
    - Mixed Reality \> Hjælpelinje til Mixed Reality

- [Konfigurere Dynamics 365 Guides](/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 200.0.0.96 eller nyere.

## <a name="use-dynamics-365-guides-with-asset-management"></a>Bruge Dynamics 365 Guides med Styring af aktiver

Hvis du vil tilknytte en hjælpelinje, skal du bruge en vedligeholdelsestjeklistelinje i Styring af aktiver. Du kan oprette tilknytningen via en vedligeholdelsestjeklisteskabelon, en vedligeholdelsesjobtype eller en arbejdsordre, da alle tre indeholder vedligeholdelsestjeklistelinjer. Du kan spare tid ved at bruge en skabelon, da en skabelon kan knyttes til alle de vedligeholdelsesjobtyper, der bruger den. En hjælpelinje, der f.eks. er tilknyttet en vedligeholdelsesjobtype, knyttes automatisk til alle de arbejdsordrer, der angiver den pågældende jobtype. På den anden side eksisterer en hjælpelinje, der er tilknyttet en arbejdsordre direkte, kun for den pågældende arbejdsordre.

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a>Knytte en hjælpelinje til en vedligeholdelsestjeklisteskabelon

Du kan knytte en hjælpelinje til en vedligeholdelsestjekliste ved at følge disse trin.

1. Opret en hjælpelinje ved hjælp af Dynamics 365 Guides-pc- og HoloLens-appen. Du kan få oplysninger om, hvordan du opretter en hjælpelinje, i følgende emner:

    - [Bruge pc-appen til at oprette en hjælpelinje](/dynamics365/mixed-reality/guides/pc-app-overview)
    - [Bruge HoloLens-appen til at placere din hologrammer](/dynamics365/mixed-reality/guides/hololens-app-overview)

1. [Opret en vedligeholdelsestjeklisteskabelon](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template) i Supply Chain Management.
1. Knyt den hjælpelinje, du har oprettet, til en vedligeholdelsestjeklistelinje i den nye vedligeholdelsestjeklisteskabelon:

    1. På oversigtspanelet **Vedligeholdelsestjeklistelinjer** skal du vælge den linje, du vil knytte hjælpelinjen til.
    1. Vælg **Tilføj hjælpelinje** på oversigtspanelet **Tilknyttede hjælpelinjer**.

        ![Knytte en hjælpelinje til en vedligeholdelsestjeklistelinje.](media/am-guides-integration-add-guide.png "Knytte en hjælpelinje til en vedligeholdelsestjeklistelinje")

    1. Vælg en hjælpelinje i feltet **Navn**, og vælg derefter **Gem**.

        ![Vælge en hjælpelinje i feltet Navn.](media/am-guides-integration-select-guide.png "Vælge en hjælpelinje i feltet Navn")

1. Knyt vedligeholdelsestjeklisteskabelonen til en jobtype:

    1. [Opret en vedligeholdelsesjobtype](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), eller vælg en eksisterende vedligeholdelsesjobtype.
    1. Vælg **Standarder for vedligeholdelsesjobtype** i handlingsruden.

        ![Knappen Standarder for vedligeholdelsesjobtype.](media/am-guides-integration-job-defaults.png "Knappen Standarder for vedligeholdelsesjobtype")

    1. Opret en linje, og vælg derefter **Gem**.

        ![Oprette en linje.](media/am-guides-integration-add-line.png "Oprette en linje")

    1. Vælg **Vedligeholdelsestjekliste** i handlingsruden.

        ![Knappen Vedligeholdelsestjekliste.](media/am-guides-integration-maintenance-checklist.png "Knappen Vedligeholdelsestjekliste")

    1. På oversigtspanelet **Vedligeholdelsestjeklistelinjer** skal du tilføje en linje og derefter ændre værdien i feltet **Type** til **Skabelon**.

        ![Ændre værdien Type.](media/am-guides-integration-checklist-lines.png "Ændre værdien Type")

    1. Vælg den skabelon, du har knyttet til hjælpelinjen, i feltet **Skabelon** på oversigtspanelet **Linjedetaljer**, og vælg derefter **Gem**.

        ![Vælge skabelonen.](media/am-guides-integration-checklist-line-details.png "Vælge skabelonen")

1. [Opret en arbejdsordre](work-orders/manually-created-workorders.md#create-work-order), og vælg derefter den vedligeholdelsesjobtype, der bruger den vedligeholdelsestjeklisteskabelon, du har tilknyttet hjælpelinjen med. Hjælpelinjen knyttes automatisk til arbejdsordren.

    ![Vælge en vedligeholdelsesjobtype.](media/am-guides-integration-create-work-order.png "Vælge en vedligeholdelsesjobtype")

1. Få vist den hjælpelinje, der er tilknyttet arbejdsordren og arbejderne:

    1. Åbn [Arbejdsområdet Styring af aktiver på mobilenheder](asset-management-mobile-workspace.md) for at få adgang til arbejdsordren.
    1. [Åbn vedligeholdelsestjeklisten](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for arbejdsordren.
    1. Vælg en tjeklistelinje for at få vist den tilknyttede hjælpelinje.

        ![Hjælpelinje knyttet til en tjeklistelinje.](media/am-guides-integration-show-guide.png "Hjælpelinje knyttet til en tjeklistelinje")

    1. Åbn hjælpelinjen i HoloLens.

        ![Åbne hjælpelinjen i HoloLens.](media/am-guides-integration-hololens-select.png "Åbne hjælpelinjen i HoloLens")

> [!NOTE]
> Du kan også knytte en hjælpelinje direkte til vedligeholdelsestjeklisten for en arbejdsordre eller en jobtype.

> [!IMPORTANT]
> Der er et velkendt problem, når du knytter en vedligeholdelsestjeklisteskabelon til en standardvedligeholdelsesjobtype, hvor hjælpelinjen, der er tilknyttet skabelonen, ikke vises på oversigtspanelet **Tilknyttede hjælpelinjer** på siden **Standarder for vedligeholdelsesjobtype**. Hjælpelinjen vises dog, når denne jobtype anvendes på en arbejdsordre på oversigtspanelet **Tilknyttede hjælpelinjer**.

## <a name="see-also"></a>Se også

- [Oversigt over dobbeltskrivning](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [Oversigt over aktivstyring](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]