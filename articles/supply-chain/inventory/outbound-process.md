---
title: Oversigt over udgående proces
description: Denne artikel indeholder en oversigt over den udgående proces i Lagerstyring.
author: yufeihuang
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "274363"
- intro-internal
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 4e3c97862858e219d98b4ef9a81b52c6ab1623ab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852470"
---
# <a name="outbound-process-overview"></a>Oversigt over udgående proces

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over den udgående proces i Lagerstyring.

## <a name="output-orders"></a>Udlagringsordrer

Udlagringsordrer bruges til at sammenkæde salgsordrelinjer og flytteordrelinjer med udgående plukprocesser, der bruger pluklister.

Når pluklister genereres fra enten salgsordrer eller flytteordrer, oprettes outputordrer og forsendelser automatisk. En plukliste har en en til en-relation med en forsendelse. Flytteordreforsendelsen eller salgsordrefølgesedlen kan behandles fra forsendelsen. 

Følgende diagram viser en oversigt over processen for udgående ordrer. 

[![Oversigt over processen for udgående ordre.](./media/outbound-order.png)](./media/outbound-order.png)

Du kan konfigurere udgående regler for at definere, hvordan programmet skal håndtere den udgående proces. Du kan bruge disse regler til at styre forsendelsesprocessen. Du kan især bruge reglerne til at styre, hvilket stadie i processen en forsendelse kan sendes under. Følgende indstillinger definerer, hvordan udgående processer håndteres.

## <a name="picking-route-status-for-sales-and-transfer-orders"></a>Status for plukrute for salgsordrer og flytteordrer 

Gå til **Debitor** \> **Konfiguration** \> **Debitorparametre**, og under fanen **Opdateringer** skal du vælge en værdi i feltet **Plukrutestatus**.

[![Feltet Plukrutestatus for salgsordrer.](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)

Hvis feltet **Plukrutestatus** er angivet til **Fuldført**, sker plukprocessen automatisk som en del af processen til oprettelse af pluklister. Hvis feltet er angivet til **Aktiveret**, skal pluklinjerne opdateres manuelt.

Den samme opsætning gælder for flytteordrer. Gå til **Lagerstyring** \> **Konfiguration** \> **Parametre til lager- og lokationsstyring**, og under fanen **Transport** skal du derefter vælge en værdi i feltet **Plukrutestatus**.

[![Feltet Plukrutestatus for flytteordrer.](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)

## <a name="end-output-inventory-orders"></a>Afslut udgående lagerordrer

Gå til **Lagerstyring** \> **Konfiguration** \> **Parametre til lager- og lokationsstyring**, og angive derefter under fanen **Generelt** indstillingen **Afslut udgående lagerordre**.

[![Indstillingen Afslut udgående lagerordre.](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)

Når lagermedarbejderen reducerer pluklisteantallene, fjernes de tilsvarende lagerordreantal fra forsendelsen. Når pluklisten opdateres på et tidspunkt, rapporteres den resterende mængde tilbage til ordren, hvis indstillingen **Afslut udgående lagerordre** er angivet til **Ja**. Hvis den **Afslut udgående lagerordre** er angivet til **Nej**, bevares de resterende mængder som et åbent outputordreantal og skal føjes til en ny plukliste som en del af funktionen **Åbne udlagringsordrer**. 

[![Kommandoen Åbn outputordrer i menuen Funktioner.](./media/open-output-order.png)](./media/open-output-order.png)

[![Menuen Funktioner på siden Åbne outputordrer.](./media/open-output-order-function.png)](./media/open-output-order-function.png)

## <a name="reduce-quantity"></a>Reducer antal

Den tredje parameter, som du kan bruge som en del af processen til oprettelse af pluklister er parameteren **Reducer antal**. Indstillingen af denne parameter bruges sammen med indstillingen **Reservation**, der udløser en reservationsproces som en del af frigivelsen til lageret.

[![Parameteren Reducer antal.](./media/reduce-quantity.png)](./media/reduce-quantity.png)

## <a name="example-of-an-outbound-process-for-a-sales-order"></a>Eksempel på en udgående proces for en salgsordre

I dette eksempel er der en salgsordre på to varer. Under pluklisteoprettelsen vælger du parameteren **Reducer antal**. Derfor kan du kun frigive og oprette pluklinjer for tilgængeligt disponibelt lager. Plukningen skal rapporteres via en registreringsproces for pluklister (**Plukrutestatus** = **Aktiveret**).

Det lager, der ikke allerede er reserveret, reserveres under pluklisteoprettelsen. Den ikke-disponible lagerbeholdning kan enten fjernet fra salgsordren eller frigives til lageret til senere udgående behandling, når lagerbeholdningen ikke er disponibel til pluk.

[![Opdater pluklisten.](./media/update-picking-list.png)](./media/update-picking-list.png)

Så snart pluklinjerne er blevet plukket på siden **Pluklisteregistrering**, fuldføres den tilknyttede forsendelse. Processen for følgesedler for salgsordren kan derefter initialiseres baseret på den plukkede lagerbeholdning.

[![Opdater udgående forsendelser.](./media/outbound-shipments.png)](./media/outbound-shipments.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]