---
title: Oprette serviceordrer automatisk
description: Du kan generere serviceordrer ud fra en serviceaftale for den serviceaftalens gyldighedsperiode.
author: ShylaThompson
ms.date: 05/01/2018
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
ms.openlocfilehash: 0b864aee332c82bc6b6845e7f9e425cfef377033
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824624"
---
# <a name="automatically-create-service-orders"></a><span data-ttu-id="14ffd-103">Oprette serviceordrer automatisk</span><span class="sxs-lookup"><span data-stu-id="14ffd-103">Automatically create service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="14ffd-104">Du kan generere serviceordrer ud fra en serviceaftale for den serviceaftalens gyldighedsperiode.</span><span class="sxs-lookup"><span data-stu-id="14ffd-104">You can generate service orders that are based on a service agreement for the valid period of the service agreement.</span></span>

<span data-ttu-id="14ffd-105">Alle de serviceordrer, du opretter ud fra en serviceaftale, knyttes til serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="14ffd-105">The service orders that you generate from a service agreement are all attached to the service agreement.</span></span>

<span data-ttu-id="14ffd-106">Serviceordrer oprettes automatisk ud fra følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="14ffd-106">Service orders are generated automatically from the following settings:</span></span>

  - <span data-ttu-id="14ffd-107">Det serviceaftaleinterval, der er angivet i serviceaftalelinjerne.</span><span class="sxs-lookup"><span data-stu-id="14ffd-107">The service agreement interval that is set up in the service agreement lines.</span></span> <span data-ttu-id="14ffd-108">Serviceaftaleintervallet angiver den hyppighed, serviceordrelinjer oprettes med.</span><span class="sxs-lookup"><span data-stu-id="14ffd-108">The service agreement interval indicates the frequency that service-order lines are created.</span></span> <span data-ttu-id="14ffd-109">Du kan finde flere oplysninger under [Serviceintervaller](service-intervals.md).</span><span class="sxs-lookup"><span data-stu-id="14ffd-109">For more information, see [Service intervals](service-intervals.md).</span></span>

  - <span data-ttu-id="14ffd-110">Den periode, som du angiver for at definere serviceperioden i felterne **Fra dato** og **Til dato** i formularen **Opret serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="14ffd-110">The period that you specify to define the service period in the **From date** and **To date** fields in the **Create service orders** form.</span></span> <span data-ttu-id="14ffd-111">Du kan finde flere oplysninger under [Oprette serviceordrer automatisk](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="14ffd-111">For more information, see [Create service orders automatically](create-service-orders-automatically.md).</span></span>

  - <span data-ttu-id="14ffd-112">Indstillingen **Kombiner serviceordrer** i sidehovedet for serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="14ffd-112">The **Combine service orders** option on the service agreement header.</span></span> <span data-ttu-id="14ffd-113">Denne indstilling angiver, om serviceordrelinjer, der er oprettet fra en serviceaftale, samler serviceordrer efter medarbejder, serviceopgave, serviceobjekt eller serviceaftale.</span><span class="sxs-lookup"><span data-stu-id="14ffd-113">This option defines whether service order lines generated from a service agreement, combines service orders according to employee, service task, service object, or service agreement.</span></span> <span data-ttu-id="14ffd-114">Du kan finde flere oplysninger under [Kombinere serviceordrer](combine-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="14ffd-114">For more information, see [Combine service orders](combine-service-orders.md).</span></span>

  - <span data-ttu-id="14ffd-115">Indstillingen **Tidsvindue** på serviceaftalelinjen.</span><span class="sxs-lookup"><span data-stu-id="14ffd-115">The **Time window** option on the service agreement line.</span></span> <span data-ttu-id="14ffd-116">I tidsvinduet defineres, hvor langt en servicelinje kan flyttes i forhold til den beregnede dato.</span><span class="sxs-lookup"><span data-stu-id="14ffd-116">The time window defines how far a service order line can move with regard to its calculated date.</span></span> <span data-ttu-id="14ffd-117">Du kan finde flere oplysninger under [Tidsvinduer](time-windows.md).</span><span class="sxs-lookup"><span data-stu-id="14ffd-117">For more information, see [Time windows](time-windows.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="14ffd-118">Hvis den dag, der er angivet for en serviceordre, ikke er åben i den kalender, du har valgt i formularen <STRONG>Parametre for servicestyring</STRONG>, modtager du en meddelelse om, at der er opstået en kalenderkonflikt.</span><span class="sxs-lookup"><span data-stu-id="14ffd-118">If the day that is specified for a service order is not open in the calendar that you have selected in the <STRONG>Service management parameters</STRONG> form, a message will indicate that there is a calendar conflict.</span></span> <span data-ttu-id="14ffd-119">Du kan blot ignorere meddelelsen. Serviceordren vil blive oprettet, selvom dagen er lukket i kalenderen.</span><span class="sxs-lookup"><span data-stu-id="14ffd-119">You can safely ignore the message; the service order will be created, even though the day is closed on the calendar.</span></span></P>

## <a name="example-1"></a><span data-ttu-id="14ffd-120">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="14ffd-120">Example 1</span></span>

<span data-ttu-id="14ffd-121">Serviceaftalen gælder fra 1. januar 2012 til 31. december 2012.</span><span class="sxs-lookup"><span data-stu-id="14ffd-121">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="14ffd-122">Hvis den serviceperiode, du angiver i formularen **Opret serviceordrer**, gælder fra den 1. november 2012 til den 1. februar 2013, oprettes der serviceordrer fra den 1. november 2012 til den 31. december 2012.</span><span class="sxs-lookup"><span data-stu-id="14ffd-122">If the service period that you specify in the **Create service orders** form is from November 1, 2012 until February 1, 2013, service orders are created from November 1, 2012 until December 31, 2012.</span></span>

## <a name="example-2"></a><span data-ttu-id="14ffd-123">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="14ffd-123">Example 2</span></span>

<span data-ttu-id="14ffd-124">Serviceaftalen gælder fra 1. januar 2012 til 31. december 2012.</span><span class="sxs-lookup"><span data-stu-id="14ffd-124">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="14ffd-125">Der knyttes to serviceaftalelinjer til serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="14ffd-125">Two service agreement lines are attached to the service agreement.</span></span> <span data-ttu-id="14ffd-126">Den første serviceaftalelinje har startdato den 2. januar 2012 og slutdato den 1. marts 2012.</span><span class="sxs-lookup"><span data-stu-id="14ffd-126">The first service agreement line has a starting date on January 2, 2012 and an ending date on March 1, 2012.</span></span> <span data-ttu-id="14ffd-127">Den anden serviceaftalelinje har startdato den 1. april 2012 og slutdato den 31. december 2012.</span><span class="sxs-lookup"><span data-stu-id="14ffd-127">The second service agreement line has a starting date on April 1, 2012 and an ending date on December 31, 2012.</span></span> <span data-ttu-id="14ffd-128">Du angiver en periode i formularen **Opret serviceordrer**, der går fra 1. oktober 2012 til 31. december 2012.</span><span class="sxs-lookup"><span data-stu-id="14ffd-128">You specify a period in the **Create service orders** form that is from October 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="14ffd-129">Derfor genereres der kun serviceordrer for den anden aftalelinje, da startdatoen og slutdatoen for den første aftalelinje ligger før den periode, du har angivet for serviceordren.</span><span class="sxs-lookup"><span data-stu-id="14ffd-129">Therefore, service orders are generated only for the second agreement line, because the starting date and ending date of the first agreement line are before the period that you specified for the service order.</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]