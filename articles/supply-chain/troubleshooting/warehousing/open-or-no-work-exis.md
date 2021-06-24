---
title: Du kan ikke bekræfte en forsendelse på grund af ufuldstændig eller manglende arbejde
description: Du kan ikke bekræfte en forsendelse på grund af ufuldstændig eller manglende arbejde
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm, WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: beef0909d41e69f3e7bcc1021527be35b7e6fd44
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123837"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a>Du kan ikke bekræfte en forsendelse på grund af ufuldstændig eller manglende arbejde

Fejlkode: WAX515

## <a name="symptoms"></a>Symptomer

Når du forsøger at bekræfte en forsendelse, vises følgende fejlmeddelelse:

> Forsendelsen af lasten %1 kan ikke bekræftes, fordi alt arbejde på lasten skal være fuldført.

Du kan derfor ikke bekræfte forsendelsen for lasten.

## <a name="cause"></a>Årsag

Lasten eller forsendelsen er i øjeblikket i en tilstand, hvor forsendelsesbekræftelsen mislykkes. Inden du kan bekræfte forsendelsen, skal der som minimum være udført noget arbejde med lasten, og alt arbejde skal have statussen *Lukket* eller *Annulleret*.

## <a name="resolution"></a>Løsning

Kontrollér de relaterede salgsordrer eller flytteordrer for lasten eller forsendelsen, og kontrollér, at alt relateret arbejde er fuldført eller annulleret.

Du kan arbejde med forsendelser og last på flere sider. Følgende underafsnit indeholder nogle få eksempler.

### <a name="all-loads-page"></a>Side for alle laster

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Vælg den last, som forsendelsen ikke kan bekræftes for.
1. under fanen **Laster** i gruppen **Relaterede oplysninger** i handlingsruden skal du vælge **Arbejde**.
1. Kontrollér status for hvert arbejds-id. Følg op på hvert arbejds-id, der ikke har statussen *Lukket* eller *Annulleret*.
1. Når hvert arbejds-id har statussen *Lukket* eller *Annulleret*, kan du prøve igen at bekræfte forsendelsen.

### <a name="all-shipments-page"></a>Side for alle forsendelser

1. Gå til **Lagerstyringssted \> Forsendelser \> Alle forsendelser**.
1. Vælg den forsendelse, der ikke kan bekræftes.
1. Vælg **Forsendelser** i gruppen **Arbejde** i handlingsruden, og vælg **Arbejdsdetaljer**.
1. Kontrollér status for hvert arbejds-id. Følg op på hvert arbejds-id, der ikke har statussen *Lukket* eller *Annulleret*.
1. Når hvert arbejds-id har statussen *Lukket* eller *Annulleret*, kan du prøve igen at bekræfte forsendelsen.

### <a name="all-work-page"></a>Side for alt arbejde

1. Gå til **Lagerstedsstyring \> Arbejde \> Alt arbejde**.
1. Vælg det arbejde for ordrenummeret, som forsendelsen ikke kan bekræftes for.
1. I handlingsruden under fanen **Forsendelse** i gruppen **Forsendelse** skal du vælge **Bekræft forsendelse**.
1. Kontrollér status for hvert arbejds-id. Følg op på hvert arbejds-id, der ikke har statussen *Lukket* eller *Annulleret*.
1. Når hvert arbejds-id har statussen *Lukket* eller *Annulleret*, kan du prøve igen at bekræfte forsendelsen.
