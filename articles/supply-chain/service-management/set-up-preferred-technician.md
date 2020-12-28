---
title: Konfigurere en foretrukket tekniker
description: Du kan vælge enhver arbejder som en foretrukket tekniker til en serviceaftale eller serviceordre.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 850d91372fb1a918840ebc316a4479f4a70bdc24
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424306"
---
# <a name="set-up-a-preferred-technician"></a><span data-ttu-id="fde02-103">Konfigurere en foretrukket tekniker</span><span class="sxs-lookup"><span data-stu-id="fde02-103">Set up a preferred technician</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="fde02-104">Du kan vælge enhver arbejder som en foretrukket tekniker til en serviceaftale eller serviceordre.</span><span class="sxs-lookup"><span data-stu-id="fde02-104">You can select any worker as a preferred technician for a service agreement or service order.</span></span> <span data-ttu-id="fde02-105">Det er dog en god idé at føje arbejderen til et relevant planlægningsteam, så arbejderen er medtaget på **Planlægningstavle**.</span><span class="sxs-lookup"><span data-stu-id="fde02-105">However, it is a good idea to add the worker to the appropriate dispatch team so that the worker is included on the **Dispatch board**.</span></span>

## <a name="assign-employee-to-a-dispatch-team"></a><span data-ttu-id="fde02-106">Knytte en medarbejder til et planlægningsteam</span><span class="sxs-lookup"><span data-stu-id="fde02-106">Assign employee to a dispatch team</span></span>

1.  <span data-ttu-id="fde02-107">Klik på **Personale** \> **Generelt** \> **Arbejdere** \> **Arbejdere**.</span><span class="sxs-lookup"><span data-stu-id="fde02-107">Click **Human resources** \> **Common** \> **Workers** \> **Workers**.</span></span> <span data-ttu-id="fde02-108">Dobbeltklik på en arbejder for at åbne arbejderens side med detaljer.</span><span class="sxs-lookup"><span data-stu-id="fde02-108">Double-click a worker to open the worker details page.</span></span> <span data-ttu-id="fde02-109">I **handlingsruden** skal du klikke på **Opsætning** \> **Planlægningsteam** for at åbne formularen **Planlæg medarbejdere**.</span><span class="sxs-lookup"><span data-stu-id="fde02-109">On the **Action Pane**, click **Setup** \>**Dispatch team** to open the **Dispatch workers** form.</span></span>

2.  <span data-ttu-id="fde02-110">Vælg det team, der skal tilknyttes arbejderen, i feltet **Planlægningsteam**.</span><span class="sxs-lookup"><span data-stu-id="fde02-110">In the **Dispatch team** field, select the team to assign the worker to.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a><span data-ttu-id="fde02-111">Knytte en foretrukken tekniker til en serviceaftale</span><span class="sxs-lookup"><span data-stu-id="fde02-111">Assign a preferred technician to a service agreement</span></span>

1.  <span data-ttu-id="fde02-112">Klik på **Servicestyring** \> **Almindelige** \> **Serviceaftaler** \> **Serviceaftaler**.</span><span class="sxs-lookup"><span data-stu-id="fde02-112">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="fde02-113">Dobbeltklik på en serviceaftale for at åbne formen med detaljer.</span><span class="sxs-lookup"><span data-stu-id="fde02-113">Double-click a service agreement to open the details form.</span></span>

2.  <span data-ttu-id="fde02-114">Under fanen **Generelt** skal du vælge feltet **Foretrukken tekniker** for at knytte et medlem af det relevante planlægningsteam til serviceaftalen som den foretrukne tekniker.</span><span class="sxs-lookup"><span data-stu-id="fde02-114">On the **General** tab, select the **Preferred technician** field, and then select a member of the appropriate dispatch team as the preferred technician for the service agreement.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-order"></a><span data-ttu-id="fde02-115">Knytte en foretrukken tekniker til en serviceordre</span><span class="sxs-lookup"><span data-stu-id="fde02-115">Assign a preferred technician to a service order</span></span>

1.  <span data-ttu-id="fde02-116">Klik på **Servicestyring** \> **Periodisk** \> **Planlægningstavle**.</span><span class="sxs-lookup"><span data-stu-id="fde02-116">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="fde02-117">I formularen <STRONG>Planlægningstavle</STRONG> skal du angive et datointerval til de planlægningsaktiviteter, du vil have vist.</span><span class="sxs-lookup"><span data-stu-id="fde02-117">In the <STRONG>Dispatch board</STRONG> form, specify a date range for dispatch activities to view.</span></span> <span data-ttu-id="fde02-118">Angiv også, om lukkede aktiviteter skal vises, og om planlægningsaktivitetslisten skal begrænses til teams, som du tilhører, eller som du er bemyndiget til at overvåge.</span><span class="sxs-lookup"><span data-stu-id="fde02-118">Also, specify whether to display closed activities and whether to limit the dispatch activity list to teams that you belong to or are authorized to monitor.</span></span> <span data-ttu-id="fde02-119">Klik på <STRONG>OK</STRONG> for at åbne formularen <STRONG>Planlægningstavle</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="fde02-119">Click <STRONG>OK</STRONG> to open the <STRONG>Dispatch board</STRONG>.</span></span></P>



2.  <span data-ttu-id="fde02-120">Markér linjen for den serviceaktivitet, du vil redigere.</span><span class="sxs-lookup"><span data-stu-id="fde02-120">Select the line of the service activity to modify.</span></span>

3.  <span data-ttu-id="fde02-121">Vælg fanen **Relateret**, og brug listen **Arbejder** til at tilknytte et medlem af det relevante planlægningsteam som den foretrukne tekniker til servicebesøget.</span><span class="sxs-lookup"><span data-stu-id="fde02-121">On the **Related** tab, use the **Worker** list to assign a member of the appropriate dispatch team as the preferred technician for the service call.</span></span>

## <a name="see-also"></a><span data-ttu-id="fde02-122">Se også</span><span class="sxs-lookup"><span data-stu-id="fde02-122">See also</span></span>

[<span data-ttu-id="fde02-123">Oversigt over udvikling og udfyldelse af serviceaftaler</span><span class="sxs-lookup"><span data-stu-id="fde02-123">Develop and establish service agreements overview</span></span>](service-agreements.md)

[<span data-ttu-id="fde02-124">Oprette serviceordrer manuelt</span><span class="sxs-lookup"><span data-stu-id="fde02-124">Create service orders manually</span></span>](create-service-orders-manually.md)

<span data-ttu-id="fde02-125">[Serviceaftaler (form)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="fde02-125">[Service agreements (form)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span></span>
  


