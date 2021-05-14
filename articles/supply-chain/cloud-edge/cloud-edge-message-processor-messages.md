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
# <a name="message-processor-messages"></a><span data-ttu-id="884ad-103">Meddelelser om meddelelsesprocessor</span><span class="sxs-lookup"><span data-stu-id="884ad-103">Message processor messages</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="884ad-104">Meddelelser fra Meddelelsesprocessoren anvendes ved kørsel af cloud- og kantskaleringsenheder til [produktionsbelastninger](cloud-edge-workload-manufacturing.md) og [belastninger i lagerstedsstyring](cloud-edge-workload-warehousing.md)</span><span class="sxs-lookup"><span data-stu-id="884ad-104">Message processor messages are used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="884ad-105">Der udveksles store mængder data mellem installationsmiljøerne for hubber og skaleringsenheder for at holde dem synkroniserede, men kun nogle få af disse dataudvekslinger behandles af *meddelelsesprocessoren*.</span><span class="sxs-lookup"><span data-stu-id="884ad-105">A large amount of data is exchanged between the hub and scale unit deployment environments to keep them in sync, but only a few of these data exchanges will be processed by the *message processor*.</span></span> <span data-ttu-id="884ad-106">Du kan få vist de meddelelser, der er behandlet af meddelelsesprocessoren, ved at gå til **Systemadministration > Meddelelsesprocessor > Meddelelser for meddelelsesprocessor**.</span><span class="sxs-lookup"><span data-stu-id="884ad-106">You can view the messages processed by the message processor by going to **System administration > Message processor > Message processor messages**.</span></span>

## <a name="message-grid-columns-and-filters"></a><span data-ttu-id="884ad-107">Kolonner og filtre i meddelelsesgitteret</span><span class="sxs-lookup"><span data-stu-id="884ad-107">Message grid columns and filters</span></span>

<span data-ttu-id="884ad-108">Du kan bruge felterne øverst på siden **Meddelelser for meddelelsesprocessor** til at finde bestemte meddelelser, du søger efter.</span><span class="sxs-lookup"><span data-stu-id="884ad-108">You can use the fields at the top of the **Message processor messages** page to help find any particular messages you are looking for.</span></span> <span data-ttu-id="884ad-109">De fleste af disse filtre svarer til kolonneoverskrifterne i meddelelsesgitteret.</span><span class="sxs-lookup"><span data-stu-id="884ad-109">Most of these filters match the column headings in the message grid.</span></span> <span data-ttu-id="884ad-110">Følgende filter- og kolonneoverskrifter er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="884ad-110">The following filters and column headings are available:</span></span>

- <span data-ttu-id="884ad-111">**Meddelelsestype** – Angiver meddelelsestypen.</span><span class="sxs-lookup"><span data-stu-id="884ad-111">**Message type** – Specifies the type of message.</span></span>
- <span data-ttu-id="884ad-112">**Meddelelseskø** – Angiver navnet på den kø, som meddelelsen skal behandles i.</span><span class="sxs-lookup"><span data-stu-id="884ad-112">**Message queue** – Specifies the name of the queue in which the message is to be processed.</span></span> <span data-ttu-id="884ad-113">Følgende køer er angivet:</span><span class="sxs-lookup"><span data-stu-id="884ad-113">The following queues are provided:</span></span>
  - <span data-ttu-id="884ad-114">*Skalaenhed til hub*</span><span class="sxs-lookup"><span data-stu-id="884ad-114">*Scale unit to hub*</span></span>
  - <span data-ttu-id="884ad-115">*Hub til skalaenhed for lagerstedsudførelse*</span><span class="sxs-lookup"><span data-stu-id="884ad-115">*Hub to warehouse execution scale unit*</span></span>
  - <span data-ttu-id="884ad-116">*Hub til skalaenhed for produktionsudførelse*</span><span class="sxs-lookup"><span data-stu-id="884ad-116">*Hub to manufacturing execution scale unit*</span></span>
