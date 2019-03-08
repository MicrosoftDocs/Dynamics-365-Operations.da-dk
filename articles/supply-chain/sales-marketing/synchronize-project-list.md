---
title: Synkronisere projektliste fra Finance and Operations til Field Service
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: b5aeb4c3925994d7488e8e113e88b9d06ee6b350
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "312502"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="b7366-103">Synkronisere projektliste fra Finance and Operations til Field Service</span><span class="sxs-lookup"><span data-stu-id="b7366-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b7366-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="b7366-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="b7366-105">[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="b7366-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b7366-106">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="b7366-106">Templates and tasks</span></span>
<span data-ttu-id="b7366-107">Følgende skabelon og underliggende opgaver bruges til at køre synkronisering af projekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="b7366-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="b7366-108">**Skabelon i dataintegration**</span><span class="sxs-lookup"><span data-stu-id="b7366-108">**Template in Data integration**</span></span>
- <span data-ttu-id="b7366-109">Projekter (Finance and Operations til Field Service)</span><span class="sxs-lookup"><span data-stu-id="b7366-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="b7366-110">**Opgave i dataintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="b7366-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="b7366-111">Projekter</span><span class="sxs-lookup"><span data-stu-id="b7366-111">Projects</span></span>

<span data-ttu-id="b7366-112">Følgende synkroniseringsopgaver kræves, før projektlister kan synkroniseres:</span><span class="sxs-lookup"><span data-stu-id="b7366-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="b7366-113">Konti (Sales til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="b7366-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="b7366-114">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="b7366-114">Entity set</span></span>
| <span data-ttu-id="b7366-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="b7366-115">Field Service</span></span>           | <span data-ttu-id="b7366-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b7366-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="b7366-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="b7366-117">msdynce_externalprojects</span></span> | <span data-ttu-id="b7366-118">Projekter</span><span class="sxs-lookup"><span data-stu-id="b7366-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="b7366-119">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="b7366-119">Entity flow</span></span>
<span data-ttu-id="b7366-120">Projekter oprettes i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b7366-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="b7366-121">Projekter med **Projekttype** indstillet til **Tid og materialer** og **Projektstadie** indstillet til **Under behandling** bliver synkroniseret til enheden **Eksternt projekt** i Field Service, herunder projektnummer, projektnavn, projektstadie og oplysninger om debitorkonti.</span><span class="sxs-lookup"><span data-stu-id="b7366-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="b7366-122">Listen **Eksternt projekt** bruges til at parre arbejdsordrer i Field Service med Finance and Operations-projekter.</span><span class="sxs-lookup"><span data-stu-id="b7366-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="b7366-123">CRM-løsning til Field Service</span><span class="sxs-lookup"><span data-stu-id="b7366-123">Field Service CRM solution</span></span>
<span data-ttu-id="b7366-124">Enheden **Eksternt projekt** får alle projekterne fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b7366-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="b7366-125">Feltet **Eksternt projekt** er føjet til enheden **Arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="b7366-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="b7366-126">Dette er et opslagsfelt, så hvis du mærker arbejdsordren til et projekt, bliver salgsordren forbundet med et projekt i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b7366-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="b7366-127">Når **Systemstatus** ændrer **Åben - i gang (690,970,000)** til en højere status, låses feltet **Eksternt projekt**, og du kan ikke længere tilføje, fjerne eller ændre værdien.</span><span class="sxs-lookup"><span data-stu-id="b7366-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="b7366-128">Forudsætninger og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="b7366-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="b7366-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b7366-129">Finance and Operations</span></span>
<span data-ttu-id="b7366-130">Gør det muligt at spore ændringer for Dataenhed-projekter.</span><span class="sxs-lookup"><span data-stu-id="b7366-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b7366-131">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="b7366-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="b7366-132">Projekter (Finance and Operations til Field Service): Projekter</span><span class="sxs-lookup"><span data-stu-id="b7366-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="b7366-133">[![Skabelontilknytning i dataintegration](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="b7366-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
