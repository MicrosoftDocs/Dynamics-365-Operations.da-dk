---
title: Konfigurer serviceordrestadier
description: Konfigurer serviceordrestadier.
author: YuyuScheller
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
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
ms.openlocfilehash: 6e2556dd8f3f32da16e53bfe46faec7489d84efa
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-service-order-stages"></a><span data-ttu-id="7e9fd-103">Konfigurer serviceordrestadier</span><span class="sxs-lookup"><span data-stu-id="7e9fd-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="7e9fd-104">Klik på **Servicestyring** \> **Opsætning** \> **Serviceordrer** \> **Servicestadier**.</span><span class="sxs-lookup"><span data-stu-id="7e9fd-104">Click **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="7e9fd-105">Tryk på Ctrl+N for at oprette en ny post.</span><span class="sxs-lookup"><span data-stu-id="7e9fd-105">Press CTRL+N to create a new record.</span></span>

3.  <span data-ttu-id="7e9fd-106">Indtast et servicestadie-id og en beskrivelse i felterne **Servicestadie** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="7e9fd-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="7e9fd-107">Vælg de rette parametre for stadiet.</span><span class="sxs-lookup"><span data-stu-id="7e9fd-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="7e9fd-108">Vælg det overordnede stadie til det aktuelle stadie, eller lad feltet **Overordnet** være tomt, hvis stadiet er begyndelsesstadiet i stadieopsætningen.</span><span class="sxs-lookup"><span data-stu-id="7e9fd-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7e9fd-109">Du kan ikke redigere feltet <STRONG>Overordnet</STRONG>, når du har gemt stadiet.</span><span class="sxs-lookup"><span data-stu-id="7e9fd-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="7e9fd-110">I stedet kan du slette posten og oprette den igen med et andet valg i feltet <STRONG>Overordnet</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="7e9fd-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="7e9fd-111">Du kan også kun oprette ét stadie med et tomt <STRONG>Overordnet</STRONG>-felt.</span><span class="sxs-lookup"><span data-stu-id="7e9fd-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="7e9fd-112">Det er altså kun tilladt at have ét begyndelsesstadie.</span><span class="sxs-lookup"><span data-stu-id="7e9fd-112">That is, only one initial stage is permitted.</span></span></P>


  