- <span data-ttu-id="884ad-117">**Meddelelsestilstand** – Angiver meddelelsens tilstand.</span><span class="sxs-lookup"><span data-stu-id="884ad-117">**Message state** – Specifies the state of the message.</span></span> <span data-ttu-id="884ad-118">Der findes følgende tilstande:</span><span class="sxs-lookup"><span data-stu-id="884ad-118">The following states exists:</span></span>
  - <span data-ttu-id="884ad-119">*Kø* – Meddelelsen er klar til at blive behandlet af meddelelsesprocessoren.</span><span class="sxs-lookup"><span data-stu-id="884ad-119">*Queued* – The message is ready to be processed by the message processor.</span></span>
  - <span data-ttu-id="884ad-120">*Behandlet* – Meddelelsen er blevet behandlet af meddelelsesprocessoren.</span><span class="sxs-lookup"><span data-stu-id="884ad-120">*Processed* – The message was successfully processed by the message processor.</span></span>
  - <span data-ttu-id="884ad-121">*Annulleret* – Meddelelsen blev behandlet, men behandlingen mislykkedes.</span><span class="sxs-lookup"><span data-stu-id="884ad-121">*Canceled* – The message was processed, but processing failed.</span></span>
- <span data-ttu-id="884ad-122">**Meddelelses indhold** – Dette filter udfører en fuldtekstsøgning af meddelelsens indhold.</span><span class="sxs-lookup"><span data-stu-id="884ad-122">**Message content** – This filter does a full-text search of message content.</span></span> <span data-ttu-id="884ad-123">(Meddelelses indhold vises ikke i gitteret.) Filteret behandler de fleste specialsymboler (som f.eks. "-") som mellemrum, og alle mellemrum behandles som booleske OR-operatorer.</span><span class="sxs-lookup"><span data-stu-id="884ad-123">(Message content is not shown in the grid.) The filter treats most special symbols (such as "-") as spaces, and treats all space characters as Boolean OR operators.</span></span> <span data-ttu-id="884ad-124">T=Hvis du søger efter en bestemt værdi for en bestemt `journalid`-værdi svarende til "USMF-123456", vil systemet finde alle meddelelser, der indeholder "USMF" eller "123456", hvilket sandsynligvis vil give en lang liste.</span><span class="sxs-lookup"><span data-stu-id="884ad-124">T=For example, this means if you search for a specific `journalid` value equal "USMF-123456", the system will find all messages that contain "USMF" or "123456", which is likely to be a long list.</span></span> <span data-ttu-id="884ad-125">Det vil derfor være bedre kun at angive "123456", fordi det vil returnere mere specifikke resultater.</span><span class="sxs-lookup"><span data-stu-id="884ad-125">Therefore, it would be better to enter just "123456" alone because that will return more specific results.</span></span>

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a><span data-ttu-id="884ad-126">Eksempel på meddelelsestype: Anmode om økonomisk opdatering af lagerregulering</span><span class="sxs-lookup"><span data-stu-id="884ad-126">Example message type: Request inventory adjustment financial update</span></span>

<span data-ttu-id="884ad-127">**Meddelelsestypen** *Anmod om økonomisk opdatering af lagerregulering* bruges f.eks. til at oprette og bogføre en optællingskladde i hubben, når en arbejder bruger lagerstedsappen til at [registrere en lagerregulering](cloud-edge-warehouse-inventory-adjustment.md) i en skaleringsenhed for lagerstedsstyringens arbejdsbelastning.</span><span class="sxs-lookup"><span data-stu-id="884ad-127">For example, the **Message type** *Request inventory adjustment financial update* is used to create and post a counting journal on the hub when a worker uses the warehouse app to [register an inventory adjustment](cloud-edge-warehouse-inventory-adjustment.md) on a scale unit warehouse management workload.</span></span> <span data-ttu-id="884ad-128">Da denne specifikke proces stammer fra en skaleringsenhed, viser feltet **Meddelelseskø** værdien *Skaleringsenhed til hub*.</span><span class="sxs-lookup"><span data-stu-id="884ad-128">Because this specific process originates from a scale unit, the **Message queue** field will show the value *Scale unit to hub*.</span></span>

