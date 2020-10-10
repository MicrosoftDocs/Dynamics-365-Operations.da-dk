---
title: Beregn varebudget
description: Dette emne beskriver, hvordan du beregner varebudget i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f8f38ac7bfb270f648cd561da50ee5477721ab47
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888707"
---
# <a name="calculate-item-forecast"></a><span data-ttu-id="65f6a-103">Beregn varebudget</span><span class="sxs-lookup"><span data-stu-id="65f6a-103">Calculate item forecast</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="65f6a-104">Ligesom du kan foretage kapacitetsbelastningsberegninger, som er beskrevet i forrige afsnit, kan du også foretage beregninger af varebudgettet på:</span><span class="sxs-lookup"><span data-stu-id="65f6a-104">Just as you can make capacity load calculations, which are described in the previous section, you can also make item forecast calculations on:</span></span>

- <span data-ttu-id="65f6a-105">vedligeholdelsestidsplanslinjer</span><span class="sxs-lookup"><span data-stu-id="65f6a-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="65f6a-106">arbejdsordrer, der endnu ikke er planlagt</span><span class="sxs-lookup"><span data-stu-id="65f6a-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="65f6a-107">planlagte arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="65f6a-107">scheduled work orders</span></span>

<span data-ttu-id="65f6a-108">Dette er nyttigt, hvis du vil have en oversigt over forventet vareforbrug (reservedele og andre varer, der kræves for at udføre arbejdsordrer) i en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="65f6a-108">This is useful if you want to get an overview of expected item consumption (spare parts as well as other items required for completing work orders) for a specific period.</span></span> <span data-ttu-id="65f6a-109">Beregning af varebudget kan foretages på alle aktiver eller udvalgte aktiver.</span><span class="sxs-lookup"><span data-stu-id="65f6a-109">Calculation of item forecast can be done on all assets or selected assets.</span></span> <span data-ttu-id="65f6a-110">Du kan også foretage en beregning på en aktivitet for vedligeholdelsesnedetid (**Alle aktiviteter for vedligeholdelsesnedetid** eller **Aktive aktiviteter for vedligeholdelsesnedetid**) eller på en arbejdsordrepulje (**Alle arbejdsordrepuljer** eller **Aktive arbejdsordre puljer**).</span><span class="sxs-lookup"><span data-stu-id="65f6a-110">You can also make a calculation on a maintenance downtime activity (**All maintenance downtime activities** or **Active maintenance downtime activities**), or on a work order pool (**All work order pools** or **Active work order pools**).</span></span>

1. <span data-ttu-id="65f6a-111">Klik på **Styring af aktiver** > **Forespørgsler** > **Varebudget** eller **Styring af aktiver** > **Generelt** > **Arbejdsordrepuljer** > **Alle arbejdsordrepuljer** / **Aktive arbejdsordrepuljer** > vælg arbejdsordrepulje på listen > knappen **Varebudget** eller **Styring af aktiver** > **Generelt** > **Aktiviteter med vedligeholdelsesnedetid** > **Alle aktiviteter med vedligeholdelsesnedetid** / **Aktive aktiviteter med vedligeholdelsesnedetid** > vælg aktivitet for vedligeholdelsesnedetid på listen > knappen **Varebudget**.</span><span class="sxs-lookup"><span data-stu-id="65f6a-111">Click **Asset management** > **Inquiries** > **Item forecast**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Item forecast** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance downtime activity in the list > **Item forecast** button.</span></span>

2. <span data-ttu-id="65f6a-112">Vælg en periode til beregningen i felterne **Startdato/-klokkeslæt** og **Slutdato/-klokkeslæt** i dialogboksen **Beregn varebudget**.</span><span class="sxs-lookup"><span data-stu-id="65f6a-112">In the **Calculate item forecast** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="65f6a-113">Vælg "Ja" på knappen **Medtag vedligeholdelsestidsplan**, hvis du vil medtage vedligeholdelsestidsplanlinjer i budgetberegningen.</span><span class="sxs-lookup"><span data-stu-id="65f6a-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the forecast calculation.</span></span>

4. <span data-ttu-id="65f6a-114">Vælg "Ja" på knappen **Medtag arbejdsordre**, hvis du vil medtage arbejdsordrejob i budgetberegningen.</span><span class="sxs-lookup"><span data-stu-id="65f6a-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the forecast calculation.</span></span>

5. <span data-ttu-id="65f6a-115">Du kan bruge feltet **Niveau** til at angive, hvor detaljerede varebudgetlinjerne skal være i forbindelse med arbejdssteder.</span><span class="sxs-lookup"><span data-stu-id="65f6a-115">You can use the **Level** field to indicate how detailed you want the item forecast lines to be regarding functional locations.</span></span> 

      <span data-ttu-id="65f6a-116">Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle vedligeholdelsestidsplanslinjer og arbejdsordrer for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau.</span><span class="sxs-lookup"><span data-stu-id="65f6a-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
  
      <span data-ttu-id="65f6a-117">Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle vedligeholdelsestidsplanlinjer og alle arbejdsordrer på alle de arbejdsstedsniveauer, de er relateret til.</span><span class="sxs-lookup"><span data-stu-id="65f6a-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="65f6a-118">Klik på **OK** for at starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="65f6a-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="65f6a-119">I **Sammenlæg pr.**-grupperne skal du klikke på de relevante knapper for at få vist det nødvendige detaljeringsniveau i beregningen.</span><span class="sxs-lookup"><span data-stu-id="65f6a-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="65f6a-120">I skærmbilledet nedenfor fremhæves de valgte **Sammenlæg pr.**-knapper med blå farve.</span><span class="sxs-lookup"><span data-stu-id="65f6a-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="65f6a-121">Klik på en knap for at aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="65f6a-121">Click on a button to activate or deactivate it.</span></span>

8. <span data-ttu-id="65f6a-122">Klik på knappen **Vis dimensioner**, hvis du vil se de produkt-, lagrings- eller sporingsdimensioner, der er relateret til varerne.</span><span class="sxs-lookup"><span data-stu-id="65f6a-122">Click the **Display dimensions** button if you want to see the product, storage, or tracking dimensions related to the items.</span></span> <span data-ttu-id="65f6a-123">Markér relevante afkrydsningsfelter, og klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="65f6a-123">Select the relevant check boxes, and click **OK**.</span></span>

![Figur 1](media/02-capacity-planning.png)
