---
title: Oprette vedligeholdelsesanmodninger
description: Dette emne forklarer, hvordan du opretter en vedligeholdelsesanmodning i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 03e090633276cd264ad03f561ddb425a9816357e
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847499"
---
# <a name="create-maintenance-requests"></a><span data-ttu-id="218f4-103">Oprette vedligeholdelsesanmodninger</span><span class="sxs-lookup"><span data-stu-id="218f4-103">Create maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="218f4-104">Vedligeholdelsesanmodninger kan bruges, hvis vedligeholdelsesarbejdere eller produktionsmedarbejdere opdager, at udstyr kræver reparation, men reparationsjobbet ikke kan udføres med det samme.</span><span class="sxs-lookup"><span data-stu-id="218f4-104">Maintenance requests can be used if maintenance workers or production workers discover that equipment requires repair, but the repair job can't be done right away.</span></span>

<span data-ttu-id="218f4-105">**Eksempel:** Mens en vedligeholdelsesarbejder foretager en reparation, opdager hun, at et andet aktiv på samme sted skal serviceres.</span><span class="sxs-lookup"><span data-stu-id="218f4-105">**Example:** While a maintenance worker is making a repair, she discovers that another asset at the same location must be serviced.</span></span> <span data-ttu-id="218f4-106">Vedligeholdelsesarbejderen har dog ikke tid eller de nødvendige reservedele til at udføre reparationsjobbet.</span><span class="sxs-lookup"><span data-stu-id="218f4-106">However, the maintenance worker doesn't have the time or the required spare parts to do the repair job.</span></span> <span data-ttu-id="218f4-107">Derfor opretter hun en vedligeholdelsesanmodning på aktivet og indtaster en kort beskrivelse af problemet.</span><span class="sxs-lookup"><span data-stu-id="218f4-107">Therefore, she creates a maintenance request on the asset and enters a short description of the issue.</span></span>

<span data-ttu-id="218f4-108">Afsnittet **Aktive vedligeholdelsesanmodninger** i ruden **Relaterede oplysninger** i højre side af siden **Alle aktiver** eller **Aktive aktiver** (**Styring af aktiver** \> **Fælles** \> **Aktiver** \> **Alle aktiver** eller **Aktive aktiver**) viser de aktive vedligeholdelsesanmodninger, der er knyttet til det valgte aktiv.</span><span class="sxs-lookup"><span data-stu-id="218f4-108">The **Active maintenance requests** section of the **Related information** pane on the right side of the **All assets** or **Active assets** page (**Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**) shows the active maintenance requests that are attached to the selected asset.</span></span>