<span data-ttu-id="884ad-129">For denne meddelelsestype registrerer en arbejdsbyrden for en skaleringsenhed meddelelsen som en del af en lagerreguleringshandling for en lagerstedsapp.</span><span class="sxs-lookup"><span data-stu-id="884ad-129">For this message type, a scale unit workload records the message as part of a warehouse app inventory adjustment operation.</span></span> <span data-ttu-id="884ad-130">Meddelelsesdataene overføres derefter til hubben som en del af den samme proces, der bruges til [arkitekturen for Commerce Data Exchange](../../commerce/commerce-architecture.md).</span><span class="sxs-lookup"><span data-stu-id="884ad-130">The message data is then transferred to the hub as part of the same process used for the [Commerce data exchange architecture](../../commerce/commerce-architecture.md).</span></span> <span data-ttu-id="884ad-131">Meddelelsen opdateres, så den viser **Meddelelses tilstand** som *Kø*.</span><span class="sxs-lookup"><span data-stu-id="884ad-131">The message will be updated to show **Message state** as *Queued*.</span></span> <span data-ttu-id="884ad-132">Meddelelsesprocessoren forsøger derefter at behandle meddelelsen og opdaterer **Meddelelses tilstand** til *Behandlet* ved fuldført behandling eller *Annulleret* ved fejl.</span><span class="sxs-lookup"><span data-stu-id="884ad-132">The message processor then attempts to process the message and updates the **Message state** to *Processed* on success, or *Canceled* on failure.</span></span>

## <a name="view-the-message-log-message-content-and-details"></a><span data-ttu-id="884ad-133">Få vist meddelelsesloggen, meddelelses indhold og detaljer</span><span class="sxs-lookup"><span data-stu-id="884ad-133">View the message log, message content, and details</span></span>

<span data-ttu-id="884ad-134">Du kan finde detaljerede oplysninger om en meddelelse ved at markere den i gitteret og derefter åbne fanerne **Log** eller **Meddelelses indhold** under meddelelsesgitteret, hvor hver enkelt behandlingshændelse vises.</span><span class="sxs-lookup"><span data-stu-id="884ad-134">You can find detailed information about a message by selecting it in the grid and then opening the **Log** or **Message content** tabs under the message grid, where each processing event is shown.</span></span>

<span data-ttu-id="884ad-135">**Meddelelses indhold** afhænger af **Meddelelsestype** og vil derfor have en anden tekstlængde.</span><span class="sxs-lookup"><span data-stu-id="884ad-135">The **Message content** depends on the **Message type** and will therefore have different text length.</span></span> <span data-ttu-id="884ad-136">En typisk tekst til meddelelsens indhold begynder med **{** og slutter med **}** og derimellem vises feltnavne som f.eks. `journalId` efterfulgt af **:** og en værdi som f.eks. *USMF-123456*.</span><span class="sxs-lookup"><span data-stu-id="884ad-136">A typical message content text will start with a **{** and end with a **}** and in between have field names such as `journalId` followed by a **:** and a value such as *USMF-123456*.</span></span>

<span data-ttu-id="884ad-137">Værktøjslinjen under fanen **Log** indeholder følgende knapper:</span><span class="sxs-lookup"><span data-stu-id="884ad-137">The toolbar on the **Log** tab includes the following buttons:</span></span>

- <span data-ttu-id="884ad-138">**Log** – Viser behandlingsresultaterne.</span><span class="sxs-lookup"><span data-stu-id="884ad-138">**Log** – Displays the processing results.</span></span> <span data-ttu-id="884ad-139">Det er især nyttigt, når du skal forstå årsagerne til en behandlingsfejl i meddelelser med **Behandlingsresultat** angivet til *Mislykket*.</span><span class="sxs-lookup"><span data-stu-id="884ad-139">This is especially helpful for understanding the reasons for a processing failure for messages having a **Processing result** of *Failed*.</span></span>
- <span data-ttu-id="884ad-140">**Bundt** – Du kan køre flere operationer til behandling af meddelelser som en del af samme batchproces.</span><span class="sxs-lookup"><span data-stu-id="884ad-140">**Bundle** – Multiple message processing operations can run as part of the same batch process.</span></span> <span data-ttu-id="884ad-141">Klik på denne knap for at få vist disse detaljerede data.</span><span class="sxs-lookup"><span data-stu-id="884ad-141">Select this button to view this detailed data.</span></span> <span data-ttu-id="884ad-142">Du kan f.eks. se, om der findes afhængigheder, som kræver, at systemet behandler bestemte meddelelser i en bestemt rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="884ad-142">For example, you can see whether dependencies exist that require the system to process certain messages in a specific sequence.</span></span>

