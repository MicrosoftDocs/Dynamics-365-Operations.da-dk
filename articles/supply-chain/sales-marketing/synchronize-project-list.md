---
title: Synkronisere projektliste fra Supply Chain Management til Field Service
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projekter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: b74a7f0445b3bdad671da4c61e561bc0d9d80cd1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251586"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a><span data-ttu-id="1e7e2-103">Synkronisere projektliste fra Supply Chain Management til Field Service</span><span class="sxs-lookup"><span data-stu-id="1e7e2-103">Synchronize project list from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1e7e2-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projekter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="1e7e2-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="1e7e2-105">[![Synkronisering af forretningsprocesser mellem Supply Chain Management og Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="1e7e2-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="1e7e2-106">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="1e7e2-106">Templates and tasks</span></span>
<span data-ttu-id="1e7e2-107">Følgende skabelon og underliggende opgaver bruges til at synkronisere projekter fra Supply Chain Management til Field Service.</span><span class="sxs-lookup"><span data-stu-id="1e7e2-107">The following template and underlying tasks are used to run synchronization of projects from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="1e7e2-108">**Skabelon i dataintegration**</span><span class="sxs-lookup"><span data-stu-id="1e7e2-108">**Template in Data integration**</span></span>
- <span data-ttu-id="1e7e2-109">Projekter (Supply Chain Management til Field Service)</span><span class="sxs-lookup"><span data-stu-id="1e7e2-109">Projects (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="1e7e2-110">**Opgave i dataintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="1e7e2-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="1e7e2-111">Projekter</span><span class="sxs-lookup"><span data-stu-id="1e7e2-111">Projects</span></span>

<span data-ttu-id="1e7e2-112">Følgende synkroniseringsopgaver kræves, før projektlister kan synkroniseres:</span><span class="sxs-lookup"><span data-stu-id="1e7e2-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="1e7e2-113">Konti (Sales til Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="1e7e2-113">Accounts (Sales to Supply Chain Management)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="1e7e2-114">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="1e7e2-114">Entity set</span></span>
| <span data-ttu-id="1e7e2-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="1e7e2-115">Field Service</span></span>           | <span data-ttu-id="1e7e2-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1e7e2-116">Supply Chain Management</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="1e7e2-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="1e7e2-117">msdynce_externalprojects</span></span> | <span data-ttu-id="1e7e2-118">Projekter</span><span class="sxs-lookup"><span data-stu-id="1e7e2-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="1e7e2-119">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="1e7e2-119">Entity flow</span></span>
<span data-ttu-id="1e7e2-120">Projekter oprettes i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1e7e2-120">Projects are created in Supply Chain Management.</span></span> <span data-ttu-id="1e7e2-121">Projekter med **Projekttype** indstillet til **Tid og materialer** og **Projektstadie** indstillet til **Under behandling** bliver synkroniseret til enheden **Eksternt projekt** i Field Service, herunder projektnummer, projektnavn, projektstadie og oplysninger om debitorkonti.</span><span class="sxs-lookup"><span data-stu-id="1e7e2-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="1e7e2-122">Listen **Eksternt projekt** bruges til at parre arbejdsordrer i Field Service med projekter i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1e7e2-122">The **External Project** list is used to pair Field service work orders with Supply Chain Management projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="1e7e2-123">CRM-løsning til Field Service</span><span class="sxs-lookup"><span data-stu-id="1e7e2-123">Field Service CRM solution</span></span>
<span data-ttu-id="1e7e2-124">Enheden **Eksternt projekt** får alle projekterne fra Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1e7e2-124">The **External Project** entity gets all the projects from Supply Chain Management.</span></span> <span data-ttu-id="1e7e2-125">Feltet **Eksternt projekt** er føjet til enheden **Arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="1e7e2-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="1e7e2-126">Dette er et opslagsfelt, så hvis du mærker arbejdsordren til et projekt, bliver salgsordren forbundet med et projekt i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1e7e2-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Supply Chain Management.</span></span> <span data-ttu-id="1e7e2-127">Når **Systemstatus** ændrer **Åben - i gang (690,970,000)** til en højere status, låses feltet **Eksternt projekt**, og du kan ikke længere tilføje, fjerne eller ændre værdien.</span><span class="sxs-lookup"><span data-stu-id="1e7e2-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="1e7e2-128">Forudsætninger og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="1e7e2-128">Prerequisites and mapping setup</span></span>
### <a name="supply-chain-management"></a><span data-ttu-id="1e7e2-129">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1e7e2-129">Supply Chain Management</span></span>
<span data-ttu-id="1e7e2-130">Gør det muligt at spore ændringer for Dataenhed-projekter.</span><span class="sxs-lookup"><span data-stu-id="1e7e2-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1e7e2-131">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="1e7e2-131">Template mapping in Data integration</span></span>


### <a name="projects-supply-chain-management-to-field-service-projects"></a><span data-ttu-id="1e7e2-132">Projekter (Supply Chain Management til Field Service): Projekter</span><span class="sxs-lookup"><span data-stu-id="1e7e2-132">Projects (Supply Chain Management to Field Service): Projects</span></span>

<span data-ttu-id="1e7e2-133">[![Skabelontilknytning i dataintegration](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="1e7e2-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
