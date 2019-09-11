---
title: Arbejdsordrer og anlægsaktiver
description: Dette emne beskriver arbejdsordrer og anlægsaktiver i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f03b7fa073c4e5338b7b5681ba7b8c9fe00a657b
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875561"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="a208f-103">Arbejdsordrer og anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="a208f-103">Work orders and fixed assets</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="a208f-104">I Styring af aktiver kan aktiver knyttes til anlægsaktiver, og du kan oprette arbejdsordrer for disse aktiver.</span><span class="sxs-lookup"><span data-stu-id="a208f-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="a208f-105">Hvis du bruger denne funktion, kan du få en komplet oversigt over anlægsaktiver, relaterede investeringsprojekter og de omkostninger, der er registreret for investeringsprojekterne i modulet **Projektstyring og regnskab**, og modulet **Anlægsaktiver** i Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a208f-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs registered on the investment projects in the **Project management and accounting** module and the **Fixed assets** module in Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="a208f-106">Feltet **Nummer på anlægsaktiv** udfyldes kun på arbejdsordrejobprojektet, hvis typen "Investering" er valgt som projekttypen for arbejdsordrejobprojektet.</span><span class="sxs-lookup"><span data-stu-id="a208f-106">The **Fixed asset number** field is only filled out on the work order job project if type "Investment" is selected as the project type on the work order job project.</span></span>

![Figur 1](media/24-work-orders.png)

<span data-ttu-id="a208f-108">Følgende procedure beskriver relationen mellem aktiverne, arbejdsordrerne, arbejdsordrejobprojekter og anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="a208f-108">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="a208f-109">Du opretter et aktiv, som du relaterer til et anlægsaktiv, som vist på nedenstående illustration.</span><span class="sxs-lookup"><span data-stu-id="a208f-109">You create an asset that you relate to a fixed asset, as shown in the figure below.</span></span>

![Figur 2](media/25-work-orders.png)

2. <span data-ttu-id="a208f-111">Når du opretter arbejdsordretyper (**Styring af aktiv** > **Opsætning** > **Arbejdsordrer** > **Arbejdsordretyper**), skal du oprette en arbejdsordre type til håndtering af investeringer.</span><span class="sxs-lookup"><span data-stu-id="a208f-111">When you set up work order types (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="a208f-112">Se også [Arbejdsordretyper](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="a208f-112">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![Figur 3](media/26-work-orders.png)

3. <span data-ttu-id="a208f-114">Når du opretter projektgrupper for arbejdsordrer (**Styring af aktiver** > **Opsætning** > **Arbejdsordrer** > **Opsætning af projekt** > **Projektgruppe**-linket), opretter du en relation mellem den arbejdsordretype, der bruges til investeringer, og den projektgruppe, der er oprettet for investeringer i modulet **Projektstyring og regnskab** (**Projektstyring og regnskab** > **Opsætning** > **Bogføring** > **Projektgrupper**).</span><span class="sxs-lookup"><span data-stu-id="a208f-114">When you set up work order project groups (**Asset management** > **Setup** > **Work orders** > **Project setup** > **Project group** link), you create a relation between the work order type used for investments and the project group created for investments in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![Figur 4](media/27-work-orders.png)

4. <span data-ttu-id="a208f-116">Når du opretter en arbejdsordre, der vedrører et anlægsaktivobjekt, skal du vælge den type arbejdsordre, der bruges til håndtering af investeringer, f.eks. "Investering".</span><span class="sxs-lookup"><span data-stu-id="a208f-116">When you create a work order that relates to a fixed asset object, you select the work order type used for handling investments, for example, "Investment".</span></span>

5. <span data-ttu-id="a208f-117">Når arbejdsordren oprettes, vises den relaterede arbejdsordretype i **Alle arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a208f-117">When the work order is created, the related work order type is shown in **All work orders**.</span></span>

![Figur 5](media/28-work-orders.png)

6. <span data-ttu-id="a208f-119">Når arbejdsordren oprettes, oprettes det projekt, der er relateret til arbejdsordren, i **Projektstyring og regnskab** > **Alle projekter**.</span><span class="sxs-lookup"><span data-stu-id="a208f-119">When the work order is created, the project related to the work order is created in **Project management and accounting** > **All projects**.</span></span> <span data-ttu-id="a208f-120">Du kan få vist projektrelaterede oplysninger ved at klikke på **Projekt-id**-linket i arbejdsordren (i **Styring af aktiver** skal du åbne arbejdsordren i visningen Detaljer > oversigtspanelet **Linjedetaljer** > **Generelt** > feltet **Projekt-id**).</span><span class="sxs-lookup"><span data-stu-id="a208f-120">You can see project-related information by clicking the **Project ID** link on the work order (in **Asset management**, open the work order in Details view > **Line details** FastTab > **General** tab > **Project ID** field).</span></span>

![Figur 6](media/29-work-orders.png)

7. <span data-ttu-id="a208f-122">I **Anlægsaktiver** kan du få vist en oversigt over de projekter, der er knyttet til et anlægsaktiv (**Anlægsaktiver** > **Anlægsaktiver** > **Anlægsaktiver** > klik på anlægsaktivet i **Nummer på anlægsaktiv**-feltet > se indholdet i ruden **Relaterede oplysninger** > sektionen **Tilknyttede projekter**).</span><span class="sxs-lookup"><span data-stu-id="a208f-122">In **Fixed assets**, you are able to see an overview of the projects associated with a fixed asset (**Fixed assets** > **Fixed assets** > **Fixed assets** > click on the fixed asset in the **Fixed asset number** field > view the contents in the **Related information** pane > **Associated projects** section).</span></span>