## <a name="message-processor-batch-job"></a><span data-ttu-id="884ad-143">Batchjob for meddelelsesprocessor</span><span class="sxs-lookup"><span data-stu-id="884ad-143">Message processor batch job</span></span>

<span data-ttu-id="884ad-144">Når du kører en cloud- og kantinstallation, startes batchjobbet *Meddelelsesprocessor* automatisk, når der oprettes en ny meddelelse til behandling, så du ikke behøver at planlægge dette job manuelt.</span><span class="sxs-lookup"><span data-stu-id="884ad-144">When running a cloud and edge deployment, the *Message processor* batch job will automatically be evoked when a new message is created for processing, so you should not need to schedule this job manually.</span></span>

<span data-ttu-id="884ad-145">Hvis det er nødvendigt, kan du få adgang til batchjobbet ved at gå til **Systemadministration > Meddelelsesprocessor > Meddelelsesprocessor**.</span><span class="sxs-lookup"><span data-stu-id="884ad-145">If necessary, you can access the batch job by going to **System administration > Message  processor > Message processor**.</span></span>

## <a name="manually-process-or-cancel-a-message"></a><span data-ttu-id="884ad-146">Behandle eller annullere en meddelelse manuelt</span><span class="sxs-lookup"><span data-stu-id="884ad-146">Manually process or cancel a message</span></span>

<span data-ttu-id="884ad-147">Du kan om nødvendigt behandle eller annullere en meddelelse manuelt, afhængigt af dens aktuelle tilstand.</span><span class="sxs-lookup"><span data-stu-id="884ad-147">If needed, you can manually process or cancel a message, depending on its current state.</span></span> <span data-ttu-id="884ad-148">Det gør du ved at markere meddelelsen i gitteret og derefter vælge **Behandl** eller **Annuller** i handlingsruden</span><span class="sxs-lookup"><span data-stu-id="884ad-148">To do so, select the message in the grid and then select **Process** or **Cancel** on the Action Pane</span></span>

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a><span data-ttu-id="884ad-149">Konfigurere virksomhedshændelser for at give besked om mislykket behandling af data</span><span class="sxs-lookup"><span data-stu-id="884ad-149">Set up business events to deliver alerts for failed processing results</span></span>

<span data-ttu-id="884ad-150">Udover filtrering ud fra værdien *Annulleret* for **Meddelelsestilstand** for at forespørge på mislykkede meddelelser, kan du konfigurere [Virksomhedshændelser](../../fin-ops-core/dev-itpro/business-events/home-page.md) i hubben for at give dig besked om mislykket behandling af data.</span><span class="sxs-lookup"><span data-stu-id="884ad-150">In addition to filtering on the **Message state** value *Canceled* to inquire for failed messages, you can set up [Business events](../../fin-ops-core/dev-itpro/business-events/home-page.md) on the hub to alert you to failed processing results.</span></span> <span data-ttu-id="884ad-151">Det gør du ved at aktivere virksomhedshændelsen *Meddelelse for meddelelsesprocessor behandlet* på siden **Katalog over virksomhedshændelser** (**Systemadministration > Opsætning > Virksomhedshændelser > Katalog over virksomhedshændelser**).</span><span class="sxs-lookup"><span data-stu-id="884ad-151">To do so, activate the business event named *Message processor message processed*  on the **Business events catalog** page (**System administration > Setup > Business events > Business events catalog**).</span></span>

<span data-ttu-id="884ad-152">Som en del af aktiveringsprocessen bliver du guidet til at angive, om hændelsen er specifik for en eller alle juridiske enheder, og angive et **Slutpunktnavn**, som skal defineres først.</span><span class="sxs-lookup"><span data-stu-id="884ad-152">As part of the activation process, you will be guided to specify whether the event is specific to one or all legal entities and provide an **Endpoint name**, which must be defined first.</span></span>

>[!NOTE]
> <span data-ttu-id="884ad-153">Hvis **Når en virksomhedshændelse indtræffer** er angivet til *Microsoft Power Automate* (i stedet for *HTTPS*), oprettes **Slutpunktsnavn** automatisk automatisk i Supply Chain Management baseret på opsætningen af *Microsoft Power Automate*.</span><span class="sxs-lookup"><span data-stu-id="884ad-153">If **When a Business Event occurs** is set to *Microsoft Power Automate* (rather than *HTTPS*, for example), the **Endpoint name** will automatically be created in Supply Chain Management based on the *Microsoft Power Automate* setup.</span></span>

