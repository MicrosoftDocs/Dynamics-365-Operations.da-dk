---
title: Scenarieopsætning for IoT-viden
description: Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere et scenarie i Supply Chain Management for IoT-viden.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5633741fcd9c04b68e5b174447d7ead3c521ccd7
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597162"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="33540-103">Scenarieopsætning for IoT-viden</span><span class="sxs-lookup"><span data-stu-id="33540-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="33540-104">Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere et scenarie i Supply Chain Management for IoT-viden.</span><span class="sxs-lookup"><span data-stu-id="33540-104">This topic describes how to configure a scenario in Supply Chain Management for IoT Intelligence.</span></span> <span data-ttu-id="33540-105">Før du kan konfigurere scenarierne, skal du [konfigurere LCS](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="33540-105">Before you can setup the scenarios, you must [setup LCS](iot-lcs-setup.md).</span></span>

<span data-ttu-id="33540-106">I dette emne skal du konfigurere scenariet **Nedetid for udstyr** for at generere en besked i Supply Chain Management, når en maskine går ned.</span><span class="sxs-lookup"><span data-stu-id="33540-106">In this topic, you will configure the **Equipment downtime** scenario to generate a notification in Supply Chain Management when a machine goes down.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="33540-107">Konfigurere scenariet **Nedetid for udstyr** i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="33540-107">Configure the **Equipment downtime** scenario in Supply Chain Management</span></span>

<span data-ttu-id="33540-108">Scenariet **Nedetiden for udstyr** tilknytter et del ude-signal til en maskines beskedgrænse.</span><span class="sxs-lookup"><span data-stu-id="33540-108">The **Equipment downtime** scenario maps a part out signal to a machine alert threshold.</span></span> <span data-ttu-id="33540-109">Maskinen overvåges kun, når maskinen er valgt til scenariet og er angivet til at køre i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="33540-109">The machine is monitored only when the machine is selected for the scenario and is set to running in Supply Chain Management.</span></span> <span data-ttu-id="33540-110">Hvis tiden efter, at maskinens sidste modtagne del ude-signal er større end tærskelværdien for beskeden, udløses beskeden **Maskine nede**.</span><span class="sxs-lookup"><span data-stu-id="33540-110">If the time since the machine’s last received Part Out signal is greater than the alert threshold, then a **Machine down** notification is triggered.</span></span> <span data-ttu-id="33540-111">Hvis maskinen stadig kører, når det næste **Del ud**-signal modtages, udløses der en besked **Maskine oppe**.</span><span class="sxs-lookup"><span data-stu-id="33540-111">If the machine is still running, when the next **PartOut** signal is received a **Machine up** notification is triggered.</span></span> <span data-ttu-id="33540-112">Hvis en maskine er nede i 30 minutter, udløses en ny besked **Maskine nede**.</span><span class="sxs-lookup"><span data-stu-id="33540-112">If a machine stays down for 30 mins a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="33540-113">Scenariet for **nedetid for udstyr** har følgende afhængigheder:</span><span class="sxs-lookup"><span data-stu-id="33540-113">The **Equipment downtime** scenario has these dependencies:</span></span>

+ <span data-ttu-id="33540-114">En produktionsordre skal køre på en tilknyttet maskine, før der kan udløses en påmindelse.</span><span class="sxs-lookup"><span data-stu-id="33540-114">A production order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="33540-115">Et signal, der repræsenterer en tilknyttet maskines del ud-signal, skal sendes til IoT Hub med et entydigt egenskabsnavn.</span><span class="sxs-lookup"><span data-stu-id="33540-115">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="33540-116">Der skal være en tidsstempelegenskab i millisekunder for UNIX i IoT-meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="33540-116">A Unix milliseconds timestamp property must be present in the IoT hub message.</span></span>

<span data-ttu-id="33540-117">Hvis du vil konfigurere scenariet, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="33540-117">To configure the scenario, follow these steps:</span></span>

1. <span data-ttu-id="33540-118">Log på Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="33540-118">Log into Supply Chain Management.</span></span>
2. <span data-ttu-id="33540-119">Aktivér IoT-viden-funktionsflaget.</span><span class="sxs-lookup"><span data-stu-id="33540-119">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="33540-120">Få flere oplysninger i [Oversigt over funktionsstyring](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="33540-120">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
3. <span data-ttu-id="33540-121">Konfigurer de metriske værdier.</span><span class="sxs-lookup"><span data-stu-id="33540-121">Configure the metrics.</span></span> <span data-ttu-id="33540-122">Få flere oplysninger i [Sådan konfigurer du metriske værdier](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="33540-122">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="33540-123">Gå til **Produktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="33540-123">Navigate to **Production control**.</span></span>
5. <span data-ttu-id="33540-124">Gå til **Konfiguration \> IoT-viden \> Scenariestyring**.</span><span class="sxs-lookup"><span data-stu-id="33540-124">Navigate to **Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="33540-125">Klik på **Opsætning** i feltet **Nedetid for udstyr**.</span><span class="sxs-lookup"><span data-stu-id="33540-125">Click **Configure** on the **Equipment downtime** tile.</span></span> <span data-ttu-id="33540-126">Konfigurationsguiden starter med siden **Skemadefinition for udstyrssensor**.</span><span class="sxs-lookup"><span data-stu-id="33540-126">The configuration wizard starts with the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="33540-127">Målet er at angive, at skemaet i Supply Chain Management skal svare til JSON-formatet i IoT-meddelelserne.</span><span class="sxs-lookup"><span data-stu-id="33540-127">The goal here is to setup the schema in Supply Chain Management to match the JSON format of the IoT messages.</span></span> <span data-ttu-id="33540-128">Der kan defineres flere meddelelsesskemaer.</span><span class="sxs-lookup"><span data-stu-id="33540-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="33540-129">Få flere oplysninger i [Formater for meddelelsesskemaer for IoT Hub](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="33540-129">For more information, see [Message schema formats for IoT Hub](iot-schema-format.md).</span></span> <span data-ttu-id="33540-130">I dette eksempel indeholder meddelelsesdataene en batch af meddelelser med dette format:</span><span class="sxs-lookup"><span data-stu-id="33540-130">In this example, the message payload contains a batch of messages with this format:</span></span>

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

7. <span data-ttu-id="33540-131">Føj en række til tabellen.</span><span class="sxs-lookup"><span data-stu-id="33540-131">Add a row to the table.</span></span>

    1. <span data-ttu-id="33540-132">Angiv **Skemanavn** til **Id**.</span><span class="sxs-lookup"><span data-stu-id="33540-132">Set the **Schema name** to **ID**.</span></span>
    2. <span data-ttu-id="33540-133">Angiv **Skemasti** til **/payload[\*]/id**.</span><span class="sxs-lookup"><span data-stu-id="33540-133">Set the **Schema path** to **/payload[\*]/id**.</span></span>
    3. <span data-ttu-id="33540-134">Angiv **Beskrivelse** til **Meddelelses-id**.</span><span class="sxs-lookup"><span data-stu-id="33540-134">Set the **Description** to **Message ID**.</span></span>

8. <span data-ttu-id="33540-135">Føj en række til tabellen.</span><span class="sxs-lookup"><span data-stu-id="33540-135">Add a row to the table.</span></span>

    1. <span data-ttu-id="33540-136">Angiv **Skemanavn** til **Tidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="33540-136">Set the **Schema name** to **Timestamp**.</span></span>
    2. <span data-ttu-id="33540-137">Angiv **Skemasti** til **/payload[\*]/tidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="33540-137">Set the **Schema path** to **/payload[\*]/timestamp**.</span></span>
    3. <span data-ttu-id="33540-138">Angiv **Beskrivelse** til **Meddelelsestidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="33540-138">Set the **Description** to **Message timestamp**.</span></span>

9. <span data-ttu-id="33540-139">Føj en række til tabellen.</span><span class="sxs-lookup"><span data-stu-id="33540-139">Add a row to the table.</span></span>

    1. <span data-ttu-id="33540-140">Angiv **Skemanavn** til **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="33540-140">Set the **Schema name** to **Value**.</span></span>
    2. <span data-ttu-id="33540-141">Angiv **Skemasti** til **/payload[\*]/værdi**.</span><span class="sxs-lookup"><span data-stu-id="33540-141">Set the **Schema path** to **/payload[\*]/value**.</span></span>
    3. <span data-ttu-id="33540-142">Angiv **Beskrivelse** til **Meddelelsesværdi**.</span><span class="sxs-lookup"><span data-stu-id="33540-142">Set the **Description** to **Message value**.</span></span>

    <span data-ttu-id="33540-143">Du behøver ikke at definere alle egenskaberne i meddelelsen, kun dem, du skal bruge.</span><span class="sxs-lookup"><span data-stu-id="33540-143">You don't need to define all the properties in the message, only the ones that you need.</span></span> <span data-ttu-id="33540-144">I dette eksempel oprettede du ikke en række for **Rodtidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="33540-144">In this example, you did not create a row for **Root timestamp**.</span></span> <span data-ttu-id="33540-145">Stien for et **Rodtidsstempel** ville være **/Tidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="33540-145">The path for **Root timestamp** would be **/timestamp**.</span></span>
  
10. <span data-ttu-id="33540-146">Klik på **Næste** for at gå til siden **Skematilknytning for udstyrssensor**.</span><span class="sxs-lookup"><span data-stu-id="33540-146">Click **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="33540-147">I rækken for **Udstyrsressource-id** skal du angive **Skemanavn** til **Id**.</span><span class="sxs-lookup"><span data-stu-id="33540-147">In the row for **Equipment resource ID** set the **Schema name** to **ID**.</span></span> <span data-ttu-id="33540-148">De gyldige værdier vises i en rulleliste.</span><span class="sxs-lookup"><span data-stu-id="33540-148">The valid values are displayed in a dropdown table.</span></span>
12. <span data-ttu-id="33540-149">I rækken for **UTC-tid** skal du angive **Skemanavn** til **Tidsstempel**.</span><span class="sxs-lookup"><span data-stu-id="33540-149">In the row for **UTC time** set the **Schema name** to **Timestamp**.</span></span> <span data-ttu-id="33540-150">De gyldige værdier vises i en rulleliste.</span><span class="sxs-lookup"><span data-stu-id="33540-150">The valid values are displayed in a dropdown table.</span></span>
13. <span data-ttu-id="33540-151">I rækken for **Delproduceret signal** skal du angive **Skemanavn** til **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="33540-151">In the row for **Part produced signal** set the **Schema name** to **Value**.</span></span> <span data-ttu-id="33540-152">De gyldige værdier vises i en rulleliste.</span><span class="sxs-lookup"><span data-stu-id="33540-152">The valid values are displayed in a dropdown table.</span></span>
14. <span data-ttu-id="33540-153">Klik på **Næste** for siden **Konfiguration af udstyrsressource-id**.</span><span class="sxs-lookup"><span data-stu-id="33540-153">Click **Next** for the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="33540-154">I dette trin knytter du IoT-meddelelsesværdierne til de Supply Chain Management-ressourcerne.</span><span class="sxs-lookup"><span data-stu-id="33540-154">In this step, you map the IoT Hub message values to the Supply Chain Management resources.</span></span>

    1. <span data-ttu-id="33540-155">I tabellen **Signaldataværdier** skal du tilføje en ny række og angive **IoTInt.Machine1225.PartOut** i kolonnen **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="33540-155">In the **Signal Data Values** table, add a new row, and enter **IoTInt.Machine1225.PartOut** in the **Value** column.</span></span> <span data-ttu-id="33540-156">Værdien **IoTInt. Machine1225. PartOut** kommer fra egenskaben JSON-**id** i IOT hub-meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="33540-156">The value **IoTInt.Machine1225.PartOut** comes from the JSON **id** property in the IoT hub message.</span></span>
    2. <span data-ttu-id="33540-157">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="33540-157">Click **Save**.</span></span>
    3. <span data-ttu-id="33540-158">Klik på **Ny** i tabellen **Forretningsposttilknytning**.</span><span class="sxs-lookup"><span data-stu-id="33540-158">In the **Business Record Mapping** table, click **New**.</span></span> <span data-ttu-id="33540-159">Standardværdien for **Forretningsposttypen** udfyldes automatisk, og du behøver ikke at ændre den.</span><span class="sxs-lookup"><span data-stu-id="33540-159">The default value for the **Business record type** is autopopulated, and you don't need to change it.</span></span>
    4. <span data-ttu-id="33540-160">I kolonnen **Forretningspost** skal du vælge den Supple Chain Management-maskinressource, denne signaværdi er blevet sendt fra.</span><span class="sxs-lookup"><span data-stu-id="33540-160">In the **Business record** column, select the Supple Chain Management machine resource this signal value is being sent from.</span></span>
    5. <span data-ttu-id="33540-161">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="33540-161">Click **Save**.</span></span>
    6. <span data-ttu-id="33540-162">Gentag disse trin, og tilføj en ny forretningsposttilknytning for **Maskin1226**.</span><span class="sxs-lookup"><span data-stu-id="33540-162">Repeat these steps, adding a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="33540-163">Du kan knytte flere signaldataværdier til en enkelt post i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="33540-163">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="33540-164">Brug kolonnen **Valgt** til at vælge, hvilke maskiner du vil behandle.</span><span class="sxs-lookup"><span data-stu-id="33540-164">Use the **Selected** column to choose which machines you want to process.</span></span> <span data-ttu-id="33540-165">Du behøver ikke at definere alle signalværdier, og du behøver ikke at vælge alle maskiner.</span><span class="sxs-lookup"><span data-stu-id="33540-165">You do not have to define all signal values and you do not have to select all machines.</span></span>
17. <span data-ttu-id="33540-166">Klik på **Næste** for at gå til siden **Konfiguration af delproduceret signal**.</span><span class="sxs-lookup"><span data-stu-id="33540-166">Click **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="33540-167">I tabellen **Signaldataværdier** skal du tilføje en række og indstille **Værdi** til **Sand**.</span><span class="sxs-lookup"><span data-stu-id="33540-167">In the **Signal Data Values** table, add a row, and set **Value** to **True**.</span></span> <span data-ttu-id="33540-168">Værdien **Sand** kommer fra egenskaben JSON-**værdi** i IoT Hub-meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="33540-168">The value **True** comes from the JSON **value** property in the IoT hub message.</span></span> <span data-ttu-id="33540-169">Du kan tilføje lige så mange værdier, du har brug for til dit scenarie.</span><span class="sxs-lookup"><span data-stu-id="33540-169">You can add as many values as you need for your scenario.</span></span>
19. <span data-ttu-id="33540-170">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="33540-170">Click **Save**.</span></span>
20. <span data-ttu-id="33540-171">Klik på **Næste** for at gå til siden **Tærskel for nedetid for udstyr**.</span><span class="sxs-lookup"><span data-stu-id="33540-171">Click **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="33540-172">De angivne maskiner er de maskiner, der tidligere er knyttet til signalværdier.</span><span class="sxs-lookup"><span data-stu-id="33540-172">The machines listed are the machines previously mapped to signal values.</span></span> <span data-ttu-id="33540-173">I dette trin skal du definere en tærskel for at afgøre, om en maskine er nede.</span><span class="sxs-lookup"><span data-stu-id="33540-173">In this step, you define a threshold to determine if a machine is down.</span></span> <span data-ttu-id="33540-174">Hvis du f.eks. angiver tærsklen til 10, genererer Supply Chain Management en besked, hvis der ikke er en del ud-meddelelse fra en maskine i 10 minutter.</span><span class="sxs-lookup"><span data-stu-id="33540-174">For example, if you set the threshold to 10, Supply Chain Management generates a notification if there is no part out message from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="33540-175">Klik på **Næste** for at gå til siden **Aktivér scenarie**.</span><span class="sxs-lookup"><span data-stu-id="33540-175">Click **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="33540-176">Slå skyderen til og fra for at aktivere scenariet.</span><span class="sxs-lookup"><span data-stu-id="33540-176">Toggle the slider to enable the scenario.</span></span>
22. <span data-ttu-id="33540-177">Klik på **Udfør**.</span><span class="sxs-lookup"><span data-stu-id="33540-177">Click **Finish**.</span></span>

<span data-ttu-id="33540-178">Konfigurationen af scenariet er fuldført.</span><span class="sxs-lookup"><span data-stu-id="33540-178">The scenario setup is complete.</span></span> <span data-ttu-id="33540-179">IoT-viden vil automatisk starte behandlingen af IoT hub-meddelelserne.</span><span class="sxs-lookup"><span data-stu-id="33540-179">IoT Intelligence will automatically start processing the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="33540-180">Konfigurere scenariet **Produktkvalitet** i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="33540-180">Configure the **Product quality** scenario in Supply Chain Management</span></span>

<span data-ttu-id="33540-181">Scenariet **Produktkvalitet** genererer en besked, hvis en attribut for en vare ligger uden for et angivet interval.</span><span class="sxs-lookup"><span data-stu-id="33540-181">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="33540-182">En sensor kan f.eks. sende vægten af hver enkelt vare til IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="33540-182">For example, a sensor could send the weight of each item to IoT Hub.</span></span> <span data-ttu-id="33540-183">I Supply Chain Management genereres der en besked, hvis varen er for tung eller for let.</span><span class="sxs-lookup"><span data-stu-id="33540-183">In Supply Chain Management, a notification would be generated if the item was too heavy or too light.</span></span>

<span data-ttu-id="33540-184">Scenariet har følgende afhængigheder:</span><span class="sxs-lookup"><span data-stu-id="33540-184">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="33540-185">En produktionsordre skal køre på en tilknyttet maskine og fremstille et produkt med en tilknyttet batchattribut, for at der kan udløses en påmindelse.</span><span class="sxs-lookup"><span data-stu-id="33540-185">A Production Order must be running on a mapped machine and producing a product with a mapped batch attribute for an alert to be triggered.</span></span>
+ <span data-ttu-id="33540-186">Et signal, der repræsenterer batchattributten skal sendes til IoT Hub med et entydigt egenskabsnavn.</span><span class="sxs-lookup"><span data-stu-id="33540-186">A signal representing the batch attribute must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="33540-187">Der skal være en tidsstempelegenskab i millisekunder for UNIX i IoT Hub-meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="33540-187">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="33540-188">Konfigurere scenariet **Produktionsforsinkelser** i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="33540-188">Configure the **Production delays** scenario in Supply Chain Management</span></span>

<span data-ttu-id="33540-189">Scenariet **Produktionsforsinkelser** genererer en besked, hvis produktions gennemløb falder under en tærskelværdi.</span><span class="sxs-lookup"><span data-stu-id="33540-189">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="33540-190">I dette scenarie sendes et **Del ud**-signal til IoT Hub for hver fremstillet vare.</span><span class="sxs-lookup"><span data-stu-id="33540-190">In this scenario, a **PartOut** signal is sent to IoT Hub for each item produced.</span></span> <span data-ttu-id="33540-191">I Supply Chain Management beregnes ordreforsinkelsen på basis af, hvor længe produktionsordren er planlagt til at køre, hvor mange varer der skal produceres, hvor længe jobbet har kørt, og hvor mange **Del ud**-signaler, der modtages.</span><span class="sxs-lookup"><span data-stu-id="33540-191">In Supply Chain Management, the order delay is calculated based on how long the production order is scheduled to run, how many items should be produced, how long the job has been running, and how many **PartOut** signals are received.</span></span> <span data-ttu-id="33540-192">Der ville blive genereret en forsinkelsesbesked, hvis nummeret på **Del ud**-signalerne for jobbet falder under tærskelværdien for den forventede værdi.</span><span class="sxs-lookup"><span data-stu-id="33540-192">A delay notification would be generated if the number of the **PartOut** signals for the job falls below the threshold value of the expected value.</span></span>

<span data-ttu-id="33540-193">Scenariet har følgende afhængigheder:</span><span class="sxs-lookup"><span data-stu-id="33540-193">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="33540-194">En produktionsordre skal køre på en tilknyttet maskine, før der kan udløses en påmindelse.</span><span class="sxs-lookup"><span data-stu-id="33540-194">A Production Order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="33540-195">Et signal, der repræsenterer en tilknyttet maskines del ud-signal, skal sendes til IoT Hub med et entydigt egenskabsnavn.</span><span class="sxs-lookup"><span data-stu-id="33540-195">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="33540-196">Der skal være en tidsstempelegenskab i millisekunder for UNIX i IoT Hub-meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="33540-196">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="how-to-disable-a-scenario"></a><span data-ttu-id="33540-197">Sådan deaktiveres et scenarie</span><span class="sxs-lookup"><span data-stu-id="33540-197">How to disable a scenario</span></span>

<span data-ttu-id="33540-198">Følg disse trin for at deaktivere et scenarie:</span><span class="sxs-lookup"><span data-stu-id="33540-198">To disable a scenario, follow these steps:</span></span>

1. <span data-ttu-id="33540-199">I Supply Chain Management skal du gå til **Produktionsstyring \> Konfiguration \> IoT-viden \> Scenariestyring**.</span><span class="sxs-lookup"><span data-stu-id="33540-199">In Supply Chain Management, navigate to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="33540-200">Klik på **Opsætning** i scenariet.</span><span class="sxs-lookup"><span data-stu-id="33540-200">Click **Configure** on the scenario.</span></span>
3. <span data-ttu-id="33540-201">Klik på **Næste** for at åbne den sidste fane i guiden.</span><span class="sxs-lookup"><span data-stu-id="33540-201">Click **Next** to get to the last wizard tab.</span></span>
4. <span data-ttu-id="33540-202">Slå skyderen til og fra for at deaktivere scenariet.</span><span class="sxs-lookup"><span data-stu-id="33540-202">Toggle the slider to disable the scenario.</span></span>
