---
title: Oprette serviceordrer manuelt
description: "Du kan oprette serviceordrer manuelt ved hjælp af en serviceaftale eller formularen **Serviceordrer**."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a0cc6b2646929776f4efb20474de6b0fc5c4719c
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="create-service-orders-manually"></a><span data-ttu-id="75b20-103">Oprette serviceordrer manuelt</span><span class="sxs-lookup"><span data-stu-id="75b20-103">Create service orders manually</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="75b20-104">Du kan oprette serviceordrer manuelt ved hjælp af en serviceaftale eller formularen **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="75b20-104">You can create service orders manually by using a service agreement or by using the **Service orders** form.</span></span> <span data-ttu-id="75b20-105">Du kan også oprette en serviceordre fra et projekt.</span><span class="sxs-lookup"><span data-stu-id="75b20-105">You can also create a service order from a project.</span></span>

> [!TIP]
> <P><span data-ttu-id="75b20-106">Du kan bruge automatiske processer til at oprette serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="75b20-106">You can use automated processes to create service orders.</span></span> 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a><span data-ttu-id="75b20-107">Oprette en serviceordre manuelt fra en serviceaftale</span><span class="sxs-lookup"><span data-stu-id="75b20-107">Create a service order manually from a service agreement</span></span>

1.  <span data-ttu-id="75b20-108">Klik på **Servicestyring** \> **Almindelige** \> **Serviceaftaler** \> **Serviceaftaler**.</span><span class="sxs-lookup"><span data-stu-id="75b20-108">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="75b20-109">Vælg en serviceaftale, eller opret en ny serviceaftale.</span><span class="sxs-lookup"><span data-stu-id="75b20-109">Select a service agreement or create a new service agreement.</span></span>

3.  <span data-ttu-id="75b20-110">Klik på fanen **Levér** og klik i gruppen **Opret** på **Planlagte serviceordrer** for at åbne formularen **Opret serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="75b20-110">Click the **Deliver** tab and in the **Create** group click **Planned service orders** to open the **Create service orders** form.</span></span>

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a><span data-ttu-id="75b20-111">Oprette en serviceordre manuelt i formen Serviceordrer</span><span class="sxs-lookup"><span data-stu-id="75b20-111">Create a service order manually in the Service orders form</span></span>

1.  <span data-ttu-id="75b20-112">Klik på **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="75b20-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="75b20-113">Tryk på Ctrl+N for at oprette en ny serviceordre.</span><span class="sxs-lookup"><span data-stu-id="75b20-113">Press Ctrl+N to create a new service order.</span></span>

3.  <span data-ttu-id="75b20-114">Opret serviceordrelinjer til serviceordren.</span><span class="sxs-lookup"><span data-stu-id="75b20-114">Create service order lines for the service order.</span></span>

> [!NOTE]
> <P><span data-ttu-id="75b20-115">Hvis afkrydsningsfeltet <STRONG>Tillad uden serviceaftale</STRONG> i formularen <STRONG>Parametre for servicestyring</STRONG> er markeret, kan du bogføre posteringer fra serviceordrelinjerne uden at knytte serviceordren til en serviceaftale.</span><span class="sxs-lookup"><span data-stu-id="75b20-115">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="75b20-116">Hvis markeringen i afkrydsningsfeltet fjernes, skal du knytte den manuelt oprettede serviceordre til et projekt, inden du bogfører serviceordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="75b20-116">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-a-project"></a><span data-ttu-id="75b20-117">Oprette en serviceordre ud fra et projekt</span><span class="sxs-lookup"><span data-stu-id="75b20-117">Create a service order from a project</span></span>

1.  <span data-ttu-id="75b20-118">Klik på **Projektstyring og regnskab** \> **Generelt** \> **Projekter** \> **Alle projekter**.</span><span class="sxs-lookup"><span data-stu-id="75b20-118">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="75b20-119">I formularen **Projekter** skal du i **handlingsruden** klikke på fanen **Administrer** \> og klikke på **Service** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="75b20-119">In the **Projects** form, on the **Action pane**, click the **Manage** tab \> click **Service** \> **Service orders**.</span></span>

3.  <span data-ttu-id="75b20-120">Følg den foregående fremgangsmåde for at oprette en serviceordre manuelt i formularen **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="75b20-120">Follow the previous procedure to create a service order manually in the **Service orders** form.</span></span> <span data-ttu-id="75b20-121">I feltet **Projekt-id** vises projektreferencen.</span><span class="sxs-lookup"><span data-stu-id="75b20-121">The **Project ID** field displays the project reference.</span></span>

> [!NOTE]
> <P><span data-ttu-id="75b20-122">Hvis afkrydsningsfeltet <STRONG>Tillad uden serviceaftale</STRONG> i formularen <STRONG>Parametre for servicestyring</STRONG> er markeret, kan du bogføre posteringer fra serviceordrelinjerne uden at knytte serviceordren til en serviceaftale.</span><span class="sxs-lookup"><span data-stu-id="75b20-122">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="75b20-123">Hvis markeringen i afkrydsningsfeltet fjernes, skal du knytte den manuelt oprettede serviceordre til et projekt, inden du bogfører serviceordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="75b20-123">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-the-sales-order-form"></a><span data-ttu-id="75b20-124">Oprette en serviceordre fra formen Salgsordre</span><span class="sxs-lookup"><span data-stu-id="75b20-124">Create a service order from the Sales order form</span></span>