### <a name="microsoft-power-automate-example"></a><span data-ttu-id="884ad-154">Eksempel på Microsoft Power Automate</span><span class="sxs-lookup"><span data-stu-id="884ad-154">Microsoft Power Automate example</span></span>

<span data-ttu-id="884ad-155">I dette eksempel vil **Når en virksomhedshændelse indtræffer** sammen med *Microsoft Power Automate* sende mails med InfoLog-meddelelser og hyperlinks til åbning af siden **Meddelelser for meddelelsesprocessor** for en specifik mislykket meddelelse i hubinstallationen.</span><span class="sxs-lookup"><span data-stu-id="884ad-155">In this example, use **When a Business Event occurs** with *Microsoft Power Automate* sends emails containing InfoLog messages and hyperlinks to open the **Message processor messages** page for a specific failed message on the hub deployment.</span></span> <span data-ttu-id="884ad-156">Hvis det er nødvendigt, kan du tilføje ekstra logik for at sende beskederne parallelt ved hjælp af forskellige kanaler og kontrollere modtagerne ud fra hændelsesdataene.</span><span class="sxs-lookup"><span data-stu-id="884ad-156">If needed, you can add extra logic to send the notifications in parallel using different channels and control the recipients based on the event data.</span></span>

1. <span data-ttu-id="884ad-157">I [Power Automate](https://preview.flow.microsoft.com) skal du oprette et nyt automatisk cloudflow for flowudløseren **Når der forekommer en virksomhedshændelse – Fin & Ops App (Dynamics 365)** efterfulgt af trinnene **Analysér JSON** og **Send en mail** som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="884ad-157">In [Power Automate](https://preview.flow.microsoft.com), create a new automated cloud flow for the flow trigger **When a Business Event occurs - Fin & Ops App (Dynamics 365)** followed by the **Parse JSON** and **Send an email** steps, as shown in the following illustration.</span></span>

    Automatiseret :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate-cloudflow":::

1. <span data-ttu-id="884ad-159">I trinnet **Når en virksomhedshændelse indtræffer** kan du søge efter eller indtaste hubbens **Forekomst** efter **Kategori**, og derefter *Meddelelse for meddelelsesprocessor behandlet* for **Virksomhedshændelse** som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="884ad-159">In the **When a Business Event occurs** step, you can look up or enter the hub **Instance** following the **Category** and then the **Business event** *Message processor message processed*, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate-trinnet Når en virksomhedshændelse forekommer":::

1. <span data-ttu-id="884ad-161">I trinnet **Analysér JSON** skal du angive et **Skema**, der definerer de udvidede felter.</span><span class="sxs-lookup"><span data-stu-id="884ad-161">For the **Parse JSON** step, enter a **Schema** that defines the extended fields.</span></span> <span data-ttu-id="884ad-162">Du kan bruge indstillingen *Hent skema* på siden **Katalog over virksomhedshændelser** i Supply Chain Management eller starte med at indsætte eksempeltekst i skemaet.</span><span class="sxs-lookup"><span data-stu-id="884ad-162">You can use the *Download schema* option on the **Business events catalog** page in Supply Chain Management or start by pasting in the example schema text.</span></span> <span data-ttu-id="884ad-163">Denne eksempeltekst vises efter følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="884ad-163">This example text is provided after the following illustration.</span></span>

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

1. <span data-ttu-id="884ad-165">I trinnet **Send en mail** kan du vælge de enkelte felter eller starte med at indsætte eksempeltekst i mailen i feltet **Brødtekst**.</span><span class="sxs-lookup"><span data-stu-id="884ad-165">In the **Send an email** step, you can select the individual fields or start by pasting the email body example into the **Body** field.</span></span> <span data-ttu-id="884ad-166">Dette eksempel vises efter følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="884ad-166">This example is provided after the following illustration.</span></span>

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

1. <span data-ttu-id="884ad-168">Når du gemmer virksomhedshændelsen, aktiveres den automatisk og er klar til brug som en del af Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="884ad-168">When you save the business event, it will automatically be activated and ready to use as part of Supply Chain Management.</span></span>