1. <span data-ttu-id="218f4-109">Vælg **Styring af aktiver** \> **Almindelig** \> **Vedligeholdelsesanmodninger** \> **Alle vedligeholdelsesanmodninger** eller **Aktive vedligeholdelsesanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="218f4-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="218f4-110">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="218f4-110">Select **New**.</span></span>
3. <span data-ttu-id="218f4-111">Vælg typen af vedligeholdelsesanmodning i feltet **Vedligeholdelsesanmodningstype** i dialogboksen **Opret anmodning**.</span><span class="sxs-lookup"><span data-stu-id="218f4-111">In the **Create request** dialog box, in the **Maintenance request type** field, select the type of maintenance request.</span></span> <span data-ttu-id="218f4-112">Der foreslås en standardtype.</span><span class="sxs-lookup"><span data-stu-id="218f4-112">A default type is suggested.</span></span>
4. <span data-ttu-id="218f4-113">I feltet **Beskrivelse** skal du angive et navn eller en titel, der kort beskriver vedligeholdelsesanmodningen.</span><span class="sxs-lookup"><span data-stu-id="218f4-113">In the **Description** field, enter a name or title that briefly describes the maintenance request.</span></span>
5. <span data-ttu-id="218f4-114">I felterne **Arbejdssted** og **Aktiv** skal du vælge et arbejdssted eller et aktiv eller en kombination af et arbejdssted og et aktiv, som du har brug for.</span><span class="sxs-lookup"><span data-stu-id="218f4-114">In the **Functional location** and **Asset** fields, select a functional location or an asset, or a combination of a functional location and an asset, as you require.</span></span> <span data-ttu-id="218f4-115">Du kan oprette en vedligeholdelsesanmodning uden at vælge et aktiv, og aktivet kan føjes til vedligeholdelsesanmodningen senere.</span><span class="sxs-lookup"><span data-stu-id="218f4-115">You can create a maintenance request without selecting an asset, and the asset can be added to the maintenance request later.</span></span> <span data-ttu-id="218f4-116">Hvis den vedligeholdelsesarbejder, der er logget på Microsoft Dynamics 365 for Finance and Operations, er relateret til en ressource, der er relateret til et aktiv, er feltet **Aktiv** automatisk angivet.</span><span class="sxs-lookup"><span data-stu-id="218f4-116">If the maintenance worker who is signed in to Microsoft Dynamics 365 for Finance and Operations is related to a resource that is related to an asset, the **Asset** field is automatically set.</span></span>

    <span data-ttu-id="218f4-117">Hvis der allerede er knyttet en vedligeholdelsesanmodning til det valgte aktiv, vises der en meddelelseslinje øverst i dialogboksen **Opret anmodning** for at give dig besked om id'et for den eksisterende vedligeholdelsesanmodning.</span><span class="sxs-lookup"><span data-stu-id="218f4-117">If a maintenance request is already attached to the selected asset, a message bar appears at the top of the **Create request** dialog box to notify you about the ID of the existing maintenance request.</span></span> <span data-ttu-id="218f4-118">En meddelelseslinje giver dig også besked, hvis aktivet er dækket af en garantiaftale.</span><span class="sxs-lookup"><span data-stu-id="218f4-118">A message bar also notifies you if the asset is covered by a warranty agreement.</span></span>

6. <span data-ttu-id="218f4-119">I feltet **Serviceniveau** skal du vælge et serviceniveau, der angiver anmodningens prioritetsniveau.</span><span class="sxs-lookup"><span data-stu-id="218f4-119">In the **Service level** field, select a service level that indicates the urgency of the request.</span></span>
7. <span data-ttu-id="218f4-120">Hvis du har valgt et aktiv i trin 5, kan du bruge felterne **Fejlsymptom**, **Fejlområde** og **Fejltype** til at oprette en fejlregistrering.</span><span class="sxs-lookup"><span data-stu-id="218f4-120">If you selected an asset in step 5, you can use the **Fault symptom**, **Fault area**, and **Fault type** fields to create a fault registration.</span></span>
8. <span data-ttu-id="218f4-121">Hvis vedligeholdelsesanmodningen har medført vedligeholdelsesnedetid, skal du angive startdato og -tidspunkt for nedetiden.</span><span class="sxs-lookup"><span data-stu-id="218f4-121">If the maintenance request has caused maintenance downtime, enter the start date and time of the downtime.</span></span>

    <span data-ttu-id="218f4-122">Feltet **Startet af** indstilles automatisk til dit navn.</span><span class="sxs-lookup"><span data-stu-id="218f4-122">The **Started by** field is automatically set to your name.</span></span>

10. <span data-ttu-id="218f4-123">Feltet **Faktisk start** angives automatisk til den aktuelle dato og tid.</span><span class="sxs-lookup"><span data-stu-id="218f4-123">The **Actual start** field is automatically set to the current date and time.</span></span> <span data-ttu-id="218f4-124">Du kan dog ændre værdien efter behov.</span><span class="sxs-lookup"><span data-stu-id="218f4-124">However, you can change the value as you require.</span></span>
11. <span data-ttu-id="218f4-125">Udfyld eventuelt feltet **Noter** med yderligere bemærkninger.</span><span class="sxs-lookup"><span data-stu-id="218f4-125">In the **Notes** field, enter any additional notes that are required.</span></span>
12. <span data-ttu-id="218f4-126">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="218f4-126">Select **OK**.</span></span>

