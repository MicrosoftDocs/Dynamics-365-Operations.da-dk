---
title: Meddelelser om meddelelsesprocessor
description: Dette emne indeholder oplysninger om meddelelsesfunktionen Meddelelsesprocessor for belastninger af skaleringsenheder.
author: perlynne
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b1428e2e657e653874d4ec07605932a32bd803b2
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938244"
---
# <a name="message-processor-messages"></a>Meddelelser om meddelelsesprocessor

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Meddelelser fra Meddelelsesprocessoren anvendes ved kørsel af cloud- og kantskaleringsenheder til [produktionsbelastninger](cloud-edge-workload-manufacturing.md) og [belastninger i lagerstedsstyring](cloud-edge-workload-warehousing.md)

Der udveksles store mængder data mellem installationsmiljøerne for hubber og skaleringsenheder for at holde dem synkroniserede, men kun nogle få af disse dataudvekslinger behandles af *meddelelsesprocessoren*. Du kan få vist de meddelelser, der er behandlet af meddelelsesprocessoren, ved at gå til **Systemadministration > Meddelelsesprocessor > Meddelelser for meddelelsesprocessor**.

## <a name="message-grid-columns-and-filters"></a>Kolonner og filtre i meddelelsesgitteret

Du kan bruge felterne øverst på siden **Meddelelser for meddelelsesprocessor** til at finde bestemte meddelelser, du søger efter. De fleste af disse filtre svarer til kolonneoverskrifterne i meddelelsesgitteret. Følgende filter- og kolonneoverskrifter er tilgængelige:

- **Meddelelsestype** – Angiver meddelelsestypen.
- **Meddelelseskø** – Angiver navnet på den kø, som meddelelsen skal behandles i. Følgende køer er angivet:
  - *Skalaenhed til hub*
  - *Hub til skalaenhed for lagerstedsudførelse*
  - *Hub til skalaenhed for produktionsudførelse*
- **Meddelelsestilstand** – Angiver meddelelsens tilstand. Der findes følgende tilstande:
  - *Kø* – Meddelelsen er klar til at blive behandlet af meddelelsesprocessoren.
  - *Behandlet* – Meddelelsen er blevet behandlet af meddelelsesprocessoren.
  - *Annulleret* – Meddelelsen blev behandlet, men behandlingen mislykkedes.
- **Meddelelses indhold** – Dette filter udfører en fuldtekstsøgning af meddelelsens indhold. (Meddelelses indhold vises ikke i gitteret.) Filteret behandler de fleste specialsymboler (som f.eks. "-") som mellemrum, og alle mellemrum behandles som booleske OR-operatorer. T=Hvis du søger efter en bestemt værdi for en bestemt `journalid`-værdi svarende til "USMF-123456", vil systemet finde alle meddelelser, der indeholder "USMF" eller "123456", hvilket sandsynligvis vil give en lang liste. Det vil derfor være bedre kun at angive "123456", fordi det vil returnere mere specifikke resultater.

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a>Eksempel på meddelelsestype: Anmode om økonomisk opdatering af lagerregulering

**Meddelelsestypen** *Anmod om økonomisk opdatering af lagerregulering* bruges f.eks. til at oprette og bogføre en optællingskladde i hubben, når en arbejder bruger lagerstedsappen til at [registrere en lagerregulering](cloud-edge-warehouse-inventory-adjustment.md) i en skaleringsenhed for lagerstedsstyringens arbejdsbelastning. Da denne specifikke proces stammer fra en skaleringsenhed, viser feltet **Meddelelseskø** værdien *Skaleringsenhed til hub*.

For denne meddelelsestype registrerer en arbejdsbyrden for en skaleringsenhed meddelelsen som en del af en lagerreguleringshandling for en lagerstedsapp. Meddelelsesdataene overføres derefter til hubben som en del af den samme proces, der bruges til [arkitekturen for Commerce Data Exchange](../../commerce/commerce-architecture.md). Meddelelsen opdateres, så den viser **Meddelelses tilstand** som *Kø*. Meddelelsesprocessoren forsøger derefter at behandle meddelelsen og opdaterer **Meddelelses tilstand** til *Behandlet* ved fuldført behandling eller *Annulleret* ved fejl.

## <a name="view-the-message-log-message-content-and-details"></a>Få vist meddelelsesloggen, meddelelses indhold og detaljer

Du kan finde detaljerede oplysninger om en meddelelse ved at markere den i gitteret og derefter åbne fanerne **Log** eller **Meddelelses indhold** under meddelelsesgitteret, hvor hver enkelt behandlingshændelse vises.

**Meddelelses indhold** afhænger af **Meddelelsestype** og vil derfor have en anden tekstlængde. En typisk tekst til meddelelsens indhold begynder med **{** og slutter med **}** og derimellem vises feltnavne som f.eks. `journalId` efterfulgt af **:** og en værdi som f.eks. *USMF-123456*.

