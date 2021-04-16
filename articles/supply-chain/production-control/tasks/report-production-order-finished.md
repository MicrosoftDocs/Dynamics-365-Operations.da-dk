---
title: Rapportere en produktionsordre som færdig
description: Denne procedure viser, hvordan du færdigmelder en produktionsordre.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9b676ffefa9fd4b8d66a5c35012630295f8a263
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828604"
---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="b0e0b-103">Rapportere en produktionsordre som færdig</span><span class="sxs-lookup"><span data-stu-id="b0e0b-103">Report a production order as finished</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0e0b-104">Denne procedure viser, hvordan du færdigmelder en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="b0e0b-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b0e0b-106">Dette er den sjette procedure ud af syv, der beskriver produktionsordrelivscyklussen.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="b0e0b-107">Rapportere en produktionsordre som færdig</span><span class="sxs-lookup"><span data-stu-id="b0e0b-107">Report a production order as finished</span></span>
1. <span data-ttu-id="b0e0b-108">Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="b0e0b-109">Vælg en produktionsordre, som har statussen Påbegyndt.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="b0e0b-110">Klik på Produktionsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="b0e0b-111">Klik på Færdigmelding.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-111">Click Report as finished.</span></span>
    * <span data-ttu-id="b0e0b-112">På denne side kan du bekræfte mængden af det færdige produkt, der skal færdigmeldes.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="b0e0b-113">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-113">Click the General tab.</span></span>
5. <span data-ttu-id="b0e0b-114">Indstil Antal gode til '18'.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="b0e0b-115">Indstil Antal fejl til '2'.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="b0e0b-116">Vælg 'Materiale' i feltet Fejlårsag.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="b0e0b-117">Markér eller fjern markering af afkrydsningsfeltet Slutkørsel.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="b0e0b-118">Markér eller fjern markeringen i afkrydsningsfeltet Accepter fejl.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="b0e0b-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="b0e0b-120">Bekræft færdigmeldingskladden</span><span class="sxs-lookup"><span data-stu-id="b0e0b-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="b0e0b-121">Klik på Vis i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="b0e0b-122">Klik på Færdigmeldt.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="b0e0b-123">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b0e0b-124">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b0e0b-125">Færdigmeldingskladden bogføres.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="b0e0b-126">Hvis du vil foretage ændringer i kladden, kan du oprette en ny kladde, hvor du kan foretage ændringer manuelt.</span><span class="sxs-lookup"><span data-stu-id="b0e0b-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]