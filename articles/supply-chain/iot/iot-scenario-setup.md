---
title: Scenarieopsætning for IoT-viden
description: Dette emne forklarer, hvordan du kan konfigurere scenarier for IoT-viden i Microsoft Dynamics 365 Supply Chain Management.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d1deaa2130b63272da39a42315c6a1bc4b7ccb8a
ms.sourcegitcommit: 8adc65e26d78e229271eb427659a87ee5f371319
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/15/2020
ms.locfileid: "3814053"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="0c063-103">Scenarieopsætning for IoT-viden</span><span class="sxs-lookup"><span data-stu-id="0c063-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0c063-104">Dette emne forklarer, hvordan du kan konfigurere scenarier for IoT-viden i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0c063-104">This topic explains how to configure scenarios for IoT Intelligence in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0c063-105">Inden du kan konfigurere scenarier, skal du [konfigurere Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="0c063-105">Before you can set up the scenarios, you must [set up Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>

<span data-ttu-id="0c063-106">I dette emne skal du konfigurere scenariet **Nedetid for udstyr** for at generere en besked i Supply Chain Management, når en maskine går ned.</span><span class="sxs-lookup"><span data-stu-id="0c063-106">In this topic, you will configure the **Equipment downtime** scenario so that a notification is generated in Supply Chain Management when a machine goes down.</span></span> <span data-ttu-id="0c063-107">I emnet vises også, hvordan du kan konfigurere scenariet **Produktkvalitet**, så der genereres en besked, hvis en attribut for en vare ligger uden for et angivet interval, og hvordan du kan konfigurere scenariet **Produktionsforsinkelser**, så der genereres en besked, hvis produktionshastigheden falder under en tærskelværdi.</span><span class="sxs-lookup"><span data-stu-id="0c063-107">The topic also shows how to configure the **Product quality** scenario so that a notification is generated if an attribute of an item is outside a specified range, and how to configure the **Production delays** scenario so that a notification is generated if the production throughput falls below a threshold value.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="0c063-108">Konfigurere scenariet Nedetid for udstyr i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0c063-108">Configure the Equipment downtime scenario in Supply Chain Management</span></span>

<span data-ttu-id="0c063-109">Scenariet **Nedetiden for udstyr** tilknytter et **PartOut**-signal til en maskines beskedgrænse.</span><span class="sxs-lookup"><span data-stu-id="0c063-109">The **Equipment downtime** scenario maps a **PartOut** signal to a machine alert threshold.</span></span> <span data-ttu-id="0c063-110">Maskinen overvåges kun, når den er valgt til scenariet og er angivet til **Kører** i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0c063-110">The machine is monitored only when it's selected for the scenario and when is set to **Running** in Supply Chain Management.</span></span> <span data-ttu-id="0c063-111">Hvis tiden efter, at et **PartOut** sidst blev modtaget fra maskinen, overstiger tærskelværdien for beskeden, udløses beskeden **Maskine nede**.</span><span class="sxs-lookup"><span data-stu-id="0c063-111">If the time since a **PartOut** signal was last received from the machine exceeds the alert threshold, a **Machine down** notification is triggered.</span></span> <span data-ttu-id="0c063-112">Hvis maskinen stadig kører, når det næste **PartOut**-signal modtages, udløses der en besked om **Maskine oppe**.</span><span class="sxs-lookup"><span data-stu-id="0c063-112">If the machine is still running, a **Machine up** notification is triggered when the next **PartOut** signal is received.</span></span> <span data-ttu-id="0c063-113">Hvis en maskine er nede i 30 minutter, udløses en ny besked **Maskine nede**.</span><span class="sxs-lookup"><span data-stu-id="0c063-113">If a machine stays down for 30 minutes, a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="0c063-114">Scenariet **Nedetid for udstyr** har følgende afhængigheder:</span><span class="sxs-lookup"><span data-stu-id="0c063-114">The **Equipment downtime** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="0c063-115">En besked kan kun udløses, hvis en produktionsordrer kører på en tilknyttet maskine.</span><span class="sxs-lookup"><span data-stu-id="0c063-115">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="0c063-116">Et signal, der repræsenterer en tilknyttet maskines **PartOut**-signal, skal sendes til IoT Hub sammen med et entydigt egenskabsnavn.</span><span class="sxs-lookup"><span data-stu-id="0c063-116">A signal that represents a mapped machine's **PartOut** signal must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="0c063-117">En UNIX-egenskab for **tidsstempel**, hvor værdien angives i millisekunder (ms), skal være til stede i Azure IoT Hub-meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="0c063-117">A UNIX **timestamp** property, where the value is expressed in milliseconds (ms), must be present in the Azure IoT Hub message.</span></span>

<span data-ttu-id="0c063-118">Hvis du vil konfigurere scenariet, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="0c063-118">To configure the scenario, follow these steps.</span></span>

1. <span data-ttu-id="0c063-119">Log på Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0c063-119">Sign in to Supply Chain Management.</span></span>
2. <span data-ttu-id="0c063-120">Aktivér IoT-viden-funktionsflaget.</span><span class="sxs-lookup"><span data-stu-id="0c063-120">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="0c063-121">Få flere oplysninger i [Oversigt over funktionsstyring](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="0c063-121">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
3. <span data-ttu-id="0c063-122">Konfigurer de metriske værdier.</span><span class="sxs-lookup"><span data-stu-id="0c063-122">Configure the metrics.</span></span> <span data-ttu-id="0c063-123">Få flere oplysninger i [Sådan konfigurer du metriske værdier](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="0c063-123">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="0c063-124">Gå til **Produktionsstyring \> Konfiguration \> IoT-viden \> Scenariestyring**.</span><span class="sxs-lookup"><span data-stu-id="0c063-124">Go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="0c063-125">I feltet **Udstyrs nedetid** skal du vælge **Konfigurer** for at åbne konfigurationsguiden.</span><span class="sxs-lookup"><span data-stu-id="0c063-125">On the **Equipment downtime** tile, select **Configure** to open the configuration wizard.</span></span>

   <span data-ttu-id="0c063-126">Guiden starter med siden **Skemadefinition for udstyrssensor**.</span><span class="sxs-lookup"><span data-stu-id="0c063-126">The first page in the wizard is the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="0c063-127">På denne side er dit mål at konfigurere skemaet i Supply Chain Management, så det svarer til formatet JavaScript Object Notation (JSON) i IoT Hub-meddelelser.</span><span class="sxs-lookup"><span data-stu-id="0c063-127">On this page, your goal is to set up the schema in Supply Chain Management so that it matches the JavaScript Object Notation (JSON) format of the IoT Hub messages.</span></span> <span data-ttu-id="0c063-128">Der kan defineres flere meddelelsesskemaer.</span><span class="sxs-lookup"><span data-stu-id="0c063-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="0c063-129">Få flere oplysninger i [Meddelelsesskemaformater for IoT Hub](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="0c063-129">For more information, see [Schema formats for IoT Hub messages](iot-schema-format.md).</span></span> <span data-ttu-id="0c063-130">I dette eksempel indeholder meddelelsens nyttedata en batch af meddelelser med følgende format.</span><span class="sxs-lookup"><span data-stu-id="0c063-130">In this example, the message payload contains a batch of messages that has the following format.</span></span>

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. <span data-ttu-id="0c063-131">Føj en række til tabellen, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="0c063-131">Add a row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="0c063-132">Angiv feltet **Skemanavn** til **Id**.</span><span class="sxs-lookup"><span data-stu-id="0c063-132">Set the **Schema name** field to **ID**.</span></span>
    2. <span data-ttu-id="0c063-133">Angiv feltet **Skemasti** til **/nyttedata\[\*\]/id**.</span><span class="sxs-lookup"><span data-stu-id="0c063-133">Set the **Schema path** field to **/payload\[\*\]/id**.</span></span>
    3. <span data-ttu-id="0c063-134">Angiv feltet **Beskrivelse** til **Meddelelses-id**.</span><span class="sxs-lookup"><span data-stu-id="0c063-134">Set the **Description** field to **Message ID**.</span></span>

8. <span data-ttu-id="0c063-135">Føj endnu en række til tabellen, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="0c063-135">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="0c063-136">Angiv feltet **Skemanavn** til **Tidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="0c063-136">Set the **Schema name** field to **Timestamp**.</span></span>
    2. <span data-ttu-id="0c063-137">Angiv feltet **Skemasti** til **/nyttedata\[\*\]/tidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="0c063-137">Set the **Schema path** field to **/payload\[\*\]/timestamp**.</span></span>
    3. <span data-ttu-id="0c063-138">Angiv feltet **Beskrivelse** til **Meddelelsestidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="0c063-138">Set the **Description** field to **Message timestamp**.</span></span>

9. <span data-ttu-id="0c063-139">Føj endnu en række til tabellen, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="0c063-139">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="0c063-140">Angiv feltet **Skemanavn** til **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="0c063-140">Set the **Schema name** field to **Value**.</span></span>
    2. <span data-ttu-id="0c063-141">Angiv feltet **Skemasti** til **/nyttedata\[\*\]/værdi**.</span><span class="sxs-lookup"><span data-stu-id="0c063-141">Set the **Schema path** field to **/payload\[\*\]/value**.</span></span>
    3. <span data-ttu-id="0c063-142">Angiv feltet **Beskrivelse** til **Meddelelsesværdi**.</span><span class="sxs-lookup"><span data-stu-id="0c063-142">Set the **Description** field to **Message value**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0c063-143">Du behøver ikke at definere alle egenskaberne i meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="0c063-143">You don't have to define all the properties in the message.</span></span> <span data-ttu-id="0c063-144">Definer kun de egenskaber, du skal bruge.</span><span class="sxs-lookup"><span data-stu-id="0c063-144">Define only the properties that you require.</span></span> <span data-ttu-id="0c063-145">I de foregående trin har du ikke oprettet en række til **Rodtidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="0c063-145">In the preceding steps, you didn't create a row for **Root timestamp**.</span></span> <span data-ttu-id="0c063-146">Stien til et **Rodtidsstempel** skulle være **/tidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="0c063-146">The path of **Root timestamp** would be **/timestamp**.</span></span>

10. <span data-ttu-id="0c063-147">Vælg **Næste** for at gå til siden **Skematilknytning for udstyrssensor**.</span><span class="sxs-lookup"><span data-stu-id="0c063-147">Select **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="0c063-148">I rækken for **Udstyrsressource-id** skal du angive feltet **Skemanavn** til **Id**.</span><span class="sxs-lookup"><span data-stu-id="0c063-148">In the row for **Equipment resource ID**, in the **Schema name** field, select **ID**.</span></span>
12. <span data-ttu-id="0c063-149">I rækken for **UTC-tid** skal du angive feltet **Skemanavn** til **Tidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="0c063-149">In the row for **UTC time**, in the **Schema name** field, select **Timestamp**.</span></span>
13. <span data-ttu-id="0c063-150">I rækken for **Delproduceret signal** skal du angive feltet **Skemanavn** til **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="0c063-150">In the row for **Part produced signal**, in the **Schema name** field, select **Value**.</span></span>
14. <span data-ttu-id="0c063-151">Vælg **Næste** for at gå til siden **Konfiguration af udstyrsressource-id**.</span><span class="sxs-lookup"><span data-stu-id="0c063-151">Select **Next** to go to the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="0c063-152">Følg disse trin for at knytte meddelelsesværdierne i IoT Hub til Supply Chain Management-ressourcerne:</span><span class="sxs-lookup"><span data-stu-id="0c063-152">Follow these steps to map the values in the IoT Hub message to the Supply Chain Management resources:</span></span>

    1. <span data-ttu-id="0c063-153">Tilføj en ny række i tabellen **Signaldataværdier**.</span><span class="sxs-lookup"><span data-stu-id="0c063-153">In the **Signal Data Values** table, add a new row.</span></span> <span data-ttu-id="0c063-154">I feltet **Værdi** skal du angive **IoTInt.Machine1225.PartOut**.</span><span class="sxs-lookup"><span data-stu-id="0c063-154">In the **Value** field, enter **IoTInt.Machine1225.PartOut**.</span></span> <span data-ttu-id="0c063-155">Værdien kommer fra JSON-egenskaben **id** i IoT Hub-meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="0c063-155">This value  comes from the JSON **id** property in the IoT Hub message.</span></span>
    2. <span data-ttu-id="0c063-156">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0c063-156">Select **Save**.</span></span>
    3. <span data-ttu-id="0c063-157">Vælg **Ny** i tabellen **Forretningsposttilknytning**.</span><span class="sxs-lookup"><span data-stu-id="0c063-157">In the **Business Record Mapping** table, select **New**.</span></span> <span data-ttu-id="0c063-158">Standardværdien for feltet **Forretningsposttype** udfyldes automatisk, og du behøver ikke at ændre den.</span><span class="sxs-lookup"><span data-stu-id="0c063-158">A default value for the **Business record type** field is automatically filled in, and you don't have to change it.</span></span>
    4. <span data-ttu-id="0c063-159">I feltet **Forretningspost** skal du vælge den Supple Chain Management-maskinressource, som denne signaværdi er blevet sendt fra.</span><span class="sxs-lookup"><span data-stu-id="0c063-159">In the **Business record** field, select the Supply Chain Management machine resource that the signal value is being sent from.</span></span>
    5. <span data-ttu-id="0c063-160">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0c063-160">Select **Save**.</span></span>
    6. <span data-ttu-id="0c063-161">Gentag disse trin for at tilføje en ny forretningsposttilknytning for **Machine1226**.</span><span class="sxs-lookup"><span data-stu-id="0c063-161">Repeat these steps to add a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="0c063-162">Du kan knytte flere signaldataværdier til en enkelt post i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0c063-162">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="0c063-163">Brug kolonnen **Valgt** til at vælge, hvilke maskiner du vil behandle.</span><span class="sxs-lookup"><span data-stu-id="0c063-163">Use the **Selected** column to select the machines that you want to process.</span></span> <span data-ttu-id="0c063-164">Du behøver ikke at definere alle signalværdier, og du behøver ikke at vælge alle maskiner.</span><span class="sxs-lookup"><span data-stu-id="0c063-164">You don't have to define all signal values, and you don't have to select all machines.</span></span>
17. <span data-ttu-id="0c063-165">Vælg **Næste** for at gå til siden **Konfiguration af delproduceret signal**.</span><span class="sxs-lookup"><span data-stu-id="0c063-165">Select **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="0c063-166">I tabellen **Signaldataværdier** skal du tilføje en række og indstille feltet **Værdi** til **Sand**.</span><span class="sxs-lookup"><span data-stu-id="0c063-166">In the **Signal Data Values** table, add a row, and set the **Value** field to **True**.</span></span> <span data-ttu-id="0c063-167">Værdien kommer fra JSON-egenskaben **værdi** i IoT Hub-meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="0c063-167">This value comes from the JSON **value** property in the IoT Hub message.</span></span> <span data-ttu-id="0c063-168">Du kan tilføje lige så mange værdier, du har brug for til dit scenarie.</span><span class="sxs-lookup"><span data-stu-id="0c063-168">You can add as many values as you require for your scenario.</span></span>
19. <span data-ttu-id="0c063-169">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0c063-169">Select **Save**.</span></span>
20. <span data-ttu-id="0c063-170">Vælg **Næste** for at gå til siden **Tærskel for nedetid for udstyr**.</span><span class="sxs-lookup"><span data-stu-id="0c063-170">Select **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="0c063-171">De angivne maskiner her er dem, der tidligere er knyttet til signalværdier.</span><span class="sxs-lookup"><span data-stu-id="0c063-171">The machines that are listed are the machines that were previously mapped to signal values.</span></span> <span data-ttu-id="0c063-172">På denne side skal du definere en tærskel for at afgøre, om en maskine er nede.</span><span class="sxs-lookup"><span data-stu-id="0c063-172">On this page, you will define a threshold to determine whether a machine is down.</span></span> <span data-ttu-id="0c063-173">Hvis du f.eks. angiver tærsklen til **10**, genererer Supply Chain Management en besked, hvis der ikke er modtaget et **PartOut**-signal fra en maskine i 10 minutter.</span><span class="sxs-lookup"><span data-stu-id="0c063-173">For example, if you set the threshold to **10**, Supply Chain Management will generate a notification if no **PartOut** signal is received from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="0c063-174">Vælg **Næste** for at gå til siden **Aktivér scenarie**.</span><span class="sxs-lookup"><span data-stu-id="0c063-174">Select **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="0c063-175">Angiv indstillingen for at aktivere scenariet.</span><span class="sxs-lookup"><span data-stu-id="0c063-175">Set the option to enable the scenario.</span></span>
22. <span data-ttu-id="0c063-176">Vælg **Udfør**.</span><span class="sxs-lookup"><span data-stu-id="0c063-176">Select **Finish**.</span></span>

<span data-ttu-id="0c063-177">Konfigurationen af scenariet er nu fuldført.</span><span class="sxs-lookup"><span data-stu-id="0c063-177">The scenario setup is now completed.</span></span> <span data-ttu-id="0c063-178">IoT-viden vil automatisk starte behandlingen af IoT Hub-meddelelserne.</span><span class="sxs-lookup"><span data-stu-id="0c063-178">IoT Intelligence will automatically start to process the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="0c063-179">Konfigurere scenariet Produktkvalitet i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0c063-179">Configure the Product quality scenario in Supply Chain Management</span></span>

<span data-ttu-id="0c063-180">Scenariet **Produktkvalitet** genererer en besked, hvis en attribut for en vare ligger uden for et angivet interval.</span><span class="sxs-lookup"><span data-stu-id="0c063-180">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="0c063-181">En sensor kan f.eks. sende vægten af hver enkelt vare til IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="0c063-181">For example, a sensor sends the weight of each item to IoT Hub.</span></span> <span data-ttu-id="0c063-182">I Supply Chain Management genereres der en besked, hvis varen er for tung eller for let.</span><span class="sxs-lookup"><span data-stu-id="0c063-182">If an item is too heavy or too light, a notification is generated in Supply Chain Management.</span></span>

<span data-ttu-id="0c063-183">Scenariet **Produktkvalitet** har følgende afhængigheder:</span><span class="sxs-lookup"><span data-stu-id="0c063-183">The **Product quality** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="0c063-184">En besked kan kun udløses, hvis en produktionsordre kører på en tilknyttet maskine og fremstiller et produkt med en tilknyttet batchattribut.</span><span class="sxs-lookup"><span data-stu-id="0c063-184">An alert can be triggered only if a production order is running on a mapped machine and producing a product that has a mapped batch attribute.</span></span>
+ <span data-ttu-id="0c063-185">Et signal, der repræsenterer batchattributten, skal sendes til IoT Hub sammen med et entydigt egenskabsnavn.</span><span class="sxs-lookup"><span data-stu-id="0c063-185">A signal that represents the batch attribute must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="0c063-186">En UNIX-egenskab for **tidsstempel**, hvor værdien angives i millisekunder (ms), skal være til stede i Azure IoT Hub-meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="0c063-186">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="0c063-187">Konfigurere scenariet Produktionsforsinkelser i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0c063-187">Configure the Production delays scenario in Supply Chain Management</span></span>

<span data-ttu-id="0c063-188">Scenariet **Produktionsforsinkelser** genererer en besked, hvis produktions gennemløb falder under en tærskelværdi.</span><span class="sxs-lookup"><span data-stu-id="0c063-188">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="0c063-189">I dette scenarie sendes et **PartOut**-signal til IoT Hub for hver fremstillet vare.</span><span class="sxs-lookup"><span data-stu-id="0c063-189">In this scenario, a **PartOut** signal is sent to IoT Hub for each item that is produced.</span></span> <span data-ttu-id="0c063-190">I Supply Chain Management beregnes ordreforsinkelsen på basis af den mængde tid, som produktionsordren er planlagt til at køre, det antal varer, der skal produceres, den tid, jobbet har kørt, og antallet af **PartOut**-signaler, der er modtaget.</span><span class="sxs-lookup"><span data-stu-id="0c063-190">In Supply Chain Management, the order delay is calculated based on the amount of time that the production order is scheduled to run, the number of items that should be produced, the amount of time that the job has been running, and the number of **PartOut** signals that are received.</span></span> <span data-ttu-id="0c063-191">Der genereres en forsinkelsesbesked, hvis antallet af **PartOut**-signaler for jobbet falder under tærskelværdien.</span><span class="sxs-lookup"><span data-stu-id="0c063-191">A delay notification is generated if the number of **PartOut** signals for the job falls below the threshold value.</span></span>

<span data-ttu-id="0c063-192">Scenariet **Produktionsforsinkelser** har følgende afhængigheder:</span><span class="sxs-lookup"><span data-stu-id="0c063-192">The **Production delays** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="0c063-193">En besked kan kun udløses, hvis en produktionsordrer kører på en tilknyttet maskine.</span><span class="sxs-lookup"><span data-stu-id="0c063-193">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="0c063-194">Et signal, der repræsenterer en tilknyttet maskines **PartOut**-signal, skal sendes til Azure IoT Hub sammen med et entydigt egenskabsnavn.</span><span class="sxs-lookup"><span data-stu-id="0c063-194">A signal that represents a mapped machine's **PartOut** signal must be sent to the Azure IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="0c063-195">En UNIX-egenskab for **tidsstempel**, hvor værdien angives i millisekunder (ms), skal være til stede i Azure IoT Hub-meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="0c063-195">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="disable-a-scenario"></a><span data-ttu-id="0c063-196">Deaktivere et scenarie</span><span class="sxs-lookup"><span data-stu-id="0c063-196">Disable a scenario</span></span>

<span data-ttu-id="0c063-197">Følg disse trin for at deaktivere et scenarie.</span><span class="sxs-lookup"><span data-stu-id="0c063-197">To disable a scenario, follow these steps.</span></span>

1. <span data-ttu-id="0c063-198">I Supply Chain Management skal du gå til **Produktionsstyring \> Konfiguration \> IoT-viden \> Scenariestyring**.</span><span class="sxs-lookup"><span data-stu-id="0c063-198">In Supply Chain Management, go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="0c063-199">I feltet til scenariet skal du vælge **Konfigurer**.</span><span class="sxs-lookup"><span data-stu-id="0c063-199">On the tile for the scenario, select **Configure**.</span></span>
3. <span data-ttu-id="0c063-200">Vælg **Næste** for at gå til den sidste side i guiden.</span><span class="sxs-lookup"><span data-stu-id="0c063-200">Select **Next** to go to the last wizard page.</span></span>
4. <span data-ttu-id="0c063-201">Angiv indstillingen for at deaktivere scenariet.</span><span class="sxs-lookup"><span data-stu-id="0c063-201">Set the option to disable the scenario.</span></span>