<span data-ttu-id="75b20-125">Du kan oprette en serviceordre fra formularen **Salgsordrer** ved hjælp af guiden **Opret en ny serviceordre ud fra salgsordren**.</span><span class="sxs-lookup"><span data-stu-id="75b20-125">You can create a service order from the **Sales orders** form by using the **Create a new service order based on the sales order** wizard.</span></span>

1.  <span data-ttu-id="75b20-126">Klik på **Salg og marketing** \> **Generelt** \> **Salgsordrer** \> **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="75b20-126">Click **Sales and marketing** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="75b20-127">Åbn den relevante salgsordre.</span><span class="sxs-lookup"><span data-stu-id="75b20-127">Open the relevant sales order.</span></span>

3.  <span data-ttu-id="75b20-128">Under fanen **Salgsordre** skal du klikke på **Serviceordre** for at starte guiden **Opret en ny serviceordre ud fra salgsordren**.</span><span class="sxs-lookup"><span data-stu-id="75b20-128">On the **Sales order** tab, click **Service order** to start the **Create a new service order based on the sales order** wizard.</span></span>

4.  <span data-ttu-id="75b20-129">Klik på **Næste \>**, og udfør derefter følgende trin på siden **Vælg aftale for serviceordre**:</span><span class="sxs-lookup"><span data-stu-id="75b20-129">Click **Next \>**, and then complete the following steps on the **Select agreement for service order** page:</span></span>
    
      - <span data-ttu-id="75b20-130">Brug feltet **Serviceaftale** til at vælge den serviceaftale, den nye serviceordre skal knyttes til.</span><span class="sxs-lookup"><span data-stu-id="75b20-130">Use the **Service agreement** field to select the service agreement with which the new service order should be associated.</span></span>
    
      - <span data-ttu-id="75b20-131">Valgfrit: Brug feltet **Projekt-id** til at knytte denne serviceordre til et bestemt projekt.</span><span class="sxs-lookup"><span data-stu-id="75b20-131">Optional: Use the **Project ID** field to associate this service order with a particular project.</span></span>

5.  <span data-ttu-id="75b20-132">Klik på **Næste \>**, og udfør derefter følgende trin på siden **Opret serviceordre**:</span><span class="sxs-lookup"><span data-stu-id="75b20-132">Click **Next \>**, and then complete the following steps on the **Create service order** page:</span></span>
    
      - <span data-ttu-id="75b20-133">Angiv en dato og et klokkeslæt for, hvornår servicebesøget skal starte, i feltet **Foretrukket servicetidspunkt**.</span><span class="sxs-lookup"><span data-stu-id="75b20-133">Enter a date and time for the service call to begin in the **Preferred service time** field.</span></span>
    
      - <span data-ttu-id="75b20-134">Valgfrit: Rediger teksten i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="75b20-134">Optional: Modify the text in the **Description** field.</span></span> <span data-ttu-id="75b20-135">Dette felt indeholder som standard en beskrivelse af den serviceaftale, du har valgt på forrige side.</span><span class="sxs-lookup"><span data-stu-id="75b20-135">By default, this field contains the description of the service agreement that you selected on the previous page.</span></span>
    
      - <span data-ttu-id="75b20-136">Vælg id'et for den medarbejder, der er ansvarlig for aftalen, i feltet **Ansvarlig**, og hvis du kender id'et for kundens foretrukne tekniker ved servicebesøget, skal du også angive det.</span><span class="sxs-lookup"><span data-stu-id="75b20-136">In the **Responsible** field, select the ID of the employee who is responsible for the agreement, and if you know what it is, enter the ID of the customer's preferred technician for the service call.</span></span>
    
      - <span data-ttu-id="75b20-137">Vælg den person hos kunden, der skal kontaktes angående denne serviceordre, i feltet **Kontakt-id**.</span><span class="sxs-lookup"><span data-stu-id="75b20-137">In the **Contact ID** field, select the person in the customer's company who should be contacted regarding this service order.</span></span>

6.  <span data-ttu-id="75b20-138">Klik på **Næste \>**, og klik derefter på **Udfør**.</span><span class="sxs-lookup"><span data-stu-id="75b20-138">Click **Next \>**, and then click **Finish**.</span></span>


## <a name="see-also"></a><span data-ttu-id="75b20-139">Se også</span><span class="sxs-lookup"><span data-stu-id="75b20-139">See also</span></span>

[<span data-ttu-id="75b20-140">Serviceordrer</span><span class="sxs-lookup"><span data-stu-id="75b20-140">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="75b20-141">Oprette serviceordrer automatisk</span><span class="sxs-lookup"><span data-stu-id="75b20-141">Create service orders automatically</span></span>](create-service-orders-automatically.md)

<span data-ttu-id="75b20-142">[Opret serviceordrer (klasseform)](https://technet.microsoft.com/en-us/library/aa553901\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="75b20-142">[Create service orders (class form)](https://technet.microsoft.com/en-us/library/aa553901\(v=ax.60\))</span></span> 


