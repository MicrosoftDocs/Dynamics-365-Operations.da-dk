---
title: Synkronisere projektliste fra Finance and Operations til Field Service
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: 535094821ca7efa33bf40f2057fac8ffc17bb822
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843547"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="e8c46-103">Synkronisere projektliste fra Finance and Operations til Field Service</span><span class="sxs-lookup"><span data-stu-id="e8c46-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e8c46-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="e8c46-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e8c46-105">[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="e8c46-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e8c46-106">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="e8c46-106">Templates and tasks</span></span>
<span data-ttu-id="e8c46-107">Følgende skabelon og underliggende opgaver bruges til at køre synkronisering af projekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="e8c46-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e8c46-108">**Skabelon i dataintegration**</span><span class="sxs-lookup"><span data-stu-id="e8c46-108">**Template in Data integration**</span></span>
- <span data-ttu-id="e8c46-109">Projekter (Fin and Ops til Field Service)</span><span class="sxs-lookup"><span data-stu-id="e8c46-109">Projects (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="e8c46-110">**Opgave i dataintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="e8c46-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="e8c46-111">Projekter</span><span class="sxs-lookup"><span data-stu-id="e8c46-111">Projects</span></span>

<span data-ttu-id="e8c46-112">Følgende synkroniseringsopgaver kræves, før projektlister kan synkroniseres:</span><span class="sxs-lookup"><span data-stu-id="e8c46-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="e8c46-113">Konti (salg til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="e8c46-113">Accounts (Sales to Fin and Ops)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="e8c46-114">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="e8c46-114">Entity set</span></span>
| <span data-ttu-id="e8c46-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="e8c46-115">Field Service</span></span>           | <span data-ttu-id="e8c46-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e8c46-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="e8c46-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="e8c46-117">msdynce_externalprojects</span></span> | <span data-ttu-id="e8c46-118">Projekter</span><span class="sxs-lookup"><span data-stu-id="e8c46-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="e8c46-119">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="e8c46-119">Entity flow</span></span>
<span data-ttu-id="e8c46-120">Projekter oprettes i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e8c46-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="e8c46-121">Projekter med **Projekttype** indstillet til **Tid og materialer** og **Projektstadie** indstillet til **Under behandling** bliver synkroniseret til enheden **Eksternt projekt** i Field Service, herunder projektnummer, projektnavn, projektstadie og oplysninger om debitorkonti.</span><span class="sxs-lookup"><span data-stu-id="e8c46-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="e8c46-122">Listen **Eksternt projekt** bruges til at parre arbejdsordrer i Field Service med Finance and Operations-projekter.</span><span class="sxs-lookup"><span data-stu-id="e8c46-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="e8c46-123">CRM-løsning til Field Service</span><span class="sxs-lookup"><span data-stu-id="e8c46-123">Field Service CRM solution</span></span>
<span data-ttu-id="e8c46-124">Enheden **Eksternt projekt** får alle projekterne fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e8c46-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="e8c46-125">Feltet **Eksternt projekt** er føjet til enheden **Arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="e8c46-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="e8c46-126">Dette er et opslagsfelt, så hvis du mærker arbejdsordren til et projekt, bliver salgsordren forbundet med et projekt i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e8c46-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="e8c46-127">Når **Systemstatus** ændrer **Åben - i gang (690,970,000)** til en højere status, låses feltet **Eksternt projekt**, og du kan ikke længere tilføje, fjerne eller ændre værdien.</span><span class="sxs-lookup"><span data-stu-id="e8c46-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="e8c46-128">Forudsætninger og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="e8c46-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="e8c46-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e8c46-129">Finance and Operations</span></span>
<span data-ttu-id="e8c46-130">Gør det muligt at spore ændringer for Dataenhed-projekter.</span><span class="sxs-lookup"><span data-stu-id="e8c46-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e8c46-131">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="e8c46-131">Template mapping in Data integration</span></span>


### <a name="projects-fin-and-ops-to-field-service-projects"></a><span data-ttu-id="e8c46-132">Projekter (Fin and Ops til Field Service): projekter</span><span class="sxs-lookup"><span data-stu-id="e8c46-132">Projects (Fin and Ops to Field Service): Projects</span></span>

<span data-ttu-id="e8c46-133">[![Skabelontilknytning i dataintegration](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="e8c46-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
