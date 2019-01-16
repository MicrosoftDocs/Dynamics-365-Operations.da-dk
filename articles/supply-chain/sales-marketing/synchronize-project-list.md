---
title: Synkronisere projektliste fra Finance and Operations til Field Service
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere projekter fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: da-dk
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="27657-103">Synkronisere projektliste fra Finance and Operations til Field Service</span><span class="sxs-lookup"><span data-stu-id="27657-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="27657-104">Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere projekter fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="27657-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="27657-105">[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="27657-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="27657-106">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="27657-106">Templates and tasks</span></span>
<span data-ttu-id="27657-107">Følgende skabelon og underliggende opgaver bruges til at køre synkronisering af projekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="27657-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="27657-108">**Navnet på skabelonen i dataintegration:**</span><span class="sxs-lookup"><span data-stu-id="27657-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="27657-109">Projekter (Finance and Operations til Field Service)</span><span class="sxs-lookup"><span data-stu-id="27657-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="27657-110">**Navne på opgaverne i dataintegrationsprojektet:**</span><span class="sxs-lookup"><span data-stu-id="27657-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="27657-111">Projekter</span><span class="sxs-lookup"><span data-stu-id="27657-111">Projects</span></span>

<span data-ttu-id="27657-112">Følgende synkroniseringsopgaver kræves, før projektlister kan synkroniseres:</span><span class="sxs-lookup"><span data-stu-id="27657-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="27657-113">Konti (Sales til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="27657-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="27657-114">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="27657-114">Entity set</span></span>
<span data-ttu-id="27657-115">Field Service   Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27657-115">Field Service   Finance and Operations</span></span>

| <span data-ttu-id="27657-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="27657-116">Field Service</span></span>           | <span data-ttu-id="27657-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27657-117">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="27657-118">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="27657-118">msdynce_externalprojects</span></span> | <span data-ttu-id="27657-119">Projekter</span><span class="sxs-lookup"><span data-stu-id="27657-119">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="27657-120">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="27657-120">Entity flow</span></span>
<span data-ttu-id="27657-121">Projekter oprettes i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="27657-121">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="27657-122">Projekter med **Projekttype** Tid og materialer og **Projektstadie** Under behandling bliver synkroniseret til enheden **Eksternt projekt** i Field Service, herunder projektnummer, projektnavn, projektstadie og oplysninger om debitorkonti.</span><span class="sxs-lookup"><span data-stu-id="27657-122">Projects with **Project type** Time and material and **Project stage** In process will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage and Customer account information.</span></span> <span data-ttu-id="27657-123">Listen **Eksternt projekt** bruges til at parre Field Service-serviceordrer med Finance and Operations-projekter.</span><span class="sxs-lookup"><span data-stu-id="27657-123">The list of **External Project** is used to pair Field service Work orders with Finance and Operations projects.</span></span>
<span data-ttu-id="27657-124">CRM-løsningen til Field Service Eksternt projekt er en ny enhed, der får alle projekterne fra Operations.</span><span class="sxs-lookup"><span data-stu-id="27657-124">Field Service CRM solution The External Project is a new entity that gets all the Projects from Operations.</span></span>
<span data-ttu-id="27657-125">Feltet Eksternt projekt er føjet til enheden Arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="27657-125">The External Project field has been added to the Work Order entity.</span></span> <span data-ttu-id="27657-126">Dette er et find og køb-felt, som mærker arbejdsordren til et projekt. Salgsordren bliver derefter forbundet med et projekt i Operations.</span><span class="sxs-lookup"><span data-stu-id="27657-126">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Operations.</span></span> <span data-ttu-id="27657-127">Når systemstatus skifter Åben - i gang (690,970,000) til en højere status, låses feltet Eksternt projekt, og du kan ikke tilføje, fjerne eller ændre værdien.</span><span class="sxs-lookup"><span data-stu-id="27657-127">Ones the System Status changes Open – In Progress(690,970,000) to a higher status the External Project field will be locked and you can't add, remove or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="27657-128">Forudsætninger og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="27657-128">Prerequisites and mapping setup</span></span>
### <a name="in-finance-and-operations"></a><span data-ttu-id="27657-129">I Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27657-129">In Finance and Operations</span></span>
<span data-ttu-id="27657-130">Gøre det muligt at spore ændringer for Dataenhed-projekter</span><span class="sxs-lookup"><span data-stu-id="27657-130">Enable change tracking for Data entity Projects</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="27657-131">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="27657-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="27657-132">Projekter (Finance and Operations til Field Service): Projekter</span><span class="sxs-lookup"><span data-stu-id="27657-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="27657-133">[![Skabelontilknytning i dataintegration](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="27657-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>

