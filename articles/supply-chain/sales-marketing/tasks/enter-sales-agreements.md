--- 
title: "Indgå salgsaftaler"
description: "Denne procedure viser, hvordan du opretter en salgsaftale, der forpligter en af dine kunder til at købe et produkt for et aftalt beløb over en tidsperiode mod at få særlige rabatter."
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 965826f5fddc2f53f33157434929eb265979376e
ms.openlocfilehash: 025c9fe2f769f37b63bd79c6c3afedc31a955310
ms.contentlocale: da-dk
ms.lasthandoff: 09/17/2018

---
# <a name="enter-sales-agreements"></a><span data-ttu-id="614ec-103">Indgå salgsaftaler</span><span class="sxs-lookup"><span data-stu-id="614ec-103">Enter sales agreements</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="614ec-104">Denne procedure viser, hvordan du opretter en salgsaftale, der forpligter en af dine kunder til at købe et produkt for et aftalt beløb over en tidsperiode mod at få særlige rabatter.</span><span class="sxs-lookup"><span data-stu-id="614ec-104">This procedure shows you how to create a sales agreement that commits one of your customers to buy a product for an agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="614ec-105">Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.</span><span class="sxs-lookup"><span data-stu-id="614ec-105">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="614ec-106">Konfigurere salgsaftaleoverskrift</span><span class="sxs-lookup"><span data-stu-id="614ec-106">Set up sales agreement header</span></span>
1. <span data-ttu-id="614ec-107">Gå til salg og marketing > Salgsaftaler > Salgsaftaler.</span><span class="sxs-lookup"><span data-stu-id="614ec-107">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="614ec-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="614ec-108">Click New.</span></span>
3. <span data-ttu-id="614ec-109">Klik på rullelisten i feltet Kundekonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="614ec-109">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="614ec-110">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="614ec-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="614ec-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="614ec-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="614ec-112">Klik på rullelisten i feltet Salgsaftaleklassifikation for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="614ec-112">In the Sales agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="614ec-113">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="614ec-113">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="614ec-114">Udvid afsnittet Generelt.</span><span class="sxs-lookup"><span data-stu-id="614ec-114">Expand the General section.</span></span>
9. <span data-ttu-id="614ec-115">Vælg "Bundet produktværdi" i feltet Standardtilsagn.</span><span class="sxs-lookup"><span data-stu-id="614ec-115">In the Default commitment field, select 'Product value commitment'.</span></span>
    * <span data-ttu-id="614ec-116">En tilsagnstype er et obligatorisk kriterium, som du skal tildele til aftalen for at definere, hvordan aftalekontrakten skal opfyldes.</span><span class="sxs-lookup"><span data-stu-id="614ec-116">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="614ec-117">Med de fire foruddefinerede typer kan du angive kundens tilsagnsmål udtrykt som en mængde eller værdi.</span><span class="sxs-lookup"><span data-stu-id="614ec-117">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="614ec-118">Mængdetilsagnstypen kan kun anvendes på et bestemt produkt, men de værdibaserede typerne gælder for salget af specifikke og ikke-specifikke produkter.</span><span class="sxs-lookup"><span data-stu-id="614ec-118">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
