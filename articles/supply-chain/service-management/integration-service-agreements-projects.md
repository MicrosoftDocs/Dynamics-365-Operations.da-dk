---
title: Integration for serviceaftaler og -projekter
description: "Når du arbejder med serviceaftaler og serviceaftalelinjer, bruger du de data, der er konfigureret i følgende områder i Projektstyring og regnskab."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 6bd2fb1f54a3decb77f019db6b2016cebdcaddb9
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---

# <a name="integration-for-service-agreements-and-projects"></a><span data-ttu-id="885de-103">Integration for serviceaftaler og -projekter</span><span class="sxs-lookup"><span data-stu-id="885de-103">Integration for service agreements and projects</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="885de-104">Når du arbejder med serviceaftaler og serviceaftalelinjer, bruger du de data, der er konfigureret i følgende områder i **Projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="885de-104">When you work with service agreements and service agreement lines, you use data that is set up in the following areas in **Project management and accounting**.</span></span>

## <a name="project-prices"></a><span data-ttu-id="885de-105">Projektpriser</span><span class="sxs-lookup"><span data-stu-id="885de-105">Project prices</span></span>

<span data-ttu-id="885de-106">Kost- og salgsprisen for en serviceaftalepostering er afledt af den opsætning af kostpriser, der gælder for det projekt, som er knyttet til serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="885de-106">The cost and the sales price for a service agreement transaction are derived from the cost price setup that applies to the project that is attached to the service agreement.</span></span> <span data-ttu-id="885de-107">Kost- og salgspriser kan oprettes efter projekt, medarbejder og kategori.</span><span class="sxs-lookup"><span data-stu-id="885de-107">Cost and sales prices can be set up by project, employee, and category.</span></span> 

## <a name="project-validation"></a><span data-ttu-id="885de-108">Validering - projekter</span><span class="sxs-lookup"><span data-stu-id="885de-108">Project validation</span></span>

<span data-ttu-id="885de-109">De projekter, medarbejdere og kategorier, der kan vælges til en serviceaftalelinje, kan begrænses af opsætningen af validering i **Projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="885de-109">The projects, employees, and categories that are available for selection on a service agreement line can be limited by the validation setup in **Project management and accounting**.</span></span> <span data-ttu-id="885de-110">Ved hjælp af opsætning af validering kan du kombinere projekter, medarbejdere og kategorier for at kontrollere adgangen.</span><span class="sxs-lookup"><span data-stu-id="885de-110">By using the validation setup, you can combine employees, projects, and categories for control access.</span></span> 

## <a name="project-line-properties"></a><span data-ttu-id="885de-111">Projektlinjeegenskaber</span><span class="sxs-lookup"><span data-stu-id="885de-111">Project line properties</span></span>

<span data-ttu-id="885de-112">En linjeegenskab angives automatisk for en serviceaftalelinje.</span><span class="sxs-lookup"><span data-stu-id="885de-112">A line property is entered automatically for a service agreement line.</span></span>

<span data-ttu-id="885de-113">Linjeegenskaber oprettes i formularen **Linjeegenskaber** i **Projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="885de-113">Line properties are created in the **Line properties** form in **Project management and accounting**.</span></span> <span data-ttu-id="885de-114">Den linjeegenskab, der indsættes i en serviceaftale, knyttes til det projekt, der er valgt for serviceaftalen, og overføres efterfølgende til serviceaftalelinjen.</span><span class="sxs-lookup"><span data-stu-id="885de-114">The line property that is entered on a service agreement is attached to the project that is selected for the service agreement and inherited subsequently by the service agreement line.</span></span> 

## <a name="default-offset-accounts"></a><span data-ttu-id="885de-115">Standardmodkonti</span><span class="sxs-lookup"><span data-stu-id="885de-115">Default offset accounts</span></span>

<span data-ttu-id="885de-116">Hvis du angiver en udgiftspostering, vælges der automatisk en standardmodkonto for denne postering.</span><span class="sxs-lookup"><span data-stu-id="885de-116">If you enter an expense transaction, a default expense offset account is selected automatically for the transaction.</span></span> <span data-ttu-id="885de-117">Standardudgiftskontoen konfigureres for det projekt, der er knyttet til den aktuelle serviceaftale.</span><span class="sxs-lookup"><span data-stu-id="885de-117">The default expense account is set up for the project that is attached to the current service agreement.</span></span>

## <a name="project-categories"></a><span data-ttu-id="885de-118">Projektkategorier</span><span class="sxs-lookup"><span data-stu-id="885de-118">Project categories</span></span>

