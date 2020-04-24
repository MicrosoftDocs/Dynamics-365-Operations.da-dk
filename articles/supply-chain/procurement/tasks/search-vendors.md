---
title: Søge efter kreditorer
description: Lær at søge efter leverandører ud fra bestemte kriterier.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendSearchCriterion, VendSearchAddCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dda8cfa55809ebeeda695d02ed5f99e493325c3b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207571"
---
# <a name="search-for-vendors"></a><span data-ttu-id="c1130-103">Søge efter kreditorer</span><span class="sxs-lookup"><span data-stu-id="c1130-103">Search for vendors</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1130-104">Lær at søge efter leverandører ud fra bestemte kriterier.</span><span class="sxs-lookup"><span data-stu-id="c1130-104">Learn how to search for vendors based on specific criteria.</span></span> <span data-ttu-id="c1130-105">Dette eksempel viser, hvordan du kan søge efter leverandører, der er godkendt til en bestemt indkøbskategori og har deres primære adresse i et bestemt land.</span><span class="sxs-lookup"><span data-stu-id="c1130-105">This example shows you how to search for vendors that are approved for a particular procurement category and have their primary address in a specific country.</span></span> <span data-ttu-id="c1130-106">Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.</span><span class="sxs-lookup"><span data-stu-id="c1130-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="c1130-107">Denne opgave vil normalt udføres af en professionel indkøb.</span><span class="sxs-lookup"><span data-stu-id="c1130-107">This task would usually be carried out by a procurement professional.</span></span>

1. <span data-ttu-id="c1130-108">Gå til Indkøb og forsyning > Kreditorer > Kreditorsøgning.</span><span class="sxs-lookup"><span data-stu-id="c1130-108">Go to Procurement and sourcing > Vendors > Vendor search.</span></span>
2. <span data-ttu-id="c1130-109">Klik på ikonet Plus for at åbne siden Valg af indkøbskategori.</span><span class="sxs-lookup"><span data-stu-id="c1130-109">Click on the Plus icon to open the Procurement category selection page.</span></span>  
3. <span data-ttu-id="c1130-110">Vælg "FIRMAS INDKØBSKATEGORIER\KONTORMASKINER" i træet.</span><span class="sxs-lookup"><span data-stu-id="c1130-110">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'.</span></span>
    * <span data-ttu-id="c1130-111">Hvis du kører denne procedure som en opgaveguide, skal du eventuelt klikke på knappen Lås op, før du kan vælge den korrekte node.</span><span class="sxs-lookup"><span data-stu-id="c1130-111">If you're running this procedure as a task guide, you may have to click the Unlock button before you can select the correct node.</span></span> <span data-ttu-id="c1130-112">Hvis du ikke bruger USMF, kan du vælge en af de kategorier, du har.</span><span class="sxs-lookup"><span data-stu-id="c1130-112">If you're not using USMF, select one of the categories that you have.</span></span>  
4. <span data-ttu-id="c1130-113">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="c1130-113">Click Add.</span></span>
    * <span data-ttu-id="c1130-114">Det er muligt at vælge mere end én kategori her.</span><span class="sxs-lookup"><span data-stu-id="c1130-114">It's possible to select more than one category here.</span></span> <span data-ttu-id="c1130-115">Hvis du gør det, finder søgningen alle kreditorer, der er godkendt til mindst én af kategorierne.</span><span class="sxs-lookup"><span data-stu-id="c1130-115">If you do so, the search will find all the vendors that are approved for at least one of the categories.</span></span>  
5. <span data-ttu-id="c1130-116">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c1130-116">Click OK.</span></span>
6. <span data-ttu-id="c1130-117">Indtast en værdi i feltet Land/område.</span><span class="sxs-lookup"><span data-stu-id="c1130-117">In the Country/region field, type a value.</span></span>
7. <span data-ttu-id="c1130-118">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c1130-118">Click OK.</span></span>