10. <span data-ttu-id="614ec-119">Indstil datoen i feltet Udløbsdato til en fremtidig dato, hvor du vil have, at aftalen udløber.</span><span class="sxs-lookup"><span data-stu-id="614ec-119">In the Expiration date field, set the date to a future date when you want the agreement to expire.</span></span>
11. <span data-ttu-id="614ec-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="614ec-120">Click OK.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="614ec-121">Konfigurere bundede produktværdilinjer</span><span class="sxs-lookup"><span data-stu-id="614ec-121">Set up product value commitment lines</span></span>
1. <span data-ttu-id="614ec-122">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="614ec-122">Click Add line.</span></span>
2. <span data-ttu-id="614ec-123">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="614ec-123">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="614ec-124">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="614ec-124">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="614ec-125">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="614ec-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="614ec-126">Tilsagnstypen, som du har valgt til denne aftale, påvirker, hvilken type oplysninger du kan angive for aftalelinjerne.</span><span class="sxs-lookup"><span data-stu-id="614ec-126">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="614ec-127">For en værdibaseret aftale skal du for eksempel angive det samlede nettobeløb (i den aftalte valuta), som kunden giver tilsagn om at købe varer fra dig for.</span><span class="sxs-lookup"><span data-stu-id="614ec-127">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="614ec-128">I dette eksempel er felterne Antal og Enhed på linjen ikke tilgængelige, fordi du opretter en aftale for kunden om at købe en bestemt værdi af et produkt.</span><span class="sxs-lookup"><span data-stu-id="614ec-128">In this example the Quantity and Unit fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
5. <span data-ttu-id="614ec-129">Angiv det pengebeløb, som kunden har forpligtet sig til at købe for, i feltet Nettobeløb.</span><span class="sxs-lookup"><span data-stu-id="614ec-129">In the Net amount field, enter the monetary amount that the customer has committed to buying.</span></span>
6. <span data-ttu-id="614ec-130">Angiv en værdi i procent, som skal gælde for kundens salgsordrelinjer, der er knyttet til denne aftale, i feltet Rabatprocent.</span><span class="sxs-lookup"><span data-stu-id="614ec-130">In the Discount percent field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
7. <span data-ttu-id="614ec-131">Vis eller skjul sektionen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="614ec-131">Expand the Line details section.</span></span>
8. <span data-ttu-id="614ec-132">Vælg Ja i feltet Maks. gennemtvinges.</span><span class="sxs-lookup"><span data-stu-id="614ec-132">Select Yes in the Max is enforced field.</span></span>
    * <span data-ttu-id="614ec-133">Hvis du vælger Maks. gennemtvinges betyder det, at det samlede beløb for alle de salgsordrelinjer, der bruger tilsagnets specielle priser, rabatter og/eller betalingsbetingelser, ikke må overstige det beløb, der er angivet i tilsagnet.</span><span class="sxs-lookup"><span data-stu-id="614ec-133">Selecting Max is enforced means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    * <span data-ttu-id="614ec-134">Minimum- og maksimumfrigivelsesbeløbet angiver et interval af værdier, der skal sælges på hver salgsordre, der bruger den valgte aftale.</span><span class="sxs-lookup"><span data-stu-id="614ec-134">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
9. <span data-ttu-id="614ec-135">Udvid sektionen Salgsaftaleoverskrift.</span><span class="sxs-lookup"><span data-stu-id="614ec-135">Expand the Sales agreement header section.</span></span>
    * <span data-ttu-id="614ec-136">Medmindre aftalens status er indstillet til Gældende, kan salgsordrer ikke knyttes til aftalen og kan derfor ikke bidrage til opfyldelsen af denne aftale.</span><span class="sxs-lookup"><span data-stu-id="614ec-136">Unless the status of the agreement is set to Effective, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="614ec-137">Du kan ændre statussen manuelt på dette trin.</span><span class="sxs-lookup"><span data-stu-id="614ec-137">You can change the status manually at this stage.</span></span> <span data-ttu-id="614ec-138">Status vil dog normalt ændres, når du bekræfter aftalen for kunden.</span><span class="sxs-lookup"><span data-stu-id="614ec-138">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
10. <span data-ttu-id="614ec-139">Klik på Salgsaftale i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="614ec-139">On the Action Pane, click Sales agreement.</span></span>
11. <span data-ttu-id="614ec-140">Klik på Bekræftelse.</span><span class="sxs-lookup"><span data-stu-id="614ec-140">Click Confirmation.</span></span>
    * <span data-ttu-id="614ec-141">Kontrollér, at indstillingen Markér aftale som gældende er sat til Ja.</span><span class="sxs-lookup"><span data-stu-id="614ec-141">Make sure that the Mark agreement as effective option is set to Yes.</span></span>  
12. <span data-ttu-id="614ec-142">Vælg Ja i feltet Udskriv rapport.</span><span class="sxs-lookup"><span data-stu-id="614ec-142">Select Yes in the Print report field.</span></span>
13. <span data-ttu-id="614ec-143">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="614ec-143">Click OK.</span></span>
14. <span data-ttu-id="614ec-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="614ec-144">Close the page.</span></span>
    * <span data-ttu-id="614ec-145">Aftalen er nu gældende, og du kan begynde at tilknytte kundens ordrer til aftalen for at modpostere mod tilsagnsmålet.</span><span class="sxs-lookup"><span data-stu-id="614ec-145">The agreement is now effective and you can start linking the customer's orders to the agreement, to offset against the committed target.</span></span>  