Værktøjslinjen under fanen **Log** indeholder følgende knapper:

- **Log** – Viser behandlingsresultaterne. Det er især nyttigt, når du skal forstå årsagerne til en behandlingsfejl i meddelelser med **Behandlingsresultat** angivet til *Mislykket*.
- **Bundt** – Du kan køre flere operationer til behandling af meddelelser som en del af samme batchproces. Klik på denne knap for at få vist disse detaljerede data. Du kan f.eks. se, om der findes afhængigheder, som kræver, at systemet behandler bestemte meddelelser i en bestemt rækkefølge.

## <a name="message-processor-batch-job"></a>Batchjob for meddelelsesprocessor

Når du kører en cloud- og kantinstallation, startes batchjobbet *Meddelelsesprocessor* automatisk, når der oprettes en ny meddelelse til behandling, så du ikke behøver at planlægge dette job manuelt.

Hvis det er nødvendigt, kan du få adgang til batchjobbet ved at gå til **Systemadministration > Meddelelsesprocessor > Meddelelsesprocessor**.

## <a name="manually-process-or-cancel-a-message"></a>Behandle eller annullere en meddelelse manuelt

Du kan om nødvendigt behandle eller annullere en meddelelse manuelt, afhængigt af dens aktuelle tilstand. Det gør du ved at markere meddelelsen i gitteret og derefter vælge **Behandl** eller **Annuller** i handlingsruden

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Konfigurere virksomhedshændelser for at give besked om mislykket behandling af data

Udover filtrering ud fra værdien *Annulleret* for **Meddelelsestilstand** for at forespørge på mislykkede meddelelser, kan du konfigurere [Virksomhedshændelser](../../fin-ops-core/dev-itpro/business-events/home-page.md) i hubben for at give dig besked om mislykket behandling af data. Det gør du ved at aktivere virksomhedshændelsen *Meddelelse for meddelelsesprocessor behandlet* på siden **Katalog over virksomhedshændelser** (**Systemadministration > Opsætning > Virksomhedshændelser > Katalog over virksomhedshændelser**).

Som en del af aktiveringsprocessen bliver du guidet til at angive, om hændelsen er specifik for en eller alle juridiske enheder, og angive et **Slutpunktnavn**, som skal defineres først.

>[!NOTE]
> Hvis **Når en virksomhedshændelse indtræffer** er angivet til *Microsoft Power Automate* (i stedet for *HTTPS*), oprettes **Slutpunktsnavn** automatisk automatisk i Supply Chain Management baseret på opsætningen af *Microsoft Power Automate*.

### <a name="microsoft-power-automate-example"></a>Eksempel på Microsoft Power Automate

I dette eksempel vil **Når en virksomhedshændelse indtræffer** sammen med *Microsoft Power Automate* sende mails med InfoLog-meddelelser og hyperlinks til åbning af siden **Meddelelser for meddelelsesprocessor** for en specifik mislykket meddelelse i hubinstallationen. Hvis det er nødvendigt, kan du tilføje ekstra logik for at sende beskederne parallelt ved hjælp af forskellige kanaler og kontrollere modtagerne ud fra hændelsesdataene.

1. I [Power Automate](https://preview.flow.microsoft.com) skal du oprette et nyt automatisk cloudflow for flowudløseren **Når der forekommer en virksomhedshændelse – Fin & Ops App (Dynamics 365)** efterfulgt af trinnene **Analysér JSON** og **Send en mail** som vist i følgende illustration.

    Automatiseret :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate-cloudflow":::

1. I trinnet **Når en virksomhedshændelse indtræffer** kan du søge efter eller indtaste hubbens **Forekomst** efter **Kategori**, og derefter *Meddelelse for meddelelsesprocessor behandlet* for **Virksomhedshændelse** som vist i følgende illustration.

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate-trinnet Når en virksomhedshændelse forekommer":::

1. I trinnet **Analysér JSON** skal du angive et **Skema**, der definerer de udvidede felter. Du kan bruge indstillingen *Hent skema* på siden **Katalog over virksomhedshændelser** i Supply Chain Management eller starte med at indsætte eksempeltekst i skemaet. Denne eksempeltekst vises efter følgende illustration.

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate-trinnet Analysér JSON":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. I trinnet **Send en mail** kan du vælge de enkelte felter eller starte med at indsætte eksempeltekst i mailen i feltet **Brødtekst**. Dette eksempel vises efter følgende illustration.

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate-trinnet Send en mail":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. Når du gemmer virksomhedshændelsen, aktiveres den automatisk og er klar til brug som en del af Supply Chain Management.
