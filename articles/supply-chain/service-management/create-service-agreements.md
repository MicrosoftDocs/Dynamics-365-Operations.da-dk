---
title: Oprette serviceaftaler
description: I dette emne beskrives det, hvordan du kan bruge funktionerne i modulerne Servicestyring og Projektstyring og regnskab til at oprette serviceaftaler.
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef5ca8cc9c80581b9f7ef69bd8c4403d3d0296e8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965953"
---
# <a name="create-service-agreements"></a><span data-ttu-id="406b0-103">Oprette serviceaftaler</span><span class="sxs-lookup"><span data-stu-id="406b0-103">Create service agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="406b0-104">I dette emne beskrives det, hvordan du kan bruge funktionerne i modulerne Servicestyring og Projektstyring og regnskab til at oprette serviceaftaler.</span><span class="sxs-lookup"><span data-stu-id="406b0-104">This topic describes how to use features in the Service management and the Project management and accounting modules to create service agreements.</span></span>

## <a name="create-a-service-agreement-from-service-management"></a><span data-ttu-id="406b0-105">Oprette en serviceaftale fra Service</span><span class="sxs-lookup"><span data-stu-id="406b0-105">Create a service agreement from Service management</span></span>

1. <span data-ttu-id="406b0-106">Gå til **Servicestyring**.</span><span class="sxs-lookup"><span data-stu-id="406b0-106">Navigate to **Service management**.</span></span>
2. <span data-ttu-id="406b0-107">Klik på **Serviceaftaler** for at oprette en ny serviceaftalelinje i sidehovedet.</span><span class="sxs-lookup"><span data-stu-id="406b0-107">Click **Service agreements** to create a new service agreement line in the page header.</span></span> 
3. <span data-ttu-id="406b0-108">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="406b0-108">Click **New**.</span></span> <span data-ttu-id="406b0-109">Indtast en beskrivelse, vælg en reference til et projekt i feltet **Projekt-id**, og udfyld resten af felterne og linjerne til serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="406b0-109">Enter a description, select a reference to a project in the **Project ID** field, and fill in the rest of the fields and lines for the service agreement.</span></span> <span data-ttu-id="406b0-110">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="406b0-110">Click **Save**.</span></span>
4. <span data-ttu-id="406b0-111">Under fanen **Relationer** skal du vælge **Serviceobjekter** eller **Serviceopgaver** for at oprette serviceobjektrelationer eller serviceopgaverelationer for serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="406b0-111">On the **Relations** tab, select **Service objects** or **Service tasks** to create service object relations or service task relations for the service agreement.</span></span> <span data-ttu-id="406b0-112">De serviceobjekter og -opgaver, du har oprettet relationer for, kan tilknyttes på serviceaftalelinjerne.</span><span class="sxs-lookup"><span data-stu-id="406b0-112">The service objects and tasks that you have created relations for can be attached on the lines of the service agreement.</span></span>
5. <span data-ttu-id="406b0-113">På den nederste halvdel af siden kan du oprette serviceaftalelinjer ved at kopiere linjer fra en serviceskabelon eller en anden serviceaftale eller ved at oprette serviceaftalelinjerne manuelt.</span><span class="sxs-lookup"><span data-stu-id="406b0-113">In the lower half of the page, create service agreement lines by copying lines from a service template, another service agreement, or manually creating the service-agreement lines.</span></span>

> [!NOTE]
> <span data-ttu-id="406b0-114">Hvis du kopierer linjer til serviceaftalen fra en anden serviceaftale, kan du angive, om du også vil kopiere serviceobjektrelationer og serviceaftalerelationer.</span><span class="sxs-lookup"><span data-stu-id="406b0-114">If you copy lines into the service agreement from another service agreement, you can indicate whether you also want to copy service object and service task relations.</span></span> <span data-ttu-id="406b0-115">Hvis du kopierer disse relationer, føjes de til eventuelle eksisterende relationer på serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="406b0-115">If you copy these relations, they are added to any existing relations on the service agreement.</span></span> <span data-ttu-id="406b0-116">Hvis du kopierer serviceaftalelinjer fra en serviceskabelon, kopieres serviceobjektrelationerne og serviceopgaverelationerne automatisk som serviceobjektrelationer og serviceopgaverelationer på de nye serviceaftalelinjer.</span><span class="sxs-lookup"><span data-stu-id="406b0-116">If you copy service-agreement lines from a service template, the service-object and service-task relations are automatically copied as service-object relations and service-task relations on the new service-agreement lines.</span></span>

## <a name="create-service-agreement-lines-manually"></a><span data-ttu-id="406b0-117">Oprette serviceaftalelinjer manuelt</span><span class="sxs-lookup"><span data-stu-id="406b0-117">Create service agreement lines manually</span></span>

1. <span data-ttu-id="406b0-118">På siden **Serviceaftaler** skal du tilføje en serviceaftalelinje i linjegitteret.</span><span class="sxs-lookup"><span data-stu-id="406b0-118">From the **Service agreements** page, add a service agreement line in the lines grid.</span></span> 
2. <span data-ttu-id="406b0-119">Angiv de relevante oplysninger for serviceaftalelinjen.</span><span class="sxs-lookup"><span data-stu-id="406b0-119">Enter the appropriate information for the service agreement line.</span></span> 
3. <span data-ttu-id="406b0-120">Tryk på **CTRL+S** for at gemme linjen, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="406b0-120">Press **CTRL+S** to save the line, and then close the page.</span></span>

## <a name="create-a-service-agreement-from-project"></a><span data-ttu-id="406b0-121">Oprette en serviceaftale fra Projekt</span><span class="sxs-lookup"><span data-stu-id="406b0-121">Create a service agreement from Project</span></span>

1. <span data-ttu-id="406b0-122">Klik på **Projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="406b0-122">Click **Project management and accounting**.</span></span>
2. <span data-ttu-id="406b0-123">Klik på **Alle projekter**.</span><span class="sxs-lookup"><span data-stu-id="406b0-123">Click **All projects**.</span></span>
3. <span data-ttu-id="406b0-124">Vælg projektet på listen.</span><span class="sxs-lookup"><span data-stu-id="406b0-124">Select the project from the list.</span></span>
4. <span data-ttu-id="406b0-125">Klik på **Administrer** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="406b0-125">On the **Action Pane**, click **Manage**.</span></span> <span data-ttu-id="406b0-126">I den **Ny** aktionsgruppe skal du klikke på **Service** og vælge **Serviceaftale**.</span><span class="sxs-lookup"><span data-stu-id="406b0-126">In the **New** Action group, click **Service** and select **Service agreement**.</span></span>
5. <span data-ttu-id="406b0-127">Følg trinnene i sektionen med titlen **Oprette en serviceaftale** som beskrevet tidligere i dette emne for at angive projektreferencen.</span><span class="sxs-lookup"><span data-stu-id="406b0-127">Follow the steps in the section titled **Create a service agreement** as described earlier in this topic to enter the project reference.</span></span>


## <a name="related-topics"></a><span data-ttu-id="406b0-128">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="406b0-128">Related topics</span></span>

[<span data-ttu-id="406b0-129">Oversigt over udvikling og udfyldelse af serviceaftaler</span><span class="sxs-lookup"><span data-stu-id="406b0-129">Develop and establish service agreements overview</span></span>](service-agreements.md)


