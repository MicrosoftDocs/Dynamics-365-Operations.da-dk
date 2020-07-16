---
title: Overvåge og administrere IoT-viden
description: Dette emne forklarer, hvordan du kan overvåge og administrere IoT-viden.
author: robinarh
manager: AnnBe
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
ms.openlocfilehash: 97a87b78a0178424f00e464262bb7f69e8a5b4a0
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386496"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="0448f-103">Overvåge og administrere IoT-viden</span><span class="sxs-lookup"><span data-stu-id="0448f-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0448f-104">Dette emne forklarer, hvordan du kan overvåge og administrere IoT-viden.</span><span class="sxs-lookup"><span data-stu-id="0448f-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="0448f-105">Overvågningsscenarier i Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0448f-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="0448f-106">Du kan overvåge IoT-viden-behandling fra flere steder:</span><span class="sxs-lookup"><span data-stu-id="0448f-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="0448f-107">**Moduler \> Produktionsstyring \> Forespørgsler og rapporter \> IoT-viden \> Beskeder** – vis listen over uløste beskeder.</span><span class="sxs-lookup"><span data-stu-id="0448f-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="0448f-108">**Moduler \> Produktionsstyring \> Forespørgsler og rapporter \> IoT-viden \> Lukkede beskeder** – vis listen over beskeder, der er blevet løst eller afvist.</span><span class="sxs-lookup"><span data-stu-id="0448f-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="0448f-109">**Moduler \> Produktionsstyring \> Forespørgsler og rapporter \> IoT-viden \> Metriske værdier** – vis de metriske værdier for tidsseriediagrammerne for **Ressourcestatus**.</span><span class="sxs-lookup"><span data-stu-id="0448f-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="0448f-110">**Moduler \> Produktionsstyring \> Produktionsudførelse \> Ressourcestatus** – spor specifikke metriske værdier ved at bruge dialogboksen **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="0448f-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="0448f-111">Hvis et scenarie registrerer en undtagelse, vises der en besked med oplysninger om undtagelsen.</span><span class="sxs-lookup"><span data-stu-id="0448f-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="0448f-112">**Arbejdsområder \> Administration af produktion \> Beskeder** – vis en løste over uløste beskeder.</span><span class="sxs-lookup"><span data-stu-id="0448f-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="0448f-113">Redigere et kørende IoT-viden-scenarie</span><span class="sxs-lookup"><span data-stu-id="0448f-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="0448f-114">Når et scenarie kører, kan du foretage disse ændringer:</span><span class="sxs-lookup"><span data-stu-id="0448f-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="0448f-115">Tilføje nye sensorskemadefinitioner.</span><span class="sxs-lookup"><span data-stu-id="0448f-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="0448f-116">Vælge nye signaldataværdier.</span><span class="sxs-lookup"><span data-stu-id="0448f-116">Select new signal data values.</span></span>
+ <span data-ttu-id="0448f-117">Annullere markeringen af eksisterende signaldataværdier.</span><span class="sxs-lookup"><span data-stu-id="0448f-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="0448f-118">Tilføje og tilknyt nye signaldataværdier.</span><span class="sxs-lookup"><span data-stu-id="0448f-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="0448f-119">Opdatere tærskelværdier.</span><span class="sxs-lookup"><span data-stu-id="0448f-119">Update threshold values.</span></span>

<span data-ttu-id="0448f-120">Når et scenarie kører, er disse ændringer ikke tilladt:</span><span class="sxs-lookup"><span data-stu-id="0448f-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="0448f-121">Slette eller redigere skemadefinitioner, der i øjeblikket forbruges af et aktiveret scenarie.</span><span class="sxs-lookup"><span data-stu-id="0448f-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="0448f-122">Redigere det aktiverede scenaries valgte skemastier.</span><span class="sxs-lookup"><span data-stu-id="0448f-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="0448f-123">Simuleringsindstillinger</span><span class="sxs-lookup"><span data-stu-id="0448f-123">Simulation options</span></span>

<span data-ttu-id="0448f-124">Du kan simulere fabriksmaskinsignaler.</span><span class="sxs-lookup"><span data-stu-id="0448f-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="0448f-125">Du kan finde flere oplysninger i disse emner:</span><span class="sxs-lookup"><span data-stu-id="0448f-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="0448f-126">Forbinde IoT DevKit AZ3166 til Azure IoT Hub</span><span class="sxs-lookup"><span data-stu-id="0448f-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="0448f-127">Forbinde Raspberry Pi-onlinesimulator til Azure IoT Hub (Node.js)</span><span class="sxs-lookup"><span data-stu-id="0448f-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="0448f-128">Oversigt over løsningsaccelerator til enhedsimuleringer</span><span class="sxs-lookup"><span data-stu-id="0448f-128">Device Simulation solution accelerator overview</span></span>](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)