<span data-ttu-id="885de-119">De kategorier, der er tilgængelige for serviceaftalelinjer, er konfigureret i formularen **Projektkategori** i afsnittet **Projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="885de-119">The categories that are available for service agreement lines are set up in the **Project categories** form in **Project management and accounting**.</span></span> 

> [!NOTE]
> <P><span data-ttu-id="885de-120">Kategorier, hvor afkrydsningsfeltet <STRONG>Aktiv i kladder</STRONG> er markeret under fanen <STRONG>Projekt</STRONG> i formularen <STRONG>Projektkategorier</STRONG>, kan vælges.</span><span class="sxs-lookup"><span data-stu-id="885de-120">Categories that have the <STRONG>Active in journals</STRONG> check box selected on the <STRONG>Project</STRONG> tab in the <STRONG>Project categories</STRONG> form are available for selection.</span></span> <span data-ttu-id="885de-121">Hvis afkrydsningsfeltet <STRONG>Inaktive kategorier</STRONG> er markeret under fanen <STRONG>Kladder</STRONG> i formularen <STRONG>Parametre for projektstyring og regnskab</STRONG>, kan alle kategorier vælges.</span><span class="sxs-lookup"><span data-stu-id="885de-121">However, if the <STRONG>Inactive categories</STRONG> check box is selected on the <STRONG>Journals</STRONG> tab in the <STRONG>Project management and accounting parameters</STRONG> form, all categories are available for selection.</span></span></P>

## <a name="project-parameters"></a><span data-ttu-id="885de-122">Projektparametre</span><span class="sxs-lookup"><span data-stu-id="885de-122">Project parameters</span></span>

<span data-ttu-id="885de-123">Hvis feltet **Fratrådte arbejdere** under fanen **Kladder** i formularen **Parametre for projektstyring og regnskab** er markeret, kan du vælge inaktive medarbejdere og aktive medarbejdere i formularerne **Serviceaftaler** og **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="885de-123">If the **Terminated workers** field on the **Journals** tab in the **Project management and accounting parameters** form is selected, you can select inactive employees and active employees in the **Service agreements** and **Service orders** forms.</span></span>

<span data-ttu-id="885de-124">Du kan også aktivere felterne **Starttidspunkt** og **Sluttidspunkt** under fanen **Projekt** i formularen **Serviceordrer** for at angive start- og sluttidspunkter på serviceordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="885de-124">Also, you can enable the **Start time** and **End time** fields on the **Project** tab in the **Service orders** form to enter starting and ending times on service order lines.</span></span>

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a><span data-ttu-id="885de-125">Aktivere funktionen for start- og sluttidspunkter på serviceordrer</span><span class="sxs-lookup"><span data-stu-id="885de-125">Enable the starting and ending time feature for service orders</span></span>

1.  <span data-ttu-id="885de-126">Klik på **Projektstyring og regnskab** \> **Opsætning** \> **Parametre for projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="885de-126">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="885de-127">Klik på fanen **Kladder**, og marker afkrydsningsfeltet **Vis start-/ sluttidspunkt**.</span><span class="sxs-lookup"><span data-stu-id="885de-127">Click the **Journals** tab, and then select the **Show start/end times** check box.</span></span>

3.  <span data-ttu-id="885de-128">Klik på **Projektstyring og regnskab** \> **Opsætning** \> **Kladder** \> **Kladdenavne**.</span><span class="sxs-lookup"><span data-stu-id="885de-128">Click **Project management and accounting** \> **Setup** \> **Journals** \> **Journal names**.</span></span>

4.  <span data-ttu-id="885de-129">Markér det kladdenavn, der er knyttet til serviceordren.</span><span class="sxs-lookup"><span data-stu-id="885de-129">Select the journal name that is attached to the service order.</span></span>

5.  <span data-ttu-id="885de-130">Klik på fanen **Generelt**, og marker afkrydsningsfeltet **Vis start-/ sluttidspunkt**.</span><span class="sxs-lookup"><span data-stu-id="885de-130">Click the **General** tab, and then select the **Show start/end times** check box.</span></span>


> [!NOTE]
> <P><span data-ttu-id="885de-131">Vælg det kladdenavn for serviceordren i feltet <STRONG>Time</STRONG> under fanen <STRONG>Kladder</STRONG> i formularen <STRONG>Parametre for servicestyring</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="885de-131">Select the journal name for the service order in the <STRONG>Hour</STRONG> field on the <STRONG>Journals</STRONG> tab in the <STRONG>Service management parameters</STRONG> form.</span></span></P>






