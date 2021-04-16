---
title: Konfigurer serviceordrestadier
description: Konfigurer serviceordrestadier.
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b6e245b351b66724eedf8e0d1a0ebf0202df857
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824408"
---
# <a name="set-up-service-order-stages"></a><span data-ttu-id="317f1-103">Konfigurer serviceordrestadier</span><span class="sxs-lookup"><span data-stu-id="317f1-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="317f1-104">Gå til **Servicestyring** \> **Opsætning** \> **Serviceordrer** \> **Servicestadier**.</span><span class="sxs-lookup"><span data-stu-id="317f1-104">Go to **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="317f1-105">Vælg **Ny** for at oprette en ny post.</span><span class="sxs-lookup"><span data-stu-id="317f1-105">Select **New** to create a new record.</span></span>

3.  <span data-ttu-id="317f1-106">Indtast et servicestadie-id og en beskrivelse i felterne **Servicestadie** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="317f1-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="317f1-107">Vælg de rette parametre for stadiet.</span><span class="sxs-lookup"><span data-stu-id="317f1-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="317f1-108">Vælg det overordnede stadie til det aktuelle stadie, eller lad feltet **Overordnet** være tomt, hvis stadiet er begyndelsesstadiet i stadieopsætningen.</span><span class="sxs-lookup"><span data-stu-id="317f1-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="317f1-109">Du kan ikke redigere feltet <STRONG>Overordnet</STRONG>, når du har gemt stadiet.</span><span class="sxs-lookup"><span data-stu-id="317f1-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="317f1-110">I stedet kan du slette posten og oprette den igen med et andet valg i feltet <STRONG>Overordnet</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="317f1-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="317f1-111">Du kan også kun oprette ét stadie med et tomt <STRONG>Overordnet</STRONG>-felt.</span><span class="sxs-lookup"><span data-stu-id="317f1-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="317f1-112">Det er altså kun tilladt at have ét begyndelsesstadie.</span><span class="sxs-lookup"><span data-stu-id="317f1-112">That is, only one initial stage is permitted.</span></span></P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]