![Figur 1](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a><span data-ttu-id="218f4-128">Efterfølgende behandling af vedligeholdelsesanmodninger</span><span class="sxs-lookup"><span data-stu-id="218f4-128">Subsequent processing of maintenance requests</span></span>

<span data-ttu-id="218f4-129">Når der er oprettet en vedligeholdelsesanmodning, men før den konverteres til en arbejdsordre, skal der opdateres forskellige oplysninger på den.</span><span class="sxs-lookup"><span data-stu-id="218f4-129">After a maintenance request is created, but before it's converted to a work order, various information should be updated on it.</span></span> <span data-ttu-id="218f4-130">En planlægger eller en anden administrativ medarbejder fuldfører typisk denne opgave.</span><span class="sxs-lookup"><span data-stu-id="218f4-130">Typically, a planner or another administrative employee completes this task.</span></span>

- <span data-ttu-id="218f4-131">På siden **Alle vedligeholdelsesanmodninger** eller **Aktive vedligeholdelsesanmodninger** skal du vælge den anmodning, du vil arbejde med, og derefter vælge **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="218f4-131">On the **All maintenance requests** or **Active maintenance requests** page, select the request to work with, and then select **Edit**.</span></span>

<span data-ttu-id="218f4-132">I detaljevisningen kan du opdatere forskellige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="218f4-132">In the details view, you can update various information.</span></span> <span data-ttu-id="218f4-133">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="218f4-133">Here are some examples:</span></span>

- <span data-ttu-id="218f4-134">Vælg og bekræft aktivet.</span><span class="sxs-lookup"><span data-stu-id="218f4-134">Select and verify the asset.</span></span> <span data-ttu-id="218f4-135">Hvis du senere skal vælge et andet aktiv, kan du angive indstillingen **Aktiv verificeret** til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="218f4-135">If you must select a different asset later, you can set the **Asset verified** option to **No**.</span></span>
- <span data-ttu-id="218f4-136">Vælg en ansvarlig vedligeholdelsesarbejdergruppe og/eller en ansvarlig vedligeholdelsesarbejder.</span><span class="sxs-lookup"><span data-stu-id="218f4-136">Select a responsible maintenance worker group and/or a responsible maintenance worker.</span></span> <span data-ttu-id="218f4-137">Du finder flere oplysninger om den påkrævede opsætning under [Ansvarlige vedligeholdelsesarbejdere](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="218f4-137">For more information about the required setup, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>
- <span data-ttu-id="218f4-138">Vælg en vedligeholdelsesjobtype og, hvis disse oplysninger er relevante, en relateret vedligeholdelsesjobvariant og en jobhandel.</span><span class="sxs-lookup"><span data-stu-id="218f4-138">Select a maintenance job type and, if this information is relevant, a related maintenance job variant and a job trade.</span></span>
- <span data-ttu-id="218f4-139">Angiv geografiske koordinater i felterne **Breddegrad** og **Længdegrad**.</span><span class="sxs-lookup"><span data-stu-id="218f4-139">In the **Latitude** and **Longitude** fields, enter geographic coordinates.</span></span> <span data-ttu-id="218f4-140">Alle koordinater, der føjes til en vedligeholdelsesanmodning, overføres automatisk til en relateret arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="218f4-140">Any coordinates that are added to a maintenance request are automatically transferred to a related work order.</span></span> 

![Figur 2](media/04-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="218f4-142">Hvis du vælger et aktiv, når du opretter en vedligeholdelsesanmodning, kan du føje én fejl til aktivet.</span><span class="sxs-lookup"><span data-stu-id="218f4-142">If you select an asset when you create a maintenance request, you can add one fault to the asset.</span></span> <span data-ttu-id="218f4-143">Når vedligeholdelsesanmodningen er blevet oprettet, kan du tilføje flere fejl efter behov.</span><span class="sxs-lookup"><span data-stu-id="218f4-143">After the maintenance request has been created, you can add more faults, as you require.</span></span> <span data-ttu-id="218f4-144">Hvis du vil tilføje fejl, skal du vælge **Aktivfejl** på siden **Alle vedligeholdelsesanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="218f4-144">To add faults, select **Asset fault** on the **All maintenance requests** page.</span></span>
